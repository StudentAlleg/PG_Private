# Product Roadmap — Future Features

**Created:** 2026-03-15
**Source:** Full-team brainstorming session (party mode)
**Status:** Ideas validated by team — stories to be created when the time is right

> **Prerequisite:** Alpha customer live and providing feedback. Security Sprints 31-33 complete. Entity formed. These features are sequenced AFTER alpha validation — ship, learn, iterate.

---

## Guiding Principles

1. **The wedge:** Junior staff get instant answers about firm data without interrupting partners. Every feature sharpens this wedge.
2. **Intelligence, not automation.** We're the brain, not the hands. Don't build invoice processing or bank reconciliation — build the layer that makes sense of the data.
3. **Win with 5-30 person firms first.** Partner makes the buying decision in one meeting. Don't chase enterprise.
4. **Ship before perfect.** Everything here is sequenced AFTER the first firm is live and giving feedback.

---

## Horizon 1: Make the Alpha Customer Wildly Successful (0-6 months post-launch)

These features make the existing product stickier, more useful, and more trusted.

### F1. Conversation Memory (Session Persistence)

**Problem:** Each chat is stateless. Sarah asks about Q3 taxes, then wants to compare to Q2 — she re-explains context every time.

**Solution:** Persist conversation sessions. The question graph already logs every query. Add session IDs, store message history, and resume conversations.

**Impact:** High | **Effort:** Small
**Technical notes:** Question graph schema + new `sessions` table in PostgreSQL. Frontend stores session_id.

---

### F2. Scheduled Digests

**Problem:** Partners want a weekly pulse without logging in. "What do I need to know this Monday?"

**Solution:** Automated email/Slack summaries: overdue invoices, upcoming deadlines, cash position, flagged items. Configurable per user — daily, weekly, or custom triggers.

**Impact:** High | **Effort:** Medium
**Technical notes:** Celery/APScheduler + email integration. Agent tools already produce the data — this adds a delivery mechanism.

---

### F3. Natural Language Report Builder

**Problem:** "Show me revenue by client for the last 6 months" should produce a chart, not a text answer.

**Solution:** The agent generates SQL via the dynamic SQL generator, executes it, and returns structured data. Frontend renders it as a chart (Recharts already in the stack). Users can ask for bar charts, line charts, tables, comparisons.

**Impact:** High | **Effort:** Medium
**Technical notes:** New response type (`chart_data`) in ChatResponse. Frontend component that switches between text and chart rendering based on response type.

---

### F4. Confidence-Tiered Responses

**Problem:** The AI gives every answer with the same tone, whether it's 99% confident or 50% confident.

**Solution:** Surface the verifier's confidence signal meaningfully:
- **High confidence:** Direct answer with citation
- **Medium confidence:** Answer with caveat ("Based on available data...")
- **Low confidence:** "I'm not sure — here's what I found, but verify with [partner name]"

**Impact:** Medium | **Effort:** Small
**Technical notes:** Verifier already produces a confidence score. Map score ranges to response templates. Frontend shows confidence indicator (green/yellow/red).

---

### F5. Cross-Client Benchmarking

**Problem:** "Which of my clients has the highest AR aging?" requires manually comparing across 90 clients.

**Solution:** Aggregate queries across the 90-client synthetic firm (and eventually real clients). "Compare revenue growth across manufacturing clients." "Rank clients by profitability."

**Impact:** High | **Effort:** Medium
**Technical notes:** Dynamic SQL generator + gold views already support multi-client queries. May need new gold views for cross-client aggregation.

---

### F6. 30-Minute Onboarding

**Problem:** Current onboarding requires OAuth setup + data sync + validation — multi-step, multi-day.

**Solution:** One-click QBO/Xero connect → automatic sync → instant insights. Target: firm goes from "never heard of us" to "asking their first question" in 30 minutes.

**Impact:** Very High | **Effort:** Medium
**Technical notes:** Onboarding orchestration API already exists. Streamline the flow, add progress indicators, pre-compute gold views immediately after sync.

---

### F7. Tax Deadline Intelligence

**Problem:** Firms live and die by deadlines. "What's due this week?" is table stakes.

**Solution:** Cross-reference deadlines with document status. "Which deadlines are at risk because the client hasn't sent their documents yet?" Proactive alerts, not just lookups.

**Impact:** High | **Effort:** Medium
**Technical notes:** Requires document tracking per client + deadline correlation. Gold view extension.

---

### F8. Guided Onboarding for Junior Staff

**Problem:** First-time users don't know what to ask.

**Solution:** Category cards on the Assistant page: "Financials," "Clients," "Deadlines," "Staff." Each shows 3-4 example questions contextual to the firm's actual data (not generic). Starter questions already exist — make them smart.

**Impact:** Medium | **Effort:** Small
**Technical notes:** Frontend component + API endpoint that generates contextual starter questions based on the firm's gold views.

---

### F9. Follow-Up Question Suggestions

**Problem:** Users ask one question and stop. They don't know what else the system can do.

**Solution:** After every answer, suggest 2-3 logical follow-up questions. "You asked about revenue — want to see it by client? By month? Compared to last year?" Teaches the system's capabilities through use.

**Impact:** Medium | **Effort:** Small
**Technical notes:** LLM generates follow-ups based on the query + answer + available tools. New field in ChatResponse.

---

### F10. Mobile-Responsive Assistant

**Problem:** Partners check things on their phones between meetings. Current UI is desktop-first.

**Solution:** Responsive design for the Assistant page. Touch-friendly input, readable cards, swipeable results.

**Impact:** Medium | **Effort:** Small
**Technical notes:** Tailwind responsive utilities. No backend changes.

---

## Horizon 2: Scale from 1 Firm to 50 Firms (6-18 months)

These features create network effects, increase stickiness, and expand the addressable market.

### F11. Client Portal (Archetype 2 — Explanation Engine)

**Problem:** Firm clients call the firm to ask basic questions about their own financials. "Why did my tax bill go up?" "What's my current AR?"

**Solution:** A separate login for firm clients. The AI explains — it does NOT advise. Guardrails enforce approved language, prohibited topics, and confidence thresholds. Firm staff review flagged responses before they reach clients.

**Impact:** Very High | **Effort:** Large
**Technical notes:** New user role (`client`), firm-configurable guardrails, response review queue, separate frontend portal or gated section. Citation enforcement on every financial claim.

**Risk:** Highest-risk feature. Requires legal review of response guardrails. Firm sign-off on approved language. Audit trail of every client-facing response. Kill switch per client/topic.

---

### F12. Notification Badges & Ambient Awareness

**Problem:** Users only open the app when they have a specific question. They miss things that need attention.

**Solution:** Dashboard badges: "3 deadlines this week," "2 clients with overdue invoices," "1 unusual transaction flagged." Pull users into the product with ambient awareness.

**Impact:** Medium | **Effort:** Medium
**Technical notes:** Background analysis job + WebSocket push notifications + badge component.

---

### F13. Multi-Firm Anonymized Benchmarking

**Problem:** Firms don't know how they compare to peers. "Is my revenue per partner good?"

**Solution:** Anonymized, aggregated metrics across all firms on the platform. "Your revenue per partner is $450K — the median for firms your size is $380K." "Your client retention is top quartile."

**Impact:** Very High | **Effort:** Large
**Technical notes:** Requires 10+ firms on the platform. Aggregation pipeline with k-anonymity guarantees. Opt-in consent model. New gold views for cross-firm metrics.

**Moat:** Data network effect. More firms = better benchmarks = more firms want to join. Extremely hard for competitors to replicate.

---

### F14. Workflow Automation Triggers (Watchdog Mode)

**Problem:** Firms react to problems instead of catching them early.

**Solution:** User-defined triggers: "When a client's AR exceeds 90 days, notify the engagement partner." "When payroll costs exceed 45% of revenue, flag it." The agent becomes a watchdog, not just a librarian.

**Impact:** Very High | **Effort:** Large
**Technical notes:** Rule engine (condition + action), scheduled evaluation, notification system (email/Slack/Teams). Builds on F2 (scheduled digests) infrastructure.

---

### F15. Microsoft Teams Integration

**Problem:** 90%+ of target firms live in Microsoft 365. Making them open a separate app reduces daily usage.

**Solution:** Teams bot that exposes the assistant. Ask questions directly in Teams chat. Get answers with the same quality as the web app. Share answers in team channels.

**Impact:** High | **Effort:** Large
**Technical notes:** M365 Agents SDK (formerly Bot Framework). Azure AD integration for SSO. Requires Microsoft Partner Center registration.

---

### F16. White-Label / Embedded (Platform Play)

**Problem:** Practice management vendors (Karbon, Canopy, TaxDome) want AI features but don't want to build them.

**Solution:** Offer Project Green as an embeddable intelligence layer. API-first, white-labeled, multi-tenant by design (already built). Partners embed your AI in their UI.

**Impact:** Very High | **Effort:** Very Large
**Technical notes:** Already multi-tenant with firm_id scoping. Need: partner API keys, usage-based billing, documentation portal, SLA guarantees. This is a business model shift from direct-to-firm to B2B2B.

---

## Horizon 3: Platform Plays & New Archetypes (18+ months)

These features transform the product from a tool into a platform.

### F17. Process Twin (Archetype 3)

**Problem:** Firms don't understand how work actually flows. "Where do things get stuck?" "What would happen if we hired two more associates?"

**Solution:** Model how work flows through the firm. Process mapping, bottleneck identification, what-if simulation, client profitability analysis, PE exit readiness metrics.

**Impact:** Very High | **Effort:** Very Large
**Technical notes:** Requires time-tracking data (from practice management integrations), engagement lifecycle modeling, simulation engine. This is the feature PE firms will pay premium for.

**Target buyer shift:** Phase 3+ is where PE-backed firms become primary buyers. They need operational clarity for exit readiness.

---

### F18. Tax Research Agent

**Problem:** Junior staff can't answer tax questions without senior guidance. "Is this deductible under IRC 280A?"

**Solution:** Agent connected to IRS publications, state tax databases, Cornell LII. Researches the regulation, gives the firm-specific context, cites the source. Accountants verify — the AI does the research legwork.

**Impact:** High | **Effort:** Large
**Technical notes:** New RAG corpus (federal + state tax code). New specialist agent. Different accuracy requirements (legal citations must be exact). Potentially separate product SKU.

---

### F19. Audit Preparation Assistant

**Problem:** Audit prep takes days of manual compilation.

**Solution:** When a client faces an audit, automatically compile: relevant GL entries, supporting documents, timeline of transactions, prior-year comparisons, anomaly explanations. Reduce prep from days to hours.

**Impact:** High | **Effort:** Large
**Technical notes:** Cross-domain query (financial + document + timeline). New report generation pipeline. Document assembly from RAG corpus.

---

### F20. Multi-Language Support

**Problem:** Many mid-size firms serve immigrant business communities. Language is a barrier.

**Solution:** Spanish, Mandarin, Vietnamese financial assistance. The LLM handles translation; the data layer is language-agnostic. Interface localization for the most common languages in the firm's client base.

**Impact:** Medium | **Effort:** Medium
**Technical notes:** LLM handles translation natively. Frontend i18n framework. Prompt engineering for financial terminology in target languages. Start with Spanish (largest demand).

---

## Anti-Patterns: What NOT to Build

| Don't | Why |
|-------|-----|
| General-purpose AI assistant | ChatGPT exists. Our value is firm-specific data. |
| Accounting automation (invoicing, reconciliation) | Botkeeper and Vic.ai own this space. We're intelligence, not automation. |
| Enterprise features first | Long sales cycles, custom requirements. Win small firms first. |
| Features before alpha feedback | Ship, learn, iterate. Everything above is post-alpha. |
| Custom reporting engine | Build on the dynamic SQL generator, not a separate reporting product. |
| Compliance/audit software | Crowded market (CaseWare, Wolters Kluwer). Stay in your lane. |

---

## Prioritization Framework

When it's time to pick the next feature, score on:

| Factor | Weight | Question |
|--------|--------|----------|
| Customer pull | 40% | Are customers asking for this? |
| Retention impact | 25% | Does this make them use the product daily? |
| Competitive moat | 20% | Does this get harder to replicate over time? |
| Engineering effort | 15% | Can we ship it in one sprint? |

Features with customer pull + retention impact + moat potential should always win over "cool but nobody asked for it."

---

*This document is a living roadmap. Features will be promoted to stories when customer feedback and business timing align. See `docs/roadmap-forward.md` for the engineering execution timeline.*
