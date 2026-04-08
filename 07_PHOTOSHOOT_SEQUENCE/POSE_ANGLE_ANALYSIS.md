# DEVETESION — INSPO POSE ANALYSIS

**Analisis 43 foto editorial fashion dari folder inspo-pose/.**

Hasil analisis ini menjadi ACUAN untuk pose dan camera angle di MASTER_PHOTOSHOOT_PROMPT.md.

---

## 🎯 TEMUAN UTAMA — MENGAPA HASIL GENERATE TERLIHAT JELEK

### Masalah Utama: Camera Angle Terlalu Monoton
Prompt sekarang tidak mengontrol camera angle. AI default ke **eye-level front view** — yang bikin semua foto terlihat sama dan sangat "AI slop".

### Yang Ada di Reference (43 Foto):
**6 jenis camera angle berbeda** — bukan cuma front view:

| Angle | Frekuensi di Reference | Contoh |
|-------|----------------------|--------|
| **High angle (looking down)** — kamera di atas, model terlihat dari atas | ~25% | Model reaching toward camera, fisheye energy |
| **Low angle (looking up)** — kamera di bawah, model towering | ~15% | Model di underpass, difoto dari bawah |
| **Eye level, 3/4 angle** — model TIDAK menghadap langsung kamera | ~20% | Model looking away, contemplative |
| **Eye level, front-on** — langsung ke kamera | ~15% | Editorial portrait |
| **Top-down (bird's eye)** — kamera tepat di atas | ~10% | Model duduk di lantai, difoto dari atas |
| **Ground level** — kamera sejajar tanah | ~15% | Crouching, low angle |

**Kesimpulan:** Hanya 15% yang front-on eye level. Sisanya **85% punya angle yang bervariasi**. Ini yang bikin foto editorial terlihat real dan tidak "AI slop".

---

## 📐 CAMERA ANGLE DETAIL

### Angle 1: HIGH ANGLE — Looking Down (Most Dynamic)
**Apa itu:** Kamera diposisikan di atas model, melihat ke bawah. Model bisa reaching toward camera.

**Ciri khas:**
- Tangan/jari model terlihat besar di foreground (perspektif dramatis)
- Kepala model terlihat kecil dari atas
- Background terlihat dari atas (lantai, jalan, dll)
- Sering pakai wide-angle/fisheye lens untuk efek dramatis
- Model bisa crouching atau standing, yang penting kamera di atas

**Vibe:** Confrontational, dynamic, Y2K energy, paparazzi-style
**Kapan dipakai:** Streetwear, techwear, casual, outerwear

**Referensi di folder:** `_ (2).jpeg`, `_ (3).jpeg`, `_ (5).jpeg`, `AW22.jpeg`, `_ (9).jpeg`

**Prompt keyword:**
```
High camera angle — camera positioned above the model looking down.
Model reaching toward camera lens, hands prominent in foreground.
Wide-angle lens distortion, fisheye energy.
Dramatic perspective — head small, hands large.
```

---

### Angle 2: LOW ANGLE — Looking Up
**Apa itu:** Kamera diposisikan di bawah model, melihat ke atas. Model terlihat towering.

**Ciri khas:**
- Model terlihat besar, megah, berkuasa
- Langit/ceiling terlihat di background atas
- Kaki model terlihat lebih panjang
- Chin tilted up atau straight
- Sering dipakai di outdoor urban settings

**Vibe:** Powerful, architectural, dominant
**Kapan dipakai:** Tailoring, couture, outerwear, ketika outfit perlu terlihat commanding

**Referensi di folder:** `_ (7).jpeg`, `_ (13).jpeg`, `Editorial photoshoot underpass.jpeg`

**Prompt keyword:**
```
Low camera angle — camera positioned below the model looking upward.
Model towers over the camera, chin slightly lifted.
Sky/ceiling visible in upper background.
Legs elongated, commanding presence.
```

---

### Angle 3: EYE LEVEL — 3/4 Angle (NOT Front-On)
**Apa itu:** Kamera setinggi mata tapi model TIDAK menghadap langsung ke kamera. Body at 30-60 degree angle.

**Ciri khas:**
- Model looking away from camera, atau looking past camera
- Body at angle, not squared to lens
- More contemplative, editorial mood
- One shoulder closer to camera than the other

**Vibe:** Contemplative, editorial, sophisticated
**Kapan dipakai:** Tailoring, couture, ketika outfit perlu terlihat dari sudut interesting

**Referensi di folder:** `_ (14).jpeg`, `city niht.jpeg`, `CITY LIGHTS.jpeg`

**Prompt keyword:**
```
Eye-level camera angle but model at 3/4 angle to camera.
Model NOT looking directly at lens — looking past camera or away.
One shoulder closer to camera than the other.
Contemplative, editorial mood.
```

---

### Angle 4: EYE LEVEL — Front-On (Direct)
**Apa itu:** Kamera setinggi mata, model menghadap langsung ke kamera.

**Ciri khas:**
- Direct eye contact
- Both shoulders equidistant from camera
- Confrontational or portrait energy
- Paling umum tapi paling riskan untuk AI slop

**Vibe:** Confrontational, portrait, direct
**Kapan dipakai:** Ketika outfit punya detail depan yang perlu terlihat jelas

**Referensi di folder:** `_ (10).jpeg`, `_ (11).jpeg`

**Prompt keyword:**
```
Eye-level camera angle, model facing camera directly.
Both shoulders equidistant from lens.
Direct eye contact with camera.
Editorial portrait energy.
```

---

### Angle 5: TOP-DOWN (Bird's Eye)
**Apa itu:** Kamera tepat di atas model, melihat straight down.

**Ciri khas:**
- Model terlihat dari atas — seperti peta
- Body spread out on ground/floor
- Geometric, symmetrical compositions possible
- Sangat editorial, sangat intentional

**Vibe:** Sculptural, geometric, high-fashion
**Kapan dipakai:** Couture, avant-garde, ketika pose di lantai

**Referensi di folder:** `QUEEN OF ICE.jpeg`

**Prompt keyword:**
```
Top-down camera angle — camera positioned directly above the model looking straight down.
Model lying or sitting on ground, body spread out.
Geometric, bird's eye perspective.
High-fashion editorial composition.
```

---

### Angle 6: GROUND LEVEL
**Apa itu:** Kamera sejajar tanah, sangat rendah.

**Ciri khas:**
- Ground/pavement fills lower portion of frame
- Model crouching or standing, but camera is at ground level
- Long shadows visible on ground
- Very cinematic, very editorial

**Vibe:** Cinematic, raw, urban
**Kapan dipakai:** Streetwear, outdoor urban, ketika shadow penting

**Referensi di folder:** `Editorial photoshoot underpass.jpeg`, `Grunge Photoshoot in Arizona.jpeg`

**Prompt keyword:**
```
Ground-level camera angle — camera positioned at ground level, parallel to the floor.
Pavement/ground fills lower portion of frame.
Long shadows cast on ground visible.
Cinematic, urban editorial energy.
```

---

## 🧍 POSE TYPES YANG ADA DI REFERENCE

### Pose Type 1: HANDS REACHING TOWARD CAMERA
**Deskripsi:** Model menjangkau tangan ke arah kamera. Tangan/jari terlihat besar di foreground karena perspektif.

**Body mechanics:**
- Satu atau kedua tangan extended toward lens
- Fingers spread or gesturing
- Body crouching atau standing
- Eye contact with camera

**Vibe:** Confrontational, dynamic, engaging
**Frekuensi di reference:** ~20%

---

### Pose Type 2: CROUCHING / SQUATTING
**Deskripsi:** Model berjongkok, rendah ke tanah.

**Body mechanics:**
- Both knees bent, body low
- One or both hands on ground or near knees
- Head tilted or looking at camera
- Can be compact (knees to chest) or wide (knees apart)

**Vibe:** Raw, feral, grounded
**Frekuensi di reference:** ~15%

---

### Pose Type 3: SITTING ON GROUND/FLOOR
**Deskripsi:** Model duduk di lantai, bukan di kursi.

**Body mechanics:**
- Sitting on ground with legs extended, crossed, or spread
- One hand behind for support, or both hands on knees
- Leaning forward or back
- Casual but intentional

**Vibe:** Relaxed, intimate, editorial
**Frekuensi di reference:** ~15%

---

### Pose Type 4: STANDING WITH HIP POP / CONTRAPPOSTO
**Deskripsi:** Model berdiri tapi dengan hip popped ke satu sisi.

**Body mechanics:**
- Weight on one leg, hip pushed outward
- Free leg relaxed or slightly bent
- Shoulders counter-tilted to hips
- Classic fashion pose

**Vibe:** Confident, editorial, classic
**Frekuensi di reference:** ~20%

---

### Pose Type 5: WIDE STANCE / LEGS SPREAD
**Deskripsi:** Model berdiri dengan kaki lebar, mengambil space.

**Body mechanics:**
- Feet planted wider than shoulder width
- Arms extended or on hips
- Torso upright, chest open
- Territorial, commanding

**Vibe:** Powerful, commanding, bold
**Frekuensi di reference:** ~10%

---

### Pose Type 6: HAND FRAMING FACE
**Deskripsi:** Tangan membingkai atau menyentuh wajah.

**Body mechanics:**
- One or both hands near face
- Fingers framing cheekbones, chin, or forehead
- Head tilted slightly
- Intimate, beauty-focused

**Vibe:** Intimate, beauty, editorial portrait
**Frekuensi di reference:** ~15%

---

### Pose Type 7: LEANING AGAINST SURFACE
**Deskripsi:** Model bersandar di dinding, pillar, atau permukaan.

**Body mechanics:**
- One shoulder or back against surface
- Weight shifted onto the surface
- Free leg extended or bent
- Head turned toward camera

**Vibe:** Casual, effortless, urban
**Frekuensi di reference:** ~10%

---

### Pose Type 8: WALKING / MID-STRIDE
**Deskripsi:** Model berjalan, caught mid-movement.

**Body mechanics:**
- One foot forward, one back
- Arms swinging naturally
- Torso leaning forward slightly
- Hair/clothing in motion

**Vibe:** Dynamic, candid, editorial
**Frekuensi di reference:** ~10%

---

### Pose Type 9: ONE LEG LIFTED
**Deskripsi:** Model berdiri dengan satu kaki diangkat/lifted.

**Body mechanics:**
- Standing on one leg
- Free leg lifted — knee bent or extended
- Arms positioned for balance or style
- Dynamic, sculptural

**Vibe:** Playful, dynamic, high-fashion
**Frekuensi di reference:** ~5%

---

### Pose Type 10: HEAD TILTED, LOOKING AWAY
**Deskripsi:** Model melihat menjauh dari kamera, head tilted.

**Body mechanics:**
- Head turned 30-90 degrees from camera
- Eyes looking past or away from lens
- Body at angle to camera
- Contemplative expression

**Vibe:** Contemplative, sophisticated, editorial
**Frekuensi di reference:** ~10%

---

## 🎨 VISUAL VIBES YANG ADA DI REFERENCE

### Vibe 1: CONFRONTATIONAL
- Direct eye contact
- Hands reaching toward camera
- Low or high angle for drama
- Model challenging the lens

### Vibe 2: CANDID / CAUGHT MID-MOVEMENT
- Hair blowing
- Mid-stride walking
- Slight motion blur
- Like paparazzi caught them

### Vibe 3: SCULPTURAL
- Body as form — wide stances, extended limbs
- Geometric compositions
- Body occupying space intentionally
- Fashion as architecture

### Vibe 4: RELAXED BUT INTENTIONAL
- Sitting on ground
- Leaning against walls
- Hands in pockets
- Not trying too hard but still editorial

### Vibe 5: Y2K / FUTURIST
- Fisheye/wide angle distortion
- Hands reaching toward camera
- Sunglasses, tech accessories
- Urban, digital energy

### Vibe 6: HIGH-FASHION EDITORIAL
- Clean studio or grand location
- Perfect lighting
- Sculptural poses
- Vogue/Dazed energy

---

## ✅ REKOMENDASI UNTUK PROMPT DEVETESION

### Yang HARUS Ditambahkan ke Prompt:

**1. Camera Angle Variety — WAJIB**
Prompt sekarang TIDAK specify camera angle sama sekali. AI default ke front-on eye level. Ini harus diubah:

```
CAMERA ANGLE: [pilih per look]
- High angle looking down — camera above model, fisheye energy, hands toward camera
- Low angle looking up — camera below model, model towering, sky visible
- Eye level 3/4 angle — model NOT facing camera directly, looking past lens
- Eye level front-on — direct, confrontational
- Top-down bird's eye — camera directly above, model on ground
- Ground level — camera parallel to ground, shadows visible

TIDAK BOLEH semua look pakai angle yang sama.
Distribusi yang direkomendasikan untuk 30 look:
- High angle: 6 looks (20%)
- Low angle: 4 looks (13%)
- Eye level 3/4: 6 looks (20%)
- Eye level front-on: 4 looks (13%)
- Top-down: 4 looks (13%)
- Ground level: 6 looks (20%)
```

**2. Pose Type per Look — WAJIB**
Setiap look harus punya pose direction yang spesifik, bukan cuma "keep the pose".

**3. Anti-AI Slop Enforcement — LEBIH KERAS**
```
STRICTLY FORBIDDEN:
- Perfectly symmetrical faces or bodies
- Porcelain-smooth skin with no texture
- Plastic/doll-like appearance
- Overly perfect lighting with no shadows
- Generic "fashion model" poses
- All photos shot from eye-level front view
- Identical framing across all images
```

---

## 📊 RINGKASAN DISTRIBUSI IDEAL 30 LOOK

| Pose Type | Camera Angle | Jumlah | Energi |
|-----------|-------------|--------|--------|
| Hands reaching toward camera | High angle looking down | 5 | HIGH |
| Crouching/squatting | Ground level | 4 | HIGH |
| Sitting on ground | Top-down bird's eye | 4 | MEDIUM |
| Standing with hip pop | Eye level 3/4 angle | 5 | MEDIUM |
| Wide stance / legs spread | Low angle looking up | 3 | HIGH |
| Hand framing face | Eye level front-on | 3 | LOW |
| Leaning against surface | Eye level 3/4 angle | 2 | LOW |
| Walking / mid-stride | Ground level | 2 | MEDIUM |
| One leg lifted | Eye level front-on | 1 | HIGH |
| Head tilted, looking away | Eye level 3/4 angle | 1 | LOW |

**Total: 30 looks dengan variasi maksimal.**
