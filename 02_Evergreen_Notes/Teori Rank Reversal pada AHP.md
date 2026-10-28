---
title: Teori Rank Reversal pada AHP
created: 2026-10-28
type: evergreen
tags:
  - teori
  - ahp
  - rank-reversal
  - mcdm
---

# Teori Rank Reversal pada AHP

## Definisi dan Fenomena
*Rank Reversal* (pembalikan peringkat) adalah sebuah anomali atau paradoks matematis dalam metode pengambilan keputusan multikriteria (*Multi-Criteria Decision Making* / MCDM) di mana urutan preferensi relatif antar-alternatif yang ada berubah (misalnya alternatif $A_1 > A_2$ berbalik menjadi $A_2 > A_1$) semata-mata karena:
1. Ditambahkannya alternatif baru (meskipun alternatif baru tersebut identik, sangat inferior, atau tidak relevan).
2. Dihapuskannya salah satu alternatif yang tidak terpilih dari himpunan alternatif.

Fenomena ini pertama kali diidentifikasi secara kritis oleh Belton dan Gear (1983) dan terus menjadi perdebatan metodologis fundamental dalam penerapan *Analytic Hierarchy Process* (AHP) konvensional.

## Mengapa AHP Rentan Terhadap Rank Reversal?
Kerentanan struktural AHP berakar pada dua mekanisme kalkulasinya:
1. **Normalisasi Aditif Berbasis Jumlah Kolom Matriks Lokal**:
   Dalam AHP murni, skor performa alternatif terhadap kriteria dihitung melalui normalisasi perbandingan berpasangan alternatif:
   $$ \bar{a}_{ik} = \frac{a_{ik}}{\sum_{i=1}^m a_{ik}} $$
   Penyebut pada rumus ini ($\sum_{i=1}^m a_{ik}$) merupakan fungsi dari *seluruh* alternatif yang ada. Ketika alternatif baru dimasukkan, penyebut berubah untuk semua alternatif, mendistorsi skala perbandingan lokal secara tidak proporsional.
2. **Ketergantungan Terhadap Alternatif Tidak Relevan**:
   Mekanisme ini melanggar aksioma *Independence of Irrelevant Alternatives* (IIA) yang dirumuskan oleh Kenneth Arrow. Penilaian terhadap preferensi relatif antara opsi $A_1$ dan $A_2$ seharusnya tidak boleh dipengaruhi oleh hadir atau tidaknya opsi $A_3$.

Validasi mutakhir mengenai kelemahan struktural rank reversal pada AHP telah dipublikasikan dan dibuktikan secara matematis dalam literatur internasional terindeks [[Paper Axioms (Yan & Mao, 2025)]].

## Justifikasi Mengapa Menggunakan Weighted Product (WP)
Dalam studi kasus dinamis seperti **pemilihan platform investasi emas**, alternatif platform senantiasa bertambah atau berkembang:
- Jika perankingan alternatif menggunakan AHP murni, masuknya platform baru ke dalam sistem dapat membalikkan peringkat platform terbaik yang sebelumnya direkomendasikan kepada calon investor, meskipun performa internal platform tersebut tidak berubah sama sekali. Hal ini sangat merusak kredibilitas sistem pendukung keputusan.
- Oleh karena itu, arsitektur keputusan yang tangguh membatasi penggunaan AHP **hanya untuk penentuan bobot kriteria global**, di mana perbandingan antar kriteria stabil dan tidak terpengaruh oleh jumlah alternatif.
- Tahap perangkingan dialihkan ke metode *Weighted Product* (WP), yang memanfaatkan [[Sifat Pemangkatan Eksponensial WP]] sehingga secara inheren kebal terhadap efek *rank reversal*.

---
**Terkait:**
- [[Draft_Pendahuluan]]
- [[Paper Axioms (Yan & Mao, 2025)]]
- [[Sifat Pemangkatan Eksponensial WP]]
- [[Aksioma Konsistensi Saaty (CR)]]
