# DEVETESION — Sistem Sequence Photoshoot

**Sistem lengkap untuk menghasilkan foto fashion sequence yang terlihat seperti difoto oleh fotografer manusia profesional di satu sesi pemotretan nyata — bukan AI.**

Semua hasil akhir terlihat seperti editorial fashion sungguhan yang bisa muncul di Vogue, Dazed, atau System Magazine.

---

## 📁 Struktur Folder

```
07_PHOTOSHOOT_SEQUENCE/
├── README.md                      ← Dokumen ini (panduan lengkap)
├── MASTER_PHOTOSHOOT_PROMPT.md    ← SATU prompt utama — upload 1 look, paste, generate
├── POSE_LIBRARY.md                ← 30 pose detail, satu per look (opsional)
├── SEQUENCE_SHOT_LIST.md          ← Urutan shot, framing, angle kamera per look (opsional)
├── COLOR_GRADE_SYSTEM.md          ← Referensi color grade (default: Portra 400 Warm)
└── WEB_LAYOUT_GUIDE.md            ← Cara arrange foto jadi moodboard & layout web app
```

---

## 🎯 Tujuan Sistem Ini

Kamu punya 30 look dari Season 12 (atau season lain) yang sudah di-generate satu-satu. Masalahnya: kalau di-generate terpisah, hasilnya **tidak konsisten** — lighting beda, warna beda, style beda. Terlihat seperti random images, bukan satu photoshoot.

**Sistem ini menyelesaikan masalah itu** dengan memastikan semua 30 foto berbagi DNA visual yang sama:
- ✅ AI otomatis pilih lokasi yang cocok sama outfit (indoor / outdoor)
- ✅ Lighting natural sesuai lokasi
- ✅ Color grade konsisten (Portra 400 Warm)
- ✅ Photographer eye yang sama (medium format, film grain, real skin texture)
- ✅ Anti-AI enforcement — tidak boleh terlihat seperti AI

Hasilnya: **30 foto yang terlihat seperti satu sesi pemotretan profesional di dunia nyata.**

---

## 🔄 Alur Kerja — SUPER SIMPLE (3 Langkah)

### Langkah 1: Upload 1 Foto Look
Buka AI image generator (FLOW by Google, Midjourney, DALL-E, dll). Upload 1 foto look yang sudah kamu generate dari Season 12.

### Langkah 2: Paste Prompt
Copy **SELURUH isi** `MASTER_PHOTOSHOOT_PROMPT.md` (dari "STRICT IMAGE PRESERVATION MODE" sampai akhir). Paste di prompt generator. **Jangan ganti apapun.**

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

## 🎨 Color Grade & Lighting

**Default (otomatis):**
- Color Grade: **Kodak Portra 400 Warm** — hangat, skin tone bagus, editorial
- Lighting: **Natural sesuai lokasi** — kalau indoor + jendela = daylight soft, kalau outdoor = overcast, kalau parking garage = fluorescent

**Mau ganti color grade?** Buka `COLOR_GRADE_SYSTEM.md` — ada 3 pilihan:
1. Kodak Portra 400 Warm (default, recommended)
2. Fuji Pro 400H Cool (dingin, intelektual)
3. Raw Flash — No Grade (mentah, straight out of camera)

Kalau mau ganti, edit bagian "LIGHTING AND COLOR GRADE" di `MASTER_PHOTOSHOOT_PROMPT.md`.

---

## 📋 Penjelasan Detail Setiap File

### `MASTER_PHOTOSHOOT_PROMPT.md`
**Apa isinya:** SATU prompt lengkap yang mengandung:
- Identity Lock — wajah & outfit tidak berubah
- Photographer Treatment — spesifikasi kamera, lens, film, anti-AI enforcement
- Autonomous Environment Selection — AI analisa outfit, pilih lokasi yang cocok
- Lighting & Color Grade — Portra 400 warm, natural lighting
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

**Kapan dipakai:** Kalau kamu mau ganti color grade dari default Portra 400 Warm. Baca, pilih grade, copy parameternya ke master prompt.

### `WEB_LAYOUT_GUIDE.md`
**Apa isinya:** 4 moodboard layout + 5 web app layout + CSS examples + responsive behavior.

**Kapan dipakai:** Setelah semua 30 foto selesai, pakai guide ini untuk arrange jadi moodboard atau layout web.

---

## ⚠️ Aturan Penting

### JANGAN Lakukan Ini:
- ❌ Edit prompt secara sembarangan — pakai apa adanya
- ❌ Ganti color grade antar foto — semua foto harus sama
- ❌ Skip identity lock — tanpa ini, AI akan ubah wajah/outfit model
- ❌ Upload gambar yang bukan look fashion — prompt ini khusus fashion photography

### HARUS Lakukan Ini:
- ✅ Pakai SELURUH prompt — jangan potong-potong
- ✅ Upload look yang sudah di-generate sebelumnya (bukan foto random)
- ✅ Validasi hasil — pastikan tidak terlihat AI-generated
- ✅ Re-generate kalau ada foto yang warnanya tidak match

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

### Kalau Warna Tidak Konsistensi Antar Foto
- Pastikan bagian "LIGHTING AND COLOR GRADE" tidak diubah
- Batch-compare semua foto dalam grid — yang menonjol harus di-re-generate
- Kalau perlu, tambahkan lebih eksplisit: "This image must have the EXACT same color grading as all other images: Kodak Portra 400 warm"

---

## 📊 Ringkasan Cepat

| Langkah | Aksi | File yang Dipakai |
|---------|------|-------------------|
| 1 | Upload 1 look foto | Foto dari Season 12 |
| 2 | Paste seluruh prompt | MASTER_PHOTOSHOOT_PROMPT.md |
| 3 | Generate | AI image generator |
| 4 | Ulangi 30x | — |
| 5 | Arrange jadi layout | WEB_LAYOUT_GUIDE.md |

---

## 🎬 Contoh Workflow Lengkap (Look 01)

```
1. Kamu sudah punya foto Look 01 dari Season 12:
   → Model dalam racing suit bone white

2. Buka FLOW by Google (atau Midjourney/DALL-E)

3. Upload foto Look 01

4. Paste SELURUH isi MASTER_PHOTOSHOOT_PROMPT.md
   → Jangan ganti apapun
   → AI otomatis analisa: "ini racing suit" → pilih "rooftop parking deck"

5. Generate
   → Hasil: model dalam racing suit di rooftop beton, langit mendatar,
     color grade Portra 400 warm, terlihat seperti Vogue editorial

6. Simpan sebagai "S12_Look_01_Photoshoot.png"

7. Ulangi untuk Look 02 sampai 30
```

Setelah 30 foto selesai → arrange pakai layout dari WEB_LAYOUT_GUIDE.md.

---

## 💡 Perbedaan dengan 05_PHOTOSHOOT_OPTIONS

| | `05_PHOTOSHOOT_OPTIONS` | `07_PHOTOSHOOT_SEQUENCE` |
|---|------------------------|---------------------------|
| **Tujuan** | Generate foto GROUP dari multi-model | Generate foto INDIVIDUAL per look |
| **Lokasi** | Kamu pilih manual (studio/outdoor/indoor) | AI otomatis pilih berdasarkan outfit |
| **Jumlah model** | Multi-model (2-6 orang) | 1 model per foto |
| **Output** | 1 foto group | 30 foto individual sequence |
| **Kapan dipakai** | Awal — generate look pertama kali | Kedua — retouch look jadi photoshoot |

**Workflow lengkap:**
```
Season 12 prompts → generate 30 look individual
→ 07_PHOTOSHOOT_SEQUENCE → retouch 30 look jadi photoshoot quality
→ WEB_LAYOUT_GUIDE → arrange jadi moodboard / web layout
```

---

**Sistem ini dirancang untuk menghasilkan satu hal:**
**30 foto yang terlihat seperti satu sesi pemotretan fashion profesional di dunia nyata.**

**Bukan 30 gambar AI yang berbeda satu sama lain.**

DEVETƎSION. Built, not born.
