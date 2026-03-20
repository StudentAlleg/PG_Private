# Section 4: Business Model, GTM & Sales

*Business plan section 4 — Project Green*

---

## 1. Business Model Overview

Project Green operates a **services-plus-software** model: a productized platform (the AI twin) wrapped in professional services (assessment, setup, tuning). We do not sell pure SaaS; firms buy an outcome—“we build your firm’s AI twin”—delivered through a combination of software and human delivery. Revenue comes from one-time setup, recurring platform access, and optional ongoing services. This structure matches how firms already buy managed IT, fractional CFO, and practice management: they expect a relationship and implementation support, not self-serve tooling, when the product touches their financial data and operations.

---

## 2. Revenue Streams and Pricing

### Revenue Streams

| Stream | Type | Timing | Description |
|--------|------|--------|-------------|
| **Twin Setup** | One-time | At onboarding | Connect data sources (QBO, etc.), configure agents, load firm knowledge (SOPs, policies). |
| **Platform Fee** | Recurring monthly | Ongoing | Core access to the AI twin; includes a defined number of users. |
| **Tuning Retainer** | Recurring monthly | Optional, ongoing | Monthly check-ins, new use cases, knowledge base updates, optimization. |
| **Expansion Projects** | One-time or recurring | As needed | Add Archetype 2 (Explanation Engine), new integrations (Xero, Gusto), Process Twin modules; project- or module-priced. |

### Pricing Structure

**Setup + platform + optional retainer:**

| Component | Range | Notes |
|-----------|--------|--------|
| **Firm Assessment** | Free | Lead generation; demonstrates value and builds trust. |
| **Twin Setup** | $5,000–$15,000 one-time | Covers integration, configuration, knowledge loading. |
| **Monthly Platform** | $2,000–$5,000/month | Varies by firm size and tier; includes up to N users. |
| **Ongoing Tuning Retainer** | $1,000–$3,000/month (optional) | Monthly check-ins, new use cases, knowledge updates. |

**Tiered ACV by firm size (representative):**

| Tier | Firm Revenue | ACV (approx.) | Monthly Platform |
|------|-------------|---------------|------------------|
| Starter | $2M–$10M | $18K–$30K | $1,500–$2,500/mo |
| Growth | $10M–$25M | $36K–$48K | $3,000–$4,000/mo |
| Scale | $25M–$50M | $48K–$72K | $4,000–$6,000/mo |

**Target ACV for first 5 firms:** $30,000–$70,000 per firm (blended). Full-year target ACV at scale: ~$40K (validated against vertical SaaS medians, accounting firm IT budgets, managed services, practice management software, and ROI from recovered partner time).

### Pricing Validation

Pricing is anchored to existing budget categories (managed IT, fractional CFO, practice management) and to value (e.g. recovery of 20% of one FTE’s time). Validation plan: test in 10+ firm conversations; use first customer(s) as beta/discounted engagements in exchange for case studies and feedback; refine based on willingness-to-pay and perceived value, not cost.

---

## 3. Unit Economics (Summary)

**Cost to serve one firm:**

- **LLM inference:** ~$5–$50/month depending on model mix and query volume (local or low-cost cloud models).
- **Infrastructure (MVP):** ~$0–$70/month (local or single VPS). At production scale: ~$150–$670/month per firm (hosting, lakehouse, vector DB, monitoring).
- **Human time:** 20–40 hours one-time setup; 6–12 hours/month ongoing (tuning, support). This is the main capacity constraint for a small team.

**Gross margin:** Software-like. Phase 1: ~97–98% (revenue $2K–$3.5K/month per firm, cost ~$50). Phase 2–3: ~86–94% (revenue $3.5K–$8K/month, cost ~$300–$500). Local-first and efficient model routing keep inference cost low versus cloud-heavy competitors (55–70% gross margin), enabling either competitive pricing or reinvestment in the services layer.

**Revenue expansion:** Net Revenue Retention above 120% is expected from: (1) Archetype 1 → Archetype 2 expansion, (2) additional integrations and users within the firm, (3) Process Twin and benchmarking as paid upgrades. Vertical SaaS benchmarks support this range. Detailed projections are in Section 5 (Financials).

---

## 4. Ideal Customer Profile and Disqualifiers

**Primary ICP (Phase 1–2):**

| Attribute | Criteria | Rationale |
|-----------|----------|------------|
| Firm size | 10–50 employees | Large enough to feel pain, small enough to decide quickly. |
| Services | Tax + bookkeeping / business management | Same data, maximum value from one integration. |
| General ledger | QuickBooks Online | First integration; most common in segment. |
| Geography | Within reach of founder (driving distance or strong relationship) | Founder-led sales and support for first 3–5 firms. |
| Pain | Capacity constraints; too much work, not enough people; knowledge loss | CPA shortage and partner bottleneck as entry wedge. |
| Decision maker | Managing partner or ops partner who feels the pain | Single decision maker who can say yes. |
| Technology stance | Open to AI but not yet committed to a solution | Easier to win in a new category than to displace an incumbent. |

**Secondary ICP (Phase 3+):** 50–200 person firms; PE-backed (operating partner as champion); full-service (tax, audit, advisory); need for operational standardization across acquired practices.

**Disqualifiers (for now):** Solo practitioners (too small); desktop-only software (no cloud API); no documented processes (nothing for RAG); firms in active M&A transition (too distracted).

---

## 5. Positioning and Messaging

**Core message:** *“Ask this before you ask a human.”*

Outcome-based, not technology-based. It speaks to the pain (interruptions, capacity, slow answers) without requiring the buyer to understand AI, agents, or lakehouses.

**By persona:**

| Persona | Pain | Our message |
|---------|------|-------------|
| Managing Partner | “I spend half my day on questions my team should know.” | “Your AI twin knows what you know. Your team asks it first.” |
| Ops Partner | “Every new hire takes months to get up to speed.” | “New hires get answers on day one. Your SOPs, your policies, your way.” |
| Senior Accountant | “I get interrupted constantly with the same questions.” | “The AI handles repeatable questions. You handle the ones that matter.” |
| Junior Associate | “I don’t know who to ask or where to find the answer.” | “Ask the AI. It knows your firm’s procedures and points you to the right person when it doesn’t.” |

**What we do not say:** We do not say “AI will replace your staff.” We do not lead with technical jargon (LangGraph, RAG, etc.). We do not position as an ERP. We do say “your firm gets smarter every day” (aspiration, growth).

**Dual mode for lead gen vs. product:** For lead generation (cold/warm outreach, content, conferences), we lead with “AI digital transformation” and a consultative, problem-first frame. For demos and pilot proposals, we switch to product positioning: “Ask this before you ask a human” and show the product on representative data.

---

## 6. Sales Motion

### Phase 1: Founder-Led Sales (First 5 Firms)

Mike (and Owen where relevant) personally sell, onboard, and support. No dedicated sales team or paid funnel. Reliance on personal relationships and warm introductions.

**Process:**

1. **Identify** — Map networks for accounting firm connections (personal contacts, LinkedIn, local CPA society, ProAdvisor networks).
2. **Warm introduction** — Get introduced to managing partner or ops partner. No cold outreach for the first 5.
3. **Free assessment** — “Let us look at your firm’s systems and processes. We’ll show you where AI can help.” Lead-gen offer; builds trust.
4. **Demo** — Show the product on representative accounting data (e.g. QBO sandbox). “This is what your team’s experience would look like.”
5. **Pilot proposal** — “Connect your QuickBooks, load your SOPs, run a 30-day pilot with 3–5 staff. Here’s what we’ll measure.”
6. **Pilot** — 30-day trial with active support, weekly check-ins, rapid iteration.
7. **Convert** — Convert to paid annual contract when value is proven.

**Alpha customer (secured Feb 2026):** First “customer” is an alpha partner at 99% discount in exchange for alpha partnership. This validates that the “discount for alpha” tactic works, that founder-led sales works, and that the pain is real. Pricing validation is deferred until conversion to paid or engagement of the second customer. The flywheel starts with this engagement: case study, reference, feedback, and warm intros to peers.

### Phase 2: Referral-Driven (Firms 6–20)

- Every satisfied firm generates referrals to 2–3 peers.
- Case studies fuel conference talks, webinars, and thought leadership.
- QBO ProAdvisor and accounting tech consultant networks as referral channels.
- Content and conferences (e.g. state CPA societies, Scaling New Heights, Intuit Connect) drive inbound interest.

### Phase 3: Channel Sales (20+ Firms)

- **PE operating partners** — One PE relationship can mean 5–20 portfolio accounting practices. PE needs operational intelligence, standardization, and margin data; we become the recommended platform.
- **Accounting technology consultants** — Referral partners who include us in tech stack recommendations.
- **Industry associations** — Partnerships and visibility through AICPA, state societies, and accounting technology communities.

---

## 7. The Flywheel

Each new firm increases the value of the product and the efficiency of sales:

- **More data** → better benchmarks and patterns (anonymized) for all firms.
- **More questions and usage** → better agent behavior and training signal.
- **More use cases** → broader product coverage and expansion revenue.
- **More case studies** → stronger proof and easier conversion of the next firm.

One firm delivers value → case study and thought leadership → conference talks and referrals → next firm → expanded usage and cross-firm data → product more valuable for every firm. The flywheel is the same whether we stay bootstrap or raise capital; the only variable is how fast we spin it.

---

## 8. Partnerships and Content

**Partnerships (build in Phase 1–2):** QBO ProAdvisors (access to accounting firm network), local CPA societies (speaking, credibility), accounting technology consultants (referrals). **Phase 2–3:** PE operating partners, Intuit/QuickBooks (co-marketing, API), Microsoft (M365 Agents SDK, distribution).

**Content and thought leadership:** LinkedIn 2–3×/week (trends, operations, build updates); blog 2×/month (deep dives on AI and accounting); conference talks quarterly; podcast appearances monthly; case study per customer. Conferences: AICPA ENGAGE, Intuit Connect, Xerocon, Scaling New Heights, AccountingWEB Live, state CPA society meetings. See also lead-gen target lists for organizations and directories.

---

## 9. Customer #2 and Beyond

With the alpha engagement in place, the next customer should test a different variable: closer to standard pricing (e.g. 50% discount rather than 99%), ideally a referral from the alpha customer, same ICP (10–50 person, QBO, capacity-constrained), and willing to provide a case study. Each subsequent customer de-risks repeatability of onboarding and pricing.

---

## Summary

- **Business model:** Services-plus-software. Revenue from setup (one-time), platform fee (recurring), optional tuning retainer, and expansion projects. Target ACV $30K–$70K for first 5 firms; ~$40K at scale.
- **Unit economics:** High gross margin (97–98% Phase 1, 86–94% Phase 2–3); main constraint is human time (6–12 hrs/month per firm). NRR >120% from archetype expansion, integrations, and modules.
- **ICP:** 10–50 person firms, tax + bookkeeping, QBO, reachable, managing partner who feels capacity/knowledge pain. Disqualify solo, desktop-only, no processes, active M&A.
- **Positioning:** “Ask this before you ask a human.” Persona-specific messages; no fear-based or technical positioning.
- **Sales:** Phase 1 founder-led (warm intro → assessment → demo → pilot → convert); Phase 2 referral and content; Phase 3 PE and consultant channels.
- **Alpha customer:** Validates founder-led motion and “discount for alpha”; flywheel and pricing validation start with conversion and customer #2.
