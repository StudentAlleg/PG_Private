---
name: Project Green Strategy Suite
overview: Create a comprehensive `docs/strategy/` folder containing 8 interconnected strategy documents that form Project Green's complete strategic operating plan -- from market thesis through technical architecture, GTM playbook, financial framework, and risk analysis.
todos:
  - id: strat-index
    content: Create docs/strategy/README.md index
    status: completed
  - id: strat-exec
    content: Write docs/strategy/executive-strategy-brief.md
    status: completed
  - id: strat-market
    content: Write docs/strategy/market-landscape.md
    status: completed
  - id: strat-product
    content: Write docs/strategy/product-strategy.md
    status: completed
  - id: strat-tech
    content: Write docs/strategy/technical-architecture.md
    status: completed
  - id: strat-gtm
    content: Write docs/strategy/go-to-market.md
    status: completed
  - id: strat-finance
    content: Write docs/strategy/financial-framework.md
    status: completed
  - id: strat-risk
    content: Write docs/strategy/risk-register.md
    status: completed
isProject: false
---

# Project Green Strategy Suite

## Mindset

This is written as if a Fortune 20 CEO with deep domain expertise is entering the AI-for-professional-services space with a small, fast team. The strategy is aggressive but disciplined -- every bet is sized, every risk is named, every milestone has a decision gate.

## Document Structure

All documents go in `docs/strategy/` with an index README. Documents reference each other and the existing `docs/knowledge/` and `docs/research/` materials.

### 1. `README.md` -- Strategy Index
- One-page table of contents with document descriptions
- Reading order guide (executive brief first, then based on audience)

### 2. `executive-strategy-brief.md` -- The Thesis
The 4-page document you'd hand a board or an investor. Contains:
- **Vision statement:** "Build the operating intelligence layer for every professional service firm"
- **Market thesis:** $4.87B market growing to $96.69B at 39.6% CAGR; adoption inflection from 9% to 41% in one year; agentic AI tipping point in 2025-2026
- **Why now:** PE consolidation wave creating demand for operational clarity; 80,000+ fragmented US accounting firms; CPA retirement crisis; Big Four investing $9.5B but building for themselves, not for SMB firms
- **The bet:** Services-plus-software model -- productized AI core (Layer 1) wrapped in professional services (Layer 2: "We build your firm's AI twin")
- **Key strategic decisions:** Platform-agnostic core via MCP, Microsoft surface first, DuckLake for MVP data layer, narrow ICP to start
- **2026 objectives and success criteria**

### 3. `market-landscape.md` -- Market Analysis & Competitive Intelligence
Deep analysis covering:
- **TAM/SAM/SOM calculation:** US accounting firms (80,000+), firm size segmentation, technology spend per firm, AI-addressable portion
- **Market dynamics:** The five forces at play (PE rollups, CPA shortage, AI adoption inflection, Big Four investment, client expectations rising)
- **Competitive landscape matrix:** Enterprise (Oracle, SAP, Dynamics), mid-market (Acumatica, NetSuite), SMB (Business Central, Odoo), startups (Gravis AI, Truewind, Vic.ai, Numeric), Big Four internal tools
- **Project Green differentiation:** Overlay vs replacement, multi-agent vs single copilot, lakehouse vs single-system data, role-specific vs generic
- **PE opportunity deep dive:** One-third of top 30 firms PE-backed, exit wave timing, what PE buyers need (operational clarity, margin optimization, documented processes)
- **Competitive moat analysis:** What makes this defensible over time (firm-specific data, process knowledge accumulation, switching costs, network effects across firms)

### 4. `product-strategy.md` -- Product Strategy & Phased Roadmap
The product plan from MVP to full vision:
- **The three archetypes** with build order rationale (Archetype 1 first, then 2, then 3)
- **Layer 1 / Layer 2 model** in detail -- what's platform, what's services
- **Feature roadmap by phase:**
  - Phase 0 (Now - Q2 2026): Core agent infrastructure, DuckLake data layer, QuickBooks integration, single-firm chat interface
  - Phase 1 (Q3-Q4 2026): Staff Copilot MVP with one beta firm, RAG on firm SOPs, benchmarking and quality metrics
  - Phase 2 (Q1-Q2 2027): Multi-vendor data (Xero, Gusto), Microsoft Teams surface, second firm onboarding
  - Phase 3 (Q3 2027+): Client-Facing Explanation Engine, multi-tenant, production security, Databricks migration
  - Phase 4 (2028+): Process Twin, PE-facing product, full digital twin simulation
- **Decision gates** at each phase transition -- what must be true to proceed
- **Platform decision timeline:** When the Microsoft-vs-Google-vs-both question must be resolved

### 5. `technical-architecture.md` -- Technical Architecture & Stack Decisions
The system architecture blueprint:
- **Architecture diagram** (mermaid) showing all layers: UI surface, super agent/copilot, orchestrator, specialist sub-agents, LLM stack, RAG, data lakehouse, vendor integrations
- **Technology stack table:** Every component with chosen technology, alternatives considered, and rationale
- **Build vs buy analysis** for each component
- **MCP strategy:** How MCP enables platform independence; MCP server design for each vendor integration
- **Data architecture:** Medallion pattern (bronze/silver/gold), common schema design, ingestion pipeline
- **Agent architecture:** LangGraph graph design, state management, routing logic, tool binding, iteration control
- **Observability architecture:** OpenTelemetry integration plan, span hierarchy, production monitoring
- **Security architecture by phase:** From prototype (no-op) through production (SAGA-style tokens, RLS, conversation-scoped RBAC)
- **Infrastructure evolution:** Local DuckDB -> cloud DuckLake + S3 -> Databricks; ChromaDB -> Qdrant/Pinecone

### 6. `go-to-market.md` -- Go-to-Market Playbook
The execution plan for getting to market:
- **Ideal Customer Profile (ICP):** Specific firm characteristics (size, software stack, geography, pain points)
- **Positioning:** "Ask this before you ask a human" -- outcome-based messaging by persona (managing partner, ops partner, senior accountant)
- **Pricing model:** Exploration of per-firm, per-user, tiered, and retainer-based pricing; comparison to competitors
- **Sales motion:** Founder-led sales for first 5 firms, then referral-driven; demo-first approach; free assessment as lead gen
- **The flywheel:** One firm -> case study -> thought leadership -> conference talks -> next firm -> expanded firm usage -> more case studies
- **Beta client strategy:** Local pharmacy opportunity, ideal beta characteristics, what to learn from beta
- **Partnership strategy:** Accounting associations, technology consultants, QBO ProAdvisor network, PE operating partners
- **Content and thought leadership plan:** Conference circuit, blog posts, LinkedIn, podcast appearances

### 7. `financial-framework.md` -- Financial Model & Unit Economics
The money side:
- **Revenue model:** Setup fee + monthly platform fee + retainer for ongoing tuning
- **Unit economics:** Cost to serve one firm (LLM inference, hosting, storage, support), target gross margin
- **LLM cost analysis:** Using benchmarking framework data -- cost per query across providers (GPT-4o, Claude, Gemini, local models), cost optimization strategies
- **Pricing scenarios:** Conservative/moderate/aggressive pricing with revenue projections
- **Cost structure:** Infrastructure (cloud, LLM APIs, vector DB), development (Mike + Owen + future hires), go-to-market (conferences, content, tooling)
- **Funding considerations:** Bootstrap vs seed round, what capital enables, when to raise
- **Key financial milestones:** Revenue targets by quarter, break-even analysis, burn rate management

### 8. `risk-register.md` -- Risk Analysis & Mitigations
Every material risk, rated and mitigated:
- **Competitive risk:** Big Four build it, ERP vendors add it, startup with more funding gets there first
- **Technical risk:** LLM reliability for financial data, data quality from vendor APIs, integration complexity
- **Regulatory risk:** AI liability for accounting advice, evolving FINRA/state CPA board rules, data privacy
- **Market risk:** Firms slower to adopt than expected, PE cycle timing, economic downturn
- **Execution risk:** Two-person team, split focus (Owen FT employment), technology complexity
- **Platform risk:** Microsoft/Google change SDK terms, vendor API deprecation, LLM pricing changes
- **Each risk:** Probability (H/M/L), impact (H/M/L), mitigation strategy, early warning indicators

## Cross-References

Strategy documents will reference:
- `docs/knowledge/` for domain context and product architecture
- `docs/research/` for technical specifics and market data
- `docs/PLAN.md` for team context and prototyping philosophy
