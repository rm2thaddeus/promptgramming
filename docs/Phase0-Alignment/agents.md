---
phase: 0
artifact: agents
project: <project_name>
owner: <user_or_team>
updated: <YYYY-MM-DD>
sources: []
links:
  profile: ./docs/Phase0-Alignment/PROFILE.yaml
  context: ./docs/Phase0-Alignment/CONTEXT.md
  expertise_assessment: ./docs/Phase0-Alignment/EXPERTISE_ASSESSMENT.md
  progressive_disclosure: ./docs/Phase0-Alignment/PROGRESSIVE_DISCLOSURE.md
---

Agent Roster (Timeboxed)
- Profiler (Level 1 first):
  - Purpose: quickly infer core environment and expertise; capture main idea
  - Triggers: new project start or reset
  - Inputs: PROGRESSIVE_DISCLOSURE.md (Level 1), EXPERTISE_ASSESSMENT.md
  - Outputs: PROFILE.yaml (initial gaps), CONTEXT.md (one-sentence idea)

- Synthesizer (Scribe):
  - Purpose: normalize answers into structured fields; confirm with user
  - Triggers: after Profiler completes a level
  - Inputs: interview notes, PROFILE.yaml, CONTEXT.md
  - Outputs: minimal diffs to PROFILE.yaml/CONTEXT.md with confirmations

- Guide (Navigator):
  - Purpose: propose next depth or phase with small, clear steps
  - Triggers: after Synthesizer updates artifacts
  - Inputs: PROFILE.yaml gaps, user’s time preference
  - Outputs: 1–2 next actions; optional escalation to Level 2/3

Progressive Disclosure Protocol
- Always start at Level 1 (5–10 min). Escalate only by user opt‑in.
- Keep questions scoped; avoid multi-part prompts unless requested.
- Gate to Phase 1 only when:
  - [ ] PROFILE.yaml has explicit gaps and preferences
  - [ ] CONTEXT.md has a clear, one‑sentence main idea

Handoffs
- Profiler → Synthesizer: raw answers → structured updates and confirmations.
- Synthesizer → Guide: updated artifacts → next step options (Level 2, Level 3, or Phase 1).

Editing Rules
- Prefer small, reviewable patches; update frontmatter `updated` date.
- Mirror the user’s preferred tone and verbosity from PROFILE.yaml.
- Record assumptions in CONTEXT.md; confirm or remove later.

Prompt Starters
```text
Run Level 1 (timebox 7 minutes):
- Ask the 5 Level 1 questions from PROGRESSIVE_DISCLOSURE.md.
- Propose one-sentence main idea; confirm or revise.
- Update PROFILE.yaml (gaps, preferences) and CONTEXT.md (idea, env).
Output: minimal diffs and a choice to continue to Level 2 or Phase 1.
```
