# Pitch Deck Content

*Slide-by-slide content for a 12-15 slide investor pitch deck.
Each slide includes the visual content, speaker notes, and design guidance.
Target presentation time: 20 minutes with 10 minutes for Q&A.*

*Transfer this content into Google Slides or PowerPoint. Use a clean, modern
template with dark backgrounds and high-contrast text. Minimal text per slide --
the speaker notes carry the narrative.*

---

## Slide 1: Cover

**Visual:**
- Company name (TBD) -- large, centered
- Tagline: **"Ask this before you ask a human."**
- Mike Leavenworth, CEO & Founder
- mike@mlgroup.us | 561-898-1700
- Pre-Seed | March 2026

**Speaker notes:**
> "We're building the AI operating system for professional service firms --
> starting with accounting. I'm Mike. I've spent 18 years in accounting and
> finance, I run my own practice, and I built this because I needed it myself.
> Let me show you what we're doing."

---

## Slide 2: The Problem

**Visual:**
Three large statistics, stacked vertically:
- **75%** of CPAs are approaching retirement
- **33%** decline in CPA exam candidates since 2016
- **50%** of a partner's day spent answering questions their team should already know

Below: *"The accounting industry is losing its experts faster than it can replace them."*

**Speaker notes:**
> "The accounting profession is facing a structural crisis. Not a downturn -- a
> fundamental workforce shortage. Three-quarters of CPAs are nearing retirement.
> The pipeline of new CPAs has dropped by a third. And the partners who remain
> are spending half their day answering the same questions over and over.
>
> This isn't a technology problem yet. Firms are solving it with tribal knowledge,
> interruptions, and overtime. But those solutions don't scale, and the workforce
> gap is only getting wider."

**Source citations (for appendix or Q&A):** AICPA Trends Report; Karbon State of AI in Accounting 2025; industry surveys.

---

## Slide 3: The Cost

**Visual:**
A simple before/after comparison:

| Today | With AI |
|-------|---------|
| Month-end close: **12 days** | Month-end close: **3 days** |
| New hire productive: **6 months** | New hire productive: **weeks** |
| Partner answers **20+ questions/day** | Partner answers **only the hard ones** |

Below: *"Revenue per employee: $175K-$211K. Every hour of recovered partner capacity is worth $200+."*

**Speaker notes:**
> "The cost is real and measurable. The median accounting firm generates $175,000
> to $211,000 in revenue per employee. Partner time is the most expensive resource
> in the firm -- and it's being consumed by questions a system should be able to answer.
>
> Industry data shows that AI automation can cut month-end close from 12 days to 3.
> That's not theoretical -- early adopters are already reporting these numbers. The
> question isn't whether AI will transform this industry. It's who builds the
> platform these firms trust."

**Source citations:** IPA Data Dive 2024; Rosenberg Survey 2025; Karbon 2025.

---

## Slide 4: The Solution

**Visual:**
Center: **"Your firm's AI twin."**

Three icons in a row:
1. **Knows your data** -- Connects to QuickBooks, payroll, tax systems
2. **Knows your processes** -- Reads your SOPs, policies, handbooks
3. **Answers like you would** -- Staff ask the AI before interrupting a partner

Below: *"Not a chatbot. Not an ERP. An intelligent layer that understands your entire firm."*

**Speaker notes:**
> "We're building a digital twin -- an AI system that ingests a firm's financial
> data and documents, understands them, and can answer questions accurately,
> consistently, and instantly.
>
> Think of it as an intelligent overlay. We don't replace QuickBooks or any
> system of record. We connect to all of them, build a unified intelligence
> layer, and let anyone in the firm ask questions in plain English.
>
> A junior accountant asks 'What's the cash balance for Client X?' and gets an
> answer in seconds -- sourced, cited, from the firm's actual data. No
> interrupting a partner. No searching through spreadsheets."

---

## Slide 5: How It Works

**Visual:**
Three-step flow diagram (left to right):

**Step 1: Connect** → **Step 2: Learn** → **Step 3: Ask**

- Connect: QuickBooks, Gusto, Xero, firm documents (icons)
- Learn: Data flows into a unified lakehouse; documents are indexed
- Ask: Staff or clients ask questions via chat; AI answers with citations

Below: A small architecture note: *"Multi-agent AI with specialist agents for
firm data, client data, and documents. Each agent has tools and domain expertise."*

**Speaker notes:**
> "The architecture is straightforward. We connect to the firm's existing systems --
> QuickBooks for the general ledger, Gusto for payroll, and their document storage
> for SOPs and policies.
>
> That data flows into a unified lakehouse -- think of it as a single brain that
> understands all the firm's data in one place, not siloed across 6 different apps.
>
> Then staff ask questions through a simple chat interface. Behind the scenes,
> specialized AI agents route the question to the right data source, retrieve
> the answer, and present it with citations.
>
> We're not building on top of ChatGPT. This is a purpose-built multi-agent system
> with domain-specific tools for accounting, tax, payroll, and operations."

---

## Slide 6: Product

**Visual:**
Screenshot of the Streamlit chat interface showing a real query and response.
Highlight the tool-calling trace (shows the AI "thinking").

Key metrics in a row below the screenshot:
- **120+** automated tests
- **97.9%** correct tool selection
- **8** specialized tool modules
- **120+** automated tests

*"This is working today. Not a mockup. Not a prototype. A functioning system."*

**Speaker notes:**
> "Let me show you what this looks like. [Demo the product live or walk through
> the screenshot.]
>
> This is a real query against our evaluation data. The system correctly identified
> this as a client-level financial question, routed it to the right specialist agent,
> called the appropriate database tool, and returned a sourced answer.
>
> We've built a structured evaluation framework with 24 questions spanning financial
> queries, staffing, scheduling, analytics, and document retrieval, backed by 120+
> automated tests. We're iterating toward production accuracy.
>
> This isn't a demo that was hand-tuned for 5 questions. It's a production-grade
> evaluation across the full range of questions a firm would ask."

---

## Slide 7: Market

**Visual:**
Three concentric circles (TAM/SAM/SOM):
- **TAM: $540M/year** -- All US accounting firms 11+ employees
- **SAM: $228M/year** -- Cloud GL, AI-ready, capacity-constrained
- **SOM Year 3: $2M-$4M** -- Founder-led sales + referrals + PE channel

Below the circles:
- **Expansion markets:** Law firms ($4B AI legal tech), Healthcare ($36B AI medical billing by 2034), Fractional CFO firms
- *"Accounting is the beachhead. The architecture serves any professional service firm."*

**Speaker notes:**
> "There are roughly 88,000 accounting firms in the US. Our serviceable market
> is about 6,000 firms -- those with $2M+ revenue, cloud-based accounting
> systems, and active capacity constraints.
>
> At a blended $38,000 ACV, that's a $228M SAM in accounting alone.
>
> But here's what makes this bigger: the same architecture -- multi-system
> intelligence layer, document knowledge base, specialist AI agents -- applies
> to any professional service firm. Law firms have the same knowledge
> fragmentation problem. Healthcare practices have the same billing complexity.
> Fractional CFO firms need the same multi-client intelligence.
>
> The AI-in-accounting market alone is projected to grow from $7B to $36B by 2030
> at 41-50% CAGR. We're entering at the inflection point."

**Source citations:** IBISWorld; CPA-list.com; Mordor Intelligence; Research and Markets 2025.

---

## Slide 8: Business Model

**Visual:**
Pricing tier table:

| Tier | Firm Revenue | ACV | Monthly |
|------|-------------|-----|---------|
| **Starter** | $2M-$10M | $18K-$30K | $1,500-$2,500/mo |
| **Growth** | $10M-$25M | $36K-$48K | $3,000-$4,000/mo |
| **Scale** | $25M-$50M | $48K-$72K | $4,000-$6,000/mo |

Plus: One-time setup ($5K-$15K) + Optional tuning retainer ($1K-$3K/mo)

Below: **Gross margins: 86-98%** | Unit economics: LLM inference $5-$50/mo per firm

**Speaker notes:**
> "Our pricing is tiered by firm size and anchored at $40K ACV for the core
> target segment -- firms with $10M to $50M in revenue.
>
> For context: these firms spend $350K to $525K per year on technology. They pay
> $42K to $60K for managed IT services. They pay $35K to $53K for practice
> management software like Karbon -- which has no AI.
>
> At $40K, we're below the vertical SaaS median ACV of $50K for this category,
> and we deliver measurable ROI against a single FTE's recovered capacity.
>
> Gross margins are software-like: 86-98%. Our local-first architecture means
> LLM inference costs are near zero. The primary cost is human time for setup
> and ongoing tuning, which is included in the services wrapper."

**Source citations:** B2B SaaS ACV Benchmark Study; IPA Data Dive 2025; Karbon pricing 2026.

---

## Slide 9: Traction

**Visual:**
Four proof points in a grid:

| Proof Point | Detail |
|-------------|--------|
| **Working product** | Working prototype with 120+ automated tests, 8 tool modules, evaluation framework |
| **Alpha customer** | Healthcare practice, $10M revenue, engaged February 2026 |
| **Advisory board** | 6 formal advisors: cybersecurity (BMO/Navy), AI/engineering, marketing/GTM |
| **Market validation** | 64% of firms plan AI investment next year; $40K ACV validated by 6 benchmarks |

Below: *"We've done the homework. The product works. The market is ready. What we need is execution capital."*

**Speaker notes:**
> "Most pre-seed companies come to you with a slide deck and a promise.
> We come with a working system, a formal advisory board, and the most thorough
> market analysis you'll see at this stage.
>
> The product works -- not in theory, but measured against a 24-question evaluation
> framework that tests financial queries, staffing questions, scheduling, and
> document retrieval.
>
> Our alpha customer is a $10M healthcare practice that I've personally served
> for 9 years. They said yes because they trust me and they see the value. This
> also validates something important: the architecture works beyond accounting.
> Healthcare is a natural expansion market.
>
> And the advisory board brings deep expertise in cybersecurity, AI engineering,
> marketing, and compliance -- the exact domains this product needs to succeed."

---

## Slide 10: Go-to-Market

**Visual:**
Three-phase timeline:

**Phase 1** (Now-2027): Founder-led sales → First 5 firms
**Phase 2** (2027-2028): Referral-driven → Firms 6-20
**Phase 3** (2028+): PE channel → 20+ firms (1 PE firm = 5-20 deployments)

Below: The flywheel diagram:
```
One Firm → Value → Case Study → Thought Leadership → Next Firm
    ↑                                                    ↓
    ← Cross-Firm Benchmarks ← Expanded Usage ←──────────┘
```

**Speaker notes:**
> "Our go-to-market is phased to match our resources.
>
> Phase 1 is founder-led sales. I personally know the industry, I speak the
> language, and I have the relationships. The first 5 firms will come through
> my network and the advisory board's connections.
>
> Phase 2 is referral-driven. Every happy firm generates introductions to 2-3
> peer firms. Every deployment produces a case study. We start speaking at
> CPA society events and accounting conferences.
>
> Phase 3 is where it scales. Private equity firms are actively acquiring
> accounting practices. One PE operating partner relationship equals 5 to 20
> firm deployments. PE firms need exactly what we build -- operational
> intelligence, process standardization, and margin optimization data.
>
> Each firm makes the product better. More data means better benchmarks.
> More questions mean better AI training. More case studies mean stronger proof.
> It's a flywheel."

---

## Slide 11: Why We Win

**Visual:**
Five moat elements, each with an icon:

1. **Data accumulation** -- Every day of usage makes switching harder
2. **Network effects** -- Cross-firm benchmarking improves for all
3. **Integration depth** -- Deep connections to QBO, Xero, Gusto are expensive to replicate
4. **Services relationship** -- Human trust layer compounds with data layer
5. **The founder IS the customer** -- Domain expertise that cannot be hired

Below: Competitive positioning matrix showing Project Green vs. point solutions (Tofu, Xenett), practice management (Karbon), and generic AI (ChatGPT).

**Speaker notes:**
> "Let me be direct about defensibility, because I know you'll ask.
>
> First: data moat. Every day the product runs at a firm, it accumulates more
> operational intelligence. The AI gets better at that firm's terminology,
> processes, and patterns. Migrating away means losing years of accumulated
> intelligence. Workflow switching costs in vertical SaaS exceed $500K for
> mid-market customers.
>
> Second: network effects. As we onboard more firms, anonymized benchmarking
> becomes possible. 'Firms like yours close in X days.' 'Top performers do Y
> differently.' Each new firm makes the data more valuable for everyone.
>
> Third: the founder advantage. I'm not a software engineer who read about
> accounting. I've spent 18 years in this industry. I've reviewed the work of
> 60+ accountants. I run a practice. I AM the customer. That means I know
> which problems are real and which are imaginary -- and investors in this
> room know how rare that is."

---

## Slide 12: The Team

**Visual:**
Founder section:
- **Mike Leavenworth** -- CEO & Founder
  - 18+ years in accounting and finance
  - Founder, ML Financial Group (accounting practice since 2017)
  - Reviewed financial reporting across 60+ accountants for HNW clients
  - Internal audit → Category management → Founder → AI builder
  - Stanford Lean Startup; IIA Board Member

- **Owen [Last Name]** -- Co-Founder & CTO (developing)
  - AI/ML research and engineering
  - 20+ year collaborative relationship through open-source community

Advisory board section (logos or initials):
- **Cybersecurity & Compliance** -- Sr Analyst, BMO; US Navy veteran; NIST/PCI-DSS
- **AI & Engineering** -- Deep AI expertise, entrepreneurial builder
- **Marketing & GTM** -- Marketing strategy and go-to-market specialist
- Plus 3 additional advisors across operations, judgment, and problem-solving

**Speaker notes:**
> "I started in accounting at 19. Worked my way through internal audit at Office
> Depot -- a Fortune 500 -- to category management, then founded my own practice.
> I've reviewed the financial output of 60 accountants managing high-net-worth
> clients. I built this product because I needed it.
>
> Owen is my co-founder and technical lead. We've collaborated for over 20 years
> through an open-source community -- this isn't a LinkedIn connection, it's a
> decades-long working relationship. With this funding, Owen moves to a
> significantly increased role.
>
> The advisory board brings the domains we need: cybersecurity and NIST compliance
> from a BMO analyst and Navy veteran, deep AI and engineering expertise,
> and go-to-market strategy. These are formal advisors with equity agreements
> and real commitment."

---

## Slide 13: Financial Projections

**Visual:**
Revenue chart showing three scenarios over 5 years (2026-2031):

| Year | Conservative | Moderate | Aggressive |
|------|-------------|----------|------------|
| 2027 | $240K ARR | $570K ARR | $800K ARR |
| 2028 | $612K ARR | $1.68M ARR | $2.76M ARR |
| 2029 | $1.14M ARR | $3.52M ARR | $7.50M ARR |
| 2030 | $1.80M ARR | $6.44M ARR | $16.2M ARR |
| 2031 | $2.73M ARR | $10.56M ARR | $29.0M ARR |

Below: **"Our plan targets the moderate scenario. Conservative is the floor."**

**Speaker notes:**
> "Three scenarios. Conservative assumes bootstrap-only, no PE channel, pure
> organic growth. We reach $2.7M ARR in 5 years with 65 firms.
>
> Moderate assumes a PE channel opens by year 2, a small sales team, and
> expanding ACV as larger firms adopt. We reach $10.6M ARR with 220 firms.
>
> Aggressive assumes seed funding, dedicated sales, multiple PE partners, and
> product-led expansion. $29M ARR with 500 firms.
>
> Our plan targets moderate. Conservative is the floor. The aggressive scenario
> requires capturing about 8% of the broader SAM over 5 years -- ambitious but
> plausible for a well-positioned vertical SaaS product with strong retention.
>
> At 10x revenue -- the median for vertical SaaS -- the moderate scenario implies
> a $100M+ valuation by 2031."

**Source:** Detailed model in [financial-model.md](financial-model.md). Valuation multiples from Windsor Drake Q4 2025.

---

## Slide 14: The Ask

**Visual:**
Large text: **Staged Raise: $75K Now → $300K-$500K After Revenue**

Two-column layout:

| Stage 1: Friends Round | Stage 2: Pre-Seed |
|----------------------|-------------------|
| **$50K-$75K SAFE** | **$300K-$500K SAFE** |
| **$3M-$3.5M cap** | **$6M-$8M cap** |
| Entity, legal, first deployment | Team, engineering, GTM scale |
| → 1-3 paying firms | → 5-10 paying firms, $200K+ ARR |

Below: *"The founder takes no salary. The business is already self-funded at ~$1,200/month. This is pure growth capital."*

**Speaker notes:**
> "We're raising in two stages. Stage 1 is a friends round -- $50,000
> on a SAFE with a $3 to $3.5 million cap. That gets us incorporated,
> insured, deployed at our first customer, and to first revenue.
>
> Here's what makes this different from most pre-seed raises: I don't
> take a salary. My personal expenses are covered by my W-2 job and my
> own accounting practice. I'm already self-funding the entire business --
> including my co-founder's compensation -- at about $1,200 a month.
> I'm already paying for AI tools, subscriptions, and Owen's time out
> of pocket.
>
> So this $50K? It's not survival money. It's pure growth capital. Legal
> foundation, entity formation, conferences to meet customers, and
> hosting for the first deployment. Every dollar goes to scaling.
>
> Once we have 1 to 3 paying customers and real revenue, we raise Stage 2 --
> $300,000 to $500,000 at a $6 to $8 million cap. That's when I start
> drawing a salary and we hire. By that point, revenue justifies the
> higher valuation and the costs.
>
> If you invest in Stage 1 at a $3.5 million cap, and our seed round comes
> in at $15 million, your $50K position is worth over $200,000. That's a
> 4x return before we hit $1 million ARR.
>
> You're investing at the earliest possible stage of a company with a
> working product, a clear market, and a founder who doesn't need your
> money to survive -- he needs it to move faster."

---

## Slide 15: Vision

**Visual:**
A expanding visual showing the platform growing from one firm to an industry utility:

Center: **"The operating system for professional service firms."**

Rings expanding outward:
1. **Accounting firms** (today)
2. **Law firms** (same architecture, different integrations)
3. **Healthcare practices** (alpha customer validates this)
4. **Cross-firm intelligence** (anonymized benchmarks, industry patterns)
5. **Industry utility** (every firm that joins makes it smarter for all)

Below: *"Every firm that joins makes the platform more valuable for every other firm."*

**Speaker notes:**
> "The long-term vision is bigger than accounting.
>
> We start with accounting because I know it, the pain is acute, and the market
> timing is perfect. But the underlying architecture -- connect to a firm's systems,
> build a unified intelligence layer, let anyone ask questions in plain English --
> that applies to any professional service firm.
>
> Law firms have the same knowledge fragmentation. Healthcare practices have the
> same billing complexity. Fractional CFO firms need the same multi-client
> intelligence.
>
> And as we onboard firms across verticals, cross-firm intelligence becomes
> a platform asset. Anonymized benchmarking. Industry patterns. Best practices
> derived from data, not surveys.
>
> We're not building a tool. We're building the intelligence layer that
> professional service firms run on. And the earlier you're in, the more
> that compounding benefits you."

---

## Appendix Slides (Have Ready for Q&A)

### A1: Competitive Landscape Detail

| Category | Players | Threat | Our Advantage |
|----------|---------|--------|---------------|
| Enterprise ERP (Oracle, SAP) | AI on massive platforms | Low | Wrong segment, wrong price |
| Mid-Market ERP (NetSuite, Acumatica) | AI features in cloud ERP | Low-Medium | ERP-centric, not firm-specific |
| AI Startups (Truewind, Vic.ai, Numeric) | Point solutions | Medium | Narrow scope; we span domains |
| Big Four Internal | $9.5B in AI investment | Low | Different segment; they validate demand |
| Horizontal AI (ChatGPT, Claude) | General-purpose AI | Medium | Cannot access firm data or enforce access control |
| Practice Management (Karbon) | Workflow, not intelligence | Medium | No AI; $35-53K/year without intelligence |

### A2: Unit Economics Detail

| Metric | Phase 1 (MVP) | Phase 2-3 (Production) |
|--------|---------------|----------------------|
| Monthly cost per firm | ~$50 | ~$300-$500 |
| Monthly revenue per firm | $2,000-$3,500 | $3,500-$8,000 |
| Gross margin | 97-98% | 86-94% |
| LLM inference cost | $5-$50/mo | $5-$50/mo |
| Human time (setup) | 20-40 hrs one-time | 20-40 hrs one-time |
| Human time (ongoing) | 6-12 hrs/mo | 6-12 hrs/mo |

### A3: Product Architecture

Include the system architecture diagram from [technical-architecture.md](../technical-architecture.md) -- the multi-agent orchestration flow from user query through router to specialist agents to MCP tools to data lakehouse.

### A4: Market Timing Evidence

- AI adoption in accounting: 9% (2024) → 41% (2025) -- 4.5x in one year
- 77% of firms plan to increase AI investment
- 82% of early adopters see positive ROI within first year
- Big Four committed $9.5B to AI transformation
- Gartner: by 2028, one-third of enterprise software includes agentic AI
- The window: 2025-2027 is the adoption inflection. By 2029, it's a mature market.
