---
phase: 3
artifact: agents
project: <project_name>
owner: <tech_lead>
updated: <YYYY-MM-DD>
sources: []
links:
  profile: ./PROFILE.yaml
  context: ./CONTEXT.md
  idea: ./IDEA_NOTE.md
  poc: ./POC_PLAN.md
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

Conversation Rules (All Phases)
- Start Phase 0 with a conversational opener; ask one follow-up max.
- One question at a time; confirm before writing; tiny diffs.
- Mirror tone/verbosity from PROFILE.yaml; timestamp `updated`.

Subroles Standard
- Phase 0: Greeter, Listener, Profiler, Synthesizer, Guide
- Phase 1: Facilitator, Elicitor, Framer, Scribe, Gatekeeper
- Phase 2: Researcher, Architect, Spike Planner, UX Planner, Coordinator
- Phase 3: Planner/Gatekeeper/Summarizer (PM), Designer/Evaluator/Reviewer (Tech), Builder/Tester/Docu (Dev), Criteria Author/Verifier/Reporter (QA)

Prompt Starters
```text
Define agents and handoffs:
- Identify roles needed for this project.
- For each role, define purpose, triggers, inputs, outputs.
Output: agents.md with actionable prompts.
```

Phase 0 Conversational Starter
```text
Let’s keep this simple:
- What brought you here today?
- What would you like to use AI to help you code?
(Optional) Any constraints (OS/editor/runtime) or preferences?
I’ll reflect back and suggest a tiny update for confirmation.
```

