# Workshop Landing Page Build v13 — Claude Task

## Source
- **DESIGN.md:** `/opt/data/tasks/design-result.md`
- **Live site:** `https://tilltomorrow.tech` (current v12 output)
- **Working copy:** `/opt/data/tasks/workshop-build-v13-task.md`

## Target
- `/opt/data/websites/workshop-landing/index.html` (overwrite)
- Vault mirror: `/opt/vault/Projects/workshop-landing/index.html`

**Use Sonnet** (`--model sonnet`, Medium effort). This is implementation — HTML/CSS, not design reasoning.

---

## ⚠️ DESIGN.md Overrides

Where DESIGN.md and this task conflict, **this task wins**.

| DESIGN.md says | v13 override |
|---|---|
| `canvas-2` (#F4EDE4) for section breaks | Do NOT use `canvas-2` or `canvas-3` anywhere. All backgrounds = `canvas-1` (#FFFFFF). Section rhythm comes from **layout variety + dividers + glass depth**, not background tint. |
| `canvas-3` (#ECE2D5) for footer | Footer = `canvas-1` (#FFFFFF) + subtle top border. |
| Sapphire glass centerpiece (§4.11) | Delete. Replace with blurry iridescent orbs. See 🔴2. |
| Drifts at 72% opacity, multiply blend | Keep drifts. Add scroll-reactive orbs in hero as NEW element. |
| Hero headline 6rem (`display-hero`) | Reduce to 4.5rem. See 🔴3. |
| Section order in build-task.md | Keep current section order from live site. Do not reorder. |

---

## 🔴 CRITICAL

### 🔴 1. Kill ALL off-white — replace section rhythm with dividers + layout variety

Search and destroy: `canvas-2`, `canvas-3`, `#F4EDE4`, `#ECE2D5` → replace with `canvas-1` / `#FFFFFF` everywhere.

**New section separation strategy** (replaces background tint alternation):

- **Iridescent divider** between major sections — 1px tall, full-width, `linear-gradient(90deg, transparent, var(--iris-grad), transparent)` at 40% opacity. Use between sections 01/02, 02/03, 03/04. Never between every section — rhythm needs breathing room too.
- **Layout variety** — no two adjacent sections use the same grid pattern (see per-section specs below).
- **Depth elements** — each section gets ONE primary depth device (glass card, glow, elevation, accent stripe). Never the same device in adjacent sections.

### 🔴 2. Hero: Replace prism with blurry iridescent orbs

Remove the faceted prism entirely. Replace with:

**Blurry Orbs Spec:**
- 3–5 overlapping `radial-gradient()` circles in the hero right column
- Colors from iridescent palette: `iris-violet`, `iris-blue`, `iris-cyan`, `iris-pink` at 30–40% opacity
- Each orb is a soft radial gradient fading to transparent at edges (no hard circle boundary)
- Blur: 80–120px via `filter: blur()` on each orb
- Sizes: 200–400px diameter, varying
- Positioned to overlap and create a soft atmospheric glow

**Motion (3 layers):**
1. **Ambient float:** Each orb on independent 60–90s `@keyframes` sinusoidal drift (translate ±30px)
2. **Scroll parallax:** Orbs translate vertically at 0.1–0.3× scroll speed (back layers slower). `transform: translate3d()` on scroll, rAF-throttled.
3. **Cursor response:** Orbs ease toward cursor at 0.04 lerp, max 60px offset. Pointer-fine only, skip on touch.

`prefers-reduced-motion`: freeze all motion — static orbs at final position.

**Performance:** Pure CSS (`radial-gradient` + `filter: blur()` + `transform`). No SVG, no canvas, no images. Zero KB.

**Reference vibe:** Apple product-page gradient orbs — soft, atmospheric, alive but not distracting.

### 🔴 3. Hero headline: Reduce size + restore rainbow word

- **Size:** Drop hero headline from `6rem` to **4.5rem** on desktop (`clamp(2.2rem, 8vw, 4.5rem)`), 3rem tablet, 2.2rem mobile.
- **Rainbow word:** Apply iridescent gradient text-fill to ONE key word per headline (see 🟠5 for full list).
  ```css
  .rainbow-word {
    background: linear-gradient(135deg, #7C6BFF, #5B8DEF, #7FD8E0, #F7A8C9, #FFC9A8);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }
  ```
- Hero: *"You're Already Using ChatGPT. Now Make It **Work** For You."* — "Work" (already italicized) gets the rainbow.

### 🔴 4. Hero: Add banner polish
- The banner "FIRST BATCH: JULY 2026 · LIMITED TO 6 SEATS" is currently white text on light gray. Fix contrast: use `ink-1` text on a subtle `iris-violet` 8% background, or keep it minimal with `ink-2` on `canvas-1` with a thin bottom border.

---

## 🟠 SECTION-BY-SECTION REDESIGN

Each section uses a DIFFERENT primary device. No two adjacent sections feel the same.

---

### 🟠 5. Section 01 — THE PROBLEM
**Layout:** 2-column (60/40)
**Depth device:** Glass card + iridescent accent stripe

**Left column (60%):**
- Mono label: "01 / THE PROBLEM"
- Heading: "You're Using AI. You're Just Not Getting Results."
- Body paragraph 1
- Body paragraph 2

**Between columns — the callout text** (spans both columns below, or sits between):
> "While you're figuring out how to 'use AI better,' others are automating their inboxes, their scheduling, their research. They're freeing up 10+ hours a week. Every month you wait, the gap gets wider."

Styling for callout:
- Type: `t-md` (Geist 400, 1.25rem, 1.5 line-height)
- Color: `ink-2`
- Left edge: 2px iridescent gradient border (vertical stripe, 135°)
- Generous padding-left (24px) and vertical whitespace
- **No box.** No rainbow top border. No arrow. Just the accent stripe.

**Right column (40%):**
- One **glass card** (DESIGN.md §4.3 spec) containing 3 pain-point rows:
  1. Icon + "You're prompting, copying, pasting" + "...switching tools — the admin is still there"
  2. Icon + "No system, no memory" + "...every session starts from zero"
  3. Icon + "The gap is widening" + "...others are automating 10+ hrs/week while you figure it out"
- Icons: Phosphor Duotone, `ink-2`, 20px
- Rows separated by subtle `ink-3` dividers at 15% opacity

---

### 🟠 6. Section 02 — WHAT YOU'LL WALK AWAY WITH
**Layout:** 3-column card grid
**Depth device:** 3 glass cards with hover lift

- Mono label: "02 / WHAT YOU'LL WALK AWAY WITH"
- Heading: "After This Workshop, You'll Have an Agent That Actually Works."

**3 glass cards** in `repeat(3, 1fr)`:
1. **Card 1:** Icon (envelope/inbox) → "It handles your inbox." → paragraph
2. **Card 2:** Icon (magnifying glass) → "It does your research." → paragraph
3. **Card 3:** Icon (key/lock) → "Yours. Fully." → paragraph

- Each card: `glass-card` component (frosted bg, `backdrop-filter`, 1px `glass-border`, 20px radius, 32px padding)
- **Hover:** Lift 4px over 240ms, shadow deepens to `0 18px 50px rgba(64,58,74,0.11)`, border → `glass-border-hover`
- Icons: Phosphor Duotone, 24px, `ink-2` inside each card
- "Yours." in Card 3 gets rainbow gradient word treatment
- Grid collapses: 3→2 at tablet, 2→1 at mobile

---

### 🟠 7. Section 03 — RESULTS
**Layout:** Centered, big-stat showcase
**Depth device:** Gradient background glow behind the number

- Mono label: "03 / RESULTS"
- Heading: use the rainbow gradient on the key word: *"What **Changes** When You Automate"* (or keep existing if locked)
- **Centered large stat:** E.g. "10+" in Fraunces 300, ~6rem, with a subtle radial glow behind it (`radial-gradient(ellipse, iris-violet 8%, transparent 70%)`)
- Label below stat: "hours freed per week" in `t-base`, `ink-2`
- Small "(placeholder — real results coming)" note in `t-xs`, `ink-3`

This section is intentionally minimal but atmospheric — the glow gives it presence.

---

### 🟠 8. Section 04 — PRICING
**Layout:** 2 pricing cards side by side
**Depth device:** Card elevation + rainbow price highlight

- Mono label: "04 / PRICING"
- Heading: "What It Costs"

**2 cards** in `repeat(2, 1fr)`:
1. **Early Bird:** 299€ (rainbow gradient text!), "Limited — first 6 seats", CTA button
2. **Regular:** 399€ (`ink-1`), "After early bird sells out", CTA button

- Cards: `glass-card` component with Level 1 elevation
- **299€** gets the rainbow gradient word treatment — make it the hero of this section
- Remove "14-day money-back guarantee" — verify it's NOT present (was removed in v12)
- Grid collapses to 1 column at mobile — Early Bird card on top
- Subtle "BEST VALUE" or similar tag-pill on the Early Bird card (DESIGN.md §4.5 tag-pill)

---

### 🟠 9. About Me
**Layout:** 2-column (40/60)
**Depth device:** Portrait frame glow

- Mono label: "05 / ABOUT ME"

**Left (40%):**
- Portrait placeholder (rounded, subtle `box-shadow: 0 0 40px rgba(255,201,168,0.35)` in `iris-peach` glow)
- Keep the existing "(photo coming soon)" treatment

**Right (60%):**
- Heading: "I Figured This Out the Hard Way. You Don't Have To."
- Bio paragraphs
- Pull-quote: *"I've spent the last 3 years deep in AI and automation — so you don't have to start from scratch."*
- Impact message (verify present from v12): *"I want to help people focus on work that actually matters. Work that has impact. Together we can change the world — a little dramatic, but I mean it."*

One word in the pull-quote or impact message gets subtle rainbow gradient.

---

### 🟠 10. Section 06 — APPLY (Application Form)
**Layout:** Centered form, 540px max-width
**Depth device:** Glass card wrapping the form

- Mono label: "06 / APPLY"
- Heading: "Apply for a Spot"
- Subtext: "6 seats. First batch July 2026. I read every application."
- Form (Name, Email, "What's your biggest time-waster?") wrapped in a `glass-card`
- Primary CTA button: "Apply"
- Form fields per DESIGN.md §4.4 (8px radius, iris-blue focus ring)

---

## 🟡 GLOBAL POLISH

### 🟡 11. Rainbow gradient word map

| Section | Target word/phrase |
|---|---|
| Hero | "Work" |
| 01 Problem | "gap" or "system" in the headline |
| 02 Walk Away | "Yours." in Card 3 heading |
| 03 Results | "Changes" or the stat number |
| 04 Pricing | "299€" |
| About Me | One word in pull-quote |

**Rule:** Maximum ONE rainbow word per section. Never on body text. Never on UI labels or buttons.

### 🟡 12. Iridescent dividers between sections

Use between 01→02, 02→03, 03→04. NOT after every section — skip between Hero→01 and 04→About.
```css
.iris-divider {
  height: 1px;
  width: 100%;
  background: linear-gradient(90deg, transparent, var(--iris-grad), transparent);
  opacity: 0.4;
}
```

### 🟡 13. Site-wide motion for life
- **Drift blobs:** Verify they're animate + visible (50–80s loops, scroll parallax)
- **Section reveals:** Each major section fades up on scroll entry (IntersectionObserver, threshold 0.15, 40px rise, 600ms ease-out). Subtle — no bounce, no slide.
- **Button hover sweeps:** Primary buttons get slow iris gradient sweep (DESIGN.md §4.1 — verify working)
- `prefers-reduced-motion`: freeze all non-essential motion

### 🟡 14. Footer
- Background: `canvas-1` (#FFFFFF)
- Top border: `1px solid rgba(122, 114, 134, 0.2)` (ink-3 at 20%)
- Keep existing content: wordmark, links (Imprint, Privacy, Contact), language switcher
- Good as-is otherwise

### 🟡 15. Verify from v12 (don't regress)
- "14-day money-back guarantee" is REMOVED from pricing (was in v12 🔴1)
- Impact message in About Me is present (was in v12 🔴2)
- Grain overlay at 2% (was in v12 🟡6)

---

## ❌ WHAT NOT TO DO

- Do NOT use `canvas-2` or `canvas-3` anywhere
- Do NOT use the faceted prism / Sapphire centerpiece
- Do NOT add boxes, arrows, or rainbow top borders
- Do NOT use the rainbow gradient on body text, buttons, or UI
- Do NOT make adjacent sections use the same layout pattern
- Do NOT change section order or copy (except where explicitly instructed)
- Do NOT add new sections
- Do NOT use emoji, stock icons, or decorative SVG illustrations
- Do NOT pure `#000` for text — always `ink-1` (#1A1820)

---

## Rule

This task file is the specification. Where it conflicts with DESIGN.md, this file wins. Every item must be implemented exactly.

All existing CSS custom properties (tokens) are available. Use them. The iridescent palette covers everything.
