---
name: Market Gap Analysis
overview: "Create a market gap analysis that avoids duplicating the existing (strong) competitive landscape, market sizing, and positioning research, and instead fills genuine blind spots: buyer journey, substitute/alternative analysis, adoption barriers, competitive pricing intelligence, adjacent market opportunities, and a \"jobs to be done\" framework for firm owners."
todos:
  - id: web-research
    content: "Web research: competitor pricing (Truewind, Vic.ai, Numeric, Gravis AI), CPA tech adoption data, law firm AI market, vertical AI SaaS benchmarks"
    status: completed
  - id: write-gap-analysis
    content: Write docs/strategy/market-gap-analysis.md with all 10 sections
    status: pending
  - id: update-changelog
    content: Update docs/CHANGELOG.md with the market gap analysis entry
    status: completed
isProject: false
---

# Market Gap Analysis

## What Already Exists (Will NOT Duplicate)

The existing research is strong in these areas. The new document will reference them, not restate them:

- **Competitive landscape**: [market-landscape.md](docs/strategy/market-landscape.md) and [ai-erp-landscape.md](docs/research/ai-erp-landscape.md) cover competitors thoroughly (enterprise ERP, mid-market, SMB, 60+ funded startups, Big Four)
- **Market sizing**: TAM/SAM/SOM documented in [market-landscape.md](docs/strategy/market-landscape.md) ($8B TAM, $2B SAM, $5M SOM)
- **Positioning**: "Overlay not replacement" and "Ask this before you ask a human" are well-articulated across multiple docs
- **Market timing**: The 2025-2026 window, PE consolidation wave, CPA crisis are all well-documented
- **Competitive moats**: Firm-specific data accumulation, cross-firm network effects, integration depth -- all covered

## What's Missing (The Genuine Gaps)

These are the blind spots that a market gap analysis should fill:

### 1. Substitute Analysis -- "What Do Firms Do TODAY?"

No existing document answers: when a junior has a question right now, what actually happens? The docs describe the *problem* (interruptions, tribal knowledge) but not the *current solutions* firms use. These substitutes are the real competition, not Truewind or Vic.ai. Options include: asking a senior, searching email/Slack, Excel lookups, QBO's built-in search, ChatGPT with manual data, outsourced bookkeeping services, nothing (they just guess).

### 2. Buyer Journey -- "How Do Firm Owners Actually Decide?"

The GTM has a sales motion (warm intro -> assessment -> demo -> pilot -> convert) but no analysis of how firm owners evaluate and buy technology. Key questions: Who initiates the search? What triggers the buying decision? Who else influences the decision? What's the typical evaluation timeline? Where do they look for solutions (conferences, QBO marketplace, peer recommendations)?

### 3. Adoption Barriers -- "What Specifically Stops Firms?"

The [risk-register.md](docs/strategy/risk-register.md) identifies R11 (firms adopt AI slower than expected) but doesn't analyze the specific barriers: data security fears, change management resistance, "we've always done it this way" culture, unclear ROI, no internal champion, bad experience with past technology, cost sensitivity. Understanding which barriers are biggest determines how to overcome them.

### 4. Competitive Pricing Intelligence

The [financial-framework.md](docs/strategy/financial-framework.md) has pricing models ($2K-$5K/month) but no analysis of what competitors charge. Web research on Truewind, Vic.ai, Numeric, Gravis AI, and comparable vertical AI SaaS pricing would ground our pricing assumptions.

### 5. Adjacent Market Profiling

The docs mention law firms and healthcare as future verticals but don't analyze them. Key questions: How big are these markets? What's the equivalent pain point? Are there existing solutions? Would the same product architecture work? Which adjacent market is easiest to enter?

### 6. Jobs to Be Done Framework

The docs describe pain points but not from the buyer's perspective as "jobs." What is the firm owner hiring a product to do? Examples: "Help me answer my team's questions without being interrupted," "Help me onboard new hires faster," "Help me close the books in fewer days." This framework clarifies which product features matter most and in what order.

### 7. Market Segment Profiling

The ICP says "10-50 person firms." But 78,000 small firms aren't monolithic. Sub-segments include: solo tax shops, tax + bookkeeping firms, full-service firms, outsourced/virtual accounting firms, industry-specialized firms. Each has different pain points, technology stacks, and willingness to pay.

## Deliverable

### Single new file: `docs/strategy/market-gap-analysis.md`

Structured as:

1. **Preamble** -- what's already covered and where to find it (avoids duplication)
2. **Substitute analysis** -- what firms do today to solve the problems we target
3. **Buyer journey map** -- how a firm owner goes from "I have a problem" to "I bought a solution"
4. **Adoption barrier analysis** -- specific barriers ranked by severity, with mitigation strategies
5. **Competitive pricing landscape** -- what comparable products charge (web-researched)
6. **Adjacent market scan** -- law, healthcare, fractional CFO, outsourced accounting
7. **Jobs to be done** -- firm owner "jobs" mapped to product archetypes
8. **Market segment profiles** -- sub-segments within the 78,000 small firms
9. **Gap summary** -- the specific market gaps Project Green is best positioned to fill
10. **Open questions** -- what we still don't know and can only learn from conversations

### Web Research

I'll use web search to gather current (February 2026) data on:

- Competitor pricing (Truewind, Vic.ai, Numeric, Gravis AI, and similar)
- Law firm and healthcare AI market sizing/solutions
- CPA firm technology adoption surveys (AICPA, Accounting Today, Journal of Accountancy)
- Vertical AI SaaS benchmarks for pricing and adoption

### Changelog

Update [docs/CHANGELOG.md](docs/CHANGELOG.md) with the new document.

## What This Document Is NOT

- Not a rewrite of competitive analysis (already strong)
- Not a strategy recommendation (the evaluation and traction docs handle that)
- Not a product spec (the PRD and product strategy handle that)
- It IS a research document that fills knowledge gaps and provides a foundation for sharper decision-making
