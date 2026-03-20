# Business Model: Dual License + Commission

**Author:** Michael Leavenworth
**Date:** March 16, 2026
**Status:** Vision — captures the full market potential of the digital twin platform

---

## The Insight

An accounting firm with 90 clients is not just one customer. It's a distribution channel to 90 businesses that need financial intelligence. If we build the product so firms can re-license it to their clients, we turn every firm into a revenue multiplier.

## The Model

### Two Revenue Streams Per Firm

| Stream | Payer | Amount | Frequency |
|--------|-------|--------|-----------|
| **Firm License** | Accounting firm | $100,000 | Annual |
| **Client Commission** | Accounting firm (pass-through) | 20% of client fees | Monthly |

### How It Works

1. **Accounting firm licenses Project Green** for $100,000/year. They get the full digital twin: AI-powered Q&A over their firm's financials, staff data, scheduling, and operations.

2. **Firm re-licenses to its clients.** Each client business (like Delray Dermatology) gets their own digital twin — AI-powered Q&A over their own books. The firm sets the price. Our recommended rate: **$1,000/month per client.**

3. **Project Green collects a 20% commission** on all client license fees. The firm keeps 80%. This is passive revenue for the firm — the software does the work.

## Unit Economics

### Per Firm (90 Clients)

```
Client license revenue to firm:
  $1,000/month × 12 months × 90 clients = $1,080,000/year

Project Green commission (20%):
  $1,080,000 × 0.20 = $216,000/year

Plus firm license fee:
  $100,000/year

Total Project Green revenue per firm:
  $316,000/year

Firm's net from client licenses:
  $1,080,000 - $216,000 = $864,000/year

Firm's ROI:
  $864,000 net revenue / $100,000 software cost = 8.6x return
```

### Why the Firm Says Yes

The firm pays $100,000 for software that generates $864,000 in net licensing revenue. That's an **8.6x annual return** on their software investment. The product pays for itself in the first 6 weeks of client deployments.

The firm also benefits operationally:
- Junior staff get instant answers instead of interrupting partners
- Client questions are handled 24/7 by the digital twin
- The gap analysis feature (Red answers) creates consulting engagements to improve client data
- Firms become more valuable to their clients, reducing churn

### Why the Client Says Yes

At $1,000/month, a business owner gets:
- Instant answers about their financials — no waiting for the quarterly review
- Trend analysis, projections, and overhead ratios on demand
- Data quality diagnostics that show exactly what's missing and how to fix it
- A direct line to their accounting firm's expertise, amplified by AI

For a business doing $2M+ in revenue, $12,000/year for real-time financial intelligence is trivial. It's less than one hour of partner time per month.

## Market Sizing

### Target Market: Small US Accounting Firms

| Metric | Value | Source |
|--------|-------|--------|
| Small accounting firms in the US | ~46,000 | AICPA / IBISWorld |
| Firms with 50-150 clients (sweet spot) | ~12,500 | Estimated |
| Realistic penetration (10% of sweet spot) | 1,250 firms | Conservative |

### Revenue at Scale

| Scenario | Firms | Revenue/Firm | Annual Revenue |
|----------|-------|-------------|----------------|
| **Early traction** (Year 2) | 10 | $316,000 | $3.2M |
| **Growth** (Year 3) | 50 | $316,000 | $15.8M |
| **Scale** (Year 4) | 250 | $316,000 | $79M |
| **Market leadership** (Year 5+) | 1,250 | $316,000 | $395M |

### Valuation Scenarios

| Revenue | Multiple | Market Cap |
|---------|----------|-----------|
| $15.8M (Year 3) | 10x (high-growth SaaS) | $158M |
| $79M (Year 4) | 8x | $632M |
| $395M (Year 5+) | 7x | $2.77B |

## The Flywheel

```
Firm deploys Project Green
  → Firm's clients get digital twins
    → Clients ask questions
      → Some questions reveal data gaps (Red answers)
        → Firm gets hired to fix the data
          → Better data → better answers → more usage
            → More clients want it → firm deploys to more clients
              → Project Green revenue grows with zero additional sales effort
```

Every Red answer is a consulting engagement for the firm. Every consulting engagement produces better data. Better data produces better answers. Better answers produce more usage. More usage reveals more gaps. The flywheel is self-reinforcing.

## What This Means for Product Development

1. **The product must work for both audiences.** Firm partners asking about their practice AND business owners asking about their own books. Epic 34 (Delray Dermatology) validates the client-facing use case.

2. **The Data Gap Protocol is a revenue engine.** When the product honestly identifies data limitations and recommends fixes, it creates natural demand for the firm's services. This is not a bug — it's the core business model.

3. **Multi-tenant architecture is essential.** One firm, many clients, each with isolated data. This is already built (Epic 19-25).

4. **Self-service onboarding for client books.** Firms need to be able to connect a new client's QBO in minutes, not days. The onboarding flow (Epic 20-22) serves this.

5. **The commission model requires usage tracking.** We need to track which clients are active and what the firm charges them. This is a future epic — not needed for alpha.

---

*This document captures the vision as of March 16, 2026. The immediate focus remains on validating the product with real data (Epic 34) and completing the Parr3 resolution before any go-to-market activity.*
