# Dataset & Komputasi Numerik Terverifikasi (AHP - WP & Evaluasi)
**Studi Kasus:** Penentuan Lokasi Strategis Bisnis Ritel Perhiasan (Toko Emas) di D.I. Yogyakarta  
**Metode:** Hibrida Analytic Hierarchy Process (AHP) & Weighted Product (WP)  
**Status Audit Numerik:** Terverifikasi presisi ganda (IEEE-754) — nilai acuan menggunakan bobot normalisasi rata-rata baris eksak (tampilan tabel dibulatkan 4 angka di belakang koma).

---

## 1. Definisi Operasional & Karakteristik Kriteria

| Kode | Nama Kriteria | Sifat Atribut | Logika Eksponensial (WP) | Deskripsi Operasional |
| :---: | :--- | :---: | :---: | :--- |
| **$C_1$** | Biaya Beban Properti | **Cost** | Negatif ($-w_1$) | Total biaya sewa dan beban operasional tetap tahunan gedung/ruang usaha dasar (Juta Rp/tahun). Semakin rendah biaya, nilai preferensi semakin tinggi. |
| **$C_2$** | Keamanan Eksternal Kawasan | **Benefit** | Positif ($+w_2$) | Tingkat keamanan di luar kendali internal toko, mencakup jarak dari kantor polisi/aparat, patroli keamanan berkala, dan rekam jejak kriminalitas kawasan (skala 1–5). |
| **$C_3$** | Potensi Daya Beli Lingkungan | **Benefit** | Positif ($+w_3$) | Kualitas lalu lintas pengunjung (*traffic*) berdasarkan probabilitas dan daya beli untuk transaksi perhiasan emas (membedakan pusat niaga/belanja dengan wisata biasa, skala 1–5). |
| **$C_4$** | Visibilitas Lokasi | **Benefit** | Positif ($+w_4$) | Keterlihatan fisik bangunan dari koridor jalan utama/pejalan kaki untuk eksposur pemasaran sekaligus pengawasan visual alami (*natural surveillance*, skala 1–5). |
| **$C_5$** | Fleksibilitas Perombakan Struktur Bangunan | **Benefit** | Positif ($+w_5$) | Kebebasan perizinan dari pemilik properti/pengelola gedung untuk memodifikasi struktur (pengeboran lantai brankas baja tonase berat, partisi kaca anti-peluru, skala 1–5). |
| **$C_6$** | Aglomerasi / Kepadatan Sentra Emas | **Benefit** | Positif ($+w_6$) | Keberadaan dan konsentrasi gerai ritel perhiasan sejenis di area sekitar yang membentuk klaster pasar dan menarik konsumen tertarget (skala 1–5). |

> **Urutan Hierarki Prioritas Hasil Sintesis AHP:**  
> $$C_3 > C_4 > C_1 > C_6 > C_2 > C_5$$
> *(Catatan: meskipun pada perbandingan berpasangan langsung $a_{16} = 1$, bobot global hasil sintesis menunjukkan $w_1 = 0{,}1333 > w_6 = 0{,}1023$ karena dominasi $C_1$ terhadap $C_2$, $C_3$, dan $C_5$ lebih tinggi dibanding $C_6$.)*

---

## 2. Matriks Perbandingan Berpasangan AHP (*Pairwise Comparison*)

Penilaian matriks perbandingan berpasangan disusun berdasarkan asumsi dan penilaian tim peneliti menggunakan skala fundamental Saaty (1–9):

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

### Tabel 1. Matriks Perbandingan Berpasangan Skala Saaty
| Kriteria | $C_1$ (Biaya) | $C_2$ (Keamanan) | $C_3$ (Daya Beli) | $C_4$ (Visibilitas) | $C_5$ (Struktur) | $C_6$ (Aglomerasi) |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **$C_1$** | $1$ | $5$ | $1/5$ | $1/3$ | $7$ | $1$ |
| **$C_2$** | $1/5$ | $1$ | $1/7$ | $1/5$ | $3$ | $1/3$ |
| **$C_3$** | $5$ | $7$ | $1$ | $3$ | $9$ | $7$ |
| **$C_4$** | $3$ | $5$ | $1/3$ | $1$ | $7$ | $3$ |
| **$C_5$** | $1/7$ | $1/3$ | $1/9$ | $1/7$ | $1$ | $1/5$ |
| **$C_6$** | $1$ | $3$ | $1/7$ | $1/3$ | $5$ | $1$ |
| **Total Kolom** | **$10{,}3429$** | **$21{,}3333$** | **$1{,}9302$** | **$5{,}0095$** | **$32{,}0000$** | **$12{,}5333$** |

---

## 3. Normalisasi Matriks, Pembobotan AHP, & Verifikasi Konsistensi

### Tabel 2. Matriks Normalisasi Kolom & Vektor Bobot Prioritas ($w_j$)
| Kriteria | $C_1$ | $C_2$ | $C_3$ | $C_4$ | $C_5$ | $C_6$ | Jumlah Baris | Bobot ($w_j$) | Persentase | Peringkat |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **$C_1$** | $0{,}0967$ | $0{,}2344$ | $0{,}1036$ | $0{,}0665$ | $0{,}2188$ | $0{,}0798$ | $0{,}7998$ | **$0{,}1333$** | $13{,}33\%$ | 3 |
| **$C_2$** | $0{,}0193$ | $0{,}0469$ | $0{,}0740$ | $0{,}0399$ | $0{,}0938$ | $0{,}0266$ | $0{,}3005$ | **$0{,}0501$** | $5{,}01\%$ | 5 |
| **$C_3$** | $0{,}4834$ | $0{,}3281$ | $0{,}5181$ | $0{,}5989$ | $0{,}2813$ | $0{,}5585$ | $2{,}7683$ | **$0{,}4614$** | $46{,}14\%$ | 1 |
| **$C_4$** | $0{,}2901$ | $0{,}2344$ | $0{,}1727$ | $0{,}1996$ | $0{,}2188$ | $0{,}2394$ | $1{,}3549$ | **$0{,}2258$** | $22{,}58\%$ | 2 |
| **$C_5$** | $0{,}0138$ | $0{,}0156$ | $0{,}0576$ | $0{,}0285$ | $0{,}0313$ | $0{,}0160$ | $0{,}1627$ | **$0{,}0271$** | $2{,}71\%$ | 6 |
| **$C_6$** | $0{,}0967$ | $0{,}1406$ | $0{,}0740$ | $0{,}0665$ | $0{,}1563$ | $0{,}0798$ | $0{,}6139$ | **$0{,}1023$** | $10{,}23\%$ | 4 |
| **Total** | **$1{,}0000$** | **$1{,}0000$** | **$1{,}0000$** | **$1{,}0000$** | **$1{,}0000$** | **$1{,}0000$** | **$6{,}0000$** | **$1{,}0000$** | **$100{,}00\%$** | - |

### Uji Konsistensi Matematis (Saaty Consistency)
Vektor jumlah berbobot $(A \cdot w)$ dan rasio konsistensi per kriteria $(A \cdot w)_j / w_j$:

| Kriteria | $(A \cdot w)_j$ | $w_j$ | $(A \cdot w)_j / w_j$ |
| :---: | :---: | :---: | :---: |
| **$C_1$** | $0{,}8434$ | $0{,}1333$ | $6{,}3276$ |
| **$C_2$** | $0{,}3033$ | $0{,}0501$ | $6{,}0557$ |
| **$C_3$** | $3{,}1162$ | $0{,}4614$ | $6{,}7540$ |
| **$C_4$** | $1{,}5267$ | $0{,}2258$ | $6{,}7610$ |
| **$C_5$** | $0{,}1668$ | $0{,}0271$ | $6{,}1518$ |
| **$C_6$** | $0{,}6626$ | $0{,}1023$ | $6{,}4764$ |

- Nilai Eigen Maksimum ($\lambda_{\max}$):
  $$\lambda_{\max} = \frac{6{,}3276 + 6{,}0557 + 6{,}7540 + 6{,}7610 + 6{,}1518 + 6{,}4764}{6} = \mathbf{6{,}4211}$$
- Ordo Matriks ($n$): **$6$**
- *Consistency Index* ($CI$):
  $$CI = \frac{\lambda_{\max} - n}{n - 1} = \frac{6{,}4211 - 6}{6 - 1} = \frac{0{,}4211}{5} = \mathbf{0{,}0842}$$
- *Random Index* ($RI$) untuk $n = 6$: **$1{,}24$**
- *Consistency Ratio* ($CR$):
  $$CR = \frac{CI}{RI} = \frac{0{,}0842}{1{,}24} = \mathbf{0{,}0679} \quad (6{,}79\%)$$
- **Kesimpulan:** Karena $CR = 0{,}0679 \le 0{,}10$, matriks perbandingan berpasangan dinyatakan **konsisten dan valid secara matematis**.

---

## 4. Matriks Penilaian Alternatif Lokasi ($X$)

| Kode | Nama Alternatif | Deskripsi Ringkas Lokasi | $C_1$ (Biaya - Juta Rp) | $C_2$ (Keamanan) | $C_3$ (Daya Beli) | $C_4$ (Visibilitas) | $C_5$ (Struktur) | $C_6$ (Aglomerasi) |
| :---: | :--- | :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **$A_1$** | Sinduadi (Jl. Umbul Permai) | Luas tanah 218 m² / bangunan 210 m², lebar muka 12 m, listrik 7.000 W | $130$ | $3$ | $4$ | $5$ | $5$ | $2$ |
| **$A_2$** | Jl. Magelang | Ruko 2 lantai, tepi jalan arteri utama dekat Jogja City Mall | $120$ | $3$ | $3$ | $4$ | $5$ | $2$ |
| **$A_3$** | Babarsari | Ruko 2 lantai, luas tanah 102 m² / bangunan 165 m², kawasan kampus, lebar 4,2 m | $150$ | $3$ | $2$ | $3$ | $5$ | $1$ |
| **$A_4$** | Taman Siswa | Ruko hook 2 lantai, luas tanah 162 m² / bangunan 200 m², lebar 10 m, akses padat | $250$ | $3$ | $4$ | $5$ | $5$ | $3$ |
| **$A_5$** | Malioboro Mall | Ruang usaha dalam pusat perbelanjaan pariwisata & niaga, luas **78 m²**, listrik 5.500 W | $346{,}32$ | $5$ | $5$ | $4$ | $2$ | $4$ |

*Keterangan:* Skala penilaian kualitatif $C_2$ s.d. $C_6$ menggunakan interval $1$ hingga $5$ berdasarkan penilaian tim peneliti dari observasi lapangan dan data listing properti.

---

## 5. Komputasi Weighted Product (WP)

### A. Penyesuaian Pangkat Eksponen ($W_j^*$) & Perhitungan Vektor Preferensi $S$ ($S_i$)
Pangkat eksponen untuk kriteria biaya ($C_1$) bertanda negatif ($W_1^* = -0{,}1333$) dan untuk kriteria keuntungan ($C_2$–$C_6$) bertanda positif ($W_j^* = +w_j$):

$$S_i = (x_{i1})^{-0{,}1333} \times (x_{i2})^{+0{,}0501} \times (x_{i3})^{+0{,}4614} \times (x_{i4})^{+0{,}2258} \times (x_{i5})^{+0{,}0271} \times (x_{i6})^{+0{,}1023}$$

Rincian faktor pangkat per kriteria dan nilai $S_i$ (dihitung dengan presisi bobot penuh $w_j$):

| Alternatif | $x_{i1}^{-w_1}$ | $x_{i2}^{+w_2}$ | $x_{i3}^{+w_3}$ | $x_{i4}^{+w_4}$ | $x_{i5}^{+w_5}$ | $x_{i6}^{+w_6}$ | Vektor $S_i$ (Eksak) | Vektor $S_i$ (Bobot 4dp) |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **$A_1$ (Sinduadi)** | $0{,}5227$ | $1{,}0566$ | $1{,}8957$ | $1{,}4382$ | $1{,}0446$ | $1{,}0735$ | **$1{,}6885$** | $1{,}6884$ |
| **$A_2$ (Jl. Magelang)** | $0{,}5283$ | $1{,}0566$ | $1{,}6601$ | $1{,}3676$ | $1{,}0446$ | $1{,}0735$ | **$1{,}4210$** | $1{,}4209$ |
| **$A_3$ (Babarsari)** | $0{,}5128$ | $1{,}0566$ | $1{,}3769$ | $1{,}2816$ | $1{,}0446$ | $1{,}0000$ | **$0{,}9987$** | $0{,}9986$ |
| **$A_4$ (Taman Siswa)** | $0{,}4790$ | $1{,}0566$ | $1{,}8957$ | $1{,}4382$ | $1{,}0446$ | $1{,}1190$ | **$1{,}6131$** | $1{,}6130$ |
| **$A_5$ (Malioboro Mall)** | $0{,}4587$ | $1{,}0839$ | $2{,}1013$ | $1{,}3676$ | $1{,}0190$ | $1{,}1524$ | **$1{,}6777$** | $1{,}6777$ |

**Total Akumulasi Vektor $S$:**
$$\sum_{k=1}^5 S_k = 1{,}6885 + 1{,}4210 + 0{,}9987 + 1{,}6131 + 1{,}6777 = \mathbf{7{,}3989} \quad (\text{atau } 7{,}3986 \text{ dengan bobot 4dp})$$

### B. Perhitungan Vektor Preferensi Relatif $V$ ($V_i$) & Pemeringkatan Akhir
Formulasi normalisasi: $V_i = \frac{S_i}{\sum_{k=1}^5 S_k}$ *(kedua perhitungan—bobot eksak maupun bobot 4 desimal—menghasilkan nilai $V_i$ yang identik hingga 4 angka desimal)*:

| Peringkat | Kode | Alternatif Lokasi | Nilai Vektor $S_i$ | Nilai Vektor $V_i$ | Persentase Preferensi | Status Rekomendasi |
| :---: | :---: | :--- | :---: | :---: | :---: | :--- |
| **1** | **$A_1$** | **Sinduadi (Jl. Umbul Permai)** | **$1{,}6885$** | **$0{,}2282$** | **$22{,}82\%$** | **Prioritas Utama (Terpilih)** |
| **2** | **$A_5$** | Malioboro Mall | $1{,}6777$ | $0{,}2268$ | $22{,}68\%$ | Alternatif Kedua |
| **3** | **$A_4$** | Taman Siswa | $1{,}6131$ | $0{,}2180$ | $21{,}80\%$ | Alternatif Ketiga |
| **4** | **$A_2$** | Jl. Magelang | $1{,}4210$ | $0{,}1921$ | $19{,}21\%$ | Alternatif Keempat |
| **5** | **$A_3$** | Babarsari | $0{,}9987$ | $0{,}1350$ | $13{,}50\%$ | Alternatif Kelima |
| - | - | **Total Akumulasi** | **$7{,}3989$** | **$1{,}0000$** | **$100{,}00\%$** | - |

- Margin keunggulan peringkat 1 ($A_1$) terhadap peringkat 2 ($A_5$): $\Delta V = 0{,}2282 - 0{,}2268 = \mathbf{0{,}0014}$ (**0,14%**) dengan rasio preferensi invarian:
  $$\frac{S_1}{S_5} = \frac{1{,}6885}{1{,}6777} = \mathbf{1{,}0064} > 1$$

---

## 6. Data Nyata Subbab Evaluasi

### A. Simulasi Uji *Rank Reversal* (Aksioma IIA) dengan Metrik DCG, IDCG, dan NDCG

Untuk mengukur secara kuantitatif apakah urutan peringkat awal tetap terjaga ketika gugus alternatif berubah, evaluasi menggunakan metrik **Discounted Cumulative Gain (DCG)**, **Ideal Discounted Cumulative Gain (IDCG)**, dan **Normalized DCG (NDCG)**:

$$\text{DCG}_k = \sum_{r=1}^{k} \frac{2^{\text{rel}_r} - 1}{\log_2(r + 1)}, \qquad \text{IDCG}_k = \sum_{r=1}^{k} \frac{2^{\text{rel}_r^*} - 1}{\log_2(r + 1)}, \qquad \text{NDCG}_k = \frac{\text{DCG}_k}{\text{IDCG}_k}$$

Skor relevansi bertingkat (*graded relevance*) ditetapkan dari urutan ideal *baseline* model AHP-WP: $\text{rel}(A_1)=5$, $\text{rel}(A_5)=4$, $\text{rel}(A_4)=3$, $\text{rel}(A_2)=2$, dan $\text{rel}(A_3)=1$, sehingga:
- **$\text{IDCG}@5$ (5 alternatif asli):**
  $$\text{IDCG}@5 = \frac{31}{\log_2 2} + \frac{15}{\log_2 3} + \frac{7}{\log_2 4} + \frac{3}{\log_2 5} + \frac{1}{\log_2 6} = 31{,}0000 + 9{,}4639 + 3{,}5000 + 1{,}2920 + 0{,}3869 = \mathbf{45{,}6428}$$
- **$\text{IDCG}@4$ (4 alternatif saat $A_3$ dihapus):** $\mathbf{45{,}2560}$

#### Tabel 3. Hasil Simulasi Uji *Rank Reversal* (Penambahan & Penghapusan Alternatif) pada AHP-WP
| Skenario Uji | Alternatif Tambahan / Dihapus | Peringkat Penuh Hasil WP | Proyeksi Urutan Alternatif Asli | Rasio $S_1 / S_5$ | DCG | IDCG | NDCG | Status *Rank Reversal* |
| :--- | :--- | :--- | :--- | :---: | :---: | :---: | :---: | :---: |
| **Baseline** | 5 alternatif awal ($A_1$–$A_5$) | $A_1 > A_5 > A_4 > A_2 > A_3$ | $A_1 > A_5 > A_4 > A_2 > A_3$ | $1{,}0064$ | $45{,}6428$ | $45{,}6428$ | **$1{,}0000$** | Acuan |
| **Uji 1 (Tambah Menengah)** | $+A_6$ Gejayan `[180, 4, 4, 4, 5, 3]` | $A_1(0{,}1871) > A_5(0{,}1859) > A_6(0{,}1801) > A_4(0{,}1787) > A_2(0{,}1575) > A_3(0{,}1107)$ | $A_1 > A_5 > A_4 > A_2 > A_3$ | **$1{,}0064$** | $45{,}6428$ | $45{,}6428$ | **$1{,}0000$** | Tidak terjadi |
| **Uji 2 (Tambah Super-Dominan)** | $+A_6^*$ Ekstrem Murah `[90, 5, 5, 5, 5, 5]` | $A_6^*(0{,}2304) > A_1(0{,}1756) > A_5(0{,}1745) > A_4(0{,}1678) > A_2(0{,}1478) > A_3(0{,}1039)$ | $A_1 > A_5 > A_4 > A_2 > A_3$ | **$1{,}0064$** | $45{,}6428$ | $45{,}6428$ | **$1{,}0000$** | Tidak terjadi |
| **Uji 3 (Tambah Inferior)** | $+A_6^-$ Inferior `[500, 1, 1, 1, 1, 1]` | $A_1(0{,}2155) > A_5(0{,}2141) > A_4(0{,}2059) > A_2(0{,}1814) > A_3(0{,}1275) > A_6^-(0{,}0557)$ | $A_1 > A_5 > A_4 > A_2 > A_3$ | **$1{,}0064$** | $45{,}6428$ | $45{,}6428$ | **$1{,}0000$** | Tidak terjadi |
| **Uji 4 (Hapus Terbawah)** | $-A_3$ Babarsari | $A_1(0{,}2638) > A_5(0{,}2621) > A_4(0{,}2520) > A_2(0{,}2220)$ | $A_1 > A_5 > A_4 > A_2$ | **$1{,}0064$** | $45{,}2560$ | $45{,}2560$ | **$1{,}0000$** | Tidak terjadi |
| *Pembanding (Aditif SAW)* | *Normalisasi min-max aditif pada data sama* | *$A_5(0{,}8515) > A_1(0{,}8263) > A_4(0{,}7928) > A_2(0{,}6991) > A_3(0{,}5094)$* | *$A_5 > A_1 > A_4 > A_2 > A_3$* | *-* | *$39{,}7377$* | *$45{,}6428$* | ***$0{,}8706$*** | *Beda posisi #1 ↔ #2* |

*Interpretasi:* Pada seluruh skenario penambahan alternatif baru maupun penghapusan alternatif lama, model hibrida AHP-WP mempertahankan $\text{DCG} = \text{IDCG}$ (**$\text{NDCG} = 1{,}0000$**) serta rasio $S_1 / S_5 = 1{,}0064$ yang sepenuhnya invarian, membuktikan pemenuhan aksioma *Independence of Irrelevant Alternatives* (IIA). Sebaliknya, apabila terjadi pembalikan posisi teratas $A_1 \leftrightarrow A_5$, nilai $\text{DCG}$ langsung turun ke $39{,}7377$ ($\text{NDCG} = 0{,}8706$, turun $12{,}94\%$).

---

### B. Analisis Sensitivitas Bobot Kriteria & Titik Kritis (*Tipping Point*)

Pengujian dilakukan dengan memvariasikan bobot kriteria utama ($C_1$ Biaya dan $C_3$ Daya Beli) sambil menskalakan ulang bobot kriteria lain secara proporsional agar $\sum w_j = 1{,}0000$:

#### Tabel 4. Hasil Analisis Sensitivitas Bobot pada Model AHP-WP
| Skenario Sensitivitas | $w_1$ (Biaya) | $w_3$ (Daya Beli) | $V_1$ ($A_1$) | $V_5$ ($A_5$) | $V_4$ ($A_4$) | $V_2$ ($A_2$) | $V_3$ ($A_3$) | Urutan Peringkat | DCG | NDCG |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :--- | :---: | :---: |
| **Baseline (AHP)** | $0{,}1333$ | $0{,}4614$ | **$0{,}2282$** | $0{,}2268$ | $0{,}2180$ | $0{,}1921$ | $0{,}1350$ | $A_1 > A_5 > A_4 > A_2 > A_3$ | $45{,}6428$ | **$1{,}0000$** |
| **S1: $C_1$ naik $+10\%$ relatif** | $0{,}1466$ | $0{,}4543$ | **$0{,}2291$** | $0{,}2242$ | $0{,}2168$ | $0{,}1936$ | $0{,}1363$ | $A_1 > A_5 > A_4 > A_2 > A_3$ | $45{,}6428$ | **$1{,}0000$** |
| **S2: $C_1$ naik $+20\%$ relatif** | $0{,}1600$ | $0{,}4472$ | **$0{,}2300$** | $0{,}2218$ | $0{,}2156$ | $0{,}1950$ | $0{,}1376$ | $A_1 > A_5 > A_4 > A_2 > A_3$ | $45{,}6428$ | **$1{,}0000$** |
| **S3: $C_1$ turun $-20\%$ relatif** | $0{,}1066$ | $0{,}4756$ | $0{,}2264$ | **$0{,}2318$** | $0{,}2204$ | $0{,}1891$ | $0{,}1323$ | $A_5 > A_1 > A_4 > A_2 > A_3$ | $39{,}7377$ | $0{,}8706$ |
| **S4: $C_3$ naik ke $50\%$** | $0{,}1237$ | $0{,}5000$ | $0{,}2279$ | **$0{,}2302$** | $0{,}2184$ | $0{,}1902$ | $0{,}1332$ | $A_5 > A_1 > A_4 > A_2 > A_3$ | $39{,}7377$ | $0{,}8706$ |
| **S5: $C_3$ naik ke $55\%$** | $0{,}1114$ | $0{,}5500$ | $0{,}2275$ | **$0{,}2348$** | $0{,}2190$ | $0{,}1879$ | $0{,}1309$ | $A_5 > A_1 > A_4 > A_2 > A_3$ | $39{,}7377$ | $0{,}8706$ |
| **S6: $C_3$ naik ke $60\%$** | $0{,}0990$ | $0{,}6000$ | $0{,}2271$ | **$0{,}2393$** | $0{,}2195$ | $0{,}1855$ | $0{,}1286$ | $A_5 > A_1 > A_4 > A_2 > A_3$ | $39{,}7377$ | $0{,}8706$ |
| **S7: Bobot Seragam ($1/6$)** | $0{,}1667$ | $0{,}1667$ | **$0{,}2226$** | $0{,}1983$ | $0{,}2135$ | $0{,}2072$ | $0{,}1584$ | $A_1 > A_4 > A_2 > A_5 > A_3$ | $43{,}7635$ | $0{,}9588$ |

**Temuan Titik Kritis (*Tipping Point*) Sensitivitas:**
- Karena margin awal antara Sinduadi ($A_1$) dan Malioboro Mall ($A_5$) sangat ketat ($\Delta V = 0{,}14\%$), keputusan peringkat 1 sensitif terhadap pergeseran preferensi antara efisiensi sewa ($C_1$) dan daya beli ($C_3$):
  - Kenaikan bobot biaya sewa ($C_1$) sebesar $+10\%$ hingga $+20\%$ makin memperkokoh keunggulan $A_1$ ($\text{NDCG} = 1{,}0000$).
  - Sebaliknya, $A_5$ (Malioboro Mall) mulai menggeser $A_1$ tepat saat **$w_3 > 0{,}4764$ ($47{,}64\%$)** atau saat **$w_1 < 0{,}1276$ ($12{,}76\%$)**.
- Sementara itu, posisi peringkat 3 ($A_4$), 4 ($A_2$), dan 5 ($A_3$) tetap stabil di seluruh skenario S1–S6; kawasan Babarsari ($A_3$) konsisten menempati peringkat terakhir pada seluruh skenario termasuk bobot seragam (S7).
