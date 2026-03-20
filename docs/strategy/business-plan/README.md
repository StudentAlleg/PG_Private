# Business Plan — Multi-Agent Exercise

This folder holds the **full business plan** for Project Green, produced via a **multi-agent handoff** process. Each section is owned by one agent (A–F); agents read shared state and prior sections, then write their section and update the state file. The result is a single, coherent plan without copying existing strategy docs verbatim.

## Purpose

- Produce one cohesive business plan in one place.
- Use existing strategy docs as **read-only inputs** (see [business_plan_state.md](business_plan_state.md)); leave all other strategy files unchanged.
- Output **section files only**. Assembly into one merged document is a **later step**, not part of this run.

## State and task list

**Single source of truth:** [business_plan_state.md](business_plan_state.md)

- **Task checklist** — which section each agent owns, completion status, output filename.
- **Prior/source material** — list of strategy docs agents must read for consistency.
- **Round summaries** — after each agent run, "Key content produced" and findings are appended so the next agent has context.

## Section list and output files

| # | Section | Agent | Output file |
|---|---------|-------|-------------|
| 1 | Problem, opportunity & why now | A | `01-problem-opportunity-why-now.md` |
| 2 | Solution & product | B | `02-solution-and-product.md` |
| 3 | Market size & competition | C | `03-market-and-competition.md` |
| 4 | Business model, GTM & sales | D | `04-business-model-and-gtm.md` |
| 5 | Financial projections & unit economics | E | `05-financials.md` |
| 6 | Traction, team, ask & risks | F | `06-traction-team-ask-risks.md` |

**Order:** A → B → C → D → E → F. Same order is used in the Rebuild run for comparability.

## How to run the agents

1. **Read** — State file ([business_plan_state.md](business_plan_state.md)), any prior section files already written, and the source material listed in the state file.
2. **Write** — One section file (e.g. `02-solution-and-product.md`) in this folder. Use the filenames in the table above.
3. **Update state** — In [business_plan_state.md](business_plan_state.md): mark the section done (checkbox) and add a short "Key content produced" (and any cross-cutting findings) under the corresponding Round Summary.

In Cursor, the AI "plays" one agent at a time (e.g. "run Agent B"); handoff is file-based via the state file and section files.

## Assembly and Rebuild comparison

- **Assembly:** Turning the six section files into one merged business plan document is **out of scope** for this exercise; do that in a separate step when ready.
- **Rebuild run:** The same section list and state structure are used in **ProjectGreenRebuild** (BMAD template, Claude sub-agents). That allows a direct comparison: Cursor (one AI, sequential agents) vs Claude (native sub-agent teams) on the same inputs and outline.
