# Project Context & Agent Instructions — Paper SPK (AHP-WP)

Dokumen ini menjadi *single source of truth* konteks, aturan, data, dan roadmap pengembangan paper SPK di folder `Paper/`. Setiap agen yang bekerja di proyek ini wajib mengikuti pedoman berikut.

## 1. Identitas & Ruang Lingkup Paper

- **Topik:** Penentuan lokasi strategis bisnis ritel perhiasan (toko emas) di Daerah Istimewa Yogyakarta menggunakan model hibrida **Analytic Hierarchy Process (AHP)** dan **Weighted Product (WP)**.
- **Judul Kerja:**
  - *ID:* Integrasi Metode AHP dan Weighted Product pada Penentuan Lokasi Strategis Bisnis Ritel Perhiasan
  - *EN (untuk template MALCOM, maks. 14 kata):* Integration of AHP and Weighted Product Methods for Jewelry Retail Strategic Location Selection *(dapat disesuaikan saat finalisasi, maksimal 14 kata)*
- **Tim Penulis & Afiliasi:**
  1. Novelia Harlinda (`noveliahrlnd@gmail.com`)
  2. Auliah Qorinaya (`qorinayaaulia@gmail.com`)
  3. Muhammad Adin Dwi Ramadhan (`madindwir@gmail.com`)
  4. Muhammad Riski (`muhamaddriski098@gmail.com`)
  5. Rafael Aga Pratama (`rafaelagapratama0@gmail.com`)
  - *Afiliasi:* Program Studi Pendidikan Teknik Informatika, Fakultas Teknik, Universitas Negeri Yogyakarta
- **Batasan Ruang Lingkup:** Fokus **murni pada riset operasi, pemodelan matematis MCDM, komputasi numerik, dan evaluasi model** (tanpa perancangan antarmuka/UI, database, atau implementasi kode aplikasi web).
- **Target Output Akhir:** Manuskrip paper **siap submit** dalam format `.docx` mengikuti template resmi **MALCOM** (`01_Dokumen_dan_Template/New Malcom Template.docx`), disertai master draft Markdown yang rapi di `03_Manuscript_Draft/`.

## 2. Struktur Folder `Paper/`

- `01_Dokumen_dan_Template/` — Template resmi jurnal: `New Malcom Template.docx`.
- `02_Literature_Notes/papers/` — **17 artikel PDF terverifikasi (tahun 2023–2026)** sebagai kolam referensi utama.
- `03_Manuscript_Draft/` — Draf naskah dan dataset (`Dataset_Penelitian.md`, serta draf bab lama yang sedang/akan ditata ulang).
- `Ringkasan Progress/` — Catatan ringkasan presentasi dan log progres historis.
- `SKILLS/` — Skill pendukung (`academic-writing-refiner`, `humanizer-indonesia-main`, dan `claude-office-skills/public/{docx,pdf,pptx,xlsx}`).

## 3. Struktur Baru Paper yang Wajib Dipakai

Naskah tidak lagi menggunakan struktur lama RMSI (tidak ada bab *Landasan Teori* terpisah). Gunakan struktur berikut:

1. **Judul** (Bahasa Inggris & Bahasa Indonesia, masing-masing maksimal 14 kata)
2. **Abstrak** (`Abstract` Inggris + `Abstrak` Indonesia, masing-masing maks. 200 kata, font 9 pt; disertai minimal 5 kata kunci berurutan abjad A–Z)
3. **Pendahuluan**
4. **Metode**
   - **Data Kriteria dan Alternatif**
   - **Desain Penelitian** *(wajib menampilkan bagan model SPK, lalu menjelaskan tiap tahap dan rumus matematisnya)*
5. **Hasil dan Pembahasan**
   - **Perhitungan AHP** *(matriks perbandingan berpasangan, normalisasi, eigen vector/bobot, dan uji konsistensi $\lambda_{\max}, CI, CR$)*
   - **Perhitungan (WP)** *(kalibrasi pangkat eksponen cost/benefit, Vektor $S_i$, Vektor $V_i$, pemeringkatan akhir, serta grafik)*
   - **Evaluasi** *(analisis trade-off antaralternatif, pembuktian kestabilan terhadap rank reversal / aksioma IIA, serta tabel uji sensitivitas & simulasi penambahan/penghapusan alternatif)*
6. **Kesimpulan dan Saran** *(sesuai aturan template MALCOM: tidak boleh ada sitasi/referensi di dalam Kesimpulan)*
7. **Daftar Pustaka** *(minimal 15 pustaka, format IEEE, terbitan 2023–2026)*

## 4. Aturan Format Template MALCOM (`01_Dokumen_dan_Template/New Malcom Template.docx`)

- **Bahasa Naskah:** Isi artikel boleh berbahasa **Indonesia**; Judul & Abstrak/Keywords wajib dwibahasa (**Inggris + Indonesia**).
- **Halaman & Margin:** A4 (`210 × 297 mm`), margin Kiri `3,0 cm`, Atas `2,25 cm`, Kanan `2,5 cm`, Bawah `2,25 cm`; panjang naskah **6–11 halaman** (termasuk tabel dan gambar).
- **Tipografi:** **Times New Roman**, spasi tunggal (`1.0`), teks rata kanan-kiri (*justified*), tanpa jarak paragraf ekstra (`before 0`, `after 0`).
  - Judul: `14 pt` (EN: Bold Italic; ID: Bold), Center.
  - Abstract/Abstrak & Keywords/Kata Kunci: `9 pt`.
  - Heading 1, Heading 2, isi teks, judul & isi tabel, serta judul gambar: `10 pt`.
- **Tabel & Gambar:**
  - Judul tabel diletakkan **di atas** tabel, rata tengah (*center*).
  - Judul gambar diletakkan **di bawah** gambar, rata tengah (*center*).
  - Setiap tabel, gambar, dan persamaan bernomor `(1)`, `(2)`, dst. wajib dirujuk di dalam teks.

## 5. Data & Angka Acuan (*Ground Truth*)

- **Sumber Penilaian:** Matriks perbandingan berpasangan AHP dan skor skala 1–5 ($C_2$–$C_6$) disusun berdasarkan **asumsi dan penilaian tim peneliti** yang diturunkan dari observasi lapangan serta data listing properti (jangan menulis klaim wawancara pakar eksternal yang tidak pernah dilakukan).
- **Kriteria Keputusan ($n = 6$) & Bobot AHP:**
  - $C_1$ Biaya Beban Properti (*Cost*, Juta Rp/tahun): $w_1 = 0{,}1333$ ($13{,}33\%$)
  - $C_2$ Keamanan Eksternal Kawasan (*Benefit*, skala 1–5): $w_2 = 0{,}0501$ ($5{,}01\%$)
  - $C_3$ Potensi Daya Beli Lingkungan (*Benefit*, skala 1–5): $w_3 = 0{,}4614$ ($46{,}14\%$)
  - $C_4$ Visibilitas Lokasi (*Benefit*, skala 1–5): $w_4 = 0{,}2258$ ($22{,}58\%$)
  - $C_5$ Fleksibilitas Perombakan Struktur (*Benefit*, skala 1–5): $w_5 = 0{,}0271$ ($2{,}71\%$)
  - $C_6$ Aglomerasi Sentra Emas (*Benefit*, skala 1–5): $w_6 = 0{,}1023$ ($10{,}23\%$)
  - **Uji Konsistensi AHP:** $\lambda_{\max} = 6{,}420$, $CI = 0{,}084$, $RI = 1{,}24$, $CR = 0{,}0677 \le 0{,}10$ (Konsisten).
- **Alternatif Lokasi ($m = 5$) & Hasil WP:**
  1. **$A_1$ — Sinduadi (Jl. Umbul Permai):** $C_1=130$, $C_2=3, C_3=4, C_4=5, C_5=5, C_6=2$ → $S_1 = 1{,}6934$, $V_1 = 0{,}2302$ ($23{,}02\%$) — **Peringkat 1**.
  2. **$A_5$ — Malioboro Mall:** luas ruang usaha **78 m²** *(koreksi resmi dari pengguna!)*, $C_1=346{,}32$, $C_2=5, C_3=5, C_4=4, C_5=2, C_6=4$ → $S_5 = 1{,}6501$, $V_5 = 0{,}2243$ ($22{,}43\%$) — **Peringkat 2**.
  3. **$A_4$ — Taman Siswa:** $C_1=250$, $C_2=3, C_3=4, C_4=5, C_5=5, C_6=3$ → $S_4 = 1{,}5872$, $V_4 = 0{,}2158$ ($21{,}58\%$) — **Peringkat 3**.
  4. **$A_2$ — Jl. Magelang Km. 5:** $C_1=120$, $C_2=3, C_3=3, C_4=4, C_5=5, C_6=2$ → $S_2 = 1{,}4246$, $V_2 = 0{,}1937$ ($19{,}37\%$) — **Peringkat 4**.
  5. **$A_3$ — Babarsari:** $C_1=150$, $C_2=3, C_3=2, C_4=3, C_5=5, C_6=1$ → $S_3 = 1{,}0006$, $V_3 = 0{,}1360$ ($13{,}60\%$) — **Peringkat 5**.
  - Total $\sum S_k = 7{,}3559$, $\sum V_k = 1{,}0000$.
- **Koreksi Tertunda di Draf Lama:** Di `03_Manuscript_Draft/Draft_Metodologi_Penelitian.md` (baris 49) masih tertulis luas $A_5$ sebesar `54 meter persegi`—wajib diganti menjadi **78 m²** saat revisi draf nanti.

## 6. Aturan Sitasi, Keakuratan, & Penggunaan Skill

- **Wajib Referensi Nyata (2023–2026):** Seluruh sitasi `[1]`, `[2]`, dst. wajib merujuk pada artikel valid yang PDF-nya ada di `02_Literature_Notes/papers/` (17 PDF tahun 2023–2026) atau sumber primer terverifikasi lain (mis. literatur klasik Saaty jika diperlukan sebagai teori dasar, namun utamakan komposisi 2023–2026). **Dilarang keras** mengarang judul, penulis, jurnal, DOI, atau angka statistik.
- **Konsistensi Notasi & Penomoran:** Seragamkan simbol bobot/pangkat WP (`W_j^*` atau `W_j`), serta urutkan ulang nomor `Tabel 1..N` dan `Gambar 1..M` dari awal sampai akhir naskah.
- **Gunakan Skill yang Tersedia di `SKILLS/`:**
  - `academic-writing-refiner` & `humanizer-indonesia` saat memoles kualitas tulisan ilmiah Bahasa Indonesia agar mengalir alami dan bebas gaya AI/terjemahan kaku.
  - `docx` (`SKILLS/claude-office-skills/public/docx`) saat memindahkan naskah final ke `01_Dokumen_dan_Template/New Malcom Template.docx`.

## 7. Roadmap Pekerjaan Selanjutnya

1. **Verifikasi Numerik & Uji Sensitivitas:** Pastikan seluruh hitungan AHP & WP presisi, dan buat data/tabel angka nyata untuk simulasi uji sensitivitas bobot serta simulasi tambah/hapus alternatif (bagian *Evaluasi*).
2. **Revisi & Konsolidasi Master Draft:** Gabungkan materi relevan dari file-file terpisah di `03_Manuscript_Draft/` ke dalam struktur baru (Pendahuluan → Metode → Hasil dan Pembahasan), perbaiki luas $A_5$ menjadi `78 m²`, perbaiki narasi sumber penilaian (asumsi/observasi tim peneliti, bukan wawancara pakar eksternal), dan sinkronkan sitasi `[1]`–`[15+]` terhadap PDF di `02_Literature_Notes/papers/`.
3. **Lengkapi Bagian Kosong:** Tulis `Kesimpulan dan Saran` (tanpa sitasi), `Abstract`/`Abstrak` + kata kunci dwibahasa, dan `Daftar Pustaka` IEEE ($\ge 15$ pustaka).
4. **Poles Bahasa & Layout `.docx`:** Jalankan review bahasa (`humanizer-indonesia` + `academic-writing-refiner`), render bagan model SPK dan grafik menjadi gambar statis, lalu rakit menjadi dokumen `.docx` siap submit sesuai `New Malcom Template.docx`.
