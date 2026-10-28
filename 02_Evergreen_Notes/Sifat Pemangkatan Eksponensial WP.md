---
title: Sifat Pemangkatan Eksponensial WP
created: 2026-10-28
type: evergreen
tags:
  - teori
  - wp
  - eksponensial
  - rank-reversal-immune
  - mcdm
---

# Sifat Pemangkatan Eksponensial WP

## Mekanisme Matematis Perkalian Berpangkat
Metode *Weighted Product* (WP) menggunakan teknik agregasi non-linear yang didasarkan pada perkalian seluruh atribut nilai alternatif yang dipangkatkan dengan bobot kriteria terkait. Karakteristik inti algoritma ini terletak pada perhitungan **Vektor $S$**:

$$
S_i = \prod_{j=1}^n \left( x_{ij} \right)^{W_j^*}
$$

di mana:
- $x_{ij}$ : Nilai kinerja alternatif ke-$i$ pada kriteria ke-$j$.
- $W_j^*$ : Pangkat bobot ternormalisasi, dengan nilai bernilai positif untuk kriteria keuntungan (*benefit*) dan negatif untuk kriteria biaya (*cost*).

## Mengapa Vektor S Kebal Terhadap Rank Reversal?
Kekebalan metode WP terhadap anomali [[Teori Rank Reversal pada AHP]] bertumpu pada sifat algebra perkalian eksponensial:

1. **Kemandirian Evaluasi Alternatif (*Independence of Irrelevant Alternatives - IIA*)**:
   Perhitungan nilai skor absolut $S_i$ untuk alternatif $i$ **hanya** bergantung pada matriks data internal alternatif $i$ ($x_{ij}$) dan vektor bobot kriteria ($W_j$). Nilai $S_i$ sama sekali tidak melibatkan nilai alternatif lain ($x_{kj}$ untuk $k \neq i$) maupun penjumlahan agregat antar-alternatif.
   
2. **Kekekalan Rasio Preferensi**:
   Jika kita membandingkan preferensi relatif antara alternatif $A_1$ dan $A_2$:
   $$
   \frac{S_1}{S_2} = \frac{\prod_{j=1}^n x_{1j}^{W_j^*}}{\prod_{j=1}^n x_{2j}^{W_j^*}} = \prod_{j=1}^n \left( \frac{x_{1j}}{x_{2j}} \right)^{W_j^*}
   $$
   Perhatikan bahwa rasio $\frac{S_1}{S_2}$ adalah konstanta murni yang sepenuhnya bebas dari alternatif ketiga ($A_3$) atau alternatif baru ($A_{new}$). Jika $S_1 > S_2$, maka rasio $\frac{S_1}{S_2} > 1$ akan selalu berlaku, berapapun jumlah alternatif baru yang dimasukkan ke dalam sistem.

3. **Peran Vektor $V_i$ pada Normalisasi Akhir**:
   Tahap akhir pembagian $V_i = \frac{S_i}{\sum S_k}$ hanyalah penskalaan linier sederhana agar total probabilitas preferensi berjumlah 1 ($\sum V_i = 1$). Karena semua $S_i$ dibagi oleh angka skalar yang sama ($\sum S_k$), urutan monotonik peringkat ($V_1 > V_2 \iff S_1 > S_2$) dijamin tidak pernah tertukar.

## Formulasi Benefit vs Cost
- **Kriteria Keuntungan (*Benefit*)**: Dipangkatkan dengan eksponen positif ($+W_j$). Semakin besar nilai $x_{ij}$, semakin besar nilai $S_i$. Contoh pada platform emas: likuiditas pencairan, legalitas izin regulasi, kemudahan fitur.
- **Kriteria Biaya (*Cost*)**: Dipangkatkan dengan eksponen negatif ($-W_j$), yang secara matematis ekuivalen dengan pembagian:
  $$ x_{ij}^{-W_j} = \frac{1}{x_{ij}^{W_j}} $$
  Semakin tinggi biaya atau selisih harga (*spread*) buyback pada suatu platform, semakin mengecil nilai $S_i$ secara proporsional.

Penyajian formulasi murni ini diadopsi secara konsisten sesuai kaidah algoritmik tanpa distorsi sistem [[Paper Jurnal Krisnadana (Sutrisno, 2023)]].

---
**Terkait:**
- [[Teori Rank Reversal pada AHP]]
- [[Draft_Persamaan_Matematika]]
- [[Paper Jurnal Krisnadana (Sutrisno, 2023)]]
- [[Draft_Pendahuluan]]
