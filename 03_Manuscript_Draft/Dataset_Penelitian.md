# Dataset & Komputasi Numerik (AHP - WP)
**Studi Kasus:** Penentuan Lokasi Strategis Bisnis Ritel Perhiasan (Toko Emas)  
**Metode:** Hibrida Analytic Hierarchy Process (AHP) & Weighted Product (WP)

---

## 1. Definisi Operasional & Karakteristik Kriteria

| Kode | Nama Kriteria | Sifat Atribut | Logika Eksponensial (WP) | Deskripsi Operasional |
| :---: | :--- | :---: | :---: | :--- |
| **$C_1$** | Biaya Beban Properti | **Cost** | Negatif ($-w_1$) | Total biaya sewa dan beban operasional tetap tahunan gedung/ruang usaha dasar. Semakin rendah biaya, nilai preferensi semakin tinggi. |
| **$C_2$** | Keamanan Eksternal Kawasan | **Benefit** | Positif ($+w_2$) | Tingkat keamanan di luar kendali internal toko, mencakup jarak dari kantor polisi/aparat, patroli keamanan berkala, dan rekam jejak kriminalitas kawasan. |
| **$C_3$** | Potensi Daya Beli Lingkungan | **Benefit** | Positif ($+w_3$) | Kualitas lalu lintas pengunjung (*traffic*) berdasarkan probabilitas dan daya beli untuk transaksi perhiasan emas (membedakan pusat niaga/belanja dengan wisata biasa). |
| **$C_4$** | Visibilitas Lokasi | **Benefit** | Positif ($+w_4$) | Keterlihatan fisik bangunan dari koridor jalan utama/pejalan kaki untuk eksposur pemasaran sekaligus pengawasan visual alami (*natural surveillance*). |
| **$C_5$** | Fleksibilitas Perombakan Struktur Bangunan | **Benefit** | Positif ($+w_5$) | Kebebasan perizinan dari pemilik properti/pengelola gedung untuk memodifikasi struktur (pengeboran lantai brankas baja tonase berat, partisi kaca anti-peluru). |
| **$C_6$** | Aglomerasi / Kepadatan Sentra Emas | **Benefit** | Positif ($+w_6$) | Keberadaan dan konsentrasi gerai ritel perhiasan sejenis di area sekitar yang membentuk klaster pasar dan menarik konsumen tertarget. |

> **Hirarki Prioritas Keputusan:**  
> $$C_3 > C_4 > (C_1 = C_6) > C_2 > C_5$$

---

## 2. Matriks Perbandingan Berpasangan AHP (Pairwise Comparison)

$$
A = 
\begin{pmatrix}
1 & 5 & 1/5 & 1/3 & 7 & 1 \\
1/5 & 1 & 1/7 & 1/5 & 3 & 1/3 \\
5 & 7 & 1 & 3 & 9 & 7 \\
3 & 5 & 1/3 & 1 & 7 & 3 \\
1/7 & 1/3 & 1/9 & 1/7 & 1 & 1/5 \\
1 & 3 & 1/7 & 1/3 & 5 & 1
\end{pmatrix}
$$

### Tabel Perbandingan Berpasangan Skala Saaty:
| Kriteria | $C_1$ (Biaya) | $C_2$ (Keamanan) | $C_3$ (Daya Beli) | $C_4$ (Visibilitas) | $C_5$ (Struktur) | $C_6$ (Aglomerasi) |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **$C_1$** | $1$ | $5$ | $1/5$ | $1/3$ | $7$ | $1$ |
| **$C_2$** | $1/5$ | $1$ | $1/7$ | $1/5$ | $3$ | $1/3$ |
| **$C_3$** | $5$ | $7$ | $1$ | $3$ | $9$ | $7$ |
| **$C_4$** | $3$ | $5$ | $1/3$ | $1$ | $7$ | $3$ |
| **$C_5$** | $1/7$ | $1/3$ | $1/9$ | $1/7$ | $1$ | $1/5$ |
| **$C_6$** | $1$ | $3$ | $1/7$ | $1/3$ | $5$ | $1$ |
| **Total Kolom** | $10{,}3429$ | $21{,}3333$ | $1{,}9206$ | $5{,}0095$ | $32{,}0000$ | $12{,}5333$ |

---

## 3. Hasil Pembobotan AHP & Verifikasi Konsistensi

### Vektor Bobot Prioritas ($W$):
* $w_1$ ($C_1$ - Biaya Beban Properti): **$0{,}1333$** ($13{,}33\%$)
* $w_2$ ($C_2$ - Keamanan Eksternal Kawasan): **$0{,}0501$** ($5{,}01\%$)
* $w_3$ ($C_3$ - Potensi Daya Beli Lingkungan): **$0{,}4614$** ($46{,}14\%$)
* $w_4$ ($C_4$ - Visibilitas Lokasi): **$0{,}2258$** ($22{,}58\%$)
* $w_5$ ($C_5$ - Fleksibilitas Perombakan Struktur): **$0{,}0271$** ($2{,}71\%$)
* $w_6$ ($C_6$ - Aglomerasi / Kepadatan Sentra Emas): **$0{,}1023$** ($10{,}23\%$)
* **Total Akumulasi Bobot:** $\sum_{j=1}^6 w_j = 1{,}0000$ ($100{,}00\%$)

### Uji Konsistensi Matematis (Saaty Consistency):
* Nilai Eigen Maksimum ($\lambda_{\max}$): **$6{,}420$**
* Ordo Matriks ($n$): **$6$**
* *Consistency Index* ($CI$):
  $$CI = \frac{\lambda_{\max} - n}{n - 1} = \frac{6{,}420 - 6}{6 - 1} = \frac{0{,}420}{5} = 0{,}084$$
* *Random Index* ($RI$) untuk $n = 6$: **$1{,}24$**
* *Consistency Ratio* ($CR$):
  $$CR = \frac{CI}{RI} = \frac{0{,}084}{1{,}24} \approx 0{,}0677 \quad (6{,}77\%)$$
* **Kesimpulan:** Karena $CR = 0{,}0677 < 0{,}10$, matriks perbandingan berpasangan dinyatakan **konsisten dan valid secara matematis**.

---

## 4. Matriks Penilaian Alternatif Lokasi

| Kode | Nama Alternatif | Deskripsi Ringkas Lokasi | $C_1$ (Biaya - Juta Rp) | $C_2$ (Keamanan) | $C_3$ (Daya Beli) | $C_4$ (Visibilitas) | $C_5$ (Struktur) | $C_6$ (Aglomerasi) |
| :---: | :--- | :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **$A_1$** | Sinduadi (Jl. Umbul Permai) | Luas 210/218 m², lebar muka 12m, listrik 7000W | $130$ | $3$ | $4$ | $5$ | $5$ | $2$ |
| **$A_2$** | Jl. Magelang | Ruko 2 lantai, tepi jalan utama dekat JCM | $120$ | $3$ | $3$ | $4$ | $5$ | $2$ |
| **$A_3$** | Babarsari | Ruko 2 lantai, kawasan kampus, lebar 4,2m | $150$ | $3$ | $2$ | $3$ | $5$ | $1$ |
| **$A_4$** | Taman Siswa | Ruko hook 2 lantai, lebar 10m, akses padat | $250$ | $3$ | $4$ | $5$ | $5$ | $3$ |
| **$A_5$** | Malioboro Mall | Ruang usaha dalam mall pariwisata & pusat ritel | $346{,}32$ | $5$ | $5$ | $4$ | $2$ | $4$ |

*Keterangan:* Skala penilaian kualitatif $C_2$ s.d. $C_6$ menggunakan interval $1$ hingga $5$.

---

## 5. Komputasi Weighted Product (WP)

### A. Perhitungan Vektor Preferensi $S$ ($S_i$)
Formulasi umum:
$$S_i = (x_{i1})^{-0{,}1333} \times (x_{i2})^{+0{,}0501} \times (x_{i3})^{+0{,}4614} \times (x_{i4})^{+0{,}2258} \times (x_{i5})^{+0{,}0271} \times (x_{i6})^{+0{,}1023}$$

* **$S_1$ (Sinduadi):**
  $$S_1 = (130)^{-0{,}1333} \cdot (3)^{0{,}0501} \cdot (4)^{0{,}4614} \cdot (5)^{0{,}2258} \cdot (5)^{0{,}0271} \cdot (2)^{0{,}1023} = \mathbf{1{,}6934}$$
* **$S_2$ (Jl. Magelang):**
  $$S_2 = (120)^{-0{,}1333} \cdot (3)^{0{,}0501} \cdot (3)^{0{,}4614} \cdot (4)^{0{,}2258} \cdot (5)^{0{,}0271} \cdot (2)^{0{,}1023} = \mathbf{1{,}4246}$$
* **$S_3$ (Babarsari):**
  $$S_3 = (150)^{-0{,}1333} \cdot (3)^{0{,}0501} \cdot (2)^{0{,}4614} \cdot (3)^{0{,}2258} \cdot (5)^{0{,}0271} \cdot (1)^{0{,}1023} = \mathbf{1{,}0006}$$
* **$S_4$ (Taman Siswa):**
  $$S_4 = (250)^{-0{,}1333} \cdot (3)^{0{,}0501} \cdot (4)^{0{,}4614} \cdot (5)^{0{,}2258} \cdot (5)^{0{,}0271} \cdot (3)^{0{,}1023} = \mathbf{1{,}5872}$$
* **$S_5$ (Malioboro Mall):**
  $$S_5 = (346{,}32)^{-0{,}1333} \cdot (5)^{0{,}0501} \cdot (5)^{0{,}4614} \cdot (4)^{0{,}2258} \cdot (2)^{0{,}0271} \cdot (4)^{0{,}1023} = \mathbf{1{,}6501}$$

**Total Akumulasi Vektor $S$:**
$$\sum_{k=1}^5 S_k = 1{,}6934 + 1{,}4246 + 1{,}0006 + 1{,}5872 + 1{,}6501 = \mathbf{7{,}3559}$$

---

### B. Perhitungan Vektor Preferensi Relatif $V$ ($V_i$) & Pemeringkatan Akhir
Formulasi normalisasi:
$$V_i = \frac{S_i}{\sum_{k=1}^5 S_k}$$

| Peringkat | Kode | Alternatif Lokasi | Nilai Vektor $S$ | Nilai Vektor $V$ | Persentase Preferensi | Status Rekomendasi |
| :---: | :---: | :--- | :---: | :---: | :---: | :--- |
| **1** | **$A_1$** | **Sinduadi (Jl. Umbul Permai)** | $\mathbf{1{,}6934}$ | $\mathbf{0{,}2302}$ | **$23{,}02\%$** | **Prioritas Utama (Terpilih)** |
| **2** | **$A_5$** | Malioboro Mall | $1{,}6501$ | $0{,}2243$ | $22{,}43\%$ | Alternatif Kedua |
| **3** | **$A_4$** | Taman Siswa | $1{,}5872$ | $0{,}2158$ | $21{,}58\%$ | Alternatif Ketiga |
| **4** | **$A_2$** | Jl. Magelang | $1{,}4246$ | $0{,}1937$ | $19{,}37\%$ | Alternatif Keempat |
| **5** | **$A_3$** | Babarsari | $1{,}0006$ | $0{,}1360$ | $13{,}60\%$ | Alternatif Kelima |
