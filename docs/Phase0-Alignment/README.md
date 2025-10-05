# Phase 0 - Alignment

## Purpose
Establish collaboration norms, infer user profile, and define the main project idea through structured conversation.

## Key Activities
- **User Profiling**: Understand editor, OS, experience level, communication style
- **Collaboration Setup**: Define how AI and user will work together
- **Idea Articulation**: Help user express their main project idea in one clear sentence

## Deliverables
- `PROFILE.yaml` — User profile and collaboration preferences
- `CONTEXT.md` — Project background, constraints, and main idea

## Agents Quick Start
- Open `docs/Phase0-Alignment/agents.md`.
- Run the Level 1 Prompt Starter (progressive disclosure, 5–10 minutes).
- Update `PROFILE.yaml` (gaps, preferences) and `CONTEXT.md` (one‑sentence idea, env).
- Decide: continue to Level 2/3 or proceed to Phase 1.

## Base Prompt
```text
You are my AI pair programmer. Start Phase 0 (Alignment) - Expertise Assessment.
- Assess my technical expertise gaps using the EXPERTISE_ASSESSMENT.md framework.
- Identify specific areas where I need targeted assistance.
- Help me articulate the main project idea in one sentence.
- Adapt your assistance style based on identified gaps.
Output: update PROFILE.yaml with expertise gaps and CONTEXT.md with main idea.
```

## Expertise-Focused Approach
The goal is not to assess general communication preferences, but to identify specific technical knowledge gaps so the AI can provide targeted assistance that bridges expertise while preserving your agency as the decision-maker.

## Assessment Levels
- **Level 1 (5-10 min)**: Core programming, tools, basic prompting
- **Level 2 (10-15 min)**: Specific gaps, learning preferences, collaboration style  
- **Level 3 (15-20 min)**: Advanced concepts, architecture, long-term goals

Choose your preferred depth based on project complexity and available time.

## Success Criteria
- [ ] Technical expertise gaps identified and documented
- [ ] AI assistance strategy tailored to user needs
- [ ] Project context documented with constraints
- [ ] Main idea clearly stated in one sentence
- [ ] Learning path established for priority gaps
- [ ] Collaboration preferences established
