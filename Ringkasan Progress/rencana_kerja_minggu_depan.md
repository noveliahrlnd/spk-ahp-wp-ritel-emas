# 🗓️ Rencana Kerja Minggu Depan (Roadmap Eksekusi Paper SPK)
**Penelitian:** Integrasi Metode AHP dan Weighted Product pada Penentuan Lokasi Ritel Emas di DIY  
**Target Output:** Draf Utuh Manuskrip (*Full Draft*) Sesuai Template Jurnal RMSI (UIN Suska)  
**Periode:** 11 November – 17 November 2026

---

## 🎯 Target Utama (Weekly Milestone)
> **Goal:** Menyelesaikan penulisan seluruh bab yang tersisa (Metode Penelitian, Hasil dan Pembahasan, Kesimpulan, Abstrak Bilingual, dan Referensi IEEE), menyatukannya ke dalam template Word `.docx`, serta menyiapkan presentasi kelompok.

---

## 📅 Jadwal Harian (Daily Action Plan)

### 🔹 Hari 1 (Senin / Langkah 1): Draf Bab Metode Penelitian
* **Fokus:** Menulis penjelasan operasional metode riset (bukan cuma teori).
* **Rincian Tugas:**
  1. Menjelaskan tahapan alur penelitian dari identifikasi masalah hingga penarikan kesimpulan.
  2. Menjabarkan teknik pengumpulan data sekunder/lapangan di 5 kandidat lokasi DIY.
  3. Menyajikan profil operasional 6 kriteria ($C_1$ sampai $C_6$) beserta skala penilaiannya.
* **Output Berkas:** `03_Manuscript_Draft/Draft_Metode_Penelitian.md`

---

### 🔹 Hari 2 (Selasa / Langkah 2): Draf Bab Hasil dan Pembahasan
* **Fokus:** Menarasikan temuan komputasi dan membedah perbandingan antar-lokasi secara mendalam.
* **Rincian Tugas:**
  1. **Sub-bab 1 (Analisis Bobot AHP):** Menjelaskan rasionalitas kenapa $C_3$ (Daya Beli, 46,14%) dan $C_4$ (Visibilitas, 22,58%) mendominasi, serta melaporkan hasil uji konsistensi ($CR = 0{,}0677$).
  2. **Sub-bab 2 (Hasil Ranking WP):** Membedah skor Vektor $S$ dan $V$ kelima alternatif.
  3. **Sub-bab 3 (Diskusi Trade-Off):** 
     * Mengapa Sinduadi ($A_1$) bisa menang tipis dari Malioboro Mall ($A_5$).
     * Analisis efek penalti eksponensial biaya sewa mahal Malioboro (Rp 346,32 juta).
     * Alasan Babarsari ($A_3$) berada di posisi terbawah.
* **Output Berkas:** `03_Manuscript_Draft/Draft_Hasil_dan_Pembahasan.md`

---

### 🔹 Hari 3 (Rabu / Langkah 3): Kesimpulan & Abstrak Bilingual
* **Fokus:** Merumuskan intisari naskah untuk gerbang pertama pembaca dan reviewer.
* **Rincian Tugas:**
  1. **Menulis Bab Kesimpulan:**
     * Menjawab tujuan penelitian secara langsung (lokasi terpilih adalah Sinduadi dengan skor $V = 0{,}2302$).
     * Menegaskan stabilitas integrasi AHP-WP bebas *rank reversal*.
     * Memberikan saran praktis bagi investor emas dan saran pengembangan riset (misal: integrasi GIS/SIG spasial).
  2. **Menulis Abstrak (Bahasa Indonesia & Bahasa Inggris):**
     * Format 150–250 kata, mencakup: Latar belakang & masalah $\rightarrow$ Metode hibrida AHP-WP $\rightarrow$ Temuan numerik utama ($CR$, $V_{\max}$) $\rightarrow$ Implikasi praktis.
     * Kata kunci (*keywords*): 5–6 kata kunci standar.
* **Output Berkas:** `03_Manuscript_Draft/Draft_Abstrak_dan_Kesimpulan.md`

---

### 🔹 Hari 4 (Kamis / Langkah 4): Daftar Pustaka IEEE & Harmonasi Naskah
* **Fokus:** Memastikan standarisasi sitasi ilmiah dan keterpaduan argumen lintas-bab.
* **Rincian Tugas:**
  1. Mengompilasi minimal 10–15 literatur primer (jurnal bereputasi 10 tahun terakhir) ke dalam format IEEE standar:
     * Literatur AHP Saaty & Aksioma Konsistensi.
     * Literatur anomali *rank reversal* & aksioma IIA Kenneth Arrow.
     * Literatur ekonomi tata ruang (Christaller, Marshall, Hotelling).
     * Literatur pembanding (Jurnal Krisnadana & Jurnal JUSTIN).
  2. Menjalankan *Cross-Check Review*: Memastikan setiap sitasi `[1]`, `[2]`, dst. di badan naskah terhubung presisi dengan Daftar Pustaka.
* **Output Berkas:** `03_Manuscript_Draft/Daftar_Pustaka.md`

---

### 🔹 Hari 5 (Jumat / Langkah 5): Layouting Template Word Jurnal & Rehearsal
* **Fokus:** Menyatukan seluruh bab ke dalam file dokumen master sesuai panduan RMSI.
* **Rincian Tugas:**
  1. Memindahkan seluruh konten Markdown ke berkas `Tamplate Paper SPK.docx`.
  2. Menyesuaikan format selingkung:
     * Font: Times New Roman, format 2 kolom.
     * Tabel ilmiah: hanya garis horizontal tanpa garis vertikal.
     * Gambar: monokrom rata tengah dengan keterangan di bawah (10 pt).
  3. Latihan presentasi kelompok menggunakan slide panduan `ringkasan_2026-11-10.md`.
* **Output Berkas:** Berkas final `Paper_SPK_Final_Kelompok.docx` & Push Git `main`.

---

## 👥 Rekomendasi Pembagian Tugas Anggota Kelompok

| Nama Anggota | Peran Utama | Tanggung Jawab Spesifik |
| :--- | :--- | :--- |
| **Novelia Harlinda** | *Project Lead & Final Reviewer* | Mengoordinasikan seluruh integrasi naskah, review gaya bahasa (`academic-writing-refiner`), dan komitmen git. |
| **Auliah Qorinaya** | *Author - Hasil & Pembahasan* | Menyusun narasi komputasi Tabel 1–4 dan analisis perbandingan keunggulan Sinduadi vs Malioboro. |
| **Muhammad Adin Dwi R.** | *Author - Metode Penelitian* | Menyusun detail tahapan algoritma hibrida dan profil parameter operasional 6 kriteria. |
| **Muhammad Riski** | *Author - Abstrak & Kesimpulan* | Merumuskan draft abstrak dwibahasa dan menyusun poin kesimpulan serta rekomendasi manajerial. |
| **Rafael Aga Pratama** | *Technical Layout & References* | Memvalidasi sitasi IEEE, menyusun daftar pustaka, dan melakukan layouting presisi pada berkas template Word. |

---

## 📋 Checklist Kesiapan Akhir Minggu Depan
- [ ] Draf Bab Metode Penelitian selesai ditulis
- [ ] Draf Bab Hasil dan Pembahasan selesai ditulis
- [ ] Draf Bab Kesimpulan & Saran selesai ditulis
- [ ] Abstrak Bahasa Indonesia & Bahasa Inggris siap
- [ ] Daftar Pustaka format IEEE (minimal 10 jurnal terkait) tuntas
- [ ] Seluruh bab berhasil di-*layout* ke `Tamplate Paper SPK.docx`
- [ ] Repositori GitHub ter-update bersih di branch `main`
- [ ] Kelompok siap presentasi progres lengkap di depan dosen

