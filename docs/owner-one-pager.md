# Owner One-Pager — Michael Leavenworth

*Personal accountability and next steps. Internal only.*

---

## Who You're Accountable To

| Party | What you owe them |
|-------|--------------------|
| **Alpha customer** | Working system on their data, support, check-ins, path to paid. Success = 3–5 staff using it in 30 days. |
| **Owen** | 25% stake, committed. If he gets a full-time offer elsewhere, the 25% remains. Path to full-time here by Q3 2026 if we get there. |
| **Advisors (6)** | Periodic updates; don’t leave them in the dark. |
| **Parr3 (W2)** | Fully aware of what you’re doing; legal leave-behind docs (from Legal Review) already provided. Compliance with employment/confidentiality; investor conversation only after attorney clears. |
| **2026 plan** | Ship beta, first paying customer, flywheel (case study + pipeline). |

---

## Next Business Actions (Non-Technical)

1. **Legal (unblocks everything)** — **In progress.** CA startup attorney engaged. Disclosed to work (Parr3); they’re aware; leave-behind document provided. Attorney assessment expected this afternoon; follow-up meeting tomorrow. Entity formation follows once clear.
2. **Alpha commitment** — **Update sent.** You’ve looped them in (not a pitch): integration central, possible super-early friends/family round, team (you + technical co-developer), advisory board (6 @ 0.25%), startup attorney retained. Still to do: formal one-pager on what you’ll deliver by when, check-in cadence, path to paid.
3. **Owen** — 25% committed; stake stays even if he takes a full-time offer elsewhere. Possible later: onboard a CTO, dilute (you + Owen) to give CTO ~10%. Keep aligned on when/how full-time here is in play.
4. **Stakeholder rhythm** — You’re keeping everyone in the loop (possibly overcommunicating); comfortable here. Alpha and advisors stay updated.
5. **Fundraising sequence** — Attorney is actively reviewing your employment agreements; you’ve already given Parr3 the legal leave-behind docs (Legal Review folder), so W2 is fully aware. Once attorney clears → entity formation → then Parr3 as Stage 1 lead. No pitch before legal clarity.
6. **Flywheel** — Andrew (board advisor) is ready to run GTM: assessments, then case studies. He’s got the plan and personas; he’s gated by legal, which you’re working on. Alpha → case study → 3+ warm leads once the gate lifts.

---

## Product Focus (Build)

1. **Live QBO** — Alpha agreement promises “real data.” Get QBO developer account (if needed), wire real client in onboarding, one successful full sync + ETL for alpha firm. Update runbook so “live QBO” is the path for alpha.
2. **Runbook dry run** — Deploy from scratch using `docs/runbook/alpha-deployment.md`, then onboard a test firm with `docs/runbook/customer-onboarding.md`. Fix any gaps so handoff is repeatable.
3. **Frontend ↔ backend** — Confirm React (Dashboard, Clients, Workflows, Reports) calls real APIs and shows lakehouse data; fix placeholders or broken wiring.
4. **Tests** — Add tests for the 6 tool modules that don’t have them yet; keep critical paths (QBO, onboarding) covered.
5. **Doc refresh** — When you have a slot: update `docs/current-state.md` and CLAUDE “Living Section” so they describe the rebuild, not the prototype.

---

## Quick Reference

- **Strategy:** `docs/strategy/executive-strategy-brief.md`
- **Alpha terms:** `docs/strategy/alpha-customer-agreement.md`
- **Fundraising:** `docs/strategy/fundraising/fundraising-strategy.md`
- **Legal checklist:** `docs/strategy/fundraising/legal-prerequisites.md`
- **Risk register:** `docs/strategy/risk-register.md`

---

*Last updated: 2026-03-06 — Legal: attorney engaged (Grey Ocean, 3/3/2026); Parr3 fully aware; awaiting legal opinion. All GTM paused pending resolution ([Risk Register R22](strategy/risk-register.md)). Required sequence: legal opinion → employer conversation → resolution → entity formation → GTM. Product build at Sprint 13.2, 505 tests.*
