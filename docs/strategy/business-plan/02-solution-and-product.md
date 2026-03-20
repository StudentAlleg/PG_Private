# Section 2: Solution & Product

*Business plan section 2 — Project Green*

---

## 1. The Solution in Brief

Project Green builds an **AI-powered operating intelligence layer** for professional service firms. We do not replace the firm’s existing systems—QuickBooks, payroll, tax software, document stores—we connect to them, aggregate the data, and deliver a **firm-specific AI assistant** that answers questions in plain English with accurate, cited answers drawn from the firm’s own data and documents.

The product is an **intelligent overlay**: it makes the accountant’s entire firm queryable, reduces partner interruption, captures institutional knowledge, and—over time—enables client-facing explanation and process-level visibility. We are not an ERP, not a general-purpose chatbot, and not a compliance tool. We are the layer that sits on top of what firms already use.

---

## 2. Two-Layer Model: Platform + Services

### Layer 1: Productized Core (The Platform)

The platform we build, own, and deliver:

| Component | Role |
|-----------|------|
| **Multi-agent orchestration** | Routes questions to the right specialist; coordinates tool calls; formats answers for the user. Built on LangGraph with an orchestrator and domain specialists (firm-level, client-level, document). |
| **Data lakehouse** | Single data layer that aggregates all firm systems. Medallion architecture: raw ingestion (bronze) → normalized schema (silver) → business-ready views (gold). Same agent logic works whether the source is QuickBooks, Xero, or payroll—data is normalized at the silver layer. |
| **RAG knowledge base** | Vector store for firm SOPs, policies, memos, and past work. Enables “ask the firm’s knowledge” without manual documentation. Improves over time as more documents and Q&A are ingested. |
| **Security and access control** | Multi-tenant isolation (every query scoped by firm); conversation and role-aware access; audit trails for production. |
| **Deployment adapters** | Thin presentation layer: standalone web UI today; Microsoft Teams and Google Workspace later. Core logic is platform-agnostic via the Model Context Protocol (MCP). |

### Layer 2: Professional Services (How We Deploy)

Firms do not self-serve this product. We deploy it with them:

- **Assessment** — Review the firm’s systems, data quality, and readiness (lead-gen or flat fee).
- **Twin setup** — Connect data sources, configure agents, load firm knowledge (one-time setup fee).
- **Ongoing tuning** — Refine behavior, add use cases, update the knowledge base (monthly retainer).

The pitch: **“We build your firm’s AI twin.”** This is a services-plus-software model (similar in spirit to Palantir or Salesforce): the services revenue supports the build; the platform and accumulated data create the long-term moat.

---

## 3. Three Product Archetypes (Sequenced)

We deliver value in three stages. Each archetype builds on the previous one’s data and infrastructure.

### Archetype 1: Internal Staff Copilot (MVP — 2026)

**What it is:** A private, firm-specific AI used only by firm staff. Trained on the firm’s financial data (via the lakehouse) and documents (SOPs, policies, memos via RAG). Staff ask in plain English; the AI answers with citations. “What’s our policy on capitalizing expenses over $500?” “What was Client X’s AR balance last month?” “How do we handle month-end close for clients on cash basis?”

**Why first:** Internal-only, so no client liability. Highest immediate value—reduces partner interruption (the most expensive resource), speeds onboarding, and ensures consistent answers. Proves the platform before we add client-facing or process-modeling complexity.

**Success looks like:** The firm uses it daily without being prompted; partners report measurable time back; new hires get answers from the AI instead of interrupting seniors.

### Archetype 2: Client-Facing Explanation Engine (V2 — 2027)

**What it is:** A client-safe AI that **explains** financial data—not advice, only explanation. Example: “Your operating expenses increased 12% this month, driven mainly by contractor payments on Jan 15 and Jan 22. [Source: GL entries #1842, #1856].” Guardrails keep the AI from crossing into advisory or recommendations.

**Why second:** Requires live financial data and firm-approved language; liability and tone need to be designed and tested. Builds on the same lakehouse and agent stack; adds guardrails, citation standards, and client-facing UX.

### Archetype 3: Process Twin (Long-Term — 2028+)

**What it is:** A digital model of how work flows through the firm. Questions like: “Where do we lose time in month-end close?” “What happens if we add two associates?” “Which clients are most profitable per hour?” Simulation and optimization for capacity, staffing, and client mix.

**Why third:** Highest value but highest complexity—process data, simulation, and change-management. Natural buyers are PE-backed firms that need operational clarity and exit readiness. We get there after Archetypes 1 and 2 are proven and the data foundation is in place.

---

## 4. How It Works: Architecture Summary

- **User** asks a question (today: web chat; later: Teams or other surfaces).
- **Orchestrator** interprets the question and routes to the right specialist: firm-level financials, per-client financials, or document/knowledge.
- **Specialist agents** call tools (via MCP) against the lakehouse or the RAG store. They do not call vendor APIs directly; they query the normalized lakehouse so one integration (e.g. QuickBooks) can be swapped or extended without rewriting agent logic.
- **Answers** are grounded in retrieved data and documents, with citations. A verifier step checks answers against source data where appropriate. We do not generate financial numbers without a source.
- **Data flow:** Vendor systems (QuickBooks Online first; then Xero, Gusto, etc.) feed the lakehouse. Firm documents feed the RAG pipeline. Both are isolated per firm (multi-tenant).

**What we are NOT building:** We are not an ERP (we don’t replace QuickBooks or any system of record). We are not a general-purpose AI (we are firm-specific). We are not a compliance or audit tool (operational questions and intelligence, not regulatory filings). We are not a generic data warehouse product—the lakehouse is infrastructure that powers the AI, not a standalone offering.

---

## 5. Current State and Roadmap to Production

### Current State (as of 2026)

The platform is built and measurable:

| Dimension | Status |
|-----------|--------|
| **Multi-agent system** | Orchestrator + firm, client, and document specialists; 8 tool modules (ledger, analytics, staff, time/billing, scheduling, tax, payroll, documents). |
| **Correctness** | 120+ automated tests with structured evaluation framework; iterating toward production accuracy. |
| **Data layer** | DuckDB/DuckLake medallion architecture in place; QuickBooks Online integration in progress. |
| **RAG** | ChromaDB-based pipeline in progress for document Q&A. |
| **Interface** | Streamlit chat UI with message history and tool-call visibility. |
| **Quality assurance** | 120+ automated tests; evaluation harness for regression. |

Development uses a local LLM (e.g. Qwen3:32B via Ollama) for zero marginal inference cost; production can use the same or a cloud model. The architecture is model-agnostic.

### Phased Roadmap (Summary)

| Phase | Focus | Outcome |
|-------|--------|--------|
| **Phase 0 (now – Q2 2026)** | Foundation | QBO + RAG live; system answers 10 representative questions correctly with real data and documents. |
| **Phase 1 (Q3–Q4 2026)** | Staff Copilot MVP | One beta firm (alpha customer) onboarded; daily use; feedback loop; path to paid conversion. |
| **Phase 2 (Q1–Q2 2027)** | Multi-vendor, multi-surface | Xero and Gusto integrations; Teams surface; second firm; onboarding repeatable. |
| **Phase 3 (Q3 2027+)** | Explanation Engine and scale | Archetype 2 live with guardrails; production infra (e.g. cloud lakehouse, vector DB); 5–10 firms. |
| **Phase 4 (2028+)** | Process Twin | Process modeling and simulation; PE-focused packaging; cross-firm benchmarking; optional vertical expansion (law, healthcare). |

The first alpha customer (February 2026) is the forcing function for Phase 1: we are committed to delivering a production-ready Staff Copilot they can rely on, then converting to paid and replicating.

---

## 6. Strategic Choices That Shape the Product

- **Platform-agnostic core via MCP:** Integrations and presentation (Teams, web, etc.) are adapters. We avoid locking into one vendor before we need to; Microsoft is the likely first surface for the target segment.
- **DuckLake for MVP:** Full lakehouse behavior (ACID, time travel, schema evolution) without cloud dependency. We move to cloud when multi-tenant scale and compliance require it.
- **QuickBooks first:** Most common GL among target firms; mature SDK and sandbox. Fastest path to real accounting data through the system.
- **Narrow ICP for launch:** 10–50 person firms, tax + bookkeeping, QuickBooks Online, reachable metro, managing partner who feels capacity and knowledge pain. One segment, one use case, prove it before widening.

---

## Summary

- **Solution:** An AI operating intelligence layer that connects to a firm’s existing systems and delivers a firm-specific assistant with cited, accurate answers.
- **Model:** Productized platform (orchestration, lakehouse, RAG, security, adapters) plus professional services (assessment, setup, tuning). “We build your firm’s AI twin.”
- **Archetypes:** (1) Internal Staff Copilot (MVP, 2026)—internal only, highest immediate value; (2) Client-Facing Explanation Engine (2027)—explanation, not advice; (3) Process Twin (2028+)—operational model and simulation, PE-oriented.
- **Architecture:** Orchestrator + specialists, MCP-based tools, medallion lakehouse, RAG. We do not replace ERPs; we overlay them.
- **Status:** Multi-agent system and evaluation in place; QBO and RAG in progress; alpha customer secured; roadmap is Phase 0 → 1 (beta with one firm) → 2 (multi-vendor, second firm) → 3 (Explanation Engine, scale) → 4 (Process Twin).
