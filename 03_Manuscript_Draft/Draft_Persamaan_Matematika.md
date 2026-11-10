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

Penelitian ini menerapkan pendekatan hibrida sekuensial yang membagi komputasi ke dalam dua fase: penentuan bobot prioritas kriteria menggunakan *Analytic Hierarchy Process* (AHP) dan pemeringkatan kandidat lokasi menggunakan *Weighted Product* (WP). Pembagian peran ini bukan kombinasi arbitrer; masing-masing metode dipilih karena keunggulan spesifiknya pada tahap yang bersangkutan dan untuk menutup kelemahan struktural yang muncul jika salah satu metode digunakan secara tunggal hingga tahap akhir.

### 1.1. Multi-Criteria Decision Making (MCDM) dan Matriks Keputusan

MCDM adalah cabang riset operasi yang menyelesaikan masalah pemilihan di antara alternatif diskrit $A = \{A_1, A_2, \dots, A_m\}$ berdasarkan kriteria evaluasi $C = \{C_1, C_2, \dots, C_n\}$ yang saling bertentangan dan tidak sepadan satuannya (*incommensurable*). Data masukan direpresentasikan sebagai matriks keputusan $X$:

$$
X = [x_{ij}]_{m \times n} =
\begin{pmatrix}
x_{11} & x_{12} & \dots & x_{1n} \\
x_{21} & x_{22} & \dots & x_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
x_{m1} & x_{m2} & \dots & x_{mn}
\end{pmatrix}
$$

di mana $x_{ij}$ adalah nilai kinerja alternatif ke-$i$ pada kriteria ke-$j$. Dalam konteks penelitian ini, $m = 5$ kandidat lokasi dan $n = 6$ kriteria evaluasi membentuk matriks keputusan berukuran $5 \times 6$.

### 1.2. Teori Ekonomi Tata Ruang dan Karakteristik Ritel Toko Emas

Pemilihan lokasi gerai ritel perhiasan berakar pada teori ekonomi tata ruang (*spatial retail economics*). Berdasarkan *Central Place Theory* Christaller [7], emas tergolong barang berorde tinggi (*high-order goods*): nilai transaksi per unit besar, frekuensi pembelian terencana, dan konsumen bersedia menempuh jarak jauh untuk mendapatkannya. Karena itu, gerai emas membutuhkan lokasi dengan ambang batas populasi (*population threshold*) dan jangkauan spasial (*spatial range*) yang memadai. Teori aglomerasi Marshall [8] dan model diferensiasi spasial Hotelling [9] menambahkan bahwa pemusatan gerai sejenis pada satu klaster niaga menurunkan biaya pencarian konsumen dan meningkatkan volume kunjungan terarah.

Dua karakteristik operasional toko emas memperkuat urgensi pemilihan lokasi yang cermat. Pertama, konsentrasi inventori bernilai tinggi dalam satu titik fisik menciptakan kerentanan terhadap kejahatan, sehingga keamanan eksternal kawasan ($C_2$) dan visibilitas lokasi untuk pengawasan visual alami ($C_4$) menjadi atribut yang tidak dapat diabaikan. Kedua, instalasi brankas baja bertonase berat dan partisi pengaman memerlukan izin modifikasi struktur properti, yang tercermin pada kriteria fleksibilitas perombakan struktur bangunan ($C_5$). Kedua karakteristik ini, bersama biaya sewa properti ($C_1$), potensi daya beli lingkungan ($C_3$), dan aglomerasi sentra niaga ($C_6$), membentuk enam kriteria evaluasi yang digunakan dalam model ini.

---

### 1.3. Penentuan Bobot Kriteria Global dan Pengujian Konsistensi AHP

AHP digunakan **hanya untuk sintesis bobot prioritas kriteria**, tanpa melibatkan penilaian alternatif. Pembatasan ini disengaja untuk mencegah anomali yang dibahas pada Sub-bab 1.4 [2].

#### A. Matriks Perbandingan Berpasangan

Pengambil keputusan menyusun matriks perbandingan berpasangan $A = [a_{ik}]_{n \times n}$, di mana $a_{ik}$ menyatakan derajat kepentingan relatif kriteria ke-$i$ terhadap kriteria ke-$k$ pada skala fundamental Saaty (1–9). Matriks harus memenuhi **Aksioma Resiprokal** [2]:

$$
a_{ki} = \frac{1}{a_{ik}} \quad \text{dan} \quad a_{ii} = 1 \quad \forall i, k \in \{1, 2, \dots, n\}
$$

> [!NOTE]
> Jika evaluasi melibatkan lebih dari satu responden, nilai elemen matriks agregat disintesis menggunakan rata-rata geometrik sebelum normalisasi untuk mempertahankan sifat resiprokal:
> $$ a_{ik} = \left( \prod_{p=1}^P a_{ik}^{(p)} \right)^{\frac{1}{P}} $$
> di mana $P$ adalah jumlah responden dan $a_{ik}^{(p)}$ adalah penilaian responden ke-$p$.

#### B. Persamaan 1 untuk Sintesis Bobot Prioritas Eigen Vector

Bobot prioritas $w_j$ dihitung dengan menormalisasi setiap kolom matriks terhadap total kolomnya, lalu merata-ratakan setiap baris. Secara intuitif, kriteria yang secara konsisten mendapat nilai tinggi di seluruh kolom akan menghasilkan bobot yang besar:

$$
w_j = \frac{1}{n} \sum_{k=1}^n \frac{a_{jk}}{\sum_{i=1}^n a_{ik}} \quad \forall j \in \{1, 2, \dots, n\}
\tag{1}
$$

*Keterangan:*
* $w_j$ : Bobot prioritas kriteria ke-$j$, dengan batasan $\sum_{j=1}^n w_j = 1$.
* $n$ : Jumlah kriteria yang dievaluasi.
* $a_{jk}$ : Nilai perbandingan berpasangan kriteria ke-$j$ terhadap kriteria ke-$k$.
* $\sum_{i=1}^n a_{ik}$ : Total kolom ke-$k$ dalam matriks perbandingan berpasangan.

#### C. Persamaan 2 untuk Evaluasi Rasio Konsistensi CI dan CR

Penilaian perbandingan berpasangan oleh manusia tidak selalu transitif sempurna. Untuk mengukur deviasi dari konsistensi logis, dihitung *Consistency Index* ($CI$) dan *Consistency Ratio* ($CR$) [2]:

$$
CI = \frac{\lambda_{\max} - n}{n - 1}
\tag{2a}
$$

$$
CR = \frac{CI}{RI}
\tag{2b}
$$

*Keterangan:*
* $\lambda_{\max}$ : Nilai eigen terbesar, dihitung dari rata-rata elemen vektor konsistensi:
  $$ \lambda_{\max} = \frac{1}{n} \sum_{i=1}^n \frac{(A \cdot w)_i}{w_i} $$
* $n$ : Ordo matriks.
* $RI$ : *Random Index*, yaitu rata-rata $CI$ dari ribuan matriks acak berukuran $n \times n$ (Saaty):

| $n$ | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **$RI$** | 0,00 | 0,00 | 0,58 | 0,90 | 1,12 | 1,24 | 1,32 | 1,41 | 1,45 | 1,49 |

* $CR$ : Matriks dinyatakan **konsisten** jika $CR \le 0{,}10$.

Ambang batas $CR \le 0{,}10$ memiliki tiga implikasi konkret:
1. **Validasi rasionalitas**: Deviasi penilaian masih dalam batas kesalahan manusiawi yang dapat diterima.
2. **Kekebalan transitivitas**: Relasi $A > B$ dan $B > C$ secara praktis menjamin $A > C$.
3. **Integritas bobot sebagai eksponen WP**: Bobot $w_j$ yang tidak lolos batas ini tidak dapat dipercaya sebagai eksponen pada Fase 2 dan penilaian harus diulang.

---

### 1.4. Pemeringkatan Alternatif Weighted Product dan Ketahanan terhadap Rank Reversal

#### A. Cacat Struktural AHP Murni Akibat Anomali Rank Reversal

AHP murni yang diperluas hingga pemeringkatan alternatif mengandung cacat struktural berupa anomali *rank reversal*, yaitu kondisi di mana urutan preferensi yang ditetapkan ($A_1 > A_2$) berbalik ($A_2 > A_1$) semata-mata karena penambahan atau penghapusan alternatif yang tidak relevan [3], [4]. Mekanismenya berakar dari skema normalisasi kolom lokal:

$$
\bar{a}_{ik} = \frac{a_{ik}}{\sum_{i=1}^m a_{ik}}
$$

Penyebut $\sum_{i=1}^m a_{ik}$ berubah setiap kali komposisi alternatif berubah, sehingga skor setiap alternatif bergantung pada alternatif lain dalam gugus. Dependensi ini secara langsung melanggar aksioma *Independence of Irrelevant Alternatives* (IIA) Kenneth Arrow [10].

#### B. Persamaan 3 untuk Perhitungan Vektor Preferensi S_i

WP menggantikan AHP pada fase pemeringkatan karena menggunakan agregasi multiplikatif, bukan aditif [5]. Dalam agregasi multiplikatif, perubahan pada alternatif $A_c$ tidak mengubah hasil operasi perkalian antara $A_a$ dan $A_b$; sifat ini yang membuat WP kebal terhadap *rank reversal*. Sebelum digunakan, bobot $w_j$ dinormalisasi ulang:

$$
W_j = \frac{w_j}{\sum_{k=1}^n w_k} \quad \text{sehingga} \quad \sum_{j=1}^n W_j = 1
\tag{3a}
$$

Karena AHP pada Persamaan (1) menghasilkan bobot yang sudah ternormalisasi ($\sum w_k = 1{,}0000$), maka $W_j = w_j$ secara numerik. Nilai preferensi absolut setiap alternatif dihitung melalui **Vektor $S_i$**:

$$
S_i = \prod_{j=1}^n \left( x_{ij} \right)^{W_j^*} \quad \forall i \in \{1, 2, \dots, m\}
\tag{3b}
$$

di mana tanda eksponen $W_j^*$ ditentukan oleh karakter atribut:

$$
W_j^* =
\begin{cases}
+W_j, & \text{jika kriteria } j \text{ bersifat keuntungan (benefit)} \\
-W_j, & \text{jika kriteria } j \text{ bersifat biaya (cost)}
\end{cases}
$$

*Keterangan:*
* $m$ : Jumlah alternatif ($m = 5$ dalam penelitian ini).
* $n$ : Jumlah kriteria ($n = 6$ dalam penelitian ini).
* $x_{ij}$ : Nilai kinerja alternatif ke-$i$ pada kriteria ke-$j$.
* $W_j$ : Bobot ternormalisasi kriteria ke-$j$.
* $S_i$ : Skor preferensi absolut alternatif ke-$i$.
* Eksponen negatif pada kriteria biaya secara matematis ekuivalen dengan $x_{ij}^{-W_j} = \frac{1}{x_{ij}^{W_j}}$, sehingga biaya sewa yang lebih tinggi menghasilkan $S_i$ yang lebih kecil.

#### C. Bukti Aljabar Invariansi Rasio terhadap Perubahan Gugus Alternatif

Ketahanan WP terhadap *rank reversal* dapat dibuktikan secara aljabar [5], [6]. Rasio preferensi dua alternatif $A_a$ dan $A_b$ adalah:

$$
\frac{S_a}{S_b} = \frac{\prod_{j=1}^n \left( x_{aj} \right)^{W_j^*}}{\prod_{j=1}^n \left( x_{bj} \right)^{W_j^*}} = \prod_{j=1}^n \left( \frac{x_{aj}}{x_{bj}} \right)^{W_j^*}
$$

Rasio $S_a / S_b$ hanya bergantung pada nilai intrinsik $A_a$ dan $A_b$ serta bobot kriteria $W_j^*$. Tidak ada suku yang mengandung nilai alternatif ketiga $A_c$. Oleh karena itu, jika $S_a > S_b$, hubungan ini tetap berlaku terlepas dari penambahan atau penghapusan alternatif lain, sehingga aksioma IIA terpenuhi.

#### D. Persamaan 4 untuk Penentuan Preferensi Relatif Vektor V_i dan Pemeringkatan Akhir

Rekomendasi lokasi ditetapkan berdasarkan **Vektor $V_i$**, yang merupakan normalisasi $S_i$ terhadap total seluruh alternatif:

$$
V_i = \frac{S_i}{\sum_{k=1}^m S_k} = \frac{\prod_{j=1}^n \left( x_{ij} \right)^{W_j^*}}{\sum_{k=1}^m \prod_{j=1}^n \left( x_{kj} \right)^{W_j^*}} \quad \forall i \in \{1, 2, \dots, m\}
\tag{4}
$$

*Keterangan:*
* $V_i$ : Preferensi relatif alternatif ke-$i$, dengan $\sum_{i=1}^m V_i = 1$.
* Karena pembagi $\sum S_k$ adalah skalar positif yang seragam, urutan $V_i$ bersifat monotonik ketat terhadap $S_i$:
  $$ V_a > V_b \iff S_a > S_b $$
* Alternatif dengan $V_i$ tertinggi adalah lokasi yang paling direkomendasikan.
