# Traction Acceleration: A Parallel Track to Market

> **HOLD (2026-03-06):** All public traction and GTM activity is deliberately paused pending resolution of the founder's employment agreement ([Risk Register R22](risk-register.md)). This plan is ready to execute the moment the legal gate clears.

> A practical guide to generating customer conversations and potentially
> alpha-level revenue while product development continues. This document
> is a **companion** to the existing [Go-to-Market Playbook](go-to-market.md),
> not a replacement. It proposes a parallel traction track that can run
> alongside engineering work.
>
> **Status**: On hold — gated on R22 resolution
>
> **Context**: See [GTM Evaluation](gtm-evaluation.md) for the assessment
> that motivated this document.
>
> **Date**: February 2026

---

## Why a Parallel Track

The existing GTM sequences customer engagement after product completion.
This made sense when the product was 15% built. Now that we have a working
agent with 94.4% accuracy, a chat UI, and a full evaluation framework,
the product is demonstrable today. The remaining Phase 0 work (QBO
integration, RAG, multi-agent) makes the product better but is not
required to start conversations.

The risk of waiting: every month without customer contact is a month of
assumptions going untested. The risk of starting now: none, as long as
we are honest about what the product is today versus what it will become.

---

## Dual Positioning Framework

Two messages for two contexts. Neither replaces the other.

### Lead Generation Mode: "AI Digital Transformation"

**When to use**: Cold or warm outreach, LinkedIn content, conference
talks, initial conversations with firm owners. Any situation where the
goal is to open a door, not close a sale.

**The message**: "We help accounting firms navigate the AI transformation.
The industry is changing faster than most firms realize -- 41% AI adoption
in just one year, a CPA workforce crisis, and clients expecting real-time
financial visibility. We work with firm owners to assess where AI can
create the most value in their practice."

**Why this works for lead gen**:
- Problem-first, not product-first
- Positions Mike as an expert and advisor, not a vendor
- Opens a consultative conversation ("tell me about your firm")
- Doesn't require the product to be finished
- Applies whether the firm eventually uses Project Green or not (genuine value)

**What NOT to say in lead-gen mode**:
- Don't mention LangGraph, DuckDB, MCP, or any technical infrastructure
- Don't mention pricing or contracts
- Don't say "we have a product we'd like to sell you"
- Don't use "digital twin" unless the conversation naturally goes there

### Product Positioning Mode: "Ask This Before You Ask a Human"

**When to use**: Demos, deeper conversations with interested firm owners,
pilot proposals. Any situation where someone has already expressed interest
and wants to see what the product does.

**The message**: From the existing [Go-to-Market Playbook](go-to-market.md):
"Your AI twin knows what you know. Your team asks it first." Variations
by persona are already documented there and remain unchanged.

**Why this works for demos**:
- Outcome-based, not technology-based
- Speaks directly to the partner's pain (interruptions, capacity)
- Easy to demonstrate with the working prototype

### How the Two Modes Connect

```
Lead Gen Mode                              Product Mode
─────────────                              ────────────
LinkedIn content about AI in accounting
    ↓
Firm owner engages / responds
    ↓
Exploratory conversation ("tell me
about your firm's challenges")
    ↓
AI Readiness Assessment offer
    ↓
Assessment conversation (30 min)
    ↓
Deliver assessment results               → "Want to see what this
    ↓                                       looks like in practice?"
Natural follow-up                             ↓
                                          Live demo of prototype
                                              ↓
                                          Pilot proposal
```

The lead-gen mode creates conversations. The product mode converts interest
into engagement. The AI Readiness Assessment is the bridge between the two.

---

## 30/60/90-Day Action Plan

### Days 1-30: Foundation

The goal for the first 30 days is simple: **have 3 real conversations
with people connected to accounting firms.**

| Week | Action | Deliverable | Time |
|------|--------|-------------|------|
| **1** | Map the warm network | A list of every person Mike and Owen know who is (a) an accounting firm owner, (b) connected to firm owners, or (c) in the accounting industry. Include name, relationship, and how to reach them. | 2-3 hours |
| **1** | Record a demo video | A 3-minute screen recording of the Streamlit prototype answering 3-4 accounting questions. No editing needed -- raw and authentic. See [Demo Playbook](demo-playbook.md). | 1-2 hours |
| **2** | Send 5 outreach messages | Personal messages (not mass email) to the 5 most promising contacts from the network map. Tone: "I'm building something for accounting firms and I'd love your perspective. Coffee?" | 1-2 hours |
| **2** | Write first LinkedIn post | Topic: "The CPA shortage is real. Here's what I'm seeing." or similar. Establish presence. One post is enough to start. | 1 hour |
| **3** | Have first conversation | Listen more than talk. Ask about their firm's challenges, how they handle knowledge transfer, what they've tried with AI. Take notes. | 1 hour + prep |
| **3-4** | Have 2 more conversations | Same approach. Different people. Look for patterns in what they say. | 2 hours + prep |
| **4** | Write a reflection | What did you learn? What surprised you? Which assumptions from the GTM were validated, challenged, or irrelevant? This is the most important deliverable of the month. | 1-2 hours |

**Total time commitment**: ~10-15 hours over 30 days. This is deliberately light -- it runs in parallel with engineering work, not instead of it.

**Success criteria for Day 30**: At least 3 conversations completed. At least 1 insight that changes how you think about the product or market. A written reflection capturing what you learned.

### Days 31-60: Traction Building

The goal for days 31-60 depends on what was learned in the first 30 days.

**If conversations went well** (people were interested, asked good questions, wanted to see more):

| Week | Action | Notes |
|------|--------|-------|
| **5** | Design the AI Readiness Assessment | See [AI Readiness Assessment](ai-readiness-assessment.md). Use what you learned from conversations to shape the assessment dimensions. |
| **5-6** | LinkedIn: 1 post per week | Topics drawn from what firm owners told you. "I talked to 3 firm owners this month. Here's what surprised me about their AI readiness." |
| **6** | Offer the AI Readiness Assessment to 3 firms | "We're developing a free AI readiness assessment for accounting firms. Would you be interested in being one of our first participants?" |
| **7** | Conduct first AI Readiness Assessment | Walk through the assessment with a willing firm owner. Deliver the one-page results. See how they react. |
| **8** | Follow up with demo | For firms that scored well on the assessment, offer a live demo. "Based on your assessment, you're well-positioned to benefit from AI. Want to see what we're building?" |

**If conversations were lukewarm** (polite but not excited, hard to get meetings, no strong signal):

| Week | Action | Notes |
|------|--------|-------|
| **5** | Reassess the ICP | Were you talking to the right people? The right-sized firms? The right roles? |
| **5-6** | Try a different channel | If warm network is thin, try: local CPA society events, LinkedIn cold outreach to firm owners who post about technology, or the pharmacy lead. |
| **6-7** | Adjust the message | Try different angles: operational efficiency instead of AI, time savings instead of digital transformation, cost reduction instead of innovation. |
| **8** | Try outbound content | Write a short piece (LinkedIn article or blog post) that addresses the specific pain points you heard. Use it as a conversation starter. |

**Success criteria for Day 60**: At least 1 AI Readiness Assessment conducted OR a clear understanding of why conversations aren't converting and an adjusted approach.

### Days 61-90: Signal or Pivot

The goal for days 61-90 is to have a **clear signal** on whether the
traction track is working.

**Strong signal** (3+ firms engaged, at least 1 asking "when can we try this?"):

| Action | Notes |
|--------|-------|
| Pursue pilot with most interested firm | Even if QBO integration isn't done, a pilot on synthetic data with their input on questions demonstrates commitment. |
| Discuss pricing informally | "We're figuring out our pricing model. What would a tool like this be worth to your firm?" Gauge reaction to ranges. |
| Accelerate QBO integration | Now there's a real reason to connect to their data. Engineering priority shifts. |
| Write a case study draft | Even before revenue, "Firm X participated in our AI readiness program. Here's what we found." Content that fuels the next conversations. |

**Weak signal** (fewer than 3 engaged firms, no one asking for more):

| Action | Notes |
|--------|-------|
| Honest evaluation | Is this a messaging problem, a channel problem, or a market problem? |
| Test a different segment | Try the pharmacy lead, or a law firm, or a larger accounting firm. |
| Consider a different entry point | Maybe the copilot (Archetype 1) isn't the first thing they'll buy. Maybe the assessment / consulting is the product for now. |
| Revisit timeline | If the market needs more time, focus on building and wait for better timing signals. No shame in this. |

**Success criteria for Day 90**: Either (a) a qualified pipeline of 3+ firms with at least 1 willing to pilot, or (b) a clear, evidence-based decision to adjust the approach.

---

## Content Engine Launch Plan

Content marketing is a long game. It compounds. The earlier it starts,
the more it's worth by the time you need it.

### Platform: LinkedIn (Primary)

Why LinkedIn: accounting firm owners and managing partners are active on
LinkedIn. It's where professional services firms build their brand. It's
free. It has algorithmic distribution that favors text posts.

### Content Cadence

| Phase | Frequency | Type | Example Topics |
|-------|-----------|------|----------------|
| **Month 1** | 1 post/week | Short observations | "Had coffee with a firm owner this week. They spend 3 hours a day answering questions their team should know the answer to." |
| **Month 2** | 2 posts/week | Observations + insight | "The CPA shortage isn't just about hiring. It's about how firms use the people they already have." |
| **Month 3+** | 2-3 posts/week | Mix of insight, data, and story | Industry data, firm owner quotes (with permission), behind-the-scenes of building AI for accounting |

### Content Principles

1. **Lead with the problem, not the solution.** Talk about firm challenges, not about Project Green.
2. **Be specific, not generic.** "One firm owner told me..." is better than "Firms are struggling with..."
3. **Share what you learn from conversations.** This creates a virtuous cycle: conversations become content, content generates more conversations.
4. **Never sound like you're selling.** The moment a post reads like an ad, engagement drops. Share insights. Let people come to you.
5. **Engage with others' content.** Comment thoughtfully on posts from firm owners, CPA society leaders, accounting tech influencers. This is how you get noticed before you have an audience.

### Content Topics (Starter Bank)

Drawing from the research already documented in this project:

| Topic | Angle | Source |
|-------|-------|--------|
| CPA workforce crisis | "75% of CPAs at retirement age -- what does your firm's succession plan look like?" | [market-landscape.md](market-landscape.md) |
| AI adoption in accounting | "AI adoption in accounting jumped from 9% to 41% in one year. Here's what that actually means." | [ai-erp-landscape.md](../research/ai-erp-landscape.md) |
| Month-end close | "Some firms are closing in 3 days instead of 12. AI is part of it, but not the whole story." | [ai-erp-landscape.md](../research/ai-erp-landscape.md) |
| Knowledge management | "Every time a senior leaves your firm, they take 20 years of institutional knowledge with them." | [digital-twins.md](../research/digital-twins.md) |
| PE in accounting | "Private equity is buying accounting firms at record pace. What does that mean for the rest of us?" | [market-landscape.md](market-landscape.md) |
| Staff onboarding | "It takes a new hire 6 months to get up to speed. What if it took 6 weeks?" | [go-to-market.md](go-to-market.md) |
| AI readiness | "I've been assessing accounting firms' readiness for AI. Here are the 5 things that predict success." | [ai-readiness-assessment.md](ai-readiness-assessment.md) (after conducting assessments) |

---

## Network Activation Playbook

### Step 1: Map the Network (2-3 hours, one sitting)

Create a simple spreadsheet or list with these columns:

| Name | Relationship | Connection to Accounting | Reachability | Priority |
|------|-------------|-------------------------|-------------|----------|
| *Example: John Smith* | *College friend* | *His wife runs a 20-person firm* | *Can text him* | *High* |
| *Example: Sarah Chen* | *Former colleague* | *Works at a CPA society* | *LinkedIn connection* | *Medium* |

Categories of people to include:
- Direct contacts who own or manage accounting firms
- Family and friends connected to firm owners
- Former colleagues in accounting, finance, or professional services
- LinkedIn connections in the accounting industry
- People you've met at business events who mentioned accounting
- The pharmacy lead mentioned in the GTM
- Owen's professional network (with his input)

### Step 2: Prioritize (30 minutes)

Rank by two dimensions:
1. **Closeness to a firm owner** (direct owner > connected to owner > in the industry)
2. **Warmth of relationship** (can call/text > can email > LinkedIn only)

The top 5-10 names are the outreach list.

### Step 3: Craft the Outreach (1 hour)

The message is NOT a pitch. It's a request for perspective.

**Template for warm contacts**:

> "Hey [Name] -- I've been working on something in the AI space for
> accounting firms and I'm trying to learn as much as I can about what
> firm owners are actually dealing with day to day. Would you be open
> to a quick 15-minute call? I'm not selling anything -- I genuinely
> want your perspective. [Specific reason: 'I know your wife runs a
> firm' / 'I remember you mentioned working with accounting clients']"

**Template for LinkedIn connections**:

> "Hi [Name] -- I've been following your posts about [topic]. I'm
> researching how AI is changing operations for accounting firms and
> would love to hear your perspective as someone in the industry.
> Would you be open to a brief conversation? Happy to share what
> I've been learning in return."

### Step 4: Follow Through

- Send 5 messages in the first week. Not all at once -- space them out.
- Track responses in the spreadsheet (responded / meeting scheduled / declined / no response).
- For every conversation, take notes on: their challenges, what they've tried, what they'd pay for, who else you should talk to.
- Every conversation should end with: "Who else should I be talking to?" This expands the network organically.

---

## Alpha Revenue: What It Could Look Like

This section is speculative. It's included because the stated goal is
to explore paths to self-funding, not because revenue is expected in
the near term.

### Scenario A: Consulting-Led (Lowest Barrier)

Position as an AI consulting practice for accounting firms. The "product"
is Mike's expertise plus the AI Readiness Assessment.

| Offering | Price | What the Firm Gets |
|----------|-------|--------------------|
| AI Readiness Assessment | Free or $500 | One-page assessment + recommendations |
| AI Strategy Workshop (half-day) | $2,000-$5,000 | Detailed AI roadmap for the firm, prioritized use cases, vendor evaluation |
| Ongoing Advisory | $500-$1,500/month | Monthly check-in, AI implementation guidance, vendor management |

Revenue potential: 2-3 firms at advisory retainer = $1,000-$4,500/month. Modest, but covers infrastructure costs and buys time.

**Pros**: Revenue from day one. Builds deep firm relationships. Learnings feed directly into the product.
**Cons**: Doesn't scale. It's consulting, not software. Can distract from product development.

### Scenario B: Early Access / Beta Program

Once the prototype has QBO integration, offer a discounted beta program.

| Offering | Price | What the Firm Gets |
|----------|-------|--------------------|
| Beta access (6 months) | $500/month (discounted from $2K+ target) | Working AI copilot connected to their QBO data, direct access to the development team |
| Case study participation | Free (in exchange for the case study) | Everything in beta access, plus co-creation of the product |

Revenue potential: 1-3 beta firms at $500/month = $500-$1,500/month. More importantly, this validates willingness to pay.

**Pros**: Software revenue. Validates the product model. Creates case studies.
**Cons**: Requires QBO integration (not yet built). Support burden on a two-person team.

### Scenario C: Hybrid (Consulting Funds the Build)

Start with Scenario A immediately. Transition to Scenario B when the
product is ready. Consulting revenue funds infrastructure. Beta revenue
validates the product.

This is the most pragmatic path and aligns with the services-plus-software
model already described in [product-strategy.md](product-strategy.md).

---

## What Success Looks Like

At the end of 90 days, the ideal outcome is:

1. **10+ conversations completed** with firm owners or close proxies
2. **1-3 firms actively engaged** (took the AI Readiness Assessment, saw a demo, expressed interest)
3. **A written record** of what was learned -- which assumptions held, which broke, what surprised you
4. **A content presence** on LinkedIn (12+ posts, some engagement)
5. **A clearer answer** to: "Is the existing GTM right, does it need adjustment, or do we need to pivot?"

At the end of 90 days, the minimum acceptable outcome is:

1. **5+ conversations attempted** (even if some didn't convert)
2. **An honest evaluation** of why conversations did or didn't work
3. **A decision** on whether to continue this traction track, adjust it, or table it

---

## Relationship to Existing Strategy

This document does not replace or contradict any existing strategy document.

| Document | Status | Relationship |
|----------|--------|-------------|
| [Go-to-Market Playbook](go-to-market.md) | Unchanged | This traction track feeds into the GTM's Phase 1 (founder-led sales) by generating the pipeline that the GTM assumes |
| [Product Strategy](product-strategy.md) | Unchanged | The product roadmap continues. This track runs in parallel. |
| [Financial Framework](financial-framework.md) | Unchanged | Alpha revenue scenarios here are additive, not replacing the financial projections |
| [Executive Strategy Brief](executive-strategy-brief.md) | Unchanged | The 2026 objectives (beta product, first customer, flywheel) are accelerated by this track, not changed |
| [Risk Register](risk-register.md) | Unchanged | This track directly addresses R13 (capacity) by validating market demand before over-investing in engineering |
