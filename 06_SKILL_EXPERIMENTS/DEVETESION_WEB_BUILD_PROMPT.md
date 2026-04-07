# DEVETESION — MASTER WEB BUILD PROMPT

**Use this document as the single source of truth for all design and development work on the DEVETESION website.**

Every designer, developer, and AI agent must read and enforce this document before touching any code or pixel.

---

## PART 0: BRAND DNA — NON-NEGOTIABLES

### Identity

**Brand:** DEVETESION (stylized: DEVETƎSION — third E mirrored)
**Positioning:** Dark luxury fashion house. Season-based collections. Monolithic brutalism.
**Audience:** Creative class, 18-35, fashion-forward, designers, architects, photographers
**Attitude:** Rebellious, uncompromising, editorial. Does not ask for permission. Does not try to be liked.

### 5 DOs
1. Use short, declarative sentences — make statements, not suggestions
2. Let silence work — fewer words = more weight per word
3. Use construction/architecture verbs: built, forged, cast, carved, imposed
4. Create tension — beauty through brutality, luxury through rawness
5. Address audience as insiders — they already understand, no explaining

### 5 DON'Ts
1. NO fashion clichés: "stunning," "gorgeous," "elegant," "chic," "must-have"
2. NO exclamation marks — ever
3. NO rhetorical questions — DEVETESION doesn't ask, it tells
4. NO hedging language — never "we believe," "we think," "we hope"
5. NO warm/friendly language — cold is luxurious, warmth is cheap

### Word List

| USE | NEVER USE |
|-----|-----------|
| Built, forged, cast, carved | Beautiful, gorgeous, stunning |
| Collection, drop, season, archive | Must-have, essential, iconic |
| Architecture, structure, mass, weight | Chic, trendy, stylish, fashionable |
| Command, demand, impose | We hope, we think, we believe |
| Raw, unfiltered, direct | Amazing, incredible, spectacular |
| Silence, shadow, concrete, water | Love, obsessed, incredible |

---

## PART 0.5: REQUIRED SKILLS — USE IN THIS ORDER

Every task must use the correct skill for its phase. Do not skip phases. Do not use image/video/voice generation skills.

### PHASE 1: Design — Structure & Visual System

**Order of execution:**

```
1. ui-ux-designer        → Wireframes, layout architecture, UX flows
2. product-design        → Visual system, design tokens, UI engineering, accessibility
3. ui-ux-pro-max         → Audit against 168 research-backed UX principles
```

**How to use:**

```
skill: ui-ux-designer

Build the wireframes and UX architecture for the DEVETESION website.

MANDATORY: Read and enforce the entire DEVETESION_WEB_BUILD_PROMPT.md before designing.
This is not a generic e-commerce site. Every rule in this document applies.

PAGES: /, /collection, /look-detail, /archive, /membership

Deliver: Wireframes (low-fi) → layout structure → user flow map
```

```
skill: product-design

Build the complete visual system for DEVETESION.

MANDATORY: Read and enforce the entire DEVETESION_WEB_BUILD_PROMPT.md before designing.
Use the color tokens, typography scale, and spacing system from Part 1 of this document.

Deliver: High-fidelity designs for all 5 pages + design tokens + component specs
```

```
skill: ui-ux-pro-max

Audit the DEVETESION website designs against 168 UX principles.

Deliver: Scored audit report with violations flagged and fix recommendations
```

---

### PHASE 2: Development — Code

**Order of execution:**

```
4. react-nextjs-development  → Next.js 14 App Router, Server Components, all pages
5. tailwind-design-system    → Design tokens, component variants, responsive patterns
```

**How to use:**

```
skill: react-nextjs-development

Build the DEVETESION website in Next.js 14 App Router.

MANDATORY: Read and enforce the entire DEVETESION_WEB_BUILD_PROMPT.md before coding.
Tech stack: Next.js 14 (App Router, Server Components), TypeScript strict, Tailwind CSS v4

PAGES TO BUILD:
- / — Homepage (one image, one word, one link)
- /collection — Season lookbook grid
- /collection/[look] — Individual look detail
- /archive — Past seasons (viewable, not purchasable)
- /membership — Exclusive access program

Deliver: Complete, functional pages with server components, responsive layout, dark-only mode
```

```
skill: tailwind-design-system

Build the design system in Tailwind CSS v4 for DEVETESION.

MANDATORY: Read and enforce the entire DEVETESION_WEB_BUILD_PROMPT.md before coding.
Use the exact color tokens, typography, spacing, radius, and motion from Part 1.

Deliver:
- globals.css with all CSS custom properties
- tailwind.config with theme tokens
- Reusable component variants (button primary/secondary/ghost, nav, footer, image treatment)
```

---

### PHASE 3: Polish — Animation, Refinement, Accessibility

**Order of execution:**

```
6. animate            → Scroll reveals, hover states, page transitions, loading states
7. polish             → Final quality pass — alignment, spacing, consistency, edge cases
8. fixing-accessibility → Audit and fix all a11y issues (focus, contrast, keyboard nav)
```

**How to use:**

```
skill: animate

Add purposeful motion to the DEVETESION website.

MANDATORY: Read and enforce the entire DEVETESION_WEB_BUILD_PROMPT.md.
Specifically: Part 3 (Interaction Design) — NO bouncy animations, opacity-only hovers, max 300ms.

Add:
- Scroll-driven reveals (elements fade in as user scrolls — heavy, deliberate)
- Hover states on collection items (opacity shift only)
- Page transitions (fast fade to dark, 200ms)
- Loading states (dark skeleton screens, never spinners)

Deliver: Framer Motion implementations for all interactive states
```

```
skill: polish

Final quality pass on the DEVETESION website.

MANDATORY: Run the entire Part 9 (Enforcement Checklist) from DEVETESION_WEB_BUILD_PROMPT.md.

Fix:
- Alignment issues
- Spacing inconsistencies
- Copy that violates brand DNA
- Edge cases (empty states, error states, sold-out pieces)
- Mobile-specific issues (touch targets, safe areas)

Deliver: Clean, production-ready code with all checklist items passing
```

```
skill: fixing-accessibility

Audit and fix all accessibility issues on the DEVETESION website.

MANDATORY: Follow Part 7 (Accessibility) from DEVETESION_WEB_BUILD_PROMPT.md.

Fix:
- Focus ring visibility and styling
- Keyboard navigation (Tab, Enter, Escape)
- Aria labels on icon buttons
- Alt text on images
- Color contrast (WCAG AA minimum)
- prefers-reduced-motion support

Deliver: All items from accessibility checklist passing
```

---

### PHASE 4: Content — Copy & Strategy (Optional, Run Before or After Build)

```
brand-guidelines     → Audit all copy for brand voice compliance
content-creator      → Generate page-specific copy that matches brand DNA
ad-creative          → Generate ad copy for paid campaigns (if launching)
```

**How to use:**

```
skill: brand-guidelines

Audit all copy on the DEVETESION website for brand voice compliance.

MANDATORY: Read Part 0 (Brand DNA) from DEVETESION_WEB_BUILD_PROMPT.md.
Check: No banned words, no exclamation marks, no rhetorical questions, no hedging.

Deliver: Audit report with every non-compliant copy flagged + corrected alternatives
```

```
skill: content-creator

Generate platform-specific content for DEVETESION launch.

MANDATORY: Read Part 0 (Brand DNA) from DEVETESION_WEB_BUILD_PROMPT.md.

Deliver:
- Instagram captions for collection posts
- Landing page hero copy
- Email newsletter for collection drop
All in DEVETESION brand voice: cold, declarative, no clichés
```

---

### SKILL SUMMARY — FULL ORDER

```
Phase 1 (Design):
  1 → ui-ux-designer
  2 → product-design
  3 → ui-ux-pro-max

Phase 2 (Development):
  4 → react-nextjs-development
  5 → tailwind-design-system

Phase 3 (Polish):
  6 → animate
  7 → polish
  8 → fixing-accessibility

Phase 4 (Content — optional):
  9 → brand-guidelines
  10 → content-creator
  11 → ad-creative
```

**SKILLS TO NEVER USE:** Any image generation, video generation, or voice generation skills. This is a web build — text and code only.

---

## PART 1: VISUAL DESIGN SYSTEM

### Color Tokens

```css
:root {
  /* Primary */
  --color-background: #0a0a0a;
  --color-surface: #121214;
  --color-surface-raised: #1a1a1e;
  --color-border: #2a2a2e;

  /* Neutrals */
  --color-bone: #e8e4df;
  --color-ash: #8a8a8e;
  --color-ghost: #5a5a5e;
  --color-void: #050507;

  /* Accent — use sparingly, max 5% of any screen */
  --color-accent: #c0c0c0;

  /* Semantic */
  --color-text: #f0f0f0;
  --color-text-muted: #6a6a6e;
  --color-text-disabled: #3a3a3e;
}
```

**Rules:**
- Background is always near-black (#0a0a0a to #121214)
- NO warm tones, NO golden hour colors, NO gradients toward warmth
- Flash photography aesthetic — harsh direct light, deep shadows
- Accent color appears only where the eye has been led by form alone
- NO gradient backgrounds. Ever.

### Typography

```css
:root {
  /* Font Families */
  --font-display: 'Helvetica Neue', Arial, sans-serif;
  --font-body: 'Helvetica Neue', Arial, sans-serif;
  --font-mono: 'SF Mono', 'Menlo', monospace;

  /* Scale — max 3 sizes per screen */
  --text-4xl: 48px;    /* H1 — one per page */
  --text-3xl: 36px;    /* H2 — section headers */
  --text-xl: 24px;     /* H3 — sub-sections */
  --text-lg: 18px;     /* Body — rare use */
  --text-base: 14px;   /* Body — default */
  --text-sm: 12px;     /* Captions, labels */
  --text-xs: 10px;     /* Reference marks */

  /* Tracking — always wide */
  --tracking-widest: 0.2em;
  --tracking-wider: 0.1em;
  --tracking-wide: 0.05em;

  /* Line heights */
  --leading-tight: 1.1;
  --leading-normal: 1.5;
  --leading-relaxed: 1.7;
}
```

**Rules:**
- Thin fonts only — font-weight: 300 (light) or 400 (regular)
- Text as architectural marks — not paragraphs
- Headings: tracking-widest, uppercase
- Body: tracking-wide, sentence case
- No decorative fonts — restrained, architectural
- Max 3 font sizes on any single screen

### Spacing System

```css
:root {
  --space-1: 4px;
  --space-2: 8px;
  --space-3: 12px;
  --space-4: 16px;
  --space-6: 24px;
  --space-8: 32px;
  --space-10: 40px;
  --space-12: 48px;
  --space-16: 64px;
  --space-20: 80px;
  --space-24: 96px;
  --space-32: 128px;
}
```

**Rules:**
- Massive negative space as luxury signal
- Breathing room: content never touches edges (min 24px mobile, 48px desktop)
- Grouping: related elements close, groups far apart
- Everything is multiple of 4px

### Border Radius

```css
:root {
  --radius-none: 0px;
  --radius-sm: 2px;
  --radius-md: 4px;
}
```

**Rules:**
- NO rounded corners beyond 4px
- Sharp edges by default
- Max radius 4px for interactive elements only
- No pill-shaped buttons, no rounded cards

### Shadows

```css
:root {
  --shadow-none: none;
  --shadow-subtle: 0 1px 3px rgba(0, 0, 0, 0.4);
}
```

**Rules:**
- NO shadows as depth indicator
- Flat, heavy, grounded aesthetic
- If shadow used, it's barely perceptible

### Motion

```css
:root {
  --duration-fast: 100ms;
  --duration-normal: 200ms;
  --duration-slow: 300ms;
  --ease-in: cubic-bezier(0.4, 0, 1, 1);
  --ease-out: cubic-bezier(0, 0, 0.2, 1);
}
```

**Rules:**
- NO bouncy spring animations
- Ease-in for exits (fast), ease-out for entries
- Max duration: 300ms — anything longer feels sluggish
- Hover states: opacity shift only, no transforms
- Scroll reveals: fade-in from bottom, subtle, heavy

---

## PART 2: SPATIAL DESIGN PRINCIPLES

### Core Philosophy: "Monolithic Silence"

1. **Mass over detail** — enormous forms occupy space with quiet authority
2. **Corridors of light** — narrow gaps between massive forms create tension
3. **Implied information** — what's not shown matters more than what is
4. **Scale as language** — gravitational pull, not directional arrows
5. **Simplicity as achievement** — appears effortless, is actually meticulous

### Composition Rules

- Massive dark form in upper third → thin light line → small mark in lower right
- Elements do NOT sit next to each other — they occupy relationships of tension and distance
- No card-based layouts (no "cards with drop shadows")
- No grid of equal boxes (no "feature cards")
- No centered paragraph blocks
- Asymmetric compositions feel heavier, more authoritative

### What The Eye Sees (In Order)

1. **Mass** — the biggest dark thing on screen
2. **Light** — the brightest spot draws second attention
3. **Mark** — the smallest, most placed element anchors
4. **Text** — discovered, not read

---

## PART 3: INTERACTION DESIGN

### Hover States

```css
/* CORRECT */
.button:hover { opacity: 0.8; }
.link:hover { text-decoration: underline; text-underline-offset: 4px; }
.card:hover { opacity: 0.9; }

/* WRONG — NEVER */
.button:hover { transform: scale(1.05); }
.card:hover { transform: translateY(-4px); box-shadow: ... }
```

### Loading States

```
CORRECT: Dark skeleton screens that match final layout shape
WRONG: Spinners, loading text, progress bars, shimmer effects
```

### Error States

```
CORRECT: "Something went wrong. Try again." (specific, actionable)
WRONG: "Error 404 — Oops! Something went wrong 😅"
```

### Page Transitions

```
CORRECT: Fast fade to dark (200ms), then new page fades in
WRONG: Slide transitions, zoom transitions, parallax page changes
```

### Scroll Behavior

```
CORRECT: Elements reveal as user scrolls — heavy, deliberate
WRONG: Parallax scrolling, scroll-jacking, horizontal scroll sections
```

### Button States

```css
.button {
  background: var(--color-bone);
  color: var(--color-background);
  padding: var(--space-3) var(--space-6);
  font-size: var(--text-sm);
  font-weight: 400;
  letter-spacing: var(--tracking-widest);
  text-transform: uppercase;
  border: none;
  border-radius: var(--radius-sm);
  cursor: pointer;
  transition: opacity var(--duration-normal) var(--ease-out);
}
.button:hover { opacity: 0.8; }
.button:active { opacity: 0.6; }
.button:disabled { opacity: 0.3; cursor: not-allowed; }
```

---

## PART 4: ANTI-PATTERNS — NEVER BUILD THESE

The following patterns are **banned** from the DEVETESION website. If you see one, remove it.

| Pattern | Why It's Banned | Replace With |
|---------|-----------------|--------------|
| Hero section with smiling people | Generic, warm, welcoming | Single image, single word, single link |
| Testimonial carousel | Social proof = insecurity | Silence. Let the work speak. |
| "About Us" origin story | Nobody cares when you started | Archive page: seasons as closed doors |
| Newsletter signup popup | Desperate for attention | "Join The Grid" — minimal, no popup |
| Social proof badges | "Trusted by 10,000+" = cheap | Zero badges. Authority needs no proof. |
| Rounded cards with shadows | Every SaaS ever | Flat surfaces, hard edges, raw |
| Gradient backgrounds | Warmth = cheap | Near-black. Always. |
| Stock photography | Fake, lifeless | Real campaign photography only |
| "Learn More" buttons | Weak, non-committal | "Shop [Season]" / "Enter" / "View" |
| Hamburger menu on desktop | Lazy responsive pattern | Horizontal nav, 4 items max |
| Breadcrumb navigation | Clutters the void | Simple back links only |
| Search bar in header | E-commerce pattern | Search lives on collection page only |
| Footer with 4 columns | Information dump | 3 lines max. Brand. Season. Link. |
| Cookie consent banner (custom) | Legal, but make it minimal | System-level, dark, non-intrusive |
| Chat widget | "Need help?" = not confident | No chat. Figure it out. |
| Back-to-top button | Clutters the void | Scroll is the only scroll. |

---

## PART 5: PAGE SPECIFICATIONS

### Page 1: HOMEPAGE `/`

**Purpose:** Command attention. One image. One word. One link.

**Layout:**
```
┌─────────────────────────────────────┐
│                                     │
│         [Full-bleed image]          │
│         Current season visual        │
│         occupies 70% of screen       │
│                                     │
│                                     │
│         [SEASON IDENTIFIER]         │
│                                     │
│         [ Shop Collection ]         │
│                                     │
│                                     │
│       DEVETESION · The Grid         │
└─────────────────────────────────────┘
```

**Content:**
- One hero image (current season campaign)
- One identifier: current season code (e.g., "S12.", "FW16.", etc.)
- One CTA button: "Shop [Season]"
- Bottom: minimal footer — "DEVETESION" + link to "The Grid"

**No:** Navigation bar, logo animation, scrolling text, multiple CTAs, taglines

**Copy:**
```
[S12.]

[ Shop S12 ]

DEVETESION · The Grid
```

---

### Page 2: COLLECTION `/[season]`

**Purpose:** Display all looks for a season. Dark grid. No fluff.

**Layout:**
```
┌─────────────────────────────────────┐
│ [SEASON] · [COLLECTION TITLE]       │
│ [X] looks · No restocks             │
├─────────────────────────────────────┤
│                                     │
│  [Look 01]  [Look 02]  [Look 03]   │
│  [Look 04]  [Look 05]  [Look 06]   │
│  [Look 07]  [Look 08]  [Look 09]   │
│  [Look 10]  [Look 11]  [Look 12]   │
│  ...continue                        │
│                                     │
├─────────────────────────────────────┤
│ DEVETESION · Archive · The Grid     │
└─────────────────────────────────────┘
```

**Grid Rules:**
- 3 columns desktop, 2 tablet, 1 mobile
- No gap between images (or 2px max)
- No image titles on grid — only numbers: "01", "02", "03"
- No hover overlays — hover = opacity 0.9
- Images are full-bleed within their cell

**Header:**
```
[S12] · [MOTORSPORT COUTURE]
[30] looks · No restocks
```

**Copy rules:**
- No product descriptions on grid
- No prices visible until hover (or click through)
- "Sold Out" badge on unavailable pieces (small, top-right, grey text on dark bg)

---

### Page 3: LOOK DETAIL `/[season]/[look-number]`

**Purpose:** One look. Full bleed. Details as architectural marks.

**Layout:**
```
┌─────────────────────────────────────┐
│                                     │
│      [Full-bleed look image]        │
│      occupies entire viewport       │
│                                     │
└─────────────────────────────────────┘
┌─────────────────────────────────────┐
│ Look [01]                           │
│ [Piece Name] — [Color/Material]     │
│ [Detail line 1]. [Detail line 2].  │
│ [Detail line 3].                    │
│                                     │
│ [ Add to Grid — Early Access ]      │
│ [ or: Sold Out ]                    │
│                                     │
│ ← [prev]  |  [01]/[30]  |  [next] →│
└─────────────────────────────────────┘
```

**Content:**
- Full-bleed image (no crop, no zoom wheel)
- Look number (large): "Look 01"
- Piece name (medium): "Racing Suit — Bone White"
- Details (small, monospace): short descriptive fragments
- CTA (if available): "Add to Grid — Early Access" or "Sold Out"
- Navigation: previous/next look + counter

**No:** Size selector (handle on purchase flow), related products, reviews, share buttons

---

### Page 4: ARCHIVE `/archive`

**Purpose:** Past seasons. Each feels like a closed door.

**Layout:**
```
┌─────────────────────────────────────┐
│                                     │
│ THE ARCHIVE                         │
│                                     │
│ [S16] · [Neo-Clergy]        [View]  │
│ [FW16] · [Descriptor line]          │
│                                     │
│ [S15] · [Title]             [View]  │
│ [Descriptor line]                   │
│                                     │
│ [S14] · [Title]             [View]  │
│ [Descriptor line]                   │
│                                     │
│ ...all past seasons                 │
│                                     │
│ "Once the grid clears, it's gone."  │
│                                     │
├─────────────────────────────────────┤
│ DEVETESION · [Current Season] · Grid│
└─────────────────────────────────────┘
```

**Rules:**
- Each season = one row, not a card
- Season title: bold, tracking-wide
- Descriptor: muted, one line max
- "View" link: small, monospace, right-aligned
- Past seasons are viewable (not purchasable)
- Quote at bottom: "Once the grid clears, it's gone."

---

### Page 5: THE GRID `/grid`

**Purpose:** Membership. Exclusive. No hard sell. Just facts.

**Layout:**
```
┌─────────────────────────────────────┐
│                                     │
│         THE GRID                    │
│                                     │
│ Early access to collections.        │
│ Behind the lens content.            │
│ First purchase window.              │
│                                     │
│ Free: Email list.                   │
│ Paid: Early access + exclusives.    │
│                                     │
│ [ Join The Grid ]                   │
│                                     │
│ Already a member? [ Enter ]         │
│                                     │
├─────────────────────────────────────┤
│ DEVETESION · [Current Season] · Arch│
└─────────────────────────────────────┘
```

**Rules:**
- No pricing visible on first view (reveal after click)
- No "benefits" bullet list with checkmarks
- No testimonial from a member
- No countdown timer or urgency gimmick
- Copy is factual, not persuasive

**Copy:**
```
THE GRID

Early access to collections.
Behind the lens content.
First purchase window.

Free: Email list.
Paid: Early access + exclusives.

[ Join The Grid ]

Already a member? [ Enter ]
```

---

## PART 6: COMPONENT LIBRARY

### Navigation

```
Top nav — 4 items max, horizontal, no hamburger on desktop:

[Current Season]    Archive    The Grid    [Icon: Menu for mobile only]
```

- No logo in nav (brand is in footer)
- No search icon
- No cart icon (handle in purchase flow)
- Active state: underline, not bold
- Sticky: NO — nav scrolls away with content
- Season nav item updates automatically to current season

### Footer

```
3 lines max:

DEVETESION
[Current Season] · [Collection Title]
The Grid · Archive
```

- No social media icons
- No newsletter signup
- No sitemap
- No legal links (put in /legal page, not footer)
- No "© 2026 Devetesion. All rights reserved."

### Buttons

| Type | Style | Usage |
|------|-------|-------|
| Primary | Bone bg, black text, uppercase, tracked | Main CTA |
| Secondary | Transparent, bone border, bone text | Secondary action |
| Ghost | No border, bone text, underline on hover | Navigation links |

```css
/* Primary */
background: var(--color-bone);
color: var(--color-background);
padding: 12px 24px;
text-transform: uppercase;
letter-spacing: 0.2em;
font-size: 12px;

/* Secondary */
background: transparent;
color: var(--color-bone);
border: 1px solid var(--color-bone);
padding: 12px 24px;
text-transform: uppercase;
letter-spacing: 0.2em;
font-size: 12px;

/* Ghost */
background: transparent;
color: var(--color-text-muted);
text-decoration: none;
border-bottom: 1px solid transparent;
```

### Image Treatment

- NO rounded corners on images
- NO hover zoom
- NO overlay text on images
- NO shadow behind images
- Images are full-bleed within their container
- Aspect ratio: 3:4 (portrait) for look images, 16:9 for hero

---

## PART 7: TECHNICAL SPECIFICATIONS

### Tech Stack

```
Framework: Next.js 14 (App Router, Server Components)
Styling: Tailwind CSS v4 + CSS custom properties
Language: TypeScript strict
Animation: Framer Motion (minimal use)
Font: next/font (Helvetica Neue fallback)
Images: next/image with proper sizing
Deployment: Vercel
```

### Performance Targets

```
LCP < 2.5s
CLS < 0.1
TTI < 3.8s
First Contentful Paint < 1.8s
Total Bundle < 200KB (initial load)
```

### Accessibility

```
- All interactive elements: keyboard accessible (Tab, Enter, Escape)
- Focus ring: visible, 2px outline, bone color
- aria-label on all icon buttons
- Alt text on all images (descriptive, not decorative)
- Contrast: WCAG AA minimum (4.5:1 for normal text)
- prefers-reduced-motion: disable all animations
```

### Responsive Breakpoints

```
Mobile: < 640px (1 column)
Tablet: 640px — 1024px (2 columns)
Desktop: > 1024px (3 columns)
```

### Dark Mode

```
Dark mode is the ONLY mode. No light mode toggle.
No "system preference" detection.
Always dark. Always.
```

---

## PART 8: COPY REFERENCE

### All Copy By Page

**Homepage:**
```
[SEASON IDENTIFIER].
[ Shop SEASON ]
DEVETESION · The Grid
```

**Collection Header:**
```
[SEASON] · [COLLECTION TITLE]
[X] looks · No restocks
```

**Look Detail:**
```
Look [NUMBER]
[Piece Name] — [Color/Material]
[Detail fragment 1]. [Detail fragment 2]. [Detail fragment 3].
[ Add to Grid — Early Access / Sold Out ]
← [prev]  |  [current]/[total]  |  [next] →
```

**Archive:**
```
THE ARCHIVE
[SEASON] · [Title]
[Descriptor line]
[View]
...
"Once the grid clears, it's gone."
```

**The Grid:**
```
THE GRID
Early access to collections.
Behind the lens content.
First purchase window.
Free: Email list.
Paid: Early access + exclusives.
[ Join The Grid ]
Already a member? [ Enter ]
```

**Footer (all pages):**
```
DEVETESION
[Current Season] · [Collection Title]
The Grid · Archive
```

---

## PART 9: ENFORCEMENT CHECKLIST

Before any design or code is considered complete, verify every item:

### Visual
- [ ] Background is #0a0a0a to #121214 (not pure black, not grey)
- [ ] No warm tones anywhere on the site
- [ ] No gradient backgrounds
- [ ] No rounded corners beyond 4px
- [ ] No shadows (or barely perceptible)
- [ ] Max 3 font sizes per screen
- [ ] All headings are uppercase + tracking-wide
- [ ] Body text is 14px minimum
- [ ] No exclamation marks in any copy
- [ ] No rhetorical questions in any copy

### Layout
- [ ] No card-based layouts
- [ ] No grid of equal boxes
- [ ] No centered paragraph blocks
- [ ] Massive negative space present
- [ ] Asymmetric composition on at least one page
- [ ] No hamburger menu on desktop
- [ ] Footer is 3 lines max

### Interaction
- [ ] No bouncy animations
- [ ] No spring physics
- [ ] No spinners (skeleton screens only)
- [ ] No hover transforms (opacity only)
- [ ] No parallax scrolling
- [ ] No scroll-jacking
- [ ] Page transitions are fast (max 200ms)
- [ ] No chat widget
- [ ] No back-to-top button

### Anti-Pattern Audit
- [ ] No hero with smiling people
- [ ] No testimonial carousel
- [ ] No "About Us" origin story
- [ ] No newsletter popup
- [ ] No social proof badges
- [ ] No stock photography
- [ ] No "Learn More" buttons
- [ ] No 4-column footer

### Technical
- [ ] LCP < 2.5s
- [ ] CLS < 0.1
- [ ] All images have alt text
- [ ] All interactive elements keyboard accessible
- [ ] Focus ring visible and styled
- [ ] prefers-reduced-motion respected
- [ ] Mobile touch targets 44px minimum
- [ ] TypeScript strict, no `any`
- [ ] Bundle < 200KB initial

---

## PART 10: HOW TO USE THIS DOCUMENT

### For Designers (Figma, UI tools)
1. Read Parts 0-2 before touching any pixel
2. Use the color tokens and typography scale exactly
3. Check Part 5 for each page layout spec
4. Run Part 9 checklist before handoff

### For Developers (Code)
1. Set up Tailwind config with Part 1 tokens
2. Build components from Part 6
3. Follow page specs in Part 5
4. Enforce Part 3 interaction rules
5. Audit against Part 9 before merge

### For AI Agents
1. Read this entire document as context before any task
2. Use the correct skill from Part 0.5 for the task phase
3. Reference specific sections in your output
4. Flag any deviation from this document
5. Run Part 9 checklist as final validation

---

**This document is the source of truth. If any decision conflicts with this document, this document wins.**

DEVETƎSION. Built, not born.
