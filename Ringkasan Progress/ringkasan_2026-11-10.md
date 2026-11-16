# 🖥️ SLIDE PRESENTASI PROGRESS: REVISI & PEMOLESAN MANUSKRIP PAPER SPK
**Judul Paper:** Integrasi Metode AHP dan Weighted Product pada Penentuan Lokasi Strategis Bisnis Ritel Perhiasan (Toko Emas) di Daerah Istimewa Yogyakarta  
**Tanggal Progress:** 10 November 2026  
**Status GitHub:** Branch `main` | Commit `48de015` (Up-to-Date)

---

## 🎯 SLIDE 1: PENGANTAR & HIGHLIGHT UTAMA

### Mengapa Naskah Kita Perlu Dipoles?
> *"Sebelumnya, draf paper kita sudah punya data komputasi yang lengkap, tapi gaya penulisannya masih kaku, banyak kalimat berbelit-belit, dan argumennya belum 'membumi' dengan kondisi nyata di Yogyakarta. Hari ini, kita menyelaraskan naskah dengan prinsip **Clarity, Precision, dan Word Economy**."*

```
📊 STATISTIK GIT DIFF HARI INI
   4 Berkas Dipoles  |  +76 Baris Masuk  |  -75 Baris Keluar
   (Revisi murni substitusi kalimat presisi, 0% perubahan pada angka dan rumus)
```

---

## 📌 SLIDE 2: BAB PENDAHULUAN (`Draft_Pendahuluan.md`)
> **Fokus Revisi:** Membangun alur logika 5 tahap: dari tren emas 2025 → realita 4 zona Jogja → cacat *rank reversal* AHP → keunggulan WP → tujuan riset.

### 🔍 Komparasi Nyata Before vs After

#### 1. Pembuka Latar Belakang (Emas Safe Haven & Gerai Fisik)
| 🔴 SEBELUM (Draf Lama) | 🟢 SESUDAH (Draf Revisi) |
| :--- | :--- |
| *"Komoditas emas **mencatatkan rekor lonjakan harga tertinggi** pada tahun 2025 sebagai refleksi langsung dari ketidakpastian ekonomi global dan pelemahan nilai tukar rupiah. Meskipun harga mengalami volatilitas yang tajam, emas secara konsisten dipertahankan oleh masyarakat sebagai aset pelindung nilai (*safe haven asset*) utama di tengah gejolak pasar [1]. Fenomena lonjakan harga ini secara empiris tidak menyurutkan minat beli, melainkan memicu pergeseran preferensi transaksi ke produk yang lebih fleksibel, di mana 41,7% masyarakat beralih pada produk cicil emas dan 25% memilih tabungan emas fisik. **Tingginya adaptabilitas dan resiliensi permintaan pasar tersebut mendorong ekspansi agresif jaringan ritel toko emas fisik**, mengingat transaksi logam mulia menuntut kehadiran gerai konvensional..."* | *"**Harga emas mencatat titik tertinggi sepanjang sejarah** pada tahun 2025, didorong oleh ketidakpastian ekonomi global dan pelemahan nilai tukar rupiah [1]. Volatilitas harga ini tidak meredam minat beli; **sebaliknya, masyarakat menggeser preferensi transaksi ke instrumen yang lebih likuid: 41,7% beralih ke produk cicil emas dan 25% ke tabungan emas fisik.** Pergeseran ini membuktikan bahwa permintaan terhadap emas sebagai aset pelindung nilai (*safe haven*) bersifat struktural, bukan spekulatif. **Akibatnya, jaringan gerai ritel emas fisik menghadapi tekanan ekspansi yang kuat.** Gerai konvensional tetap diperlukan karena tiga fungsi yang tidak dapat didigitalisasi: verifikasi keaslian kadar secara langsung, penyimpanan berkeamanan tinggi, dan likuiditas instan fisik."* |

💡 **Kenapa Diubah?**  
Draf lama memaksakan 4 ide rumit ke dalam satu kalimat raksasa (50+ kata). Draf baru memecahnya: **1 kalimat = 1 argumen jelas** dengan kata transisi tegas (*"sebaliknya"*, *"Akibatnya"*). Tiga alasan butuh toko fisik langsung dirinci padat.

---

#### 2. Konteks Wilayah Jogja (Dari Abstrak Menjadi Konkret Spasial)
| 🔴 SEBELUM (Draf Lama) | 🟢 SESUDAH (Draf Revisi) |
| :--- | :--- |
| *"Urgensi ekspansi gerai fisik tersebut secara nyata dihadapi oleh pelaku usaha ritel perhiasan di wilayah aglomerasi Daerah Istimewa Yogyakarta. Sebagai kawasan strategis yang memadukan pusat niaga pariwisata, koridor perkuliahan padat, serta zona hunian suburban... Kendati demikian, penentuan lokasi cabang gerai baru dalam praktik bisnis kerap kali masih mengandalkan intuisi subjektif dan pertimbangan spekulatif pemilik modal."* | *"Tekanan ekspansi tersebut nyata dirasakan di wilayah Daerah Istimewa Yogyakarta, di mana heterogenitas zona niaga menghadirkan pilihan lokasi yang kompleks. **Koridor pariwisata Malioboro menawarkan lalu lintas tinggi namun beban sewa yang sangat mahal; koridor primer Jl. Magelang dan Sinduadi menyajikan keseimbangan biaya-visibilitas yang berbeda; sementara kawasan padat mahasiswa Babarsari dan Taman Siswa memiliki profil daya beli yang tidak setara.** Dalam kondisi ini, penentuan lokasi gerai baru tidak dapat disandarkan pada intuisi pemilik modal."* |

💡 **Kenapa Diubah?**  
Draf lama terlalu umum. Draf baru **langsung menyebut 4 zona nyata DIY** beserta dilema bisnisnya masing-masing. Audience langsung paham kenapa pemilihan lokasi di Jogja itu menantang dan butuh SPK.

---

#### 3. Kritik Tajam Metodologi (AHP Cacat Rank Reversal vs WP Anti-Oleng)
| 🔴 SEBELUM (Draf Lama) | 🟢 SESUDAH (Draf Revisi) |
| :--- | :--- |
| *"Studi teoretis membuktikan bahwa anomali rank reversal pada AHP berakar dari skema normalisasi penjumlahan aditif berbasis jumlah kolom matriks lokal... Seluruh prosedur pemeringkatan alternatif **sengaja diamputasi dan dieliminasi** dari domain komputasi AHP..."* | *"Penyebab matematis anomali ini telah diidentifikasi: **skema normalisasi AHP membagi setiap elemen kolom dengan total kolomnya, sehingga nilai setiap alternatif bergantung pada jumlah dan komposisi alternatif lain dalam gugus.** Dependensi lintas-alternatif ini secara langsung melanggar aksioma *Independence of Irrelevant Alternatives* (IIA). Karena itu, penelitian ini mengambil posisi metodologis yang eksplisit: **AHP dibatasi hanya pada fase sintesis bobot prioritas kriteria global dan verifikasi konsistensi ($CR \le 0{,}10$). Fase pemeringkatan alternatif sepenuhnya diserahkan kepada metode yang secara struktural kebal (WP).**"* |

💡 **Kenapa Diubah?**  
Kata *"diamputasi"* di draf lama terasa bombastis/tidak baku. Draf baru menjelaskan **akar matematisnya** (pelanggaran aksioma IIA akibat pembagian kolom) sehingga argumen kita solid dan berbobot akademis.

---

## 📌 SLIDE 3: BAB PERSAMAAN MATEMATIKA (`Draft_Persamaan_Matematika.md`)
> **Fokus Revisi:** Rumus tidak lagi "ujug-ujug muncul"; ada narasi pengantar, pembersihan simbol pada judul, serta pembuktian matematis kekebalan WP.

### 🔍 Komparasi Nyata Before vs After

#### 1. Perapian Judul Sub-Bab (Bebas Titik Dua dan Ampersand)
* 🔴 **Sebelum:** `### 1.1. Multi-Criteria Decision Making (MCDM) & Matriks Keputusan`
* 🟢 **Sesudah:** `### 1.1. Multi-Criteria Decision Making (MCDM) dan Matriks Keputusan`
* 🔴 **Sebelum:** `#### D. Persamaan 4: Perhitungan Nilai Preferensi Relatif (Vektor V_i) & Pemeringkatan Akhir`
* 🟢 **Sesudah:** `#### D. Persamaan 4 untuk Penentuan Preferensi Relatif Vektor V_i dan Pemeringkatan Akhir`

#### 2. Keterangan Dimensi Riil pada Matriks Keputusan
| 🔴 SEBELUM (Draf Lama) | 🟢 SESUDAH (Draf Revisi) |
| :--- | :--- |
| *"...di mana $x_{ij}$ menyatakan nilai kinerja alternatif ke-$i$ pada kriteria ke-$j$. Sistem komputasi bertujuan menemukan solusi kompromi terbaik (*compromise solution*) yang memenuhi prinsip non-dominasi Pareto."* | *"...di mana $x_{ij}$ adalah nilai kinerja alternatif ke-$i$ pada kriteria ke-$j$. **Dalam konteks penelitian ini, $m = 5$ kandidat lokasi dan $n = 6$ kriteria evaluasi membentuk matriks keputusan berukuran $5 \times 6$.**"* |

💡 **Kenapa Diubah?**  
Di draf baru, angka riil dataset ($5 \times 6$) langsung diikat ke teori dasar, sehingga pembaca langsung tahu ukuran matriks yang sedang dihitung.

#### 3. Bukti Aljabar Kenapa WP Kebal Perubahan Opsi (Invariansi Rasio)
Tampilkan rumus elegan ini ke audience:
$$\frac{S_a}{S_b} = \frac{\prod_{j=1}^n \left( x_{aj} \right)^{W_j^*}}{\prod_{j=1}^n \left( x_{bj} \right)^{W_j^*}} = \prod_{j=1}^n \left( \frac{x_{aj}}{x_{bj}} \right)^{W_j^*}$$

| 🔴 SEBELUM (Draf Lama) | 🟢 SESUDAH (Draf Revisi) |
| :--- | :--- |
| *"Formulasi di atas membuktikan bahwa rasio $S_a / S_b$ **bersifat invarian murni**. Rasio preferensi hanya ditentukan secara eksklusif oleh kinerja intrinsik alternatif a dan b serta bobot kriteria terkait, tanpa memuat elemen dari alternatif ketiga..."* | *"**Rasio $S_a / S_b$ hanya bergantung pada nilai intrinsik $A_a$ dan $A_b$ serta bobot kriteria $W_j^*$. Tidak ada suku yang mengandung nilai alternatif ketiga $A_c$.** Oleh karena itu, jika $S_a > S_b$, hubungan ini tetap berlaku terlepas dari penambahan atau penghapusan alternatif lain, sehingga aksioma IIA terpenuhi."* |

💡 **Kenapa Diubah?**  
Frasa klise *"invarian murni"* diganti dengan penjelasan logika yang gamblang: perbandingan Toko A dan Toko B sama sekali tidak memuat unsur Toko C!

---

## 📌 SLIDE 4: BAB PENULISAN TABEL (`Draft_Penulisan_Tabel.md`)
> **Fokus Revisi:** Memperbaiki typo, membuang kalimat pasif, dan menghubungkan angka bobot AHP langsung ke realita 5 kawasan di DIY.

### 🔍 Komparasi Nyata Before vs After

#### 1. Perbaikan Typo & Kalimat Berbelit di Paragraf Pembuka
* 🔴 **Sebelum:** *"Tahap awal **permodelan** keputusan dimulai dari penentuan preferensi pengambil keputusan terhadap kepentingan relatif kriteria pemilihan lokasi toko emas... Penilaian preferensi antar kriteria dikuantifikasi menggunakan **skala** fundamental Saaty (**skala** 1 hingga 9)."*
* 🟢 **Sesudah:** *"**Pemodelan** keputusan diawali dengan pengisian matriks perbandingan berpasangan untuk menentukan kepentingan relatif enam kriteria spasial dan operasional... Setiap pasang kriteria dikuantifikasi menggunakan skala fundamental Saaty (1 hingga 9)."*
* 💡 **Masalah yang Diperbaiki:** Typo kata *"permodelan"* menjadi *"pemodelan"*; pemborosan kata *"skala"* yang diulang dua kali dihapus; struktur kalimat diubah jadi kalimat aktif.

---

#### 2. Interpretasi Hasil Bobot Kriteria (Tabel 2)
Hasil AHP: $C_3$ (Daya Beli) = **$46{,}14\%$**, $C_4$ (Visibilitas) = **$22{,}58\%$**, $C_1$ (Biaya) = **$13{,}33\%$**.

| 🔴 SEBELUM (Draf Lama) | 🟢 SESUDAH (Draf Revisi) |
| :--- | :--- |
| *"Hasil pembobotan ini mencerminkan **struktur industri ritel perhiasan emas**, di mana keberhasilan komersial sangat ditentukan oleh konsentrasi konsumen berdaya beli tinggi serta keterlihatan fisik gerai dari koridor lalu lintas."* | *"Distribusi pembobotan ini mencerminkan karakteristik spesifik zona komersial di Daerah Istimewa Yogyakarta: **koridor primer Jl. Magelang-Sinduadi dan Malioboro mengungguli kawasan padat mahasiswa Babarsari dan Taman Siswa justru karena konsentrasi konsumen berdaya beli tinggi ($C_3$) dan keterlihatan fisik gerai dari koridor lalu lintas utama ($C_4$)** menjadi penentu daya saing komersial yang dominan."* |

💡 **Kenapa Diubah?**  
Draf lama hanya bicara *"struktur industri"* tanpa bukti. Draf baru langsung menjelaskan: **inilah alasan kenapa lokasi mahasiswa (Babarsari) kalah saing dibanding koridor Magelang/Sinduadi untuk toko perhiasan emas!**

---

#### 3. Bedah Pemenang Lokasi (Tabel 4)
* **Juara 1:** Sinduadi ($A_1$) — Nilai Preferensi $V = 0{,}2302$ ($23{,}02\%$)
* **Juara 2:** Malioboro Mall ($A_5$) — Nilai Preferensi $V = 0{,}2243$ ($22{,}43\%$)

| 🔴 SEBELUM (Draf Lama) | 🟢 SESUDAH (Draf Revisi) |
| :--- | :--- |
| *"...keunggulan lokasi $A_1$ (Sinduadi) terbentuk karena alternatif ini menawarkan **titik kompromi terbaik (*optimal trade-off*)** antara aspek biaya dan atribut keuntungan... Hasil pemeringkatan pada Tabel 4 **secara lugas** membuktikan efektivitas integrasi AHP-WP..."* | *"...keunggulan lokasi $A_1$ (Sinduadi) terbentuk karena alternatif ini menawarkan ***trade-off* yang paling menguntungkan** antara aspek biaya dan atribut keuntungan... Hasil pemeringkatan pada Tabel 4 **membuktikan** efektivitas integrasi AHP-WP dalam menghasilkan rekomendasi lokasi yang objektif, konsisten, dan stabil."* |

💡 **Kenapa Diubah?**  
Menghapus pemborosan kata *"titik kompromi terbaik"* (cukup *"trade-off yang paling menguntungkan"*) dan membuang kata pengisi *"secara lugas"*.

---

## 📌 SLIDE 5: BAB PENGGUNAAN GAMBAR (`Draft_Penggunaan_Gambar.md`)
> **Fokus Revisi:** Membuang diksi bombastis, memperjelas batas titik potong (*cut-off*) pada diagram alir.

### 🔍 Komparasi Nyata Before vs After

| Titik Evaluasi | 🔴 SEBELUM (Draf Lama) | 🟢 SESUDAH (Draf Revisi) | Catatan Perbaikan |
| :--- | :--- | :--- | :--- |
| **Pengantar Gambar 2** | *"..dengan menetapkan **batas demarkasi** komputasi yang tegas."* | *"..dengan **batas komputasi yang tegas antara fase pembobotan dan fase pemeringkatan**."* | Kata *"demarkasi"* berlebihan; diganti nama kedua fase agar informatif. |
| **Logika Titik Potong** | *"..penggunaan metode AHP **langsung dihentikan secara permanen**."* | *"..penggunaan metode AHP **dihentikan**."* | Redundansi ganda (*langsung* & *secara permanen*) dipangkas. |
| **Kalimat Penutup** | *"..memberikan **justifikasi ilmiah yang kuat** bagi pembuat keputusan.."* | *"..memberikan **landasan analitis** bagi pembuat keputusan.."* | Gaya bahasa bombastis dinetralkan menjadi bahasa akademik standar. |

---

## 🎤 SLIDE 6: CHEAT SHEET PRESENTASI (PANDUAN TANYA-JAWAB DOSEN)

### Q1: "Kenapa gak pakai AHP murni saja sampai selesai?"
> **Jawaban:**  
> *"Karena AHP menggunakan normalisasi penjumlahan kolom lokal. Jika nanti pemilik bisnis ingin menambah 1 alternatif baru di Jogja (misalnya di Gejayan), posisi peringkat alternatif lama bisa mendadak berbalik secara tidak logis (*rank reversal*). Untuk investasi bernilai miliaran rupiah, anomali ini sangat berbahaya."*

### Q2: "Kenapa gak pakai Weighted Product saja sejak awal?"
> **Jawaban:**  
> *"Metode WP tidak memiliki fitur perbandingan berpasangan (*pairwise comparison*) dan tidak bisa menguji konsistensi pembuat keputusan. Jadi penentuan bobot tetap paling unggul menggunakan AHP melalui validasi $CR \le 0{,}10$."*

### Q3: "Kenapa Malioboro Mall kalah dengan Sinduadi?"
> **Jawaban:**  
> *"Malioboro memang sempurna pada daya beli dan keamanan (skor 5). Namun, biaya sewanya sangat mahal (Rp 346,32 juta/tahun). Pada metode WP, biaya sewa dipangkatkan negatif ($-0{,}1333$), sehingga Malioboro terkena penalti eksponensial yang berat. Sinduadi keluar sebagai juara karena menyajikan biaya yang moderat (Rp 130 juta/tahun) dengan performa fisik yang seimbang."*

---

## ✅ KESIMPULAN REVISI (TAKEAWAY PRESENTASI)

1. **Alur Cerita Presisi:** Pembaca dipandu runtut dari motif finansial emas → realita sewa Jogja → isolasi kelemahan AHP → keunggulan aljabar WP.
2. **Kesesuaian Data 100%:** Seluruh narasi di Bab Pendahuluan, Persamaan, Tabel, dan Gambar sinkron dengan data komputasi riil ($CR = 0{,}0677$, Sinduadi = Peringkat 1).
3. **Format Naskah Baku Jurnal:** Bersih dari *em-dash* (`—`), tanpa tanda titik dua pada judul bab, bebas frasa klise AI, dan sitasi patuh pada format IEEE `[n]`.
