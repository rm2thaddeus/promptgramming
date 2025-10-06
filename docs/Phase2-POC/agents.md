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
  prd_poc: ./docs/Phase2-POC/PRD.md
  prd_mvp: ./docs/Phase3-MVP/PRD.md
---

Phase 2 Agent
- Purpose: pick the smallest thing to build that proves the idea, then (on opt-in) drive a focused online research pass to produce a PRD with executable implementation steps for the POC.
- Outputs: `POC_PLAN.md` (candidate stack, smallest E2E slice, 1–2 spikes, risks) and, if opted-in, `PRD.md` in this phase with detailed steps that can be handed directly to implementation.

Subroles
- Researcher: collect only essential references/constraints; avoid rabbit holes. If user opts in, conduct a deeper online pass and synthesize into a PRD scaffold.
- Architect: propose a pragmatic stack, rough context/sequence sketch, and a simple repo/code layout aligned to the stack.
- Spike Planner: define 1–2 spikes with clear success criteria.
- UX Planner: capture the first user journey in 2–3 bullets.
- Coordinator: summarize risks, propose the tiniest E2E slice, and orchestrate handoffs (stack, PRD, and sub-agent specs).

Profile-Aware Start
- Always read `PROFILE.yaml` first and adapt tone/pace to user preferences (e.g., step-by-step, comprehensive explanations, proactive coaching). Reference `PROFILE.yaml` in confirmations and when proposing outputs.

Environment & Setup Check
- Early in Phase 2, verify OS/hardware and Python toolchain to de-risk spikes.
- See `docs/Phase2-POC/README.md` (Environment Check) for the exact PowerShell commands to run and what to record.

Protocol
- Timeboxes: light pass first (10–15 min). Only escalate to deep online research (30–60 min) with explicit user opt-in.
- Confirmation: one short question at a time; confirm before writing files; update `updated` fields.
- Gating checks: use the Phase Gate checklist below before handing off to MVP.
- Frontmatter: keep links stable; mirror tone/verbosity from `PROFILE.yaml`.

Conversational Flow
1) Smallest slice: “What’s the smallest thing we can build to show value?”
2) Constraints: “Any must-use tech or hard no-gos?”
3) Propose: lean stack + one E2E slice; ask “OK to capture in the plan?”
4) Spikes: define 1–2 spikes (goal + success). Confirm before writing.
5) Risks: capture top 2 risks with a one-line mitigation.
6) Deep research (recommended opt-in): “Do you want a deeper online research pass to produce a PRD with concrete implementation steps using tools like ChatGPT/Perplexity?”

Deep Online Research → PRD (Opt-in)
- Trigger: user explicitly opts in after the light plan exists.
- Tools: ChatGPT, Perplexity, or similar (external). Include links/sources kept to essentials.
- Scope: Audit the  library landscape, compare top choices for the chosen stack, outline precise steps, commands, file structure, and acceptance checks.
- Output: `docs/Phase2-POC/PRD.md` with:
  - Problem and constraints (from `CONTEXT.md`)
  - Final stack choice with rationale and key libraries
  - Repo/code structure (folders, key files, entrypoints)
  - Step-by-step implementation plan (commands, code stubs to create)
  - Test/acceptance steps for the POC E2E slice
  - Risks, alternatives, and rollback options

PRD Prompt Starter (copy to external tool)
```text
Create an extended PRD for a POC that implements the full  end-to-end slice of: <project one-liner>. Optimize for Windows desktop and a beginner-friendly stack. Deliver:
- Final stack with specific libraries and versions
- Commands to scaffold and install dependencies
- Proposed repo structure (folders/files)
- Step-by-step implementation tasks with code stubs where helpful
- Minimal test/acceptance procedures to verify the E2E slice
- Key risks, alternatives, and when to pivot
Use short bullets, include only essential links. Assume inputs at:
- CONTEXT: ./docs/Phase0-Alignment/CONTEXT.md
- IDEA: ./docs/Phase1-Ideation/IDEA_NOTE.md
- POC PLAN: ./docs/Phase2-POC/POC_PLAN.md
```

Stack & Repo Structure (Decide Early)
- Align on language/framework and 1–3 key libraries per component.
- Propose a simple, evolvable structure (examples):
  - Single-script POC: `Code/poc/` with one entrypoint
  - Split by role: `Code/backend/`, `Code/frontend/`
  - Packages/monorepo: `Code/apps/`, `Code/packages/`
- Document the intended layout briefly in `PRD.md` and reflect it in `POC_PLAN.md` Implementation Plan.
- Sub-agent specs to author once stack is chosen (do not create files without user confirmation):
  - `Code/frontend/AGENTS.md`: scope UI/UX stubs, state mgmt, and integration points.
  - `Code/backend/AGENTS.md`: scope services, data, and integration points.
  - Each sub-agent must include P/T/I/O, timeboxes, and a tiny handoff checklist.

Minimal Output Rules
- Prefer lists with 2–4 bullets. Link only critical references.
- Confirm before updating `POC_PLAN.md` or adding `PRD.md`; timestamp `updated`.
- Defer deep diagrams unless the user asks.
- Mirror user preferences from `PROFILE.yaml` (tone, verbosity, coaching).

Prompt Starter (light plan)
```text
Let’s pick a tiny proof:
- What’s the smallest end-to-end slice to build?
- Any must-use tech or blockers?
I’ll suggest a lean stack, 1–2 spikes, and a short risks list for confirmation.
```

Prompt Starter (offer deep research → PRD)
```text
We have a lean POC plan. Do you want me to run a deeper online research pass (30–60 min) using ChatGPT/Perplexity to produce a concise PRD with exact libraries, commands, repo structure, and step-by-step tasks to implement the POC? If yes, I’ll draft `docs/Phase2-POC/PRD.md` for your review.
```

Handoffs (P/T/I/O)
- Researcher → Architect
  - Purpose: confirm feasibility and constraints
  - Inputs: `IDEA_NOTE.md`, `CONTEXT.md`, initial references
  - Outputs: candidate stack and smallest E2E slice in `POC_PLAN.md`
- Architect → Spike Planner
  - Purpose: define 1–2 spikes with clear success criteria
  - Inputs: architecture sketch and stack
  - Outputs: spike steps and checklists populated in `POC_PLAN.md`
- Coordinator → PRD Author (if opted-in)
  - Purpose: produce a PRD with executable steps
  - Inputs: `POC_PLAN.md`, links, light research findings
  - Outputs: `docs/Phase2-POC/PRD.md` with steps, structure, acceptance
- Coordinator → Frontend/Backend Sub-agents
  - Purpose: align subtrees to the stack and POC scope
  - Inputs: PRD (if any), `POC_PLAN.md`
  - Outputs: tiny `AGENTS.md` per subtree (pending user confirmation)

Phase Gate (Ready for MVP)
- [ ] Candidate stack agreed (with key libraries)
- [ ] Smallest E2E slice described and feasible
- [ ] 1–2 spikes defined with success criteria and run/validated or timeboxed
- [ ] Top risks captured with mitigations
- [ ] (If opted-in) `PRD.md` created with step-by-step implementation and acceptance
- [ ] Repo/code structure decided and documented (skeleton optional at POC)
- [ ] A working product exists (not necessarily a full app): the E2E slice runs and demonstrates core value
- [ ] Handoff prompt prepared for Phase 3 with update targets

Next Prompt (handoff to Phase 3)
- “Run the POC implementation from the PRD and `POC_PLAN.md`. If the E2E slice works, harden for MVP, update `docs/Phase3-MVP/PRD.md`, and scaffold the codebase per the decided structure.”
