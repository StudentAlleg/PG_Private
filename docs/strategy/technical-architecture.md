# Technical Architecture and Stack Decisions

## System Architecture

```
                         +-----------------+
                         |   User / Firm   |
                         |   Employee or   |
                         |     Client      |
                         +--------+--------+
                                  |
                    +-------------+-------------+
                    |                           |
             +------+------+           +-------+-------+
             | MS Teams /  |           |  Standalone   |
             | Copilot     |           |  Web UI       |
             +------+------+           +-------+-------+
                    |                           |
                    +-------------+-------------+
                                  |
                         +--------+--------+
                         |  Super Agent /  |
                         |    Copilot      |
                         |  (Formatter)    |
                         +--------+--------+
                                  |
                         +--------+--------+
                         |  Orchestrator   |
                         |  (Router /      |
                         |   Dispatcher)   |
                         +--------+--------+
                                  |
              +-------------------+-------------------+
              |                   |                   |
     +--------+--------+ +------+-------+ +---------+-------+
     |  Firm Agent     | |Client Agent  | | Document Agent  |
     | (firm-level)    | |(per-client)  | | (SOPs, memos)   |
     +--------+--------+ +------+-------+ +---------+-------+
              |                   |                   |
              |          +-------+-------+            |
              |          | Payroll Agent |            |
              |          | (Payroll data)|            |
              |          +-------+-------+            |
              |                   |                   |
     +--------+-------------------+-------------------+--------+
     |                    MCP Tool Layer                        |
     |  (Each agent calls tools via MCP protocol)              |
     +--------+-------------------+-------------------+--------+
              |                   |                   |
     +--------+--------+ +------+-------+ +---------+-------+
     |  QBO MCP Server | | Gusto MCP    | | RAG MCP Server  |
     |                 | | Server       | | (Vector Search) |
     +---------+-------+ +------+-------+ +---------+-------+
               |                 |                   |
               +--------+-------+-------------------+
                        |
               +--------+--------+
               |  Data Lakehouse |
               |  (DuckLake)     |
               |  Bronze/Silver/ |
               |  Gold           |
               +--------+--------+
                        |
        +---------------+---------------+
        |               |               |
   +----+----+    +-----+-----+   +----+----+
   |QuickBooks|   |   Gusto   |   |  Xero   |
   | Online   |   |  Payroll  |   |         |
   +----------+   +-----------+   +---------+
```

## Technology Stack

### Chosen Technologies

| Component | Technology | Alternatives Considered | Rationale |
|-----------|-----------|------------------------|-----------|
| **Agent Framework** | LangGraph | AutoGen, CrewAI, Semantic Kernel | Already prototyped; graph-based control flow matches our orchestration model; production features (persistence, streaming, time travel) |
| **Agent Protocol** | MCP (Model Context Protocol) | Custom REST APIs, LangChain tools only | Industry standard; platform-agnostic; thousands of community servers; Anthropic-backed |
| **LLM (Development)** | Local via Docker Model Runner (Gemma 3) | Ollama | Already configured; free; no API key needed |
| **LLM (Production)** | GPT-4o-mini or Claude 3.5 Sonnet | Gemini 1.5 Flash, local models | Best cost/quality tradeoff for financial reasoning; benchmarking framework enables easy comparison |
| **Data Lakehouse (MVP)** | DuckDB + DuckLake | SQLite, Postgres, Databricks | Zero infrastructure; local-first; ACID; time travel; graduates to cloud later |
| **Data Lakehouse (Prod)** | Databricks Delta Lake | Snowflake, BigQuery | Best governance, multi-tenant isolation, and financial-grade compliance |
| **Vector Database (MVP)** | ChromaDB | pgvector | Simplest setup for prototyping; embedded mode; pip install and go |
| **Vector Database (Prod)** | Qdrant or Pinecone | Weaviate, Milvus | Qdrant for self-hosted control; Pinecone for zero-ops managed service |
| **Observability** | OpenTelemetry + OpenLIT | Langfuse, custom sinks | Vendor-neutral standard; existing sink architecture is compatible |
| **Auth (MVP)** | Simple API key / session | OAuth 2.0 | Sufficient for single-firm beta; upgrade later |
| **Auth (Prod)** | OAuth 2.0 + Azure AD / Google Identity | Auth0, Clerk | Must integrate with firm's existing identity provider |
| **Web Framework** | FastAPI or Streamlit (MVP) | Flask, Django, Next.js | FastAPI for API-first; Streamlit for rapid prototype UI |
| **Deployment (MVP)** | Local / single VPS | Docker Compose | Simplest path; no Kubernetes until multi-tenant |
| **Deployment (Prod)** | Azure (if Microsoft-first) or AWS | GCP | Azure if we commit to Microsoft surface; AWS as neutral alternative |

### Build vs Buy Analysis

| Component | Build | Buy | Decision | Rationale |
|-----------|-------|-----|----------|-----------|
| Agent orchestration | LangGraph (open source) | LangGraph Cloud | **Build on open source** | Control, cost, already prototyped |
| Data lakehouse | DuckLake (open source) | Databricks managed | **Build now, buy later** | Free for MVP; managed when multi-tenant |
| Vector database | ChromaDB (open source) | Pinecone managed | **Build now, buy later** | Free for MVP; managed when latency matters |
| QuickBooks integration | Custom Python + SDK | Unified API (Merge, Rutter) | **Build custom first** | Learn the data model deeply; consider unified APIs later for speed |
| Chat UI | Custom (Streamlit/FastAPI) | Vercel AI SDK, Chainlit | **Evaluate both** | Custom for control; off-the-shelf if faster |
| Monitoring | OpenTelemetry (open source) | Datadog, New Relic | **Build on open source** | Vendor-neutral; export to any backend |
| Auth | Custom OAuth | Auth0, Clerk | **Buy when needed** | Not worth building auth from scratch |

## MCP Strategy

MCP is the architectural decision that enables platform independence and clean separation of concerns.

### MCP Server Design

Each data source and capability gets its own MCP server:

| MCP Server | Tools It Exposes | Data Source |
|------------|-----------------|-------------|
| `accounting-mcp` | `query_journal_entries`, `get_account_balance`, `get_trial_balance`, `get_invoice` | Lakehouse (silver/gold layer) |
| `payroll-mcp` | `get_employee_list`, `get_payroll_run`, `get_pay_stub` | Lakehouse (silver/gold layer) |
| `document-mcp` | `search_documents`, `get_document`, `search_policies` | Vector database (RAG) |
| `analytics-mcp` | `get_monthly_pnl`, `compare_periods`, `get_client_summary` | Lakehouse (gold layer) |

### Why MCP Servers Query the Lakehouse, Not Vendor APIs Directly

- **Performance:** Lakehouse queries are fast (local/cached); vendor API calls have latency and rate limits
- **Normalization:** The lakehouse common schema means agents get consistent data regardless of whether the firm uses QBO or Xero
- **Offline resilience:** Agents work even if a vendor API is down
- **Access control:** The lakehouse enforces row-level security; vendor APIs don't understand our permission model

## Data Architecture

### Medallion Pattern

```
[Vendor APIs] --> [Bronze: Raw] --> [Silver: Normalized] --> [Gold: Business-Ready]
```

| Layer | Contents | Schema | Update Frequency |
|-------|----------|--------|-----------------|
| **Bronze** | Raw API responses (JSON), CSV imports, file uploads | Vendor-specific; stored as-is | On sync (hourly or daily) |
| **Silver** | Normalized records: journal entries, employees, invoices, contacts | Common schema (see below) | After each bronze update |
| **Gold** | Aggregated metrics: monthly P&L, trial balance, payroll summaries, KPIs | Business metric schema | After each silver update |

### Common Schema (Silver Layer)

Example: Unified Journal Entry

```sql
CREATE TABLE silver.journal_entries (
    entry_id        UUID PRIMARY KEY,
    firm_id         UUID NOT NULL,         -- Multi-tenant isolation
    source_system   VARCHAR NOT NULL,      -- 'quickbooks' | 'xero'
    source_id       VARCHAR NOT NULL,      -- Original vendor record ID
    entry_date      DATE NOT NULL,
    account_code    VARCHAR NOT NULL,
    account_name    VARCHAR NOT NULL,
    debit           DECIMAL(12,2) DEFAULT 0,
    credit          DECIMAL(12,2) DEFAULT 0,
    description     VARCHAR,
    client_id       UUID,                  -- Which client this relates to
    created_at      TIMESTAMP DEFAULT NOW(),
    synced_at       TIMESTAMP DEFAULT NOW()
);
```

### Ingestion Pipeline

Phase 0-1 (MVP): Simple Python scripts triggered by cron or manual run.

```
QuickBooks API --> Python ETL script --> Bronze table (raw JSON)
                                            |
                                     Transform script
                                            |
                                     Silver table (normalized)
                                            |
                                     Aggregate script
                                            |
                                     Gold table (metrics)
```

Phase 2+: Event-driven ingestion with webhook triggers and incremental sync.

## Agent Architecture

### LangGraph Graph Design

Building on the existing prototype, the production graph expands to:

```
START
  |
  v
[Intake Node] -- Parse user query, extract intent
  |
  v
[Router Node] -- Determine which specialist agent(s) to invoke
  |
  +---> [Firm Agent] -- Firm-level financials, operations
  +---> [Client Agent] -- Per-client queries
  +---> [Tax Agent] -- Tax data, filing status, estimates
  +---> [Payroll Agent] -- Employee data, payroll runs, compensation
  +---> [Document Agent] -- SOP search, policy lookup, memo retrieval
  |
  v
[Aggregator Node] -- Combine results from specialist agents
  |
  v
[Verifier Node] -- Check answer quality, verify citations, enforce guardrails
  |
  v
[Formatter Node] -- Format response for user's role and surface (Teams, web, etc.)
  |
  v
END --> Response to user
```

### State Management

Expanding the existing `State` schema:

```python
class AgentState(TypedDict):
    messages: list[BaseMessage]      # Conversation history
    iterations: int                  # Loop guard
    user_role: str                   # partner | manager | associate | client
    firm_id: str                     # Multi-tenant context
    client_id: str | None            # Which client context (if any)
    tools_used: list[str]            # Audit trail of tools invoked
    confidence: float                # Agent's confidence in its answer
    citations: list[dict]            # Source references for the answer
```

## Observability Architecture

### Span Hierarchy

```
Trace: "User asks about account 1000 balance"
  |
  +-- Span: IntakeNode (50ms)
  |     +-- attribute: query_text = "What is account 1000 balance?"
  |
  +-- Span: RouterNode (30ms)
  |     +-- attribute: routed_to = "firm_agent"
  |
  +-- Span: FirmAgent (1200ms)
  |     +-- Span: LLMCall (800ms)
  |     |     +-- attribute: model = "gpt-4o-mini"
  |     |     +-- attribute: input_tokens = 450
  |     |     +-- attribute: output_tokens = 120
  |     |
  |     +-- Span: ToolCall:query_journal_entries (200ms)
  |     |     +-- attribute: tool = "query_journal_entries"
  |     |     +-- attribute: results_count = 15
  |     |
  |     +-- Span: LLMCall (200ms)
  |           +-- attribute: model = "gpt-4o-mini"
  |
  +-- Span: VerifierNode (100ms)
  +-- Span: FormatterNode (50ms)
```

### Metrics to Track

| Metric | Purpose |
|--------|---------|
| Query latency (p50, p95, p99) | User experience |
| LLM token usage per query | Cost management |
| Tool call success/failure rate | Reliability |
| Answer confidence distribution | Quality |
| Queries per user per day | Adoption |
| Escalation rate (AI to human) | Effectiveness |

## Security Architecture by Phase

| Phase | Authentication | Authorization | Data Isolation | Audit |
|-------|---------------|--------------|----------------|-------|
| **0 (Prototype)** | None / API key | None | Single-tenant | Console logs |
| **1 (Beta)** | Simple login | Basic role check | Single-tenant | Database audit log |
| **2 (Multi-tenant)** | OAuth 2.0 | Conversation-scoped RBAC | Row-level security (firm_id) | OpenTelemetry traces |
| **3 (Production)** | OAuth 2.0 + SSO (Azure AD) | SAGA-style tokens | RLS + encrypted at rest | Full compliance logging |

The architecture is designed so that security can be layered in progressively. Interfaces and abstraction points are built from Phase 0; implementations start simple and strengthen.

## Infrastructure Evolution

| Component | Phase 0-1 | Phase 2 | Phase 3+ |
|-----------|-----------|---------|----------|
| **Compute** | Local machine / single VPS | Docker Compose on cloud VM | Kubernetes or managed containers |
| **Lakehouse** | DuckDB + DuckLake (local) | DuckDB + DuckLake + S3 | Databricks Delta Lake |
| **Vector DB** | ChromaDB (embedded) | Qdrant (Docker) | Qdrant Cloud or Pinecone |
| **LLM** | Local (Gemma 3) | Cloud API (GPT-4o-mini) | Multi-provider with fallback |
| **Monitoring** | PrintSink / console | OpenTelemetry + Jaeger (local) | OpenTelemetry + OpenLIT (cloud) |
| **CI/CD** | Manual pytest | GitHub Actions | GitHub Actions + staged deploys |
