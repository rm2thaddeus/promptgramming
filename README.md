Translation Hill Project Template

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
  Output: update docs/templates/PROFILE.yaml and docs/templates/CONTEXT.md.
  """

- Phase 1 refinement
  """
  Move to Phase 1. Refine the idea into structured goals, scope, and assumptions.
  Output: fill docs/templates/IDEA_NOTE.md with frontmatter and a clear objective.
  """

- Phase 2 spike
  """
  Move to Phase 2. Research feasibility, architecture options, and dependencies.
  Output: populate docs/templates/POC_PLAN.md with findings, candidate stacks, and risks.
  """

- Phase 3 implementation
  """
  Move to Phase 3. Draft PRD acceptance criteria and define agents/personas.
  Output: docs/templates/PRD.md and docs/templates/agents.md with checklists and next actions.
  """

MCP and Rules
- Follow project rules in `docs/templates/.cursor/rules/*.mdc` (e.g., debugging, testing, docs, MCP usage).
- Suggested MCP servers: GitHub, Supabase, Browser Tools, Browser Control, Context7, Docker, Mindmap.
- Use the alignment and communication rules for consistent, high-signal exchanges.

Repository Structure
```
├── docs/                    # Documentation and templates
│   └── templates/           # All template files organized
│       ├── PROFILE.yaml    # User profile & collaboration style
│       ├── CONTEXT.md      # Project background & constraints
│       ├── IDEA_NOTE.md    # Refined idea & goals
│       ├── POC_PLAN.md     # Research & architecture
│       ├── PRD.md          # Product requirements
│       ├── agents.md       # AI roles & coordination
│       ├── TEMPLATE_USAGE.md   # Usage guide
│       ├── BRANCHING_GUIDE.md  # Git workflow
│       ├── README.md       # Template documentation
│       └── .cursor/rules/  # MCP and development guidance
├── reference/               # External reference materials
│   └── research/           # Symlinked to C:\Users\aitor\Documents\research
├── Code/                   # Project code (when using template)
│   ├── Backend/
│   └── Frontend/
└── README.md               # This file
```

Notes on the Attached Translation Hill Document
- This template anticipates alignment with the Translation Hill methodology. Where the document specifies patterns, map them into the corresponding phase files and rules.
- Replace placeholders with project-specific details once available.


