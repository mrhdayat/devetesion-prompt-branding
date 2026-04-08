# DEVETESION — Sistem Sequence Photoshoot

**Sistem lengkap untuk menghasilkan foto fashion sequence yang terlihat seperti difoto oleh fotografer manusia profesional di satu sesi pemotretan nyata — bukan AI.**

Semua hasil akhir terlihat seperti editorial fashion sungguhan yang bisa muncul di Vogue, Dazed, atau System Magazine.

---

## 📁 Struktur Folder

```
07_PHOTOSHOOT_SEQUENCE/
├── README.md                      ← Dokumen ini (panduan lengkap)
├── MASTER_PHOTOSHOOT_PROMPT.md    ← SATU prompt utama — Season Config + prompt lengkap
├── POSE_LIBRARY.md                ← 30 pose detail, satu per look (opsional)
├── SEQUENCE_SHOT_LIST.md          ← Urutan shot, framing, angle kamera per look (opsional)
├── COLOR_GRADE_SYSTEM.md          ← Referensi detail color grade (opsional)
└── WEB_LAYOUT_GUIDE.md            ← Cara arrange foto jadi moodboard & layout web app
```

---

## 🎯 Tujuan Sistem Ini

Kamu punya 30 look dari satu season yang sudah di-generate satu-satu. Masalahnya: kalau di-generate terpisah, hasilnya **tidak konsisten** — lighting beda, warna beda, style beda. Terlihat seperti random images, bukan satu photoshoot.

**Sistem ini menyelesaikan masalah itu** dengan memastikan semua 30 foto berbagi DNA visual yang sama:
- ✅ AI otomatis pilih lokasi yang cocok sama outfit (indoor / outdoor)
- ✅ Color grade konsisten dalam 1 season (tapi beda season bisa beda)
- ✅ Lighting konsisten dalam 1 season (tapi beda season bisa beda)
- ✅ Photographer eye yang sama (medium format, film grain, real skin texture)
- ✅ Anti-AI enforcement — tidak boleh terlihat seperti AI

Hasilnya: **30 foto yang terlihat seperti satu sesi pemotretan profesional di dunia nyata.**

---

## 🔄 Alur Kerja — Season Config + Generate

### Langkah 0: Isi Season Config (Sekali Per Season)

Di bagian paling atas `MASTER_PHOTOSHOOT_PROMPT.md`, ada **Season Config Block**:

```
SEASON: [nama season]
COLOR GRADE: [pilih 1]
LIGHTING: [pilih 1]
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

**Contoh config per season:**

| Season | Color Grade | Lighting | Hasil |
|--------|------------|----------|-------|
| S12 Motorsport Couture | Portra 400 Warm | Natural Match | Expensive, editorial, hangat |
| S13 Street Utility | Raw Flash No Grade | Harsh Flash | Raw, confrontational, documentary |
| S14 Minimal Tailoring | Fuji 400H Cool | Natural Match | Dingin, intelektual, refined |

**Dalam 1 season** → semua foto konsisten.
**Antar season** → bisa beda vibe total.

---

### Langkah 1: Upload 1 Foto Look

Buka AI image generator (FLOW by Google, Midjourney, DALL-E, dll). Upload 1 foto look yang sudah kamu generate dari Season yang sedang dikerjakan.

### Langkah 2: Paste Prompt

Copy **SELURUH isi** `MASTER_PHOTOSHOOT_PROMPT.md` (dari Season Config sampai akhir). Paste di prompt generator. **Jangan ganti apapun** kecuali Season Config.

### Langkah 3: Generate

Klik generate. Hasilnya: foto yang sama, tapi sekarang terlihat seperti difoto profesional di lokasi real-world yang cocok dengan outfit.

**Ulangi untuk 30 look.** Selesai.

---

## 🤖 Cara AI Memilih Lokasi

AI akan **otomatis analisa outfit** dan pilih lokasi yang masuk akal:

| Jenis Outfit | Lokasi yang Akan Dipilih AI |
|--------------|---------------------------|
| Racing suit, techwear, streetwear | Urban infrastructure — rooftop parking, underpass, loading dock |
| Tailoring, formal, minimalist | Interior arsitektur — gallery, hotel lobby, modernist showroom |
| Couture, avant-garde, voluminous | Grand interior — abandoned warehouse, disused theatre, vaulted hall |
| Casual, knitwear, relaxed | Lived-in interior — loft apartment, sunlit studio, conservatory |
| Outerwear, heavy coats, winter | Outdoor urban — city street, concrete plaza, harbor edge |

**Semua lokasi real-world.** Bukan fantasy, bukan sci-fi, bukan abstract void.

**Contoh:**
- Upload racing suit → AI pilih "rooftop parking deck, overcast sky, wet concrete"
- Upload tailored suit → AI pilih "modernist gallery, skylight, white walls"
- Upload draped gown → AI pilih "abandoned theatre, high ceilings, dramatic shadows"

---

## 📋 Penjelasan Detail Setiap File

### `MASTER_PHOTOSHOOT_PROMPT.md`
**Apa isinya:** SATU prompt lengkap yang mengandung:
- Season Config — diisi sekali per season (color grade + lighting)
- Identity Lock — wajah & outfit tidak berubah
- Photographer Treatment — spesifikasi kamera, lens, film, anti-AI enforcement
- Autonomous Environment Selection — AI analisa outfit, pilih lokasi yang cocok
- Color Grade Application — sesuai Season Config
- Lighting Application — sesuai Season Config
- Pose & Framing — pose tetap sama, framing 4:5 portrait
- Output Specification — harus terlihat seperti Vogue/Dazed

**Kapan dipakai:** DI-TEMPER seluruhnya setiap kali mau retouch 1 look jadi photoshoot.

### `POSE_LIBRARY.md`
**Apa isinya:** 30 pose detail — satu untuk setiap look. Ditulis sebagai arahan fotografer ke model.

**Kapan dipakai:** OPSIONAL. Kalau kamu mau generate look DENGAN pose spesifik, baca pose yang sesuai dan tambahkan deskripsi pose ke prompt sebelum generate look aslinya.

### `SEQUENCE_SHOT_LIST.md`
**Apa isinya:** Tabel shot-by-shot — framing, camera angle, energy level untuk setiap look.

**Kapan dipakai:** OPSIONAL. Referensi kalau kamu mau tahu shot type dan angle yang direkomendasikan per look.

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
- ❌ Skip identity lock — tanpa ini, AI akan ubah wajah/outfit model
- ❌ Upload gambar yang bukan look fashion — prompt ini khusus fashion photography

### HARUS Lakukan Ini:
- ✅ Isi Season Config SEKALI di awal sebelum generate look pertama
- ✅ Pakai SELURUH prompt — jangan potong-potong
- ✅ Upload look yang sudah di-generate sebelumnya (bukan foto random)
- ✅ Validasi hasil — pastikan tidak terlihat AI-generated

---

## 🔧 Tips Tambahan

### Kalau Hasil Terlihat Terlalu "AI"
- Pastikan prompt tidak diubah — terutama bagian "ANTI-AI ENFORCEMENT"
- Tambahkan di akhir prompt: "This must NOT look AI-generated. It must pass as a real photograph from a real editorial fashion shoot."
- Kalau pakai Midjourney: tambahkan `--v 6 --style raw --s 50`

### Kalau Lokasi yang Dipilih AI Tidak Cocok
- AI mungkin salah baca outfit. Coba deskripsikan outfit lebih jelas di bagian atas prompt:
  "The outfit is: [deskripsi singkat outfit]"
- Atau override manual dengan tambahkan: "IGNORE the decision tree. Use this location: [deskripsi lokasi kamu]"

### Mau Semua Look di Season yang Sama Lokasinya
- Tambahkan di Season Config: "FORCE LOCATION: [deskripsikan lokasi]"
- Atau edit bagian AUTONOMOUS ENVIRONMENT SELECTION: "IGNORE the decision tree above. ALL images must be shot in: [deskripsikan lokasi]."

---

## 📊 Ringkasan Cepat

| Langkah | Aksi | File yang Dipakai |
|---------|------|-------------------|
| 0 | Isi Season Config (sekali per season) | MASTER_PHOTOSHOOT_PROMPT.md |
| 1 | Upload 1 look foto | Foto dari Season kamu |
| 2 | Paste seluruh prompt | MASTER_PHOTOSHOOT_PROMPT.md |
| 3 | Generate | AI image generator |
| 4 | Ulangi 30x | — |
| 5 | Arrange jadi layout | WEB_LAYOUT_GUIDE.md |

---

## 🎬 Contoh Workflow Lengkap

### Season 12 — Portra 400 Warm + Natural Match

```
1. Isi Season Config di MASTER_PHOTOSHOOT_PROMPT.md:
   SEASON: S12
   COLOR GRADE: Portra 400 Warm
   LIGHTING: Natural Match

2. Buka FLOW by Google (atau Midjourney/DALL-E)

3. Upload foto Look 01 (Racing Suit Bone White)

4. Paste SELURUH isi MASTER_PHOTOSHOOT_PROMPT.md

5. Generate
   → AI analisa: "ini racing suit" → pilih "rooftop parking deck"
   → Lighting: natural overcast (Natural Match)
   → Color grade: Portra 400 warm
   → Hasil: foto racing suit di rooftop beton, langit mendatar, tone hangat,
     terlihat seperti Vogue editorial

6. Simpan sebagai "S12_Look_01_Photoshoot.png"

7. Ulangi untuk Look 02 sampai 30 — config SAMA, lokasi BEDA sesuai outfit
```

### Season 13 — Raw Flash + Harsh Flash

```
1. GANTI Season Config:
   SEASON: S13
   COLOR GRADE: Raw Flash No Grade
   LIGHTING: Harsh Flash

2. Upload foto Look 01 Season 13

3. Paste SELURUH isi MASTER_PHOTOSHOOT_PROMPT.md

4. Generate
   → AI analisa outfit → pilih lokasi
   → Lighting: HARSH FLASH (override natural, semua foto dapat flash treatment)
   → Color grade: Raw Flash (no correction, straight out of camera)
   → Hasil: raw, confrontational, seperti paparazzi photograph
   → Vibe BEDA total dari S12
```

Setelah semua 30 foto selesai → arrange pakai layout dari WEB_LAYOUT_GUIDE.md.

---

## 💡 Perbedaan dengan 05_PHOTOSHOOT_OPTIONS

| | `05_PHOTOSHOOT_OPTIONS` | `07_PHOTOSHOOT_SEQUENCE` |
|---|------------------------|---------------------------|
| **Tujuan** | Generate foto GROUP dari multi-model | Generate foto INDIVIDUAL per look |
| **Lokasi** | Kamu pilih manual (studio/outdoor/indoor) | AI otomatis pilih berdasarkan outfit |
| **Jumlah model** | Multi-model (2-6 orang) | 1 model per foto |
| **Output** | 1 foto group | 30 foto individual sequence |
| **Kapan dipakai** | Awal — generate look pertama kali | Kedua — retouch look jadi photoshoot quality |

**Workflow lengkap:**
```
Season prompts → generate 30 look individual
→ 07_PHOTOSHOOT_SEQUENCE → retouch 30 look jadi photoshoot quality (dengan Season Config)
→ WEB_LAYOUT_GUIDE → arrange jadi moodboard / web layout
```

---

**Sistem ini dirancang untuk menghasilkan satu hal:**
**30 foto yang terlihat seperti satu sesi pemotretan fashion profesional di dunia nyata.**

**Bukan 30 gambar AI yang berbeda satu sama lain.**

DEVETƎSION. Built, not born.
