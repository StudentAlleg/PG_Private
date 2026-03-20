# Go-to-Market Strategy Evaluation

> **Status (2026-03-06):** GTM execution is deliberately paused pending Parr3 employment agreement resolution ([Risk Register R22](risk-register.md)). Product development continues privately at full speed. This evaluation's recommendations remain valid but are gated on legal resolution.

> An honest assessment of the existing GTM strategy against current reality.
> This document does not replace the [Go-to-Market Playbook](go-to-market.md)
> or any other strategy document. It identifies gaps between strategy and
> execution, tests assumptions, and recommends a potential parallel traction
> track that could run alongside continued product development.
>
> **Status**: Exploratory -- potential pivot under evaluation
>
> **Date**: February 2026

---

## 1. Current State: What We Have

Before evaluating the strategy, an honest inventory of where things stand.

### Product

| Asset | Status | Notes |
|-------|--------|-------|
| Firm/client/document specialists (LangGraph) | Working | 10 tool modules, 94.4% correctness |
| Streamlit chat UI | Working | Browser-based, message history, tool call traces |
| Evaluation framework | Working | 24-question bank, correctness scoring, baseline saved |
| Data lakehouse (DuckLake) | Working | Medallion architecture, synthetic data |
| Local LLM (Ollama + Qwen3:32B) | Working | GTX 5090, no cloud costs |
| 120+ automated tests | Passing | Agents, tools, data, scoring |

### Product Gaps (per Phase 0 roadmap)

| Component | Status | Required for Demo? | Required for First Conversation? |
|-----------|--------|-------------------|----------------------------------|
| QuickBooks Online integration | Not started | No -- synthetic data demos the experience | No |
| RAG pipeline (document Q&A) | Not started | No -- can describe the vision | No |
| Multi-agent orchestration | Not started | No -- single agent is enough to show | No |
| Real firm data | Not available | No -- synthetic data is realistic | No |

### GTM Execution

| Activity | Status | Notes |
|----------|--------|-------|
| Customer conversations | **Zero** | No firm owners contacted |
| Warm network mapped | **Not done** | GTM says to do this; hasn't happened |
| Content (LinkedIn, blog) | **Not started** | Calendar documented but not launched |
| Demo video / recording | **Does not exist** | No async sales asset |
| AI Readiness Assessment | **Concept only** | Mentioned as a bullet point in GTM, not designed |
| Pricing validation | **Zero data points** | Pricing model documented but untested |
| Conference appearances | **None** | No speaking slots secured |
| Partnership outreach | **None** | QBO ProAdvisors, CPA societies not contacted |

### The Gap

The product is roughly 60-70% of Phase 0 completion. The GTM execution is at 0%. The strategy documents are thorough and well-reasoned, but none of the customer-facing activities have started. The strategy implicitly sequences as "finish building, then sell." This evaluation questions whether that sequencing is optimal.

---

## 2. Assumption Audit

The existing GTM makes several assumptions. Some are well-supported by research. Others are untested and could be wrong. Testing assumptions requires conversations, not more documents.

### Assumption 1: Accounting firm owners will pay $2K-$5K/month for an AI copilot

**Evidence for**: Market research shows 82% early adopter ROI, 77% planning to increase AI spend. ACV is comparable to managed IT services (a budget category firms understand).

**Evidence against**: Zero pricing conversations. The 41% AI adoption figure may overcount firms using basic tools (ChatGPT, Excel copilot) and undercount how few have adopted purpose-built AI products. Small firms are notoriously price-sensitive.

**Test**: Have 10 conversations about willingness to pay. The number doesn't need to be exact -- the signal is whether firm owners flinch or lean in when a price range is mentioned.

**Status**: Untested.

### Assumption 2: "Ask this before you ask a human" is a compelling value proposition

**Evidence for**: Directly addresses the CPA shortage and the partner-as-bottleneck problem. Simple, outcome-based. Doesn't require understanding AI.

**Evidence against**: No firm owner has heard this pitch. The message assumes the buyer already knows they have a "knowledge accessibility" problem. Some may frame their pain differently -- as a hiring problem, a training problem, or a "we just need more people" problem.

**Test**: Use this line in 5 conversations. Watch for reaction. Does it land, or does it need translation?

**Status**: Untested.

### Assumption 3: The ICP (10-50 person firms, QBO, tax + bookkeeping) is the right starting segment

**Evidence for**: Large enough to feel pain, small enough to decide fast. QBO is the most common GL in this segment. Tax + bookkeeping maximizes data density from one integration.

**Evidence against**: These firms may be the most conservative adopters. Larger firms (50-200) may have dedicated ops/tech partners who are easier to reach and faster to act. Alternatively, very tech-forward small firms (5-10 people, cloud-native) might adopt faster even if the ACV is smaller.

**Test**: Talk to firms in different segments. See who leans in hardest.

**Status**: Untested.

### Assumption 4: Founder-led sales through warm network is the right initial channel

**Evidence for**: Standard startup playbook. Personal relationships build trust. No marketing budget needed.

**Evidence against**: Mike and Owen's warm network in accounting may be thin. If the network doesn't produce 3-5 qualified conversations, the channel is wrong and cold outreach, content marketing, or partnership channels need to start sooner.

**Test**: Map the network. Count the connections. If fewer than 10 reachable firm owners or connectors, the warm network channel is insufficient alone.

**Status**: Network not yet mapped.

### Assumption 5: Firms won't engage until the product is "ready"

**Evidence for**: This assumption isn't stated explicitly, but it's implicit in the sequencing. The roadmap puts customer engagement after Phase 0 completion.

**Evidence against**: The existing prototype is already more than enough to generate conversations. A working AI agent that answers accounting questions with 94% accuracy, running on local hardware, is genuinely impressive. Most firm owners have never seen anything like this. The demo itself is the conversation opener.

**Test**: Show the demo to 3 people. Gauge reaction.

**Status**: Untested -- and this is the most important assumption to challenge.

### Assumption 6: The "digital twin" framing resonates with firm owners

**Evidence for**: It's a powerful concept. Deloitte and RSM use the language. It captures the long-term vision accurately.

**Evidence against**: "Digital twin" is enterprise jargon. Most 15-person accounting firm owners have never heard the term. It may confuse more than it clarifies. The concept may need to be sold in stages -- start with "AI assistant for your firm," graduate to "digital twin" once they understand the scope.

**Test**: Use "digital twin" in 3 conversations, use "AI assistant" in 3 others. See which opens doors.

**Status**: Untested.

---

## 3. Gap Analysis

### What's Missing Between Strategy and Execution

| Gap | Impact | Effort to Close |
|-----|--------|----------------|
| **No customer conversations** | Critical -- all assumptions are untested | Low -- requires outreach, not building |
| **No demo asset** | High -- can't show the product asynchronously | Low -- record a 3-minute screen capture |
| **No content engine** | Medium -- missing compounding lead generation | Medium -- requires consistent weekly effort |
| **No warm network map** | High -- don't know the size of the initial channel | Low -- one session of mapping connections |
| **No AI Readiness Assessment** | Medium -- missing the primary lead-gen offer | Medium -- needs design and a deliverable template |
| **No "AI digital transformation" positioning** | Medium -- only have product messaging, not consultative messaging | Low -- framing exercise |

### What's NOT Missing

The existing strategy documents are genuinely strong in these areas:

- **ICP definition** is sharp and well-reasoned (even if untested)
- **Competitive positioning** is clear -- overlay, not replacement
- **Phased roadmap** is realistic with honest timelines
- **Unit economics** are favorable (86-98% gross margin)
- **Risk register** is comprehensive and honest
- **The flywheel concept** is sound (one firm -> case study -> next firm)

These don't need to be rewritten. They need to be tested against reality.

---

## 4. The Central Question

The existing GTM is a plan for a company that has a finished product and is ready to sell. Project Green is not there yet. The question is:

**Can we start generating conversations, testing assumptions, and potentially earning alpha-level revenue BEFORE the product is "complete" -- and if so, what does that motion look like?**

This evaluation suggests yes. The working prototype, combined with consultative positioning around AI digital transformation, could open doors today. The detailed recommendations for this parallel traction track are in [Traction Acceleration](traction-acceleration.md).

---

## 5. Recommendations

### Do Now (This Month)

1. **Map the warm network.** Write down every person Mike and Owen know who is connected to accounting firm owners. Count them. If fewer than 10, the warm network channel is too thin to rely on alone.

2. **Record a demo.** Take the working Streamlit prototype, run 3-4 questions, record the screen. This becomes an async sales asset. See [Demo Playbook](demo-playbook.md).

3. **Have 3 conversations.** Not sales calls. Exploratory conversations. "We're building AI tools for accounting firms and I'd love your perspective on what the industry needs." Listen more than you talk.

### Do Soon (Next 60 Days)

4. **Design the AI Readiness Assessment.** This is the lead-gen offer. See [AI Readiness Assessment](ai-readiness-assessment.md).

5. **Start the content engine.** One LinkedIn post per week minimum. Topic: the CPA shortage, AI in accounting, firm operational challenges. Build an audience before you need one.

6. **Test positioning.** Use "AI digital transformation" as a consultative opener in some conversations. Use "Ask this before you ask a human" as a product pitch in others. See what resonates.

### Do When Ready

7. **Test pricing.** Only after 10+ conversations. Frame as "we're exploring pricing models" and gauge reactions to ranges, not exact numbers.

8. **Pursue the pharmacy lead.** The local pharmacy mentioned in the GTM is a real, warm lead. Even though it's not the primary ICP, a real deployment teaches more than any amount of planning.

9. **Pursue conference speaking.** Local CPA society events are the lowest-barrier entry. A 15-minute talk on "How AI Is Changing Firm Operations" positions Mike as a thought leader without requiring a finished product.

---

## 6. What This Evaluation Does NOT Recommend

- **Do not rewrite the existing strategy documents.** They are sound. They need testing, not revision.
- **Do not stop building the product.** Engineering work (QBO integration, RAG, multi-agent) should continue. The traction track runs in parallel, not instead of.
- **Do not commit to a pivot.** This evaluation proposes a *potential parallel track*. If conversations reveal that the existing strategy is correct as-is, stay the course.
- **Do not lower the quality bar.** The 94.4% accuracy standard is a genuine differentiator. Rushing to market with a half-baked product would be worse than waiting.

---

## Related Documents

- [Go-to-Market Playbook](go-to-market.md) -- the existing GTM strategy (unchanged)
- [Traction Acceleration](traction-acceleration.md) -- the proposed parallel traction track
- [AI Readiness Assessment](ai-readiness-assessment.md) -- the lead-gen tool design
- [Demo Playbook](demo-playbook.md) -- how to demo the existing prototype
- [Product Strategy](product-strategy.md) -- phased roadmap and product archetypes
- [Financial Framework](financial-framework.md) -- unit economics and projections
- [Risk Register](risk-register.md) -- risk assessment and mitigations
