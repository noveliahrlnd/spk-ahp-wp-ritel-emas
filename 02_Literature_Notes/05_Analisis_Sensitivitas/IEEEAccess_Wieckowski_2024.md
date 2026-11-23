# Więckowski, Wątróbski, & Sałabun (2024) — Analisis Komparatif Ketahanan RANCOM dan AHP terhadap Ketidakakuratan Penilaian Pakar pada Pemilihan Lokasi

- **Sitasi IEEE:** J. Więckowski, J. Wątróbski, and W. Sałabun, "Inaccuracies in expert judgment: Comparative analysis of RANCOM and AHP methods in housing location selection problem," *IEEE Access*, vol. 12, pp. 142083–142100, 2024, doi: 10.1109/ACCESS.2024.3443451.
- **PDF Lokal:** `../papers/IEEEAccess_Wieckowski_2024.pdf`
- **Tahun:** 2024
- **Topik Utama:** Perbandingan sensitivitas dan stabilitas pembobotan subjektif AHP vs RANCOM terhadap galat penilaian pakar (5%–40%) pada masalah pemilihan lokasi.

## Ringkasan Inti
- **Permasalahan & Tujuan:** Metode pembobotan subjektif berbasis perbandingan berpasangan seperti AHP rentan terhadap inkonsistensi dan keraguan penilaian ketika jumlah kriteria meningkat. Penelitian ini membandingkan kinerja, konsistensi, serta ketahanan peringkat AHP dan RANCOM ketika diintegrasikan dengan 9 metode MCDA di bawah berbagai tingkat ketidakakuratan respons pakar pada studi kasus pemilihan lokasi hunian.
- **Metode / Pendekatan:** Studi empiris mengevaluasi 16 alternatif lokasi hunian di Polandia menggunakan 8 kriteria (28 pasangan perbandingan unik) dan 3 profil pengambil keputusan. Bobot AHP dan RANCOM digabungkan ke 9 metode MCDA (ARAS, EDAS, COPRAS, MABAC, MAIRCA, MOORA, TOPSIS, PROMETHEE II, VIKOR), lalu disimulasikan galat penilaian sebesar 5%–40% (1–11 kesalahan entri) dan diukur konsistensinya ($CR$ vs $1 - C_{Tr}$) serta kemiripan peringkatnya dengan koefisien $WS$ dan *Weighted Spearman* ($r_W$).
- **Temuan Kunci:**
  - Pada kondisi tanpa galat simulasi, bobot AHP dan RANCOM menghasilkan peringkat antar-MCDA yang sangat seragam ($WS = 0{,}882\text{--}0{,}951$ dan $r_W = 0{,}858\text{--}0{,}951$ untuk AHP; $WS = 0{,}893\text{--}0{,}943$ dan $r_W = 0{,}833\text{--}0{,}943$ untuk RANCOM), dengan AHP memberikan sebaran bobot lebih tajam pada kriteria paling dominan.
  - Konsistensi AHP ($CR$) merosot drastis saat galat meningkat—dari `0,095–0,167` (galat 5%) menjadi `0,515–0,968` (galat 40%, puncak `1,027` pada Expert$_2$ galat 20%)—sedangkan RANCOM ($1 - C_{Tr}$) terjaga di rentang `0,000–0,285`.
  - Ketahanan peringkat terhadap gangguan penilaian lebih tinggi pada RANCOM ($r_W \in [0{,}65, 1{,}00]$ untuk Expert$_1$) dibanding AHP ($r_W \in [0{,}25, 1{,}00]$ untuk Expert$_1$ dan $[0{,}53, 1{,}00]$ untuk Expert$_2$).

## Relevansi untuk Paper SPK (AHP-WP Lokasi Toko Emas DIY)
- **Bagian yang Cocok Dikutip:** Pendahuluan, Metode (Data Kriteria & Desain Penelitian), serta Hasil dan Pembahasan (Evaluasi: analisis sensitivitas bobot).
- **Poin Argumen yang Didukung:** Mendukung argumen bahwa dalam pemilihan lokasi berbasis preferensi subjektif, AHP unggul membedakan bobot kriteria dominan secara kontras (seperti $C_3$ daya beli sebesar `46,14%`), namun sensitivitasnya terhadap ketidakakuratan penilaian mengharuskan pengujian konsistensi ketat ($CR \le 0{,}10$) dan uji sensitivitas bobot secara eksplisit pada tahap evaluasi.
