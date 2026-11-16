# B. LANDASAN TEORI

## B.2. Penulisan Tabel

Penyajian data numerik dan tahapan komputasi pada model hibrida ini disusun secara sistematis ke dalam bentuk tabel yang terstruktur. Berdasarkan pedoman template penulisan jurnal ilmiah, judul tabel ditempatkan tepat di bagian atas tabel pada posisi rata kiri dengan ukuran huruf 10 pt dalam format Title Case, sedangkan isi sel tabel itu menggunakan ukuran huruf 8 pt. Tata letak tabel menerapkan format baku yang hanya memanfaatkan garis pembatas horizontal tanpa menggunakan garis vertikal. Setiap tabel dirujuk secara berurutan di dalam teks naskah untuk memandu pemahaman pembaca.

### B.2.1. Matriks Perbandingan Berpasangan Kriteria AHP

Pemodelan keputusan diawali dengan pengisian matriks perbandingan berpasangan untuk menentukan tingkat kepentingan relatif dari enam kriteria evaluasi yang dianalisis dalam penelitian ini. Kriteria tersebut mencakup biaya beban properti ($C_1$), keamanan eksternal kawasan ($C_2$), potensi daya beli lingkungan ($C_3$), visibilitas lokasi ($C_4$), fleksibilitas perombakan struktur bangunan ($C_5$), serta aglomerasi sentra niaga emas ($C_6$). Setiap pasang parameter dikuantifikasi menggunakan skala fundamental Saaty yang bernilai antara 1 hingga 9. Rekapitulasi matriks perbandingan berpasangan tersebut disajikan pada Tabel 1.

Tabel 1. Matriks Perbandingan Berpasangan Kriteria Pembobotan AHP
> *Format cetak: Judul 10 pt, isi sel 8 pt, layout garis horizontal tanpa garis vertikal.*

| Kriteria | $C_1$ (Biaya) | $C_2$ (Keamanan) | $C_3$ (Daya Beli) | $C_4$ (Visibilitas) | $C_5$ (Struktur) | $C_6$ (Aglomerasi) |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **$C_1$ (Biaya)** | 1 | 5 | 1/5 | 1/3 | 7 | 1 |
| **$C_2$ (Keamanan)** | 1/5 | 1 | 1/7 | 1/5 | 3 | 1/3 |
| **$C_3$ (Daya Beli)** | 5 | 7 | 1 | 3 | 9 | 7 |
| **$C_4$ (Visibilitas)** | 3 | 5 | 1/3 | 1 | 7 | 3 |
| **$C_5$ (Struktur)** | 1/7 | 1/3 | 1/9 | 1/7 | 1 | 1/5 |
| **$C_6$ (Aglomerasi)** | 1 | 3 | 1/7 | 1/3 | 5 | 1 |
| **Total Kolom** | 10,3429 | 21,3333 | 1,9206 | 5,0095 | 32,0000 | 12,5333 |

Sebagaimana disajikan pada Tabel 1, setiap elemen diagonal utama bernilai 1 karena membandingkan kriteria dengan dirinya sendiri. Elemen di bawah diagonal utama merupakan nilai resiprokal dari elemen di atasnya sesuai dengan aksioma perbandingan berpasangan. Baris paling bawah tersebut menunjukkan akumulasi penjumlahan kolom yang difungsikan sebagai faktor penormalisasi dalam proses sintesis vektor bobot prioritas. Kriteria potensi daya beli lingkungan menghasilkan nilai total kolom paling kecil, yaitu 1,9206. Angka tersebut membuktikan bahwa kriteria daya beli dinilai jauh lebih dominan terhadap kriteria lainnya. Nilai total kolom terkecil mencerminkan prioritas tertinggi.

### B.2.2. Sintesis Bobot Kriteria dan Evaluasi Rasio Konsistensi

Normalisasi matriks perbandingan berpasangan dilakukan dengan membagi setiap elemen sel terhadap total kolomnya, lalu merata-ratakan nilai baris sesuai dengan formulasi Persamaan (1). Tahapan komputasi ini dilakukan untuk menghasilkan vektor bobot prioritas kriteria. Logika penilaian itu kemudian dapat diuji secara menyeluruh melalui perhitungan nilai eigen maksimum beserta rasio konsistensi logisnya. Rangkuman hasil pembobotan prioritas dan evaluasi konsistensi tersebut disajikan pada Tabel 2.

Tabel 2. Hasil Pembobotan Prioritas Kriteria dan Parameter Evaluasi Konsistensi
> *Format cetak: Judul 10 pt, isi sel 8 pt, layout garis horizontal tanpa garis vertikal.*

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

Berdasarkan komputasi pada Tabel 2, kriteria potensi daya beli lingkungan menempati urutan prioritas tertinggi dengan bobot sebesar 0,4614 (46,14%). Posisi kedua ditempati oleh visibilitas lokasi dengan bobot 0,2258 (22,58%), disusul oleh biaya beban properti sebesar 0,1333 (13,33%). Distribusi pembobotan ini mencerminkan karakteristik spasial di Daerah Istimewa Yogyakarta, dengan koridor primer yang ramai mengungguli kawasan sekitar kampus karena konsentrasi konsumen berdaya beli tinggi menjadi penentu utama perputaran transaksi. Pada pengujian konsistensi, diperoleh nilai eigen maksimum sebesar 6,420 dan rasio konsistensi sebesar 0,0677. Mengingat angka tersebut berada di bawah ambang batas 0,10, struktur preferensi yang dianalisis ini dinyatakan konsisten dan valid. Temuan ini membuktikan konsistensi penilaian.

### B.2.3. Matriks Keputusan Alternatif Lokasi

Penilaian terhadap lima kandidat lokasi di Daerah Istimewa Yogyakarta dilaksanakan untuk mengamankan stabilitas keputusan dari anomali pembalikan peringkat. Evaluasi ini mencakup lima kawasan alternatif di Daerah Istimewa Yogyakarta: Sinduadi ($A_1$), Jalan Magelang ($A_2$), Babarsari ($A_3$), Taman Siswa ($A_4$), dan Malioboro Mall ($A_5$). Data kinerja masing-masing kandidat dikompilasi ke dalam nilai riil dan diklasifikasikan ke dalam atribut keuntungan serta atribut biaya. Profil data awal untuk seluruh lokasi tersebut disajikan pada Tabel 3.

Tabel 3. Matriks Keputusan Alternatif Lokasi Ritel Perhiasan Emas
> *Format cetak: Judul 10 pt, isi sel 8 pt, layout garis horizontal tanpa garis vertikal.*

| Kode | Nama Alternatif Lokasi | $C_1$ (Cost)<br>Biaya Sewa (Juta Rp) | $C_2$ (Benefit)<br>Keamanan (1-5) | $C_3$ (Benefit)<br>Daya Beli (1-5) | $C_4$ (Benefit)<br>Visibilitas (1-5) | $C_5$ (Benefit)<br>Struktur (1-5) | $C_6$ (Benefit)<br>Aglomerasi (1-5) |
| :---: | :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **$A_1$** | Sinduadi (Jl. Umbul Permai) | 130 | 3 | 4 | 5 | 5 | 2 |
| **$A_2$** | Jl. Magelang | 120 | 3 | 3 | 4 | 5 | 2 |
| **$A_3$** | Babarsari | 150 | 3 | 2 | 3 | 5 | 1 |
| **$A_4$** | Taman Siswa | 250 | 3 | 4 | 5 | 5 | 3 |
| **$A_5$** | Malioboro Mall | 346,32 | 5 | 5 | 4 | 2 | 4 |

Data pada Tabel 3 bertindak sebagai matriks keputusan yang menjadi titik tolak komputasi metode pemeringkatan. Kriteria biaya beban properti berstatus sebagai atribut biaya sehingga nilai yang lebih rendah akan memberikan kontribusi preferensi yang lebih menguntungkan bagi investor. Sebaliknya, lima kriteria lainnya berstatus sebagai atribut keuntungan dengan nilai yang lebih tinggi mencerminkan performa lokasi yang lebih unggul. Melalui operasi perkalian eksponensial ini, disparitas dimensi ukuran antara biaya sewa bernilai ratusan juta rupiah dan skor kualitatif dapat diproses secara langsung tanpa proses transformasi normalisasi antarkolom. Karakteristik ini menyederhanakan perhitungan data.

### B.2.4. Komputasi Preferensi dan Pemeringkatan Akhir Alternatif

Komputasi pemeringkatan akhir diawali dengan menghitung nilai preferensi Vektor S untuk setiap kandidat lokasi melalui formulasi perkalian eksponensial. Bobot kriteria hasil AHP diterapkan sebagai eksponen matematis, yaitu bernilai negatif untuk atribut biaya dan bernilai positif untuk kelima atribut keuntungan. Nilai preferensi relatif Vektor V kemudian dihitung dengan menormalisasi nilai Vektor S terhadap total akumulasi nilai seluruh alternatif. Urutan peringkat akhir kandidat lokasi tersebut disusun berdasarkan nilai Vektor V dari yang tertinggi hingga terendah sebagaimana disajikan pada Tabel 4.

Tabel 4. Hasil Perhitungan Preferensi Vektor S, Vektor V, dan Pemeringkatan Akhir
> *Format cetak: Judul 10 pt, isi sel 8 pt, layout garis horizontal tanpa garis vertikal.*

| Peringkat | Kode | Nama Alternatif Lokasi | Nilai Vektor $S$ | Nilai Vektor $V$ | Persentase Preferensi | Rekomendasi Keputusan |
| :---: | :---: | :--- | :---: | :---: | :---: | :--- |
| **1** | **$A_1$** | **Sinduadi (Jl. Umbul Permai)** | **1,6934** | **0,2302** | **23,02%** | **Prioritas Utama (Terpilih)** |
| **2** | **$A_5$** | Malioboro Mall | 1,6501 | 0,2243 | 22,43% | Alternatif Kedua |
| **3** | **$A_4$** | Taman Siswa | 1,5872 | 0,2158 | 21,58% | Alternatif Ketiga |
| **4** | **$A_2$** | Jl. Magelang | 1,4246 | 0,1937 | 19,37% | Alternatif Keempat |
| **5** | **$A_3$** | Babarsari | 1,0006 | 0,1360 | 13,60% | Alternatif Kelima |
| - | - | **Total Akumulasi** | **7,3559** | **1,0000** | **100,00%** | - |

Berdasarkan hasil pemeringkatan pada Tabel 4, alternatif Sinduadi menempati peringkat pertama dengan nilai preferensi relatif sebesar 0,2302 (23,02%). Malioboro Mall berada pada peringkat kedua dengan nilai 0,2243 (22,43%), disusul oleh Taman Siswa sebesar 0,2158 (21,58%), Jalan Magelang dengan skor 0,1937 (19,37%), dan Babarsari pada posisi terakhir dengan nilai 0,1360 (13,60%). Urutan ini menunjukkan stabilitas hasil.

Keunggulan lokasi Sinduadi terbentuk karena alternatif ini menawarkan keseimbangan yang paling menguntungkan antara aspek efisiensi biaya dan atribut keuntungan operasional. Lokasi Malioboro Mall memang mencatatkan skor tertinggi pada potensi daya beli dan keamanan kawasan, namun beban sewa tahunan yang mencapai 346,32 juta rupiah menimbulkan penalti eksponensial yang cukup besar pada komputasi Vektor S. Sebaliknya, lokasi Sinduadi menawarkan efisiensi biaya sewa yang moderat sebesar 130 juta rupiah yang dipadukan dengan visibilitas koridor yang tinggi serta keleluasaan renovasi struktur gedung untuk penempatan brankas berat. Hasil komputasi pada Tabel 4 ini membuktikan bahwa integrasi AHP-WP berhasil menetapkan rekomendasi lokasi investasi yang objektif dan konsisten.
