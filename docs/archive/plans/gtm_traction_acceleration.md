---
name: GTM Traction Acceleration
overview: Critically evaluate the existing go-to-market strategy against the reality of zero customer conversations, then produce an iterated GTM focused on the fastest path to lead generation and meaningful conversations with accounting firm owners -- repositioned around "AI digital transformation."
todos:
  - id: gtm-evaluation
    content: Write docs/strategy/gtm-evaluation.md -- critical assessment of current GTM against zero-conversation reality
    status: completed
  - id: revise-gtm
    content: Major revision of docs/strategy/go-to-market.md -- add Phase 0 Traction, dual positioning, 30/60/90-day plan, content engine, network activation
    status: completed
  - id: ai-readiness
    content: Create docs/strategy/ai-readiness-assessment.md -- concrete lead-gen tool with scoring rubric and deliverable template
    status: completed
  - id: demo-playbook
    content: Create docs/strategy/demo-playbook.md -- how to demo the existing prototype effectively
    status: completed
  - id: changelog-update
    content: Update docs/CHANGELOG.md with this GTM iteration work
    status: completed
isProject: false
---

# GTM Strategy Evaluation and Traction Acceleration

## The Central Problem

The strategy docs are thorough and well-reasoned. The prototype is impressive (94.4% accuracy, working chat UI, 120+ passing tests). But there are **zero customer conversations**. The entire GTM is theoretical. The strategy implicitly sequences as "finish building, then start selling" -- which means traction keeps getting pushed to the right as engineering scope expands.

The fastest path to traction is **not building more product**. It's getting the existing prototype in front of people while the technical work continues in parallel.

## What the Evaluation Will Challenge

### 1. Phase 0 completion is gating customer outreach (it shouldn't be)

The current roadmap requires QBO integration, RAG, and multi-agent expansion before engaging firms. But for generating conversations, the working ledger agent with synthetic data and the Streamlit chat UI is a compelling demo **today**. Firms don't need to see their own data to get excited -- they need to see the *experience*.

### 2. The positioning needs two modes

- **"AI digital transformation"** for lead generation -- consultative, problem-first, opens conversations without selling
- **"Ask this before you ask a human"** for product positioning -- sharp, outcome-oriented, used when demoing

The existing GTM only has the product message. The lead-gen message doesn't exist yet. This is the biggest gap.

### 3. The AI Readiness Assessment is the fastest lead-gen tool but it's only a bullet point

[go-to-market.md](docs/strategy/go-to-market.md) mentions a "Free Assessment" as step 3 of the sales process. But it's not designed. It needs to be a concrete, repeatable framework that:
- Gives the firm owner genuine value (not just a sales pitch)
- Positions Mike as the expert
- Creates natural follow-up ("based on what we found, here's what we could do")

### 4. The content engine is documented but not launched

The content calendar in the GTM specifies LinkedIn 2-3x/week and blogs 2x/month. None of this has started. Every week without content is a week without building an audience of firm owners. Content is the cheapest, most scalable lead-gen channel.

### 5. Pricing detail is premature for this phase

The financial framework has ACVs, unit economics, and revenue projections -- but zero pricing conversations with real firms. For traction, the question isn't "what do we charge?" It's "would anyone pay *anything* for this?" Pricing should emerge from conversations, not precede them.

### 6. The warm network hasn't been mapped or activated

The GTM says "map personal networks for accounting firm connections." This hasn't happened. A systematic network map (who do Mike and Owen know who knows firm owners?) is the single highest-leverage action for generating conversations in the next 30 days.

## Deliverables

### 1. GTM Evaluation Document (new)

**File**: `docs/strategy/gtm-evaluation.md`

A permanent record of this strategic inflection point. Structured as:
- Current state assessment (what we have, what we don't)
- Assumption audit (which GTM assumptions are untested)
- Gap analysis (what's missing between strategy and execution)
- Recommendations (what to change and why)

### 2. Revised Go-to-Market Playbook (major update)

**File**: `docs/strategy/go-to-market.md`

Major revision to add a **"Phase 0: Traction"** stage that runs in parallel with engineering. Key additions:
- Dual positioning framework ("AI digital transformation" for lead gen, "Ask this before you ask a human" for product)
- 30/60/90-day traction action plan with specific weekly activities
- Content engine launch plan (topics, cadence, platforms)
- Network activation playbook (systematic warm outreach)
- Demo narrative using the *existing* prototype (not the future product)
- Revised sales motion that starts with conversations, not a finished product

### 3. AI Readiness Assessment Framework (new)

**File**: `docs/strategy/ai-readiness-assessment.md`

The concrete lead-gen tool. A structured framework that Mike can walk a firm owner through in 30 minutes:
- Assessment dimensions (data readiness, process documentation, technology stack, team capacity, AI awareness)
- Scoring rubric
- Deliverable template (what the firm owner gets: a one-page summary of their AI readiness with recommendations)
- Follow-up playbook (how the assessment naturally leads to a deeper conversation about Project Green)

### 4. Demo Playbook (new)

**File**: `docs/strategy/demo-playbook.md`

How to use the existing Streamlit prototype to generate excitement:
- Demo narrative and flow (what to show, what to say, what NOT to say)
- Setup checklist (what needs to be running for a live demo)
- Objection handling (common questions and how to answer them)
- Follow-up actions (what to do after a demo generates interest)
- Guidance for recording a 3-minute video demo for async distribution

### 5. Changelog Update

**File**: `docs/CHANGELOG.md` -- record this GTM iteration work.
