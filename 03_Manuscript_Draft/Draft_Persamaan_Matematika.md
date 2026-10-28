---
title: Draf Persamaan Matematika (AHP-WP)
created: 2026-10-28
status: Ready for Manuscript
format: LaTeX / MathJax
tags:
  - draft
  - metodologi
  - persamaan-matematika
  - ahp-wp
---

# Draf Persamaan Matematika: Kerangka Algoritmik Terintegrasi AHP-WP

Pendekatan hibrida dalam penelitian ini membagi proses komputasi keputusan ke dalam dua fase sekuensial yang saling melengkapi: penentuan bobot kriteria global menggunakan *Analytic Hierarchy Process* (AHP) dan perankingan alternatif menggunakan *Weighted Product* (WP). Alur matematis disajikan melalui formulasi formal berikut:

---

## 1. Fase Penentuan Bobot Kriteria (AHP)

### Persamaan 1: Normalisasi Matriks Perbandingan Berpasangan & Sintesis Bobot Kriteria
Pengambil keputusan atau pakar menyusun matriks perbandingan berpasangan $A = [a_{ik}]_{n \times n}$ berukuran $n \times n$, di mana $a_{ik}$ menyatakan derajat kepentingan relatif kriteria ke-$i$ terhadap kriteria ke-$k$ menurut skala Saaty (1–9). Bobot prioritas kriteria ke-$j$ ($w_j$) diperoleh melalui rata-rata baris dari elemen matriks yang telah dinormalisasi terhadap jumlah kolomnya:

$$
w_j = \frac{1}{n} \sum_{k=1}^n \frac{a_{jk}}{\sum_{i=1}^n a_{ik}} \quad \forall j \in \{1, 2, \dots, n\}
\tag{1}
$$

*Keterangan:*
- $n$ : Jumlah total kriteria yang dievaluasi.
- $a_{jk}$ : Nilai perbandingan berpasangan kriteria baris ke-$j$ terhadap kriteria kolom ke-$k$.
- $\sum_{i=1}^n a_{ik}$ : Jumlah total elemen pada kolom ke-$k$ matriks perbandingan berpasangan.
- $w_j$ : Bobot prioritas relatif kriteria ke-$j$, dengan batasan $\sum_{j=1}^n w_j = 1$.

> [!NOTE]
> Jika evaluasi melibatkan multiresponden/dewan pakar, nilai elemen matriks agregat diperoleh melalui rata-rata geometrik (*Geometric Mean*) sebelum normalisasi [[Paper JUSTIN (Mahendra, 2020)]]:
> $$ a_{jk} = \left( \prod_{p=1}^P a_{jk}^{(p)} \right)^{\frac{1}{P}} $$
> di mana $P$ adalah jumlah pakar dan $a_{jk}^{(p)}$ adalah penilaian pakar ke-$p$.

---

### Persamaan 2: Uji Konsistensi Logis Saaty (CI dan CR)
Guna memastikan bahwa penilaian perbandingan berpasangan bebas dari pertentangan logis dan bias subjektivitas berlebih [[Aksioma Konsistensi Saaty (CR)]], dihitung nilai *Consistency Index* ($CI$) dan *Consistency Ratio* ($CR$):

$$
CI = \frac{\lambda_{\max} - n}{n - 1}
\tag{2a}
$$

$$
CR = \frac{CI}{RI}
\tag{2b}
$$

*Keterangan:*
- $\lambda_{\max}$ : Nilai *eigen* terbesar (*principal eigenvalue*) yang diperoleh dari rata-rata elemen vektor konsistensi:
  $$ \lambda_{\max} = \frac{1}{n} \sum_{i=1}^n \frac{(A \cdot w)_i}{w_i} $$
- $n$ : Ordo atau ukuran matriks perbandingan berpasangan.
- $CI$ : Indeks konsistensi penyimpangan perbandingan.
- $RI$ : *Random Index*, yaitu indeks acak konsistensi rata-rata dari matriks acak berukuran $n$ yang distandardisasi oleh Saaty:
  - $n=3 \rightarrow RI=0{,}58$
  - $n=4 \rightarrow RI=0{,}90$
  - $n=5 \rightarrow RI=1{,}12$
  - $n=6 \rightarrow RI=1{,}24$
  - $n=7 \rightarrow RI=1{,}32$
- $CR$ : Rasio konsistensi matriks. Matriks perbandingan dinyatakan **valid dan konsisten** apabila memenuhi kondisi batas:
  $$ CR \le 0{,}10 \quad (10\%) $$

---

## 2. Fase Pemeringkatan Alternatif (Weighted Product)

Setelah vektor bobot $w = [w_1, w_2, \dots, w_n]^T$ dinyatakan konsisten ($CR \le 0{,}10$), bobot tersebut dialirkan ke algoritma WP sebagai eksponen pangkat.

### Persamaan 3: Normalisasi Pangkat Bobot & Perhitungan Vektor Preferensi Alternatif ($S_i$)
Bobot kriteria terlebih dahulu dinormalisasi untuk memastikan jumlah eksponen setara dengan 1:

$$
W_j = \frac{w_j}{\sum_{k=1}^n w_k}
\tag{3a}
$$

Selanjutnya, dihitung nilai vektor preferensi $S_i$ untuk setiap alternatif ke-$i$ ($i = 1, 2, \dots, m$) melalui perkalian seluruh atribut kriteria yang dipangkatkan dengan bobot yang bersangkutan [[Sifat Pemangkatan Eksponensial WP]]:

$$
S_i = \prod_{j=1}^n \left( x_{ij} \right)^{W_j^*} \quad \forall i \in \{1, 2, \dots, m\}
\tag{3b}
$$

di mana pemangkatan $W_j^*$ didefinisikan secara tegas berdasarkan sifat kriteria:
$$
W_j^* = 
\begin{cases} 
+W_j, & \text{jika kriteria } j \text{ bersifat keuntungan (benefit)} \\
-W_j, & \text{jika kriteria } j \text{ bersifat biaya/ongkos (cost)}
\end{cases}
$$

*Keterangan:*
- $m$ : Jumlah total alternatif (misal: platform investasi emas).
- $n$ : Jumlah total kriteria evaluasi.
- $x_{ij}$ : Nilai kinerja alternatif ke-$i$ pada kriteria ke-$j$.
- $W_j$ : Pangkat bobot ternormalisasi kriteria ke-$j$.
- $S_i$ : Skor agregasi multiplikatif non-linear alternatif ke-$i$. Perhitungan $S_i$ hanya melibatkan nilai internal alternatif $i$, sehingga terbebas secara mutlak dari pengaruh alternatif luar (*independent of irrelevant alternatives*).

---

### Persamaan 4: Perhitungan Nilai Preferensi Relatif Vektor ($V_i$) untuk Pemeringkatan
Nilai preferensi komprehensif relatif $V_i$ diperoleh dengan membagi nilai vektor $S_i$ dari alternatif ke-$i$ terhadap total penjumlahan nilai vektor $S$ dari seluruh alternatif yang dievaluasi:

$$
V_i = \frac{S_i}{\sum_{k=1}^m S_k} = \frac{\prod_{j=1}^n \left( x_{ij} \right)^{W_j^*}}{\sum_{k=1}^m \prod_{j=1}^n \left( x_{kj} \right)^{W_j^*}} \quad \forall i \in \{1, 2, \dots, m\}
\tag{4}
$$

*Keterangan:*
- $V_i$ : Nilai preferensi akhir relatif alternatif ke-$i$, dengan batasan $\sum_{i=1}^m V_i = 1$.
- Nilai $V_i$ terbesar ($V_{\max}$) menunjukkan alternatif optimal (peringkat pertama) yang paling direkomendasikan bagi calon investor.

> [!TIP]
> Penyajian matematis murni Persamaan (1) hingga (4) ini mengadopsi standar pemodelan analitik tanpa ketergantungan antarmuka perangkat lunak [[Paper Jurnal Krisnadana (Sutrisno, 2023)]], siap disalin secara langsung ke dalam format dokumen publikasi (Word/LaTeX template).
