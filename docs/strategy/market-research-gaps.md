# Market Research Gaps

> An inventory of what we don't know yet and need to learn through
> research, customer conversations, and market testing. This document
> makes explicit what is assumed vs what is validated, and provides
> a structured research agenda.
>
> For the strategic analysis of market opportunities, see
> [market-gap-analysis.md](market-gap-analysis.md).
>
> This document feeds directly into the conversation agenda proposed
> in [traction-acceleration.md](traction-acceleration.md).
>
> **Date**: February 2026

---

## Research Status Legend

| Status | Meaning |
|--------|---------|
| **Covered** | Already researched in existing docs |
| **Partial** | Some data exists but incomplete |
| **Gap** | Not yet researched -- requires attention |
| **Assumption** | We believe this but haven't validated it |

---

## 1. Substitute Analysis

**Status**: Gap

What do firms do TODAY to solve the problems Project Green addresses?
We have assumptions but no validated data from conversations.

### Current Substitutes (Assumed)

| Problem | Substitute | Strengths | Weaknesses |
|---------|-----------|-----------|------------|
| "What was Client X's revenue last quarter?" | Ask a senior / search QBO | Fast if the senior is available | Senior is a bottleneck; QBO search is limited |
| "What's our policy on capitalizing expenses?" | Ask a partner / search SharePoint | Accurate from the right person | Knowledge walks out the door; search rarely works |
| "How are we performing this month?" | Excel dashboard updated manually | Familiar, trusted | Stale by the time it's done; hours to build |
| "Summarize this client's financials" | ChatGPT with pasted data | Quick, decent quality | No live data connection; confidentiality risk |
| "Where are our bottlenecks?" | Gut feeling / partner meeting | Captures institutional intuition | Subjective, not actionable, no data |
| "Compare us to other firms" | Industry surveys (AICPA, Rosenberg) | Authoritative benchmarks | Annual, retrospective, not firm-specific |

### What We Need to Learn

- [ ] Which substitutes are "good enough" (firms won't switch)?
- [ ] Which substitutes are painful (firms want something better)?
- [ ] What triggers the switch from substitute to purpose-built solution?
- [ ] How much time/money do firms spend on each substitute today?
- [ ] Are there substitutes we haven't considered?

### How to Learn It

- **Discovery conversations**: Ask firm owners "Walk me through what
  happens when a junior staff member has a question about a client."
- **Shadow sessions**: If possible, observe a day-in-the-life at a firm.
- **Survey**: Quick 5-question survey distributed through CPA networks.

---

## 2. Buyer Journey Map

**Status**: Gap

How does a firm owner actually decide to buy a technology product?
Our GTM strategy assumes a buyer journey but hasn't mapped it.

### Assumed Buyer Journey

```
Trigger Event --> Awareness --> Evaluation --> Decision --> Adoption --> Expansion
```

### What We Need to Learn

| Stage | Open Questions |
|-------|---------------|
| **Trigger** | What causes a firm to start looking? Losing a key staff member? Client complaint? Capacity crunch? Competitive pressure? PE directive? |
| **Awareness** | Where do firm owners learn about new tools? Conferences? Peer recommendations? Vendor outreach? Publications (Accounting Today, Journal of Accountancy)? Social media? |
| **Evaluation** | Who evaluates? (Partner? IT person? Office manager?) How long does evaluation take? What criteria matter most? Do they trial before buying? |
| **Decision** | Who makes the final decision? Is there a committee? What kills a deal? Budget cycle timing? |
| **Adoption** | What does onboarding look like? Who uses it first? How long until value is perceived? What causes churn in the first 90 days? |
| **Expansion** | What triggers expansion to more users or use cases? When does a firm become a reference customer? |

### How to Learn It

- **Customer conversations**: The traction acceleration plan targets
  5 conversations in the first 30 days. Dedicate part of each
  conversation to mapping the buyer journey.
- **Lost-deal analysis**: Once we have pipeline, track why firms say no.
- **Channel partners**: Accounting technology consultants (Right Networks,
  Woodard) know how firms buy.

---

## 3. Adoption Barrier Analysis

**Status**: Partial (general data exists; Project Green-specific data does not)

### Known Barriers (From Industry Research)

Per Deloitte's 2025-2026 survey and Thomson Reuters research:

| Barrier | Severity | Evidence |
|---------|----------|---------|
| **Trust** | Critical | Only 2.7% of finance professionals fully trust AI agents; 19.9% don't trust them at all. 59.7% want AI to operate only within defined frameworks with human oversight. |
| **Data security / privacy** | Critical | Ranked #1 concern for tax firms. Confidentiality of client data in AI tools is the #3 concern overall. |
| **Integration complexity** | High | 20.1% cite difficulties integrating AI into existing systems. Legacy system compatibility is a persistent challenge. |
| **Cost** | High | High integration costs; unclear ROI; small firms have limited technology budgets ($5K-$100K/year). |
| **Talent / skills gap** | Medium-High | 13.5% identify lack of skilled personnel to operate AI agents. Staff training is a widespread challenge. |
| **Regulatory uncertainty** | Medium | Evolving standards around AI use in accounting; firms uncertain about compliance requirements. |
| **No comprehensive strategy** | Medium | 86% of firms lack a comprehensive AI strategy; leads to ad hoc adoption without clear outcomes. |

### What We Need to Learn (Project Green-Specific)

- [ ] Which barriers matter most for our specific ICP (10-50 person firms)?
- [ ] Does local-first deployment meaningfully reduce the data security barrier?
- [ ] Does the services wrapper (human setup/tuning) meaningfully reduce
  the trust barrier?
- [ ] What price point triggers "too expensive" vs "that's reasonable" vs
  "that's suspiciously cheap"?
- [ ] Is integration complexity a barrier if we start with QBO-only?
- [ ] What's the firm owner's mental model of AI? (Magic? Threat? Tool?
  Distraction?)

### How to Learn It

- **AI Readiness Assessment conversations**: The assessment framework
  is designed to surface barriers naturally. Capture the unstructured
  conversation, not just the scores.
- **Pricing validation**: In conversations, test pricing ranges. Don't
  quote a price -- ask "If a tool like this existed, what would you
  expect to pay monthly?"

---

## 4. Competitive Pricing Intelligence

**Status**: Partial (web-researched February 2026; needs ongoing updates)

### What We Know Now

| Competitor | Target | Pricing Model | Price Range | Notes |
|-----------|--------|--------------|-------------|-------|
| **Truewind** | Funded startups, SMBs | Custom (contact sales) | ~$500-$1,500/month | Based on company size and complexity. Y Combinator backed. 100+ customers. |
| **Vic.ai** | Mid-market, enterprise AP teams | Custom (contact sales) | Undisclosed | AP-specific. Claims 5x faster processing, 99% accuracy. No published tiers. |
| **Numeric** | Accounting teams (QBO, Xero, NetSuite) | Tiered | Essentials: $30/user/month; Growth/Enterprise: custom | Close automation. CPA-led onboarding included in paid tiers. |
| **Gravis AI** | Service businesses, agencies | Custom (contact sales) | Undisclosed | AI-powered ERP (replacement, not overlay). Currently in technical preview. |
| **Intuit Assist** | QBO users | Bundled with QBO | Included in QBO subscription ($30-$200/month) | Within-system only. Limited to QBO data. |

### Vertical AI SaaS Pricing Benchmarks

| Metric | Range | Source |
|--------|-------|--------|
| Median ACV, vertical SaaS | $25K-$50K | Industry benchmarks (2025) |
| Median ACV, horizontal SaaS | $8K-$15K | Industry benchmarks (2025) |
| AI-first SaaS gross margins | 55-70% | vs 78-85% traditional SaaS |
| Inference cost per enterprise customer | $500-$2,000/month | AI-first B2B SaaS economics (2026) |
| ACV growth rate (growth-stage) | 15-25% annually | Optifai benchmarks |

### What We Need to Learn

- [ ] What do firms currently pay for technology overall (total tech spend)?
- [ ] How do firms think about per-seat vs per-firm vs outcome-based pricing?
- [ ] What's the psychological price ceiling for a "firm intelligence" tool?
- [ ] What pricing model reduces friction for a first deal (monthly vs annual)?
- [ ] How does our local-first architecture change the cost structure vs
  cloud-hosted competitors? (Our inference cost is near-zero with local models.)

### Pricing Implications for Project Green

Project Green's local-first architecture dramatically changes the economics.
While cloud-hosted AI-first SaaS operates at 55-70% gross margins due to
inference costs of $500-$2,000/month per customer, Project Green running on
Ollama locally has near-zero inference costs. This means:

- We can price below competitors while maintaining higher margins
- OR we can match pricing and invest the margin delta in services
- The services-plus-software model ($2K-$5K/month including setup and
  tuning) positions above point solutions but below consulting

This pricing hypothesis needs validation in conversations.

---

## 5. Adjacent Market Scan

**Status**: Gap (no systematic analysis in existing docs)

### Why Adjacent Markets Matter

If accounting is the beachhead, where else does the same architecture
(multi-system intelligence layer for small professional service firms)
apply? Adjacent markets inform:

- Total addressable market expansion
- Investor narrative (vision beyond accounting)
- Architecture decisions (generalize early or specialize first?)

### Adjacent Markets to Investigate

| Market | Size | Equivalent Pain Points | Existing Solutions | Architecture Fit |
|--------|------|----------------------|-------------------|-----------------|
| **Law firms (small)** | ~50,000 firms in US; AI legal tech growing by $4.07B from 2025-2029 at 31.1% CAGR | Knowledge fragmentation, document overload, billing complexity, client Q&A volume | Clio (practice mgmt), Harvey (AI for law), CoCounsel | High -- same multi-system, knowledge-capture pattern |
| **Healthcare practices (small)** | AI in medical billing alone: $3.73B (2024) growing to $36.37B by 2034 at 25.4% CAGR | Billing complexity, scheduling, insurance navigation, regulatory compliance | Athenahealth, DrChrono, many vertical point solutions | Medium -- more regulated, different data types |
| **Fractional CFO firms** | Part of $54.79B FAO market (2025), growing at 8.2% CAGR | Serve many clients with limited staff; need cross-client intelligence; margin pressure | Jirav, Fathom, LivePlan (financial planning) | Very High -- same architecture, same need for multi-client intelligence |
| **Outsourced accounting firms** | Growing segment within FAO; 84% of CFOs report talent deficits | Process standardization, client communication, capacity planning | Practice management tools (Karbon, Jetpack, Canopy) | Very High -- cloud-native, high client volume, efficiency-focused |
| **Financial advisory (RIAs)** | ~15,000 registered investment advisors; growing AI adoption | Client reporting, compliance documentation, portfolio analysis | Black Diamond, Orion, Addepar | Medium -- different data (market data vs GL data) but similar client-serving pattern |

### What We Need to Learn

- [ ] Which adjacent market has the most similar pain points and data patterns?
- [ ] Can the same DuckLake architecture serve a law firm or healthcare practice
  without major changes?
- [ ] Is there a "horizontal" positioning that covers multiple verticals (e.g.,
  "AI intelligence layer for small professional service firms")?
- [ ] Should we pursue one adjacent market as a second beachhead within 18 months,
  or stay focused on accounting until $1M ARR?
- [ ] What are the regulatory differences that would require architecture changes?

### Preliminary Assessment

The closest adjacent markets are **fractional CFO firms** and **outsourced
accounting firms** -- they're essentially sub-segments of our primary market
with slightly different emphases. These aren't true "adjacent" markets;
they're variations on the same market.

The first genuinely adjacent market is **small law firms**. The pain points
(knowledge fragmentation, document overload, client Q&A, billing) are
structurally similar. The architecture would need different bronze-layer
integrations (Clio, CARET, PracticePanther) but the silver/gold layers and
agent logic would transfer. The law firm AI market is large and growing fast.

**Recommendation**: Stay focused on accounting through $500K ARR. Begin
law firm exploration conversations at that point.

---

## 6. Jobs to Be Done Framework

**Status**: Assumption (inferred from research, not validated with customers)

### Firm Owner Jobs

| Job | Functional | Emotional | Social |
|-----|-----------|-----------|--------|
| **"Help me answer client questions faster"** | Reduce time from question to answer from hours to minutes | Feel competent and responsive | Be seen as a modern, AI-forward firm |
| **"Help me not lose knowledge when people leave"** | Capture and make queryable institutional knowledge | Feel secure that the firm isn't fragile | Demonstrate operational maturity to staff and clients |
| **"Help me understand my own firm's operations"** | Dashboards, metrics, bottleneck identification | Feel in control of the business | Compete with larger firms on operational sophistication |
| **"Help me shift from compliance to advisory"** | Auto-generate insights from client data | Feel like a trusted advisor, not a data entry clerk | Position the firm as forward-thinking to clients |
| **"Help me grow without proportionally adding staff"** | Automate repeatable tasks | Feel confident about capacity | Demonstrate scalability to partners, PE, potential acquirers |

### Staff Member Jobs

| Job | Functional | Emotional | Social |
|-----|-----------|-----------|--------|
| **"Help me find the answer without bothering a senior"** | Self-serve Q&A against firm data and policies | Feel independent and productive | Avoid being "the person who always asks questions" |
| **"Help me do this correctly the first time"** | Procedural guidance, checklists, guardrails | Feel confident in work quality | Be seen as reliable by reviewers |
| **"Help me not stay late during busy season"** | Automate tedious tasks (data entry, reconciliation) | Feel like work-life balance is possible | Retain talent in a competitive labor market |

### What We Need to Validate

- [ ] Which jobs resonate most strongly with firm owners?
- [ ] Are there jobs we haven't identified?
- [ ] What language do firm owners use to describe these jobs? (Our
  language vs their language may differ significantly.)
- [ ] Which job would a firm owner pay to solve first?
- [ ] Is there a "hair on fire" job that's more urgent than all others?

### How to Validate

- **Conversation prompt**: "If I could wave a magic wand and solve one
  thing for your firm today, what would it be?"
- **Card sort exercise**: Present 5-6 job statements and ask the owner
  to rank them.
- **Language capture**: Record (with permission) the exact words firm
  owners use. Build a vocabulary dictionary of "their language" vs
  "our language."

---

## 7. Market Segment Profiles

**Status**: Partial (ICP defined in GTM, sub-segments identified in market-gap-analysis, detailed profiles not yet built)

### What We Have

The ICP is defined in [go-to-market.md](go-to-market.md): 10-50 employee
tax + bookkeeping firms using cloud GL systems. Sub-segments are identified
in [market-gap-analysis.md](market-gap-analysis.md): tax-only, tax +
bookkeeping, full-service, outsourced/virtual, industry-specialized.

### What We Need to Build

Detailed profiles for each sub-segment that include:

- [ ] **Firmographics**: Size, revenue, geographic distribution, growth rate
- [ ] **Technographics**: What software they use (GL, tax, payroll, doc mgmt)
- [ ] **Psychographics**: Technology attitudes, risk tolerance, innovation posture
- [ ] **Buying behavior**: Budget cycle, decision maker, procurement process
- [ ] **Channel affinity**: Where they learn about new tools, who influences them
- [ ] **Pain intensity**: Which problems cause the most pain for this segment
- [ ] **Willingness to pay**: Price sensitivity by segment

### Where to Get This Data

| Data Type | Source | Status |
|-----------|--------|--------|
| Firmographics | AICPA surveys, state CPA society directories, IRS SOI data | Available, not yet compiled |
| Technographics | Intuit/Xero market share data, app ecosystem marketplaces | Available, not yet compiled |
| Psychographics | CPA.com AI in Accounting Report (2025, 2026), Thomson Reuters Future of Professionals | Available, partially referenced |
| Buying behavior | Conversations with firm owners, technology consultants | Not yet available -- requires conversations |
| Channel affinity | Conference attendee lists, publication readership data; see [Lead Generation Target Lists](lead-gen-target-lists.md) for compiled org and influencer channels | Partially available -- org list compiled |
| Pain intensity | Conversations, AI Readiness Assessment results | Not yet available -- requires conversations |
| Willingness to pay | Conversations, pricing experiments | Not yet available -- requires conversations |

---

## 8. Open Questions

Things we can only learn through conversations with actual firm owners,
staff, and industry participants.

### For Firm Owners

1. "What's the most frustrating part of your workday?" (Open-ended,
   captures language and priorities)
2. "When was the last time you lost a key staff member? What happened to
   their work?" (Validates knowledge capture gap)
3. "Have you tried any AI tools? Which ones? What happened?" (Maps
   substitute landscape)
4. "If I could build one thing for your firm, what should it be?"
   (Validates JTBD hierarchy)
5. "What would make you nervous about using AI with your client data?"
   (Surfaces barriers in their language)
6. "How do you currently keep track of how the firm is performing?"
   (Maps process visibility substitute)
7. "What do you wish you could ask your data that you can't today?"
   (Surfaces unarticulated demand)

### For Staff Members

1. "What do you do when you don't know the answer to a client question?"
   (Maps knowledge-seeking behavior)
2. "What takes up most of your time that you wish didn't?"
   (Identifies automation opportunities)
3. "Have you ever used ChatGPT or similar tools for work? What for?"
   (Maps horizontal AI usage)

### For Industry Participants

1. **Technology consultants** (Woodard, Right Networks): "What do your
   clients ask for that nobody builds?"
2. **CPA society leaders**: "What's the biggest challenge your members
   face with technology?"
3. **PE operating partners**: "What operational data do you wish you had
   from your portfolio firms?"
4. **Accounting educators**: "What skills are graduates missing? Where
   do they struggle in their first year?"

---

## Research Prioritization

### Must-Have Before Alpha Revenue

| # | Research Area | Why It's Blocking | How to Get It |
|---|-------------|-------------------|---------------|
| 1 | Substitute analysis (Section 1) | Can't position if we don't know what we're replacing | First 5 conversations |
| 2 | JTBD validation (Section 6) | Can't prioritize features without knowing which jobs matter | First 5 conversations |
| 3 | Price sensitivity (Section 4) | Can't close a deal without a defensible price | Conversations 3-10 |
| 4 | Adoption barriers, PG-specific (Section 3) | Can't reduce friction we haven't identified | First 10 conversations |

### Important But Can Wait

| # | Research Area | When It Matters | How to Get It |
|---|-------------|----------------|---------------|
| 5 | Buyer journey (Section 2) | Before scaling past founder-led sales | First 20 conversations + pipeline data |
| 6 | Segment profiles (Section 7) | Before choosing a second sub-segment | 20+ conversations across segments |
| 7 | Adjacent markets (Section 5) | Before expanding beyond accounting | After $500K ARR |

### Data We Can Compile Now (No Conversations Needed)

| # | Research Area | Source | Effort |
|---|-------------|--------|--------|
| A | Firmographics for ICP sub-segments | AICPA, state directories, IRS SOI | 1-2 days desk research |
| B | Technographics (QBO vs Xero market share by firm size) | Intuit/Xero investor reports, app ecosystem data | 1 day desk research |
| C | Conference and publication calendar for 2026 | Accounting Today, AICPA, state societies | 2-3 hours |

---

## Related Documents

- [Market Gap Analysis](market-gap-analysis.md) -- strategic view of market opportunities
- [Market Landscape](market-landscape.md) -- competitive landscape and market sizing
- [Go-to-Market Playbook](go-to-market.md) -- ICP, positioning, sales motion
- [GTM Evaluation](gtm-evaluation.md) -- critical assessment of current GTM assumptions
- [Traction Acceleration](traction-acceleration.md) -- conversation and lead-gen plan
- [AI Readiness Assessment](ai-readiness-assessment.md) -- lead-generation tool framework
- [AI ERP Landscape](../research/ai-erp-landscape.md) -- competitor deep dives
- [Lead Generation Target Lists](lead-gen-target-lists.md) -- compiled org directories, firm rankings, and influencer sourcing channels
