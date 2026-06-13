---
version: alpha
name: tilltomorrow Workshop
description: |
  "Warm light meets cool glass." A landing page that feels like
  sunrise filtered through a prism: warm, calm, atmospheric —
  with cool, iridescent blue-purple glints that hint at the
  technical depth behind the workshop.
colors:
  # Canvas (warm bright base)
  canvas-1: "#FFFFFF"
  canvas-2: "#F4EDE4"
  canvas-3: "#ECE2D5"

  # Ink (dark accents — violet undertone, NEVER pure #000)
  ink-1: "#1A1820"
  ink-2: "#403A4A"
  ink-3: "#7A7286"

  # Iridescence (cool glass accents — the heart)
  iris-violet: "#7C6BFF"
  iris-blue: "#5B8DEF"
  iris-cyan: "#7FD8E0"
  iris-pink: "#F7A8C9"
  iris-peach: "#FFC9A8"

  # Chromatic aberration (Sapphire glass edge glow — saturated rim ONLY, never fills)
  chroma-fire: "#FF4D2E"   # red-orange — warm refractive edge (inner)
  chroma-gold: "#FFB22E"   # amber-yellow — warm refractive edge (outer)
  chroma-ice: "#2EC6FF"    # electric cyan — cool refractive edge (inner)
  chroma-cobalt: "#2E6BFF" # deep blue — cool refractive edge (outer)

  # Drifts (Marimba-style background blobs)
  drift-peach: "#FFD9C2"
  drift-rose: "#F8C9D8"
  drift-periwinkle: "#C9D2FF"

  # Semantic
  ok: "#5BBF8A"
  warn: "#E8A65A"
  error: "#D86A6A"

  # Glass surface (computed reference)
  glass-bg: "rgba(255,252,247,0.55)"
  glass-border: "rgba(124,107,255,0.12)"
  glass-border-hover: "rgba(124,107,255,0.26)"

  # Nav frosted
  nav-frosted: "rgba(250,246,241,0.72)"

typography:
  display-hero:
    fontFamily: Fraunces
    fontSize: 6rem
    fontWeight: 500
    lineHeight: 1.02
    letterSpacing: "-0.02em"
  display-hero-xl:
    fontFamily: Fraunces
    fontSize: 8rem
    fontWeight: 500
    lineHeight: 1.02
    letterSpacing: "-0.02em"
  display-2xl:
    fontFamily: Fraunces
    fontSize: 4rem
    fontWeight: 300
    lineHeight: 1.1
    letterSpacing: "-0.02em"
  display-xl:
    fontFamily: Fraunces
    fontSize: 2.5rem
    fontWeight: 400
    lineHeight: 1.18
    letterSpacing: "-0.015em"
  display-lg:
    fontFamily: Fraunces
    fontSize: 1.75rem
    fontWeight: 500
    lineHeight: 1.2
    letterSpacing: "-0.01em"
  body-md:
    fontFamily: Geist Sans
    fontSize: 1.0625rem
    fontWeight: 400
    lineHeight: 1.55
    letterSpacing: "-0.005em"
  body-sm:
    fontFamily: Geist Sans
    fontSize: 0.9375rem
    fontWeight: 400
    lineHeight: 1.55
    letterSpacing: "-0.005em"
  body-xs:
    fontFamily: Geist Sans
    fontSize: 0.8125rem
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: "0em"
  ui-label:
    fontFamily: Geist Sans
    fontSize: 0.9375rem
    fontWeight: 500
    lineHeight: 1.4
    letterSpacing: "-0.005em"
  ui-button:
    fontFamily: Geist Sans
    fontSize: 0.9375rem
    fontWeight: 600
    lineHeight: 1.4
    letterSpacing: "-0.005em"
  ui-button-lg:
    fontFamily: Geist Sans
    fontSize: 1.0625rem
    fontWeight: 600
    lineHeight: 1.4
    letterSpacing: "-0.005em"
  meta-label:
    fontFamily: JetBrains Mono
    fontSize: 0.6875rem
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: "0.12em"
  wordmark:
    fontFamily: Fraunces
    fontSize: 1.08rem
    fontWeight: 400
    lineHeight: 1
    letterSpacing: "-0.01em"

rounded:
  card: 20px
  pill: 9999px
  input: 8px

spacing:
  xs: 8px
  sm: 16px
  md: 24px
  lg: 48px
  xl: 64px
  section: 96px
  section-tablet: 64px
  section-mobile: 48px
  gutter: 24px
  gutter-mobile: 16px

components:
  button-primary:
    backgroundColor: "{colors.ink-1}"
    textColor: "{colors.canvas-1}"
    rounded: "{rounded.pill}"
    padding: 14px 28px
    typography: ui-button-lg
  button-secondary:
    backgroundColor: transparent
    textColor: "{colors.ink-1}"
    rounded: "{rounded.pill}"
    padding: 14px 28px
    typography: ui-button-lg
  glass-card:
    backgroundColor: "{colors.glass-bg}"
    textColor: "{colors.ink-2}"
    rounded: "{rounded.card}"
    padding: 32px
  form-field:
    backgroundColor: "{colors.canvas-1}"
    textColor: "{colors.ink-1}"
    rounded: "{rounded.input}"
    padding: 12px 16px
  tag-pill:
    backgroundColor: transparent
    textColor: "{colors.ink-2}"
    rounded: "{rounded.pill}"
    padding: 6px 14px
    typography: body-sm
---

# DESIGN.md — v12

**Project:** tilltomorrow.tech — KI-Automation Workshop Landing Page
**Status:** Visual identity system, 9-section extended spec
**Languages:** EN / DE (bilingual, parity assumed)

---

## 1. Visual Theme & Atmosphere

Three forces hold the page in tension:

1. **A warm, breathing canvas** — pure white, animated by slow-drifting peach/rose/periwinkle blobs (Marimba-style). These are now a *foreground atmosphere*, not a faint wash: larger, more saturated, with gentle scroll-parallax and a soft cursor response. Hospitality, not sterility — but unmistakably alive.
2. **The Sapphire glass centerpiece** — a single meaningful glyph refracted through a real-feeling glass block, ringed with chromatic aberration (fire on the warm edge, ice on the cool edge). This is the page's optical heartbeat. It is the *hero device* and recurs as a smaller motif elsewhere — never a random shard. The technology, the "tomorrow," the edge.
3. **A quiet hand-made grain** — used sparingly (2% global noise, one Webgeil callout box, one footer stamp). A garnish, not a sauce.

The result: thoughtful, modern, atmospheric, slightly luxurious, human warmth — with a single cool, refractive heartbeat running through it. Not corporate. Not playful. **Quietly confident.**

> *"It felt warm, but smart — like the inside of a sunlit prism."*

That's the one-sentence test. Every design decision either moves toward or away from it.

**Key characteristics:**
- A 1px iridescent gradient is the page's signature accent — never overused
- Background drifts animate slowly (50–80s loops), making the page feel alive
- Glass cards with backdrop-filter create genuine depth through refraction
- Two doses of handmade texture only (callout box + footer stamp)
- Single primary CTA per section — no competing high-emphasis actions

---

## 2. Color Palette & Roles

### Canvas (warm bright base)

| Token | Hex | Role |
|---|---|---|
| `canvas-1` | #FFFFFF | Primary page background. Pure white, clean canvas. |
| `canvas-2` | #F4EDE4 | Section breaks / inset panels. Slightly deeper warmth. |
| `canvas-3` | #ECE2D5 | Footer / dense info blocks. Sandy, grounding. |

Warmth comes from the drift blobs and iridescent accents — not from tinting the background. This keeps the page crisp.

### Ink (dark accents — violet undertone)

| Token | Hex | Role |
|---|---|---|
| `ink-1` | #1A1820 | Primary headline / body. Near-black with violet undertone — never pure #000. |
| `ink-2` | #403A4A | Secondary body / meta text. |
| `ink-3` | #7A7286 | Tertiary, captions, dividers, placeholder text. WCAG AA at body sizes (5.2:1). |

The violet undertone in `ink-1` is deliberate — it ties dark text to the iridescent palette, so headlines and glass motifs feel like the same family.

### Iridescence (cool glass accents — the heart)

| Token | Hex | Role |
|---|---|---|
| `iris-violet` | #7C6BFF | Deep prism-violet. |
| `iris-blue` | #5B8DEF | Cobalt-glass core. |
| `iris-cyan` | #7FD8E0 | Cool aqua edge. |
| `iris-pink` | #F7A8C9 | Chromatic fringe (rainbow at the edge of the glass). |
| `iris-peach` | #FFC9A8 | Refracted warmth — where iris meets canvas. |

**The Iridescent Gradient (signature device):**

```css
/* 135° (diagonal) for static accents */
linear-gradient(135deg,
  #7C6BFF 0%,
  #5B8DEF 28%,
  #7FD8E0 52%,
  #F7A8C9 78%,
  #FFC9A8 100%);

/* 90° (horizontal) for button/underline sweeps */
linear-gradient(90deg,
  #7C6BFF 0%,
  #5B8DEF 28%,
  #7FD8E0 52%,
  #F7A8C9 78%,
  #FFC9A8 100%);
```

Used for: wordmark prism dot, hero glass shard, button hovers, link underline shimmer, iridescent dividers, and one section's accent text. **Sparingly and with intention.** Never on body text or critical UI labels.

### Chromatic Aberration (Sapphire edge glow)

The saturated rainbow rim that separates the dark refracted glyph from the white field. These colors appear **only as edge glow / offset shadows** — never as fills, never on type, never in the drifts. They are what makes glass read as *glass*.

| Token | Hex | Role |
|---|---|---|
| `chroma-fire` | #FF4D2E | Red-orange. Warm edge, inner ring. |
| `chroma-gold` | #FFB22E | Amber-yellow. Warm edge, outer ring. |
| `chroma-ice` | #2EC6FF | Electric cyan. Cool edge, inner ring. |
| `chroma-cobalt` | #2E6BFF | Deep blue. Cool edge, outer ring. |

Pairing rule: warm fire/gold on one side of an edge, cool ice/cobalt on the opposing side — they sit on *opposite* edges of the same shape (light splitting), never blended into one halo. See §4.11.

### Background Drifts

| Token | Hex | Role |
|---|---|---|
| `drift-peach` | #FFD9C2 | Upper-left, warm anchor. |
| `drift-rose` | #F8C9D8 | Mid-right, romantic flush. |
| `drift-periwinkle` | #C9D2FF | Lower-left, cool counter-note bridging into iridescent palette. |

Reference: the Marimba.designs hero — soft coral/blue orbs that bleed across a near-white field, clearly *present* rather than subliminal.

**Sizing & opacity (revised — must read as foreground atmosphere):**
- Three+ giant soft-edged radial blobs, **~720–1000px** each.
- Opacity **~72%** (raised from 58% — the v10 drifts were "nicht sichtbar genug").
- Blur **140–160px**. Edges always feathered to nothing; never a visible circle boundary.
- `mix-blend-mode: multiply` over `#FFFFFF` keeps them luminous rather than muddy.

**Motion (three layered behaviors):**
1. **Ambient drift** — each blob on an independent 50–80s sinusoidal `@keyframes` loop (translate + slight scale). Never sharp, never fast.
2. **Scroll parallax** — blobs translate vertically at **0.15–0.35× scroll speed** (back layers slowest), so the field shifts gently as you read. Drive via `transform: translate3d()` on scroll (rAF-throttled), not `background-attachment`.
3. **Cursor response (cherry-on-top, low priority)** — the nearest 1–2 blobs ease toward the cursor at **~0.04 lerp**, max offset ~40px. Pointer-fine devices only; skip on touch.

`prefers-reduced-motion`: freeze all three behaviors — static blobs at final opacity, no drift/parallax/cursor. The page must still look composed when motionless.

### Glass Surfaces (computed from canvas + iris)

| Token | Value | Use |
|---|---|---|
| `glass-bg` | rgba(255,252,247,0.55) | Glass card / nav backgrounds |
| `glass-border` | rgba(124,107,255,0.12) | Glass card borders |
| `glass-border-hover` | rgba(124,107,255,0.26) | Glass card hover borders |
| `nav-frosted` | rgba(250,246,241,0.72) | Nav scrolled state |

### Semantic

| Token | Hex | Role |
|---|---|---|
| `ok` | #5BBF8A | Success / confirmation. Form states only. |
| `warn` | #E8A65A | Mild attention, never alarming. |
| `error` | #D86A6A | Errors, validation. Muted, not screaming. |

---

## 3. Typography Rules

### Font Families

| Role | Font | Weights | Fallback |
|---|---|---|---|
| **Display** | Fraunces (variable, opsz, SOFT=50) | 300, 400, 500 | Georgia, serif |
| **Body / UI** | Geist Sans | 400, 500, 600 | Inter, system-ui, sans-serif |
| **Meta / Code** | JetBrains Mono | 400 | Fira Code, monospace |

### Hierarchy Table

| Token | Font | Size / rem | Weight | Line Ht | Tracking | Use |
|---|---|---|---|---|---|---|
| `t-hero` | Fraunces | 96 / 6 | 500 | 1.02 | -0.02em | Hero headline (desktop) |
| `t-hero-xl` | Fraunces | 128 / 8 | 500 | 1.02 | -0.02em | Hero headline (≥1440px) |
| `t-2xl` | Fraunces | 64 / 4 | 300 | 1.1 | -0.02em | Section openers |
| `t-xl` | Fraunces | 40 / 2.5 | 400 | 1.18 | -0.015em | Subsection heads |
| `t-lg` | Fraunces | 28 / 1.75 | 500 | 1.2 | -0.01em | Card titles |
| `t-md` | Geist | 20 / 1.25 | 400 | 1.5 | -0.005em | Lead paragraph, pull-quote text |
| `t-base` | Geist | 17 / 1.0625 | 400 | 1.55 | -0.005em | Body text |
| `t-sm` | Geist | 15 / 0.9375 | 400/500/600 | 1.55 | -0.005em | Secondary body, nav links, buttons |
| `t-xs` | Geist | 13 / 0.8125 | 400 | 1.5 | 0 | Captions |
| `t-mono` | JetBrains | 11 / 0.6875 | 400 | 1.4 | 0.12em | Section labels, meta, date chips |

### Usage Rules

- **Fraunces** for headlines, section openers, wordmark, card titles, pull-quotes. Single italicized word per headline encouraged (one weight lighter).
- **Geist** for body, navigation, buttons, form fields, and all UI. 400 body, 500 nav/UI, 600 button labels.
- **JetBrains Mono** at 11px with 0.12em tracking, uppercase. Section labels ("01 / ABOUT"), date chips, taxonomy, footer stamp. **Never in body text.**
- Hero headline: three lines, staggered fade-up (120ms delay each), 8px rise, 600ms ease-out-quart.
- Hero italic phrase: iridescent underline shimmer, sweeps left-to-right once (~2.5s), then settles.
- All type in `ink-1` color unless specified otherwise. `ink-3` reserved for non-essential captions/meta.

### Responsive Type

| Breakpoint | Hero | Section Head |
|---|---|---|
| Desktop (≥1024px) | `6rem` | `4rem` |
| Tablet (768-1023px) | `clamp(2.6rem, 10vw, 5rem)` | `2.5rem` |
| Mobile (<768px) | `2.5rem` | `2.5rem` |

---

## 4. Components

### 4.1 Primary Button

- **Default:** `ink-1` background, `canvas-1` text, `14px 28px` padding, `999px` radius (full pill).
- **Hover:** Background fills with slow horizontal sweep of the iridescent gradient (0.6s ease, `background-size: 200% 100%`). Text stays `canvas-1`. 1px iridescent outline appears.
- **Active:** `scale(0.98)`.
- **Focus-visible:** 3px ring in `iris-blue` at 40% opacity, offset 2px.
- **No labels in title case. No competing primary CTAs in the same section.**

### 4.2 Secondary Button

- **Default:** Transparent, `ink-1` text, `1px solid ink-3` border, same padding/radius as primary.
- **Hover:** Border becomes iridescent gradient (via `border-image`), text stays `ink-1`.
- **Active:** `scale(0.98)`.
- **Focus-visible:** 3px ring in `iris-blue` at 40%, offset 2px.

### 4.3 Glass Card

- **Default:**
  ```css
  background: rgba(255,252,247,0.55);
  backdrop-filter: blur(20px) saturate(140%);
  border: 1px solid rgba(124,107,255,0.12);
  border-radius: 20px;
  box-shadow: 0 8px 32px rgba(64,58,74,0.06),
              0 1px 0 rgba(255,255,255,0.6) inset;
  padding: 32px;
  ```
- **Hover:** Inset highlight strengthens, border picks up `iris-violet` at 25%, card lifts 4px over 240ms.
- **Solid fallback:** `canvas-1` for browsers without `backdrop-filter`.
- **Iridescent numeral watermark:** Top-right corner, Fraunces 300 at `t-2xl`, iridescent gradient text-fill at 8% opacity.

### 4.4 Form Field

- **Label:** Above input, `t-sm`, `ink-2`, 600 weight.
- **Input:** `canvas-1` background, `1px solid ink-3`, `12px 16px`, `8px` radius.
- **Focus:** Border `iris-blue`, 4px outer ring `iris-blue` at 12% opacity.
- **Error:** Border `error`, helper text `error` below + icon.

### 4.5 Tag Pill

- **Default:** `1px solid ink-3`, `ink-2` text, `6px 14px`, `999px` radius.
- **Hover:** Background flushes to `drift-peach` at 50% opacity, border `ink-2`.

### 4.6 Link (Inline)

- **Default:** `ink-1` (inherits from body), no underline. Distinguishable from body by context or surrounding weight.
- **Hover (nav links):** `ink-1` from `ink-2`.
- **Hover (body links):** Iridescent underline shimmer left-to-right (0.6s). Single direction only.

### 4.7 Iridescent Divider

- 1px tall, full-width.
- `background: linear-gradient(90deg, transparent, var(--iris-grad), transparent)` at 40% opacity.
- Used **once** between major sections. Never after every section — loses its specialness.

### 4.8 Nav

- **Height:** 72px desktop, 60px mobile.
- **Default (scroll-top):** Transparent background.
- **Scrolled (past 40px):** `nav-frosted` background, `backdrop-filter: blur(22px) saturate(180%)`, `1px solid rgba(124,107,255,0.14)` bottom border.
- **Left:** Wordmark (Fraunces italic, `t-1rem`, `ink-1` + prism dot).
- **Right:** 3-4 text links + language switcher + primary CTA button.

### 4.9 Language Switcher

- JetBrains Mono, 11px, `EN / DE`.
- Active: `ink-1`, inactive: `ink-3`, separator: `ink-3`.
- Click toggles active language.
- **No flag icons** (visually noisy, localization anti-pattern).

### 4.10 Link Component (In-body)

- **Default:** `ink-2` with subtle bottom border, 1px solid at `ink-3`.
- **Hover:** Color transitions to `iris-violet`, border transitions to 1px iridescent gradient.

### 4.11 Sapphire Glass Centerpiece (hero device) ★

The replacement for the old "random shard." A single **meaningful glyph** seen *through / inside* a glass block, with chromatic-aberration edges. This is the page's signature object.

**Reference:** Dalibor Pajic "Sapphire" — a glass wedge on matte white, a dark mark inside ringed by a fire-on-one-side / ice-on-the-other glow, with a bright specular corner and a soft caustic shadow.

**The glyph (what's inside the glass) — brand decision, see §9 open question:**
The glyph must be *one recognizable symbol that means something*, not abstract geometry. Candidates, in priority order:
1. A **forward / play chevron** (▸) — reads as "activate, go, make it work, tomorrow." Universal, simple, on-message with the headline.
2. The **tilltomorrow monogram** (e.g. a refined "tt" or a single "t").
3. A minimal **node-graph / agent glyph** (three linked nodes) — says "system / automation" but is busier and less instantly legible.

Default to **(1) the forward chevron** unless Till picks otherwise. Whatever the glyph, it is rendered as a solid dark `ink-1` shape; the glass and chroma do all the decorative work.

**Anatomy (back to front):**
1. **Caustic shadow** — soft warm ellipse beneath the block, `drift-peach`/`iris-peach` at ~30%, ~60px blur. Grounds the object.
2. **Glass body** — rounded slab (radius 24–28px), `backdrop-filter: blur(24px) saturate(150%)`, fill `linear-gradient(150deg, rgba(255,255,255,0.55), rgba(255,252,247,0.25))`, 1px `glass-border`. One **specular highlight**: a bright 1–2px white streak along the top-left edge fading out (`inset 0 1px 0 rgba(255,255,255,0.9)` + a thin rotated gradient bar).
3. **Refracted glyph** — the dark `ink-1` glyph, centered, slightly scaled, with the **chromatic split** (below).
4. **Edge dispersion on the slab corner** — a short iridescent gradient (135°, the `iris-grad`) bleeding off the lower-left corner of the slab at ~50% — the "rainbow caught in the bevel."

**Chromatic split (the core effect, CSS-only, no image needed):**
Offset duplicate glows of the glyph in opposing directions with opposing temperatures:
```css
filter:
  drop-shadow( 3px  2px 0   var(--chroma-fire))    /* warm, inner, down-right */
  drop-shadow( 6px  4px 6px var(--chroma-gold))    /* warm, outer, softer    */
  drop-shadow(-3px -2px 0   var(--chroma-ice))     /* cool, inner, up-left    */
  drop-shadow(-6px -4px 6px var(--chroma-cobalt)); /* cool, outer, softer    */
```
Tune offsets to glyph size (rule of thumb: inner ≈ 1.5% of glyph height, outer ≈ 3%). The two temperatures must land on **opposite** edges — that opposition *is* the dispersion. A subtle idle animation may breathe the offsets ±1px over ~6s (respect `prefers-reduced-motion`).

**Layout slot:** Hero right column, ~400–460px wide desktop. Above the headline on tablet/mobile (per §8), scaled to ~280px. Must never out-shout the headline — it is the second read, not the first.

**Performance:** Pure CSS/SVG, no raster photo (keeps the 80KB SVG budget; chroma via `filter`, zero image weight). If a higher-fidelity raster is ever desired, budget a single WebP ≤ 60KB and keep the CSS version as the no-image fallback.

**Recurring micro-motif:** The same chromatic-split treatment may appear *once more, small* — e.g. on the wordmark prism-dot or a single section's accent glyph — to tie the system together. Never more than twice per page; it loses its specialness (same discipline as the iridescent divider).

---

## 5. Layout & Spacing

### Spacing Scale (4px base)

| Token | Value | Use |
|---|---|---|
| `xs` | 8px | Tight icon-text gaps, inline badges |
| `sm` | 16px | Inter-item gaps in lists, tag clusters |
| `md` | 24px | Intra-component padding, card grid gaps |
| `lg` | 48px | Component-to-section-head spacing |
| `xl` | 64px | Large content blocks separation |
| `section` | 96px | Between major sections (desktop) |
| `section-tablet` | 64px | Between major sections (tablet) |
| `section-mobile` | 48px | Between major sections (mobile) |
| `gutter` | 24px | Page edge padding (desktop) |
| `gutter-mobile` | 16px | Page edge padding (mobile) |

### Grid

- **12-column grid**, max content width **1280px**.
- **Column gaps:** `24px` (desktop), `16px` (mobile).
- **Common grid patterns:**
  - 3-up (sessions, logistics): `repeat(3, 1fr)` → collapses to 2-up at tablet, 1-up at mobile.
  - 2-up (pricing, testimonials, pain/solution): `repeat(2, 1fr)` → collapses to 1-up at mobile.
  - Hero: `1fr 400px` (text + visual) → single column at tablet (visual above text).

### Bilingual Layout

German runs ~20-30% longer than English. Accommodated by:
- Button min-width in `ch` units, not px.
- Card titles: two-line max before truncation.
- Form labels: positioned above inputs, never beside (prevents re-layout between languages).

---

## 6. Depth & Elevation

### Shadow System (3 Levels)

| Level | Elevation | Shadow | Use |
|---|---|---|---|
| **Level 0** | 0px | None | Content directly on canvas (body text, inline elements) |
| **Level 1** | Low | `0 8px 32px rgba(64,58,74,0.06)`, + inset `0 1px 0 rgba(255,255,255,0.6)` | Glass cards, pricing cards, testimonial cards |
| **Level 2** | Medium | `0 24px 64px rgba(124,107,255,0.2)` | Sapphire centerpiece slab (plus its own caustic shadow + chroma `filter`, see §4.11), portrait frame outer glow `0 0 40px rgba(255,201,168,0.35)` |

### Surface Hierarchy

| Surface | Background | Border | Elevation |
|---|---|---|---|
| Canvas | `canvas-1` (white) | None | Level 0 |
| Section break | `canvas-2` (warm off-white) | None | Level 0 |
| Footer | `canvas-3` (sandy) | None | Level 0 |
| Glass card | `glass-bg` + `backdrop-filter: blur(20px)` | `glass-border` 1px | Level 1 |
| Nav (scrolled) | `nav-frosted` + `backdrop-filter: blur(22px)` | `iris-violet` 14% 1px | Level 2 |
| Sapphire centerpiece | Glass slab + refracted glyph | Chromatic split (fire vs ice, §4.11) | Level 2 |

### Card Hover

- Level 1 cards: Lift 4px over 240ms, shadow deepens to `0 18px 50px rgba(64,58,74,0.11)`, border transitions to `glass-border-hover`.

---

## 7. Do's and Don'ts

### Do

- **Do** use CSS custom properties for every token — single-source all values.
- **Do** use `ch` units for button min-width to accommodate bilingual labels.
- **Do** place only ONE primary CTA per section.
- **Do** apply the iridescent gradient sparingly — prism dot, hero glass, button hovers, dividers, one accent headline.
- **Do** use `canvas-2` and `canvas-3` to create visual rhythm between sections.
- **Do** keep the background drifts visible (~58% opacity, 120px blur) — they're the page's warmth engine.
- **Do** respect the section order from build-task.md — DESIGN.md defines the visual system, not the content structure.
- **Do** test all type at `ink-1` on `canvas-1` (>14:1 contrast) and `ink-3` on `canvas-1` (>5.2:1).
- **Do** provide `canvas-1` solid fallback for all glass elements in browsers without `backdrop-filter`.

### Don't

- **Don't** use pure `#000` for text — always `ink-1` (`#1A1820`).
- **Don't** put the iridescent gradient on body text, form labels, or critical UI states. Color is never the only carrier of meaning.
- **Don't** add glass cards on `canvas-3` — they need lighter backgrounds to read.
- **Don't** use flag icons for the language switcher.
- **Don't** add full-page grit, distressed type, ripped-paper dividers, splatter, or tape effects. The handmade texture is a garnish, not a sauce.
- **Don't** animate anything faster than 240ms (hover) or bounce/pop/slide-in. Motion is slow and optical.
- **Don't** place section order or page structure in DESIGN.md — that lives in build-task.md.
- **Don't** use the iridescent divider between every section — once or twice per page max.
- **Don't** combine `canvas-3` background with `ink-2` text at small sizes — contrast can dip below AA.

### Design Hygiene

- Fonts: No weight below 300 for Fraunces, no weight above 600 for Geist, no weight other than 400 for JetBrains Mono.
- Colors: No new colors without adding to the token system first. Every hex must have a name and a role.
- Cards: Glass cards only. No flat cards, no shadow-only cards without backdrop-filter.
- Buttons: Primary = full pill. No rectangular buttons anywhere.

---

## 8. Responsive Behavior

### Breakpoints

| Name | Width | Strategy |
|---|---|---|
| Desktop | ≥ 1024px | Full grid, hero prism right-aligned, 1280px max-width |
| Tablet | 768–1023px | Single-column hero (prism above text), collapsed grids, reduced section gaps |
| Mobile | 480–767px | Hamburger nav, full-width cards, compact type |
| Small Mobile | < 480px | Tighter padding (16px gutter), smallest type scale |

### Grid Collapsing Rules

| Layout | Desktop | Tablet | Mobile |
|---|---|---|---|
| Hero | 2-col (1fr + 400px) | 1-col (visual above text) | 1-col |
| 3-up grid | 3 columns | 2 columns | 1 column |
| 2-up grid | 2 columns | 2 columns | 1 column |
| Nav | Links visible | Hamburger menu | Hamburger menu |

### Touch & Interaction

- Minimum touch target: 44px (nav links, language switcher, hamburger).
- Focus rings always visible (never `outline: none` without replacement).
- Scroll-triggered reveals via IntersectionObserver (threshold 0.1).

### Loading Budget

- Largest Contentful Paint: < 1.8s on 4G mid-tier mobile.
- Total page weight: < 600 KB (fonts subset to Latin + German extended).
- Hero prism SVG: budget 80 KB. Drifts: zero KB (CSS only).

---

## 9. Agent Prompt Guide

### Quick Reference

| Token | Value | Where |
|---|---|---|
| **Page BG** | `#FFFFFF` | canvas-1 |
| **Section BG** | `#F4EDE4` | canvas-2 |
| **Footer BG** | `#ECE2D5` | canvas-3 |
| **Headline text** | `#1A1820` | ink-1 |
| **Body text** | `#403A4A` | ink-2 |
| **Meta / Captions** | `#7A7286` | ink-3 |
| **Primary CTA** | `ink-1` bg, `canvas-1` text | button-primary |
| **CTA Hover** | Iridescent gradient sweep | See §4.1 |
| **Glass Card BG** | `rgba(255,252,247,0.55)` + `backdrop-filter: blur(20px) saturate(140%)` | glass-card |
| **Glass Card Border** | `rgba(124,107,255,0.12)` 1px solid | glass-card |
| **Hero Headline** | Fraunces 500, 6rem (desktop), 1.02 line-height, -0.02em tracking | t-hero |
| **Section Head** | Fraunces 300, 4rem, 1.1 line-height, -0.02em tracking | t-2xl |
| **Body** | Geist 400, 1.0625rem (17px), 1.55 line-height | t-base |
| **Mono Labels** | JetBrains Mono 400, 11px, 0.12em tracking, uppercase | t-mono |
| **Card Radius** | 20px | rounded-card |
| **Button Radius** | 9999px (full pill) | rounded-pill |
| **Section Gap** | 96px desktop, 64px tablet, 48px mobile | spacing-section |
| **Grid Max Width** | 1280px | — |
| **Hero Gradient** | `linear-gradient(135deg, #7C6BFF, #5B8DEF, #7FD8E0, #F7A8C9, #FFC9A8)` | iris-grad |
| **Hero Centerpiece** | Glass slab + dark glyph + chromatic split (fire vs ice) | §4.11 |
| **Chroma edge** | fire #FF4D2E / gold #FFB22E (warm) vs ice #2EC6FF / cobalt #2E6BFF (cool) | §2 Chromatic |
| **Drifts** | 3+ blobs, ~72% opacity, 140-160px blur, 50-80s drift + scroll-parallax + cursor | §2 Colors |
| **Focus Ring** | 3px `iris-blue` at 40%, offset 2px | All interactive |
| **Fonts** | Fraunces (Google Fonts), Geist Sans (Google Fonts), JetBrains Mono (Google Fonts) | — |

### Icon System

- **Phosphor Icons** (Duotone weight), 20px nav, 16px body.
- Color: `ink-2`. Never iridescent-treated (reserved for prism family).

### Texture Doses (exactly 2)

1. **Webgeil callout box** — paper texture at 8% opacity, iridescent top border, hand-drawn arrow ornament.
2. **Footer stamp** — "MADE IN BERLIN · 2026" in JetBrains Mono, slightly misregistered (~ -0.7°), iridescent ink-bleed at 6%.

### Prompt Template for AI Agents

```
Build a single-file HTML landing page using the DESIGN.md above.

Design system tokens (CSS custom properties):
- Canvas: var(--canvas-1)=#FFFFFF, var(--canvas-2)=#F4EDE4, var(--canvas-3)=#ECE2D5
- Ink: var(--ink-1)=#1A1820, var(--ink-2)=#403A4A, var(--ink-3)=#7A7286
- Iris: var(--iris-violet)=#7C6BFF, var(--iris-blue)=#5B8DEF, var(--iris-cyan)=#7FD8E0, var(--iris-pink)=#F7A8C9, var(--iris-peach)=#FFC9A8
- Iridescent gradient: linear-gradient(135deg, #7C6BFF, #5B8DEF, #7FD8E0, #F7A8C9, #FFC9A8)
- Chroma edge: fire #FF4D2E, gold #FFB22E (warm) / ice #2EC6FF, cobalt #2E6BFF (cool) — edge glow only
- Fonts: Fraunces (display), Geist Sans (body), JetBrains Mono (meta)
- Glass: rgba(255,252,247,0.55) bg + backdrop-filter blur(20px) saturate(140%) + 1px solid rgba(124,107,255,0.12)

Hero centerpiece: glass slab + dark glyph (forward chevron unless told otherwise) + chromatic split via opposing fire/ice drop-shadows. Pure CSS, no raster. See §4.11.

Components: primary button (pill, ink-1 bg, iris sweep hover), secondary button (transparent, ink-3 border), glass cards (frosted + hover lift 4px), form fields (8px radius, iris-blue focus ring), tag pills (ink-3 border, drift-peach hover), iridescent dividers (gradient at 40%, use sparingly), sticky nav (frosted glass on scroll).

Background: 3+ drift blobs at ~72% opacity, 140-160px blur, multiply blend, CSS @keyframes drift + scroll-parallax (0.15-0.35x) + optional cursor lerp. 2% grain overlay over entire page.

Accessibility: ink-1 on canvas-1 >14:1. Focus rings always visible. Semantic HTML. prefers-reduced-motion support. Solid canvas-1 fallback for all glass elements.

Section order and copy from build-task.md. Do not add sections or reorder.
```

---

## 10. Open Design Questions (Opus → Till)

Decisions I made a default call on, where your input would sharpen the result:

1. **The hero glyph (needs your call).** I specced the chromatic-glass *treatment* precisely, but the glyph *inside* the glass is a brand decision. My default is a **forward / play chevron** (▸ = "activate, make it work, tomorrow"). Alternatives: tilltomorrow monogram, or a node-graph "agent" glyph. → *Which symbol should live in the glass?*
2. **Drift presence vs. text legibility.** I raised drifts to ~72% opacity + multiply blend so they read as foreground (per "nicht sichtbar genug"). On pure white this is safe, but watch hero headline contrast where a blob passes behind `ink-1` text — if it ever dips, the fix is to keep blobs out of the headline's bounding box, not to lower global opacity.
3. **Cursor interaction scope.** Specced as low-priority cherry-on-top (pointer-fine only, skipped on touch + reduced-motion). Safe to ship v1 *without* it and add later — flagging so it's not treated as blocking.
4. **Sapphire as recurring motif — how far?** I limited the chromatic-split to max twice per page (hero + one micro-accent). If you want the optic "more present," the safer lever is making the *single hero instance bigger and more confident*, not repeating it more often. → *Bigger hero, or one extra small instance?*

These are non-blocking — Sonnet can build against the defaults. Answer any you have an opinion on and I'll fold it in.

---

*v12 — Sapphire centerpiece + Marimba foreground drifts. Hero visual gap closed; glyph choice pending (§10). Ready for build.*
