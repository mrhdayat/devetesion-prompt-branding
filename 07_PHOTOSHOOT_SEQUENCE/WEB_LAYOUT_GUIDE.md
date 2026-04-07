# WEB LAYOUT GUIDE

**How to arrange the 30 photoshoot images as moodboard and web app layouts.**

All generated images are 4:5 aspect ratio (portrait editorial standard). This guide shows how to use them.

---

## PART 1: MOODBOARD LAYOUTS

### 1A: THE GRID (Reference Moodboard)

```
┌────┬────┬────┬────┬────┬────┐
│ 01 │ 02 │ 03 │ 04 │ 05 │ 06 │
├────┼────┼────┼────┼────┼────┤
│ 07 │ 08 │ 09 │ 10 │ 11 │ 12 │
├────┼────┼────┼────┼────┼────┤
│ 13 │ 14 │ 15 │ 16 │ 17 │ 18 │
├────┼────┼────┼────┼────┼────┤
│ 19 │ 20 │ 21 │ 22 │ 23 │ 24 │
├────┼────┼────┼────┼────┼────┤
│ 25 │ 26 │ 27 │ 28 │ 29 │ 30 │
└────┴────┴────┴────┴────┴────┘
```

- 6 columns × 5 rows
- 2px gap between images
- No borders, no labels
- Images in sequence order (01-30)
- Total aspect ratio: approximately 4:3 landscape

**Use for:** Internal review, press kit, lookbook overview.

---

### 1B: THE HERO + GRID

```
┌────────────────────────────────┐
│                                │
│         01 (HERO)              │
│        Full Width              │
│                                │
├────┬────┬────┬────┬────┬───────┤
│ 02 │ 03 │ 04 │ 05 │ 06 │ 07   │
├────┼────┼────┼────┼────┼───────┤
│ 08 │ 09 │ 10 │ 11 │ 12 │ 13   │
├────┼────┼────┼────┼────┼───────┤
│ 14 │ 15 │ 16 │ 17 │ 18 │ 19   │
├────┼────┼────┼────┼────┼───────┤
│ 20 │ 21 │ 22 │ 23 │ 24 │ 25   │
├────┼────┼────┼────┼────┼───────┤
│ 26 │ 27 │ 28 │ 29 │ 30 │      │
└────┴────┴────┴────┴────┴───────┘
```

- Hero image (Look 01) at full width, 2× height
- Remaining 29 images in 6-column grid below
- Hero acts as the "cover" — remaining images are the spread

**Use for:** Landing page lookbook, campaign overview.

---

### 1C: THE SEQUENCE STRIP

```
┌───┬───┬───┬───┬───┬───┬───┬───┬───┬───┐
│01 │02 │03 │04 │05 │06 │07 │08 │09 │10 │
└───┴───┴───┴───┴───┴───┴───┴───┴───┴───┘
┌───┬───┬───┬───┬───┬───┬───┬───┬───┬───┐
│11 │12 │13 │14 │15 │16 │17 │18 │19 │20 │
└───┴───┴───┴───┴───┴───┴───┴───┴───┴───┘
┌───┬───┬───┬───┬───┬───┬───┬───┬───┬───┐
│21 │22 │23 │24 │25 │26 │27 │28 │29 │30 │
└───┴───┴───┴───┴───┴───┴───┴───┴───┴───┘
```

- 3 rows of 10 images each
- Each image is narrow (portrait, cropped to fit)
- Horizontal scroll on mobile
- Read left-to-right, top-to-bottom

**Use for:** Horizontal scroll moodboard, Instagram carousel (3 carousels of 10).

---

### 1D: THE EDITORIAL SPREAD

```
┌────────────────┬────────┬────────┐
│                │   02   │   03   │
│       01       ├────────┼────────┤
│                │   04   │   05   │
├────────────────┴────────┴────────┤
│                06                │
├────────┬────────────────┬────────┤
│   07   │       08       │   09   │
├────────┼────────────────┼────────┤
│   10   │       11       │   12   │
└────────┴────────────────┴────────┘
...continue pattern for all 30
```

- Mixed sizes: some images span 2 columns, some span 2 rows
- Creates visual rhythm — not a boring uniform grid
- Mimics a magazine spread layout

**Use for:** Editorial-style lookbook, printed zine, premium web presentation.

---

## PART 2: WEB APP LAYOUTS

### 2A: COLLECTION PAGE (E-Commerce)

```
┌─────────────────────────────────────┐
│ S12 · MOTORSPORT COUTURE           │
│ 30 looks · No restocks              │
├─────────────────────────────────────┤
│                                     │
│  ┌────┐  ┌────┐  ┌────┐            │
│  │ 01 │  │ 02 │  │ 03 │            │
│  └────┘  └────┘  └────┘            │
│                                     │
│  ┌────┐  ┌────┐  ┌────┐            │
│  │ 04 │  │ 05 │  │ 06 │            │
│  └────┘  └────┘  └────┘            │
│                                     │
│  [ Load More ]                      │
│                                     │
├─────────────────────────────────────┤
│ DEVETESION · Archive · The Grid     │
└─────────────────────────────────────┘
```

- 3 columns desktop, 2 tablet, 1 mobile
- 2px gap between images
- No text on images — look number appears below each image on hover
- Click any image → Look Detail page
- Infinite scroll or "Load More" button
- All images same size, same spacing

---

### 2B: LOOK DETAIL PAGE

```
┌─────────────────────────────────────┐
│                                     │
│                                     │
│         [Full-bleed image]          │
│         Single look, full bleed     │
│         No crop, no zoom wheel      │
│         occupies entire viewport    │
│                                     │
│                                     │
└─────────────────────────────────────┘
┌─────────────────────────────────────┐
│ Look 01                             │
│ Racing Suit — Bone White            │
│ Technical fabric. Patchwork.        │
│ DEVETƎSION chest branding.          │
│                                     │
│ [ Add to Grid — Early Access ]      │
│                                     │
│ ← 02  |  01/30  |  12 →            │
└─────────────────────────────────────┘
```

- Image is full-bleed, no UI chrome
- Details appear below the fold
- Prev/Next navigation at bottom
- Keyboard navigation: ← → arrows
- Swipe on mobile

---

### 2C: HORIZONTAL SCROLL GALLERY

```
← scroll →
┌────┬────┬────┬────┬────┬────┬────┐
│ 01 │ 02 │ 03 │ 04 │ 05 │ 06 │ 07 │  ...
└────┴────┴────┴────┴────┴────┴────┘
```

- Horizontal scrolling gallery
- Each image is full height of viewport
- Snap to each image (CSS scroll-snap)
- Look counter: "01 / 30" fixed in corner
- Swipe on mobile, scroll or drag on desktop

---

### 2D: STORIES FORMAT

```
┌──────────────────┐
│                  │
│                  │
│   Full-screen    │
│   single image   │
│   9:16 crop      │
│                  │
│                  │
├──────────────────┤
│ ○○○○●○○○○○○○○○○○│
│ 04 / 30          │
│ Look 04          │
│ [Next →]        │
└──────────────────┘
```

- Full-screen, one image at a time
- Progress dots at bottom (like Instagram Stories)
- Tap/click to advance
- Auto-advance after 5 seconds
- 9:16 crop from the 4:5 original

---

### 2E: ARCHIVE PAGE

```
┌─────────────────────────────────────┐
│                                     │
│ THE ARCHIVE                         │
│                                     │
│ ┌─────────────────────────────────┐ │
│ │ S16 · Neo-Clergy          [→]  │ │
│ │ FW16 · Flooded concrete        │ │
│ │ [3 thumbnails: 01, 02, 03]     │ │
│ └─────────────────────────────────┘ │
│                                     │
│ ┌─────────────────────────────────┐ │
│ │ S15 · [Title]           [→]    │ │
│ │ [Descriptor]                   │ │
│ │ [3 thumbnails: 01, 02, 03]     │ │
│ └─────────────────────────────────┘ │
│                                     │
│ "Once the grid clears, it's gone."  │
│                                     │
└─────────────────────────────────────┘
```

- Each season = one expandable row
- Row shows 3 thumbnail previews
- Click row → expands to show all looks
- Click thumbnail → goes to that look detail
- Past seasons are viewable, not purchasable

---

## PART 3: RESPONSIVE BEHAVIOR

### Desktop (>1024px)
- 3 columns for collection grid
- Full-bleed images at 4:5 ratio
- Side-by-side layout where applicable

### Tablet (640px — 1024px)
- 2 columns for collection grid
- Images slightly larger
- Horizontal scroll for galleries

### Mobile (<640px)
- 1 column for collection grid
- Full-width images
- Stories format works best
- Swipe navigation

---

## PART 4: IMAGE OPTIMIZATION FOR WEB

### File Format
- **WebP** for all images (best compression/quality ratio)
- **Fallback:** JPEG at 85% quality for older browsers

### Sizes to Generate

| Size | Width | Use |
|------|-------|-----|
| Thumbnail | 300px | Grid previews, archive thumbnails |
| Medium | 800px | Mobile full-width, tablet 2-column |
| Large | 1200px | Desktop 3-column, tablet full-width |
| Full | 1600px | Look detail page, hero images |
| Original | As generated | Master archive, print |

### Responsive Image Markup

```html
<picture>
  <source type="image/webp"
    srcset="look-01-300.webp 300w,
            look-01-800.webp 800w,
            look-01-1200.webp 1200w,
            look-01-1600.webp 1600w"
    sizes="(max-width: 640px) 100vw,
           (max-width: 1024px) 50vw,
           33vw">
  <img src="look-01-1200.jpg"
    alt="DEVETESION S12 Look 01 — [description]"
    loading="lazy"
    width="1200"
    height="1500">
</picture>
```

---

## PART 5: CSS LAYOUT EXAMPLES

### Collection Grid (Tailwind CSS)

```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-0.5">
  {looks.map((look) => (
    <a href={`/s12/${look.number}`} class="relative aspect-[4/5] overflow-hidden">
      <Image
        src={look.src}
        alt={`S12 Look ${look.number}`}
        fill
        className="object-cover transition-opacity hover:opacity-90"
      />
    </a>
  ))}
</div>
```

### Horizontal Scroll Gallery

```html
<div class="flex overflow-x-auto snap-x snap-mandatory scrollbar-hide">
  {looks.map((look) => (
    <div class="flex-none w-screen h-screen snap-center">
      <Image src={look.src} alt="" fill className="object-cover" />
    </div>
  ))}
</div>
```

### Hero + Grid Layout

```html
<!-- Hero -->
<div class="relative w-full aspect-[16/9]">
  <Image src={hero.src} alt="" fill className="object-cover" />
</div>

<!-- Grid -->
<div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-6 gap-0.5">
  {remainingLooks.map(look => <Image key={look.number} ... />)}
</div>
```

---

## PART 6: LAZY LOADING STRATEGY

```
Priority loading:
1. Look 01 (hero/first in grid) — eager load
2. Looks 02-06 (above the fold) — lazy load, fetch immediately
3. Looks 07-18 — lazy load, fetch when scrolled near
4. Looks 19-30 — lazy load, fetch on demand

Implementation:
- Use <Image loading="lazy"> for all images except Look 01
- Use <Image loading="eager"> for Look 01
- Consider placeholder: blur-up from tiny base64 preview
```

---

## SUMMARY

This guide covers:
- 4 moodboard layouts (Grid, Hero+Grid, Sequence Strip, Editorial Spread)
- 5 web app layouts (Collection, Look Detail, Horizontal Gallery, Stories, Archive)
- Responsive behavior for mobile/tablet/desktop
- Image optimization specs (WebP, sizes, markup)
- CSS layout examples (Tailwind)
- Lazy loading strategy

All layouts use the same 4:5 aspect ratio images generated from the photoshoot sequence.
