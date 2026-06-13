# Workshop Landing Page Build v12 — Sonnet Task

## Source
- **DESIGN.md v11:** `/opt/vault/Projects/workshop-landing/DESIGN.md`
- **Working copy:** `/opt/data/tasks/design-result.md`

## Target
- `/opt/data/websites/workshop-landing/index.html` (overwrite)
- Vault mirror: `/opt/vault/Projects/workshop-landing/index.html`

**Use Sonnet** (`--model sonnet`). This is implementation — HTML/CSS, not design reasoning.

---

## What to fix

### 🔴 1. Pricing: Remove "14-day money-back guarantee"
Appears twice — under Early Bird AND under Regular. Remove completely.

### 🔴 2. About Me: Add Impact Message
Current bio is too dry. Append at end of bio:
> "I want to help people focus on work that actually matters. Work that has impact. Together we can change the world — a little dramatic, but I mean it."

### 🟠 3. Hero Visual: Implement DESIGN.md §4.1 EXACTLY
Currently a Play-Button icon. Wrong.

DESIGN.md §4.1 specifies:
- Layered SVG with `backdrop-filter` (NO PNG/WebP fallback this time)
- Irregular faceted polygon, ~5 visible faces, tilted ~15° off vertical
- Chromatic aberration: `iris-violet` left edge, `iris-peach` right edge, 1px each
- Specular highlight (white, ~60% opacity, soft-edged) crossing one face
- Prism acts as lens: `backdrop-filter: blur(40px) saturate(160%)` over the drift blobs — capturing their live color
- See DESIGN.md §4.1 for full specification

### 🟠 4. Callout Box: Implement Webgeil Styling from DESIGN.md
In Section 01 below the Pain/Solution cards: The callout block
> "While you're figuring out how to 'use AI better,' others are automating their inboxes, their scheduling, their research..."

must be styled as Webgeil accent box:
- Paper texture (SVG noise, ~8% opacity)
- Iridescent top border
- Hand-drawn arrow ornament (↳, rotated 8°)
- See DESIGN.md §5.2 Point 1

### 🟡 5. Drifts: Set Opacity to 58%
Currently at 72%. DESIGN.md v11 §2 specifies ~58% opacity.

### 🟡 6. Grain Overlay: Add `body::after`
DESIGN.md §5.1 — 1px SVG noise overlay at 2% opacity, multiplied, fixed position, z-index 9999.

### 🟡 7. Testimonials + Pricing Cards: Implement Glass-Card Hover States
DESIGN.md §4.2 / §9.3 specifies:
- Hover: lift 4px over 240ms
- Border transitions to `glass-border-hover` (rgba(124,107,255,0.26))
- Shadow deepens to `0 18px 50px rgba(64,58,74,0.11)`

---

## Rule

**No creative deviations.** DESIGN.md v11 is the single source of truth. Every token, spacing value, and component rule is defined there. All tokens are available as CSS custom properties in the existing file.

Section order and copy remain as-is on the live page — do not change them.
