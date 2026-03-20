---
type: DLV
author: Victoria, Office of the Chairman
date: 2026-03-19
status: Published
domain: project-green
context: Completed per Malik's BMC canvas assignment for NSF I-Corps preparation
method: BMAD v6.2 Creative Intelligence Suite — Design Thinking workflow (empathize → define → ideate → prototype → test)
---

# Project Green — Business Model Canvas

**Team Name:** Project Green
**Date:** March 19, 2026
**Prepared for:** Naeem Malik, SCORE Business Counselor

---

## KEY PARTNERS

**Enterprise Platform Partners**
- **Microsoft:** Azure for production cloud. M365 Agents SDK for Teams deployment — the surface where 90%+ of accounting firm staff already work. Co-development on enterprise deployment tooling.
- **GL/ERP vendors (NetSuite, Sage Intacct, QuickBooks Online, Xero):** Data source integrations across the full spectrum. Enterprise firms run NetSuite or Sage. Mid-market and emerging firms run QBO or Xero. We integrate with all of them through vendor-agnostic normalization — same product, any GL.
- **Payroll/HCM vendors (ADP, Workday, Gusto, Paychex):** Second integration layer. Enterprise firms run ADP Enterprise or Workday. Emerging firms run Gusto. Same approach — vendor-agnostic.
- **LLM providers (OpenAI, Anthropic, Google):** Inference APIs. We route between providers for cost and quality — no single-vendor lock-in. Enterprise deployments may require on-premise or private cloud LLM options for data sovereignty.

**Strategic Distribution Partners**
- **PE operating partners:** The primary channel into $5B firms. PE firms have acquired 147+ accounting practices since 2020, creating $200B+ in new enterprise value. One PE relationship = 5-20 portfolio firm deployments. They need operational standardization — we deliver it.
- **Management consulting firms:** Deloitte, McKinsey, and mid-tier consultants advise PE-backed firms on operational transformation. They currently charge $300K-$500K for digital twin consulting engagements. We are the product they deploy.
- **Enterprise technology consultants:** Boomer Consulting (300+ top firm leaders), Woodard Group, CPA.com (AICPA's technology arm). They build technology roadmaps for firms of all sizes.

**No partner develops our product.** We own all IP. Partners provide data access (GL, payroll, documents), distribution (PE networks, consulting relationships), and infrastructure (cloud, LLM). The architecture is vendor-agnostic by design — we can swap any partner without rewriting core logic.

---

## KEY ACTIVITIES

**Three core competencies — same at every firm size:**

1. **Multi-agent AI orchestration on financial data.** Specialist agents (firm, client, tax, payroll, document) that route queries, call tools, and return accurate answers grounded in real data. At a 30-person firm, this answers questions for staff. At a $5B firm with 50 acquired practices, this standardizes how every office answers the same questions. The architecture scales — the agents don't care how many offices feed data into the lakehouse.

2. **Financial data normalization across vendor systems.** Ingesting data from any GL, any payroll provider, any document store into a vendor-agnostic common schema via medallion architecture (bronze → silver → gold). At a single-office firm, this connects QBO + Gusto + SharePoint. At a PE roll-up, this connects NetSuite in one office, Sage in another, QBO in a third — and makes them all queryable from one interface. This is the core technical moat.

3. **Operational knowledge capture and standardization.** Loading SOPs, policies, procedures, and institutional knowledge into a queryable intelligence layer. At a single firm, this preserves tribal knowledge. Across a PE portfolio, this becomes the standardization engine — "here's how Practice A handles month-end close, here's how Practice B does it, here's the gap."

**Build vs. Buy:** We build anything that touches our differentiation (agent orchestration, data normalization, knowledge capture, evaluation frameworks). We buy commodity infrastructure (auth, cloud compute, managed databases, LLM inference). The build/buy line doesn't change with firm size — what changes is which tier of infrastructure we buy.

**What kind of company:** Services-plus-software. Layer 1 is the productized platform (multi-agent orchestration, lakehouse, knowledge base). Layer 2 is the professional services wrapper (assessment, deployment, tuning, ongoing optimization). At emerging firms, Layer 2 is founder-delivered. At $5B firms, Layer 2 is delivered by implementation partners or an internal professional services team. The product is the same. The delivery model scales.

---

## KEY RESOURCES

**People**
- **Mike Leavenworth** — Founder. 18 years in accounting. Runs his own firm. Has reviewed financial reporting across 60+ accountants managing high-net-worth clients. Domain expert who speaks the language of every firm size.
- **Owen Peterson** — CTO. 12+ year collaboration with Mike. AI/ML engineering. Part-time, expanding with funding.
- **Phase 2-3 hires:** Enterprise sales, customer success / implementation, additional engineering. Funded by revenue or seed round.
- **Advisory board:** Cybersecurity/NIST compliance (BMO, Navy veteran), AI engineering, GTM strategy — six formal advisors covering the capabilities a two-person team can't yet hire.

**Technology (architected to scale from one firm to one thousand)**

| Layer | Emerging Firms | Enterprise / PE Portfolio |
|-------|---------------|--------------------------|
| Compute | Single cloud instance | Multi-tenant cloud, private deployment options |
| Data lakehouse | DuckDB + DuckLake | Databricks Delta Lake |
| Vector DB | ChromaDB | Qdrant Cloud or Pinecone |
| LLM inference | Cloud APIs (routed) | Cloud APIs + on-premise options for data sovereignty |
| GL integrations | QBO, Xero | NetSuite, Sage Intacct, QBO, Xero — vendor-agnostic schema |
| Payroll integrations | Gusto | ADP Enterprise, Workday, Gusto, Paychex |
| Security | Standard encryption, RBAC | SOC 2 Type II, on-premise options, enterprise audit logging |

The architecture doesn't change between tiers — the same medallion schema, the same agent orchestration, the same MCP tool connectivity. What changes is the infrastructure tier and the number of data sources feeding into it.

**IP — Three defensible layers that compound with scale:**
1. **Orchestration engine** — proprietary multi-agent system on open-source LangGraph. More firms = more edge cases trained = better routing.
2. **Vendor-agnostic data schema** — common model mapping any GL/payroll/document system into unified queryable tables. Every integration is a barrier to entry. At enterprise scale, the number of integrations is the moat.
3. **Cross-firm operational intelligence** — anonymized benchmarking across the portfolio. "Firms like yours close in 5 days. You close in 9." This only exists at scale. A $5B PE portfolio with 20 practices generates benchmarking data no competitor can replicate.

**Financial runway:** Bootstrap at $300-$400/month from personal funds through Phase 1. Seed round trigger: demonstrated traction and a pipeline that exceeds what two people can serve. Enterprise sales motion requires capital — that's the Phase 2-3 fundraising thesis.

---

## VALUE PROPOSITIONS

*Framed through empathy mapping — what do people at each level of a firm actually experience?*

**What a managing partner at a 30-person firm says:** "I spend half my day answering questions my team should already know."
**What a PE operating partner at a $5B portfolio says:** "I have 15 acquired practices, each running different systems, different processes, different cultures. I can't tell you basic operational metrics across the portfolio."

**Three value propositions that scale from one firm to a portfolio:**

**1. Operational intelligence — from one firm to a portfolio.**
At a single firm: recover partner capacity by giving staff an AI that answers questions using the firm's own data and procedures. At a PE portfolio: standardize operations across acquired practices by giving every office the same intelligence layer, fed by whatever systems each office runs. The product is the same. The value multiplies with scale.

**2. Vendor-agnostic data unification.**
Every firm runs a different combination of GL, payroll, tax, and document systems. No product on the market connects all of them into one queryable layer. At a single firm, this means staff can ask questions across QBO + Gusto + SharePoint. At a PE roll-up, this means the operating partner can ask questions across NetSuite in Office A, Sage in Office B, and QBO in Office C — from one interface. The harder it is to integrate, the wider the moat.

**3. Institutional knowledge capture and standardization.**
75% of CPAs approaching retirement. 43% decline in exam candidates since 2016. At a single firm, the product captures tribal knowledge passively as staff use it. Across a PE portfolio, it becomes the standardization engine — documenting how each practice operates, identifying best practices, and propagating them across the portfolio. This is what PE firms pay $300K-$500K to Deloitte for. We productize it.

**Adoption threshold:** At emerging firms, the bar is "better than asking Dave down the hall." At enterprise, the bar is "better than flying consultants in for six months." Both bars are clearable — the product delivers speed (seconds vs. days), consistency (same answer every time), and accumulating intelligence (gets smarter with use).

**What we assume but haven't validated (flagged for I-Corps customer discovery):**
- Which tier feels the pain most acutely — we believe PE operating partners, but we need conversations to confirm
- Whether firms at $5B see this as a technology purchase or a consulting engagement
- Whether "ask this before you ask a human" resonates across firm sizes or needs different framing per tier
- What the trust threshold is at enterprise vs. emerging firms

---

## CUSTOMER RELATIONSHIPS

**How firms at each tier discover solutions:**

| Tier | Discovery Channel |
|------|------------------|
| **$5B / PE-backed** | PE operating partner networks, management consultants (Deloitte, McKinsey), enterprise technology evaluations, industry analyst coverage |
| **Mid-market ($5M-$100M)** | Peer circles (Boomer Consulting, Woodard Group), CPA society events, industry publications, technology consultants |
| **Emerging ($200K-$5M)** | Peer referrals ("what are you using?"), state CPA society events, LinkedIn, ProAdvisor recommendations |
| **All tiers (bottom-up)** | Young CPAs, MAcc graduates, and tech-forward staff pushing adoption upward from within the firm |

**How we build relationships at each tier:**
- **Enterprise/PE:** Consulting-led engagement. Start with an operational assessment. Demonstrate the platform on their actual data. Multi-stakeholder sales process with a named relationship owner.
- **Mid-market:** Consultative founder-led sales. AI Readiness Assessment as the entry offer. Conference speaking and thought leadership for credibility.
- **Emerging:** Warm network, referrals, direct outreach. The fastest path to deployment — one decision maker, short sales cycle.

**How we retain across tiers:**
- Data accumulation creates switching costs at every tier — the AI gets smarter with use
- At enterprise, cross-practice benchmarking creates portfolio-level value no single-office tool can match
- Integration depth — each connected system makes replacement harder
- Services relationship — at emerging firms it's Mike; at enterprise it's an implementation team

---

## CUSTOMER SEGMENTS

**Anchored on $5B revenue firms. Full spectrum.**

| Segment | Firm Revenue | Why They Buy | Decision Maker |
|---------|-------------|-------------|----------------|
| **Anchor: PE-Backed Portfolios** | $100M-$5B+ | Operational standardization across acquired practices. Exit readiness. Margin optimization. Cross-portfolio benchmarking. | COO, PE Operating Partner |
| **Growth: Mid-Market** | $5M-$100M | Cross-practice coordination, multiple data systems, compliance-to-advisory transition, succession planning. | Managing Partner, Executive Committee |
| **Beachhead: Emerging Firms** | $200K-$5M | CPA shortage pain, partner bottleneck, knowledge loss. Fastest to deploy, fastest to prove value. | Managing Partner (one person says yes) |
| **Adjacent: Outsourced/Virtual** | Varies | Cloud-native, many clients per firm, margin pressure. High data density per deployment. | Firm owner |

**Jobs to be done by tier:**
- **$5B anchor:** "Give me operational visibility across all my portfolio firms so I can standardize, optimize margins, and prove exit readiness to buyers."
- **Mid-market:** "Help me coordinate across service lines, retain knowledge through the retirement wave, and shift from compliance to advisory."
- **Emerging:** "Stop me from being the bottleneck. Let my team get answers without interrupting the most expensive person in the building."

**Go-to-market sequencing:**
We prove the product at emerging firms (fastest deployment, shortest sales cycle, lowest risk). We scale through mid-market (higher ACV, referral-driven). We reach the $5B anchor through PE operating partner relationships and consulting-led engagements. The product is the same at every tier — the deployment model, sales motion, and pricing scale up.

**What we assume but haven't validated (flagged for I-Corps):**
- Whether the beachhead → mid-market → enterprise sequencing is correct, or if a PE operating partner would deploy across a portfolio from day one
- Who the actual decision maker is at each tier — mapped from research, not from conversations
- Whether adjacent markets (law firms, healthcare practices) share enough pain to pursue in parallel

---

## CHANNELS

| Channel | Target Segment | Phase |
|---------|---------------|-------|
| Founder-led direct sales | Emerging firms (prove the model) | Phase 1 |
| Referral from existing customers | Emerging → mid-market | Phase 2 |
| PE operating partner relationships | Anchor ($100M-$5B+ portfolios) | Phase 2-3 |
| Management consulting partnerships | Anchor and mid-market | Phase 3 |
| Industry conferences (AICPA ENGAGE, Scaling New Heights) | Mid-market and emerging | Phase 1-2 |
| National organizations (AICPA, IMA, state CPA societies) | All segments | Phase 1-2 |
| Enterprise technology consultants (Boomer, Woodard, CPA.com) | Mid-market and anchor | Phase 2-3 |
| LinkedIn content + thought leadership | All segments | Phase 1 ongoing |
| Microsoft Teams (product delivery surface) | All segments | Phase 2+ |

**The scaling motion:** Founder-led sales at emerging firms generates case studies. Case studies fuel conference speaking and content. Conference visibility attracts mid-market firms. Mid-market deployments generate operational data and benchmarking. Benchmarking attracts PE operating partners. PE relationships open the $5B anchor. Each phase funds and enables the next.

---

## COST STRUCTURE

**Per-firm cost to serve (scales by tier):**

| Component | Emerging Firm | Mid-Market | Enterprise / PE Portfolio |
|-----------|--------------|------------|--------------------------|
| Infrastructure | ~$50/month | ~$350/month | $2K-$10K/month (multi-office, higher compute/storage) |
| Human time (deployment + support) | $600-$1,200/month | $1K-$3K/month | $5K-$15K/month (implementation team, multi-stakeholder) |
| Integrations | 1-2 (QBO + Gusto) | 3-5 (mixed systems) | 5-15 (multiple GLs across offices) |

**Fixed overhead:**

| Phase | Monthly G&A | Team Size |
|-------|------------|-----------|
| Phase 1 (1-5 firms) | $300-$400 | 2 (founders) |
| Phase 2 (5-20 firms) | $5K-$15K | 3-5 (first hires: sales, CS, engineering) |
| Phase 3 (20+ firms, enterprise entry) | $30K-$80K | 8-15 (enterprise sales, implementation team, engineering) |

**CAC by tier:**
- Emerging: $5K-$10K (founder-led, warm network)
- Mid-market: $15K-$30K (conferences, content, referral)
- Enterprise/PE: $50K-$100K (consulting-led, multi-stakeholder, long cycle)

Against LTV at each tier, LTV/CAC remains 5-15x across all segments.

**Gross margins:** 86-98% depending on tier and phase. Infrastructure costs are low relative to ACV at every level. Human time is the binding constraint early — capital unlocks it.

---

## REVENUE STREAM

**Pricing model (scales by tier):**

| Stream | Emerging | Mid-Market | Enterprise / PE |
|--------|----------|------------|----------------|
| Deployment | $5K-$15K one-time | $15K-$50K one-time | $50K-$200K (multi-office rollout) |
| Platform Fee | $1.5K-$3K/month | $3K-$6K/month | $10K-$40K/month (portfolio-wide) |
| Services Retainer | $1K-$2K/month (optional) | $2K-$5K/month | $5K-$15K/month (dedicated team) |
| Expansion | Per-archetype upgrades | New integrations, client-facing engine | Cross-portfolio benchmarking, Process Twin |

**ACV by tier:**

| Tier | Firm Revenue | ACV |
|------|-------------|-----|
| Emerging | $200K-$5M | $18K-$40K |
| Mid-Market | $5M-$100M | $50K-$120K |
| Enterprise / PE | $100M-$5B+ | $200K-$500K+ |

**What firms pay for comparable solutions today:**
- Practice management (Karbon, Canopy): $35K-$53K — emerging/mid-market comparison
- Managed IT services: $42K-$60K — emerging comparison
- Deloitte digital twin consulting: $300K-$500K/engagement — enterprise comparison
- PE operational consulting: $500K-$2M/year — anchor comparison

Project Green productizes what consulting firms deliver as custom engagements. At emerging firms, we're priced below practice management software for more value. At enterprise, we're priced at a fraction of consulting fees for a persistent, accumulating product instead of a one-time engagement.

**Sales cycle by tier:**
- Emerging: 30-60 days (one decision maker)
- Mid-market: 60-120 days (committee, pilot)
- Enterprise/PE: 6-12 months (multi-stakeholder, procurement, security review, pilot across 2-3 offices)

**Buying window:** May-September for emerging and mid-market (post-tax-season). Enterprise/PE buy on their own cycle — triggered by acquisition events, board directives, or exit timelines.

**Future expansion lever:** Dual-license model where firms re-license client-facing intelligence to their own clients. At enterprise scale with hundreds of clients per firm, this transforms a $200K ACV into a multi-million dollar relationship per portfolio. Not initial pricing — it's the long-term expansion engine.

---

## DESIGN THINKING: WHAT WE KNOW VS. WHAT WE ASSUME

*Per BMAD CIS Design Thinking methodology — Assumption Testing: "What are we assuming? What would prove us wrong?"*

| Element | Status | How We Validate |
|---------|--------|----------------|
| PE operating partners will buy operational intelligence | **Assumed** — from industry trend data (147 deals, $200B value created) | I-Corps: talk to 2-3 PE operating partners directly |
| The product architecture scales from one firm to a portfolio | **Designed for it** — not yet tested at scale | Prove with first multi-office deployment |
| $200K-$500K ACV is achievable at enterprise | **Benchmarked** — against Deloitte consulting fees | I-Corps: pricing conversations with enterprise buyers |
| Beachhead → mid-market → enterprise is the right sequencing | **Assumed** — standard startup playbook | I-Corps: test whether PE would deploy top-down from day one |
| Vendor-agnostic data normalization is the primary moat | **Architectural bet** — built but not stress-tested across multiple GLs | Validate with first firm running something other than QBO |
| "Ask this before you ask a human" resonates across tiers | **Untested** | I-Corps: watch reactions across firm sizes |
| Emerging firms are the fastest path to first revenue | **Assumed** — one alpha customer supports this | I-Corps: test against outsourced/virtual firms and mid-market |
| The services wrapper is what clears the trust barrier | **Assumed** — from Deloitte survey data | I-Corps: ask what would make each tier trust AI with financial data |

This canvas is a hypothesis. Every section contains assumptions that I-Corps customer discovery will validate or invalidate. The canvas will be revised after the first 20 interviews.

---

*Prepared by the bmc-canvas team: Mary (Analyst), John (PM), Conrad (Network). Synthesized by Victoria, Chief of Staff.*
*Method: BMAD v6.2 Creative Intelligence Suite — Design Thinking workflow (empathize → define → ideate → prototype → test)*
*Sources: ProjectGreenRebuild strategy documentation, financial framework, market research, pitch materials.*
