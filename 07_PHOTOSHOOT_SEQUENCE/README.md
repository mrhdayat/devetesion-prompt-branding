# DEVETESION — Sistem Sequence Photoshoot

**Sistem lengkap untuk menghasilkan foto fashion sequence yang terlihat seperti difoto oleh fotografer manusia profesional di satu sesi pemotretan nyata — bukan AI.**

Semua hasil akhir terlihat seperti editorial fashion sungguhan yang bisa muncul di Vogue, Dazed, atau System Magazine.

---

## 📁 Struktur Folder

```
07_PHOTOSHOOT_SEQUENCE/
├── README.md                      ← Dokumen ini (panduan lengkap)
├── MASTER_PHOTOSHOOT_PROMPT.md    ← Prompt utama yang ditempel ke SETIAP look
├── POSE_LIBRARY.md                ← 30 pose detail, satu per look
├── SEQUENCE_SHOT_LIST.md          ← Urutan shot, framing, angle kamera per look
├── COLOR_GRADE_SYSTEM.md          ← 4 pilihan color grade untuk konsistensi semua foto
└── WEB_LAYOUT_GUIDE.md            ← Cara arrange foto jadi moodboard & layout web app
```

---

## 🎯 Tujuan Sistem Ini

Kamu punya 30 look dari Season 12 (atau season lain) yang sudah di-generate satu-satu. Masalahnya: kalau di-generate terpisah, hasilnya **tidak konsisten** — lighting beda, warna beda, style beda. Terlihat seperti random images, bukan satu photoshoot.

**Sistem ini menyelesaikan masalah itu** dengan memastikan semua 30 foto berbagi DNA visual yang sama:
- ✅ Lokasi yang sama
- ✅ Lighting yang sama
- ✅ Color grade yang sama
- ✅ Photographer eye yang sama (lens, framing, angle)
- ✅ Film treatment yang sama (grain, texture, post-production)

Hasilnya: **30 foto yang terlihat seperti satu sesi pemotretan profesional di dunia nyata.**

---

## 🔄 Alur Kerja Lengkap

### TAHAP 1: Generate 30 Look Individual

Gunakan prompt Season 12 kamu (atau season manapun) untuk menghasilkan 30 foto individual — satu per look.

**Contoh:**
- Look 01 → Racing Suit Bone White
- Look 02 → Patchwork Jacket Charcoal
- ...hingga Look 30

**Output:** 30 file gambar individual.

---

### TAHAP 2: Pilih Konfigurasi Photoshoot (Sekali Pilih, Pakai ke Semua Foto)

Sebelum mulai, kamu harus memilih **3 pengaturan** yang akan diterapkan ke SEMUA 30 foto. Jangan ganti-ganti antar foto.

#### Pilihan 1: Environment (Lokasi)
Buka `MASTER_PHOTOSHOOT_PROMPT.md` → **Part C: Environment Lock**

Pilih **SATU** dari 4 opsi:

| Opsi | Nama | Vibe |
|------|------|------|
| 1 | Flooded Concrete Cathedral | Brutalist, air, pillar beton, flash keras |
| 2 | Concrete Parking Structure | Parkiran beton, lampu neon, urban infrastructure |
| 3 | Abandoned Industrial Warehouse | Gudang tua, bata ekspos, cahaya dari jendela tinggi |
| 4 | Rooftop Parking Deck | Rooftop beton, langit mendatar, cityscape jauh |

**Rekomendasi untuk S12:** Opsi 1 — Flooded Concrete Cathedral. Cocok dengan aesthetic "Motorsport Couture".

---

#### Pilihan 2: Lighting (Pencahayaan)
Buka `MASTER_PHOTOSHOOT_PROMPT.md` → **Part E: Lighting Specification**

Pilih **SATU** dari 3 opsi:

| Opsi | Nama | Karakter |
|------|------|----------|
| A | Harsh Direct Camera Flash | Flash keras, bayangan tajam, gelap di belakang |
| B | Natural Overcast Daylight | Cahaya alami mendung, soft, rata, cool tone |
| C | Mixed Practical + Daylight | Campuran cahaya jendela + neon, split warm/cool |

**Rekomendasi untuk S12:** Opsi A — Harsh Direct Camera Flash. Memberikan energi paparazzi/confrontational yang cocok dengan motorsport.

---

#### Pilihan 3: Color Grade
Buka `COLOR_GRADE_SYSTEM.md`

Pilih **SATU** dari 4 grade:

| Grade | Nama | Karakter |
|-------|------|----------|
| 1 | Kodak Portra 400 Warm | Hangat, skin tone bagus, editorial fashion |
| 2 | Fuji Pro 400H Cool | Dingin, intelektual, refined |
| 3 | Raw Flash — No Grade | Mentah, langsung dari kamera, jujur |
| 4 | CCTV / Surveillance | Desaturasi, kompresi, lo-fi |

**Rekomendasi untuk S12:** Grade 1 — Kodak Portra 400 Warm. Paling meyakinkan sebagai foto editorial sungguhan.

---

### TAHAP 3: Retouch Setiap Look dengan Photoshoot Treatment

Untuk SETIAP dari 30 look, lakukan langkah ini:

#### Langkah per Look:

1. **Buka AI image generator** (FLOW by Google, Midjourney, DALL-E, dll)

2. **Upload foto look** yang sudah di-generate di Tahap 1

3. **Paste prompt ini secara berurutan:**

```
[PART 1] MASTER_PHOTOSHOOT_PROMPT.md (seluruh isi file, dengan pilihan environment, lighting, grade yang sudah kamu tentukan)

[PART 2] Pose yang sesuai dari POSE_LIBRARY.md (contoh: untuk Look 01, copy POSE 01 — THE STRIDE)

[PART 3] Framing & angle dari SEQUENCE_SHOT_LIST.md (contoh: untuk Look 01: "Medium-full, eye level slightly low, HIGH energy")
```

4. **Generate**

5. **Simpan hasilnya** sebagai versi photoshoot dari look tersebut

6. **Ulangi** untuk look berikutnya

#### Contoh Konkret untuk Look 01:

```
[Upload foto Look 01]

[Paste seluruh MASTER_PHOTOSHOOT_PROMPT.md dengan pilihan:]
- Environment: OPTION 1 — FLOODED CONCRETE CATHEDRAL
- Lighting: SETUP A — HARSH DIRECT CAMERA FLASH
- Grade: GRADE 1 — KODAK PORTRA 400 WARM

[Paste POSE 01 dari POSE_LIBRARY.md:]
POSE: Model walking directly toward camera with purposeful, aggressive stride.
- Weight on front foot, back foot pushing off
- Arms swinging naturally with walk — front arm slightly forward, back arm trailing
...

[Paste dari SEQUENCE_SHOT_LIST.md:]
Shot Type: Medium-full
Framing: Mid-thigh to head + 10% headroom
Camera Angle: Eye level, slightly low
Energy: HIGH

[Generate]
```

**Hasil:** Foto Look 01 yang sekarang terlihat seperti difoto profesional di flooded concrete cathedral dengan flash keras dan color grade Portra 400.

Ulangi proses yang sama untuk Look 02 sampai Look 30, masing-masing dengan pose dan framing yang berbeda tapi environment + lighting + grade yang **sama persis**.

---

### TAHAP 4: Validasi Konsistensi

Setelah semua 30 foto selesai di-generate:

1. **Buat grid 6×5** — letakkan semua 30 foto berdampingan
2. **Periksa:**
   - [ ] Semua foto punya color cast yang sama (hangat/dingin/netral)?
   - [ ] Blacks konsisten (semua sedikit lifted, atau semua crushed)?
   - [ ] Highlights behave sama (semua warm, atau semua netral)?
   - [ ] Grain terlihat dan similar di semua foto?
   - [ ] Tidak ada satu foto yang "menonjol" warnanya?
   - [ ] Skin tone konsisten di semua model?

3. **Kalau ada yang beda** → re-generate foto tersebut dengan color grade lebih eksplisit disebutkan di prompt.

---

### TAHAP 5: Arrange jadi Moodboard & Web Layout

Buka `WEB_LAYOUT_GUIDE.md`. Kamu punya beberapa pilihan layout:

#### Moodboard (untuk presentasi/internal review)

| Layout | Deskripsi | Cocok Untuk |
|--------|-----------|-------------|
| The Grid | 6 kolom × 5 baris, semua foto sama besar | Internal review, press kit |
| Hero + Grid | Look 01 full-width, sisanya grid di bawah | Landing page lookbook |
| Sequence Strip | 3 baris × 10 foto, horizontal scroll | Instagram carousel (3x carousel) |
| Editorial Spread | Ukuran foto campur — ada yang 2 kolom, ada yang 1 | Zine cetak, premium web |

#### Web App Layout (untuk website)

| Layout | Deskripsi | Cocok Untuk |
|--------|-----------|-------------|
| Collection Page | Grid 3 kolom (desktop), klik → detail | Halaman koleksi / e-commerce |
| Look Detail | Full-bleed image + info di bawah | Halaman detail per look |
| Horizontal Gallery | Scroll horizontal, satu foto per layar | Gallery experience |
| Stories Format | Full-screen, tap untuk next | Mobile stories format |
| Archive Page | List season dengan 3 thumbnail preview | Halaman arsip season sebelumnya |

Semua layout menggunakan aspect ratio **4:5** (portrait editorial standard) — sudah diatur di `MASTER_PHOTOSHOOT_PROMPT.md`.

---

## 📖 Penjelasan Detail Setiap File

### `MASTER_PHOTOSHOOT_PROMPT.md`

**Apa isinya:** Prompt utama yang mengandung:
- **Part A:** Identity Lock — wajah & outfit model tidak berubah
- **Part B:** Photographer Treatment — spesifikasi kamera, lens, film stock, anti-AI enforcement
- **Part C:** Environment Lock — 4 pilihan lokasi (pilih 1, pakai untuk semua foto)
- **Part D:** Camera Frame Specification — aspect ratio 4:5, framing conventions
- **Part E:** Lighting Specification — 3 pilihan lighting (pilih 1, pakai untuk semua foto)
- **Part F:** Post-Production / Color Grade — 4 pilihan grade (pilih 1, pakai untuk semua foto)
- **Part G:** Output Specification — standar output (harus terlihat seperti Vogue/Dazed/System)

**Kapan dipakai:** DI-TEMPER di awal setiap kali kamu mau retouch satu look jadi photoshoot.

---

### `POSE_LIBRARY.md`

**Apa isinya:** 30 pose detail — satu untuk setiap look. Setiap pose ditulis sebagai arahan fotografer profesional ke model.

Contoh:
- Pose 01: "THE STRIDE" — model berjalan agresif ke kamera
- Pose 07: "THE SLUMP" — model merosot di dinding, exhausted
- Pose 15: "THE PIVOT" — model berputar, caught mid-rotation
- Pose 30: "THE FINALE" — model diam sempurna, center, pernyataan terakhir

**Distribusi energi:**
- Look 01-05: High → Medium (opening energy)
- Look 06-10: Medium → Low (exploring the space)
- Look 11-15: Medium (middle range, variety)
- Look 16-20: Low → Medium (quiet middle)
- Look 21-25: Medium → High (building to climax)
- Look 26-30: High → STILL (finale, resolution, silence)

Ini memastikan sequence terasa seperti fashion show sungguhan — mulai kuat, explore, temukan rhythm, bangun ke klimaks, berakhir diam.

**Kapan dipakai:** Copy pose yang sesuai (Pose 01 untuk Look 01, dst) dan tempel setelah master prompt.

---

### `SEQUENCE_SHOT_LIST.md`

**Apa isinya:** Tabel shot-by-shot untuk semua 30 look, berisi:
- Shot Type (Full body, Medium-full, Medium, Close-up)
- Framing detail (berapa % headroom, cut point di mana)
- Camera Angle (Eye level, slightly low, dead-on, 45°, perpendicular)
- Energy level (HIGH, MEDIUM, LOW, STILL)
- Notes (konteks tambahan per shot)

Juga ada:
- Master Camera Specs (lens 80mm, aperture f/4-5.6, ISO 400, dll)
- Sequence Flow — arc emosional dari look 01 sampai 30
- Framing Reference (diagram visual untuk setiap shot type)
- Camera Angle Reference (penjelasan setiap angle)

**Kapan dipakai:** Baca framing & angle untuk look yang sedang kamu kerjakan, tempel setelah pose.

---

### `COLOR_GRADE_SYSTEM.md`

**Apa isinya:** 4 color grade lengkap dengan parameter teknis:
- Color temperature, tint, contrast curve
- Saturation per channel (reds, oranges, yellows, greens, blues, purples)
- Grain pattern (amount, size, roughness)
- Sharpening settings
- Vignette amount

Juga ada:
- Perbandingan antar grade dalam tabel
- Cara apply di AI generation vs post-processing
- Consistency checklist
- Rekomendasi grade untuk S12

**Kapan dipakai:** Pilih grade di awal, baca parameter detailnya, masukkan ke prompt.

---

### `WEB_LAYOUT_GUIDE.md`

**Apa isinya:**
- 4 moodboard layout (Grid, Hero+Grid, Sequence Strip, Editorial Spread)
- 5 web app layout (Collection Page, Look Detail, Horizontal Gallery, Stories, Archive)
- Responsive behavior (desktop, tablet, mobile)
- Image optimization specs (WebP, sizes, responsive markup)
- CSS layout examples pakai Tailwind CSS
- Lazy loading strategy

**Kapan dipakai:** Setelah semua 30 foto selesai, gunakan guide ini untuk arrange jadi moodboard atau web layout.

---

## ⚠️ Aturan Penting

### JANGAN Lakukan Ini:
- ❌ Ganti environment antar foto — semua foto harus satu lokasi
- ❌ Ganti lighting antar foto — semua foto harus satu lighting setup
- ❌ Ganti color grade antar foto — ini yang bikin sequence konsisten
- ❌ Gunakan pose yang sama untuk banyak look — setiap look harus beda pose
- ❌ Skip identity lock — tanpa ini, AI akan ubah wajah/outfit model

### HARUS Lakukan Ini:
- ✅ Pilih environment, lighting, grade SEKALI di awal
- ✅ Pakai konfigurasi yang sama untuk SEMUA 30 foto
- ✅ Ganti pose dan framing per look (sesuai library & shot list)
- ✅ Validasi konsistensi setelah semua 30 foto selesai
- ✅ Re-generate foto yang warnanya tidak match

---

## 🔧 Tips Tambahan

### Kalau Hasil Terlihat Terlalu "AI"
- Tambahkan penekanan di prompt: "This must NOT look AI-generated. It must pass as a real photograph from a real editorial fashion shoot."
- Pastikan film grain disebutkan eksplisit
- Pastikan skin texture disebutkan: "real skin texture — pores, fine hairs, micro-variation visible"
- Kalau pakai FLOW/Midjourney, tambahkan parameter realism: `--v 6 --style raw --s 50` (Midjourney)

### Kalau Warna Tidak Konsisten
- Sebutkan color grade LEBIH eksplisit di prompt
- Tambahkan: "This image must have the EXACT same color grading as all other images in this sequence: [deskripsikan grade]"
- Batch-compare semua foto dalam grid — yang menonjol harus di-re-generate

### Kalau Pose Tidak Terbaca
- Pastikan pose deskripsi cukup detail — kalau AI tidak mengikuti, tambahkan konteks visual
- Contoh: alih-alih "model leaning", tulis "model leaning against a concrete pillar, right shoulder making contact, weight entirely on right side, left leg extended"

---

## 📊 Ringkasan Cepat

| Tahap | Aksi | File yang Dipakai |
|-------|------|-------------------|
| 1 | Generate 30 look individual | Prompt Season 12 kamu |
| 2 | Pilih environment + lighting + grade | MASTER_PHOTOSHOOT_PROMPT.md, COLOR_GRADE_SYSTEM.md |
| 3 | Retouch setiap look (30x) | MASTER + POSE_LIBRARY + SEQUENCE_SHOT_LIST |
| 4 | Validasi konsistensi | COLOR_GRADE_SYSTEM.md (consistency checklist) |
| 5 | Arrange jadi layout | WEB_LAYOUT_GUIDE.md |

---

## 🎬 Contoh Workflow Lengkap (Look 01)

```
1. Generate Look 01 dari prompt Season 12 kamu
   → Dapat foto: model dalam racing suit bone white

2. Buka AI image generator (FLOW/Midjourney/DALL-E)

3. Upload foto Look 01

4. Paste prompt:

   [Seluruh MASTER_PHOTOSHOOT_PROMPT.md dengan:]
   - Environment: OPTION 1 (Flooded Concrete Cathedral)
   - Lighting: SETUP A (Harsh Direct Camera Flash)
   - Grade: GRADE 1 (Kodak Portra 400 Warm)

   [Pose 01 dari POSE_LIBRARY.md:]
   "POSE: Model walking directly toward camera with purposeful, aggressive stride..."

   [Shot info dari SEQUENCE_SHOT_LIST.md:]
   "Shot Type: Medium-full | Framing: Mid-thigh to head + 10% headroom | Angle: Eye level, slightly low"

5. Generate
   → Dapat foto: model dalam racing suit, berjalan agresif di flooded concrete cathedral,
     dengan flash keras, color grade Portra 400, terlihat seperti Vogue editorial

6. Simpan sebagai "S12_Look_01_Photoshoot.png"

7. Ulangi untuk Look 02-30
```

Setelah 30 foto selesai → arrange pakai layout dari WEB_LAYOUT_GUIDE.md.

---

**Sistem ini dirancang untuk menghasilkan satu hal:**
**30 foto yang terlihat seperti satu sesi pemotretan fashion profesional di dunia nyata.**

**Bukan 30 gambar AI yang berbeda satu sama lain.**

DEVETƎSION. Built, not born.
