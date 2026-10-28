# Integrasi Metode AHP dan Weighted Product pada Penentuan Lokasi Strategis Bisnis Ritel Perhiasan

Repositori riset operasi, data komputasi numerik, dan draf manuskrip publikasi jurnal untuk penentuan lokasi optimal toko emas/ritel perhiasan menggunakan metode hibrida **Analytic Hierarchy Process (AHP)** dan **Weighted Product (WP)**.

---

## 👥 Tim Penulis
1. **Novelia Harlinda** (noveliahrlnd@gmail.com)
2. **Auliah Qorinaya** (qorinayaaulia@gmail.com)
3. **Muhammad Adin Dwi Ramadhan** (madindwir@gmail.com)
4. **Muhammad Riski** (muhamaddriski098@gmail.com)
5. **Rafael Aga Pratama** (rafaelagapratama0@gmail.com)

*Program Studi Pendidikan Teknik Informatika, Fakultas Teknik, Universitas Negeri Yogyakarta*

---

## 📂 Struktur Repositori

```text
├── 01_Literature_Notes/          # Koleksi literatur primer (PDF) & catatan sintesis
│   ├── Paper Axioms (Yan & Mao, 2025).pdf
│   ├── Paper Jurnal Krisnadana (Sutrisno, 2023).pdf
│   ├── Paper JUSTIN (Mahendra, 2020).pdf
│   └── Paper Value Jurnal (Izzaturobbani, 2026).pdf
├── 02_Evergreen_Notes/           # Konsep teoretis inti MCDM & Riset Operasi
│   ├── Aksioma Konsistensi Saaty (CR).md
│   ├── Sifat Pemangkatan Eksponensial WP.md
│   └── Teori Rank Reversal pada AHP.md
├── 03_Manuscript_Draft/          # Draf naskah paper untuk jurnal target
│   ├── Dataset_Penelitian.md      # Data numerik lengkap AHP-WP
│   ├── Draft_Pendahuluan.md       # Draf Bab Pendahuluan
│   └── Draft_Persamaan_Matematika.md # Formulasi matematis formal
├── 04_Archive/                   # Arsip draf dan catatan pendukung
├── Docs/                         # Dokumen tambahan
├── Paper SPK.docx                # Dokumen dataset asli penelitian
├── Paper_SPK_extracted.md        # Hasil ekstraksi markdown data penelitian
├── Tamplate Paper SPK.docx       # Template gaya selingkung jurnal
└── Tamplate_Paper_SPK_extracted.md # Ekstrak panduan format jurnal
```

---

## 📊 Ringkasan Model Komputasi

### 1. Kriteria Keputusan
* **$C_1$ - Biaya Beban Properti (Cost)**: Pangkat negatif ($-w_1$). Semakin murah biaya sewa tahunan, nilai preferensi semakin tinggi.
* **$C_2$ - Keamanan Eksternal Kawasan (Benefit)**: Pangkat positif ($+w_2$).
* **$C_3$ - Potensi Daya Beli Lingkungan (Benefit)**: Pangkat positif ($+w_3$).
* **$C_4$ - Visibilitas Lokasi (Benefit)**: Pangkat positif ($+w_4$).
* **$C_5$ - Fleksibilitas Perombakan Struktur (Benefit)**: Pangkat positif ($+w_5$).
* **$C_6$ - Aglomerasi Sentra Emas (Benefit)**: Pangkat positif ($+w_6$).

> **Hirarki Prioritas:** $C_3 > C_4 > (C_1 = C_6) > C_2 > C_5$

### 2. Pembobotan AHP & Uji Konsistensi
* **Bobot Kriteria ($W$):**
  * $w_1 = 0{,}1333$ ($13{,}33\%$)
  * $w_2 = 0{,}0501$ ($5{,}01\%$)
  * $w_3 = 0{,}4614$ ($46{,}14\%$)
  * $w_4 = 0{,}2258$ ($22{,}58\%$)
  * $w_5 = 0{,}0271$ ($2{,}71\%$)
  * $w_6 = 0{,}1023$ ($10{,}23\%$)
* **Uji Konsistensi Saaty:**
  * $\lambda_{\max} = 6{,}420$
  * $CI = 0{,}084$
  * $RI = 1{,}24$ ($n = 6$)
  * $CR = 0{,}0677 < 0{,}10$ (**Konsisten & Valid**)

### 3. Hasil Perangkingan Akhir (Weighted Product)

| Peringkat | Kode | Alternatif Lokasi | Vektor $S$ | Vektor $V$ | Persentase | Status |
| :---: | :---: | :--- | :---: | :---: | :---: | :--- |
| **1** | **$A_1$** | **Sinduadi (Jl. Umbul Permai)** | $\mathbf{1{,}6934}$ | $\mathbf{0{,}2302}$ | **$23{,}02\%$** | **Rekomendasi Utama** |
| 2 | $A_5$ | Malioboro Mall | $1{,}6501$ | $0{,}2243$ | $22{,}43\%$ | Rekomendasi 2 |
| 3 | $A_4$ | Taman Siswa | $1{,}5872$ | $0{,}2158$ | $21{,}58\%$ | Rekomendasi 3 |
| 4 | $A_2$ | Jl. Magelang | $1{,}4246$ | $0{,}1937$ | $19{,}37\%$ | Rekomendasi 4 |
| 5 | $A_3$ | Babarsari | $1{,}0006$ | $0{,}1360$ | $13{,}60\%$ | Rekomendasi 5 |

---

## 🎯 Target Publikasi
* **Format:** Gaya Selingkung Jurnal Ilmiah Rekayasa dan Manajemen Sistem Informasi (RMSI - UIN SUSKA).
* **Fokus:** Riset Operasi dan Algoritma Keputusan Numerik (murni matematika tanpa implementasi rekayasa perangkat lunak).
