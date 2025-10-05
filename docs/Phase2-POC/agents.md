---
phase: 2
artifact: agents
project: <project_name>
owner: <user_or_team>
updated: <YYYY-MM-DD>
sources: []
links:
  profile: ./docs/Phase0-Alignment/PROFILE.yaml
  context: ./docs/Phase0-Alignment/CONTEXT.md
  idea: ./docs/Phase1-Ideation/IDEA_NOTE.md
  poc: ./docs/Phase2-POC/POC_PLAN.md
---

Agent Roster (Targeted)
- Researcher:
  - Purpose: answer feasibility questions; identify dependencies and comparables
  - Triggers: Phase 2 kick-off
  - Inputs: IDEA_NOTE.md, CONTEXT.md
  - Outputs: feasibility notes, references, open questions

- Architect:
  - Purpose: propose candidate stack and sketch architecture
  - Triggers: after initial research
  - Inputs: research notes, constraints
  - Outputs: candidate stack, context/sequence sketch in POC_PLAN.md

- Spike Runner:
  - Purpose: define 1–2 spikes with clear success criteria
  - Triggers: after stack options exist
  - Inputs: architecture sketch
  - Outputs: spike plans with steps, expected outcomes

- UX Planner:
  - Purpose: draft personas, journey, and wireframe notes
  - Triggers: alongside architecture planning
  - Inputs: goals, constraints
  - Outputs: concise UX notes in POC_PLAN.md

- Coordinator:
  - Purpose: consolidate risks/mitigations and propose smallest E2E slice
  - Triggers: when spikes are defined
  - Inputs: all above
  - Outputs: risks list and E2E slice proposal

Protocol
- Timebox research; cite 3–5 comparables where relevant.
- Prefer the smallest end‑to‑end slice that validates assumptions.
- Gate to Phase 3 only when:
  - [ ] Feasibility questions are answered or explicitly scoped
  - [ ] Candidate stack is identified with rationale
  - [ ] Architecture sketch captures the MVP slice
  - [ ] 1–2 spikes are planned with success criteria
  - [ ] Key risks and mitigations documented

Handoffs
- Researcher → Architect → Spike Runner → UX Planner → Coordinator.
- Coordinator updates POC_PLAN.md and proposes Phase 3 readiness.

Prompt Starters
```text
Plan the POC:
- Summarize feasibility and dependencies with references.
- Propose a candidate stack and smallest E2E slice.
- Define 1–2 spikes with success criteria.
- Capture top risks and mitigations.
Output: update POC_PLAN.md and a short Phase 3 readiness note.
```

