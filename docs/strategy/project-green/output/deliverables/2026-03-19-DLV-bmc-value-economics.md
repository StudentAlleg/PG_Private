# Business Model Canvas: Value & Economics
## Value Propositions, Cost Structure, Revenue Stream

**Date:** 2026-03-19
**Author:** Conrad (Network & Social Capital Domain Leader)
**Canvas Sections:** Center column + Bottom row
**Source:** ProjectGreenRebuild strategy docs, financial framework, business plan sections 4-5, financial model, pitch deck

---

## 1. VALUE PROPOSITIONS

### How do our capabilities address customer needs?

The product addresses three distinct pain points that small accounting firms (10-50 people) face daily:

**Pain #1: Partner time is the most expensive thing in the firm, and it's being burned on repeatable questions.**
- Partners spend roughly half their day answering questions their team should already know. At $200+/hour effective rate, a firm with two partners is losing $100K+/year in capacity to interruptions.
- The Staff Copilot (Archetype 1) absorbs this load. It reads the firm's SOPs, memos, policies, and prior work product, then answers questions using the firm's own documented procedures. Junior staff ask the AI before interrupting a senior.
- The measurable claim: reduce partner interruptions, cut new-hire ramp time from months to weeks, answer questions 24/7 with firm-specific accuracy (94.4% accuracy demonstrated in evaluation framework).

**Pain #2: Firm data is scattered across 4-6 systems and nobody can see across all of them.**
- A typical firm runs QuickBooks for GL, Gusto for payroll, ProConnect for tax, SharePoint for documents, plus time tracking and scheduling tools. No existing product connects all of them. When a partner asks "How is Client X performing across all our services?" there is literally no tool that can answer.
- The lakehouse architecture (DuckLake, medallion model) ingests data from all sources into a unified intelligence layer. MCP servers isolate each integration. The firm gets one place to ask questions across all their data.
- This is the core architectural bet and the primary supply gap in the market. Nobody else does this. Point solutions (Truewind, Vic.ai, Numeric) each solve one workflow. ERPs (Gravis AI) require migration. Horizontal AI (ChatGPT) can't access firm data.

**Pain #3: When a senior accountant leaves, 20 years of institutional knowledge walks out the door.**
- Small firms don't have knowledge managers or process engineers. They don't maintain wikis. Knowledge lives in people's heads.
- The RAG pipeline on firm documents captures knowledge passively -- as a side effect of staff using the product. Q&A history accumulates. The AI learns what gets asked and what answers are correct. The firm's knowledge base grows over time without anyone having to "maintain" it.
- With 75% of CPAs approaching retirement and a 33% decline in CPA exam candidates since 2016, this isn't theoretical pain. It's a structural workforce crisis.

### How will customers prioritize where they want to be "better"?

Based on the market gap analysis and industry data, firms will prioritize in this order:

1. **Reduce partner bottleneck / increase capacity** — This is the sharpest pain. The CPA shortage makes it existential. Firms that can't leverage their senior talent more efficiently lose clients or burn out partners. The Staff Copilot directly addresses this on day one.

2. **Faster onboarding of new hires** — Directly linked to the workforce crisis. Firms are hiring less experienced staff and need them productive faster. The AI as a "always available senior colleague" cuts ramp time.

3. **Unified view across systems** — This is a latent need that becomes urgent once firms see it demonstrated. Most partners don't know this is possible. The "gap demo" (ask a question that requires data from two systems, show that ChatGPT fails, show that our product answers it) is what converts interest to commitment.

4. **Client-facing intelligence** (future) — Firms aspire to shift from compliance to advisory. The Explanation Engine (Archetype 2) enables this, but it's a Phase 3 capability. Firms will want it once they've experienced Archetype 1.

5. **Operational visibility / process optimization** (long-term) — The Process Twin (Archetype 3) and cross-firm benchmarking. PE-backed firms will care about this sooner. Most small firms won't prioritize it until they've been on the platform 12+ months.

### How much "better" do we need to be to drive adoption?

The adoption threshold is defined by three factors:

**Accuracy must exceed "good enough to trust."** The current 94.4% answer accuracy and 97.9% correct tool selection are above the threshold. For context, a junior accountant asking a senior gets the right answer maybe 85-90% of the time (the senior may not remember, may be busy, may misunderstand the question). The AI needs to be at least as reliable as the current alternative (interrupting a human), and it needs to cite its sources so answers can be verified. We're there.

**Speed must be dramatically faster than the status quo.** The status quo is: walk to a senior's office, wait for them to finish what they're doing, explain the question, wait for them to look it up or think about it, get an answer. That's 10-30 minutes for a simple question. The AI answers in seconds. This is a 100x improvement in response time. That's not incremental — that's a category change.

**Trust must be earned through the human layer.** This is the non-obvious one. The product doesn't have to be perfect; it has to be delivered by someone the firm trusts. The services-plus-software model (assessment, setup, tuning by a human who understands accounting) is what gets past the trust barrier. Deloitte's 2025 survey found that only 2.7% of finance professionals fully trust AI agents. The human wrapper — Mike doing the assessment, explaining what the AI can and can't do, being available when something goes wrong — is what converts skepticism to adoption. Pure SaaS competitors can't replicate this.

**The switching cost from "no solution" is low.** Most firms aren't switching from a competitor. They're upgrading from tribal knowledge, interruptions, and manual lookups. The bar for adoption isn't "better than the incumbent tool" — it's "better than asking Dave." That's a much lower bar to clear.

---

## 2. COST STRUCTURE

### Where will likely cost drivers come from?

**COGS (Cost of Goods Sold / Cost to Serve):**

The direct cost of serving one firm breaks down into infrastructure and human time.

*Infrastructure per firm (monthly):*

| Component | Phase 1 (MVP) | Phase 2-3 (Production) |
|-----------|---------------|------------------------|
| Compute / hosting | $0-$20 | $50-$200 |
| Data lakehouse | $0 (DuckLake local) | $50-$300 |
| Vector database | $0 (ChromaDB local) | $25-$70 |
| LLM inference | $0-$50 | $5-$50 |
| Monitoring | $0 | $20-$50 |
| **Total** | **~$45-$50** | **~$350** |

LLM inference is cheap because of model routing (GPT-4o-mini or Gemini Flash for most queries, premium models only for complex reasoning), caching of common answers, and local models for development. At 50 queries/day per firm, ~500 input + ~200 output tokens per query, monthly LLM cost per firm is $5-$50 depending on model mix.

*Human time per firm:*

| Activity | Hours | Frequency | Imputed cost ($100/hr) |
|----------|-------|-----------|------------------------|
| Initial setup | 20-40 hrs | One-time | $2,000-$4,000 |
| Monthly tuning | 4-8 hrs | Monthly | $400-$800/mo |
| Support | 2-4 hrs | Monthly | $200-$400/mo |
| **Ongoing total** | **6-12 hrs/mo** | **Monthly** | **$600-$1,200/mo** |

Human time is the binding constraint, not infrastructure. A two-person team can support ~10-15 firms before a hire is needed (assuming 50% of time goes to product development, 50% to customer work).

*Gross margin:*
- Phase 1: 97-98% (revenue $2K-$3.5K/month, infrastructure cost ~$50)
- Phase 2-3: 86-94% (revenue $3.5K-$8K/month, infrastructure cost ~$300-$500)

These are software-like margins. The human delivery cost (setup, tuning) is captured in the pricing — the setup fee and optional retainer are priced to cover the labor, not subsidize it.

**G&A (General & Administrative):**

| Category | Phase 0-1 | Phase 2 (1-20 firms) | Phase 3 (20+ firms) |
|----------|-----------|----------------------|---------------------|
| Tools (Cursor, collaboration, domain) | $300-$400 | $300-$500 | $500-$1,000 |
| Cloud / infrastructure (shared) | $0-$50 | $200-$500 | $500-$2,000 |
| LLM API (shared/dev) | $0-$50 | $50-$200 | $200-$1,000 |
| **Total fixed monthly** | **~$300-$400** | **~$600-$1,200** | **~$1,200-$4,000** |

People costs are the largest G&A line once funding arrives:

| Role | When | Annual cost |
|------|------|-------------|
| Mike (founder — no salary Stage 1) | Now | $0 (W-2 + practice covers personal) |
| Owen (part-time, $115/wk now) | Now | ~$6K; grows to $48K at Stage 1 funding |
| First hire (engineer or CS) | 10-15 firms or seed funding | $60K-$100K |

The founder self-funds the business at ~$750-$1,200/month today. Personal safety net of ~$60K exists separate from business capital. The company is capital-efficient by design — no salary draw until funding, local-first architecture eliminates cloud costs during development, and the co-founder works part-time while employed elsewhere.

**CAC (Customer Acquisition Cost):**

| Phase | CAC | Basis |
|-------|-----|-------|
| Founder-led (first 5 firms) | $5K-$10K | Mike's time, travel, demo costs |
| Referral-driven (firms 6-20) | $10K-$15K | Time + conferences + content |
| Scaled (20+ firms) | $15K-$25K | Sales team + marketing + events |

Against a customer LTV of $200K+ (5 years x ~$40K annual gross profit), LTV/CAC runs 8-20x — well above the 3x minimum threshold. Founder-led sales is the most capital-efficient acquisition channel, and it works because the founder speaks the industry's language and has existing relationships.

**R&D (Research & Development):**

R&D is currently 100% sweat equity — Mike and Owen building the platform. The existing investment includes the multi-agent orchestration engine, DuckLake lakehouse, RAG pipeline, QBO integration, benchmarking framework, and evaluation suite (120+ automated tests). Post-funding, R&D spend goes to:
- Owen's expanded role ($48K/year)
- First engineer hire ($100K/year at seed)
- LLM API costs for development and testing
- Tool licenses (Cursor at $200-$220/month)

R&D is front-loaded: the core platform is built once and reused across every firm. Each additional firm requires integration configuration and knowledge loading (covered by the setup fee), not new product development.

### What is the balance of fixed and variable costs?

The business is **predominantly variable-cost in Phase 1, shifting toward fixed-cost as it scales.**

*Phase 1 (1-5 firms):*
- Fixed costs: ~$300-$400/month (tools, infrastructure)
- Variable costs per firm: ~$50/month infrastructure + $600-$1,200/month human time
- The human time component dominates. Each firm costs real hours. The business scales linearly with headcount until processes are templatized.

*Phase 2-3 (5-40 firms):*
- Fixed costs rise: $600-$4,000/month (shared infrastructure, tools)
- Variable costs per firm: ~$350/month infrastructure (stable per firm)
- Human time per firm decreases as onboarding becomes repeatable and firm-specific tuning gets more efficient
- People costs become the largest fixed expense once hires are made

*At scale:*
- Cloud infrastructure becomes semi-variable (scales with firm count but with economies of multi-tenancy)
- LLM costs are variable but low per firm ($5-$50/month)
- People costs are the dominant fixed expense — engineering, customer success, sales
- The model has operating leverage: each incremental firm adds ~$350/month in variable cost against $2K-$5K/month in revenue

The key insight: the business looks like a services company at 1-5 firms (human time is the main cost) and like a software company at 20+ firms (infrastructure is the main variable cost, human time is amortized across more firms). The transition happens as onboarding, tuning, and support processes become standardized.

---

## 3. REVENUE STREAM

### What are customers familiar with today?

Accounting firms currently buy technology through several established channels and models:

**Practice management software (Karbon, Canopy, Jetpack Workflow):**
- Per-user monthly subscriptions, typically $30-$75/user/month
- Karbon runs $35K-$53K/year for a mid-size firm
- Self-serve onboarding with optional implementation support
- Annual contracts with monthly billing

**Managed IT services:**
- Monthly retainer model, $42K-$60K/year for firms in our ICP
- Includes setup, monitoring, ongoing support
- Relationship-based — firms expect a named contact, not a help desk
- Multi-year relationships are common

**Fractional CFO / advisory tools:**
- Project-based or retainer-based pricing
- Firms are familiar with paying for expertise wrapped around technology

**Tax and compliance software (Intuit ProConnect, Drake, Wolters Kluwer):**
- Annual license fees, often tiered by number of returns or clients
- Deep lock-in — switching tax software is painful and usually triggered by a major event

**Cloud GL (QuickBooks Online):**
- Per-client monthly subscription ($30-$200/month per client)
- Firms manage QBO subscriptions on behalf of their clients — they understand per-client recurring fees

**Consulting engagements:**
- Firms buy consulting from technology vendors, CPE providers, and peers
- Project-based pricing with SOWs
- Deloitte charges $300K-$500K for a digital twin consulting engagement — the Big Four have established "digital twin" as a concept that commands premium pricing

### How do they buy similar products and services?

**Primary model: Subscriptions (recurring monthly/annual)**
- This is the dominant model for practice management, GL software, and managed IT
- Firms are comfortable with monthly recurring payments tied to ongoing value
- Annual contracts with monthly billing are the standard structure
- Price anchors: $2K-$5K/month for firm-wide tools is within the range firms already pay for practice management + managed IT

**Secondary model: Setup + ongoing (services-plus-software)**
- Firms expect implementation support when the product touches their financial data
- One-time setup fees ($5K-$15K) are standard for managed IT and practice management onboarding
- Optional ongoing retainers for support and optimization are familiar from managed IT relationships

**How firms do NOT buy:**
- Self-serve SaaS with no human touch — not for tools that access financial data
- Usage-based pricing (pay per query) — firms want predictable costs
- Per-seat pricing at scale — managing partner doesn't want to count licenses; they want a firm-wide platform

**Project Green's pricing aligns with all of this:**

| Stream | Type | Range | Familiar analog |
|--------|------|-------|-----------------|
| Twin Setup | One-time | $5K-$15K | Managed IT onboarding, practice management implementation |
| Platform Fee | Monthly recurring | $2K-$5K/month | Practice management + managed IT combined |
| Tuning Retainer | Monthly recurring (optional) | $1K-$3K/month | Managed IT support retainer |
| Expansion Projects | One-time/project | Varies | Consulting engagements, new module purchases |

Tiered by firm size:

| Tier | Firm Revenue | ACV | Monthly Platform |
|------|-------------|-----|------------------|
| Starter | $2M-$10M | $18K-$30K | $1,500-$2,500/mo |
| Growth | $10M-$25M | $36K-$48K | $3,000-$4,000/mo |
| Scale | $25M-$50M | $48K-$72K | $4,000-$6,000/mo |

Target blended ACV: ~$40K. This is below the vertical SaaS median of $50K for this category and below what firms already spend on practice management ($35K-$53K) — for a product that delivers measurably more value (AI intelligence vs. workflow management).

### What are they paying for similar products and services?

| Product/Service | Annual cost | What it does |
|-----------------|-------------|--------------|
| Karbon (practice management) | $35K-$53K | Workflow management, no AI |
| Managed IT services | $42K-$60K | IT infrastructure, support |
| Truewind (AI bookkeeping) | $6K-$18K | Automates bookkeeping only |
| Numeric (month-end close) | $4K-$15K (est.) | Accelerates close process only |
| Vic.ai (AP automation) | Custom pricing | Automates accounts payable only |
| Intuit ProConnect Tax | $5K-$20K | Tax preparation software |
| QuickBooks Online (per client) | $4K-$30K/year across clients | General ledger |
| Total firm tech spend | $175K-$525K/year | Everything |

Project Green at $40K ACV sits between point solutions ($6K-$18K, narrow scope) and total tech spend. The positioning: "You're paying $35K-$53K for Karbon to manage workflows. For $40K, you get an intelligence layer across all your systems that actually answers questions, captures knowledge, and makes your team faster." The value comparison is not against other AI tools — it's against the cost of one senior accountant's recovered time ($60K-$100K/year in salary, plus the capacity unlocked).

**The dual-license vision (future upside):** At scale, firms can re-license client-facing digital twins to their own clients at ~$1,000/month per client. A firm with 90 clients generates $864K/year net after Project Green's 20% commission — an 8.6x return on a $100K annual license. This is the long-term revenue model that transforms a $40K ACV into a $316K ACV per firm. It's not part of the initial pricing but it's the expansion lever that drives NRR above 120%.

### What are typical budgeting and sales cycles?

**Budgeting:**
- Most firms budget annually, typically on a calendar year or fiscal year basis
- Technology purchases are budgeted as a line item within G&A
- Firms spending $175K-$525K/year on tech have budget authority for a $40K addition without board approval in most cases
- Managing partners at firms with 10-50 employees typically have sole or primary authority over technology purchases — no procurement committee, no IT department to convince

**Sales cycles:**
- **Point solutions (Karbon, Truewind):** 30-60 days from demo to purchase. Lower stakes, lower ACV.
- **Managed IT / practice management:** 60-120 days. More stakeholders, implementation planning, data migration concerns.
- **Project Green (expected):** 60-90 days for founder-led sales. The free assessment → demo → pilot → convert pipeline is designed for a 90-day cycle:
  - Week 1-2: Warm introduction, assessment scheduled
  - Week 3-4: Assessment delivered, demo of product on representative data
  - Week 5-8: Pilot proposal, negotiation, 30-day pilot with 3-5 staff
  - Week 9-12: Pilot evaluation, conversion to annual contract

**Seasonal considerations:**
- Tax season (January-April) is the worst time to sell to accounting firms. Partners are slammed and not thinking about new tools.
- **May-September is the buying window.** Post-busy season, firms reflect on what went wrong, what they need, and how to prepare for next year. This is when technology purchases happen.
- October-December is budget planning season — good for planting seeds that close in Q1 or Q2 of the following year.
- Project Green's Phase 1 timeline (first paying customer Q3 2026) is aligned with this cycle. The alpha customer was engaged in February 2026 (off-season for a healthcare practice, not a tax firm), and the product will be ready for paid deployment as firms enter their post-busy-season evaluation window.

**The first customer dynamic:**
- Alpha customer (healthcare practice, $10M revenue) engaged February 2026 at 99% discount in exchange for alpha partnership
- Customer #2 targets ~50% discount for case study and feedback
- By customer #3-5, pricing normalizes toward full ACV
- Each engagement validates willingness to pay and refines the pricing model

---

## Cross-References for Canvas Synthesis

**Adjacent sections (for Mary — Task #1):**
- Value propositions tie directly to Customer Segments (the ICP is 10-50 person firms, tax + bookkeeping, QBO, managing partner who feels capacity pain)
- Pricing validation depends on Customer Relationships (the services wrapper is what builds trust and justifies the ACV)

**Adjacent sections (for John — Task #2):**
- Cost structure depends heavily on Key Resources (the lakehouse, RAG pipeline, multi-agent engine are the infrastructure that determines COGS)
- The human time constraint ties to Key Activities (setup, tuning, support are the delivery activities that limit scale)
- R&D costs are driven by Key Partners (LLM providers — OpenAI, Google, Anthropic — and infrastructure partners — Databricks, cloud providers)

---

*This analysis is grounded in Project Green's actual strategy documents, financial models, and market research. Numbers are sourced, not estimated. Where projections are used, they come from the financial framework's moderate scenario.*
