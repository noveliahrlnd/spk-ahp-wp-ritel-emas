# Boukrouh, Tayalati, & Azmani (2024) — Kerangka Komparatif MCDM Subjektif, Objektif, dan Hibrida dengan Analisis Sensitivitas pada Sektor Ritel

- **Sitasi IEEE:** I. Boukrouh, F. Tayalati, and A. Azmani, "A comprehensive framework for supplier selection: Using subjective, objective, and hybrid multi-criteria decision-making techniques with sensitivity analysis," *IEEE Access*, vol. 12, pp. 145550–145569, 2024, doi: 10.1109/ACCESS.2024.3462348.
- **PDF Lokal:** `../papers/IEEEAccess_Boukrouh_2024.pdf`
- **Tahun:** 2024
- **Topik Utama:** Perbandingan metode pembobotan subjektif (AHP, FAHP), objektif (Entropy), dan hibrida (AHP-Entropy, FAHP-Entropy) bersama TOPSIS serta analisis sensitivitas 21 skenario.

## Ringkasan Inti
- **Permasalahan & Tujuan:** Ketergantungan penuh pada model pembobotan subjektif dapat menimbulkan bias akibat ambiguitas opini manusia, sementara perbandingan langsung efisiensi antara pendekatan subjektif, objektif, dan hibrida pada satu kasus identik masih terbatas. Penelitian ini menyusun kerangka perbandingan lima pendekatan pembobotan MCDM dengan TOPSIS serta menguji ketahanannya melalui analisis sensitivitas multi-skenario pada pemilihan pemasok sektor ritel daring.
- **Metode / Pendekatan:** Empat alternatif pemasok dievaluasi atas 7 kriteria utama dan 21 sub-kriteria berdasarkan penilaian 3 pakar industri (pengalaman 8–12 tahun). Bobot dihitung melalui AHP (tervalidasi dengan $CR = 0{,}09 < 0{,}10$ pada kriteria utama dan $0{,}0334\text{--}0{,}0942$ pada sub-kriteria), FAHP berbasis *Triangular Fuzzy Number* (TFN), Entropy, AHP-Entropy, dan FAHP-Entropy, lalu diperingkat dengan TOPSIS dan diuji ketahanannya memakai 21 skenario permutasi bobot serta jarak Euclidean rata-rata.
- **Temuan Kunci:**
  - Metode pembobotan berpengaruh signifikan terhadap peringkat akhir: AHP-TOPSIS dan FAHP-TOPSIS menghasilkan urutan $A_1 > A_4 > A_3 > A_2$ (bobot utama tertinggi pada kualitas $C_1$: `0,3749` dan `0,3820`), Entropy-TOPSIS menghasilkan $A_2 > A_1 > A_3 > A_4$, sedangkan hibrida AHP-Entropy dan FAHP-Entropy menghasilkan $A_1 > A_2 > A_4 > A_3$.
  - Pada uji sensitivitas 21 skenario (Tabel 27–28), urutan hibrida $A_1 > A_2 > A_4 > A_3$ menjadi peringkat paling dominan (muncul konsisten pada 15 skenario $S_7\text{--}S_{21}$, dengan $A_1$ peringkat 1 di 18 skenario; catatan: abstrak artikel menyebut 19 skenario), sementara Entropy cocok di 3 skenario ($S_4\text{--}S_6$) dan AHP/FAHP murni di 0 skenario.
  - Berdasarkan jarak Euclidean rata-rata terhadap skor seluruh skenario sensitivitas (Tabel 29), FAHP-Entropy-TOPSIS (`0,19574`) dan AHP-Entropy-TOPSIS (`0,2290`) paling selaras dibandingkan Entropy (`0,34690`), FAHP (`0,39085`), dan AHP (`0,43461`).

## Relevansi untuk Paper SPK (AHP-WP Lokasi Toko Emas DIY)
- **Bagian yang Cocok Dikutip:** Pendahuluan, Metode (Desain Penelitian: validasi konsistensi AHP), serta Hasil dan Pembahasan (Evaluasi: analisis sensitivitas skenario bobot).
- **Poin Argumen yang Didukung:** Memperkuat dasar ilmiah pentingnya uji konsistensi AHP ($CR < 0{,}10$) serta analisis sensitivitas berbasis skenario perubahan bobot dalam pengambilan keputusan bisnis ritel, sekaligus memberi pijakan untuk mendiskusikan potensi integrasi pembobotan objektif (seperti Entropy) sebagai pengembangan riset lanjutan.
