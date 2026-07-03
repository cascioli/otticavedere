---
name: Ottica Vedere
description: Golden-hour optician landing page — 35 years of trust in Foggia, told in navy and gold.
colors:
  gold: "#C4975A"
  gold-hi: "#DDB070"
  gold-dim: "#C4975A26"
  deep: "#05090F"
  navy: "#09101F"
  navy-mid: "#101926"
  navy-lit: "#1A2B4A"
  white: "#FAFAF8"
  muted: "#FAFAF885"
  text: "#0A1020"
  text-mid: "#0A10209E"
typography:
  display:
    fontFamily: "Cormorant Garamond, Georgia, serif"
    fontSize: "clamp(4.25rem, 11vw, 10.5rem)"
    fontWeight: 500
    lineHeight: 0.88
    letterSpacing: "-0.025em"
  headline:
    fontFamily: "Cormorant Garamond, Georgia, serif"
    fontSize: "clamp(2rem, 3.8vw, 3.5rem)"
    fontWeight: 500
    lineHeight: 1.14
    letterSpacing: "normal"
  title:
    fontFamily: "Cormorant Garamond, Georgia, serif"
    fontSize: "clamp(1.75rem, 2.6vw, 2.625rem)"
    fontWeight: 500
    lineHeight: 1.1
    letterSpacing: "normal"
  body:
    fontFamily: "DM Sans, system-ui, sans-serif"
    fontSize: "0.9375rem"
    fontWeight: 300
    lineHeight: 1.8
    letterSpacing: "normal"
  label:
    fontFamily: "DM Sans, system-ui, sans-serif"
    fontSize: "0.75rem"
    fontWeight: 400
    lineHeight: 1
    letterSpacing: "0.16em"
rounded:
  none: "0px"
spacing:
  xs: "0.5rem"
  sm: "1rem"
  md: "1.875rem"
  lg: "3rem"
  xl: "6rem"
  section: "clamp(5rem, 10vw, 10rem)"
components:
  button-primary:
    backgroundColor: "{colors.gold}"
    textColor: "{colors.deep}"
    rounded: "{rounded.none}"
    padding: "1rem 2.25rem"
    typography: "{typography.label}"
  button-primary-hover:
    backgroundColor: "{colors.gold-hi}"
    textColor: "{colors.deep}"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.white}"
    rounded: "{rounded.none}"
    padding: "1rem 2.25rem"
    typography: "{typography.label}"
  button-dark:
    backgroundColor: "transparent"
    textColor: "{colors.text}"
    rounded: "{rounded.none}"
    padding: "0.9375rem 1.875rem"
    typography: "{typography.label}"
  button-dark-hover:
    backgroundColor: "{colors.text}"
    textColor: "{colors.white}"
---

# Design System: Ottica Vedere

## 1. Overview

**Creative North Star: "The Golden Hour Optician"**

The page reads like late-afternoon light through a shop window that's held the same family name for 35 years: near-black navy as the room in shadow, warm gold as the one shaft of light picking out the frames worth noticing. Every section is a deeper or lighter shade of that same navy — the palette never leaves its own family — with gold used sparingly enough that it stays precious. Serif italics (Cormorant Garamond) carry the human, spoken parts — quotes, reviews, the name "Giuliano" — while DM Sans carries the functional parts: labels, hours, phone numbers. That contrast is the whole personality: warm heritage story told through cold, precise structure.

This explicitly rejects the generic optical-chain look — no clinical white-and-blue, no stock-photo confidence, no rounded "friendly SaaS" softness. Nothing here should look like a website builder produced it. The luxury is quiet: hairline borders, small caps, one accent color, never a gradient, never a card shadow doing the trust-building for you.

**Key Characteristics:**
- Near-black navy stacked in four tones, never leaving its own hue family
- One gold accent, used on ≤10% of any surface — text, hairlines, one button
- Serif italic for anything spoken or quoted; uppercase tracked sans for anything functional
- Zero border-radius anywhere — every edge is a sharp, deliberate line
- Flat by default; shadows are earned, not decorative (see Elevation)

## 2. Colors

Four stacked navy-blacks for depth, one warm gold for everything that should catch the eye, off-white and near-black for text on either side.

### Primary
- **Late-Afternoon Gold** (`#C4975A`): the single accent — CTA button fill, headline emphasis (`<em>`), link hover, icon color, hairline borders at low opacity. Never used for large fills.
- **Gold, Lit** (`#DDB070`): hover state for the gold button only. Not a separate decorative color — it exists solely to answer "what does gold do when you touch it."

### Neutral
- **Deepest Navy** (`#05090F`): the darkest surface — hero, services section, footer. The "room in shadow."
- **Navy** (`#09101F`): reviews section — one step lighter than deepest, used for large text-heavy dark sections that need to breathe slightly more.
- **Navy, Mid** (`#101926`): marquee strip and stats band — the shallowest dark surface, used for compact horizontal bands.
- **Navy, Lit** (`#1A2B4A`) — *reserved, not yet in markup*. The natural next step up in the tonal stack; candidate for elevated card/modal surfaces if the Elevation doctrine below is exercised.
- **Paper White** (`#FAFAF8`): all text and headlines set against navy.
- **Paper, Muted** (`#FAFAF885`, i.e. `rgba(250,250,248,0.52)`): secondary text on dark — hero subhead, nav links at rest.
- **Ink** (`#0A1020`): body text and headlines on light sections (About, Contact).
- **Ink, Mid** (`#0A10209E`, i.e. `rgba(10,16,32,0.62)`): secondary text on light — About body copy, hours values.

### Named Rules
**The One Flame Rule.** Gold never fills a surface larger than a button. It marks — a border, a word, a digit, an icon — it never floods. The moment gold becomes a background, the "one shaft of light" metaphor breaks.

**The Same-Hue Rule.** Every dark surface (`deep`, `navy`, `navy-mid`, `navy-lit`) shares one hue family, differing only in lightness. Never introduce a second dark hue (no cool gray, no black-blue-purple mix) to distinguish sections — use lightness steps only.

## 3. Typography

**Display Font:** Cormorant Garamond (with Georgia, serif fallback)
**Body Font:** DM Sans (with system-ui, sans-serif fallback)

**Character:** A classic editorial pairing built on contrast, not similarity — a warm, humanist serif for anything the shop owner would say out loud, set against a cool, geometric sans for anything the shop owner would print on a sign. The serif is always either large-display or italic-quote; it never does small print. The sans never goes above headline size.

### Hierarchy
- **Display** (500, `clamp(4.25rem, 11vw, 10.5rem)`, line-height 0.88, letter-spacing -0.025em): the hero H1 only — "Vedere / bene." One use per page.
- **Headline** (500, `clamp(2rem, 3.8vw, 3.5rem)`, line-height 1.14): section headings (Services, Reviews) and the About heading.
- **Title** (500, `clamp(1.75rem, 2.6vw, 2.625rem)`, line-height 1.1): service row names, contact column titles — mid-weight anchors inside a section.
- **Body** (300, `0.9375rem`, line-height 1.8, max ~65ch): About paragraphs, service descriptions, hero subhead. Light weight throughout — this system has no regular-weight body text, only light.
- **Label** (400, `0.75rem`, letter-spacing `0.16em`, uppercase): nav links, section eyebrows (`.lbl`), stat labels, marquee items, service tags. The uppercase-tracked treatment is the system's only "small text" register — there is no untracked small text anywhere.

### Named Rules
**The Whisper-or-Shout Rule.** Type is either large and serif (display/headline/title) or small, tracked, and uppercase (label). There is no mid-size, mid-weight, sentence-case default paragraph style beyond `body` — nothing in this system reads as "generic 16px paragraph text."

## 4. Elevation

Flat by default today — the shipped page has zero `box-shadow` anywhere; every visual boundary is a 1px hairline border at low gold opacity (`rgba(196,151,90,0.1–0.28)`) or a shift in navy lightness. The doctrine going forward allows subtle shadows to be introduced for genuinely elevated UI (a future modal, a floating card, a dropdown) — but they must stay ambient and rare, never the default way two sections are separated.

### Shadow Vocabulary (reserved for future use)
- **ambient-low** (`box-shadow: 0 4px 24px rgba(5,9,15,0.35)`): a soft navy-black glow for anything that floats above the page (modal, popover, dropdown). Not yet used in the shipped page.

### Named Rules
**The Hairline-First Rule.** Before reaching for a shadow, ask whether a 1px `gold-dim` border or a one-step navy tonal shift already does the job. On this page, it always has. Shadows are for things that genuinely float (modals, dropdowns) — not for cards, sections, or buttons at rest.

## 5. Components

### Buttons
- **Shape:** perfectly square corners everywhere (`border-radius: 0`) — see the Sharp Corner rule below.
- **Primary** (`button-primary`): solid gold fill (`#C4975A`), deep-navy text (`#05090F`), `1rem 2.25rem` padding, uppercase label typography. The only solid-fill button in the system — reserved for the single highest-priority action per screen (the phone call).
- **Hover/Focus:** background lightens to `#DDB070` (Gold, Lit); no scale, no shadow, no motion beyond the color shift (`transition: background 0.22s`).
- **Ghost** (`button-ghost`): transparent fill, off-white text at 68% opacity, 1px border at 20% white opacity. Used for the secondary action beside a primary button (e.g. "Scopri i servizi" beside "Chiamaci").
- **Dark** (`button-dark`): transparent fill, ink text, 1px border at 25% ink opacity; inverts to solid ink fill with white text on hover. Used on light sections (Contact → "Apri in Google Maps").

### Navigation
- Fixed top bar, transparent over the hero, snapping to solid `deep` navy with a gold hairline bottom border once scrolled (`.is-scrolled`). Links are uppercase label-style at 60% white opacity, brightening to gold on hover. The phone number is always visually distinct — bordered gold pill on desktop, plain gold text on mobile — because it is the one link that matters more than the others.

### Stat Band
- Three-column flat grid on `navy-mid`, separated by 1px gold hairlines (never a card, never a shadow). Big serif gold numerals over small tracked labels — the numbers do the persuading, not decoration around them.

### Service Rows
- A borderless list (`border-top` once, `border-bottom` per row) rather than a card grid — deliberately avoids the "identical card grid" pattern. Row name in serif title type slides 10px right and turns gold on hover; the tag is a small bordered label, not a badge with a fill color.

### Quote / Review Block
- Italic serif Cormorant Garamond at title-to-headline size, gold curly quote marks via CSS `content`. No card, no background tint, no avatar — the quote itself is the entire visual weight.

### Contact / Hours
- Hours render as a borderless table with hairline row dividers; closed days shown in italic at reduced opacity rather than a colored "closed" badge. Contact rows pair a gold-stroked inline SVG icon with ink text — icons are never filled, always stroke-only at `1.5` weight.

## 6. Do's and Don'ts

### Do:
- **Do** keep every dark surface within the same navy hue family (`deep` → `navy` → `navy-mid` → `navy-lit`), differing only in lightness.
- **Do** reserve solid gold fill for exactly one button per screen — the highest-priority action.
- **Do** pair serif italic (quotes, reviews, emphasis) against uppercase tracked sans (labels, nav, tags) as the system's only two typographic registers.
- **Do** use 1px gold hairline borders (`rgba(196,151,90,0.1–0.28)`) as the default way to separate content — before reaching for a shadow or a card.
- **Do** keep every corner sharp — `border-radius: 0` on every element, permanently, per the Sharp Corner Rule.
- **Do** respect `prefers-reduced-motion`: disable the blur-in hero reveal, the "35" ghost drift, and the marquee scroll for users who ask for less motion.

### Don't:
- **Don't** introduce a second accent color. Gold is the only accent; anything that needs emphasis gets gold or gets serif italic, not a new hue.
- **Don't** use card grids with icon-heading-text repeated identically — the Services section deliberately uses a list, not cards, to avoid this.
- **Don't** round any corner, anywhere — no `border-radius` on buttons, borders, tags, or future components. Sharp corners are load-bearing to the "boutique, not app" feel.
- **Don't** use gradient text, glassmorphism, or side-stripe colored borders (`border-left` accents) — none of these appear in the system and none should be introduced.
- **Don't** let the page read as a generic website-builder template — every section should carry a specific, named detail (the owner's name, the real address, a real review) rather than generic stock copy.
- **Don't** default to a shadow for depth. Try a hairline border or a navy tonal shift first; shadows are reserved for things that actually float above the page.
