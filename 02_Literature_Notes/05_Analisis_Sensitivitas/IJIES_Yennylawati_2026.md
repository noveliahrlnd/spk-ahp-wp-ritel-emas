# Yennylawati et al. (2026) — Optimasi Rasio Konsistensi AHP Berbasis Korelasi dan Rata-Rata Terbobot

- **Sitasi IEEE:** E. Yennylawati, R. Gernowo, and A. F. Rochim, “Optimizing AHP Consistency Ratio Through Correlation Theory and Weighted Mean,” *International Journal of Intelligent Engineering and Systems*, vol. 19, no. 4, pp. 404–423, 2026, doi: 10.22266/ijies2026.0430.23.
- **PDF Lokal:** `../papers/IJIES_Yennylawati_2026.pdf`
- **Tahun:** 2026
- **Topik Utama:** Validasi konsistensi AHP ($CR \le 0,10$), perbandingan pembobotan subjektif-objektif-hibrida, serta uji ketangguhan (*robustness*) pemeringkatan MCDM di bawah perturbasi data.

## Ringkasan Inti
- **Permasalahan & Tujuan:** Metode pembobotan subjektif seperti AHP menjamin koherensi logis melalui *Consistency Ratio* ($CR$), tetapi sensitif terhadap bias penilai; sebaliknya, metode objektif (CRITIC, D-CRITIC, CCSD) tidak memiliki audit konsistensi. Penelitian ini mengembangkan V-CRITIC, skema pembobotan hibrida berbasis korelasi Pearson dan *weighted mean* yang menghasilkan matriks perbandingan berpasangan kompatibel-AHP dengan $CR$ rendah dan bobot tangguh.
- **Metode / Pendekatan:** V-CRITIC menormalisasi matriks keputusan, menghitung korelasi Pearson dan rasio konflik relatif ($R_j$), membentuk matriks konsistensi konflik ($M_{jk}$), lalu menurunkan matriks perbandingan berpasangan untuk diuji menggunakan $\lambda_{\max}$, $CI$, $RI$ ($1,24$ untuk $n = 6$), dan $CR$. Pengujian dilakukan pada dua dataset (D1: 6 kriteria × 6 alternatif hambatan rantai pasok kelapa dari 65 publikasi; D2: dataset Kaggle *Green Supply Chain* 1.000 rekaman/5 alternatif × 6 kriteria) pada *solver* TOPSIS, MOORA, dan SAW dengan perturbasi $\pm 1\%$ hingga $\pm 10\%$ serta uji korelasi peringkat Spearman ($\rho$).
- **Temuan Kunci:**
  - Pada D1 ($n = 6$, $RI = 1,24$), V-CRITIC mencapai $\lambda_{\max} = 6,31$, $CI = 0,06$, dan $CR \approx 5,0\%$ (deviasi bobot rata-rata $\approx 5\%$ terhadap AHP); pada D2, $CR$ mencapai $\approx 1,21\%$, jauh lebih rendah dari *baseline* hibrida AHP-CRITIC dan AHP-Entropy ($\approx 8,42\%$).
  - Bobot V-CRITIC pada D1 (`So=0,24; In=0,21; Fa=0,15; Iv=0,13; Tr=0,13; Pr=0,14`) sangat mendekati pola bobot AHP (`0,25; 0,23; 0,14; 0,13; 0,13; 0,13`) sekaligus mencegah penghitungan ganda pada kriteria berkorelasi.
  - Pada seluruh tingkat perturbasi matriks keputusan ($\pm 1\%$, $\pm 5\%$, $\pm 10\%$), pemeringkatan pada TOPSIS, MOORA, dan SAW tetap stabil secara struktural dengan korelasi peringkat Spearman $\rho = 1,00$ pada D1 maupun D2.

## Relevansi untuk Paper SPK (AHP-WP Lokasi Toko Emas DIY)
- **Bagian yang Cocok Dikutip:** Pendahuluan; Metode (Desain Penelitian & Uji Konsistensi AHP); Hasil dan Pembahasan (Perhitungan AHP & Evaluasi).
- **Poin Argumen yang Didukung:** Menjadi rujukan metodologis sangat mutakhir (2026) yang mengukuhkan posisi AHP sebagai standar acuan koherensi logis melalui pengujian $\lambda_{\max}$, $CI$, $RI = 1,24$ (tepat sama untuk $n = 6$ kriteria pada paper ini), dan ambang $CR \le 0,10$, sekaligus menekankan pentingnya mengevaluasi ketangguhan (*robustness*) pemeringkatan di tingkat *output* keputusan (tidak hanya bobot) melalui uji perturbasi serta potensi pengembangan pembobotan objektif-hibrida di penelitian mendatang.
