---
title: Promptgramming Landing Page PRD
updated: 2026-02-03
owner: aitor
status: draft
scope: docs/plans/2026-02-03-promptgramming-landing-page-prd.md
links:
  repo: ./README.md
  phase0: ./docs/Phase0-Alignment/README.md
  phase1: ./docs/Phase1-Ideation/README.md
  phase2: ./docs/Phase2-POC/README.md
  phase3: ./docs/Phase3-MVP/README.md
  proof_skills: https://github.com/rm2thaddeus/Aitor_Skills
  proof_pixel: https://github.com/rm2thaddeus/Pixel_Detective
---

# Promptgramming Landing Page PRD

## 1. Summary
Build a single-page GitHub Pages landing page for the Promptgramming repo that blends marketing clarity with a product explainer. The page must convey that non-technical users can reach production-ready outcomes by following the Translation Hill methodology. The tone should be confident, professional, and accessible.

Primary audience: non-technical founders and PMs who want to ship production code without being engineers.

## 2. Problem & Audience
### Problem
Non-technical builders struggle to translate ideas into production systems. They lack the process to turn intent into reliable artifacts, and they don’t know how to use LLMs to cover skill gaps without losing control.

### Audience
- Non-technical founders / PMs
- Scientists and domain experts with limited engineering skills
- People who can describe a product, but can’t code it alone

## 3. Goal & Promise
### Goal
Make the Translation Hill process obvious and compelling, showing a repeatable path from idea to production.

### Promise
“Production code by non-technical users—guided step-by-step by an AI-assisted methodology.”

## 4. Core Narrative
Translation Hill is a process that turns human intent into buildable artifacts by asking the right questions in sequence and delegating sub-tasks to LLMs. The system reduces ambiguity, preserves context, and drives momentum from alignment to MVP.

## 5. Information Architecture (Single-Page)
### Required Sections
1. Hero
- Headline: “Production code by non-technical users.”
- Subheadline: how the system guides users through a repeatable process.
- Primary CTA: “Use the template (free)” -> repo link
- Secondary CTA: “See proof (Pixel Detective)” -> section anchor

2. Translation Hill Overview
- 1–2 short paragraphs
- Emphasize “ask the right questions in sequence” + “LLMs handle the parts you can’t.”
- 4-step diagram with captions

3. Workflow (Phases 0–3)
- User-friendly labels + explicit phase numbers
- Each phase: 1-sentence goal + key artifact output
- Must be simple for non-technical readers

4. How It Works Diagram
- Visual: pipeline / flowchart
- Inputs: user intent, constraints, context
- Outputs: PROFILE, IDEA_NOTE, POC_PLAN, PRD + prototype

5. Proof: Pixel Detective
- Highlight as real project built through this method
- Use “vibe coding manifesto” line from README
- Emphasize: microservices, Qdrant vector DB, UI/UX, GPU acceleration
- Link to repo

6. Proof: Aitor Skills
- Show as a smaller proof artifact (skills system + GitHub Pages)
- Link to repo

7. CTA / Open-Source Callout
- “Use the template, it’s free.”
- Encourage sharing + reach out

## 6. Content Requirements
- Avoid jargon unless defined
- Phrase benefits for non-technical users
- Emphasize repeatability and safety gates
- Keep sections short and scannable

## 7. Visual Direction
- Synthetic biology + evolutionary metaphor
- Use clean, professional typography
- Use light background with organic gradients or mesh
- Include subtle motion (e.g., animated line / pulsing flow)
- Avoid dark-mode bias

## 8. Nanobanana Image Plan (Schematic Style)
Generate 3 schematic visuals that explain the framework.

### Image A: “Translation Hill Pipeline”
- Visual: 4-node hill or stepped pathway with arrows
- Labels: Phase 0, Phase 1, Phase 2, Phase 3 + outputs
- Tone: clean, blueprint-like

Prompt:
“A clean schematic illustration of a 4-stage hill pathway labeled Phase 0 to Phase 3, with arrows showing upward progress. Each stage has a small artifact icon (profile, idea note, architecture plan, MVP). Minimalist vector style, light background, teal and amber accents, professional product diagram.”

### Image B: “Intent to Production”
- Visual: left-to-right pipeline from ‘Intent’ to ‘Production’
- Includes LLMs as helper nodes
- Emphasize translation steps

Prompt:
“Minimalist schematic flow diagram: ‘Intent’ on the left flowing through four labeled steps into ‘Production’. Include small LLM helper nodes supporting the steps. Thin line art, blueprint aesthetic, soft neutrals with teal highlights, clean labels, professional tech diagram.”

### Image C: “Evidence & Safety Loop”
- Visual: loop showing evidence capture ? synthesis ? proposal ? human approval
- Aligns with safety gating concept

Prompt:
“Schematic loop diagram with four nodes: Evidence capture, Synthesis, Proposal, Human approval. Circular flow, simple icons, minimalist vector style, soft beige background, teal and orange accents, clear labels, professional.”

## 9. Success Criteria
- A non-technical reader understands the 4 phases in < 60 seconds
- The page convinces the reader the process can yield production code
- Proof sections feel credible and concrete
- Visuals are professional and non-gimmicky

## 10. Build Checklist (Execution)
- [ ] Decide final file location for GitHub Pages (single `index.html` at repo root or `docs/`)
- [ ] Draft copy for all sections
- [ ] Design layout with synthetic biology theme
- [ ] Add Translation Hill diagram
- [ ] Add Workflow phase cards with outputs
- [ ] Add Pixel Detective proof block + link
- [ ] Add Aitor Skills proof block + link
- [ ] Generate 3 nanobanana schematic images (or placeholders)
- [ ] Integrate images into page
- [ ] Add CTA section
- [ ] Test in browser at desktop + mobile

## 11. Open Questions
- Should GitHub Pages serve from repo root or `docs/`?
- Do we want the nanobanana images generated now or later?
- Do we want a short “about the author” footer?
