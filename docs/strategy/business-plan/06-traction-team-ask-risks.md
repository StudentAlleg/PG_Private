# Section 6: Traction, Team, Ask & Risks

*Business plan section 6 — Project Green*

---

## 1. Traction

### Milestones Achieved

| Date | Milestone | Significance |
|------|-----------|--------------|
| **2026-02-22** | **First alpha test customer secured** | Agreement signed: 99% discount in exchange for alpha partnership. Project Green has a committed customer to deliver to. Validates market interest and shifts the project from prototyping to production delivery. |

The alpha engagement confirms that (1) the “discount for alpha” tactic works, (2) founder-led sales works for this segment, and (3) the pain is real—a firm was willing to invest time in an early product.

### Product and Platform Status (as of 2026)

| Dimension | Status |
|-----------|--------|
| **Multi-agent system** | Orchestrator + firm, client, and document specialists; 8 tool modules (ledger, analytics, staff, time/billing, scheduling, tax, payroll, documents). |
| **Correctness** | 120+ automated tests with structured evaluation framework; iterating toward production accuracy. |
| **Evaluation and quality** | 120+ automated tests; benchmarking framework for regression. |
| **Data layer** | DuckDB/DuckLake medallion architecture; QuickBooks Online integration in progress. |
| **RAG** | ChromaDB-based pipeline in progress for document Q&A. |
| **Interface** | Streamlit chat UI with message history and tool-call visibility. |

The product is demonstrable today. Remaining Phase 0 work (QBO live, RAG production-ready) is required for the alpha customer to use it in daily operations, not for first conversations.

### 2026 Objectives and Status

| Objective | Success criteria | Status |
|-----------|------------------|--------|
| **Ship a beta product** | Working Staff Copilot answering real questions for one firm; firm uses it daily without prompting | **Committed** — alpha customer secured 2/22; production delivery underway |
| **Develop go-to-market plan** | Documented ICP, messaging, pricing, sales motion; messaging tested with 10+ conversations | In progress — GTM docs complete; alpha validates “99% discount for alpha” |
| **Land Owen in full-time employment** | Skills development and capital generation | Unchanged (external to Project Green) |
| **Land first paying customer** | Revenue from one firm using the product; customer retains after 90 days | **On track** — alpha is the path to conversion; paid engagement follows successful alpha |
| **Build the growth flywheel** | Case study from first customer; 3+ warm leads; pipeline of 5+ qualified firms | Dependent on alpha success |

### Next Steps (Post–Alpha)

1. **Deliver to alpha** — Harden security, error handling, and deployment; connect customer’s QBO and documents; meet success criteria (operational system, trustworthy answers, 3–5 staff using it, path to paid).
2. **Convert alpha to paid** — Transition from 99% discount to paid arrangement when value is proven.
3. **Customer #2** — Ideally a referral from alpha; test pricing closer to standard (e.g. 50% discount); same ICP; case study and reference.
4. **Pipeline** — Use alpha success for warm introductions to 2–3 additional firms; begin testing messaging with 10+ firm conversations.

---

## 2. Team

### Founders

**Mike Leavenworth — CEO & Founder (75% equity)**  
18+ years in accounting and finance. Founder, ML Financial Group (accounting practice since 2017; active client of 9 years). Reviewed financial reporting across 60+ accountants for high-net-worth clients. Career path: internal audit at Fortune 500 → category management → founded own practice → building AI for the industry he knows. Stanford Lean Startup; Institute of Internal Auditors Board Member. Domain expertise that cannot be hired—the founder is the customer.

**Owen Peterson — Co-Founder & CTO (25% equity, 4-year vesting)**  
AI/ML engineering and research. 10+ year collaborative relationship with the founding team through the open-source community. Transitions to expanded role with funding; developing into CTO position. As we scale, we plan to bring on an experienced CTO through equity dilution shared across founders. This hire would work collaboratively with Owen and the CEO in a knowledge-sharing arrangement designed to accelerate technical leadership across the team.

### Advisory Board (6 formal advisors, 0.25% equity each)

| Domain | Qualification |
|--------|----------------|
| Cybersecurity & Compliance | Sr Cybersecurity Analyst, BMO. US Navy veteran. 20+ years. NIST 800-53, PCI-DSS, vendor risk management. |
| AI & Engineering | Deep AI and coding expertise. Entrepreneurial builder with hands-on depth in modern AI tooling. |
| Marketing & GTM | Marketing strategy and go-to-market. Critical for scaling. |
| Operations & Problem-Solving | Versatile, committed, action-oriented. |
| Business Judgment | Grounded, practical reality-check perspective. |
| Legal & Dealmaking | Active search; finalizing. Seeking counsel with startup, corporate, and transaction expertise to advise on entity formation, fundraising, and strategic partnerships. |

### Informal Network

A senior software architect (30+ years, principal-level at a major technology company) serves as an informal mentor and provides technical guidance through a shared community. Not a formal advisor due to conflict-of-interest constraints.

---

## 3. The Ask (Fundraising Path)

If Project Green raises external capital, the fundraise is structured in stages to minimize dilution and maximize proof points before scaling. The business plan is also executable on a bootstrap path (see Section 5); the ask is for the fundraising scenario.

### Stage 1: Friends Round

| Term | Detail |
|------|--------|
| **Instrument** | SAFE (Simple Agreement for Future Equity) |
| **Amount** | $50,000–$75,000 |
| **Valuation cap** | $3,000,000–$3,500,000 (post-money) |
| **Lead investor** | Strategic accounting firm (prospective first deployment customer) |

**Use of funds:**

| Category | Amount | Purpose |
|----------|--------|---------|
| **Legal & entity formation** | $15K | Attorney review + opinion, C-Corp, IP assignment, E&O insurance |
| **Owen compensation (12 mo)** | $12K | $1K/month co-founder retention |
| **Alpha deployment & hosting** | $5K | Production hosting for first customer(s) |
| **Conferences (2 events)** | $6K | Travel + registration for customer acquisition |
| **Sales materials** | $3K | One-pager, demo environment, basic website |
| **Reserve** | $9K | Buffer for unexpected costs |

Note: the founder takes no salary from the company during Stage 1. Personal expenses are covered by the W-2 and practice income. The founder already self-funds the entire business (including Owen's compensation) at ~$750-$1,200/month. Owen's line item formalizes his existing compensation under the entity. This raise is pure growth capital.

**Milestone:** Entity formed, legally clear, alpha deployed, 1–3 paying customers, first revenue.

### Stage 2: Pre-Seed

| Term | Detail |
|------|--------|
| **Instrument** | SAFE |
| **Amount** | $300,000–$500,000 |
| **Valuation cap** | $6,000,000–$8,000,000 (post-money, justified by revenue) |
| **Prerequisite** | 1–3 paying customers, recurring revenue, deployed product |

**Use of funds (12–18 month runway):**

| Category | Allocation | Purpose |
|----------|-----------|---------|
| **Team expansion** | 40% | Owen to 20+ hrs/week, founder salary increase, first contractor hires |
| **Engineering** | 25% | Multi-vendor integrations (Xero, Gusto), security hardening, production infrastructure |
| **Go-to-market** | 20% | Sales execution, conference circuit, content engine, customer acquisition |
| **Infrastructure & working capital** | 15% | Cloud hosting at scale, compliance prep, contingency |

**Milestone:** 5–10 paying firms, $200K+ ARR, positioning for seed round at $10M–$20M valuation.

---

## 4. Risk Factors and Mitigations

We disclose material risks and how we address them. Probability and impact are directional.

### Competitive Risks

| Risk | Severity | Mitigation |
|------|----------|------------|
| **Big Four build SMB product** | Low prob., high impact | Move fast; build firm-specific data moats and integration depth. Big Four move slowly; target 50+ firms before any downmarket move. |
| **ERP incumbents (e.g. Intuit) add agent features** | High prob., medium impact | Position as overlay connecting all systems; Intuit cannot be the multi-system layer (e.g. won’t integrate Xero). |
| **Well-funded startup wins segment** | Medium | Speed and focus; small team ships fast. Most startups are point solutions; we are multi-domain. |
| **Horizontal AI (ChatGPT, Claude) “good enough”** | Medium | Generic AI cannot access firm data or enforce access control. Demo the gap: “What was account 1000’s balance?” requires firm data. |

### Technical Risks

| Risk | Severity | Mitigation |
|------|----------|------------|
| **LLM hallucination on financial data** | High | Ground every answer in retrieved data; mandatory citations; verifier node; regression testing with 120+ automated tests. |
| **Data quality from vendor APIs** | Medium | Silver-layer data quality checks; flag issues to firm as a service; start with firms with reasonably clean books. |
| **Integration complexity** | Medium | One integration first (QBO); MCP isolates integrations; budget 2× time per integration. |

### Regulatory and Liability Risks

| Risk | Severity | Mitigation |
|------|----------|------------|
| **AI liability for accounting advice** | High impact | Archetype 1 internal-only; Archetype 2 explains, never advises; guardrails and terms; citations for verification. |
| **Data privacy regulations** | Medium | Data in firm-controlled environments where possible; encryption; multi-tenant isolation; clear data agreements. |

### Market and Execution Risks

| Risk | Severity | Mitigation |
|------|----------|------------|
| **Firms adopt AI slower than expected** | Medium | Free assessment and 30-day pilot reduce commitment; internal-only Archetype 1 is lowest-friction deployment. |
| **Two-person team capacity** | High | Ruthless prioritization; one firm, one use case at MVP; automate (CI/CD, testing); first hire at 10–15 firms. |
| **Owen’s split focus** | Medium | Planned; modular architecture allows parallel work; Owen’s employment can fund infra. |
| **Long sales cycles** | Medium | Founder-led sales and free assessment; 30-day pilot reduces perceived risk. |
| **Price sensitivity at target ACV** | Medium | Tiered pricing; $40K below vertical SaaS median; ROI anchored to recovered FTE time. |

### Alpha-Specific Risks

| Risk | Severity | Mitigation |
|------|----------|------------|
| **Product readiness gap** | High | Security hardening and error handling first; production readiness checklist; deploy with Docker. |
| **Alpha expectations exceed delivery** | Medium | Clear scope; transparency on what the system can and cannot do; structured feedback and triage. |
| **Reputation risk from poor alpha** | Medium | Treat alpha as production-grade delivery; 24-hour response on issues; avoid scope creep. |

### Other

| Risk | Severity | Mitigation |
|------|----------|------------|
| **Data security concerns** | High | Advisor with NIST/PCI-DSS expertise; security-first architecture; SOC 2 preparation at seed. |
| **Employment / IP constraints** | Medium | Governed by California law with strong employee protections (Labor Code § 2870, B&P Code § 16600); IP developed independently on own time/equipment; attorney review in progress; if current employer invests (Stage 1 strategy), resolves by mutual agreement. |

---

## Summary

- **Traction:** First alpha customer secured Feb 2026 (99% discount for alpha partnership). Product: 8 tool modules, 120+ automated tests, evaluation framework, chat UI; QBO and RAG in progress. 2026 objectives: ship beta to alpha, first paying customer via conversion, build flywheel. Next: deliver to alpha, convert to paid, land customer #2.
- **Team:** Mike (CEO, 75%) — 18+ years accounting/finance, domain founder. Owen (CTO, 25%, 4-year vesting) — AI/ML engineering, expanded role with funding. Six formal advisors (0.25% each): security, AI/engineering, marketing/GTM, operations, business judgment, marketing/strategy. Informal technical mentor.
- **Ask (fundraising path):** Staged raise — Stage 1 friends round $50K–$75K SAFE at $3M–$3.5M cap (entity, legal, first deployment, first revenue); Stage 2 pre-seed $300K–$500K SAFE at $6M–$8M cap after revenue (team, engineering, GTM). Total pre-seed dilution ~7.9% for $475K. Seed at $10M–$20M after significant ARR. Bootstrap path remains viable (Section 5).
- **Risks:** Competitive (Big Four, ERP, startups, horizontal AI); technical (LLM reliability, data quality, integration); regulatory (AI liability, privacy); market (adoption speed); execution (capacity, Owen split focus, sales cycles, price sensitivity); alpha (readiness, expectations, reputation); security and employment. Mitigations in place for each; early warning indicators and prioritization (e.g. security and alpha delivery first) reduce downside.
