# Business Model Canvas — Infrastructure Side
## Project Green | March 19, 2026

---

## 1. Key Partners

### What types of external entities do we need and for what?

**Technology Platform Partners**

- **Intuit (QuickBooks Online):** Our first and most critical integration. QBO is the most common GL among our target segment (10-50 person firms). We need their API, their sandbox environment, and eventually deeper access — co-marketing, ProAdvisor network distribution, possibly preferred partner status. They get an AI-powered overlay that makes QBO stickier for firms that might otherwise migrate to NetSuite or Xero.

- **Microsoft:** Two dependencies. First, Azure as likely production cloud (most accounting firms live in Microsoft 365). Second, the M365 Agents SDK for the Teams surface — our Phase 2 deployment channel. We need their platform tools and co-development support. They get a vertical AI proof point showing their platform supports real professional services solutions.

- **Gusto / ADP:** Payroll data is the second integration priority after QBO. Gusto first (preferred by our ICP), ADP second. We need API access for payroll data ingestion. They get deeper product stickiness — same logic as Intuit.

**Do we need a Key Partner to develop part of our "full solution"?**

Not to develop it, but to enable it. The full solution depends on data flowing from vendor systems we don't control. Without Intuit's API, we have no live financial data. Without Gusto's API, we have no payroll. These aren't development partners — they're infrastructure dependencies. We build everything ourselves; they provide the raw material.

The one exception: if we pursue the Microsoft Teams surface in Phase 2, we may need co-development support from Microsoft's M365 Agents SDK team. That's a build partnership, not just an API dependency.

**Key Suppliers**

| Supplier | What We Get | Phase |
|----------|-------------|-------|
| **LLM providers (OpenAI, Anthropic, Google)** | Inference APIs for production queries | Phase 1+ |
| **Cloud infrastructure (Azure or AWS)** | Compute, storage, managed services | Phase 2+ |
| **Databricks** | Production-grade lakehouse when we outgrow DuckLake | Phase 3+ |
| **Qdrant or Pinecone** | Managed vector database for production RAG | Phase 3+ |
| **Auth provider (Auth0 or similar)** | Authentication — not worth building from scratch | Phase 2+ |

**What will we get from them and what will they get from us?**

The LLM providers get usage revenue and a vertical AI case study. Cloud providers get workload commitment. The key dynamic: we are deliberately building on open-source and open standards (LangGraph, MCP, OpenTelemetry, DuckDB) so that no single supplier becomes a chokepoint. We can swap LLM providers, switch cloud platforms, or replace vector databases without rewriting core logic. That's a negotiating position, not just an architecture decision.

**Distribution Partners (overlaps with Channels — flagging for Mary)**

- **QBO ProAdvisors:** Accountants who recommend tools to other accountants. Access to their network is a distribution channel.
- **PE operating partners:** One PE firm = 5-20 portfolio accounting practices. Each acquisition is a new deployment opportunity.
- **Local CPA societies:** Speaking opportunities, credibility, warm introductions.
- **Accounting technology consultants:** Referral channel. They recommend tech stacks to firms.

### Questions to Consider

**Is it a Key Partner to develop part of our "full solution" for customers?**

No partner develops our product. But Intuit and Gusto are load-bearing dependencies — without their data, the product doesn't work. The distinction matters: we own the IP, the architecture, and the customer relationship. Partners provide data pipelines and distribution, not product components.

**For any Key Partner, identify what they are bringing to the table — what important component(s) will they develop or supply? What will you get from them and what will they get from us?**

See table above. The value exchange is clear: we make their products stickier (firms that use Project Green on top of QBO are less likely to leave QBO), and they give us the data access that makes our product possible. It's symbiotic, not dependent — we're building the common schema layer so we can work across vendors (QBO + Xero + whatever comes next).

---

## 2. Key Activities

### What are core competencies?

Three things we must be excellent at, and they map to the two-layer model:

1. **Multi-agent AI orchestration on financial data.** This is the technical core. Building specialist agents (firm, client, tax, payroll, document) that route queries correctly, call the right tools, and return accurate answers grounded in real financial data. Not chatbot-level AI — agents that plan, decide, act, and verify. Current eval: 94.4% correctness, 97.9% tool selection accuracy.

2. **Financial data integration and normalization.** Ingesting data from multiple vendor systems (QBO, Xero, Gusto, ADP), normalizing it into a common schema via the medallion architecture (bronze/silver/gold), and making it queryable. This is the data moat. Every integration we build is a barrier to entry for competitors.

3. **Firm-specific knowledge capture and deployment.** Loading a firm's SOPs, policies, memos, and institutional knowledge into a RAG pipeline that agents can query. This is what makes the product firm-specific rather than generic. It's also what creates switching costs — the accumulated knowledge becomes more valuable over time.

### What will we focus on versus outsourcing?

**Build internally:**
- Agent orchestration engine (LangGraph-based, our core IP)
- Data lakehouse and common schema (the normalization layer)
- MCP servers and tool modules (the integration logic)
- RAG pipeline and knowledge base management
- Evaluation and quality frameworks
- Customer-facing onboarding and tuning

**Buy / outsource:**
- Authentication (Auth0 or similar — not worth building)
- Cloud infrastructure (Azure/AWS managed services)
- Production vector database (Qdrant Cloud or Pinecone when ChromaDB isn't enough)
- Production lakehouse (Databricks when DuckLake isn't enough)
- LLM inference (cloud APIs — we don't train models)

**The decision logic:** We build anything that touches our differentiation (agent intelligence, data normalization, firm-specific knowledge). We buy commodity infrastructure. The build vs. buy analysis in the technical architecture doc is explicit: "Build on open source" for core, "Build now, buy later" for infrastructure that starts free and scales to managed services.

### What drives the decision to do internally or outsource?

Three criteria:
1. **Does it touch our differentiation?** If yes, build it. Agent logic, data schema, evaluation frameworks — these are IP.
2. **Is it commodity infrastructure?** If yes, buy it. Auth, cloud compute, managed databases — these are utilities.
3. **Does the timeline demand it?** Some things (like QBO integration) we build custom first to learn the data model deeply, then consider unified APIs (Merge, Rutter) later for speed.

### What kind of company are we building?

A services-plus-software company. Not pure SaaS, not pure consulting. The closest analogy is early Palantir or early Salesforce:

- **Layer 1 (Platform):** Productized AI core that we own and control. This is the scalable part. Software-like gross margins (86-98% depending on phase).
- **Layer 2 (Services):** Professional services wrapper that deploys, tunes, and supports the platform per-firm. This is the relationship part. It subsidizes the platform build in early stages and creates human switching costs.

The services revenue funds the platform development. The platform creates the long-term moat. Over time, the ratio shifts toward platform (more firms, less per-firm service time as onboarding becomes repeatable). A two-person team can support 10-15 firms before needing to hire, assuming 50/50 split between product development and customer work.

---

## 3. Key Resources

### How important is IP?

Critical. The defensible value of Project Green lives in three IP layers:

1. **The orchestration engine and agent architecture.** Multi-agent system with specialist agents, MCP tool connectivity, router/aggregator/verifier pipeline. Built on open-source LangGraph, but the agent designs, prompt engineering, evaluation frameworks, and orchestration logic are proprietary.

2. **The common data schema.** The normalized silver/gold layer that maps QBO, Xero, Gusto, and ADP data into a unified model. This schema is hard-won — it requires deep understanding of each vendor's data model and the accounting domain. Every new integration deepens this IP.

3. **Firm-specific accumulated intelligence.** Each firm's AI twin gets smarter over time as it processes queries, accumulates feedback, and refines its knowledge base. This isn't code IP — it's data IP. It creates natural switching costs.

Additionally, the MCP protocol choice is strategic: it's an open standard (Anthropic-backed), which means our MCP servers are platform-agnostic. The IP is in the server implementations, not the protocol.

### What key resources are needed to implement the business model?

**Technology Resources:**

| Resource | Phase 0-1 (MVP) | Phase 2-3 (Production) |
|----------|-----------------|------------------------|
| Compute | Local machine / single VPS | Cloud VMs or managed containers (Azure/AWS) |
| Data lakehouse | DuckDB + DuckLake (local, free) | Databricks Delta Lake |
| Vector database | ChromaDB (embedded, free) | Qdrant Cloud or Pinecone |
| LLM inference | Ollama + Qwen3:32B locally (free) | Cloud APIs — GPT-4o-mini, Claude, Gemini |
| Monitoring | Console logs / local sinks | OpenTelemetry + OpenLIT |
| CI/CD | Manual pytest (120+ tests passing) | GitHub Actions + staged deploys |

The architecture is deliberately designed to start at zero infrastructure cost and graduate to managed services as scale demands. DuckLake to Databricks. ChromaDB to Qdrant. Local LLM to cloud API. Each transition is planned, not improvised.

### What types of special facilities or equipment needed?

None. This is a software business. Development happens on personal machines (Mike's PC is already configured with Docker Model Runner, Ollama, DuckDB, the full dev stack). Production deployment is cloud-based. No special hardware, no lab, no physical infrastructure.

The one "facility" worth noting: Mike and Owen need reliable, high-bandwidth internet and development machines capable of running local LLMs (32B parameter models). Both already have this.

### What types of key personnel?

**Current team (Phase 0-1):**
- **Mike** — Founder. Accounting domain expert (CPA/CMA background), product strategy, sales, prototyping. The unfair advantage: he understands both the technology and the customer's world. Sweat equity.
- **Owen** — Core engineering. Building the platform. Part-time (has full-time employment goal by Q3 2026 for capital generation). Sweat equity.

**First hire (Phase 2-3, when firm count exceeds 10-15):**
- $60K-$100K/year
- Likely a customer success / implementation role — someone who can handle firm onboarding and tuning so Mike and Owen can focus on product and sales
- Could also be an engineer if the product backlog is the bottleneck

**Seed round hires (if/when external capital):**
- First 2-3 hires: engineer, customer success, and possibly a part-time sales/marketing person
- Use of $500K-$1.5M seed: accelerated integrations, hire capacity, marketing

### How much "spare" do you have? (Financial runway)

Lean. The bootstrap plan runs on sweat equity and personal savings. Monthly fixed costs are $300-$400/month in Phase 0-1 (Cursor licenses, Miro, domain, minimal cloud/API). This is manageable without revenue.

The critical constraint is human time, not money. Two people, splitting time between product development and customer work, can support ~10-15 firms. Beyond that, hiring is required — and hiring requires revenue or capital.

### What are expected financial needs (apart from sales income) and timing?

**Bootstrap path (current plan):**
- Phase 0-1: $300-$400/month from personal funds. No external capital needed.
- Phase 2: $600-$1,900/month as cloud costs scale. Revenue from 3-5 firms should cover this (even conservative scenario: $4,000-$8,000/month MRR vs. $1,900/month costs).
- Infrastructure becomes self-funding by Q1 2027 if conservative projections hold.

**Seed round path (if market moves faster than bootstrap allows):**
- Trigger: 3-5 paying firms, $100K+ ARR, 90%+ retention, and a pipeline larger than the team can serve.
- Raise: $500K-$1.5M
- Valuation basis: 15-25x ARR for vertical AI SaaS at seed
- Use: first hires, accelerated integrations, marketing
- Timing: likely Q4 2026 or Q1 2027 if traction warrants it

**The decision framework:** External capital is not about needing money. It's about whether "the opportunity is larger than we can capture at current pace, and competitors are moving." If by Q4 2026 there are 3+ paying firms and a pipeline of 20+ interested firms, it's time to accelerate.

---

## Summary: Infrastructure Side at a Glance

| Canvas Block | One-Line Summary |
|--------------|-----------------|
| **Key Partners** | Intuit (data), Microsoft (platform/cloud), LLM providers (inference), PE firms (distribution) — all symbiotic, none develop our product |
| **Key Activities** | Multi-agent AI orchestration, financial data normalization, firm-specific knowledge capture — build core IP, buy commodity infrastructure |
| **Key Resources** | Two-person team with domain + technical expertise, open-source-first tech stack that graduates to managed services, bootstrap runway with clear seed-round triggers |
