# Investor Memo

*[Company Name TBD] -- Pre-Seed Investment Opportunity*
*Prepared March 2026*
*Confidential -- for prospective investors only*

---

## 1. Executive Overview

[Company Name TBD] is building an AI-powered operational intelligence platform for professional service firms. Starting with accounting -- a $145B US industry in structural crisis -- we connect to a firm's existing financial systems, ingest their internal documents, and deliver an intelligent assistant that answers questions accurately, instantly, and with citations from the firm's own data.

The product works today. A multi-agent AI prototype with 120+ automated tests, a structured evaluation framework, and 8 specialized tool modules spanning financial queries, staffing, scheduling, tax, payroll, and document retrieval. We're iterating toward production accuracy.

We are raising in two stages: a $50K-$75K friends round on a SAFE with a $3M-$3.5M cap (led by a strategic accounting firm investor), followed by a $300K-$500K pre-seed at a $6M-$8M cap once we have paying customers. This staged approach minimizes dilution, proves the model before scaling, and makes the first check closeable in weeks rather than months.

---

## 2. The Problem: A Structural Workforce Crisis

The US accounting industry is not experiencing a cyclical downturn. It is facing a permanent workforce transformation.

**The talent crisis is accelerating:**
- 75% of CPAs are approaching retirement age (AICPA)
- CPA exam candidates declined 33% since 2016 (Karbon 2025)
- Firms cannot replace departing expertise through hiring alone
- The pipeline will not recover: the 150-hour education requirement discourages new entrants

**The operational impact is measurable:**
- Partners spend 50% of their day answering questions their team should know
- Junior staff onboarding takes 3-6 months due to undocumented tribal knowledge
- When a key staff member leaves, their institutional knowledge disappears
- Inconsistent answers erode client trust and create liability

**The cost is quantifiable:**
- Revenue per employee: $175K-$211K (IPA Data Dive 2024)
- Month-end close: 12 days (industry average) vs. 3 days with AI automation
- Partner time recovered: even 2 hours per day at $200+/hour = $100K+ annually

**Current substitutes are failing:**
- Asking a senior → bottleneck, interruption, inconsistent answers
- Searching QBO/SharePoint → slow, limited, often fruitless
- Manual Excel dashboards → stale by the time they're built
- Pasting data into ChatGPT → no live data connection, confidentiality risk
- Hiring more people → the talent doesn't exist at the volume needed

The industry spent $145B in 2024 and is projected to reach $157.4B by 2026 (IBISWorld). These firms have the budget. What they lack is the supply of human expertise to execute. AI is not optional for this industry -- it is the only scalable answer to the workforce gap.

---

## 3. The Solution: An AI Digital Twin

Our platform creates an intelligent overlay that connects to all of a firm's systems, understands the data holistically, and serves as a firm-specific AI assistant.

**Three product archetypes, deployed in sequence:**

**Archetype 1 -- Internal Staff Copilot (MVP, now):**
Internal AI assistant trained on the firm's financial data and documents. Staff ask questions in plain English; the AI answers with citations. Reduces partner interruptions, accelerates onboarding, ensures answer consistency.

**Archetype 2 -- Client-Facing Explanation Engine (Phase 2):**
Client-safe AI that explains financial data -- not advice, explanation. "Your expenses increased 12% this month, driven by contractor payments on Jan 15 and Jan 22. [Source: GL entries #1842, #1856]." Guardrailed boundaries ensure the AI never crosses into advisory territory.

**Archetype 3 -- Process Twin (Phase 3+):**
A digital model of how work flows through the firm. "Where do we lose time in month-end close?" "What happens if we add two associates?" "Which clients are most profitable per hour?" This is the PE product -- operational intelligence for portfolio firms.

**What we are NOT building:**
- Not an ERP (we don't replace QuickBooks, Xero, or any system of record)
- Not a general-purpose AI (we are firm-specific, not competing with ChatGPT)
- Not a compliance/audit tool (operational questions, not regulatory filings)

---

## 4. Product and Technology

### Current State

The platform is functional and measurable:

| Metric | Value |
|--------|-------|
| Evaluation framework | 24-question benchmark spanning financial queries, staffing, scheduling, tax, payroll, and documents |
| Automated tests | 120+ tests with regression framework |
| Tool modules | 8 (ledger, analytics, staff, time/billing, scheduling, tax, payroll, documents) |
| Automated tests | 120+ passing |
| Data architecture | DuckDB/DuckLake medallion architecture (bronze/silver/gold) |
| Agent framework | LangGraph multi-agent orchestration |
| LLM | Local Qwen3:32B via Ollama (zero inference cost for development) |
| Chat interface | Streamlit web UI with message history and tool-call tracing |

### Architecture

Multi-agent system with domain-specialized agents:

- **Orchestrator** routes questions to the appropriate specialist
- **Firm Agent** handles firm-level financial queries (trial balance, P&L, operations)
- **Client Agent** handles per-client queries (client financials, AR/AP, profitability)
- **Document Agent** answers from the firm's knowledge base (SOPs, policies, memos)

Each agent invokes tools via the MCP (Model Context Protocol) standard, connecting to data sources including QuickBooks Online, payroll systems, and document stores.

The data lakehouse uses a medallion architecture: raw data (bronze) → normalized schema (silver) → aggregated views (gold). This means the same agent architecture works regardless of whether the source is QuickBooks, Xero, or any other system -- the data is normalized at the silver layer.

### Roadmap to Production

| Milestone | Status | Timeline |
|-----------|--------|----------|
| Multi-agent system with tools | Complete | Done |
| Evaluation framework | Complete | Done |
| Chat interface | Complete | Done |
| QuickBooks Online integration | In progress | Q2 2026 |
| RAG pipeline (document Q&A) | In progress | Q2 2026 |
| Alpha deployment | Verbal commitment | Q2-Q3 2026 |
| Production security hardening | Planned | Q3 2026 |
| Second customer onboarding | Planned | Q3-Q4 2026 |

---

## 5. Market Opportunity

### US Accounting Firm Universe

| Segment | Firms | Revenue Range |
|---------|-------|---------------|
| Solo / Micro | ~30,000 | Under $500K |
| Small | ~40,000 | $500K-$2M |
| Mid-tier (target) | ~15,000 | $2M-$50M+ |
| Large | ~400 | $50M+ |
| **Total** | **~88,000** | |

### TAM / SAM / SOM

| Metric | Firms | Blended ACV | Value |
|--------|-------|-------------|-------|
| **TAM** | ~15,000 | $36K | $540M/year |
| **SAM** | ~6,000 | $38K | $228M/year |
| **SOM (Year 3)** | 50-100 | $40K | $2M-$4M/year |
| **SOM (Year 5)** | 200-500 | $44K | $8.8M-$22M/year |

### Expansion Markets

The same architecture applies to any knowledge-intensive professional service firm:

| Market | Size | Architecture Fit |
|--------|------|-----------------|
| Law firms (small) | $4B AI legal tech, 31% CAGR | High -- same knowledge-capture pattern |
| Healthcare practices | $36B AI medical billing by 2034 | Medium-High -- alpha customer validates |
| Fractional CFO firms | $55B FAO market, 8% CAGR | Very High -- identical architecture |
| Financial advisory (RIAs) | ~15,000 firms | Medium -- similar client-serving pattern |

### Market Timing

The adoption window is open but narrowing:

- AI adoption in accounting: 9% (2024) → 41% (2025) -- a 4.5x jump in one year
- 77% of firms plan to increase AI investment (Intuit 2025)
- 82% of early adopters report positive ROI within the first year
- Big Four committed $9.5B to AI -- validating the market without serving SMB
- Gartner: by 2028, one-third of enterprise software includes agentic AI

First movers who establish data moats and switching costs by 2027-2028 will own the market. Late entrants will face entrenched incumbents.

---

## 6. Business Model and Unit Economics

### Pricing

| Tier | Firm Revenue | ACV | Monthly Platform |
|------|-------------|-----|-----------------|
| Starter | $2M-$10M | $18K-$30K | $1,500-$2,500/mo |
| Growth | $10M-$25M | $36K-$48K | $3,000-$4,000/mo |
| Scale | $25M-$50M | $48K-$72K | $4,000-$6,000/mo |

Plus one-time setup ($5K-$15K) and optional tuning retainer ($1K-$3K/mo).

**$40K ACV validated by six independent benchmarks:**
1. Vertical SaaS ACV median: $50K (we're below median)
2. Accounting firm IT budget: 3.5-5.25% of revenue ($350K-$525K for a $10M firm)
3. Managed IT services: $42K-$60K/year (a budget line firms already carry)
4. Fractional CFO services: $36K-$144K/year
5. Practice management software: $35K-$53K/year (Karbon, no AI included)
6. Revenue-per-employee ROI: 20% of one FTE's time recovered = $35K-$50K value

### Unit Economics

| Metric | Phase 1 | Phase 2-3 |
|--------|---------|-----------|
| Monthly cost per firm | ~$50 | ~$300-$500 |
| Monthly revenue per firm | $2,000-$3,500 | $3,500-$8,000 |
| Gross margin | 97-98% | 86-94% |
| LLM inference cost | $5-$50/mo | $5-$50/mo |
| Human time (ongoing) | 6-12 hrs/mo | 6-12 hrs/mo |

Gross margins are software-like. The local-first architecture means LLM inference costs are near zero compared to cloud-hosted competitors who operate at 55-70% gross margins. This structural cost advantage enables either aggressive pricing or reinvestment in the services layer.

### Revenue Expansion

Net Revenue Retention (NRR) above 120% is expected via:
- Firms start with Archetype 1 (Copilot) and expand to Archetype 2 (Explanation Engine)
- Additional integrations (Xero, Gusto, ADP) generate expansion revenue
- More users added within existing firms as adoption grows
- Advanced modules (Process Twin, benchmarking) available as paid upgrades

Vertical SaaS leaders average 120%+ NRR vs. 110% for horizontal SaaS (Windsor Drake Q4 2025).

---

## 7. Go-to-Market Strategy

### Phase 1: Founder-Led Sales (First 5 firms)

Mike personally sells, onboards, and supports. No sales team, no marketing funnel. Personal relationships.

1. Map warm network for accounting firm connections
2. Free assessment as the lead-gen offer
3. 30-day pilot with 3-5 staff at each firm
4. Convert to annual contract

### Phase 2: Referral-Driven (Firms 6-20)

Every happy firm generates referrals to 2-3 peers. Case studies fuel conference talks and thought leadership.

### Phase 3: PE Channel (20+ firms)

Private equity firms are acquiring accounting practices at an accelerating rate. One PE operating partner relationship = 5-20 firm deployments. PE firms need exactly what we build: operational intelligence, process standardization, and margin optimization data.

### The Flywheel

Each firm makes the product better: more data improves benchmarks, more questions improve AI training, more case studies strengthen proof, and cross-firm intelligence becomes a platform asset no competitor can replicate.

---

## 8. Competitive Landscape

### Direct Competitors

| Company | Focus | Threat | Our Advantage |
|---------|-------|--------|---------------|
| Truewind | AI bookkeeping | Medium | Point solution; we span all firm domains |
| Vic.ai | AP automation | Medium | AP-specific; we model the entire firm |
| Numeric | Month-end close | Medium | Close-specific; we cover the full lifecycle |
| Gravis AI | AI ERP for services | Medium-High | ERP replacement vs. our overlay approach |

### Why We Win

1. **Multi-system intelligence.** Competitors live inside one system. We connect all of them into a unified brain.
2. **Data moat.** Every day of usage accumulates firm-specific operational intelligence. Switching costs exceed $500K for mid-market vertical SaaS customers.
3. **Cross-firm network effects.** Anonymized benchmarking improves for every firm as the portfolio grows.
4. **Domain founder.** 18 years of accounting experience means we build what matters, not what sounds good in a pitch.
5. **PE distribution channel.** One PE relationship = many firm deployments. This channel scales linearly with PE activity.

---

## 9. Team

### Founders

**Mike Leavenworth -- CEO & Founder (75% equity)**
- 18+ years in accounting and finance
- Founder, ML Financial Group (accounting practice since 2017; active client of 9 years)
- Reviewed financial reporting across 60+ accountants for high-net-worth clients
- Career trajectory: Internal audit at Fortune 500 → Category management → Founded own practice → Building AI for the industry he knows
- Stanford Lean Startup; Institute of Internal Auditors Board Member
- Domain expertise that cannot be hired -- the founder IS the customer

**Owen [Last Name] -- Co-Founder & CTO (25% equity, 4-year vesting)**
- AI/ML engineering and research
- 20+ year collaborative relationship with founding team through open-source community
- Transitions to expanded role with this funding; developing into CTO position

### Advisory Board (6 formal advisors, 0.25% equity each)

| Domain | Qualification |
|--------|---------------|
| Cybersecurity & Compliance | Sr Cybersecurity Analyst, BMO (Bank of Montreal). US Navy veteran. 20+ years. NIST 800-53, PCI-DSS, vendor risk management. |
| AI & Engineering | Deep AI and coding expertise. Entrepreneurial builder with hands-on technical depth in modern AI tooling. |
| Marketing & GTM | Marketing strategy and go-to-market specialist. Critical for capturing 90%+ market share. |
| Operations & Problem-Solving | Versatile, committed, action-oriented. Willing to tackle any challenge. |
| Business Judgment | Grounded, practical advisor providing reality-check perspective. |
| [6th advisor - confirming] | Recently invited; marketing and strategy focus. |

### Informal Network

A senior software architect with 30+ years of experience (principal-level at a major technology company) serves as an informal mentor and contributes technical guidance through a shared community. Not a formal advisor due to conflict-of-interest constraints, but a meaningful resource.

---

## 10. Financial Projections

### Revenue Scenarios (Moderate = Plan)

| Year | Firms | Avg ACV | ARR | Cumulative Revenue |
|------|-------|---------|-----|-------------------|
| 2026 (H2) | 3 | $30K | $90K | $60K |
| 2027 | 15 | $38K | $570K | $460K |
| 2028 | 40 | $42K | $1.68M | $1.59M |
| 2029 | 80 | $44K | $3.52M | $4.20M |
| 2030 | 140 | $46K | $6.44M | $9.18M |
| 2031 | 220 | $48K | $10.56M | $17.98M |

### Key Milestones

| Milestone | Moderate Timing |
|-----------|----------------|
| First $100K ARR | Q2 2027 |
| $1M ARR | Q1 2028 |
| $5M ARR | Q2 2030 |
| $10M ARR | Q4 2031 |

### Valuation Implications

At 10x revenue (median for vertical SaaS, Windsor Drake Q4 2025):

| ARR | Implied Valuation |
|-----|-------------------|
| $100K | $1M |
| $500K | $5M |
| $1M | $10M |
| $5M | $50M |
| $10M | $100M |

Early-stage multiples (15-25x ARR) apply at seed, compressing toward 8-12x as the company scales. The trajectory from a $3M-$3.5M friends-round cap to $6M-$8M at pre-seed to $10M+ at seed represents strong return potential for the earliest investors. Friends-round investors at a $3.5M cap who invest $75K would hold ~2.14% at conversion; if the seed round values the company at $15M, that $75K position is worth ~$320K -- a 4.3x return before the company reaches $1M ARR.

---

## 11. Risk Factors

We believe in transparent risk disclosure. These are the material risks and our mitigations:

| Risk | Severity | Mitigation |
|------|----------|------------|
| LLM hallucination on financial data | High | Every answer grounded in retrieved data; mandatory citations; verifier node; regression testing with 120+ automated tests |
| ERP incumbents add AI features | Medium | Incumbents are constrained to their own data; we connect all systems. Intuit won't integrate with Xero. |
| Price sensitivity at $40K ACV | Medium | Tiered pricing captures smaller firms; $40K is below vertical SaaS median; proven ROI against one FTE |
| Solo founder risk | Medium | Owen transitions to expanded role; first engineering hire with seed capital; advisory board provides interim expertise |
| Long sales cycles | Medium | Founder-led sales shortcut; free assessment as lead-gen; 30-day pilot reduces perceived risk |
| Data security concerns | High | Advisor with NIST/PCI-DSS expertise; security-first architecture; SOC 2 preparation planned for seed stage |
| Employment agreement constraints | Medium | Governed by California law with strong employee protections (Labor Code § 2870, B&P Code § 16600); IP developed independently on own time and equipment; attorney review in progress; if current employer invests (Stage 1 strategy), resolves by mutual agreement |

---

## 12. Terms and Use of Funds

The fundraise is structured in two stages to minimize dilution and maximize proof points before scaling.

### Stage 1: Friends Round (Current Raise)

**Instrument:** SAFE (Simple Agreement for Future Equity)
**Amount:** $50,000 (up to $75,000)
**Valuation cap:** $3,000,000-$3,500,000 (post-money)
**Discount:** None (standard post-money SAFE)
**Lead investor:** Strategic accounting firm (prospective first deployment customer)

**Use of funds:**

| Category | Amount | Purpose |
|----------|--------|---------|
| Legal & entity formation | $15K | Attorney review + opinion, C-Corp, IP assignment, E&O insurance |
| Owen compensation (12 mo) | $12K | $1K/month co-founder retention |
| Alpha deployment & hosting | $5K | Production hosting for first customer(s) |
| Conferences (2 events) | $6K | Travel + registration for customer acquisition |
| Sales materials | $3K | One-pager, demo environment, basic website |
| Reserve | $9K | Buffer for unexpected costs |

**Note:** The founder takes no salary from the company. Personal expenses ($4K/month) are covered by W-2 employment and ML Financial Group income ($30K/year). The founder already self-funds the business at ~$750-$1,200/month — including co-founder compensation (Owen at $115/week, authorized to double), AI tools (~$200/month), and subscriptions. Owen's line item formalizes his existing compensation under the entity. **This is pure growth capital** — no survival component.

**Milestone:** Entity formed, alpha deployed, 1-3 paying customers, first revenue.

### Stage 2: Pre-Seed (After Revenue)

**Instrument:** SAFE
**Amount:** $300,000-$500,000
**Valuation cap:** $6,000,000-$8,000,000 (post-money, justified by revenue)
**Prerequisite:** 1-3 paying customers, recurring revenue, deployed product

**Use of funds (12-18 month runway):**

| Category | Allocation | Purpose |
|----------|-----------|---------|
| Team expansion | 40% | Owen to 20+ hrs/week, founder salary increase, first contractor hires |
| Engineering | 25% | Multi-vendor integrations, security hardening, production infrastructure |
| Go-to-market | 20% | Sales execution, conference circuit, content engine, customer acquisition |
| Infrastructure & working capital | 15% | Cloud hosting at scale, compliance prep, contingency |

**Milestone:** 5-10 paying firms, $200K+ ARR, positioning for seed round at $10M-$20M valuation.

### Why Staged

Friends-round investors at a $3.5M cap who invest $50K hold ~1.43% at conversion. If the seed round values the company at $15M, that position is worth ~$215K (4.3x). The staged approach also means pre-seed investors enter at $6M-$8M with real revenue data -- dramatically de-risked compared to a single $400K raise at $4.5M with no revenue. And because the founder takes no salary and is already self-funding the entire business (including co-founder compensation) at ~$1,200/month, this raise has no survival component -- it is pure growth capital.

---

*This memo is confidential and intended for prospective investors only.
It does not constitute an offer to sell securities. Forward-looking statements
are based on current expectations and subject to significant uncertainty.*
