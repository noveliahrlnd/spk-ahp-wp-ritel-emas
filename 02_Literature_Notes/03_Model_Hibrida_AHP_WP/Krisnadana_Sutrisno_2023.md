# Sutrisno et al. (2023) — Evaluasi Keputusan Hibrida AHP-WP

- **Sitasi IEEE:** Sutrisno, N. Mayasari, M. Rohim, and Y. Boari, "Evaluasi Keputusan Kelayakan Bonus Karyawan Menggunakan Metode AHP-WP," *Jurnal Krisnadana*, vol. 3, no. 1, pp. 49–58, Sep. 2023.
- **PDF Lokal:** `../papers/Krisnadana_Sutrisno_2023.pdf`
- **Tahun:** 2023
- **Topik Utama:** Penerapan integrasi matematis AHP untuk pembobotan kriteria dan Weighted Product (WP) untuk pemeringkatan alternatif.

## Ringkasan Inti
- **Permasalahan & Tujuan:** Mengembangkan model evaluasi multikriteria yang objektif dan sistematis untuk menentukan kelayakan penerima bonus karyawan menggunakan kombinasi metode AHP-WP.
- **Metode / Pendekatan:** AHP dipakai menghitung bobot prioritas 5 kriteria melalui matriks perbandingan berpasangan, normalisasi, eigen vector, dan uji *Consistency Ratio* ($CR$). Bobot valid tersebut kemudian dipakai pada metode WP untuk menghitung Vektor $S_i$ (pemangkatan bobot) dan Vektor $V_i$ (normalisasi akhir) terhadap 4 alternatif karyawan.
- **Temuan Kunci:**
  - Uji konsistensi AHP menghasilkan $CR = 0{,}0441 < 0{,}10$ sehingga bobot kriteria valid.
  - Metode WP menghasilkan peringkat akhir yang tegas dengan alternatif $A_3$ sebagai prioritas utama ($S_3 = 4{,}2662$, $V_3 = 0{,}3060$).
  - Menyajikan alur komputasi matematis hibrida AHP-WP secara terstruktur dan transparan tanpa bergantung pada pengembangan antarmuka perangkat lunak.

## Relevansi untuk Paper SPK (AHP-WP Lokasi Toko Emas DIY)
- **Bagian yang Cocok Dikutip:** Pendahuluan (studi terdahulu AHP-WP); Metode (Desain Penelitian); Hasil dan Pembahasan (Perhitungan AHP & WP).
- **Poin Argumen yang Didukung:** Mendukung efektivitas arsitektur sekuensial AHP (penentuan bobot konsisten) yang diteruskan ke WP (perhitungan Vektor $S_i$ dan $V_i$) dalam pengambilan keputusan multikriteria murni matematis.
