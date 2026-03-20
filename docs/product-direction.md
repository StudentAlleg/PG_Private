# Product Direction — What We're Actually Building

*Written 2026-03-04. Based on conversation with Mike.*

> **Strategic note (2026-03-06):** GTM is deliberately paused pending resolution of Parr3 employment agreement ([R22](strategy/risk-register.md)). Product development continues at full speed. This document describes the product vision that will be executed the moment the legal gate clears.

---

## The Core Job

A junior accountant has a question they don't want to bother a partner with.

They type it in. The system does three things:

1. **Thinks through the question with them** — helps them frame it properly if they're not sure what they're actually asking
2. **Gives general accounting guidance** — enough to orient them and build confidence
3. **Points them to resources that already exist** — firm documents, templates, precedents, prior work — so they can solve it themselves

The output isn't just an answer. It's a **plan of action**: here's what you're dealing with, here's the concept, here are the resources in the firm's library that will help you, here's what to do next.

---

## What "Good" Looks Like

A junior accountant asks: *"Client wants to know if they can deduct their home office. They work from home 3 days a week but the business is an S-corp."*

A bad product says: *"Yes, home office deductions are available under IRC §280A..."* and dumps a wall of text.

A good product says:
- Here's the key issue (S-corp home office works differently than sole prop — accountable plan required)
- Here's the general guidance (what an accountable plan is, why it matters)
- Here's what we have in our library (links to the firm's accountable plan template, any prior memos on this)
- Here's your next step (set up an accountable plan for this client, use the template)

The junior walks away knowing what to do. They didn't have to interrupt anyone.

---

## What This Means for the Product

### The assistant needs to be a thinking partner, not a search engine

Don't just retrieve. Reason. If the question is vague, ask a clarifying question before answering. Help the junior understand *why* the answer is what it is, not just *what* the answer is.

### The knowledge base is the product's competitive advantage

The AI general knowledge is a commodity. What the firm has in its own library — templates, memos, past returns, internal guidance — is unique. The product's job is to surface that, not replace it.

This means:
- Document ingestion has to work really well
- RAG (retrieval) has to actually find relevant things, not just keyword match
- The response has to cite what it found ("we have a memo on this from 2024")

### The plan of action is the output format

Every response should end with something actionable. Even if it's just "based on what you've described, here are the three things you need to figure out." The junior should never finish a conversation feeling more confused than when they started.

---

## Gaps Between Today and That Vision

### 1. Document quality is everything — and we haven't tested it
The RAG pipeline exists. We have 5 sample documents. We have no idea if it actually retrieves the right things for real accounting questions. This needs to be tested with realistic questions before anything else.

### 2. The assistant doesn't guide — it just responds
Right now the chat is reactive. It answers what was asked. There's no logic for "this question is unclear, let me ask one follow-up before answering" or "here's your plan of action" as a structured output.

### 3. There's no feedback loop
When the junior gets an answer, we have no idea if it was useful. The feedback mechanism exists in the code but isn't wired into the UI in a way that anyone would actually use.

### 4. The UI is functional but not optimized for the actual use case
The assistant page is a generic chat box. There's nothing that says "this is a tool for accounting questions." No suggested starting points, no indication of what the firm's knowledge base contains.

---

## Suggested Order of Work

**1. Test and improve RAG quality** *(highest leverage)*
Load real firm documents (or realistic fakes). Ask 20 real questions a junior would ask. See what the system retrieves. Fix what's broken. This is the foundation — everything else depends on it.

**2. Wire in the "plan of action" response format**
Change the system prompt so the assistant always ends with a structured next step. Doesn't require a UI change — just better prompting and response shaping.

**3. Add one clarifying question before answering vague queries**
If the question is ambiguous, the assistant should ask one focused follow-up before answering. This makes it feel like a thinking partner, not a search bar.

**4. Make the UI feel like an accounting tool**
Add suggested starter questions on the assistant page. Show what's in the knowledge base. Make it obvious what the tool is for.

**5. Close the feedback loop**
Add a simple thumbs up/down on responses. Use that to find where the system is failing. This is how you improve it over time without guessing.

---

## What We're NOT Building (yet)

- Client portal (clients don't use this — staff does)
- Automated workflows or task assignment
- Billing or invoicing automation
- Anything that replaces a partner's judgment on a hard call

The product's job is to make the junior more capable and more confident — not to replace anyone.

---

*This document should be updated as the product evolves. It is the answer to "what are we building and why."*
