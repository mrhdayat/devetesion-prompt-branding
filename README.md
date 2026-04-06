# DEVETESION Prompt Branding

Koleksi lengkap prompt AI untuk menghasilkan gambar **fashion campaign editorial** bergaya high-end luxury runway. Dirancang khusus untuk **Midjourney**, **FLOW**, dan AI image generator lainnya.

---

## 📋 Daftar Isi

- [Arsitektur Folder](#arsitektur-folder)
- [Core Master Files](#core-master-files)
- [Campaign Styles](#campaign-styles)
- [Season Lookbooks (S11–S20)](#season-lookbooks-s11s20)
- [Modifiers & Overlays](#modifiers--overlays)
- [Fashion Week & Department](#fashion-week--department)
- [Logo Prompts](#logo-prompts)
- [Inspiration References](#inspiration-references)
- [Studio Campaign](#studio-campaign)
- [Cara Penggunaan](#cara-penggunaan)
- [Workflow Multi-Step](#workflow-multi-step)

---

## Arsitektur Folder

```
PROMPT DEVETESION/
│
├── 📄 DEVETESION_CAMPAIGN_WORKFLOW.md      ← Master workflow (multi-step campaign)
├── 📄 MASTER_LOCATION.md                    ← Image preservation + location lock system
├── 📄 PROMPT MASTER.md                      ← Fashion show prompt generator (3500+ baris)
├── 📄 ULTIMATE_REALISM_ENHANCER.md          ← Anti-AI smoothing / photorealism booster
│
├── 📁 01_CAMPAIGN_STYLES_REAL_BRANDS/       ← 20 file: gaya campaign brand nyata
├── 📁 02_CAMPAIGN_STYLES_DEVETESION/        ← 10 file: gaya khas DEVETESION
├── 📁 03_TYPOGRAPHY_OVERLAYS/               ← 12 file: tipografi / teks di atas gambar
├── 📁 04_LIGHTING_MODIFIERS/                ← 13 file: modifier pencahayaan
│
├── 📁 DEVETESION FASHION WEEK/              ← Prompt fashion show runway
├── 📁 DEVETESION.DEPT/                      ← Department / brand identity prompts
├── 📁 DEVETESION_FLOW_MODIFIERS/            ← 32 file: camera angle, pose, flow control
├── 📁 DEVETESION_LOGO_PROMPTS/              ← Prompt untuk generate logo DEVETESION
│
├── 📁 DEVETESION_SEASON_11/                 ← 30 looks (S11)
├── 📁 DEVETESION_SEASON_11_SAMPLES/         ← 2 sample looks
├── 📁 DEVETESION_SEASON_12/                 ← 30 looks (S12)
├── 📁 DEVETESION_SEASON_12_SAMPLES/
├── ... (hingga Season 20)
│
├── 📁 DEVETESION_STUDIO_CAMPAIGN_AVANTGARDE/ ← Ultra prompt avant-garde campaign
├── 📁 indoor example/                       ← Contoh indoor campaign
├── 📁 outdoor example/                      ← Contoh outdoor campaign
├── 📁 inspo fashion/                        ← Referensi inspirasi fashion
├── 📁 inspo fashion show stage/             ← Referensi panggung fashion show
├── 📁 logo/                                 ← File logo DEVETESION
└── 📁 logo racer/                           ← Logo variant / racing style
```

---

## Core Master Files

### `DEVETESION_CAMPAIGN_WORKFLOW.md`
Panduan **multi-step campaign** dari awal hingga akhir:
1. **Step 1 — Upload:** Upload 2–6 foto model raw + pakaian
2. **Step 2 — Master Conceptors:** AI otomatis memilih lokasi epik yang cocok dengan vibe outfit (museum brutalist, neon Tokyo, kastil, dll). **Dilarang keras runway/catwalk.**
3. **Step 3 — FLOW Modifiers:** Copy-paste file dari `DEVETESION_FLOW_MODIFIERS` untuk memoles lighting, angle kamera, dan tipografi akhir.

### `MASTER_LOCATION.md`
Sistem **Image Preservation + Location Lock**. Memastikan:
- Setiap model muncul sebagai individu terpisah (tidak merge/blend)
- Jumlah output = jumlah input
- Lokasi dikontrol manual (bukan auto-select)
- Fail condition: model hilang, merge, wajah tersembunyi → **INVALID**

### `PROMPT MASTER.md`
**Fashion Show Prompt Generator** (~3500 baris) — engine utama untuk generate runway show. Fitur:
- **Automatic Theme Analysis** → AI menerjemahkan tema (Gorpcore, Dark Academia, Techwear, dll) menjadi silhouette, material, dan proporsi yang tepat
- **5 looks per batch**, 2 samples saat diminta
- **Facial uniqueness** — setiap model punya wajah, rambut, dan outfit unik
- **Female & Male outfit rules** — menghindari "AI sexy outfit spam" dan "villain costume"
- **Design element limits** — max 2–3 elemen per look, corset max 1/batch, harness max 1/batch
- **Audience actions** — berbeda di setiap look
- **DEVETESION branding placement** — cycle melalui 5 posisi

### `ULTIMATE_REALISM_ENHANCER.md`
Prompt untuk **menghancurkan efek "AI generik"** — kulit plastik, porselen, terlalu mulus. Bekerja seperti "kacamata pembesar super" yang menambahkan:
- Pori-pori, micro-wrinkles, freckles, vellus hair
- Mata basah dengan specular reflection realistis
- Rambut dengan individual stray strands
- Subsurface Scattering (SSS) pada kulit
- Render feel: Sony A7R IV, 100mm macro lens

---

## Campaign Styles

### `01_CAMPAIGN_STYLES_REAL_BRANDS/` (20 file)
Gaya campaign terinspirasi dari **brand fashion nyata**:

| # | File | Brand / Style |
|---|------|---------------|
| 01 | `balenciaga_clinical_surveillance` | Balenciaga — clinical, surveillance aesthetic |
| 02 | `helmut_lang_minimalist` | Helmut Lang — minimalist industrial |
| 03 | `dazed_magazine_grunge_flash` | Dazed Magazine — grunge flash |
| 04 | `maison_margiela_obscura` | Maison Margiela — obscura / deconstructed |
| 05 | `rick_owens_brutalist` | Rick Owens — brutalist dark |
| 06 | `balenciaga_dystopian_mud` | Balenciaga — dystopian mud campaign |
| 07 | `raf_simons_subculture` | Raf Simons — subculture youth |
| 08 | `yohji_yamamoto_wabisabi` | Yohji Yamamoto — wabi-sabi |
| 09 | `dazed_y2k_cyber` | Dazed — Y2K cyber revival |
| 10 | `helmut_lang_industrial` | Helmut Lang — industrial |
| 11 | `prada_intellectual` | Prada — intellectual elegance |
| 12 | `vetements_paparazzi` | Vetements — paparazzi street |
| 13 | `balenciaga_red_carpet` | Balenciaga — red carpet |
| 14 | `givenchy_dark_romance` | Givenchy — dark romance |
| 15 | `dazed_bedroom_intimacy` | Dazed — bedroom intimacy |
| 16 | `saint_laurent_night` | Saint Laurent — night allure |
| 17 | `mcqueen_macabre` | Alexander McQueen — macabre |
| 18 | `off_white_street` | Off-White — street culture |
| 19 | `balenciaga_snowstorm` | Balenciaga — snowstorm editorial |
| 20 | `helmut_lang_archival` | Helmut Lang — archival revival |

### `02_CAMPAIGN_STYLES_DEVETESION/` (10 file)
Gaya **khas DEVETESION** — identitas brand sendiri:

| # | File | Style |
|---|------|-------|
| 24 | `devetesion_fw1997_archive` | FW1997 archival aesthetic |
| 25 | `devetesion_jungle_rhythm` | Jungle rhythm editorial |
| 26 | `devetesion_lofi_surveillance` | Lo-fi surveillance |
| 27 | `devetesion_ethereal_studio` | Ethereal studio lighting |
| 28 | `devetesion_urban_decay` | Urban decay campaign |
| 29 | `devetesion_candid_backstage` | Candid backstage |
| 30 | `devetesion_neo_noir` | Neo-noir cinematic |
| 31 | `devetesion_flash_paparazzi` | Flash paparazzi style |
| 32 | `devetesion_analog_polaroid` | Analog polaroid feel |
| 33 | `devetesion_minimalist_void` | Minimalist void |

---

## Modifiers & Overlays

### `03_TYPOGRAPHY_OVERLAYS/` (12 file)
Prompt untuk menambahkan **tipografi / teks editorial** di atas gambar:

| File | Style |
|------|-------|
| `sample_typo_helmut_red` | Helmut Lang — bold red typography |
| `sample_typo_dazed_cover` | Dazed Magazine cover style |
| `sample_typo_minimalist_elegant` | Minimalist elegant |
| `sample_typo_brutalist_streetwear` | Brutalist streetwear |
| `sample_typo_vogue_classic` | Vogue classic editorial |
| `sample_typo_prada_intellectual` | Prada intellectual |
| `sample_typo_margiela_archive` | Margiela archival |
| `sample_typo_vetements_irony` | Vetements ironic typography |
| `sample_typo_rickowens_vertical` | Rick Owens vertical text |
| `sample_typo_rafsimons_youth` | Raf Simons youth culture |
| `sample_typo_givenchy_barcode` | Givenchy barcode style |
| `sample_typo_bottega_classic` | Bottega Veneta classic |

### `04_LIGHTING_MODIFIERS/` (13 file)
Modifier **pencahayaan** untuk memoles hasil akhir:

| File | Lighting Style |
|------|---------------|
| `22_strobist_lighting` | Strobist flash photography |
| `23_y2k_flash_lighting` | Y2K harsh flash |
| `46_modifier_daytime_strobe` | Daytime strobe |
| `47_modifier_studio_rembrandt` | Studio Rembrandt lighting |
| `48_modifier_golden_hour_flare` | Golden hour with lens flare |
| `49_modifier_harsh_desert_sun` | Harsh desert sunlight |
| `50_modifier_subtle_window_blinds` | Subtle window blind shadows |
| `51_modifier_club_laser_strobe` | Club laser strobe |
| `52_modifier_ring_flash_beauty` | Ring flash beauty shot |
| `53_modifier_cinematic_firelight` | Cinematic firelight |
| `54_modifier_color_gel_split` | Color gel split lighting |
| *(dan lainnya)* | |

---

## Season Lookbooks (S11–S20)

Setiap season berisi **30 looks** (15 male + 15 female alternating) dengan model dari berbagai kebangsaan. Setiap look file berisi prompt lengkap untuk generate satu pose/editorial shot.

| Season | File | Tema |
|--------|------|------|
| **S11** | `DEVETESION_SEASON_11/` | 30 looks — British, Japanese, Russian, Korean, Brazilian, German, Senegalese, Swedish, Mexican, Moroccan, Italian, Peruvian, French, Dutch, Kenyan, Indian |
| **S12** | `DEVETESION_SEASON_12/` | 30 looks — Russian, Korean, Japanese, British, Brazilian, German, Senegalese, Swedish, Mexican, Moroccan, Italian, Peruvian, French, Dutch, Kenyan, Indian |
| **S13** | `DEVETESION_SEASON_13/` | 30 looks — French, Brazilian, Korean, British, Nigerian, German, Japanese, Italian, Senegalese, Russian, Mexican, American, Swedish, South African, Argentinian, Ukrainian, Australian, Egyptian, Scottish, Thai, Ivorian, Dutch, Kenyan, Indian, Canadian, Colombian, Moroccan, Chinese, Polish |
| **S14** | `DEVETESION_SEASON_14/` | 30 looks — Brazilian, Korean, Australian, Nigerian, French, Russian, Japanese, Swedish, Italian, Mexican, American, Thai, South African, Argentinian, Scottish, Senegalese, German, Ukrainian, Chinese, Dutch, Egyptian, Colombian, Swedish, Russian, Kenyan, Brazilian, Korean, Australian, Nigerian, German |
| **S15** | `DEVETESION_SEASON_15/` | 30 looks FW15 — Japanese, Senegalese, British, Argentinian, Mexican, Chinese, South Korean, French, Nigerian, Australian, Italian, Russian, Native American, Finnish, Moroccan, Indian, Scottish, Brazilian, Swedish, South Korean |
| **S16** | `DEVETESION_SEASON_16/` | 30 looks FW16 — German, Ethiopian, Turkish, Russian, Mexican, Japanese, Scottish, Indian, Brazilian, Chinese, Nigerian, American, French, Kenyan, Australian, Russian, Mexican, British, Korean, Nigerian |
| **S17** | `DEVETESION_SEASON_17/` | 30 looks FW17 — Argentinian, Swedish, Senegalese, Japanese, Scottish, Brazilian, Icelandic, Ethiopian, Japanese, South Korean, Somali, Navajo, Ukrainian, Sudanese, Filipino, German, Egyptian, Chilean, Irish, Moroccan, Turkish, Russian, Peruvian, Australian, Vietnamese, Italian, Georgian, Malian, Finnish, Mexican |
| **S18** | `DEVETESION_SEASON_18/` | 30 looks FW18 — Somali, Japanese, Ukrainian, Argentinian, Indian, Canadian, Korean, Ethiopian, German, Peruvian, Turkish, Egyptian, Nigerian, Russian, French, Thai, Brazilian, Senegalese, South Korean, Swedish, Kenyan, Maori, Scottish, Polynesian, Vietnamese, Jamaican, Estonian, Syrian, Ethiopian, Native American |
| **S19** | `DEVETESION_SEASON_19/` | 30 looks — Russian, Brazilian, Senegalese, Japanese, French, Somali, Estonian, Syrian, South Korean, German, Nigerian, Mexican, Ukrainian, Swedish, Indian, Canadian, Argentinian, South African, British, Senegalese, Australian, Japanese, Kenyan, Italian, Irish, Ghanaian, Vietnamese, Russian, Ethiopian, American |
| **S20** | `DEVETESION_SEASON_20/` | 30 looks — Russian, Brazilian, +更多 |

Setiap season juga punya folder **SAMPLES** (2 looks) untuk preview/testing sebelum generate full 30.

---

## Fashion Week & Department

### `DEVETESION FASHION WEEK/`
Prompt khusus untuk **fashion show runway** — berbeda dari campaign editorial. Fokus pada:
- Catwalk / runway setting
- Audience di kedua sisi
- Model berjalan mid-stride
- Lighting panggung fashion show

### `DEVETESION.DEPT/`
Prompt untuk **brand department / identity** — mungkin mencakup brand guidelines, visual identity, atau departmental styling.

---

## Logo Prompts

### `DEVETESION_LOGO_PROMPTS/`
Prompt untuk **generate logo DEVETESION** menggunakan AI image generator.

### `logo/` & `logo racer/`
File-file **logo DEVETESION** yang sudah di-generate, termasuk variant racing style.

---

## Inspiration References

### `inspo fashion/`
Koleksi **referensi inspirasi** dari fashion show nyata (Annakiki SS26, KidSuper SS26 Menswear, dll) — diambil dari Vogue Fashion Shows.

### `inspo fashion show stage/`
Referensi **panggung / stage design** fashion show — untuk memahami komposisi runway, lighting panggung, dan audience layout.

### `indoor example/` & `outdoor example/`
Contoh hasil generate untuk **indoor** dan **outdoor** campaign — sebagai benchmark kualitas.

---

## Studio Campaign

### `DEVETESION_STUDIO_CAMPAIGN_AVANTGARDE/`
Prompt **ultra avant-garde** untuk campaign studio level tertinggi:

| File | Isi |
|------|-----|
| `01_Master_Ultra_Prompt_AvantGarde` | Master prompt avant-garde |
| `02_Master_Ultra_Prompt_Adaptive_Location` | Adaptive location selection |
| `03_Final_Ultimate_Strict_Campaign` | Strict campaign mode |
| `DYNAMIC_CAMPAIGN_WORKFLOW` | Dynamic workflow guide |

---

## Cara Penggunaan

### 1. Generate Campaign Editorial (Multi-Step)
```
Step 1: Upload 2–6 foto model + pakaian ke AI
Step 2: Copy-paste prompt dari DEVETESION_CAMPAIGN_WORKFLOW.md
Step 3: Ambil hasil Step 2, upload ulang sebagai reference
Step 4: Copy-paste salah satu file dari DEVETESION_FLOW_MODIFIERS/
Step 5: (Opsional) Jalankan ULTIMATE_REALISM_ENHANCER.md untuk photorealism
```

### 2. Generate Fashion Show Runway
```
Buka PROMPT MASTER.md → beri tema (misal "Gorpcore", "Dark Academia")
→ AI otomatis generate 5 looks dengan facial, hair, outfit unik
→ Tambahkan --iw 2.0 --ar 16:9 --style raw untuk Midjourney
```

### 3. Generate Season-Specific Looks
```
Buka folder DEVETESION_SEASON_XX/ yang diinginkan
→ Copy-paste isi file look yang dipilih
→ Generate di AI image generator
```

### 4. Menghilangkan Efek "AI Look"
```
Upload gambar yang terlihat terlalu AI
→ Copy-paste prompt dari ULTIMATE_REALISM_ENHANCER.md
→ Tambahkan negative prompt jika engine mendukung
```

### 5. Menambahkan Tipografi Editorial
```
Pilih salah satu file dari 03_TYPOGRAPHY_OVERLAYS/
→ Copy-paste promptnya ke AI dengan reference image
```

---

## Workflow Multi-Step

```
┌─────────────────────────────────────────────────────────┐
│  STEP 1: Upload Model Photos                            │
│  (2–6 foto raw + pakaian)                               │
└────────────────────┬────────────────────────────────────┘
                     ▼
┌─────────────────────────────────────────────────────────┐
│  STEP 2: Master Conceptors                              │
│  (AI auto-select lokasi epik + merge models)            │
│  Source: DEVETESION_CAMPAIGN_WORKFLOW.md                │
└────────────────────┬────────────────────────────────────┘
                     ▼
┌─────────────────────────────────────────────────────────┐
│  STEP 3: FLOW Modifiers                                 │
│  (Camera angle, pose, lighting, typography)             │
│  Source: DEVETESION_FLOW_MODIFIERS/                     │
└────────────────────┬────────────────────────────────────┘
                     ▼
┌─────────────────────────────────────────────────────────┐
│  STEP 4: Realism Enhancer (Opsional)                    │
│  (Destroy AI smoothing, add skin texture)               │
│  Source: ULTIMATE_REALISM_ENHANCER.md                   │
└─────────────────────────────────────────────────────────┘
```

---

## Midjourney Parameters

Untuk hasil optimal di Midjourney, tambahkan di akhir prompt:

| Parameter | Fungsi |
|-----------|--------|
| `--iw 2.0` | Image weight maksimal (pertahankan referensi) |
| `--ar 16:9` | Aspect ratio widescreen editorial |
| `--style raw` | Render lebih natural, kurang "AI stylized" |
| `--v 7` | Versi Midjourney terbaru |

---

## Lisensi & Hak Gunakan

Semua prompt dalam repositori ini adalah **karya orisinal DEVETESION**. Gunakan untuk keperluan branding dan campaign pribadi. Dilarang mendistribusikan ulang tanpa izin.

---

> **Repository:** [mrhdayat/devetesion-prompt-branding](https://github.com/mrhdayat/devetesion-prompt-branding)
> **Author:** Muhammad Rahmat Hidayat (@mrhdayat)
> **Last Updated:** April 2026
