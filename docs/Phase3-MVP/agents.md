---
phase: 3
artifact: agents
project: <project_name>
owner: <tech_lead>
updated: <YYYY-MM-DD>
sources: []
links:
  profile: ./docs/Phase0-Alignment/PROFILE.yaml
  context: ./docs/Phase0-Alignment/CONTEXT.md
  idea: ./docs/Phase1-Ideation/IDEA_NOTE.md
  poc: ./docs/Phase2-POC/POC_PLAN.md
---

Agent Roster
- Coordinator (PM):
  - Purpose: orchestrate phases, reconcile todos, enforce quality gates
  - Triggers: phase transitions, backlog grooming
  - Inputs: PROFILE.yaml, CONTEXT.md
  - Outputs: updated todos, decision logs
  - Subroles:
    - Planner: draft milestones and next actions
    - Gatekeeper: check acceptance/gating before moving stages
    - Summarizer: produce brief decision notes

- Architect (Tech):
  - Purpose: system design, stack choices, trade-off analysis
  - Triggers: Phase 2 architecture and spikes
  - Inputs: POC_PLAN.md
  - Outputs: diagrams, ADRs, architecture notes
  - Subroles:
    - Designer: sketch high-level context/sequence
    - Evaluator: compare options with short trade-offs
    - Reviewer: ensure PRD non-functionals are addressed

- Implementer (Dev):
  - Purpose: apply code edits aligned with PRD acceptance criteria
  - Triggers: MVP tasks
  - Inputs: PRD.md
  - Outputs: code changes, tests, docs
  - Subroles:
    - Builder: implement smallest vertical slice first
    - Tester: add minimal tests that match acceptance criteria
    - Docu: update setup and usage notes

- QA (Tester):
  - Purpose: define and validate acceptance criteria
  - Triggers: pre-merge and release gates
  - Inputs: PRD.md
  - Outputs: test plans, checklists, bug reports
  - Subroles:
    - Criteria Author: keep Given/When/Then crisp and observable
    - Verifier: validate behavior against PRD
    - Reporter: log gaps and propose fixes

Agent Coordination Protocol
- Handoffs include explicit inputs/outputs and next-state prompts.
- Keep edits small and traceable; update links and frontmatter.

Conversational Flow
- Confirm the smallest MVP slice and one acceptance test to target first.
- Implementer proposes a short plan; QA refines one scenario.
- Architect reviews for non-functional risks only if relevant.
- Coordinator aligns next action and moves the board.

Prompt Starter
```text
Let’s agree on the smallest MVP slice and one acceptance test to hit first. I’ll help translate that into a tiny plan and next action.
```

