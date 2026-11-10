---
title: Bab Landasan Teori - Sub-bab Persamaan Matematika (Integrasi AHP-WP)
created: 2026-11-05
updated: 2026-11-10
status: Ready for Manuscript
target_journal: Template UIN SUSKA (Jurnal Ilmiah Rekayasa dan Manajemen Sistem Informasi)
format: LaTeX / Markdown
tags:
  - landasan-teori
  - persamaan-matematika
  - ahp
  - weighted-product
  - rank-reversal
  - lokasi-ritel-emas
---

# LANDASAN TEORI

## 1. Persamaan Matematika

Pemodelan keputusan dalam penelitian ini dirancang melalui pendekatan hibrida sekuensial yang membagi proses komputasi ke dalam dua fase komplementer: penentuan bobot prioritas kriteria global menggunakan *Analytic Hierarchy Process* (AHP) dan perankingan alternatif kandidat lokasi menggunakan *Weighted Product* (WP). Integrasi ini secara spesifik mengatasi permasalahan dalam domain *Multi-Criteria Decision Making* (MCDM) spasial, khususnya pada pemilihan lokasi strategis bisnis ritel perhiasan emas.

### 1.1. Multi-Criteria Decision Making (MCDM) & Matriks Keputusan
MCDM merupakan cabang riset operasi (*operations research*) yang menyelesaikan masalah pemilihan alternatif diskrit $A = \{A_1, A_2, \dots, A_m\}$ berdasarkan sekumpulan kriteria evaluasi $C = \{C_1, C_2, \dots, C_n\}$ yang saling bertentangan (*conflicting criteria*) dan memiliki satuan ukur yang tidak sepadan (*incommensurable*). Struktur data dasar direpresentasikan melalui matriks keputusan $X$:

$$
X = [x_{ij}]_{m \times n} = 
\begin{pmatrix}
x_{11} & x_{12} & \dots & x_{1n} \\
x_{21} & x_{22} & \dots & x_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
x_{m1} & x_{m2} & \dots & x_{mn}
\end{pmatrix}
$$

di mana $x_{ij}$ menyatakan nilai kinerja alternatif ke-$i$ pada kriteria ke-$j$. Sistem komputasi bertujuan menemukan solusi kompromi terbaik (*compromise solution*) yang memenuhi prinsip non-dominasi Pareto.

### 1.2. Teori Ekonomi Tata Ruang & Karakteristik Ritel Toko Emas
Penentuan lokasi gerai ritel perhiasan berakar pada teori ekonomi tata ruang (*spatial retail economics*). Berdasarkan *Central Place Theory* Christaller [7], komoditas emas tergolong barang berorde tinggi (*high-order goods*) dengan nilai transaksi per unit yang besar dan frekuensi transaksi terencana, sehingga menuntut ambang batas populasi (*population threshold*) dan jangkauan spasial (*spatial range*) yang luas. Di samping itu, teori aglomerasi ekonomi Marshall [8] dan model diferensiasi spasial Hotelling [9] membuktikan bahwa pemusatan gerai emas pada klaster niaga sejenis secara empiris menurunkan biaya pencarian konsumen (*consumer search cost*) dan meningkatkan volume kunjungan terarah (*targeted footfall*).

Secara operasional, toko emas memiliki karakteristik unik:
1. **Rasio Nilai terhadap Volume yang Ekstrem (*High Value-to-Volume Density*)**: Konsentrasi nilai kapital inventori yang sangat tinggi menimbulkan kerentanan terhadap kejahatan kekerasan, sehingga menuntut jaminan atribut keamanan eksternal yang ketat serta visibilitas lokasi guna mendukung pengawasan visual alami (*natural surveillance*).
2. **Kebutuhan Adaptasi Struktur Bangunan**: Operasional fisik memerlukan instalasi brankas baja tahan api dengan bobot tonase berat dan partisi pengaman khusus, yang mewajibkan keleluasaan izin modifikasi struktur properti.

Oleh karena itu, penentuan lokasi toko emas mengharuskan keseimbangan komputasi antara atribut biaya (*cost*), yakni beban harga sewa properti tahunan, dengan atribut keuntungan (*benefit*) yang meliputi keamanan kawasan, potensi daya beli lingkungan, visibilitas ruang, fleksibilitas perombakan struktur bangunan, dan aglomerasi sentra niaga.

---

### 1.3. Fase 1: Penentuan Bobot Kriteria Global & Uji Konsistensi (AHP)

Metode AHP digunakan secara **eksklusif hanya untuk sintesis pembobotan kriteria**, tanpa menyertakan penilaian alternatif, guna mereduksi bias kognitif pengambil keputusan melalui struktur hierarki dan perbandingan berpasangan [2].

#### A. Matriks Perbandingan Berpasangan
Pengambil keputusan atau pakar menyusun matriks perbandingan berpasangan $A = [a_{ik}]_{n \times n}$ berukuran $n \times n$, di mana $a_{ik}$ menyatakan derajat kepentingan relatif kriteria ke-$i$ terhadap kriteria ke-$k$ menurut skala fundamental Saaty (1–9). Matriks wajib memenuhi **Aksioma Resiprokal (*Reciprocal Axiom*)** [2]:

$$
a_{ki} = \frac{1}{a_{ik}} \quad \text{dan} \quad a_{ii} = 1 \quad \forall i, k \in \{1, 2, \dots, n\}
$$

> [!NOTE]
> Jika evaluasi melibatkan dewan pakar multiresponden, nilai elemen matriks agregat disintesis menggunakan rata-rata geometrik (*Geometric Mean*) sebelum proses normalisasi untuk mempertahankan sifat resiprokal matriks:
> $$ a_{ik} = \left( \prod_{p=1}^P a_{ik}^{(p)} \right)^{\frac{1}{P}} $$
> di mana $P$ adalah jumlah pakar dan $a_{ik}^{(p)}$ adalah penilaian pakar ke-$p$.

#### B. Persamaan 1: Normalisasi Matriks & Sintesis Bobot Prioritas (Eigen Vector)
Bobot prioritas kriteria ke-$j$ ($w_j$) diperoleh melalui rata-rata baris dari elemen matriks yang dinormalisasi terhadap jumlah kolomnya:

$$
w_j = \frac{1}{n} \sum_{k=1}^n \frac{a_{jk}}{\sum_{i=1}^n a_{ik}} \quad \forall j \in \{1, 2, \dots, n\}
\tag{1}
$$

*Keterangan:*
* $w_j$ : Bobot prioritas relatif kriteria ke-$j$, dengan batasan normalisasi $\sum_{j=1}^n w_j = 1$.
* $n$ : Jumlah total kriteria yang dievaluasi.
* $a_{jk}$ : Nilai perbandingan berpasangan antara kriteria baris ke-$j$ terhadap kriteria kolom ke-$k$.
* $\sum_{i=1}^n a_{ik}$ : Jumlah total elemen pada kolom ke-$k$ dalam matriks perbandingan berpasangan.

#### C. Persamaan 2: Evaluasi Rasio Konsistensi Logis Saaty (CI dan CR)
Guna memastikan penilaian pakar bebas dari kontradiksi logis dan fluktuasi acak, dihitung nilai *Consistency Index* ($CI$) dan *Consistency Ratio* ($CR$) [2]:

$$
CI = \frac{\lambda_{\max} - n}{n - 1}
\tag{2a}
$$

$$
CR = \frac{CI}{RI}
\tag{2b}
$$

*Keterangan:*
* $\lambda_{\max}$ : Nilai eigen terbesar (*principal eigenvalue*) yang dihitung dari rata-rata elemen vektor konsistensi:
  $$ \lambda_{\max} = \frac{1}{n} \sum_{i=1}^n \frac{(A \cdot w)_i}{w_i} $$
* $n$ : Ordo matriks perbandingan berpasangan.
* $CI$ : Indeks deviasi konsistensi logis penilai.
* $RI$ : *Random Index*, yaitu indeks konsistensi acak rata-rata dari simulasi matriks acak Saaty:

| $n$ | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **$RI$** | 0,00 | 0,00 | 0,58 | 0,90 | 1,12 | 1,24 | 1,32 | 1,41 | 1,45 | 1,49 |

* $CR$ : Rasio konsistensi matriks perbandingan. Matriks dinyatakan **valid dan konsisten** jika memenuhi kondisi batas ambang:
  $$ CR \le 0{,}10 \quad (10\%) $$

**Argumen Teoretis Pembatasan $CR \le 0{,}10$:**
1. **Validasi Rasionalitas**: Ambang batas 10% menjamin penilaian terstruktur dan terbebas dari kesalahan acak (*random errors*) manusiawi.
2. **Kekebalan Transitivitas**: Menjaga relasi transitif preferensi (jika $A > B$ dan $B > C$, maka $A > C$).
3. **Integritas Input Algoritma**: Bobot kriteria $w_j$ yang lolos batas ini terjamin valid untuk dialirkan sebagai eksponen pangkat pada metode Weighted Product. Jika $CR > 0{,}10$, perbandingan berpasangan wajib diulang.

---

### 1.4. Fase 2: Pemeringkatan Alternatif & Ketahanan Rank Reversal (Weighted Product)

#### A. Celah Struktural AHP Murni: Anomali *Rank Reversal*
Penerapan AHP murni hingga tahap pemeringkatan alternatif memiliki cacat struktural berupa kerentanan terhadap anomali *rank reversal*, yaitu kondisi di mana susunan peringkat preferensi antaralternatif yang ada ($A_1 > A_2$) berbalik ($A_2 > A_1$) semata-mata akibat penambahan atau penghapusan alternatif baru yang tidak relevan [3], [4]. Kelemahan ini berakar dari skema normalisasi penjumlahan aditif berbasis jumlah kolom matriks lokal:

$$
\bar{a}_{ik} = \frac{a_{ik}}{\sum_{i=1}^m a_{ik}}
$$

Penyebut $\sum_{i=1}^m a_{ik}$ berubah setiap kali alternatif baru masuk, sehingga mendistorsi rasio preferensi lokal dan melanggar aksioma *Independence of Irrelevant Alternatives* (IIA) Kenneth Arrow [10]. Dalam investasi gerai toko emas berkapital tinggi, distorsi ini mendisrupsi kepastian alokasi modal operasional.

#### B. Persamaan 3: Normalisasi Pangkat Bobot & Perhitungan Vektor Preferensi ($S_i$)
Metode Weighted Product (WP) dipilih menggantikan sintesis alternatif AHP karena menerapkan agregasi multiplikatif non-linear [5]. Sebelum dioperasikan, bobot $w_j$ dari AHP dinormalisasi kembali agar total eksponen setara dengan 1:

$$
W_j = \frac{w_j}{\sum_{k=1}^n w_k} \quad \text{sehingga} \quad \sum_{j=1}^n W_j = 1
\tag{3a}
$$

Mengingat vektor bobot hasil komputasi AHP pada Persamaan (1) telah memenuhi kaidah normalisasi $\sum_{k=1}^n w_k = 1{,}0000$, maka nilai pangkat bobot $W_j$ secara numerik identik dengan bobot prioritas kriteria AHP ($W_j = w_j$).

Nilai preferensi absolut setiap alternatif kandidat lokasi dihitung melalui formulasi **Vektor $S_i$**:

$$
S_i = \prod_{j=1}^n \left( x_{ij} \right)^{W_j^*} \quad \forall i \in \{1, 2, \dots, m\}
\tag{3b}
$$

di mana pemangkatan $W_j^*$ ditetapkan secara tegas berdasarkan karakter atribut:

$$
W_j^* = 
\begin{cases} 
+W_j, & \text{jika kriteria } j \text{ bersifat keuntungan (benefit)} \\
-W_j, & \text{jika kriteria } j \text{ bersifat biaya/ongkos (cost)}
\end{cases}
$$

*Keterangan:*
* $m$ : Jumlah total alternatif kandidat lokasi toko emas.
* $n$ : Jumlah total kriteria evaluasi.
* $x_{ij}$ : Nilai kinerja alternatif lokasi ke-$i$ pada kriteria ke-$j$.
* $W_j$ : Pangkat bobot ternormalisasi kriteria ke-$j$.
* $S_i$ : Skor preferensi multiplikatif alternatif lokasi ke-$i$.
* Pada kriteria biaya (*cost*), pemangkatan negatif secara matematis ekuivalen dengan pembagian ($x_{ij}^{-W_j} = \frac{1}{x_{ij}^{W_j}}$), sehingga memperkecil nilai $S_i$ secara proporsional seiring membesarnya biaya sewa properti.

#### C. Pembuktian Aljabar Ketahanan Terhadap Rank Reversal (Invariansi Rasio)
Kekebalan metode WP terhadap anomali pembalikan peringkat dibuktikan melalui rasio perbandingan preferensi antara dua alternatif sebarang, $A_a$ dan $A_b$ [5], [6]:

$$
\frac{S_a}{S_b} = \frac{\prod_{j=1}^n \left( x_{aj} \right)^{W_j^*}}{\prod_{j=1}^n \left( x_{bj} \right)^{W_j^*}} = \prod_{j=1}^n \left( \frac{x_{aj}}{x_{bj}} \right)^{W_j^*}
$$

Formulasi di atas membuktikan bahwa rasio $\frac{S_a}{S_b}$ **bersifat invarian murni**. Rasio preferensi hanya ditentukan secara eksklusif oleh kinerja intrinsik alternatif $a$ dan $b$ serta bobot kriteria terkait, tanpa memuat elemen dari alternatif ketiga ($A_c$) atau alternatif baru yang ditambahkan ($x_{kj}, k \notin \{a, b\}$). Oleh karena itu, jika $S_a > S_b$, hubungan tersebut tidak akan pernah berbalik, berapapun alternatif baru yang disertakan ke dalam model komputasi, menjamin terpenuhinya aksioma IIA.

#### D. Persamaan 4: Perhitungan Nilai Preferensi Relatif (Vektor $V_i$) & Pemeringkatan Akhir
Rekomendasi lokasi optimal dihasilkan melalui normalisasi rasio komprehensif **Vektor $V_i$**:

$$
V_i = \frac{S_i}{\sum_{k=1}^m S_k} = \frac{\prod_{j=1}^n \left( x_{ij} \right)^{W_j^*}}{\sum_{k=1}^m \prod_{j=1}^n \left( x_{kj} \right)^{W_j^*}} \quad \forall i \in \{1, 2, \dots, m\}
\tag{4}
$$

*Keterangan:*
* $V_i$ : Nilai preferensi relatif akhir alternatif lokasi ke-$i$, dengan batasan probabilistik $\sum_{i=1}^m V_i = 1$.
* Karena pembagian dilakukan dengan skalar positif yang seragam ($\sum S_k$), urutan peringkat preferensi akhir bersifat monotonik ketat:
  $$ V_a > V_b \iff S_a > S_b $$
* Nilai $V_i$ tertinggi ($V_{\max} = \max \{V_1, V_2, \dots, V_m\}$) menetapkan kandidat lokasi toko emas yang paling direkomendasikan secara objektif.
