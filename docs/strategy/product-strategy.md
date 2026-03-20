# Product Strategy and Phased Roadmap

## Product Model

### Layer 1: Productized Core (What We Own)

The platform we build, control, and deliver:

| Component | Description |
|-----------|-------------|
| **Agent Orchestration Engine** | LangGraph-based multi-agent system with super-agent routing, specialist sub-agents, and MCP tool connectivity |
| **Data Lakehouse** | Unified data layer aggregating all firm systems (GL, payroll, tax, files) via medallion architecture |
| **RAG Knowledge Base** | Firm-specific vector store for SOPs, memos, policies, and operational knowledge |
| **Security & Access Control** | Conversation-scoped RBAC, multi-tenant isolation, audit trails |
| **Platform Adapters** | Thin surface layers for Microsoft 365, Google Workspace, and standalone web deployment |

### Layer 2: Professional Services (How We Deploy)

The human-delivered layer that wraps the platform:

| Service | Description | Pricing |
|---------|-------------|---------|
| **Firm Assessment** | Audit the firm's systems, data, processes, and readiness | Free (lead gen) or flat fee |
| **Twin Setup** | Connect data sources, configure agents, load firm knowledge | One-time setup fee |
| **Ongoing Tuning** | Refine agent behavior, add new use cases, update knowledge base | Monthly retainer |
| **Expansion Projects** | Add new archetypes (Explanation Engine, Process Twin) | Project-based |

The pitch: **"We build your firm's AI twin."**

## Three Product Archetypes

### Archetype 1: Internal Staff Copilot (MVP)

**What it is:** A private, firm-specific AI assistant used internally by firm staff.

**Trained on:**
- Firm SOPs and standard operating procedures
- Prior client memos and work product
- Internal policies (PTO, billing, workflow rules)
- Past Q&A (accumulates over time)

**User experience:**
- Junior associate has a question about month-end close procedures
- Instead of interrupting a senior, they ask the AI
- The AI answers using the firm's own documented procedures
- If confidence is low, it says "ask [specific senior] about this"

**Key metrics:**
- Questions answered without human escalation
- Senior staff interruption reduction
- Onboarding time for new hires
- Answer consistency across staff

**Why start here:**
- Internal only -- no client liability risk
- Lowest technical complexity (RAG on documents, not live financial data)
- Highest immediate value (saves partner time, the most expensive resource)
- Proves the core platform works before adding complexity

### Archetype 2: Client-Facing Explanation Engine (V2)

**What it is:** A client-safe AI that explains financial data. Not advice -- explanation.

**Trained on:**
- The client's specific financials (from the lakehouse)
- Firm-approved language and terminology
- Guardrailed boundaries (what it can and cannot discuss)

**User experience:**
- Client receives monthly financial package
- Client asks: "Why did my expenses increase this month?"
- AI explains: "Your operating expenses increased by $4,200 (12%) compared to last month, driven primarily by a $3,100 increase in contractor payments recorded on Jan 15 and Jan 22. [Source: GL entries #1842, #1856]"
- AI does NOT say: "You should reduce contractor spending"

**Why this is V2, not V1:**
- Requires live financial data integration (not just documents)
- Liability and tone control are critical
- Firm-approved language templates must be developed
- Guardrails must be tested extensively before client exposure

### Archetype 3: Process Twin (Long-Term Vision)

**What it is:** A digital model of how work flows through the firm.

**Capabilities:**
- "How does a new client get onboarded?"
- "Where do we lose time in the month-end close?"
- "What happens if we add two associates and remove one manager?"
- "Which clients are most profitable per hour of effort?"

**Why this is the long game:**
- Requires deep process data (not just financial data)
- Simulation capabilities are complex to build and validate
- The value proposition is transformational but harder to sell to a firm that hasn't experienced Archetypes 1 and 2
- PE-backed firms are the natural buyers -- they need exactly this for exit readiness

## Phased Roadmap

### Phase 0: Foundation (Now -- Q2 2026)

**Objective:** Build the core infrastructure that all three archetypes depend on.

| Deliverable | Detail |
|-------------|--------|
| Multi-agent orchestration | Orchestrator built: router + firm/client/document specialists (tax, payroll placeholders for Phase 1+) |
| DuckLake data layer | Local lakehouse with medallion architecture (bronze/silver/gold) |
| QuickBooks Online integration | Live data flowing from QBO sandbox into the lakehouse |
| RAG pipeline | ChromaDB for document embedding, retrieval, and grounding |
| Chat interface | Simple web UI or terminal for interacting with agents |
| Test infrastructure | Expand benchmarking to cover correctness, not just speed and cost |

**Decision gate to Phase 1:** Can the system answer 10 representative accounting questions correctly using real QBO data and firm documents?

### Phase 1: Staff Copilot MVP (Q3 -- Q4 2026)

**Objective:** Deploy Archetype 1 with one beta firm.

| Deliverable | Detail |
|-------------|--------|
| Firm onboarding workflow | Process to connect a real firm's QBO, load their SOPs, configure agents |
| Firm-specific RAG | Load and index the beta firm's actual SOPs, memos, policies |
| Quality metrics | Track correct tool selection, answer accuracy, response time, cost |
| Feedback loop | Mechanism for firm staff to rate answers and flag errors |
| Audit logging | Record all queries and responses for review |
| Observability | OpenTelemetry integration for production monitoring |

**Decision gate to Phase 2:** Does the beta firm use the product daily? Do they report measurable time savings? Would they pay for it?

### Phase 2: Multi-Vendor and Multi-Surface (Q1 -- Q2 2027)

**Objective:** Expand data sources and deployment surfaces. Onboard second firm.

| Deliverable | Detail |
|-------------|--------|
| Xero integration | Second GL system, proving the common schema works across vendors |
| Gusto integration | Payroll data flowing into the lakehouse |
| Microsoft Teams surface | Staff Copilot accessible in Teams via M365 Agents SDK |
| Multi-tenant infrastructure | Data isolation between firms (row-level security) |
| Second firm onboarding | Validate that onboarding is repeatable, not heroic |
| Pricing validation | Test pricing with two paying firms |

**Decision gate to Phase 3:** Do two firms retain and pay? Is onboarding under 2 weeks? Does the common schema hold for multiple GL systems?

### Phase 3: Explanation Engine and Scale (Q3 2027+)

**Objective:** Launch Archetype 2. Begin production-grade operations.

| Deliverable | Detail |
|-------------|--------|
| Client-Facing Explanation Engine | Archetype 2 with guardrails, approved language, citations |
| Databricks migration | Move lakehouse to production-grade infrastructure |
| Qdrant or Pinecone migration | Production vector database for RAG |
| Production security | Full RBAC, SAGA-style tokens, compliance logging |
| Google Workspace surface | If healthcare/tech-forward firms in pipeline |
| 5-10 firm portfolio | Repeatable sales and onboarding motion |

**Decision gate to Phase 4:** Is the Explanation Engine safe and effective? Are 5+ firms retained? Is revenue covering infrastructure costs?

### Phase 4: Process Twin (2028+)

**Objective:** Launch Archetype 3. Enter PE-backed firm segment.

| Deliverable | Detail |
|-------------|--------|
| Process modeling engine | Digital twin that maps how work flows through the firm |
| Simulation capabilities | "What if" analysis for process changes, staffing, client mix |
| PE-focused packaging | Product and messaging tailored to PE operating partners |
| Cross-firm benchmarking | Anonymized industry benchmarks across the firm portfolio |
| Vertical expansion | Law firm or healthcare pilot using the same platform |

## Platform Decision Timeline

The Microsoft-vs-Google-vs-both question does not need to be resolved now. It needs to be resolved by Phase 2.

| Milestone | Decision |
|-----------|----------|
| **Phase 0-1** | Build core platform-agnostic (LangGraph + MCP). Use simple web UI for beta. |
| **Phase 2 start** | Commit to Microsoft Teams as first platform surface (90%+ of target firms use it). |
| **Phase 3** | Evaluate Google Workspace surface based on pipeline demand. Only build if paying firms need it. |

The MCP abstraction layer means this decision only affects the presentation layer, not the core product. The investment is never wasted.

## What We Are NOT Building

Clarity on scope is as important as the roadmap:

- **Not an ERP.** We do not replace QuickBooks, Xero, or any system of record.
- **Not a general-purpose AI.** We are not competing with ChatGPT or Claude. We are firm-specific.
- **Not a data warehouse product.** The lakehouse is internal infrastructure, not a product we sell.
- **Not a compliance/audit tool.** We help with operational questions, not regulatory filings (initially).
- **Not a mobile app.** Desktop/web first. Mobile only if demand warrants it.
