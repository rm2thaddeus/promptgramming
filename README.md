Promptgramming, the Translation Hill Project Template

Purpose
- A reusable, human-readable template to run robust, conversational AI coding projects.
- Implements the Translation Hill methodology across Phases 0–3 with context-carrying frontmatter and reusable base prompts.

Scope
- This repository scaffolds prompts, roles, outputs, and checklists. Replace placeholders with your project specifics as you progress.

How to Use
1. Start at Phase 0 (Alignment). Complete `PROFILE.yaml` and `CONTEXT.md` through a guided conversation.
2. Advance to Phase 1 (Ideation) to refine goals in `IDEA_NOTE.md`.
3. Conduct Phase 2 (POC) research and architecture in `POC_PLAN.md`.
4. Build Phase 3 (MVP) using `PRD.md`, `agents.md`, and your prototype code.

Running the Agents
- Start in `docs/Phase0-Alignment/agents.md`: use the Prompt Starter to run Level 1 from Progressive Disclosure, then update `PROFILE.yaml` and `CONTEXT.md`. Timebox to 5–10 minutes.
- Move to `docs/Phase1-Ideation/agents.md`: refine the objective, goals, metrics, scope, and risks into `IDEA_NOTE.md`.
- Continue with `docs/Phase2-POC/agents.md`: capture feasibility, candidate stack, spikes, and risks in `POC_PLAN.md`.
- Finalize in `docs/Phase3-MVP/agents.md`: draft `PRD.md`, confirm acceptance criteria, and coordinate roles.
- Keep edits small; always update the `updated` field in frontmatter.

Conversation Principles
- Treat dialogue like a compiler: translate human intent into buildable artifacts.
- Use explicit roles, checklists, and frontmatter to preserve context.
- Prefer small, iterative edits with clear acceptance criteria.

Frontmatter Standard (All Phases)
---
phase: <0|1|2|3>
artifact: <file purpose>
project: <project_name>
owner: <person_or_team>
updated: <YYYY-MM-DD>
sources:
  - <reference_or_link>
links:
  profile: ./PROFILE.yaml
  context: ./CONTEXT.md
---

Link Policy
- In this template, cross-phase links inside frontmatter use repo-root style paths: `./docs/<Phase>/<File>` for stability.
- Within the same folder, local paths may be used where appropriate.

Phases Overview
- Phase 0 – Alignment
  - Purpose: establish collaboration norms, infer user profile, define main idea.
  - Outputs: `PROFILE.yaml`, `CONTEXT.md`, a single-sentence main idea.

- Phase 1 – Ideation
  - Purpose: translate the idea into structured goals and assumptions.
  - Output: `IDEA_NOTE.md` (refined idea, goals, constraints, and risks).

- Phase 2 – Proof of Concept (POC)
  - Purpose: feasibility, dependencies, architecture, UX sketch, tech spikes.
  - Output: `POC_PLAN.md` (research notes, references, snippets, experiments).

- Phase 3 – MVP
  - Purpose: implement a minimal end-to-end prototype with docs and roles.
  - Outputs: `PRD.md`, `agents.md`, prototype code, and setup instructions.

Base Prompts (Copy/Paste Starters)
- Phase 0 kick-off
  """
  You are my AI pair programmer. Start Phase 0 (Alignment).
  - Ask about my editor, OS, experience, and preferences.
  - Infer my prompting expertise and communication style.
  - Help me articulate the main project idea in one sentence.
  Output: update PROFILE.yaml and CONTEXT.md.
  """

- Phase 1 refinement
  """
  Move to Phase 1. Refine the idea into structured goals, scope, and assumptions.
  Output: fill IDEA_NOTE.md with frontmatter and a clear objective.
  """

- Phase 2 spike
  """
  Move to Phase 2. Research feasibility, architecture options, and dependencies.
  Output: populate POC_PLAN.md with findings, candidate stacks, and risks.
  """

- Phase 3 implementation
  """
  Move to Phase 3. Draft PRD acceptance criteria and define agents/personas.
  Output: PRD.md and agents.md with checklists and next actions.
  """

MCP and Rules
- Follow project rules in `docs/.cursor/rules/*.mdc` (e.g., debugging, testing, docs, MCP usage).
- Suggested MCP servers: GitHub, Supabase, Browser Tools, Browser Control, Context7, Docker, Mindmap.
- Use the alignment and communication rules for consistent, high-signal exchanges.

Repository Structure
```
├── docs/                    # Phase-organized documentation
│   ├── Phase0-Alignment/    # User profiling & collaboration setup
│   │   ├── PROFILE.yaml    # User profile & collaboration style
│   │   ├── CONTEXT.md      # Project background & constraints
│   │   └── README.md       # Phase 0 guide
│   ├── Phase1-Ideation/     # Idea refinement & goal setting
│   │   ├── IDEA_NOTE.md    # Refined idea & goals
│   │   └── README.md       # Phase 1 guide
│   ├── Phase2-POC/          # Research & architecture
│   │   ├── POC_PLAN.md     # Research & architecture plan
│   │   └── README.md       # Phase 2 guide
│   ├── Phase3-MVP/          # Implementation & requirements
│   │   ├── PRD.md          # Product requirements
│   │   ├── agents.md       # AI roles & coordination
│   │   └── README.md       # Phase 3 guide
│   ├── templates/           # Shared templates & guides
│   │   └── README.md       # Template usage guide
│   └── .cursor/rules/       # MCP and development guidance
├── Code/                   # Project code (when using template)
│   ├── Backend/
│   └── Frontend/
└── README.md               # This file
```

Notes on the Attached Translation Hill Document
- This template anticipates alignment with the Translation Hill methodology. Where the document specifies patterns, map them into the corresponding phase files and rules.
- Replace placeholders with project-specific details once available.

