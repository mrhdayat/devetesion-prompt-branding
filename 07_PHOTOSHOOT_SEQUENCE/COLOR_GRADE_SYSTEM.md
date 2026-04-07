# COLOR GRADE SYSTEM

**Consistent color grading across all 30 images. Choose ONE grade and apply to every image.**

---

## WHY CONSISTENT COLOR GRADING MATTERS

A real photoshoot has consistent color because:
1. Same camera, same settings, same day
2. Same film stock (or same digital sensor profile)
3. Same post-processing — one colorist grades the entire session
4. Same lighting conditions (or intentionally varied within a known range)

Without this, each AI-generated image has its own color personality → looks like random images, not a sequence.

**This system fixes that.**

---

## THE FOUR GRADES

### GRADE 1: KODAK PORTRA 400 WARM (Recommended for DEVETESION)

**The look:** Professional fashion editorial. Warm, beautiful skin tones, fine grain.

```
COLOR TEMPERATURE: +300K shift toward warm (slight amber cast overall)
TINT: +5 toward magenta (counteracts green from fluorescent environments)
CONTRAST: Medium — gentle S-curve
  - Shadows: crushed slightly (-10 on 0-100 scale)
  - Midtones: lifted slightly (+5)
  - Highlights: compressed slightly (-5)
SATURATION: +5 overall
  - Reds: +10 (lips, warm tones)
  - Oranges: +15 (skin tones)
  - Yellows: +5 (warmth)
  - Greens: -5 (reduce fluorescent green cast)
  - Blues: -10 (cool down the daylight to balance warmth)
  - Purples: 0
GRAIN: Kodak Portra 400 pattern
  - Amount: 25 (visible but fine)
  - Size: 0.8 (small, refined)
  - Roughness: 0.7 (smooth grain)
SHARPENING: Minimal
  - Amount: 20
  - Radius: 0.8
  - Detail: 25
  - Masking: 40 (only sharpen edges, not skin)
VIGNETTE: -8 (barely perceptible edge darkening)
EXPOSURE: 0 (neutral — get exposure right in generation)
```

**Best for:** Campaign images, lookbook, anything that needs to feel expensive and editorial.

**Reference images:** Vogue editorial spreads, System Magazine, Acne Studios campaigns.

---

### GRADE 2: FUJI PRO 400H COOL

**The look:** Intellectual, refined, slightly detached. Cool where Portra is warm.

```
COLOR TEMPERATURE: -200K shift toward cool (slight blue cast)
TINT: 0 (neutral — no green or magenta shift)
CONTRAST: Low-medium — flatter than Portra
  - Shadows: neutral (0)
  - Midtones: neutral (0)
  - Highlights: lifted slightly (+5) — more shadow detail
SATURATION: 0 overall (natural, no boost)
  - Reds: 0
  - Oranges: -5 (cooler skin)
  - Yellows: -10
  - Greens: +5
  - Blues: +10
  - Purples: +5
GRAIN: Fuji Pro 400H pattern
  - Amount: 20 (less visible than Portra)
  - Size: 0.7
  - Roughness: 0.6
SHARPENING: Minimal
  - Amount: 15
  - Radius: 0.7
  - Detail: 20
  - Masking: 50
VIGNETTE: -5 (very subtle)
```

**Best for:** Archive shots, behind-the-scenes, intellectual/editorial aesthetic.

**Reference images:** Dazed editorial, i-D Magazine, Prada campaigns.

---

### GRADE 3: RAW FLASH — NO GRADE

**The look:** What the camera captured. Direct flash, no post-processing. Honest.

```
COLOR TEMPERATURE: 0 (no shift — whatever the source is)
TINT: 0
CONTRAST: High — flash naturally creates high contrast
  - Shadows: crushed (-20) — flash doesn't fill shadows
  - Midtones: neutral
  - Highlights: may clip (+10 in small specular areas)
SATURATION: +10 (flash makes colors pop naturally)
  - Reds: +10
  - Oranges: +15
  - Yellows: +5
  - Greens: 0
  - Blues: 0
  - Purples: +5
GRAIN: Digital ISO noise at ISO 400
  - Amount: 30 (more visible — it's digital noise, not film grain)
  - Size: 0.5 (fine, digital)
  - Roughness: 0.5
SHARPENING: None — straight out of camera
  - Amount: 0
VIGNETTE: -15 (flash fall-off is real — edges are naturally darker)
```

**Best for:** Flash paparazzi aesthetic, raw documentary energy, Balenciaga-style campaigns.

**Reference images:** Balenciaga SS campaigns, Juergen Teller photography, flash street style.

---

### GRADE 4: CCTV / SURVEILLANCE

**The look:** Security camera still elevated to editorial. Desaturated, compressed, degraded.

```
COLOR TEMPERATURE: +100 (slight warm shift from cheap sensor)
TINT: +15 toward green (cheap sensors lean green)
CONTRAST: Low — compressed tonal range
  - Shadows: lifted (+15) — cheap cameras can't hold deep blacks
  - Midtones: compressed (-10)
  - Highlights: compressed (-10)
SATURATION: -30 (heavily desaturated)
  - Reds: -30
  - Oranges: -30
  - Yellows: -20
  - Greens: -20
  - Blues: -30
  - Purples: -30
GRAIN: Digital compression noise
  - Amount: 40 (heavy)
  - Size: 1.0 (large, blocky)
  - Roughness: 0.3 (harsh)
SHARPENING: Over-sharpened (cheap cameras over-process)
  - Amount: 40
  - Radius: 1.2
  - Detail: 60
  - Masking: 0 (sharpens everything including noise)
VIGNETTE: -20 (cheap lenses have heavy falloff)
ADDITIONAL: Slight JPEG compression artifacts visible at edges
  - Simulate with: low-quality JPEG re-save at 75% quality
```

**Best for:** Lo-fi surveillance aesthetic, clinical/institutional campaigns, anti-fashion.

**Reference images:** Wolfgang Tillmans surveillance work, Thomas Ruff JPEG series, CCTV footage.

---

## HOW TO APPLY THE GRADE

### In AI Image Generation (FLOW, Midjourney, DALL-E)

Append the grade description to your prompt. Example:

```
COLOR GRADE: Kodak Portra 400 — warm overall cast (+300K), skin tones warm and accurate,
blacks slightly lifted (dark brown not pure black), highlights warm cream tone, fine warm
grain visible throughout, gentle S-curve contrast, minimal sharpening, barely perceptible
vignette. Scanned on Noritsu HS-1800.
```

### In Post-Processing (Lightroom, Capture One)

If you're doing a second pass on generated images:
1. Apply the grade settings above as a preset
2. Batch-apply to all 30 images
3. Fine-tune exposure per image if needed (keep other settings locked)

### For Consistency Check

Place all 30 generated images side by side in a grid. Check:
- [ ] All images have the same overall color cast (warm/cool/neutral)
- [ ] Blacks are consistent (all slightly lifted, or all crushed — same treatment)
- [ ] Highlights behave the same (all warm, or all neutral)
- [ ] Grain is visible and similar across all images
- [ ] No single image "pops out" color-wise
- [ ] Skin tones (if visible) are consistent across all models

If one image looks different → re-generate it with the grade more explicitly stated.

---

## GRADE COMPARISON

| Quality | Portra 400 | Fuji 400H | Raw Flash | CCTV |
|---------|-----------|-----------|-----------|------|
| Warmth | Warm | Cool | Neutral | Slight warm + green |
| Contrast | Medium | Low-Medium | High | Low |
| Saturation | +5 | 0 | +10 | -30 |
| Grain | Fine, warm | Fine, cool | Digital noise | Heavy, blocky |
| Vibe | Editorial | Intellectual | Raw | Surveillance |
| Best for | Campaign | Archive | Flash paparazzi | Lo-fi |

---

## RECOMMENDED GRADE FOR DEVETESION S12

**Use Grade 1: KODAK PORTRA 400 WARM**

Reasoning:
- S12 is "Motorsport Couture" — it needs to feel expensive and crafted
- Portra 400 is the most common film stock for fashion editorials
- Warm tones complement the bone white, racing suit, patchwork aesthetic
- It makes the brutalist concrete environment feel slightly warm, not clinical
- This grade says "this is a real photograph" most convincingly

**Exception:** If you want S12 to feel more raw and confrontational (Balenciaga energy),
use Grade 3: RAW FLASH instead.
