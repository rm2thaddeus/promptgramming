---
phase: 3
artifact: agents
project: <project_name>
owner: <tech_lead>
updated: <YYYY-MM-DD>
sources: []
links:
  profile: ./docs/templates/PROFILE.yaml
  context: ./docs/templates/CONTEXT.md
  idea: ./docs/templates/IDEA_NOTE.md
  poc: ./docs/templates/POC_PLAN.md
---

Agent Roster
- Coordinator (PM):
  - Purpose: orchestrate phases, reconcile todos, enforce quality gates
  - Triggers: phase transitions, backlog grooming
  - Inputs: PROFILE.yaml, CONTEXT.md
  - Outputs: updated todos, decision logs

- Architect (Tech):
  - Purpose: system design, stack choices, trade-off analysis
  - Triggers: Phase 2 architecture and spikes
  - Inputs: POC_PLAN.md
  - Outputs: diagrams, ADRs, architecture notes

- Implementer (Dev):
  - Purpose: apply code edits aligned with PRD acceptance criteria
  - Triggers: MVP tasks
  - Inputs: PRD.md
  - Outputs: code changes, tests, docs

- QA (Tester):
  - Purpose: define and validate acceptance criteria
  - Triggers: pre-merge and release gates
  - Inputs: PRD.md
  - Outputs: test plans, checklists, bug reports

Agent Coordination Protocol
- Handoffs include explicit inputs/outputs and next-state prompts.
- Keep edits small and traceable; update links and frontmatter.

Prompt Starters
```text
Define agents and handoffs:
- Identify roles needed for this project.
- For each role, define purpose, triggers, inputs, outputs.
Output: agents.md with actionable prompts.
```


