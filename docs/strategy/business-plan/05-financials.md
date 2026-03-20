# Section 5: Financial Projections & Unit Economics

*Business plan section 5 — Project Green*

---

## 1. Unit Economics

### Cost to Serve One Firm

**LLM inference (monthly):** ~$5–$50 per firm depending on model mix (e.g. GPT-4o-mini or Gemini Flash for most queries; premium models only when needed) and query volume. Assumptions: on the order of 50 queries/day per firm, ~500 input + ~200 output tokens per query (multi-turn), 22 working days/month. Strategy: model routing, caching of common answers, and RAG precision keep cost low. Local models in development keep marginal cost near zero.

**Infrastructure (monthly):**

| Component | Phase 0–1 (MVP) | Phase 2–3 (Production) |
|-----------|------------------|--------------------------|
| Compute / hosting | $0 (local) or ~$20 (VPS) | $50–$200 (cloud VM/containers) |
| Data lakehouse | $0 (DuckLake local) | $50–$300 (e.g. Databricks, S3+compute) |
| Vector database | $0 (ChromaDB local) | $25–$70 (Qdrant, Pinecone) |
| LLM inference | $0 or $5–$50 | $5–$50 |
| Monitoring | $0 | $20–$50 |
| **Total per firm** | **~$0–$70/month** | **~$150–$670/month** |

**Human time (capacity constraint):** 20–40 hours one-time setup per firm; 6–12 hours/month ongoing (tuning, support). At 6–12 hours/month per firm and ~50% of a two-person team allocated to customer work, the team can support **~10–15 firms** before a dedicated customer-success or delivery hire is required. This is the binding constraint in Phase 1–2, not infrastructure cost.

### Gross Margin by Phase

| Phase | Monthly Cost per Firm | Monthly Revenue per Firm | Gross Margin |
|-------|------------------------|--------------------------|--------------|
| **Phase 1 (MVP)** | ~$50 | $2,000–$3,500 | **97–98%** |
| **Phase 2–3 (Production)** | ~$300–$500 | $3,500–$8,000 | **86–94%** |

Margins are software-like. The main cost at scale is human delivery (setup and tuning), which is captured in the pricing (setup fee and optional retainer). Local-first and efficient model routing keep LLM and infra cost low versus cloud-heavy competitors (often 55–70% gross margin), enabling competitive pricing or reinvestment in the services layer.

### Revenue Expansion and NRR

Net Revenue Retention above **120%** is expected from: (1) Archetype 1 → Archetype 2 expansion, (2) additional integrations (Xero, Gusto) and users within the firm, (3) Process Twin and benchmarking as paid upgrades. Vertical SaaS leaders average 120%+ NRR; our expansion levers align with that pattern.

### LTV / CAC (Directional)

| Metric | Value | Basis |
|--------|--------|--------|
| Average customer lifetime | 5+ years | Vertical SaaS retention; switching costs (data moat, integration depth) |
| Target annual churn | < 10% | Vertical SaaS leaders often < 8% |
| Blended annual gross profit per firm | ~$40K | Weighted by tier mix (Starter/Growth/Scale) |
| Customer LTV | $200K+ | 5 years × ~$40K gross profit |
| CAC (founder-led) | $5K–$10K | Time, travel, demo costs |
| CAC (scaled) | $15K–$25K | Sales, marketing, events |
| LTV/CAC | 8–20× | Above the 3× minimum threshold |

---

## 2. Revenue Projections

### Scenario Conventions

- **Conservative:** Slower customer adds; lower ACV; minimal new hires.
- **Moderate (plan):** Alpha converts to paid; 2–5 new firms per quarter; ACV ramps with tier mix.
- **Aggressive:** Faster adds and higher ACV; used for upside cases only.

All figures are directional. Alpha customer is currently at 99% discount; first "revenue" in projections assumes conversion to paid or a second paying customer.

### Moderate Scenario (Plan)

| Year | Firms | Avg ACV | ARR | Cumulative Revenue |
|------|-------|---------|-----|--------------------|
| 2026 (H2) | 3 | $30K | $90K | ~$60K |
| 2027 | 15 | $38K | $570K | ~$460K |
| 2028 | 40 | $42K | $1.68M | ~$1.59M |
| 2029 | 80 | $44K | $3.52M | ~$4.20M |
| 2030 | 140 | $46K | $6.44M | ~$9.18M |
| 2031 | 220 | $48K | $10.56M | ~$18M |

### Quarterly Build (Moderate) — First 18 Months

| Quarter | Firms | Setup + Recurring | Quarterly Revenue | Cumulative |
|---------|-------|-------------------|-------------------|------------|
| Q3 2026 | 1 | 1 beta/alpha convert | ~$11K–$15K | ~$11K–$15K |
| Q4 2026 | 2–3 | New setups + MRR | ~$17K–$42K | ~$28K–$57K |
| Q1 2027 | 4–6 | New setups + MRR | ~$34K–$95K | ~$62K–$152K |
| Q2 2027 | 6–10 | New setups + MRR | ~$46K–$155K | ~$108K–$307K |
| Q3 2027 | 10–15 | New setups + MRR | ~$80K–$265K | ~$188K–$572K |
| Q4 2027 | 15–20 | New setups + MRR | ~$115K–$355K | ~$303K–$927K |

**Year 1 (mid-2026 to mid-2027) revenue:** ~$100K–$150K (conservative to moderate).  
**Year 2 run rate (end 2027):** ~$360K (conservative) to ~$1.4M (moderate).

### Conservative Scenario (Slower Ramp)

| Quarter | Firms | Monthly Recurring | Quarterly Revenue | Cumulative |
|---------|-------|-------------------|-------------------|------------|
| Q3 2026 | 1 (beta) | $2,000 | ~$11,000 | ~$11,000 |
| Q4 2026 | 2 | $4,000 | ~$17,000 | ~$28,000 |
| Q1 2027 | 4 | $8,000 | ~$34,000 | ~$62,000 |
| Q2 2027 | 6 | $12,000 | ~$46,000 | ~$108,000 |
| Q3 2027 | 10 | $20,000 | ~$80,000 | ~$188,000 |
| Q4 2027 | 15 | $30,000 | ~$115,000 | ~$303,000 |

**Year 1:** ~$108K. **Year 2 run rate:** ~$360K ARR.

### Key Revenue Milestones (Moderate Plan)

| Milestone | Target Timing |
|-----------|----------------|
| First dollar of revenue | Q3 2026 (alpha convert or second customer) |
| First $100K ARR | Q2 2027 |
| $1M ARR | Q1 2028 |
| $5M ARR | Q2 2030 |
| $10M ARR | Q4 2031 |

---

## 3. Cost Structure

### Fixed Costs (Monthly)

| Category | Phase 0–1 | Phase 2 (1–20 firms) | Phase 3 (20+ firms) |
|----------|-----------|----------------------|---------------------|
| Tools (Cursor, collaboration, domain, etc.) | ~$300–$400 | ~$300–$500 | ~$500–$1,000 |
| Cloud / infrastructure (shared) | $0–$50 | $200–$500 | $500–$2,000 |
| LLM API (shared) | $0–$50 | $50–$200 | $200–$1,000 |
| **Total fixed** | **~$300–$400** | **~$600–$1,200** | **~$1,200–$4,000** |

Fixed costs scale with firm count and product maturity (e.g. production lakehouse, monitoring). Until multi-tenant production, a large share of cost is variable per firm.

### Variable Costs (Per Firm)

See "Cost to Serve" above: **~$50/month (Phase 1)** to **~$300–$500/month (Phase 2–3)**. Variable cost is dominated by infrastructure and LLM at scale; human time is the capacity constraint, not the marginal cost of one more firm once the team is in place.

### People Costs (When They Enter)

| Role | When | Approx. Annual Cost |
|------|------|----------------------|
| Mike (no salary from company) | Stage 1 (friends round) | $0 (W-2 + practice income covers personal expenses) |
| Owen (part-time → expanded) | Stage 1: $1K/mo retention; Stage 2: $4K/mo expanded | $12K → $48K |
| First hire (engineer or customer success) | When firm count exceeds ~10–15 or seed funding | $60K–$100K |

The founder takes no salary during Stage 1. Personal expenses (~$4K/month) are covered by the W-2 salary and ML Financial Group income ($30K/year). The founder already self-funds the entire business at ~$750-$1,200/month — Owen at $115/week (authorized to double to 10 hrs/week at $230/week), AI tools (~$200/month), subscriptions (~$75/month). Personal safety net of ~$60K exists separate from business capital. Owen's Stage 1 line item formalizes his existing compensation under the entity. Stage 1 raise ($50K) is pure growth capital. See Section 6 for the staged use of funds.

---

## 4. Key Financial Milestones and Decision Gates

| Milestone | Target Date | Significance |
|-----------|-------------|---------------|
| **First dollar of revenue** | Q3 2026 | Alpha convert to paid or second paying customer; validates willingness to pay. |
| **$10K MRR** | Q4 2026 | 3–5 firms at $2K–$3.5K/month; recurring base established. |
| **Infrastructure self-funding** | Q1 2027 | Revenue covers cloud, API, and tooling costs. |
| **$50K MRR** | Q3 2027 | ~10–15 firms; capacity limit of two-person team; trigger to consider first hire or capital. |
| **$100K MRR** | Q4 2027 | Sustainable base; decide bootstrap vs. raise for acceleration. |

---

## 5. Funding Context (Summary)

**Capital efficiency:** The founder is self-funding the entire business today at ~$750-$1,200/month — including co-founder compensation (Owen at $115/week, authorized to double), AI tools (~$200/month), and subscriptions (~$75/month). Personal expenses (~$4K/month) are covered by the W-2 salary and ML Financial Group income ($30K/year). A personal safety net of ~$60K ($40K 401K + $20K investments) exists separately from business capital. No external capital is required for the business to continue operating. The raise is pure growth capital.

**Staged external capital path:** The fundraise is structured in three stages, each gated by milestones:

1. **Friends Round ($50K, SAFE at $3M–$3.5M cap):** Entity formation, legal, first customer deployment, path to first revenue. Led by a strategic accounting firm investor (prospective first customer). Closeable in weeks with one check. Founder takes no salary; entire amount is growth capital.
2. **Pre-Seed ($300K–$500K, SAFE at $6M–$8M cap):** Team expansion, engineering, go-to-market execution. Raised after 1–3 paying customers prove the model. Milestone: 5–10 paying firms, $200K+ ARR.
3. **Seed ($1M–$2M, priced round at $10M–$20M):** Full team, PE channel, Archetype 2 production. Raised after significant ARR and repeatable sales motion.

**Bootstrap path remains viable:** Development funded by sweat equity and personal savings; first customers fund infra and tools. The staged approach is not survival-driven — it is an acceleration strategy that preserves equity by raising at progressively higher valuations. Any specific "ask" (amounts, instruments, use of funds) is in Section 6.

---

## 6. Valuation Implications (Reference)

At **10× revenue** (median for vertical SaaS): $100K ARR ≈ $1M valuation; $500K ≈ $5M; $1M ≈ $10M; $5M ≈ $50M; $10M ≈ $100M. Early-stage (seed) multiples often 15–25× ARR; later stages trend toward 8–12×. Used for context in investor discussions and optionality (bootstrap vs. raise); not a commitment to a specific valuation.

---

## 7. Sensitivity and Risk (Financial)

- **Slower acquisition:** If customers close in 9 months instead of 3, revenue and cash flow shift right; runway and milestone dates extend. Bootstrap remains viable with a longer path to $100K ARR.
- **Lower ACV:** If blended ACV is ~$24K instead of ~$40K (e.g. 40% lower), ARR and valuation drop proportionally; unit economics stay profitable (e.g. 82%+ gross margin on Starter tier). Business remains viable; growth and valuation are slower.
- **Higher burn:** Adding a full-time hire before revenue or funding shortens runway; recommended only if customer acquisition is ahead of plan or capital is secured.

---

## Summary

- **Unit economics:** ~$50/month cost per firm (Phase 1), ~$300–$500 (Phase 2–3); gross margin 97–98% / 86–94%. Human time (6–12 hrs/month per firm) caps a two-person team at ~10–15 firms. NRR >120% from expansion.
- **Revenue (moderate plan):** 2026 H2 ~$90K ARR (3 firms); 2027 ~$570K (15 firms); 2028 ~$1.68M (40 firms); 2030 ~$6.44M (140 firms); 2031 ~$10.56M (220 firms). Key milestones: first revenue Q3 2026, $100K ARR Q2 2027, $1M ARR Q1 2028.
- **Cost structure:** Fixed ~$300–$400/month (Phase 0–1) to ~$1,200–$4,000 (Phase 3); variable ~$50–$500 per firm per month. First hire when firm count or funding justifies it.
- **Funding:** Bootstrap viable to ~10+ firms. Staged raise: friends round $50K → pre-seed $300K–$500K → seed $1M–$2M. Founder takes no salary during Stage 1; business self-funded at ~$1,200/month (including co-founder pay); raise is pure growth capital. Valuation context: 10× revenue median; 15–25× at seed.
- **Sensitivity:** Slower acquisition or lower ACV extends timeline or reduces valuation; unit economics remain profitable. Avoid adding fixed cost (e.g. full-time hire) before revenue or funding unless acquisition is ahead of plan.
