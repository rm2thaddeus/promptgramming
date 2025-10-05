---
phase: 1
artifact: agents
project: <project_name>
owner: <user_or_team>
updated: <YYYY-MM-DD>
sources: []
links:
  profile: ./docs/Phase0-Alignment/PROFILE.yaml
  context: ./docs/Phase0-Alignment/CONTEXT.md
  idea: ./docs/Phase1-Ideation/IDEA_NOTE.md
---

Agent Roster (Focused)
- Facilitator:
  - Purpose: convert the main idea into a measurable objective and small goals
  - Triggers: on Phase 1 start
  - Inputs: PROFILE.yaml (preferences), CONTEXT.md (main idea)
  - Outputs: IDEA_NOTE.md objective and goal candidates

- Analyst:
  - Purpose: define success metrics, scope boundaries, and key risks
  - Triggers: after objective is confirmed
  - Inputs: CONTEXT.md, preliminary goals
  - Outputs: metrics, in-scope/out-of-scope, risks in IDEA_NOTE.md

- Scribe:
  - Purpose: structure notes into IDEA_NOTE.md with clear frontmatter
  - Triggers: after Analyst proposes details
  - Inputs: all notes, links
  - Outputs: clean, minimal diffs to IDEA_NOTE.md

- Gatekeeper:
  - Purpose: verify success criteria and propose next step (Phase 2)
  - Triggers: before closing Phase 1
  - Inputs: IDEA_NOTE.md
  - Outputs: checklist status and a Phase 2 readiness summary

Protocol
- Keep iteration tight; propose at most 1–2 goals per pass.
- Reflect PROFILE.yaml preferences (verbosity, tone, review style).
- Gate to Phase 2 only when:
  - [ ] Objective is specific and measurable
  - [ ] Metrics and scope are defined
  - [ ] Top risks are documented

Handoffs
- Facilitator → Analyst: objective → metrics/scope/risk drafts.
- Analyst → Scribe: structured content → IDEA_NOTE.md updates.
- Scribe → Gatekeeper: finalized note → checklist validation and next action.

Prompt Starters
```text
Refine the idea into action:
- Propose a measurable objective (one sentence) based on CONTEXT.md.
- Suggest 2–3 concrete goals and 2–3 metrics.
- Draft in-scope/out-of-scope and top 2 risks.
Output: update IDEA_NOTE.md minimally and propose Phase 2 next step.
```

