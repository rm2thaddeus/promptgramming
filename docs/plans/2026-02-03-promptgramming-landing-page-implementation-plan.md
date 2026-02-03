# Promptgramming Landing Page Implementation Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Build a single-page GitHub Pages landing site that markets the Translation Hill methodology and explains how non-technical users can reach production-ready outcomes.

**Architecture:** Single `docs/index.html` with embedded CSS/JS, lightweight SVG/diagram elements, and three schematic images in `docs/assets/`. Content mirrors phases 0–3 and includes proof sections.

**Tech Stack:** Static HTML/CSS/JS, GitHub Pages

---

### Task 1: Decide Hosting Location + Create Base Structure

**Files:**
- Create: `docs/index.html`
- Create: `docs/assets/`

**Step 1: Set the page location**
Decide to serve GitHub Pages from `/docs` so the landing page lives at `docs/index.html`.

**Step 2: Create base HTML skeleton**
Create `docs/index.html` with:
- `<head>` including fonts, meta tags, and CSS variables
- `<body>` with top-level container and empty sections

**Step 3: Manual check**
Open `docs/index.html` in a browser to ensure the shell loads.

**Step 4: Commit**
```bash
git add docs/index.html
git commit -m "feat: scaffold landing page"
```

---

### Task 2: Build Layout + Core Sections

**Files:**
- Modify: `docs/index.html`

**Step 1: Add content sections**
Insert the full section structure:
- Hero
- Translation Hill Overview
- Workflow (Phase 0–3 cards)
- How It Works diagram
- Proof: Pixel Detective
- Proof: Aitor Skills
- CTA / Open-source callout
- Footer

**Step 2: Add typography + layout styles**
Implement grid layout, spacing, typography scale, card styles, and responsive breakpoints.

**Step 3: Manual check**
Open in browser and verify layout and section flow on desktop and mobile widths.

**Step 4: Commit**
```bash
git add docs/index.html
git commit -m "feat: add landing page sections"
```

---

### Task 3: Add Diagrams + Motion

**Files:**
- Modify: `docs/index.html`

**Step 1: Add inline diagrams**
Implement:
- Translation Hill 4-step diagram (inline SVG)
- How It Works flow diagram (inline SVG or CSS pipeline)

**Step 2: Add subtle motion**
Add scroll-reveal animation and a simple animated flow line in the pipeline.

**Step 3: Manual check**
Open in browser and verify animations run and are not distracting.

**Step 4: Commit**
```bash
git add docs/index.html
git commit -m "feat: add diagrams and motion"
```

---

### Task 4: Generate Nanobanana Images (Schematic)

**Files:**
- Create: `docs/assets/translation-hill.png`
- Create: `docs/assets/intent-to-production.png`
- Create: `docs/assets/safety-loop.png`

**Step 1: Generate images using imagen skill**
Use the prompts in the PRD (section 8) to generate 3 schematic images.

**Step 2: Add image tags**
Reference the images in relevant sections of `docs/index.html`.

**Step 3: Manual check**
Verify images load and are legible on mobile.

**Step 4: Commit**
```bash
git add docs/assets docs/index.html
git commit -m "feat: add schematic images"
```

---

### Task 5: Final Copy + Proof Accuracy Pass

**Files:**
- Modify: `docs/index.html`

**Step 1: Refine copy for clarity**
Ensure the message is non-technical, with clear outcomes and CTAs.

**Step 2: Validate proof claims**
Use the Pixel Detective README line about the "vibe coding manifesto" and list concrete achievements (microservices, Qdrant, UI/UX, GPU acceleration).

**Step 3: Manual check**
Final browser check for typos, spacing, and CTA links.

**Step 4: Commit**
```bash
git add docs/index.html
git commit -m "chore: finalize copy and proof sections"
```
