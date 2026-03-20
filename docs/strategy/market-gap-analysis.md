# Market Gap Analysis

> Identifies specific gaps in the accounting AI market -- where demand
> exists but supply doesn't -- and maps each gap to Project Green's
> capabilities. This is a strategic artifact for prioritizing product
> decisions and sharpening positioning.
>
> This document does not duplicate the competitive landscape, market
> sizing, or positioning analysis already covered in
> [market-landscape.md](market-landscape.md) and
> [ai-erp-landscape.md](../research/ai-erp-landscape.md). It builds
> on top of that foundation.
>
> For an inventory of what we still need to learn through research and
> conversations, see [market-research-gaps.md](market-research-gaps.md).
>
> **Date**: February 2026

---

## 1. Supply-Side Gaps

What firms need but nobody provides today.

### Gap S1: The Multi-System Intelligence Layer

**The gap**: No product connects to all of a firm's systems (GL, payroll,
document management, tax software, time tracking) and provides a unified
intelligence layer across them. Every existing solution is either:

- **Within-one-system** (QBO copilot, Intuit Assist): only knows QBO data
- **Replace-the-system** (Gravis AI): requires migrating off existing tools
- **One-workflow** (Vic.ai for AP, Numeric for close): solves one process, not the firm

A firm using QuickBooks + Gusto + ProConnect + SharePoint has no product
that understands all four together. When a partner asks "How is Client X
performing across all our services?", no tool can answer that today.

**Why it persists**: Building multi-system integrations is expensive and
slow. Startups focus on one integration to ship faster. ERPs are
incentivized to keep users inside their ecosystem. The lakehouse
architecture needed to aggregate heterogeneous data is a non-obvious
technical choice.

**Project Green's position**: The DuckLake lakehouse with medallion
architecture is designed for exactly this. Bronze layer ingests raw data
from any source; silver layer normalizes to a common schema; gold layer
provides business-ready aggregates. MCP servers isolate each integration.
This is our core architectural bet.

### Gap S2: Institutional Knowledge Capture for Small Firms

**The gap**: When a senior accountant retires or leaves a 15-person firm,
their 20 years of institutional knowledge walks out the door. There is
no productized solution for capturing, preserving, and making that
knowledge queryable for small professional service firms.

What exists today:
- **Knowledge management tools** (Notion, Confluence, SharePoint): require
  manual input. Nobody at a 15-person firm has time to maintain a wiki.
- **Training programs**: expensive, time-consuming, and the knowledge is
  in the trainer's head, not the system.
- **ChatGPT / Claude**: can answer general questions but don't know the
  firm's specific procedures, policies, or history.

**Why it persists**: Knowledge capture is a "boil the ocean" problem for
small firms. They don't have process engineers or knowledge managers.
Enterprise knowledge management tools are too complex and expensive.
Nobody has built a solution that captures knowledge passively (through
Q&A interactions, document ingestion) rather than actively (requiring
humans to write documentation).

**Project Green's position**: RAG on firm documents (SOPs, memos, policies)
plus accumulating Q&A history creates a knowledge base that grows over
time. The AI learns what questions get asked and what answers are correct.
This is exactly Archetype 1 (Internal Staff Copilot) -- the knowledge
capture happens as a side effect of staff using the product.

### Gap S3: Role-Based Intelligence

**The gap**: Every AI accounting product offers the same interface to
every user. A managing partner and a first-year associate see the same
screens, get the same level of detail, and have the same access.

In reality, these users need fundamentally different things:
- **Partner**: high-level dashboards, exception alerts, cross-client
  patterns, strategic questions ("Which clients are most profitable?")
- **Senior accountant**: detailed data queries, process status, review
  queues ("Show me all unreconciled items for Client X")
- **Junior associate**: procedural guidance, quick lookups, training-mode
  answers ("What's our policy on capitalizing expenses over $500?")
- **Client** (future): simplified explanations of their own financials

**Why it persists**: Role-based access control exists in most software,
but role-based *intelligence* (different answers for different roles)
requires understanding both the question and the questioner. This is
hard to do well and risky to do poorly (what if the associate gets
partner-level data?).

**Project Green's position**: The multi-agent architecture with a router
node can consider user role when routing and formatting responses. The
verifier node can enforce role-appropriate guardrails. This is a
differentiator that's architecturally natural for our system but would
require a redesign for single-agent competitors.

### Gap S4: Process Visibility for Small Firms

**The gap**: Digital twin and process mining tools exist for manufacturing
and large enterprises (Celonis, SAP Signavio, IBM Process Mining). Nothing
like this exists for a 15-person accounting firm.

Small firm owners cannot answer:
- "How long does it take us to onboard a new client?"
- "Where do bottlenecks form during tax season?"
- "What happens when we lose a staff member mid-project?"
- "How would adding two associates change our capacity?"

These questions are answerable with the right data, but no product
collects, models, or visualizes work flow through a small firm.

**Why it persists**: Process mining requires structured process logs
(timestamps, activity types, case IDs). Small firms don't generate this
data naturally. Building a process twin requires deep domain understanding
of how accounting work actually moves. Enterprise tools are too expensive
and too complex for SMB.

**Project Green's position**: Archetype 3 (Process Twin) directly targets
this gap. The path to get there: Archetype 1 captures firm knowledge,
Archetype 2 captures client interaction patterns, Archetype 3 models
the full firm. Each step feeds data into the next. This is a 2028+
opportunity but the foundation is being built now.

---

## 2. Demand-Side Gaps

What firms would pay for but can't find.

### Gap D1: Compliance-to-Advisory Transition Tools

**The gap**: The accounting industry is shifting from compliance work
(filing taxes, producing reports) to advisory work (strategic guidance,
fractional CFO services, business consulting). This shift is being
driven by:

- Client expectations for proactive insight, not just historical reporting
- Advisory services commanding higher margins than compliance
- AI automating compliance tasks, freeing capacity for advisory
- Competitive pressure (firms that don't advise lose clients to firms that do)

But firms lack tools to deliver advisory insights at scale. Today,
advisory requires a senior partner to manually analyze data, form
insights, and present them to clients. This doesn't scale.

**What would sell**: A tool that automatically identifies financial
patterns, anomalies, and opportunities in client data and presents
them in client-ready language. "Revenue from your top client dropped
15% this quarter. Here's what changed and three options to discuss."

**Project Green's position**: Archetype 2 (Client-Facing Explanation
Engine) is the first step. The leap from explanation ("here's what
happened") to advisory enablement ("here's what to consider") is the
high-value extension.

### Gap D2: Cross-Firm Benchmarking

**The gap**: Small accounting firms have zero visibility into how they
compare to peers. They don't know if their realization rate is good,
if their month-end close is slow, if their staff utilization is
competitive, or if their per-client profitability is healthy.

The Big Four have this data internally across hundreds of clients.
Industry surveys (AICPA, Rosenberg) provide high-level benchmarks
but not firm-specific, real-time comparisons.

**What would sell**: "Firms like yours (15 people, tax + bookkeeping,
Midwest) typically close in 5 days. You close in 9. Here's what top
performers do differently." Anonymized, real-time, actionable.

**Project Green's position**: This is a natural network effect. Each
firm that joins the platform contributes anonymized data. The more
firms, the better the benchmarks. The first 10-20 firms won't have
useful benchmarks. At 50+ firms, the data becomes genuinely valuable.
This is a long-term moat, not a launch feature.

### Gap D3: PE Operational Intelligence

**The gap**: Private equity firms have invested heavily in accounting
firm roll-ups. One-third of the top 30 US firms may be PE-backed by
2026. These PE-backed firms need:

- Operational clarity across acquired practices
- Standardized processes for integration
- Margin optimization data for each practice
- Exit readiness metrics that buyers can verify

Today, this requires expensive management consulting (Deloitte charges
$300-$500K for a digital twin consulting engagement). No productized
solution delivers PE-grade operational intelligence for mid-market
accounting firms.

**What would sell**: A dashboard that shows PE operating partners:
"This practice closes in 7 days, this one closes in 14. Here's why.
Here's what standardization would save." Productized at a fraction
of consulting cost.

**Project Green's position**: Archetype 3 (Process Twin) is the PE
product. The timing bet: when PE exits begin (likely 2027-2029 as
rates normalize), firms with operational intelligence from Project
Green command premium multiples. The PE operating partner becomes
both a customer and a distribution channel.

---

## 3. Segment Gaps

Who's being ignored or underserved.

### Gap G1: The 78,000 Small Firms

The most fundamental segment gap in accounting AI:

| Segment | Firms | AI Investment | Who's Building For Them |
|---------|-------|--------------|------------------------|
| Top 100 | ~100 | $5M-$500M+ | Big Four (proprietary), Oracle, SAP |
| Mid-market | ~2,000 | $250K-$5M | Acumatica, NetSuite, funded startups |
| **Small (10-50)** | **~78,000** | **$5K-$100K** | **Nobody comprehensively** |
| Solo/micro (1-9) | ~300,000 | <$5K | QBO/Xero built-in features |

The 78,000 small firms spend an estimated $5K-$100K annually on
technology. They're large enough to feel pain from capacity constraints,
knowledge loss, and operational complexity. They're small enough that
enterprise solutions are too expensive and complex.

Funded startups (Truewind, Vic.ai, Numeric) serve this segment but
with narrow point solutions -- one workflow each, not the whole firm.

### Gap G2: Sub-Segments Within Small Firms

The 78,000 small firms are not monolithic. Meaningful sub-segments:

| Sub-Segment | Characteristics | Pain Points | AI Readiness |
|-------------|----------------|-------------|-------------|
| **Tax-only firms** | 5-20 staff, seasonal, tax prep focused | Seasonal capacity crunch, client question volume | Moderate -- cloud adoption varies |
| **Tax + bookkeeping** | 10-50 staff, year-round work, our primary ICP | Knowledge fragmentation, capacity constraints, process complexity | High -- use cloud GL (QBO/Xero) |
| **Full-service firms** | 20-100 staff, tax + audit + advisory | Cross-practice coordination, multiple data systems, staffing complexity | High -- most advanced tech stacks |
| **Outsourced/virtual firms** | 5-30 staff, serve multiple clients remotely | Client communication, process standardization, margin pressure | Very high -- cloud-native by design |
| **Industry-specialized** | Varies, deep expertise in one vertical (healthcare, real estate, nonprofit) | Domain-specific compliance, specialized reporting | Moderate -- depends on the vertical |

**The fastest path to traction** may not be the primary ICP (10-50,
tax + bookkeeping). Consider:

- **Outsourced/virtual firms**: Cloud-native, tech-forward, serve many
  clients (each client = more data for the AI). They feel margin pressure
  acutely and are most likely to adopt efficiency tools.

- **Full-service firms**: More complex problems = more value from a
  multi-system intelligence layer. Higher willingness to pay. But longer
  sales cycles and more stakeholders.

### Gap G3: The "Almost Ready" Segment

An underappreciated segment: firms that are curious about AI, have decent
data and processes, but haven't committed to a solution because:

- They don't know where to start
- Available tools seem too narrow or too complex
- They've tried ChatGPT and found it useful but insufficient
- They're waiting for someone they trust to recommend something

Per the 2026 AI in Accounting Report, 59% of firms already use AI and
another 13% plan to adopt before 2027. But only 14% have comprehensive
AI strategies. This means roughly 45% of firms are using AI in an ad hoc
way without a plan.

These firms are the sweet spot: they've validated the concept (AI can
help) but haven't found the right solution. A consultative approach
(AI Readiness Assessment) is designed for exactly this segment.

---

## 4. Competitor Blind Spots

Where competitors are not looking -- and why.

### Blind Spot 1: Point Solutions Can't See the Whole Firm

Truewind automates bookkeeping. Vic.ai automates AP. Numeric
accelerates month-end close. Each is excellent at one thing. None
can answer: "How is the firm performing overall?" or "Where should
I invest my next hire?"

This isn't a bug in their strategy -- it's the natural result of startup
focus. Build one thing well, prove PMF, expand later. But it means the
"whole firm intelligence" gap remains unfilled.

**Pricing context**: Truewind charges approximately $500-$1,500/month
(custom pricing based on complexity). Numeric starts at $30/user/month
for essentials, with custom pricing for Growth and Enterprise tiers.
Vic.ai and Gravis AI use fully custom pricing (contact sales). All
target specific workflows rather than firm-wide intelligence.

### Blind Spot 2: ERP Replacements Require Migration

Gravis AI positions as "AI-powered ERP for service businesses." This
means firms must migrate off QuickBooks/Xero to use it. For a 15-person
firm that has used QBO for 5 years with hundreds of clients set up,
migration is a 6-month project that touches every client relationship.

The overlay approach (connect to what you have, don't replace it) is
structurally invisible to ERP-replacement startups. They see QBO as a
competitor to displace. We see QBO as a data source to connect to.

### Blind Spot 3: Horizontal AI Can't Access Firm Data

ChatGPT and Claude are powerful but can't query a firm's QuickBooks
instance, read their internal SOPs, or understand their chart of
accounts. Firms are using them for general questions, drafting emails,
and summarizing documents -- but not for the high-value questions that
require firm-specific data.

The moment a firm owner asks "What was Client X's AR balance last
month?" -- ChatGPT fails. This is the gap demo that converts.

### Blind Spot 4: Big Four Build for Themselves

Deloitte, PwC, KPMG, and EY have committed $9.5B to AI. They are
building digital twin consulting practices and proprietary tools.
But they are building for:

- Their own 100,000+ employee practices
- Their Fortune 500 clients
- Consulting engagements at $300K-$500K per project

They are not productizing for the 78,000 small firms. This creates
a demand signal (firm owners hear about AI in accounting from Big
Four marketing) without a supply response (no Big Four product
serves them). Project Green fills the gap between the Big Four's
marketing and the small firm's reality.

---

## 5. Gap Prioritization Matrix

Which gaps are biggest and most accessible for Project Green?

| Gap | Market Size | Urgency | PG Readiness | Competition | Priority |
|-----|------------|---------|-------------|-------------|----------|
| **S1: Multi-system intelligence** | Large (78K firms) | High (CPA crisis) | Medium (lakehouse built, integrations pending) | Low (nobody does this) | **Critical** |
| **S2: Knowledge capture** | Large | High (retirement wave) | Medium (RAG pending) | Low | **Critical** |
| **D1: Advisory enablement** | Medium-Large | Medium (industry shift underway) | Low (Archetype 2 future) | Medium (some startups) | **High** |
| **G3: "Almost ready" segment** | Medium (45% of firms) | High (window open now) | High (AI Readiness Assessment designed) | Low | **High** |
| **G2: Outsourced/virtual firms** | Small-Medium | Medium | Medium (cloud-native = easier) | Low | **Medium-High** |
| **S3: Role-based intelligence** | Medium | Medium | Medium (router planned) | Very Low | **Medium** |
| **D2: Cross-firm benchmarking** | Large at scale | Low (needs volume) | Low (needs 50+ firms) | Low | **Medium (long-term)** |
| **D3: PE operational intelligence** | Medium ($, high ACV) | Medium (timing-dependent) | Low (Archetype 3 future) | Low | **Medium (long-term)** |
| **S4: Process visibility** | Medium | Low (Archetype 3) | Low | Very Low | **Low (long-term)** |

### Where to Focus Now

The highest-priority gaps -- multi-system intelligence (S1), knowledge
capture (S2), and the "almost ready" segment (G3) -- are exactly what
the current product roadmap and traction plan address:

- **S1** is filled by the lakehouse + QBO integration (Phase 0)
- **S2** is filled by RAG on firm documents (Phase 0)
- **G3** is reached through the AI Readiness Assessment and content
  engine (traction plan)

The prioritization validates the current strategy. The gaps that are
most urgent and most accessible align with what's being built. The
long-term gaps (benchmarking, PE intelligence, process twin) are
correctly sequenced for Phases 3-4.

---

## 6. Project Green's Unique Position

Why we can fill these gaps when others can't.

### Multi-System Lakehouse Architecture

The DuckLake medallion architecture (bronze/silver/gold) is designed
to aggregate data from heterogeneous sources into a unified, queryable
layer. This is the architectural bet that makes multi-system intelligence
possible. Competitors built on single-system integrations would need
a fundamental redesign to match this.

### Local-First / Data Sovereignty

Running on Ollama with a local LLM means firm data never leaves the
building during development and can stay on-premise or in a firm-
controlled cloud environment in production. For an industry where
data security is the number-one AI adoption barrier (per Deloitte's
2025 survey: trust is the leading obstacle, with only 2.7% of finance
professionals fully trusting AI agents), this is a structural advantage.

### Services-Plus-Software Model

The Layer 2 professional services wrapper (assessment, setup, tuning)
is a feature, not a bug. Small firms don't buy SaaS and self-onboard
when the product involves their financial data. They want a human who
understands their business, sets things up correctly, and is available
when something goes wrong. The consulting touch builds trust that
pure-software competitors cannot replicate.

### MCP-Based Integration Portability

Model Context Protocol ensures that integrations built for one firm
work for every firm, and that the core agent logic is independent of
any specific integration, platform surface, or deployment model. This
means we can expand to new data sources (Xero, Gusto, ADP) and new
surfaces (Teams, Workspace) without rebuilding the core product.

---

## 7. Implications for Product and GTM

### Product Implications

| Insight | Implication |
|---------|------------|
| Multi-system intelligence is the primary supply gap | QBO integration is correctly prioritized as the next Phase 0 milestone. Each additional integration (Xero, Gusto) widens the moat. |
| Knowledge capture happens passively through Archetype 1 | The RAG pipeline isn't just for document Q&A -- it's the mechanism for capturing institutional knowledge over time. Design it for accumulation, not just retrieval. |
| Role-based intelligence is a low-competition differentiator | Build user role awareness into the router from the start, even if MVP only supports one role. The architecture should be ready. |
| Outsourced/virtual firms may be an easier early segment | Consider expanding the ICP to include this sub-segment. They're cloud-native, tech-forward, and serve many clients (more data per firm). |

### GTM Implications

| Insight | Implication |
|---------|------------|
| Trust is the #1 barrier, not price or features | The demo playbook, AI Readiness Assessment, and services wrapper all build trust. Lead with trust, not features. |
| 45% of firms use AI ad hoc with no strategy | The AI Readiness Assessment is positioned perfectly for this segment. They need guidance, not just a product. |
| Point solutions charge $30-$1,500/month | Project Green's $2K-$5K/month pricing targets the firm-wide intelligence layer, which is above point-solution pricing but below consulting rates. This needs validation in conversations. |
| The Big Four create demand they don't fulfill for SMB | Reference Big Four digital twin work in positioning: "Deloitte builds digital twins for Fortune 500 firms. We build them for yours." |

---

## Related Documents

- [Market Landscape](market-landscape.md) -- competitive landscape, market sizing, moat analysis
- [AI ERP Landscape](../research/ai-erp-landscape.md) -- competitor deep dives, positioning
- [Market Research Gaps](market-research-gaps.md) -- what we still need to learn
- [Go-to-Market Playbook](go-to-market.md) -- ICP, positioning, sales motion
- [Traction Acceleration](traction-acceleration.md) -- parallel track for customer conversations
- [Product Strategy](product-strategy.md) -- archetypes and phased roadmap
