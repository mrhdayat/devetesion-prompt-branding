# DEVETESION — MASTER WEBSITE BUILD PROMPT

**Satu-satunya file yang dibutuhkan untuk membangun seluruh website DEVETESION.**
Copy-paste seluruh isi file ini ke AI coding agent. Jangan potong, jangan edit.

---

## 🎯 BRIEF UTAMA

Bangun website untuk brand fashion **DEVETESION** — dark luxury fashion house dengan aesthetic monolithic brutalism. Website harus terasa seperti **entering a brutalist cathedral**, bukan browsing e-commerce biasa.

### Konsep Inti: MINIMALISME × MAKSIMALISME

**Minimalis di:** Struktur, navigasi, whitespace, interaksi — setiap elemen punya tujuan jelas, tidak ada yang berlebihan.

**Maksimalis di:** Impact visual, kehadiran brand, scale — gambar full-bleed, tipografi besar, momen-momen dramatis saat scroll.

**Hasilnya:** Website yang terasa kosong tapi berat. Sedikit elemen tapi masing-masing elemen punya weight luar biasa. Seperti galeri seni — dinding putih kosong tapi lukisan yang ada di sana membuatmu berhenti dan menatap.

### Avant-Garde + Luxury

**Avant-Garde:**
- Asymmetric layouts yang intentional
- Typography yang bermain dengan scale extreme (sangat besar vs sangat kecil)
- Interaksi yang unexpected tapi functional (scroll-triggered reveals yang dramatic)
- Breaking conventions tanpa breaking usability

**Luxury:**
- Ruang kosong yang berlebihan (negative space sebagai luxury signal)
- Loading screen yang deliberate (bukan cepat, tapi intentional)
- Transisi yang smooth dan berat (tidak bouncy, tidak playful)
- Tidak ada elemen yang "murah" (no popups, no chat widgets, no social proof badges)

---

##  STRUKTUR WEBSITE

### Halaman yang Harus Dibangun

| Halaman | URL | Fungsi |
|---------|-----|--------|
| Loading Screen | (overlay) | Animasi intro sebelum website muncul |
| Homepage | `/` | Hero statement + season teaser |
| Collection | `/collection/[season]` | Grid looks dengan filter |
| Look Detail | `/collection/[season]/[look-number]` | Full-bleed image + detail |
| Archive | `/archive` | List semua season lampau |
| The Grid | `/grid` | Membership/exclusive access |
| Legal | `/legal` | Privacy, terms (minimal) |

---

## 🎨 DESIGN SYSTEM — TOKENS

### Color Palette

```css
:root {
  /* Backgrounds */
  --color-bg: #0a0a0a;
  --color-bg-raised: #121214;
  --color-bg-elevated: #1a1a1e;

  /* Surfaces */
  --color-surface: #121214;
  --color-surface-hover: #1a1a1e;
  --color-surface-active: #2a2a2e;

  /* Borders */
  --color-border: #2a2a2e;
  --color-border-subtle: #1a1a1e;

  /* Text */
  --color-text: #f0f0f0;
  --color-text-muted: #6a6a6e;
  --color-text-disabled: #3a3a3e;

  /* Accent — gunakan sangat sparingly, max 5% dari area */
  --color-accent: #c0c0c0;

  /* Special */
  --color-bone: #e8e4df;
  --color-void: #050507;
}
```

**Rules:**
- Background selalu near-black, bukan pure black
- Tidak ada warm tones, tidak ada gradients
- Accent color hanya untuk micro-interactions (hover underline, active state)
- Tidak ada color yang "pop" — semua muted, refined

### Typography

```css
:root {
  /* Font Families */
  --font-sans: 'Helvetica Neue', Arial, sans-serif;
  --font-mono: 'SF Mono', 'Menlo', monospace;

  /* Scale — max 3 sizes per screen */
  --text-xs: 10px;    /* Reference marks, timestamps */
  --text-sm: 12px;    /* Captions, labels, navigation */
  --text-base: 14px;  /* Body text, descriptions */
  --text-lg: 18px;    /* Sub-headings, rare use */
  --text-xl: 24px;    /* Section headers */
  --text-2xl: 36px;   /* Page titles */
  --text-4xl: 64px;   /* Hero statements — max 1 per page */
  --text-6xl: 120px;  /* Decorative — oversized, partial crop */

  /* Tracking — selalu wide */
  --tracking-widest: 0.2em;
  --tracking-wider: 0.1em;
  --tracking-wide: 0.05em;

  /* Line heights */
  --leading-tight: 1.0;
  --leading-normal: 1.5;
  --leading-relaxed: 1.7;

  /* Font weights — thin only */
  --font-light: 300;
  --font-regular: 400;
}
```

**Rules:**
- Hanya 3 ukuran font per screen (hierarki, bukan chaos)
- Headings: uppercase + tracking-widest
- Body: sentence case + tracking-wide
- Tidak ada decorative fonts — restrained, architectural
- Font weight max 400 — bold is for emphasis, not for headings

### Spacing

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
- Massive negative space sebagai luxury signal
- Content tidak pernah menyentuh edge (min 24px mobile, 48px desktop)
- Semua spacing kelipatan 4px

### Border Radius

```css
:root {
  --radius-none: 0px;
  --radius-sm: 2px;
  --radius-md: 4px;
}
```

**Rules:**
- Sharp edges by default
- Max radius 4px untuk interactive elements saja
- Tidak ada pill-shaped buttons, tidak ada rounded cards

### Motion

```css
:root {
  --duration-fast: 100ms;
  --duration-normal: 200ms;
  --duration-slow: 300ms;
  --duration-deliberate: 600ms;  /* Untuk loading screen transitions */

  --ease-in: cubic-bezier(0.4, 0, 1, 1);
  --ease-out: cubic-bezier(0, 0, 0.2, 1);
  --ease-deliberate: cubic-bezier(0.25, 0, 0.15, 1);  /* Heavy, deliberate */
}
```

**Rules:**
- Tidak ada spring animations
- Tidak ada bouncy transitions
- Hover: opacity shift saja, tidak ada transforms
- Page transitions: fade to dark (200ms)
- Scroll reveals: fade-in from bottom, subtle, heavy
- Loading screen: deliberate, tidak terburu-buru

---

## 🖥️ LOADING SCREEN — DETAIL LENGKAP

### Konsep

Loading screen adalah **pintu masuk** ke dunia DEVETESION. Bukan sekadar spinner — ini adalah momen pertama user berinteraksi dengan brand. Harus terasa seperti berdiri di depan pintu gedung brutalist sebelum masuk.

### Visual

```
Layar penuh, background #0a0a0a (near-black)

Di tengah:
┌─────────────────────────────┐
│                             │
│        DEVETƎSION           │  ← Brand name, tracking-widest, 36px, bone color
│                             │
│        ────────────         │  ← Thin horizontal line, 1px, bone color
│                             │      Line ini "terisi" secara progresif
│                             │
│        SEASON XII           │  ← Current season, 12px, tracking-widest, muted
│                             │
└─────────────────────────────┘

Progress: Line horizontal yang "terisi" dari kiri ke kanan
Durasi: 1.5 - 2.5 detik (tidak terlalu cepat, tidak terlalu lambat)
Setelah penuh: Fade to black (300ms) → Homepage muncul
```

### Behavior

1. **Trigger:** Loading screen muncul saat:
   - First visit ke website
   - Navigasi antar halaman utama (Homepage → Collection, Collection → Archive, dll)
   - TIDAK muncul saat navigasi within collection (grid → detail)

2. **Durasi:** Minimum 1.2 detik, maksimum 2.5 detik
   - Kalau data loading lebih cepat: tetap tampilkan minimal 1.2 detik
   - Kalau data loading lebih lama: tampilkan sampai data ready, max 2.5 detik lalu fallback

3. **Transisi keluar:**
   - Line terisi penuh → pause 200ms
   - Fade to black (300ms)
   - Homepage/content fade in (400ms)
   - Total transisi: ~900ms

4. **Easter egg (opsional tapi recommended):**
   - Kalau user klik/tekan space saat loading screen: durasi dipersingkat jadi 0.5 detik
   - Ini untuk power users yang sudah familiar

### Code Structure

```tsx
// components/LoadingScreen.tsx
// - Full screen overlay
// - Brand name + line progress + season text
// - Animated line fill with CSS transition
// - Fade out animation on complete
// - Triggered by route change or initial load
```

---

## 📄 HALAMAN — DETAIL PER HALAMAN

### 1. HOMEPAGE `/`

**Tujuan:** Command attention. Satu statement. Satu gambar. Satu link.

**Layout:**
```
┌────────────────────────────────────────────┐
│  DEVETESION                    [≡] Menu    │  ← Nav: brand kiri, hamburger kanan
├────────────────────────────────────────────┤
│                                            │
│                                            │
│         [Full-bleed hero image]            │
│         70% viewport height                │
│         Current season campaign visual     │
│                                            │
│                                            │
├────────────────────────────────────────────┤
│                                            │
│              S12.                          │  ← 64px, tracking-widest, uppercase
│                                            │
│         MOTORSPORT COUTURE                 │  ← 14px, tracking-wide, muted
│                                            │
│         [ SHOP S12 ]                       │  ← Button, bone bg, black text
│                                            │
│                                            │
├────────────────────────────────────────────┤
│  DEVETESION                                │
│  S12 · Motorsport Couture                  │
│  The Grid · Archive                        │  ← Footer: 3 lines max
└────────────────────────────────────────────┘
```

**Interaksi:**
- Hero image: tidak ada hover effect, tidak ada zoom
- "S12.": static text, tidak clickable
- "MOTORSPORT COUTURE": muted, descriptive
- "SHOP S12" button: hover = opacity 0.8, click → navigate ke /collection/s12
- Nav hamburger: hover = opacity 0.8, click → slide-in menu dari kanan

**Mobile:**
- Hero image: 60% viewport height
- "S12.": 48px
- Semua spacing disesuaikan untuk touch

**No:** Scrolling text, logo animation, multiple CTAs, taglines, testimonials, social proof

---

### 2. COLLECTION `/collection/[season]`

**Tujuan:** Display semua looks dalam satu season. Dark grid. No fluff.

**Layout:**
```
┌────────────────────────────────────────────┐
│  ← Back         S12                        │  ← Nav: back left, season center
│                 MOTORSPORT COUTURE         │
│                 30 looks · No restocks     │
├────────────────────────────────────────────┤
│                                            │
│  ┌──────┐  ┌──────  ┌──────┐             │
│  │      │  │      │  │      │             │
│  │  01  │  │  02  │  │  03  │             │
│  │      │  │      │  │      │             │
│  └──────┘  └──────┘  └──────┘             │
│                                            │
│  ┌──────┐  ┌──────  ┌──────┐             │
│  │      │  │      │  │      │             │
│  │  04  │  │  05  │  │  06  │             │
│  │      │  │      │  │      │             │
│  └──────┘  └──────┘  └──────┘             │
│                                            │
│  ... grid continues ...                    │
│                                            │
├────────────────────────────────────────────┤
│  DEVETESION · Archive · The Grid           │
└────────────────────────────────────────────┘
```

**Grid Rules:**
- 3 kolom desktop, 2 tablet, 1 mobile
- Gap 2px antara images (bukan 0, bukan besar)
- Images aspect ratio 4:5 (portrait)
- Hover: opacity 0.9, NO zoom, NO overlay
- Number (01, 02, etc): muncul di bottom-left image saat hover, 12px mono, bone color
- Scroll: infinite atau pagination — tidak ada "load more" button

**Header:**
- Back arrow: clickable, kembali ke homepage
- Season (S12): large, tracking-widest
- Collection name: muted, descriptive
- "30 looks · No restocks": smallest, muted, scarcity signal

**Interaksi:**
- Klik image → navigate ke /collection/s12/01
- Scroll: smooth, tidak ada parallax
- Grid items: fade-in saat scroll into view (subtle, 200ms)

**No:** Product descriptions on grid, prices visible, hover overlays, quick view

---

### 3. LOOK DETAIL `/collection/[season]/[look-number]`

**Tujuan:** Satu look. Full bleed. Details sebagai architectural marks.

**Layout:**
```
┌────────────────────────────────────────────┐
│  ←  S12              01 / 30        →  │  ← Nav: prev, season, counter, next
├────────────────────────────────────────────┤
│                                            │
│                                            │
│         [Full-bleed image]                 │
│         No crop, no zoom wheel             │
│         Occupies entire viewport           │
│                                            │
│                                            │
├────────────────────────────────────────────┤
│                                            │
│  Look 01                                   │  ← 24px, tracking-wide
│  Racing Suit — Bone White                  │  ← 14px, muted
│  Technical fabric. Patchwork.              │  ← 12px, mono, muted
│  DEVETƎSION chest branding.                │
│                                            │
│  [ ADD TO GRID — EARLY ACCESS ]            │  ← Button or "SOLD OUT"
│                                            │
├────────────────────────────────────────────┤
│  DEVETESION · Archive · The Grid           │
└────────────────────────────────────────────┘
```

**Image:**
- Full-bleed, no cropping, no zoom
- Aspect ratio determined by source image (tidak dipaksa)
- Click: tidak ada action (bukan lightbox, bukan zoom)
- Image loading: placeholder blur saat loading

**Details:**
- Look number: large, prominent
- Piece name: medium, descriptive
- Details: small, monospace, fragment-style (bukan paragraph)
- CTA: "ADD TO GRID — EARLY ACCESS" atau "SOLD OUT" (disabled state)

**Navigation:**
- ← Previous: navigate ke look sebelumnya
- Season (S12): clickable, kembali ke collection grid
- Counter (01/30): static
- → Next: navigate ke look selanjutnya
- Keyboard: arrow keys juga berfungsi

**No:** Size selector, related products, reviews, share buttons, zoom

---

### 4. ARCHIVE `/archive`

**Tujuan:** Past seasons. Each feels like a closed door.

**Layout:**
```
┌────────────────────────────────────────────┐
│  ← Back                                    │
├────────────────────────────────────────────┤
│                                            │
│           THE ARCHIVE                      │  ← 36px, tracking-widest
│                                            │
├────────────────────────────────────────────┤
│                                            │
│  ┌──────────────────────────────────────┐  │
│  │  S16 · NEO-CLERGY             [→]    │  │  ← Row: season, title, arrow
│  │  FW16 · Flooded concrete             │  │
│  │  ┌────┐ ┌────┐ ┌────┐               │  │  ← 3 thumbnail previews
│  │  │ 01 │ │ 02 │ │ 03 │               │  │
│  │  └────┘ └────┘ └────┘               │  │
│  └──────────────────────────────────────┘  │
│                                            │
│  ┌──────────────────────────────────────┐  │
│  │  S15 · [Title]                [→]    │  │
│  │  [Descriptor line]                   │  │
│  │  ┌────┐ ┌────┐ ┌────┐               │  │
│  │  │ 01 │ │ 02 │ │ 03 │               │  │
│  │  └────┘ └────┘ └────┘               │  │
│  └──────────────────────────────────────┘  │
│                                            │
│  ... more seasons ...                      │
│                                            │
│  "Once the grid clears, it's gone."        │  ← Quote at bottom, italic, muted
│                                            │
├────────────────────────────────────────────┤
│  DEVETESION · S12 · The Grid               │
└────────────────────────────────────────────┘
```

**Row Rules:**
- Setiap season = satu row, bukan card
- Season title: bold, tracking-wide
- Descriptor: muted, one line max
- Thumbnails: 3 small previews (looks 01, 02, 03 dari season itu)
- Arrow: monospace, right-aligned, clickable
- Hover row: background subtle change (surface-raised)
- Click row: expand → show all looks in that season
- Click thumbnail: navigate ke look detail season itu

**Past seasons:** Viewable, tidak purchasable

**Quote:** "Once the grid clears, it's gone." — italic, muted, 12px

---

### 5. THE GRID `/grid`

**Tujuan:** Membership. Exclusive. No hard sell. Just facts.

**Layout:**
```
┌────────────────────────────────────────────┐
│  ← Back                                    │
├────────────────────────────────────────────┤
│                                            │
│                                            │
│              THE GRID                      │  ← 36px, tracking-widest
│                                            │
│                                            │
│      Early access to collections.          │  ← 14px, centered
│      Behind the lens content.              │
│      First purchase window.                │
│                                            │
│      Free: Email list.                     │  ← 12px, muted
│      Paid: Early access + exclusives.      │
│                                            │
│      [ JOIN THE GRID ]                     │  ← Primary button
│                                            │
│      Already a member? [ Enter ]           │  ← Ghost link
│                                            │
│                                            │
├────────────────────────────────────────────┤
│  DEVETESION · S12 · Archive                │
└────────────────────────────────────────────┘
```

**Rules:**
- No pricing visible on first view
- No "benefits" bullet list dengan checkmarks
- No testimonial dari member
- No countdown timer atau urgency gimmick
- Copy factual, bukan persuasive
- "Already a member? [ Enter ]": ghost link, navigate ke login

---

### 6. LEGAL `/legal`

**Tujuan:** Minimum viable legal page.

**Layout:**
```
┌────────────────────────────────────────────┐
│  ← Back                                    │
├────────────────────────────────────────────┤
│                                            │
│  Privacy Policy                            │
│  [Text — minimal, clear, no legalese]      │
│                                            │
│  ────────────────────────────────          │
│                                            │
│  Terms of Service                          │
│  [Text — minimal, clear, no legalese]      │
│                                            │
├────────────────────────────────────────────┤
│  DEVETESION                                │
└────────────────────────────────────────────┘
```

**Rules:**
- Tidak ada navigation di legal page (hanya back)
- Tidak ada footer links
- Text: minimal, clear, tidak bertele-tele

---

## 🧭 NAVIGATION

### Desktop Nav (Homepage)

```
┌────────────────────────────────────────────┐
│  DEVETESION                    [≡] Menu    │
└────────────────────────────────────────────┘
```

- Brand: kiri, 14px, tracking-widest, clickable → homepage
- Hamburger: kanan, icon only, clickable → slide-in menu

### Slide-In Menu (dari kanan)

```
                    ┌──────────────┐
                    │  ✕ Close     │
                    ├──────────────┤
                    │              │
                    │  S12         │  ← Current season
                    │  Archive     │
                    │  The Grid    │
                    │              │
                    │  ──────────  │
                    │              │
                    │  Legal       │
                    │              │
                    └──────────────┘
```

- Slide dari kanan, width 280px
- Overlay: dark, 50% opacity, klik overlay = close menu
- Items: 14px, tracking-wide, hover = opacity 0.6
- Active item: underline (bone color, 1px)
- Divider line: separator antara nav utama dan legal

### Mobile Nav

- Same as desktop: hamburger di kanan
- Slide-in menu: full-width di mobile
- Brand tetap di kiri

---

## 🎬 INTERAKSI & ANIMASI

### Loading Screen
- Fade in saat route change: 200ms
- Line fill progress: 1.2-2.5 detik
- Fade out: 300ms → content fade in: 400ms

### Page Transitions
- Navigate: current page fade to black (200ms) → loading screen → new page fade in (400ms)
- Within collection (look detail): no loading screen, direct fade (200ms)
- Back button: instant, no animation

### Scroll Reveals
- Grid items: fade-in + slight translate-y (10px) saat scroll into view
- Duration: 300ms, ease-out
- Stagger: 50ms antara items yang adjacent
- Tidak ada parallax, tidak ada scroll-jacking

### Hover States
- Buttons: opacity 0.8
- Links: underline muncul (transition 150ms)
- Grid images: opacity 0.9
- Nav items: opacity 0.6
- Tidak ada transforms, tidak ada shadows, tidak ada scale

### Active States
- Buttons: opacity 0.6 saat ditekan
- Links: opacity 0.8
- Tidak ada ripple effects

### Keyboard Navigation
- Tab: visible focus ring (2px, bone color, outline)
- Enter: activate focused element
- Escape: close menu, go back
- Arrow keys: prev/next look di look detail page

---

## 📱 RESPONSIVE

### Desktop (>1024px)
- Collection grid: 3 kolom
- Hero image: 70vh
- Padding: 48px horizontal
- Nav: brand kiri, hamburger kanan

### Tablet (640px — 1024px)
- Collection grid: 2 kolom
- Hero image: 60vh
- Padding: 32px horizontal
- Nav: sama

### Mobile (<640px)
- Collection grid: 1 kolom
- Hero image: 50vh
- Padding: 24px horizontal
- Nav: brand kiri, hamburger kanan
- Slide-in menu: full-width
- Touch targets: minimum 44px

---

## 🚫 ANTI-PATTERNS — JANGAN PERNAH BUILD INI

| Pattern | Kenapa Dilarang |
|---------|-----------------|
| Hero section dengan smiling people | Generic, warm, welcoming — bukan DEVETESION |
| Testimonial carousel | Social proof = insecurity |
| "About Us" origin story | Nobody cares when you started |
| Newsletter signup popup | Desperate for attention |
| Social proof badges | Authority needs no proof |
| Rounded cards dengan shadows | Every SaaS ever |
| Gradient backgrounds | Warmth = cheap |
| Stock photography | Fake, lifeless |
| "Learn More" buttons | Weak, non-committal |
| Hamburger menu di desktop | OK untuk DEVETESION karena minimalist |
| Breadcrumb navigation | Clutters the void |
| Search bar di header | E-commerce pattern — tidak untuk DEVETESION |
| Footer dengan 4 kolom | Information dump — max 3 lines |
| Cookie consent banner custom | Legal, tapi buat minimal dan dark |
| Chat widget | "Need help?" = not confident |
| Back-to-top button | Clutters the void |
| Loading spinner | Gunakan skeleton screens atau loading screen |
| Toast notifications | Clutters the void — gunakan inline feedback |
| Modal popups | Interrupt the flow — gunakan full-page atau inline |

---

## ✅ QUALITY CHECKLIST

Sebelum deliver, pastikan semua ini:

### Visual
- [ ] Background #0a0a0a sampai #121214 (bukan pure black, bukan grey)
- [ ] Tidak ada warm tones di mana pun
- [ ] Tidak ada gradient backgrounds
- [ ] Tidak ada rounded corners beyond 4px
- [ ] Tidak ada shadows (atau barely perceptible)
- [ ] Max 3 font sizes per screen
- [ ] Semua headings uppercase + tracking-wide
- [ ] Body text minimum 14px
- [ ] Tidak ada exclamation marks di copy mana pun
- [ ] Tidak ada rhetorical questions di copy

### Layout
- [ ] Tidak ada card-based layouts
- [ ] Tidak ada grid of equal boxes (collection grid OK karena functional)
- [ ] Tidak ada centered paragraph blocks
- [ ] Massive negative space present
- [ ] Asymmetric composition di minimal satu halaman
- [ ] Tidak ada hamburger menu di desktop (kecuali untuk minimalism)
- [ ] Footer max 3 lines

### Interaction
- [ ] Tidak ada bouncy animations
- [ ] Tidak ada spring physics
- [ ] Tidak ada spinners (loading screen atau skeleton only)
- [ ] Tidak ada hover transforms (opacity only)
- [ ] Tidak ada parallax scrolling
- [ ] Tidak ada scroll-jacking
- [ ] Page transitions fast (max 200ms fade)
- [ ] Tidak ada chat widget
- [ ] Tidak ada back-to-top button
- [ ] Loading screen ada dan deliberate

### Technical
- [ ] LCP < 2.5s
- [ ] CLS < 0.1
- [ ] Semua images ada alt text
- [ ] Semua interactive elements keyboard accessible
- [ ] Focus ring visible dan styled
- [ ] prefers-reduced-motion respected
- [ ] Mobile touch targets 44px minimum
- [ ] TypeScript strict, tidak ada `any`
- [ ] Initial bundle < 200KB

### Anti-Pattern Audit
- [ ] Tidak ada hero dengan smiling people
- [ ] Tidak ada testimonial carousel
- [ ] Tidak ada "About Us" origin story
- [ ] Tidak ada newsletter popup
- [ ] Tidak ada social proof badges
- [ ] Tidak ada stock photography
- [ ] Tidak ada "Learn More" buttons
- [ ] Tidak ada 4-column footer
- [ ] Tidak ada cookie banner yang mencolok

---

## 🛠️ TECH STACK

```
Framework: Next.js 15 (App Router, Server Components)
Styling: Tailwind CSS v4 + CSS custom properties
Language: TypeScript strict
Animation: Framer Motion (minimal use — only untuk loading screen dan scroll reveals)
Font: next/font (Helvetica Neue fallback)
Images: next/image dengan proper sizing dan lazy loading
Deployment: Vercel
State: React Server Components (no client state needed)
```

---

## 📋 IMPLEMENTATION ORDER

Bangun dalam urutan ini:

### Phase 1: Foundation
1. Setup Next.js 15 project dengan TypeScript strict
2. Setup Tailwind CSS v4 dengan custom properties dari design tokens
3. Setup font loading (Helvetica Neue via next/font)
4. Setup basic layout shell (nav + footer)

### Phase 2: Loading Screen
5. Buat LoadingScreen component (full-screen overlay)
6. Implement line fill animation
7. Connect to route change events
8. Test timing (1.2s min, 2.5s max)

### Phase 3: Navigation
9. Buat header component (brand + hamburger)
10. Buat slide-in menu component
11. Implement open/close animations
12. Implement keyboard navigation (Escape to close)

### Phase 4: Homepage
13. Buat homepage layout (hero + statement + CTA)
14. Implement hero image loading (blur placeholder)
15. Test responsive (desktop, tablet, mobile)

### Phase 5: Collection Grid
16. Buat collection grid layout (3/2/1 columns)
17. Implement image grid dengan 2px gap
18. Implement hover states (opacity + number reveal)
19. Implement scroll reveal animation
20. Test responsive

### Phase 6: Look Detail
21. Buat look detail layout (full-bleed image + details)
22. Implement prev/next navigation
23. Implement keyboard navigation (arrow keys)
24. Test responsive

### Phase 7: Archive
25. Buat archive layout (list of seasons)
26. Implement expand/collapse untuk each season
27. Implement thumbnail previews
28. Test responsive

### Phase 8: The Grid
29. Buat The Grid page (membership)
30. Implement form (email signup)
31. Test responsive

### Phase 9: Legal
32. Buat legal page (privacy + terms)
33. Minimal text, clean layout

### Phase 10: Polish
34. Implement page transitions (fade to black)
35. Implement scroll reveals (fade-in + translate)
36. Implement focus rings untuk accessibility
37. Implement prefers-reduced-motion
38. Test semua interactions di keyboard
39. Test responsive di semua breakpoints
40. Run performance audit (Lighthouse)
41. Fix semua issues

### Phase 11: Content
42. Isi semua copy sesuai brand guidelines
43. Pasang placeholder images (nanti diganti dengan campaign photos)
44. Final review

---

## 📝 COPY REFERENCE

### Homepage
```
S12.

MOTORSPORT COUTURE

[ SHOP S12 ]

DEVETESION
S12 · Motorsport Couture
The Grid · Archive
```

### Collection Header
```
S12 · MOTORSPORT COUTURE
30 looks · No restocks
```

### Look Detail
```
Look 01
Racing Suit — Bone White
Technical fabric. Patchwork. DEVETƎSION chest branding.

[ ADD TO GRID — EARLY ACCESS ]

← 02  |  01/30  |  12 →
```

### Archive
```
THE ARCHIVE

S16 · NEO-CLERGY
FW16 · Flooded concrete
[View]

"Once the grid clears, it's gone."
```

### The Grid
```
THE GRID

Early access to collections.
Behind the lens content.
First purchase window.

Free: Email list.
Paid: Early access + exclusives.

[ JOIN THE GRID ]

Already a member? [ Enter ]
```

### Footer (semua halaman)
```
DEVETESION
S12 · Motorsport Couture
The Grid · Archive
```

---

## 🎯 FINAL NOTE

Website ini harus terasa seperti **berjalan masuk ke sebuah brutalist cathedral yang gelap**. Bukan e-commerce. Bukan blog. Bukan landing page.

Setiap pixel harus intentional. Setiap animasi harus deliberate. Setiap kata harus load-bearing.

Kalau ada elemen yang bisa dihapus tanpa mengubah makna — hapus.
Kalau ada animasi yang terasa playful — ganti dengan yang heavy.
Kalau ada warna yang terasa warm — ganti dengan yang cool.

**DEVETESION tidak meminta perhatian. DEVETESION mengambilnya.**

---

**Ini adalah source of truth. Kalau ada keputusan yang conflict dengan dokumen ini, dokumen ini yang menang.**

DEVETƎSION. Built, not born.
