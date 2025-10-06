# Phase 1 - Ideation

## Purpose
Translate the main idea into structured concepts, actionable goals, and clear scope boundaries.

## Key Activities
- **Goal Refinement**: Convert the main idea into concrete, measurable objectives
- **Scope Definition**: Establish what's in-scope and out-of-scope
- **Risk Assessment**: Identify assumptions and potential risks
 - **Lightweight Research **: 15–20 min websearch  scan of comparable solutions, common patterns, and quick sources
 - **Technical Quicklook**: sketch a plausible stack and surface 2–3 unknowns/feasibility notes

## Prerequisites
- Completed Phase 0: `PROFILE.yaml` and `CONTEXT.md` with main idea defined

## Deliverables
- `IDEA_NOTE.md` — Structured idea with goals, scope, and risks

## Agents Quick Start
- Open `docs/Phase1-Ideation/agents.md`.
- Use the Prompt Starter to propose a measurable objective, 2–3 goals, and 2–3 metrics.
- Draft scope (in/out) and top risks; update `IDEA_NOTE.md` minimally.
- Confirm readiness for Phase 2 against the Success Criteria.
 - If the user is a novice or lacks prior research, offer the novice + research starter, run a quick scan (opt-in), and capture findings + quick technical notes in `IDEA_NOTE.md`.

## Base Prompt
```text
Move to Phase 1. Refine the idea into structured goals, scope, and assumptions.
Output: fill IDEA_NOTE.md with frontmatter and a clear objective.
```

## Success Criteria
- [ ] Objective clearly stated and measurable
- [ ] Goals and success metrics defined
- [ ] Scope boundaries established
- [ ] Risks and unknowns identified
- [ ] User preferences reflected from PROFILE.yaml
 - [ ] Research summarized or explicitly deferred by user
 - [ ] Quick technical notes captured (stack, key unknowns)
