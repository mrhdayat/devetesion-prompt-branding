# 📸 DEVETESION: Multi-Step High-Fashion Campaign Workflow

Berikut adalah **Master Strict Prompt** dan panduan alur kerja untuk membuat *campaign* editorial DEVETESION secara berjenjang (*multi-step*), dari pembentukan komposisi awal di lokasi *epic* hingga eksekusi gaya akhir. 

> *FLOW seringkali gagal (error) jika diberikan prompt abstrak dari 33 file sebelumnya karena FLOW membutuhkan kepastian mutlak mengenai angle kamera dan struktur pose badan.* **Sistem baru ini menyelesaikan masalah tersebut.**

---

## STEP 1: UPLOAD (INPUT)
Upload 2 hingga 6 foto model *raw* beserta pakaian yang akan digunakan ke dalam antarmuka AI Anda. 

---

## STEP 2: THE "MASTER CONCEPTOR" PROMPT (Pembangunan Set & Lokasi Epic Otomatis)
**Tujuan:** Menyatukan ke-2 hingga 6 model Anda ke dalam **satu frame saling berdekatan** di sebuah lokasi mahakarya kelas dunia TANPA MENGUBAH sedikit pun identitas dan rupa baju mereka. *Prompt ini sudah saya rombak total agar AI SECARA OTOMATIS berpikir dan memilih sendiri lokasi paling mahal yang cocok dengan baju model Anda (bisa berupa museum brutalist, jalanan neon Tokyo, kastil tua, hingga alam bebas), namun secara mutlak dilarang menaruhnya di acara runway/catwalk*.

*Copy-paste teks ini setelah mengunggah foto Anda:*

```text
STRICT IMAGE PRESERVATION MODE (ABSOLUTE — NO EXCEPTION):

- ANALYZE the clothing style and vibe of ALL the uploaded reference images.
- MERGE and seamlessly place ALL uploaded models into exactly ONE cohesive, hyper-realistic image frame interacting or posing together.
- DO NOT subtract, replace, or generate new faces or identities.
- DO NOT change their facial structure, expression, skin details, or identity.
- DO NOT change their outfits, styling, or proportions. Do not reinterpret garments.
- DO NOT beautify or stylize faces into a soft "AI look".

IDENTITY & THEME LOCK:
Each model must remain EXACTLY as they appear in the uploaded images. Build a SINGLE, breathtaking master environment/background for a high-fashion editorial photoshoot. 

LOCATION SELECTION (AUTONOMOUS):
You must AUTONOMOUSLY SELECT an epic, highly realistic location that perfectly matches the extracted vibe and fashion styling of their collective outfits. Do not default to just mountains or deserts. Think creatively: an abandoned French chateau, a moody brutalist concrete museum, a neon-lit Tokyo rooftop, a luxurious vintage living room, a stark white salt flat, an industrial cyberpunk warehouse, or a moody dense forest. 

BACKGROUND RESTRICTION (MANDATORY):
- NO RUNWAYS, NO FASHION SHOWS, NO CATWALKS.
- NO mundane streets or messy ambiguous events.
- It must feel like an incredibly expensive, on-location editorial luxury high-fashion campaign shoot. 

MODEL COUNT RULE:
- Number of output models MUST EXACTLY MATCH the number of uploaded images.
- If I upload 5 images → output MUST contain exactly 5 individuals posing in the scene together.

FAIL CONDITION:
If any face or outfit changes, background is a runway, or if a model goes missing → OUTPUT IS INVALID.

OUTPUT REQUEST:
Generate the base high-resolution, photorealistic, unedited group photo inside this newly specified epic environment. Raw photo, 8k.
```
*(Ingat, saat mengeksekusinya di Midjourney tambahkan `--iw 2.0 --ar 16:9 --style raw` di ujung prompt).*

---

## STEP 3: THE "FLOW" MODIFIERS (Aplikasi Kamera, Pose, dan Tipografi Akhir)
**Tujuan:** Ambil gambar hasil dari **Step 2** yang lokasinya sudah jadi secara otomatis oleh AI, lalu jadikan sebagai **Reference Image / Base Image** yang di-upload ulang.

Karena platform visual sangat ketat, **Buka folder `DEVETESION_FLOW_MODIFIERS`**. 

Tinggal *copy-paste* langsung isi dari salah satu file tersebut (baik yang pakai tipografi logo maupun `nofont`) untuk memoles *lighting*, sudut kamera, dan pose tubuh model agar bergaya super mahal!

*Dengan BACKGROUND LOCK di Step 3, lokasi apapun yang dipilih AI secara ajaib di Step 2 (misal Museum) asalkan tidak diubah, tidak akan bergeser.*
