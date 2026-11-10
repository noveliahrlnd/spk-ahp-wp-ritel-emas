---
title: Bab Landasan Teori - Sub-bab Penulisan Tabel (Integrasi AHP-WP)
created: 2026-11-05
updated: 2026-11-10
status: Ready for Manuscript
target_journal: Template UIN SUSKA (Jurnal Ilmiah Rekayasa dan Manajemen Sistem Informasi)
format: Markdown
tags:
  - landasan-teori
  - penulisan-tabel
  - ahp-wp
  - lokasi-ritel-emas
---

# LANDASAN TEORI

## 2. Penulisan Tabel

> [!NOTE]
> **Catatan Strukturasi Manuskrip:** Sub-bab ini disusun untuk memenuhi petunjuk pengujian format penulisan tabel pada template jurnal RMSI. Pada perakitan naskah publikasi utuh, Tabel 1 dan Tabel 2 dapat dialokasikan ke Bab Metode Penelitian, sedangkan Tabel 3 dan Tabel 4 dialokasikan ke Bab Hasil dan Pembahasan sebagai data komputasi empiris.

Penyajian data numerik dan tahapan komputasi dalam model hibrida *Analytic Hierarchy Process* (AHP) dan *Weighted Product* (WP) disusun secara sistematis ke dalam bentuk tabel terstruktur. Berdasarkan ketentuan template penulisan jurnal ilmiah, judul tabel ditempatkan di bagian atas tabel pada posisi rata kiri (*left alignment*) dengan ukuran huruf 10 pt dalam format *Title Case*, sedangkan isi sel tabel menggunakan ukuran huruf 8 pt. Tata letak tabel menerapkan format standar ilmiah yang hanya memanfaatkan garis pembatas horizontal tanpa menggunakan garis vertikal. Setiap tabel dirujuk secara berurutan di dalam teks naskah.

### 2.1. Matriks Perbandingan Berpasangan Kriteria AHP

Tahap awal permodelan keputusan dimulai dari penentuan preferensi pengambil keputusan terhadap kepentingan relatif kriteria pemilihan lokasi toko emas. Evaluasi dilakukan terhadap enam kriteria spasial dan operasional, yaitu biaya beban properti ($C_1$), keamanan eksternal kawasan ($C_2$), potensi daya beli lingkungan ($C_3$), visibilitas lokasi ($C_4$), fleksibilitas perombakan struktur bangunan ($C_5$), dan aglomerasi sentra emas ($C_6$). Penilaian preferensi antar kriteria dikuantifikasi menggunakan skala fundamental Saaty (skala 1 hingga 9). Rekapitulasi matriks perbandingan berpasangan kriteria disajikan pada Tabel 1.

Tabel 1. Matriks Perbandingan Berpasangan Kriteria Pembobotan AHP  
*(Format cetak: Judul 10 pt, isi sel 8 pt, layout garis horizontal tanpa garis vertikal)*

| Kriteria | $C_1$ (Biaya) | $C_2$ (Keamanan) | $C_3$ (Daya Beli) | $C_4$ (Visibilitas) | $C_5$ (Struktur) | $C_6$ (Aglomerasi) |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **$C_1$ (Biaya)** | 1 | 5 | 1/5 | 1/3 | 7 | 1 |
| **$C_2$ (Keamanan)** | 1/5 | 1 | 1/7 | 1/5 | 3 | 1/3 |
| **$C_3$ (Daya Beli)** | 5 | 7 | 1 | 3 | 9 | 7 |
| **$C_4$ (Visibilitas)** | 3 | 5 | 1/3 | 1 | 7 | 3 |
| **$C_5$ (Struktur)** | 1/7 | 1/3 | 1/9 | 1/7 | 1 | 1/5 |
| **$C_6$ (Aglomerasi)** | 1 | 3 | 1/7 | 1/3 | 5 | 1 |
| **Total Kolom** | 10,3429 | 21,3333 | 1,9206 | 5,0095 | 32,0000 | 12,5333 |

Sebagaimana disajikan pada Tabel 1, setiap elemen diagonal utama memiliki nilai 1 karena membandingkan kriteria dengan dirinya sendiri. Elemen di bawah diagonal utama merupakan nilai resiprokal ($a_{ki} = 1 / a_{ik}$) dari elemen di atas diagonal utama sesuai dengan aksioma perbandingan berpasangan. Nilai total pada baris paling bawah menunjukkan akumulasi penjumlahan kolom yang berperan sebagai faktor penormalisasi dalam proses sintesis vektor bobot prioritas. Kriteria potensi daya beli lingkungan ($C_3$) menghasilkan nilai total kolom paling kecil, yaitu 1,9206. Hal ini mengindikasikan bahwa kriteria $C_3$ secara konsisten dinilai jauh lebih dominan dibandingkan kelima kriteria pembanding lainnya.

### 2.2. Sintesis Bobot Kriteria dan Pengujian Rasio Konsistensi

Normalisasi matriks perbandingan berpasangan dilakukan dengan membagi setiap elemen sel dengan total kolom yang bersangkutan, kemudian menghitung nilai rata-rata dari setiap baris sesuai formulasi Persamaan (1). Proses komputasi ini menghasilkan vektor bobot prioritas kriteria (*Eigen Vector*). Untuk memverifikasi keabsahan logika penilai dan memastikan tidak terdapat kontradiksi preferensi yang melebihi batas acak, dilakukan perhitungan nilai eigen maksimum ($\lambda_{\max}$), indeks konsistensi (*Consistency Index* atau $CI$), dan rasio konsistensi (*Consistency Ratio* atau $CR$) berdasarkan formulasi Persamaan (2a) dan Persamaan (2b). Hasil pembobotan prioritas dan evaluasi konsistensi dirangkum pada Tabel 2.

Tabel 2. Hasil Pembobotan Prioritas Kriteria dan Parameter Evaluasi Konsistensi  
*(Format cetak: Judul 10 pt, isi sel 8 pt, layout garis horizontal tanpa garis vertikal)*

| Kode Kriteria | Deskripsi Kriteria Evaluasi | Nilai Eigen Vector ($w_j$) | Persentase Bobot | Peringkat Prioritas |
| :--- | :--- | :---: | :---: | :---: |
| **$C_1$** | Biaya Beban Properti | 0,1333 | 13,33% | 3 |
| **$C_2$** | Keamanan Eksternal Kawasan | 0,0501 | 5,01% | 5 |
| **$C_3$** | Potensi Daya Beli Lingkungan | 0,4614 | 46,14% | 1 |
| **$C_4$** | Visibilitas Lokasi | 0,2258 | 22,58% | 2 |
| **$C_5$** | Fleksibilitas Perombakan Struktur Bangunan | 0,0271 | 2,71% | 6 |
| **$C_6$** | Aglomerasi / Kepadatan Sentra Emas | 0,1023 | 10,23% | 4 |
| **Total Akumulasi** | $\sum_{j=1}^6 w_j$ | 1,0000 | 100,00% | - |
| **Parameter Uji** | **Besaran Parameter Matematis** | **Nilai Numerik** | **Ambang Batas** | **Keterangan Status** |
| Ordo Matriks ($n$) | Jumlah Kriteria yang Dievaluasi | 6 | - | Sesuai Model |
| $\lambda_{\max}$ | Nilai Eigen Maksimum | 6,420 | - | Terpenuhi ($\ge n$) |
| $CI$ | *Consistency Index* | 0,084 | - | Valid |
| $RI$ | *Random Index* Saaty ($n=6$) | 1,24 | - | Standar Literatur |
| $CR$ | *Consistency Ratio* ($CI / RI$) | 0,0677 (6,77%) | $\le 0,10$ | Konsisten dan Valid |

Berdasarkan komputasi pada Tabel 2, kriteria potensi daya beli lingkungan ($C_3$) menempati urutan prioritas tertinggi dengan bobot sebesar 0,4614 (46,14%), disusul oleh kriteria visibilitas lokasi ($C_4$) dengan bobot 0,2258 (22,58%), dan biaya beban properti ($C_1$) dengan bobot 0,1333 (13,33%). Hasil pembobotan ini mencerminkan struktur industri ritel perhiasan emas, di mana keberhasilan komersial sangat ditentukan oleh konsentrasi konsumen berdaya beli tinggi serta keterlihatan fisik gerai dari koridor lalu lintas. Pada bagian pengujian konsistensi, diperoleh nilai eigen maksimum ($\lambda_{\max}$) sebesar 6,420, nilai $CI$ sebesar 0,084, dan nilai $CR$ sebesar 0,0677. Mengingat nilai $CR$ berada di bawah batas ambang 0,10 (atau 6,77% < 10%), matriks perbandingan berpasangan dinyatakan konsisten secara logis dan terbebas dari deviasi preferensi yang bersifat spekulatif.

### 2.3. Matriks Keputusan Alternatif Lokasi

Tahap evaluasi alternatif kandidat lokasi diselesaikan menggunakan metode Weighted Product guna mengamankan stabilitas urutan keputusan dari anomali pembalikan peringkat (*rank reversal*). Sebanyak lima kandidat lokasi di wilayah Daerah Istimewa Yogyakarta dinilai berdasarkan keenam kriteria yang telah dibobotkan, yaitu Sinduadi ($A_1$), Jl. Magelang ($A_2$), Babarsari ($A_3$), Taman Siswa ($A_4$), dan Malioboro Mall ($A_5$). Data kinerja masing-masing kandidat lokasi dihimpun dalam bentuk nilai riil (*crisp data*) dan diklasifikasikan ke dalam atribut biaya (*cost*) serta atribut keuntungan (*benefit*). Struktur data profil lokasi disajikan pada Tabel 3.

Tabel 3. Matriks Keputusan Alternatif Lokasi Ritel Perhiasan Emas  
*(Format cetak: Judul 10 pt, isi sel 8 pt, layout garis horizontal tanpa garis vertikal)*

| Kode | Nama Alternatif Lokasi | $C_1$ (Cost)<br>Biaya Sewa (Juta Rp) | $C_2$ (Benefit)<br>Keamanan (1-5) | $C_3$ (Benefit)<br>Daya Beli (1-5) | $C_4$ (Benefit)<br>Visibilitas (1-5) | $C_5$ (Benefit)<br>Struktur (1-5) | $C_6$ (Benefit)<br>Aglomerasi (1-5) |
| :---: | :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **$A_1$** | Sinduadi (Jl. Umbul Permai) | 130 | 3 | 4 | 5 | 5 | 2 |
| **$A_2$** | Jl. Magelang | 120 | 3 | 3 | 4 | 5 | 2 |
| **$A_3$** | Babarsari | 150 | 3 | 2 | 3 | 5 | 1 |
| **$A_4$** | Taman Siswa | 250 | 3 | 4 | 5 | 5 | 3 |
| **$A_5$** | Malioboro Mall | 346,32 | 5 | 5 | 4 | 2 | 4 |

Data pada Tabel 3 bertindak sebagai matriks keputusan $X = [x_{ij}]_{5 \times 6}$ yang menjadi titik tolak komputasi metode Weighted Product. Kriteria biaya beban properti ($C_1$) berstatus sebagai atribut *cost*, sehingga nilai nominal yang lebih rendah memberikan kontribusi preferensi yang lebih menguntungkan bagi investor. Sebaliknya, kriteria $C_2$ hingga $C_6$ berstatus sebagai atribut *benefit*, di mana nilai skala yang semakin tinggi mencerminkan keunggulan karakteristik lokasi. Melalui metode Weighted Product, perbedaan dimensi satuan antara nominal rupiah pada $C_1$ dengan skala ordinal 1 hingga 5 pada kriteria lainnya dapat diproses secara langsung melalui operasi perkalian eksponensial tanpa memerlukan proses transformasi normalisasi linear antar kolom.

### 2.4. Preferensi Komputasi dan Pemeringkatan Akhir Alternatif

Komputasi pemeringkatan akhir diawali dengan menghitung nilai preferensi Vektor $S_i$ untuk setiap kandidat lokasi melalui formulasi Persamaan (3b). Bobot kriteria $w_j$ yang diperoleh dari metode AHP diterapkan sebagai eksponen matematis, yaitu bernilai negatif untuk atribut biaya ($-w_1 = -0{,}1333$) dan bernilai positif untuk atribut keuntungan ($+w_2$ hingga $+w_6$). Nilai preferensi relatif Vektor $V_i$ kemudian dihitung dengan menormalisasi setiap nilai $S_i$ terhadap jumlah total Vektor $S$ seluruh alternatif berdasarkan formulasi Persamaan (4). Urutan peringkat akhir disusun berdasarkan nilai preferensi Vektor $V$ dari yang tertinggi hingga terendah sebagaimana disajikan pada Tabel 4.

Tabel 4. Hasil Perhitungan Preferensi Vektor S, Vektor V, dan Pemeringkatan Akhir  
*(Format cetak: Judul 10 pt, isi sel 8 pt, layout garis horizontal tanpa garis vertikal)*

| Peringkat | Kode | Nama Alternatif Lokasi | Nilai Vektor $S$ | Nilai Vektor $V$ | Persentase Preferensi | Rekomendasi Keputusan |
| :---: | :---: | :--- | :---: | :---: | :---: | :--- |
| **1** | **$A_1$** | **Sinduadi (Jl. Umbul Permai)** | **1,6934** | **0,2302** | **23,02%** | **Prioritas Utama (Terpilih)** |
| **2** | **$A_5$** | Malioboro Mall | 1,6501 | 0,2243 | 22,43% | Alternatif Kedua |
| **3** | **$A_4$** | Taman Siswa | 1,5872 | 0,2158 | 21,58% | Alternatif Ketiga |
| **4** | **$A_2$** | Jl. Magelang | 1,4246 | 0,1937 | 19,37% | Alternatif Keempat |
| **5** | **$A_3$** | Babarsari | 1,0006 | 0,1360 | 13,60% | Alternatif Kelima |
| - | - | **Total Akumulasi** | **7,3559** | **1,0000** | **100,00%** | - |

Berdasarkan hasil pemeringkatan pada Tabel 4, alternatif $A_1$ (Sinduadi) menempati peringkat pertama dengan nilai Vektor $S$ sebesar 1,6934 dan nilai preferensi relatif Vektor $V$ tertinggi, yaitu 0,2302 (23,02%). Peringkat kedua ditempati oleh alternatif $A_5$ (Malioboro Mall) dengan nilai Vektor $V$ sebesar 0,2243 (22,43%), disusul oleh $A_4$ (Taman Siswa) dengan nilai 0,2158 (21,58%), $A_2$ (Jl. Magelang) dengan nilai 0,1937 (19,37%), dan $A_3$ (Babarsari) pada peringkat terakhir dengan nilai 0,1360 (13,60%).

Secara komputasional dan operasional, keunggulan lokasi $A_1$ (Sinduadi) terbentuk karena alternatif ini menawarkan titik kompromi terbaik (*optimal trade-off*) antara aspek biaya dan atribut keuntungan. Alternatif $A_5$ (Malioboro Mall) mencatatkan nilai tertinggi pada kriteria potensi daya beli ($C_3 = 5$) dan keamanan kawasan ($C_2 = 5$), namun beban sewa tahunan yang sangat tinggi (346,32 juta rupiah) memberikan beban penalti eksponensial negatif yang substansial pada komputasi Vektor $S$. Di sisi lain, lokasi $A_1$ (Sinduadi) menyajikan efisiensi biaya sewa yang moderat (130 juta rupiah) yang dipadukan dengan performa tinggi pada visibilitas ruang (skor 5), fleksibilitas modifikasi struktur brankas tonase berat (skor 5), serta potensi daya beli lingkungan yang kuat (skor 4). Hasil pemeringkatan pada Tabel 4 secara lugas membuktikan efektivitas integrasi AHP-WP dalam menghasilkan rekomendasi lokasi investasi ritel perhiasan emas yang objektif, konsisten, dan stabil.
