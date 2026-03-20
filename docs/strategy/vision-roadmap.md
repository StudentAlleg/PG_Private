# Vision Roadmap: From First Customer to $2.7B

**Author:** Michael Leavenworth + Project Green Team
**Date:** March 16, 2026
**Status:** Operating Roadmap — the strategic arc from today to full market realization

---

## Where We Are

- 30 epics complete. 1755 tests. 96% coverage.
- Full AI agent pipeline: 4 specialist agents + orchestrator + verifier
- Multi-tenant architecture with firm/client scoping
- QBO, Xero, Gusto integrations built
- Security audit complete, remediation planned
- First test customer identified: Delray Dermatology (via ML Financial Group)
- Entity not yet formed. GTM paused pending Parr3 resolution.
- Zero revenue. Zero public presence. Full speed privately.

## Where We're Going

**$395M ARR. 1,250 firms. Each firm re-licensing to 90 clients. $2.7B market cap.**

The path has seven phases. Each phase has a clear gate — you don't advance until the gate criteria are met. This prevents premature scaling and keeps the team focused.

---

## Phase 0: Prove It Works (NOW — Q1 2026)

**Goal:** Demonstrate that the product answers real financial questions correctly using real customer data.

### Product Milestones
- [ ] Connect Delray Dermatology's live QBO data (API or CSV export)
- [ ] Load ADP payroll data for staffing structure
- [ ] Answer Delray's 3 test questions to Mike's satisfaction
- [ ] Run 1000-question gauntlet — establish baseline pass rate
- [ ] Produce Delray gap analysis document (the first deliverable)
- [ ] Tune Data Gap Protocol — Red answers guide clients toward better data

### Business Milestones
- [ ] Complete Intuit production app approval
- [ ] Grey Ocean delivers legal opinion on Parr3 employment agreement
- [ ] Kris Knutsen NDA v4 signed by both parties

### Gate → Phase 1
- Mike says: "The product answered those 3 questions the way I would have"
- 1000-question gauntlet: >70% Green pass rate, >80% Red gap identification rate
- No hallucinated financial data in any tested response

---

## Phase 1: First Alpha Customer (Q2 2026)

**Goal:** One accounting firm (ML Financial Group) uses the product daily with one real client's data. The product runs without Mike watching every query.

### Product Milestones
- [ ] Security Sprints 31-33 complete (WebSocket auth, encryption at rest, session management, secrets hardening)
- [ ] Conversation memory / session persistence (F1)
- [ ] Confidence-tiered responses (F4) — high/medium/low signals
- [ ] 30-minute onboarding flow (F6) — OAuth connect → sync → first question
- [ ] Follow-up question suggestions (F9) — teach users what the system can do
- [ ] Mobile-responsive assistant (F10)
- [ ] Cloud deployment — accessible outside Mike's local machine

### Business Milestones
- [ ] Parr3 resolution: legal opinion + conversation + outcome
- [ ] Entity formation (Delaware C-Corp)
- [ ] IP assignment to entity with clean chain of custody
- [ ] Owen and Kris formalized (equity agreements, FAST agreements)
- [ ] ML Financial Group becomes paying alpha customer ($0 or nominal — relationship pricing)

### Metrics to Track
- Daily active queries from ML Financial Group staff
- Answer quality scores (weekly sample review by Mike)
- Time saved per question vs. asking a partner manually
- Number of Red answers that convert to consulting engagements

### Gate → Phase 2
- ML Financial Group has used the product daily for 30+ days
- Mike confirms: "I trust this enough to let a junior staff member use it unsupervised"
- At least 1 consulting engagement generated from a Red answer (gap → engagement)
- Cloud deployment stable for 30 days without critical incidents

---

## Phase 2: First 5 Paying Firms (Q3-Q4 2026)

**Goal:** Prove the product works for firms that aren't run by the founder. Establish product-market fit. Generate first real revenue.

### Product Milestones
- [ ] Self-service firm onboarding — no Mike involvement required
- [ ] Scheduled digests (F2) — weekly email summaries for partners
- [ ] Cross-client benchmarking (F5) — "Rank my clients by profitability"
- [ ] Tax deadline intelligence (F7) — proactive deadline + document status
- [ ] Guided onboarding for junior staff (F8) — contextual starter questions
- [ ] Natural language report builder (F3) — charts, not just text
- [ ] Multi-firm admin dashboard — Mike can see all 5 firms' health

### Business Milestones
- [ ] Pricing validated: $100K/year firm license (or adjusted based on feedback)
- [ ] 5 signed annual contracts
- [ ] First revenue: $500K ARR (5 × $100K)
- [ ] Hire #1: Customer success / onboarding specialist
- [ ] Hire #2: Full-stack engineer (Owen can't be the only dev forever)
- [ ] Founder-led sales: Mike and Owen personally onboard each firm
- [ ] Case study from ML Financial Group published (with permission)
- [ ] Advisory board providing quarterly feedback

### Go-To-Market
- ICP: 10-50 person firms, QBO-based, within driving distance
- Channel: Mike's professional network + warm referrals from alpha
- Sales motion: Demo → 2-week pilot → annual contract
- Pricing: $100K/year (firm license only — no client re-licensing yet)

### Gate → Phase 3
- 5 firms paying and active for 90+ days
- Net Promoter Score > 40 from firm users
- <2% churn (nobody cancels in the first year)
- At least 3 firms asking: "Can my clients access this too?"

---

## Phase 3: Client Portal + Dual License Model (2027 H1)

**Goal:** Activate the dual-license business model. Firms re-license to their clients. Revenue multiplier kicks in.

### Product Milestones
- [ ] **Client Portal (F11)** — separate login for firm clients (biggest build)
  - Client role with firm-configurable guardrails
  - Response review queue for sensitive topics
  - Approved language framework (explains, doesn't advise)
  - Audit trail of every client-facing response
  - Kill switch per client/topic
- [ ] Usage tracking and billing infrastructure — track active clients per firm
- [ ] Commission calculation engine — automated 20% pass-through
- [ ] Client onboarding flow — firm connects a client's QBO in minutes
- [ ] Notification badges / ambient awareness (F12)
- [ ] Workflow automation triggers (F14) — watchdog mode

### Business Milestones
- [ ] Dual license agreement template created and legal-reviewed
- [ ] First 3 firms deploy to their clients
- [ ] Client re-licensing revenue begins flowing
- [ ] Revenue per firm increases from $100K to ~$316K (license + commission)
- [ ] Total firms: 15-25
- [ ] ARR: $2M-$5M
- [ ] Seed round or Series A ($2-5M) to fund scaling
- [ ] Hire: 2 more engineers, 1 sales, 1 customer success
- [ ] Team size: 8-10

### Unit Economics Validation
- Confirm firm ROI is 5x+ (client license revenue vs. software cost)
- Confirm client willingness to pay $500-$1,000/month
- Measure: queries/day per client, retention rate, support tickets

### Gate → Phase 4
- Dual-license model proven: at least 3 firms re-licensing to clients
- Client retention > 90% at 6 months
- Commission revenue > firm license revenue (the multiplier works)
- No legal/compliance incidents from client-facing responses

---

## Phase 4: Scale to 50 Firms (2027 H2 — 2028 H1)

**Goal:** Transition from founder-led sales to repeatable go-to-market. Build the data moat. Become the category leader for AI in small accounting firms.

### Product Milestones
- [ ] Microsoft Teams integration (F15) — meet firms where they work
- [ ] Multi-firm anonymized benchmarking (F13) — network effect moat
- [ ] White-label / embedded API (F16) — platform play begins
- [ ] Practice management integrations (Karbon, Canopy, TaxDome)
- [ ] Xero parity with QBO (full feature set for Xero-based firms)
- [ ] SOC 2 Type II certification

### Business Milestones
- [ ] 50 firms on platform, 30+ with client portal active
- [ ] ARR: $10M-$16M
- [ ] Series A or Series B ($10-20M)
- [ ] Sales team: 3-5 reps with quota
- [ ] Customer success team: 3-5 CSMs
- [ ] Engineering team: 8-12 engineers
- [ ] Team size: 25-35
- [ ] First channel partnerships (practice management vendors, accounting associations)
- [ ] Conference presence: QuickBooks Connect, AICPA Engage, Xerocon
- [ ] Content marketing: "State of AI in Accounting" annual report

### Competitive Moat Deepening
- **Data network effect:** 50 firms × 90 clients = 4,500 businesses generating benchmarking data. New firms join partly for the benchmarks. Competitors can't replicate this without the install base.
- **Switching cost:** Firms have configured guardrails, trained staff, built client relationships around the product. Ripping it out means losing client revenue.
- **Distribution advantage:** Every firm is a distribution channel to 90 clients. Competitors must sell to both firms AND convince them to re-sell. We already have the flywheel.

### Gate → Phase 5
- Repeatable sales motion: new firms onboard without founder involvement
- Benchmarking data set large enough to be statistically meaningful (30+ firms)
- At least 1 white-label / embedded partner live
- SOC 2 Type II certified

---

## Phase 5: Market Leadership — 250 Firms (2028-2029)

**Goal:** Dominate the small accounting firm segment. Begin upmarket expansion to PE-backed firms. Activate the Process Twin.

### Product Milestones
- [ ] **Process Twin (F17)** — operational simulation for PE-backed firms
  - How work flows through the firm
  - Bottleneck identification
  - What-if hiring simulation
  - Client profitability by service line
  - PE exit readiness scoring
- [ ] Tax Research Agent (F18) — IRC/state tax code RAG
- [ ] Audit Preparation Assistant (F19) — automated audit package compilation
- [ ] Multi-language support (F20) — Spanish first, then Mandarin
- [ ] API marketplace — third-party integrations built by partners

### Business Milestones
- [ ] 250 firms, 150+ with client portal active
- [ ] ARR: $50M-$79M
- [ ] ~15,000 client businesses on platform
- [ ] Series B or C ($30-50M)
- [ ] Team size: 80-120
- [ ] International expansion planning (UK, Australia — Xero-dominant markets)
- [ ] PE-backed firms as a distinct customer segment with dedicated sales
- [ ] Advisory partnerships with top-25 accounting firms
- [ ] Patent portfolio on key innovations (benchmarking methodology, gap protocol, process simulation)

### Gate → Phase 6
- Process Twin deployed to 10+ PE-backed firms
- International pilot (1 market outside US)
- Platform revenue (white-label + marketplace) > 15% of total revenue

---

## Phase 6: Full Market Penetration — 1,250 Firms (2029-2031)

**Goal:** Capture 10% of the sweet-spot market (12,500 firms with 50-150 clients). Achieve the dual-license unit economics at scale.

### Product Milestones
- [ ] Full operational intelligence platform — financial twin + process twin + tax research + audit prep
- [ ] Industry-specific modules (medical practices, law firms, construction, nonprofits)
- [ ] AI-native workflows — not just Q&A, but suggested actions with one-click execution
- [ ] Predictive analytics — "Based on current trends, here's what Q4 looks like"
- [ ] Client self-service data improvement — guided QBO Class setup, revenue categorization

### Business Milestones
- [ ] 1,250 firms on platform
- [ ] ~100,000 client businesses on platform
- [ ] ARR: $395M
- [ ] Commission revenue: $270M (68% of total — the multiplier dominates)
- [ ] Firm license revenue: $125M (32%)
- [ ] Team size: 300-500
- [ ] Offices: HQ + 2-3 regional / international
- [ ] IPO-ready or strategic acquisition conversations
- [ ] At 7x revenue multiple: **~$2.77B market cap**

---

## Phase 7: Beyond Accounting (2031+)

**Goal:** The technology is not accounting-specific. The digital twin architecture works for any professional service firm.

### Expansion Vectors
- **Law firms:** Case management, billing, client communication intelligence
- **Healthcare practices:** (Beyond dermatology) — operational intelligence for multi-location practices
- **Consulting firms:** Utilization optimization, project profitability, resource allocation
- **PE portfolio companies:** Operational intelligence across entire portfolios

### The Endgame
Project Green becomes the **operating intelligence layer for professional services** — the platform that makes every firm's data queryable, predictable, and continuously improving. The dual-license model scales to every vertical where firms serve clients.

---

## The Two Tracks

This roadmap has two parallel tracks that must stay synchronized:

### Track 1: Product (Build)

```
Phase 0: Real data validation (1000-question gauntlet)
  ↓
Phase 1: Alpha customer daily use (security + cloud + UX)
  ↓
Phase 2: 5 firms, self-service onboarding, reports
  ↓
Phase 3: Client portal + dual-license activation
  ↓
Phase 4: Teams integration, benchmarking, platform API
  ↓
Phase 5: Process Twin, tax research, audit prep
  ↓
Phase 6: Industry modules, predictive analytics
  ↓
Phase 7: Multi-vertical platform
```

### Track 2: Business (Grow)

```
Phase 0: Legal resolution, entity prep
  ↓
Phase 1: Entity formed, IP assigned, team formalized
  ↓
Phase 2: First revenue ($500K ARR), first hires
  ↓
Phase 3: Seed/Series A, dual-license revenue begins
  ↓
Phase 4: Series A/B, sales team, SOC 2, conferences
  ↓
Phase 5: Series B/C, international, PE segment
  ↓
Phase 6: $395M ARR, IPO-ready
  ↓
Phase 7: Multi-vertical expansion
```

---

## Key Assumptions

These assumptions underpin the financial projections. If any prove wrong, the model adjusts but the strategy holds:

| Assumption | Value | Sensitivity |
|-----------|-------|-------------|
| Average clients per firm | 90 | Model works at 50+; breaks below 30 |
| Client license price | $1,000/month | Range: $500-$2,000; model works at $500+ |
| Commission rate | 20% | Range: 15-25%; must exceed cost to serve |
| Firm license price | $100,000/year | Range: $50K-$150K; higher with Process Twin |
| Target market size | 12,500 firms | Conservative; 46,000 total, filtered to sweet spot |
| Market penetration | 10% | Industry standard for category leader in SMB SaaS |
| Revenue multiple | 7x | Range: 5-12x depending on growth rate and margins |
| Time to $395M ARR | 5-6 years from first revenue | Aggressive but achievable with dual-license flywheel |

---

## What Makes This Work

### The Flywheel

```
Firm deploys Project Green → Firm's clients get digital twins
  → Clients ask questions → Red answers reveal data gaps
    → Firm gets hired to fix the data → Better data, better answers
      → More clients want access → More commission revenue
        → Firm's ROI increases → Firm renews and expands
          → More firms hear about it → Network grows
```

### The Moats (Cumulative)

| Phase | Moat | Strength |
|-------|------|----------|
| 2 | Product quality + early mover | Weak — competitors can copy features |
| 3 | Distribution (firms as channels) | Medium — hard to replicate the firm relationship |
| 4 | Data network (benchmarking) | Strong — more firms = better data = more firms |
| 5 | Switching costs + platform ecosystem | Very strong — ripping out means losing client revenue |
| 6 | Category ownership | Dominant — "Project Green" = "AI for accounting firms" |

### The Risk Register

Critical risks that could derail the roadmap:

| Risk | Phase | Mitigation |
|------|-------|-----------|
| Parr3 employment agreement blocks entity formation | 0-1 | Grey Ocean legal opinion; clean IP chain regardless |
| Intuit restricts API access for competitive reasons | 1-2 | CSV fallback already built; Xero as alternate first integration |
| Large competitor (Intuit, Sage) builds similar product | 2-3 | They'll build for enterprise; we own SMB through distribution moat |
| Client-facing AI produces harmful financial advice | 3 | Guardrails, review queue, kill switch, "explains not advises" positioning |
| Firm churn exceeds 10% annually | 2-4 | Dual-license revenue makes the product too profitable to cancel |
| Fundraising environment deteriorates | 3-4 | Bootstrap path possible with dual-license revenue ($316K/firm covers costs) |

---

## Today's Priority

Phase 0. Prove it works. Everything else follows from that.

```
Sprint 34: Load Delray's real data → Answer 3 questions → Run the gauntlet
```

That's the next 5 days. If we nail this, every phase after it is execution.

---

*This document is the operating roadmap for Project Green. It will be updated as assumptions are validated or invalidated. Every strategy doc in `docs/strategy/` feeds into this timeline. The product roadmap (`docs/product-roadmap-future.md`) maps features to phases. The GTM playbook (`docs/strategy/go-to-market.md`) activates in Phase 2.*
