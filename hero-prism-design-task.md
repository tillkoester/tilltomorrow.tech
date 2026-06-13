# Hero Prism Redesign + Background Refinement — Opus Task

## Task
Read the current DESIGN.md at `/opt/vault/Projects/workshop-landing/DESIGN.md` (vault copy; working copy at `/opt/data/tasks/design-result.md`) and the live page at https://3cd86894.tilltomorrow-tech.pages.dev. Redesign the hero visual element and refine the background/drift system.

**Use Opus** (`--model opus`). This is design reasoning, not implementation.

## What to do

### 1. Redesign the Hero Visual
The current glass prism (right side of hero) was called "random, macht keinen Sinn" — users don't understand what it represents. 

**Replace it with one of:**
- A stylized Hermes workflow screenshot / UI mockup (abstract enough to be universal, concrete enough to say "this is an AI agent")
- An abstract but recognizable visual that says "automation, agent, system" without being a random geometric shape
- Something that connects to the headline "You're Already Using ChatGPT. Now Make It Work For You."

**Design principles:**
- Must work with the iridescent glass language (backdrop-filter, chromatic edges — see DESIGN.md §4)
- Must fit the hero right-column slot (roughly 400-500px wide on desktop)
- Must not distract from the headline
- Must be understandable in 2 seconds

### 2. Refine Background & Drifts
The canvas is now **#FFFFFF** (pure white). Drifts are at 58% opacity. Evaluate:

- Are the three drift blobs balanced against the white background?
- Do they need size adjustments? Color adjustments?
- Is the 2% grain overlay still appropriate on pure white?
- Should any section backgrounds (canvas-2, canvas-3) change now that canvas-1 is white?

### 3. Document Changes in DESIGN.md
Update the DESIGN.md with:
- New hero visual specification (replace current §4.1)
- Any adjusted drift/bloom specifications (update §2.4)
- Any adjusted canvas tones (update §2.1)

## Output
Write your result to `/opt/vault/Projects/workshop-landing/DESIGN.md` (and sync working copy to `/opt/data/tasks/design-result.md` for the pipeline) Include:
1. Updated DESIGN.md with all changes
2. A brief explanation of your reasoning for the hero visual choice
3. Concrete CSS/implementation notes for the new hero element

## Context
- **Site URL:** https://3cd86894.tilltomorrow-tech.pages.dev
- **DESIGN.md:** `/opt/vault/Projects/workshop-landing/DESIGN.md`
- **Project:** KI-Automation Workshop landing page
- **Mood:** "Warm light meets cool glass" — warm, clean, iridescent accents, no corporate, no playful
- **Fonts:** Fraunces (display), Geist Sans (body), JetBrains Mono (meta)
