# Financial Framework and Unit Economics

## Revenue Model

### Revenue Streams

| Stream | Type | When | Description |
|--------|------|------|-------------|
| **Twin Setup** | One-time | At onboarding | Connect data sources, configure agents, load knowledge. $5K-$15K per firm. |
| **Platform Fee** | Recurring monthly | Ongoing | Core access to the AI twin. $2K-$5K/month per firm. |
| **Tuning Retainer** | Recurring monthly | Ongoing (optional) | Monthly check-ins, new use cases, knowledge base updates. $1K-$3K/month. |
| **Expansion Projects** | One-time | As needed | Add Archetype 2 (Explanation Engine), new integrations, custom agents. Project-priced. |

### Annual Contract Value (ACV) Scenarios

| Scenario | Setup | Monthly Platform | Monthly Retainer | Annual Total |
|----------|-------|-----------------|-----------------|--------------|
| **Conservative** | $5,000 | $2,000 | $0 | $29,000 |
| **Moderate** | $10,000 | $3,500 | $1,500 | $70,000 |
| **Aggressive** | $15,000 | $5,000 | $3,000 | $111,000 |

Target ACV for first 5 firms: **$30,000-$70,000 per firm.**

## Unit Economics: Cost to Serve One Firm

### LLM Inference Costs

Using the benchmarking framework's pricing data:

| Model | Input (per 1M tokens) | Output (per 1M tokens) | Queries/Day (est.) | Monthly Cost |
|-------|----------------------|------------------------|--------------------|----|
| **GPT-4o** | $2.50 | $10.00 | 50 | ~$45-$90 |
| **GPT-4o-mini** | $0.15 | $0.60 | 50 | ~$3-$6 |
| **Claude 3.5 Sonnet** | $3.00 | $15.00 | 50 | ~$55-$110 |
| **Gemini 1.5 Flash** | $0.075 | $0.30 | 50 | ~$1-$3 |
| **Local (Gemma 3)** | $0.00 | $0.00 | 50 | $0 (compute cost only) |

**Assumptions:** 50 queries/day per firm, ~500 input tokens + ~200 output tokens per query (multi-turn), 22 working days/month.

**Strategy:** Use GPT-4o-mini or Gemini Flash for the majority of queries. Route complex reasoning to GPT-4o or Claude only when needed. The existing benchmarking framework makes this measurable.

**Monthly LLM cost per firm: $5-$50** (depending on model mix and query volume)

### Infrastructure Costs (Per Firm)

| Component | Phase 0-1 (MVP) | Phase 2-3 (Production) |
|-----------|-----------------|----------------------|
| **Compute (hosting)** | $0 (local) or $20/month (VPS) | $50-$200/month (cloud VM or containers) |
| **Data lakehouse** | $0 (DuckLake local) | $50-$300/month (Databricks or S3 + compute) |
| **Vector database** | $0 (ChromaDB local) | $25-$70/month (Qdrant Cloud or Pinecone) |
| **LLM inference** | $0 (local) or $5-$50/month | $5-$50/month |
| **Monitoring** | $0 (local) | $20-$50/month |
| **Total per firm** | **$0-$70/month** | **$150-$670/month** |

### Cost to Serve Summary

| Phase | Monthly Cost per Firm | Monthly Revenue per Firm | Gross Margin |
|-------|----------------------|-------------------------|-------------|
| **MVP (Phase 1)** | ~$50 | $2,000-$3,500 | **97-98%** |
| **Production (Phase 2-3)** | ~$300-$500 | $3,500-$8,000 | **86-94%** |

Software-like gross margins. The primary cost is human time for setup and tuning (Layer 2 services), not infrastructure.

### Human Time Costs

This is the real constraint for a two-person team:

| Activity | Hours per Firm | Frequency | Cost (at $100/hr imputed) |
|----------|---------------|-----------|---------------------------|
| **Initial setup** | 20-40 hours | One-time | $2,000-$4,000 |
| **Monthly tuning** | 4-8 hours | Monthly | $400-$800/month |
| **Support** | 2-4 hours | Monthly | $200-$400/month |
| **Total ongoing** | 6-12 hours/month | Monthly | **$600-$1,200/month** |

At 6-12 hours/month per firm, a two-person team can support **~10-15 firms** before needing to hire (assuming ~50% of time goes to product development, 50% to customer work).

## Revenue Projections

### Conservative Scenario

| Quarter | Firms | Setup Revenue | Monthly Recurring | Quarterly Revenue | Cumulative |
|---------|-------|--------------|-------------------|-------------------|-----------|
| Q3 2026 | 1 (beta) | $5,000 | $2,000/mo | $11,000 | $11,000 |
| Q4 2026 | 2 | $5,000 | $4,000/mo | $17,000 | $28,000 |
| Q1 2027 | 4 | $10,000 | $8,000/mo | $34,000 | $62,000 |
| Q2 2027 | 6 | $10,000 | $12,000/mo | $46,000 | $108,000 |
| Q3 2027 | 10 | $20,000 | $20,000/mo | $80,000 | $188,000 |
| Q4 2027 | 15 | $25,000 | $30,000/mo | $115,000 | $303,000 |

**Year 1 (mid-2026 to mid-2027): ~$108,000**
**Year 2 run rate: ~$360,000 ARR**

### Moderate Scenario

| Quarter | Firms | ACV | Quarterly Revenue | Cumulative |
|---------|-------|-----|-------------------|-----------|
| Q3 2026 | 1 | $50,000 | $15,000 | $15,000 |
| Q4 2026 | 3 | $50,000 | $42,000 | $57,000 |
| Q1 2027 | 6 | $60,000 | $95,000 | $152,000 |
| Q2 2027 | 10 | $60,000 | $155,000 | $307,000 |
| Q3 2027 | 15 | $70,000 | $265,000 | $572,000 |
| Q4 2027 | 20 | $70,000 | $355,000 | $927,000 |

**Year 2 run rate: ~$1.4M ARR**

## Cost Structure

### Fixed Costs (Monthly)

| Category | Phase 0-1 | Phase 2-3 | Notes |
|----------|-----------|-----------|-------|
| **Cursor licenses** | $220 | $220 | Mike ($200) + Owen ($20); may change |
| **Miro** | ~$15 | ~$15 | Collaboration tool |
| **Cloud infrastructure** | $0-$50 | $200-$1,000 | Scales with firms |
| **Domain / email** | $20 | $20 | mlgroup.us |
| **LLM API costs** | $0-$50 | $50-$500 | Scales with usage |
| **Software tools** | $50 | $100 | GitHub, monitoring, etc. |
| **Total fixed** | **~$300-$400/month** | **~$600-$1,900/month** | |

### Variable Costs (Per Firm)

See "Cost to Serve" section above. $50-$500/month per firm depending on phase.

### People Costs

| Person | Phase 0-1 | Phase 2-3 | Notes |
|--------|-----------|-----------|-------|
| **Mike** | Sweat equity | Sweat equity or salary | Prototyping, strategy, sales |
| **Owen** | Part-time (has FT job goal) | Part-time or FT | Core engineering |
| **First hire** | N/A | $60K-$100K/year | When firm count exceeds 10-15 |

## LLM Cost Optimization Strategies

Since LLM inference is a marginal cost that scales with usage:

1. **Model routing:** Use cheap models (GPT-4o-mini, Gemini Flash) for simple queries; expensive models (GPT-4o, Claude) only for complex reasoning. The benchmarking framework enables this.

2. **Caching:** Cache common queries and their results. "What is our PTO policy?" doesn't need a fresh LLM call every time.

3. **RAG precision:** Better retrieval = shorter context = fewer tokens = lower cost. Investing in RAG quality directly reduces LLM costs.

4. **Local models:** For development and low-stakes queries, local models (Gemma 3 via Docker Model Runner) are free.

5. **Batch processing:** For non-interactive tasks (report generation, data summarization), batch API pricing is 50% cheaper.

## Funding Considerations

### Bootstrap Path (Current Plan)

- Mike and Owen fund development through sweat equity and personal savings
- Owen's full-time employment generates capital
- Revenue from first customers funds infrastructure and tools
- No external capital required until 10+ firms

**Pros:** Full ownership, no dilution, forced discipline on spending
**Cons:** Slower growth, limited by personal capacity, no safety net

### Seed Round Path (If Needed)

If the market moves faster than bootstrap allows:

| Metric | Target Before Raising |
|--------|----------------------|
| Firms on platform | 3-5 paying customers |
| ARR | $100K+ |
| Retention | 90%+ after 6 months |
| Case studies | 2-3 detailed success stories |

**Potential raise:** $500K-$1.5M seed round
**Use of funds:** First 2-3 hires (engineer, customer success), accelerated integrations, marketing
**Valuation basis:** 15-25x ARR for vertical AI SaaS at seed stage

### When to Consider External Capital

The trigger is not "we need money" but "the opportunity is larger than we can capture at current pace, and competitors are moving." If by Q4 2026 we have 3+ paying firms and a pipeline of 20+ interested firms, it may be time to accelerate.

## Key Financial Milestones

| Milestone | Target Date | Criteria |
|-----------|-------------|---------|
| **First dollar of revenue** | Q3 2026 | One firm pays anything (even $500/month for beta) |
| **$10K MRR** | Q4 2026 | 3-5 firms at $2K-$3.5K/month |
| **Infrastructure self-funding** | Q1 2027 | Revenue covers all cloud/API costs |
| **$50K MRR** | Q3 2027 | 10-15 firms; potential to consider first hire |
| **$100K MRR** | Q4 2027 | Sustainable business; decide on bootstrap vs. raise |
