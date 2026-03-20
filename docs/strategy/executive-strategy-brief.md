# Executive Strategy Brief

## Vision

**Build the operating intelligence layer for every professional service firm.**

Project Green creates AI-powered digital twins of professional service firms -- starting with accounting, expanding to law and healthcare. The product connects to a firm's existing software, ingests all operational data, and delivers an intelligent layer that every person in the firm (and eventually their clients) can query, learn from, and act on.

We do not replace QuickBooks. We do not replace Gusto. We do not replace the accountant. We make the accountant's entire firm queryable, predictable, and continuously improving.

## Market Thesis

### The Numbers

| Metric | Value |
|--------|-------|
| AI accounting automation market (2024) | $4.87B |
| Projected market (2033) | $96.69B |
| Growth rate | 39.6% CAGR |
| AI adoption in accounting (2024 to 2025) | 9% to 41% |
| Firms planning to increase AI investment | 77% |
| Early adopter ROI within first year | 82% |
| Month-end close time reduction | 12 days to 3 days |

This is a market in the early stages of a multi-decade transformation. Adoption jumped 4.5x in a single year. We are at the inflection point.

### Why Now -- Five Converging Forces

1. **The Agentic AI Tipping Point.** 2025-2026 is when multi-step, autonomous AI agents became production-viable. This is not chatbot-level AI. This is AI that plans, decides, acts, and verifies across complex workflows. The technology is ready.

2. **The PE Consolidation Wave.** Private equity has been rolling up accounting firms at unprecedented scale. One-third of the 30 largest US firms may be PE-backed. These firms need operational clarity, standardized processes, and margin optimization -- exactly what a Process Twin delivers. When interest rates normalize and PE exits begin, firms with operational intelligence will command premium valuations.

3. **The CPA Retirement Crisis.** Nearly three-quarters of the CPA workforce has reached retirement age. Firms cannot hire their way out of capacity constraints. They must automate or shrink. This creates urgent demand for AI that genuinely reduces the burden on remaining staff.

4. **80,000+ Fragmented Firms.** The US accounting market is massively fragmented. Unlike enterprise software markets dominated by a few large buyers, this is a market of tens of thousands of firms that need the same core capabilities. A productized solution scales naturally.

5. **Big Four Are Building for Themselves.** Deloitte, PwC, KPMG, and EY have committed $9.5B to AI -- but they are building proprietary tools for their own practices, not products for the 80,000 smaller firms. The SMB and mid-market are underserved.

## The Bet

### Services-Plus-Software Model

**Layer 1: Productized Core (The Platform)**
- Multi-agent AI orchestration engine
- Data lakehouse aggregating all firm systems
- RAG knowledge base for firm-specific intelligence
- Security and access control framework
- Deployment adapters (Microsoft 365, Google Workspace, standalone)

**Layer 2: Professional Service Wrapper**
- "We build your firm's AI twin"
- One-time setup and integration
- Ongoing tuning and optimization
- Retainer for continuous improvement

This is not pure SaaS and it is not pure consulting. It is a platform that requires professional services to deploy effectively -- similar to how Palantir or Salesforce operate. The services revenue subsidizes the platform build; the platform creates the long-term moat.

### Three Product Archetypes (Sequenced)

| Archetype | What | When | Risk Level |
|-----------|------|------|-----------|
| **1. Internal Staff Copilot** | Private AI assistant trained on firm SOPs, policies, past work. "Ask this before you ask a human." | **MVP -- 2026** | Low (internal only) |
| **2. Client-Facing Explanation Engine** | AI explainer that helps clients understand their financials. No advice, only explanation. | **V2 -- 2027** | Medium (liability, tone) |
| **3. Process Twin** | Full digital model of how work flows through the firm. Simulation, optimization, "what if" analysis. | **Long-term -- 2028+** | High (complexity, data) |

We start where risk is lowest and value is most immediate. Each archetype builds on the data and infrastructure of the previous one.

## Key Strategic Decisions

### 1. Platform-Agnostic Core via MCP

The Model Context Protocol (MCP) is our abstraction layer. Core agent logic and data integrations are platform-independent. The presentation layer (Teams, Workspace, web UI) is a thin adapter. This avoids the "one-way door" of choosing Microsoft or Google exclusively while starting with Microsoft (where accounting firms live) for the MVP.

### 2. DuckLake for MVP Data Layer

We do not need Databricks to prove the concept. DuckDB + DuckLake gives us a full lakehouse (ACID transactions, time travel, schema evolution) on a laptop with zero infrastructure. We graduate to cloud when multi-tenant scale demands it.

### 3. Narrow ICP to Start

We do not target "accounting firms." We target: **10-50 person accounting firms doing both tax and bookkeeping, using QuickBooks Online, in a reachable metro area, with a managing partner who feels the pain of capacity constraints.** One firm. One use case. One interface. Prove it works.

### 4. QuickBooks Integration First

QuickBooks Online is the most common GL system among small-to-mid accounting firms, has the most mature Python SDK, and offers a full sandbox for development. It is the fastest path to real accounting data flowing through the system.

## Milestones Achieved

| Date | Milestone | Significance |
|------|-----------|-------------|
| 2026-02-22 | **First alpha test customer secured** | Agreement signed: 99% discount in exchange for alpha partnership. Project Green now has a committed customer to deliver to. This validates market interest and shifts the project from prototyping to production delivery. See [Alpha Customer Agreement](alpha-customer-agreement.md). |

## 2026 Objectives

> **2026-03-06 NOTE:** Objectives 1, 2, 4, and 5 are gated on resolution of the founder's employment agreement (Risk Register R22). Product build continues privately at full speed. Public GTM activity is deliberately paused until the legal path is clear. See [Legal Prerequisites — Strategic Sequencing](fundraising/legal-prerequisites.md).

| # | Objective | Success Criteria | Decision Gate | Status |
|---|-----------|-----------------|---------------|--------|
| 1 | **Ship a beta product** | Working Staff Copilot answering real questions for one firm | Firm uses it daily without prompting | **Committed** -- alpha customer secured 2/22; production build at Sprint 13.2 (505 tests); delivery gated on legal resolution (R22) |
| 2 | **Develop a go-to-market plan** | Documented ICP, messaging, pricing, and sales motion | Messaging tested with 10+ firm conversations | In progress -- GTM docs complete; execution paused pending R22 |
| 3 | **Land Owen in full-time employment** | Skills development + capital generation | Employed by Q3 2026 | Unchanged |
| 4 | **Land the first paying customer** | Revenue from one firm using the product | Customer retains after 90 days | **On track** -- alpha customer committed; conversion blocked until R22 clears and entity forms |
| 5 | **Build the growth flywheel** | Case study from first customer, 3+ warm leads from network | Pipeline of 5+ qualified firms | Dependent on alpha success + R22 resolution |

## The Long Game

If we execute well through 2026-2027, the position we hold is powerful:

- **Firm-specific data moats** -- each firm's twin becomes more valuable over time, creating natural switching costs
- **Cross-firm intelligence** -- anonymized patterns across firms create industry benchmarks no single firm can build alone
- **PE exit enablement** -- when the PE exit wave comes (rate normalization, likely 2027-2029), firms with operational clarity from our Process Twin command premium multiples
- **Vertical expansion** -- the same architecture applies to law firms, healthcare practices, and any professional service business with complex workflows and fragmented data

We are building a company that gets more valuable with every firm it serves and more defensible with every month of operational data it accumulates.
