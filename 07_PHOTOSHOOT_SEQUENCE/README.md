# DEVETESION — Sistem Sequence Photoshoot

**Sistem lengkap untuk menghasilkan foto fashion sequence yang terlihat seperti difoto oleh fotografer manusia profesional di satu sesi pemotretan nyata — bukan AI.**

Semua hasil akhir terlihat seperti editorial fashion sungguhan yang bisa muncul di Vogue, Dazed, atau System Magazine.

---

## 📁 Struktur Folder

```
07_PHOTOSHOOT_SEQUENCE/
├── README.md                      ← Dokumen ini (panduan lengkap)
├── MASTER_PHOTOSHOOT_PROMPT.md    ← SATU prompt utama — Season Config + prompt lengkap
├── POSE_ANGLE_LIBRARY_30.md       ← 30 pose dengan camera angle spesifik (BERDASARKAN ANALISIS 43 FOTO EDITORIAL)
├── POSE_ANGLE_ANALYSIS.md         ← Analisis lengkap 43 foto inspo-pose: kenapa AI slop, 6 camera angle, 10 pose types
├── POSE_LIBRARY.md                ← 30 pose detail, satu per look (versi lama — lihat POSE_ANGLE_LIBRARY_30.md yang lebih baru)
├── SEQUENCE_SHOT_LIST.md          ← Urutan shot, framing, angle kamera per look (referensi)
├── COLOR_GRADE_SYSTEM.md          ← Referensi color grade (Portra 400, Fuji Cool, Raw Flash)
└── WEB_LAYOUT_GUIDE.md            ← Cara arrange foto jadi moodboard & layout web app
```

---

## 🎯 Tujuan Sistem Ini

Kamu punya 30 look dari satu season yang sudah di-generate satu-satu. Masalahnya: kalau di-generate terpisah, hasilnya **tidak konsisten** — lighting beda, warna beda, style beda. Dan yang lebih parah: **semua foto dari angle yang sama (front view eye level)** — terlihat sangat "AI slop".

**Sistem ini menyelesaikan masalah itu** dengan memastikan semua 30 foto berbagi DNA visual yang sama TAPI tetap bervariasi:
- ✅ AI otomatis pilih lokasi yang cocok sama outfit (atau satu lokasi untuk semua — kamu yang tentukan)
- ✅ **Camera angle bervariasi** — 6 jenis angle berbeda tersebar di 30 look (INI YANG MENGHILANGKAN AI SLOP)
- ✅ Pose berbeda per look — 30 pose spesifik berdasarkan analisis 43 foto editorial asli
- ✅ Color grade konsisten dalam 1 season (tapi beda season bisa beda)
- ✅ Lighting konsisten dalam 1 season (tapi beda season bisa beda)
- ✅ Anti-AI enforcement — explicit forbid karakteristik AI slop

Hasilnya: **30 foto yang terlihat seperti satu sesi pemotretan profesional di dunia nyata — bukan AI.**

---

## 🔍 Analisis dari 43 Foto Editorial (inspo-pose/)

Saya sudah analisa 43 foto editorial fashion dari folder `inspo-pose/`. Temuan utama:

### Kenapa Hasil Generate Sebelumnya Terlihat Jelek?

**Masalah:** Prompt tidak mengontrol camera angle. AI default ke **eye-level front view** untuk semua foto.

**Hasil:** Semua foto terlihat sama — front view, eye level, pose mirip — yang bikin sangat "AI slop".

### Yang Ada di Editorial Asli:

| Camera Angle | Frekuensi di Reference | Vibe |
|-------------|----------------------|------|
| High angle (looking down) | ~25% | Dynamic, Y2K, hands reaching |
| Low angle (looking up) | ~15% | Powerful, towering, architectural |
| Eye level 3/4 angle | ~20% | Contemplative, editorial |
| Eye level front-on | ~15% | Confrontational, portrait |
| Top-down bird's eye | ~10% | Sculptural, geometric |
| Ground level | ~15% | Cinematic, urban, raw |

**Kesimpulan:** Hanya 15% yang front-on eye level. **85% punya angle yang bervariasi.**

### Ciri AI Slop yang HARUS Dihindari:

- Kulit plastik tanpa tekstur
- Simetri sempurna di wajah dan tubuh
- Lighting terlalu perfect tanpa shadow natural
- Semua foto dari angle yang sama
- Pose generik "fashion model"
- Warna over-saturated

### Ciri Foto Editorial Asli:

- Skin texture terlihat (pores, fine hairs, micro-variation)
- Slight asymmetry di wajah dan pose
- Natural shadows dan imperfections
- Camera angle bervariasi
- Pose yang intentional dan editorial
- Warna true to real-world capture

---

## 🔄 Alur Kerja — Season Config + Generate

### Langkah 0: Isi Season Config (Sekali Per Season)

Di bagian paling atas `MASTER_PHOTOSHOOT_PROMPT.md`, ada **Season Config Block**:

```
SEASON: [nama season]
COLOR GRADE: [pilih 1]
LIGHTING: [pilih 1]
LOCATION MODE: [pilih 1]
POSE MODE: [pilih 1]
CAMERA ANGLE MODE: [pilih 1] ← INI YANG BARU
```

**Color Grade (pilih 1 per season):**

| Grade | Vibe | Cocok Untuk |
|-------|------|-------------|
| Portra 400 Warm | Hangat, editorial, skin tone bagus | Season yang mau terlihat expensive, luxurious |
| Fuji 400H Cool | Dingin, intelektual, refined | Season yang mau terlihat minimalist, detached |
| Raw Flash No Grade | Mentah, straight out of camera | Season yang mau terlihat raw, confrontational |

**Lighting (pilih 1 per season):**

| Lighting | Karakter |
|----------|----------|
| Natural Match | AI sesuaikan lighting dengan lokasi — indoor = daylight soft, outdoor = overcast |
| Harsh Flash | Direct camera flash ke SEMUA foto — energy paparazzi, raw |

**Location Mode (pilih 1 per season):**

| Mode | Hasil |
|------|-------|
| Auto | AI pilih lokasi berbeda per look berdasarkan outfit |
| Force | Satu lokasi untuk semua 30 look — seperti one-location photoshoot |

**Pose Mode (pilih 1 per season):**

| Mode | Hasil |
|------|-------|
| Keep | Pose mengikuti foto yang di-upload |
| Direction | Kamu tentukan pose per look dari POSE_ANGLE_LIBRARY_30.md |

**Camera Angle Mode (WAJIB — pilih 1 per season):**

| Mode | Hasil |
|------|-------|
| **Varied** ← REKOMENDASI | 6 jenis angle berbeda tersebar di 30 look: 6 high angle, 4 low angle, 8 eye-level 3/4, 6 front-on, 4 top-down, 2 ground level |
| Fixed | Semua 30 look pakai angle yang sama — monoton, tidak direkomendasikan |

**Contoh config per season:**

| Season | Grade | Lighting | Location | Pose | Camera Angle | Hasil |
|--------|-------|----------|----------|------|-------------|-------|
| S12 Motorsport Couture | Portra 400 Warm | Natural Match | Force: Rooftop | Direction | **Varied** | Satu lokasi, 30 pose + 6 angle berbeda — seperti real photoshoot |
| S13 Street Utility | Raw Flash | Harsh Flash | Auto | Keep | **Varied** | Lokasi beda, pose ikut foto, 6 angle berbeda, vibe raw |
| S14 Minimal Tailoring | Fuji Cool | Natural Match | Force: Gallery | Direction | **Varied** | Satu lokasi gallery, 30 pose + 6 angle berbeda |

**Dalam 1 season** → semua foto konsisten color grade + lighting.
**Antar season** → bisa beda vibe total.
**Dalam 1 season** → pose DAN camera angle BERBEDA per look (ini yang menghilangkan AI slop).

---

### Langkah 1: Upload 1 Foto Look

Buka AI image generator (FLOW by Google, Midjourney, DALL-E, dll). Upload 1 foto look yang sudah kamu generate dari Season yang sedang dikerjakan.

### Langkah 2: Paste Prompt

Copy **SELURUH isi** `MASTER_PHOTOSHOOT_PROMPT.md` (dari Season Config sampai akhir). Paste di prompt generator. **Jangan ganti apapun** kecuali Season Config, Forced Location, Pose Direction, dan Camera Angle.

### Langkah 3: Generate

Klik generate. Hasilnya: foto yang sama, tapi sekarang terlihat seperti difoto profesional dengan camera angle yang spesifik.

**Ulangi untuk 30 look.** Setiap look punya pose DAN camera angle berbeda.

---

## 📸 Distribusi 30 Look — Pose + Camera Angle

| Look Range | Camera Angle | Jumlah | Pose Examples | Energi |
|------------|-------------|--------|---------------|--------|
| 01-06 | High angle looking down | 6 | Hands reaching, crouching | HIGH |
| 07-10 | Low angle looking up | 4 | Wide stance, one leg lifted | HIGH |
| 11-18 | Eye level 3/4 angle | 8 | Hip pop, contrapposto, leaning | MEDIUM-LOW |
| 19-24 | Eye level front-on | 6 | Hand framing, standing | LOW-MEDIUM |
| 25-28 | Top-down bird's eye | 4 | Sitting, lying on ground | MEDIUM |
| 29-30 | Ground level | 2 | Walking lateral, crouching | MEDIUM-HIGH |

**Total: 30 looks, 6 camera angle berbeda, 30 pose berbeda.**

---

## 📋 Penjelasan Detail Setiap File

### `MASTER_PHOTOSHOOT_PROMPT.md`
**Apa isinya:** SATU prompt lengkap yang mengandung:
- Season Config — diisi sekali per season (color grade + lighting + location mode + pose mode + camera angle mode)
- Anti-AI Slop Enforcement — explicit forbid karakteristik AI
- Photographer Treatment — spesifikasi kamera, lens, film
- Camera Angle Application — 6 jenis angle dengan distribusi 30 look
- Location Application — Auto atau Force
- Pose Application — Keep atau Direction
- Color Grade + Lighting — sesuai Season Config

**Kapan dipakai:** DI-TEMPER seluruhnya setiap kali mau retouch 1 look jadi photoshoot.

### `POSE_ANGLE_LIBRARY_30.md`
**Apa isinya:** 30 pose detail — satu untuk setiap look. Setiap pose dilengkapi dengan:
- Camera angle spesifik (high angle, low angle, 3/4, front-on, top-down, ground level)
- Body mechanics detail (posisi kaki, tangan, head, torso)
- Key details (apa yang harus terlihat jelas)
- Energy level (HIGH, MEDIUM, LOW, STILL)

**Kapan dipakai:** Copy pose yang sesuai per look dan tempel ke prompt.

### `POSE_ANGLE_ANALYSIS.md`
**Apa isinya:** Analisis lengkap 43 foto editorial dari folder `inspo-pose/`:
- Kenapa hasil generate sebelumnya jelek
- 6 camera angle detail dengan frekuensi di reference
- 10 pose types yang ada di editorial asli
- 6 visual vibes
- Rekomendasi untuk prompt

**Kapan dipakai:** Baca untuk memahami kenapa camera angle penting dan bagaimana editorial asli berbeda dari AI slop.

### `POSE_LIBRARY.md`
**Apa isinya:** 30 pose detail versi lama (tanpa camera angle spesifik).

**Kapan dipakai:** Referensi tambahan. Gunakan `POSE_ANGLE_LIBRARY_30.md` yang lebih baru dan lengkap.

### `SEQUENCE_SHOT_LIST.md`
**Apa isinya:** Tabel shot-by-shot — framing, camera angle, energy level untuk setiap look.

**Kapan dipakai:** Referensi kalau kamu mau tahu shot type dan angle yang direkomendasikan per look.

### `COLOR_GRADE_SYSTEM.md`
**Apa isinya:** 3 color grade lengkap dengan parameter teknis + perbandingan.

**Kapan dipakai:** Kalau kamu mau tau detail teknis setiap grade (bukan wajib — Season Config sudah cukup).

### `WEB_LAYOUT_GUIDE.md`
**Apa isinya:** 4 moodboard layout + 5 web app layout + CSS examples + responsive behavior.

**Kapan dipakai:** Setelah semua 30 foto selesai, pakai guide ini untuk arrange jadi moodboard atau layout web.

---

## ⚠️ Aturan Penting

### JANGAN Lakukan Ini:
- ❌ Ganti Season Config di tengah season — semua 30 look harus sama config-nya
- ❌ Pakai CAMERA ANGLE MODE "Fixed" — semua foto akan angle sama = monoton = AI slop
- ❌ Skip anti-AI enforcement — tanpa ini, AI akan kasih kulit plastik, simetri sempurna
- ❌ Upload gambar yang bukan look fashion — prompt ini khusus fashion photography

### HARUS Lakukan Ini:
- ✅ Isi Season Config SEKALI di awal sebelum generate look pertama
- ✅ Set CAMERA ANGLE MODE: "Varied" — WAJIB untuk menghindari AI slop
- ✅ Pakai SELURUH prompt — jangan potong-potong
- ✅ Upload look yang sudah di-generate sebelumnya (bukan foto random)
- ✅ Gunakan pose dari POSE_ANGLE_LIBRARY_30.md — sudah include camera angle
- ✅ Validasi hasil — pastikan tidak terlihat AI-generated

---

## 🔧 Tips Tambahan

### Kalau Hasil Masih Terlihat "AI Slop"
- Pastikan CAMERA ANGLE MODE: "Varied" — ini paling penting
- Pastikan prompt tidak diubah — terutama bagian "ANTI-AI SLOP ENFORCEMENT"
- Tambahkan di akhir prompt: "This must NOT look AI-generated. It must pass as a real photograph from a real editorial fashion shoot."
- Pastikan camera angle spesifik disebutkan di setiap generate (jangan biarkan AI default ke front view)
- Kalau pakai Midjourney: tambahkan `--v 6 --style raw --s 50`

### Kalau Lokasi yang Dipilih AI Tidak Cocok
- AI mungkin salah baca outfit. Coba deskripsikan outfit lebih jelas di bagian atas prompt:
  "The outfit is: [deskripsi singkat outfit]"
- Atau set LOCATION MODE: Force dengan lokasi yang kamu tentukan sendiri

### Mau Semua Look di Season yang Sama Lokasinya
- Set LOCATION MODE: Force
- Tulis deskripsi lokasi detail di bagian "FORCED LOCATION"
- Semua 30 foto akan di lokasi yang sama, tapi pose dan camera angle berbeda

### Camera Angle Tidak Bervariasi
- Pastikan CAMERA ANGLE MODE: "Varied"
- Di setiap generate, sebutkan camera angle spesifik: "Camera angle for THIS look: High angle looking down at 60 degrees"
- Jangan biarkan AI memilih sendiri — AI akan default ke front view

---

## 📊 Ringkasan Cepat

| Langkah | Aksi | File yang Dipakai |
|---------|------|-------------------|
| 0 | Isi Season Config (sekali per season) | MASTER_PHOTOSHOOT_PROMPT.md |
| 1 | Upload 1 look foto | Foto dari Season kamu |
| 2 | Paste seluruh prompt | MASTER_PHOTOSHOOT_PROMPT.md |
| 3 | Tambahkan pose + camera angle | POSE_ANGLE_LIBRARY_30.md |
| 4 | Generate | AI image generator |
| 5 | Ulangi 30x | — |
| 6 | Arrange jadi layout | WEB_LAYOUT_GUIDE.md |

---

## 🎬 Contoh Workflow Lengkap

### Season 12 — Portra 400 Warm + Natural Match + Force Location + Varied Angles

```
1. Isi Season Config di MASTER_PHOTOSHOOT_PROMPT.md:
   SEASON: S12
   COLOR GRADE: Portra 400 Warm
   LIGHTING: Natural Match
   LOCATION MODE: Force
   POSE MODE: Direction
   CAMERA ANGLE MODE: Varied

2. Tentukan lokasi (dipakai untuk semua 30 look):
   FORCED LOCATION: A multi-level concrete parking garage with exposed ceiling pipes,
   fluorescent light fixtures, painted parking lines on sloped concrete floor, concrete
   pillars at regular intervals. Daylight enters from the open edge of the structure.

3. Buka FLOW by Google (atau Midjourney/DALL-E)

4. Upload foto Look 01 (Racing Suit Bone White)

5. Paste SELURUH isi MASTER_PHOTOSHOOT_PROMPT.md

6. Tambahkan di bagian pose + camera angle:
   POSE DIRECTION: Model reaching both hands toward the camera lens, fingers spread.
   Body crouching slightly, knees bent, torso leaning forward.
   Camera angle for THIS look: High angle looking down at approximately 60 degrees.
   Camera positioned above the model looking down. Slight wide-angle/fisheye distortion.

7. Generate
   → Hasil: foto racing suit di rooftop beton, camera dari atas (high angle),
     model reaching hands toward camera, tone hangat Portra 400,
     terlihat seperti Vogue editorial

8. Simpan sebagai "S12_Look_01_Photoshoot.png"

9. Ulangi untuk Look 02-30:
   - Config SAMA
   - Lokasi SAMA
   - Pose BERBEDA (dari POSE_ANGLE_LIBRARY_30.md)
   - Camera angle BERBEDA (dari distribusi: high angle, low angle, 3/4, front-on, top-down, ground level)
```

**Hasil akhir:** 30 foto di lokasi yang sama, tapi setiap foto punya pose DAN camera angle berbeda — persis seperti real photoshoot oleh fotografer profesional.

---

## 💡 Perbedaan dengan 05_PHOTOSHOOT_OPTIONS

| | `05_PHOTOSHOOT_OPTIONS` | `07_PHOTOSHOOT_SEQUENCE` |
|---|------------------------|---------------------------|
| **Tujuan** | Generate foto GROUP dari multi-model | Generate foto INDIVIDUAL per look |
| **Lokasi** | Kamu pilih manual (studio/outdoor/indoor) | AI otomatis pilih berdasarkan outfit (atau Force satu lokasi) |
| **Jumlah model** | Multi-model (2-6 orang) | 1 model per foto |
| **Camera angle** | Tidak ada kontrol | 6 jenis angle berbeda (Varied mode) |
| **Pose** | Tidak ada kontrol | 30 pose spesifik dari POSE_ANGLE_LIBRARY_30.md |
| **Output** | 1 foto group | 30 foto individual sequence |
| **Kapan dipakai** | Awal — generate look pertama kali | Kedua — retouch look jadi photoshoot quality |

**Workflow lengkap:**
```
Season prompts → generate 30 look individual
→ 07_PHOTOSHOOT_SEQUENCE → retouch 30 look jadi photoshoot quality
   (dengan Season Config + pose library + camera angle varied)
→ WEB_LAYOUT_GUIDE → arrange jadi moodboard / web layout
```

---

**Sistem ini dirancang untuk menghasilkan satu hal:**
**30 foto yang terlihat seperti satu sesi pemotretan fashion profesional di dunia nyata.**

**Bukan 30 gambar AI yang berbeda satu sama lain.**

DEVETƎSION. Built, not born.
