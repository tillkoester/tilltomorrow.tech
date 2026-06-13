# Workshop Landing Page Build v11 — Sonnet Task

## Task
Rebuild the workshop landing page at `/opt/vault/Projects/workshop-landing/index.html` (working copy at `/opt/data/websites/workshop-landing/index.html`) using the DESIGN.md v10 at `/opt/vault/Projects/workshop-landing/DESIGN.md` as your visual system, with the new copy and section structure below.

**Use Sonnet** (`--model sonnet`). This is implementation — HTML/CSS, not design reasoning.

## What to build
A self-contained single-file `index.html` with embedded CSS and minimal JS. Replace the existing file at `/opt/data/websites/workshop-landing/index.html` (working copy; vault reference at `/opt/vault/Projects/workshop-landing/index.html`).

## Design System (read first)
Read `/opt/vault/Projects/workshop-landing/DESIGN.md` for ALL visual tokens: colors, typography scale, spacing, component rules (buttons, cards, inputs, nav), motion, glass effects, drifts, accessibility rules.

**Key visual parameters:**
- Canvas: `#FFFFFF` (white)
- Drifts: 3 blobs at ~58% opacity, 120px blur, slow animation
- Iridescent gradient for accents
- Fraunces (display), Geist Sans (body), JetBrains Mono (meta)
- Glass Cards: `backdrop-filter: blur(20px) saturate(140%)` + iridescent border
- 12-column grid, max 1280px, responsive

## Section Order & Copy

Build exactly these sections, in this order:

---

### NAV
- Left: wordmark `tilltomorrow•tech`
- Right: links (Sessions, About, Pricing) + EN/DE toggle (placeholder, non-functional)
- Sticky, transparent at top, frosted glass on scroll

---

### HERO (no section number)

**Headline:**
> You're Already Using ChatGPT.
> Now Make It Work For You.

**Subheadline:**
> Build your own AI agent in one workshop. It handles the tasks you hate — so you can do the work that actually matters.

**Date Chip:**
> → FIRST BATCH: JULY 2026 · LIMITED TO 6 SEATS

**Primary CTA:** Apply for a Spot
**Secondary CTA:** See What You'll Build

**Visual:** Use the hero prism from DESIGN.md §4.1. If DESIGN.md has been updated with a new visual, use that instead.

---

### 01 / THE PROBLEM

**Headline:** You're Using AI. You're Just Not Getting Results.

**Body:**
ChatGPT is open in a tab. You ask it things. Sometimes brilliant. Sometimes not. But here's the gap: you don't have a system. You're prompting, copying, pasting, switching tools — and at the end of the week, the admin is still there. The follow-ups still need writing. The research still takes hours.

That's not AI working for you. That's you working for the AI.

**Callout box (visually distinct, darker background or iridescent border):**
While you're figuring out how to "use AI better," others are automating their inboxes, their scheduling, their research. They're freeing up 10+ hours a week. Every month you wait, the gap gets wider. And harder to close.

**Three benefit lines (use checkmarks or icons):**
- Save hours every week. Automate the grind. Keep the decisions.
- Stop tool-hopping. One agent. Connected to what you already use.
- Stay in control. No monthly SaaS stack. No vendor lock-in. Your agent, your rules.

**Section background:** `--canvas-1` (white)

---

### 02 / WHAT YOU'LL WALK AWAY WITH

**Headline:** After This Workshop, You'll Have an Agent That Actually Works.

**Three result blocks (not glass cards — use a different visual treatment: numbered list or icon-led):**

**1. It handles your inbox.**
Summarizes incoming emails. Drafts replies in your voice. Flags what needs your attention. And here's the difference: it gets to know your clients over time — their tone, their urgency, their patterns. Every interaction makes it smarter. After two weeks, it writes replies the way you would.

**2. It does your research.**
Market comparison? Competitor overview? Summary of a 40-page PDF? Your agent finds it, synthesizes it, delivers a brief. In minutes. Not hours.

**3. Yours. Fully.**
Your workflows. Your data. Your rules. Open-source. No monthly trap. If something better comes along, you take everything and move. No lock-in. No dependency.

**Why this works (smaller text, secondary treatment):**
You're not buying software. You're learning to run an agent that costs a few dollars a month. Connected to your email, calendar, files. Open-source. If something better comes along tomorrow, you take your workflows and move. No lock-in.

**Section background:** `--canvas-2` (slightly off-white to separate from Problem section)

---

### 03 / RESULTS (Social Proof)

**Headline:** This Section Is Empty. For Now.

**Body:**
The first batch hasn't run yet. Instead of fake testimonials, here's an honest placeholder. Tacky? Maybe. But you know where you stand.

**Two placeholder cards (use the same glass card style from DESIGN.md):**
> "FUTURE TESTIMONIAL"
> "This is where someone from Batch 1 tells you what they built."
> — Probably you?

> "FUTURE TESTIMONIAL"
> "Honest placeholder is honest."
> — The internet

---

### 04 / PRICING

**Headline:** What It Costs

**Format details (small grid, integrated — no separate section):**
- 3 sessions · ~3 hours each · Online
- Max 6 people · July 2026

**Pricing (two side-by-side cards or a simple row):**
**299 €** — Early Bird (first 5 seats)
**399 €** — Regular

**Section background:** `--canvas-1` (white)

---

### 05 / ABOUT ME

**Headline:** I Figured This Out the Hard Way. You Don't Have To.

**Body:**
I'm Till. Social media marketing at an agency. Online marketing manager at a travel company. Freelancer helping people get more from their tools. Along the way I hosted workshops, built automations, and kept hitting the same wall: the busywork never stops unless you automate it.

So I set up an AI agent that handles scheduling, research, summaries, drafting — the stuff that eats hours but doesn't need me. And when I saw how much time came back, I realized: this shouldn't be just my thing.

I like breaking complex tasks into simple, actionable steps. I like helping people save time so they can focus on the work that actually matters. That's what this workshop is.

**Layout:** Photo-split (portrait on left/gradient placeholder if no photo, text on right). Follow DESIGN.md §8 for Till's portrait treatment.

---

### 06 / APPLY

**Headline:** Apply for a Spot

**Body:** 6 seats. First batch July 2026. I read every application.

**Form:**
- Name (required)
- Email (required)
- What's your biggest time-waster?
- Submit button: Apply

**Micro-copy beneath button:** Not everyone is a fit. But you might be.

**Form styling:** Follow DESIGN.md component rules for form fields and primary button.

---

### FOOTER
- Wordmark: `tilltomorrow•tech`
- Links: Imprint, Privacy, Contact
- Stamp: "MADE IN BERLIN — 2026" (JetBrains Mono, slightly misregistered, iridescent ink-bleed per DESIGN.md)
- Language switcher: EN / DE

---

## Technical Requirements
- Self-contained single HTML file (`index.html`)
- Embed fonts via Google Fonts (Fraunces variable, Geist, JetBrains Mono)
- All DESIGN.md CSS tokens as CSS custom properties
- Background drifts: 3 blobs, ~58% opacity, 120px blur, CSS @keyframes animation
- Scroll reveal: lightweight IntersectionObserver
- Responsive: desktop → tablet (768px) → mobile (480px)
- Semantic HTML, proper heading hierarchy, focus styles, WCAG AA contrast
- No external libraries
- `prefers-reduced-motion` support

**Output:** Write complete file to `/opt/data/websites/workshop-landing/index.html` (working copy; vault mirror at `/opt/vault/Projects/workshop-landing/index.html`).
