# Go-to-Market Playbook

> **2026-03-06 — STRATEGIC HOLD:** All public GTM execution (sales conversations, conference attendance, content publishing, outbound outreach) is **deliberately paused** pending resolution of the founder's employment agreement. The GTM plan below is complete and ready to execute the moment the legal gate clears. Product development continues privately at full speed so that the gap between "legal resolution" and "product in market" is as close to zero as possible. See [Risk Register R22](risk-register.md) and [Legal Prerequisites — Strategic Sequencing](fundraising/legal-prerequisites.md).

## Ideal Customer Profile (ICP)

Not "accounting firms." This specific firm:

### Primary ICP (Phase 1-2)

| Attribute | Criteria | Why |
|-----------|----------|-----|
| **Firm size** | 10-50 employees | Large enough to feel pain, small enough to decide fast |
| **Services** | Tax + bookkeeping/business management | Both functions use the same data; maximum value from one integration |
| **General ledger** | QuickBooks Online | Our first integration; most common in this segment |
| **Payroll** | Gusto (preferred) or ADP | Second integration priority |
| **Geography** | Within driving distance of Mike/Owen | Founder-led sales requires face time for first 3-5 firms |
| **Pain point** | Capacity constraints -- too much work, not enough people | The CPA shortage is the entry wedge |
| **Decision maker** | Managing partner or ops partner who feels the pain personally | Not a committee decision; one person who can say yes |
| **Technology stance** | Open to AI but hasn't committed to a solution yet | Easier to win a new category than displace an incumbent |

### Secondary ICP (Phase 3+)

| Attribute | Criteria |
|-----------|----------|
| **Firm size** | 50-200 employees |
| **Ownership** | PE-backed (operating partner is the champion) |
| **Services** | Full-service (tax, audit, advisory, business management) |
| **Pain point** | Operational standardization across acquired practices |

### Disqualifiers

Firms we walk away from (for now):

- Solo practitioners (too small, can't justify the price)
- Firms using desktop-only software (no cloud API to integrate)
- Firms with no documented processes at all (nothing for RAG to work with)
- Firms in active M&A transition (too distracted to adopt new technology)

## Positioning

### The Core Message

**"Ask this before you ask a human."**

That's the promise. It's simple, outcome-based, and doesn't require the buyer to understand AI, agents, RAG, or lakehouses. It speaks directly to the pain: people keep interrupting expensive people with questions that should be answerable without them.

### Messaging by Persona

| Persona | Their Pain | Our Message |
|---------|-----------|-------------|
| **Managing Partner** | "I spend half my day answering questions my team should know" | "Your AI twin knows what you know. Your team asks it first." |
| **Ops Partner** | "Every new hire takes 6 months to get up to speed" | "New hires get answers on day one. Your SOPs, your policies, your way." |
| **Senior Accountant** | "I get interrupted 20 times a day with the same questions" | "The AI handles the repeatable questions. You handle the ones that matter." |
| **Junior Associate** | "I don't know who to ask or where to find the answer" | "Ask the AI. It knows your firm's procedures and will point you to the right person when it doesn't." |

### What We Are NOT Saying

- We are NOT saying "AI will replace your staff" (fear, resistance)
- We are NOT saying "cutting-edge multi-agent LangGraph orchestration" (technical jargon)
- We are NOT saying "we're an ERP" (triggers comparison to things we're not)
- We ARE saying "your firm gets smarter every day" (aspiration, growth)

## Pricing Model

### Exploration: Three Pricing Structures

| Model | Structure | Pros | Cons |
|-------|-----------|------|------|
| **Per-firm flat fee** | $2,000-$5,000/month per firm | Simple; predictable for the customer | Doesn't scale with firm size or usage |
| **Per-user** | $100-$300/user/month | Scales with firm size; familiar SaaS model | Discourages adoption (fewer seats = lower cost) |
| **Tiered** | Base platform fee + per-user for active users | Balances predictability with scaling | More complex to explain |

### Recommended Starting Point

**Setup fee + monthly platform fee + optional services retainer:**

| Component | Price | Notes |
|-----------|-------|-------|
| **Firm Assessment** | Free | Lead generation; demonstrates value |
| **Twin Setup** | $5,000-$15,000 one-time | Covers integration, configuration, knowledge loading |
| **Monthly Platform** | $2,000-$5,000/month | Depends on firm size; includes up to N users |
| **Ongoing Tuning Retainer** | $1,000-$3,000/month (optional) | Monthly check-ins, new use cases, knowledge base updates |

**Annual contract value per firm: $30,000-$100,000**

This pricing is comparable to what firms pay for managed IT services or fractional CFO services -- a budget category they already understand.

### Pricing Validation Plan

- Test pricing in conversations with 10+ firms before committing
- Offer the first firm a discounted beta rate in exchange for a case study
- Track willingness-to-pay signals during demos
- Adjust based on perceived value, not cost

## Sales Motion

### Phase 1: Founder-Led Sales (First 5 Firms)

Mike and Owen personally sell, onboard, and support the first 5 firms. No sales team. No marketing funnel. Personal relationships.

**The process:**

1. **Identify** -- Map personal networks for accounting firm connections. Mike's and Owen's contacts, LinkedIn, local CPA society events.

2. **Warm introduction** -- Get introduced to the managing partner or ops partner. No cold outreach for the first 5.

3. **Free assessment** -- "Let us look at your firm's systems and processes for 30 minutes. We'll show you where AI can help." This is the lead gen offer.

4. **Demo** -- Show the product working on representative accounting data. Use the QBO sandbox data. "This is what your team's experience would look like."

5. **Pilot proposal** -- "Let us connect to your QuickBooks, load your SOPs, and run a 30-day pilot with 3-5 of your staff. Here's what we'll measure."

6. **Pilot** -- 30-day trial with active support. Weekly check-ins. Rapid iteration based on feedback.

7. **Convert** -- If the pilot proves value, convert to a paid annual contract.

### Phase 2: Referral-Driven Sales (Firms 6-20)

- Every happy firm generates referrals to 2-3 peer firms
- Case study from each firm fuels thought leadership content
- Conference talks and webinars as inbound lead generation
- QBO ProAdvisor network as a channel (accountants who recommend tools to other accountants)

### Phase 3: Channel Sales (20+ Firms)

- PE operating partners as a distribution channel (one PE firm = 5-20 portfolio accounting practices)
- Accounting technology consultants as referral partners
- Industry association partnerships

## The Flywheel

```
                    +---> Case Study
                    |         |
                    |         v
One Firm -------> Value --> Thought Leadership
                    |         |
                    |         v
                    |    Conference Talks
                    |         |
                    |         v
                    +--- Next Firm
                    |         |
                    |         v
                    |    Expanded Usage
                    |    (More use cases
                    |     at existing firm)
                    |         |
                    |         v
                    +--- Cross-Firm Data
                         (Benchmarks, patterns)
                              |
                              v
                         More Valuable
                         for Every Firm
```

**Each firm makes the product better:**
- More data = better benchmarks
- More questions = better agent training
- More use cases = broader product coverage
- More case studies = stronger sales proof

## Alpha Customer (Secured 2/22/2026)

### The Deal

We have our first alpha test customer. Terms: 99% discount for an unspecified period in exchange for serving as our alpha partner. Full details in [Alpha Customer Agreement](alpha-customer-agreement.md).

This validates several GTM assumptions:

1. **The "discount for alpha" tactic works.** We proposed a deep discount in exchange for being our alpha partner, and the customer accepted. This confirms that firms will engage with an early product if the risk is low enough.
2. **Founder-led sales works.** This deal was closed through personal relationships, exactly as the Phase 1 sales motion described.
3. **The pain is real.** A firm was willing to invest time in an unproven product, which signals genuine need.

### What This Means for GTM

- **Pricing validation is deferred.** At 99% discount, we are not testing price. We are testing product-market fit. Pricing validation begins when we convert this customer to a paid arrangement or when we engage the second customer.
- **The flywheel starts here.** If this alpha succeeds, it produces: a case study, a referenceable customer, real-world feedback that improves the product, and warm introductions to peer firms.
- **The "free assessment" step was skipped.** We went directly to alpha engagement. This suggests that for warm leads, the free assessment may not be necessary -- the relationship does the selling.

### Updated Beta Strategy

The local pharmacy opportunity (healthcare) remains available as a secondary validation. However, priorities are clear:

1. **Primary:** Deliver successfully to the alpha customer
2. **Secondary:** If bandwidth allows, pursue the pharmacy as a cross-vertical test
3. **Next:** Use alpha success to generate warm introductions to 2-3 additional firms

### Ideal Characteristics for Customer #2

With the alpha engagement underway, the next customer should test a different variable:

- Closer to standard pricing (50% discount, not 99%)
- Ideally a referral from the alpha customer
- Same ICP (10-50 person accounting firm, QBO, capacity-constrained)
- Willing to provide a case study

## Partnership Strategy

See [Lead Generation Target Lists](lead-gen-target-lists.md) for the full
directory of accounting organizations, state CPA societies, and technology
communities with membership details, directory access, and action steps.

### Tier 1: Direct Partnerships (Build Now)

| Partner Type | Value to Us | Value to Them |
|-------------|------------|---------------|
| **QBO ProAdvisors** | Access to accounting firm network | Cutting-edge tool to recommend to clients |
| **Local CPA societies** | Speaking opportunities, credibility | Innovation content for members |
| **Accounting technology consultants** | Referral channel | New product to include in tech stack recommendations |

### Tier 2: Strategic Partnerships (Build in Phase 2-3)

| Partner Type | Value to Us | Value to Them |
|-------------|------------|---------------|
| **PE operating partners** | Distribution channel (1 PE firm = many accounting firms) | Operational intelligence for portfolio firms |
| **Intuit/QuickBooks** | Co-marketing, deeper API access | AI-powered overlay that makes QBO more valuable |
| **Microsoft** | M365 Agents SDK co-development, distribution | Proof that their platform supports vertical AI solutions |

## Content and Thought Leadership Plan

### Content Calendar (Starting Phase 1)

| Format | Frequency | Topics |
|--------|-----------|--------|
| **LinkedIn posts** | 2-3x/week | Accounting AI trends, firm operations insights, behind-the-scenes of building |
| **Blog posts** | 2x/month | Deep dives: "How AI changes month-end close", "The CPA shortage and what AI can do about it" |
| **Conference talks** | Quarterly | Local CPA society events, accounting technology conferences |
| **Podcast appearances** | Monthly | Accounting and fintech podcasts (guest appearances) |
| **Case studies** | Per customer | Results, quotes, before/after metrics |

### Key Conferences to Target

- AICPA ENGAGE
- Intuit Connect / QuickBooks Connect
- Xerocon
- Scaling New Heights (Woodard)
- AccountingWEB Live
- Local state CPA society annual meetings
