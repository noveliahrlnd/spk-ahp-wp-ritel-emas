---
title: Aksioma Konsistensi Saaty (CR)
created: 2026-10-28
type: evergreen
tags:
  - teori
  - ahp
  - consistency-ratio
  - saaty
  - mcdm
---

# Aksioma Konsistensi Saaty (CR)

## Fondasi Aksiomatik AHP
Metode *Analytic Hierarchy Process* (AHP) dirancang oleh Thomas L. Saaty di atas empat aksioma utama:
1. **Aksioma Resiprokal (*Reciprocal Axiom*)**: Jika kriteria $A$ bernilai $x$ kali lebih penting daripada kriteria $B$, maka secara otomatis kriteria $B$ bernilai $\frac{1}{x}$ kali penting dibanding $A$ ($a_{ji} = \frac{1}{a_{ij}}$).
2. **Aksioma Homogenitas (*Homogeneity Axiom*)**: Elemen-elemen yang dibandingkan tidak boleh memiliki perbedaan skala tak hingga; skala Saaty dibatasi pada rentang diskrit 1 sampai 9.
3. **Aksioma Ketergantungan (*Dependency Axiom*)**: Struktur keputusan tersusun secara hierarki linier dari tujuan (*goal*), kriteria, subkriteria, hingga alternatif.
4. **Aksioma Harapan (*Expectation Axiom*)**: Prioritas global merefleksikan seluruh preferensi dan intensitas penilaian yang disintesis dalam struktur hierarki.

## Urgensi Menekan Bias Subjektivitas di Bawah 0,10
Manusia memiliki keterbatasan kognitif dalam menjaga konsistensi transitif ketika membandingkan banyak kriteria secara simultan. Sebagai contoh ketidakkonsistenan:
- Jika Kriteria Keamanan 3 kali lebih penting dari Biaya ($A > B$ bernilai 3),
- dan Biaya 2 kali lebih penting dari Kemudahan Akses ($B > C$ bernilai 2),
- maka secara konsisten sempurna, Keamanan harus bernilai $3 \times 2 = 6$ kali lebih penting dari Kemudahan Akses ($A > C$).

Apabila penilai memberikan nilai yang bertentangan (misalnya menilai $C$ lebih penting dari $A$), terjadi inkonsistensi logis. Saaty menetapkan deviasi konsistensi melalui:
$$ CI = \frac{\lambda_{\max} - n}{n - 1} $$
$$ CR = \frac{CI}{RI} $$

Ambang batas yang ditetapkan secara universal adalah:
$$ CR \le 0{,}10 \quad (10\%) $$

### Mengapa Batas Ambang 0,10 Sangat Krusial?
- **Validitas Rasional Pengambil Keputusan**: Nilai $CR \le 0{,}10$ membuktikan bahwa pertimbangan pakar bersifat terstruktur, rasional, dan berada dalam rentang toleransi galat acak manusiawi.
- **Mencegah Bias Emosional**: Menolak matriks yang $CR > 0{,}10$ memaksa pengambil keputusan untuk mengevaluasi ulang penimbangannya agar terbebas dari opini sesaat atau kontradiksi internal.
- **Dasar Bobot untuk WP**: Hanya bobot yang lolos uji konsistensi ($CR \le 0{,}10$) yang memiliki integritas ilmiah untuk dijadikan eksponen pangkat pada metode [[Sifat Pemangkatan Eksponensial WP]].

## Agregasi Multi-Pakar Menggunakan Geometric Mean
Dalam studi empiris pemilihan platform investasi emas, penilaian perbandingan sering kali melibatkan lebih dari satu pakar/responden (misal: pakar komoditas emas, regulator, dan praktisi finansial). Untuk menggabungkan beberapa matriks pertimbangan tanpa melanggar aksioma resiprokal AHP, digunakan metode **Geometric Mean** [[Paper JUSTIN (Mahendra, 2020)]]:
$$ a_{jk} = \sqrt[P]{\prod_{p=1}^P a_{jk}^{(p)}} $$
di mana $P$ adalah jumlah pakar dan $a_{jk}^{(p)}$ adalah nilai perbandingan dari pakar ke-$p$. Penggunaan rata-rata geometrik menjamin terjaganya sifat resiprokal matriks agregat ($a_{kj} = \frac{1}{a_{jk}}$).

---
**Terkait:**
- [[Draft_Pendahuluan]]
- [[Draft_Persamaan_Matematika]]
- [[Paper JUSTIN (Mahendra, 2020)]]
- [[Teori Rank Reversal pada AHP]]
