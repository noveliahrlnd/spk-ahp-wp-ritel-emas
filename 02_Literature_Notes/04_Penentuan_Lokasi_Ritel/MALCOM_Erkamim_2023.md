# Erkamim et al. (2023) — Implementasi AHP Pemilihan Lahan & Uji Konsistensi

- **Sitasi IEEE:** M. Erkamim, Sepriano, I. G. I. Sudipa, K. Nisa, A. Z. A. Alaydrus, and Legito, "Implementasi Metode Analytic Hierarchy Process untuk Pemilihan Lahan Perkebunan Kelapa Sawit di Riau," *MALCOM: Indonesian Journal of Machine Learning and Computer Science*, vol. 3, no. 2, pp. 76–82, Oct. 2023, doi: 10.57152/malcom.v3i2.871.
- **PDF Lokal:** `../papers/MALCOM_Erkamim_2023.pdf`
- **Tahun:** 2023
- **Topik Utama:** Penerapan AHP pada masalah seleksi lokasi/lahan multikriteria dengan validasi konsistensi $CR$.

## Ringkasan Inti
- **Permasalahan & Tujuan:** Menyusun sistem pendukung keputusan pemilihan lokasi lahan perkebunan kelapa sawit terbaik dari 12 kabupaten/kota di Provinsi Riau menggunakan metode AHP.
- **Metode / Pendekatan:** Dekomposisi 5 kriteria lahan (curah hujan, ketinggian DPL, kandungan bahan dasar, ketebalan gambut, keasaman tanah), konstruksi matriks perbandingan berpasangan berskala Saaty 1–9, perhitungan nilai eigen, pemeringkatan 12 alternatif, serta pengujian *Consistency Ratio* ($CR$).
- **Temuan Kunci:**
  - Kriteria ketebalan gambut memperoleh bobot tertinggi (0,506), diikuti curah hujan (0,248).
  - Pengujian konsistensi menghasilkan $CR = 0{,}026$ (2,6% < 10%), menandakan matriks perbandingan konsisten.
  - Kuantan Singingi terpilih sebagai prioritas pertama (0,209) dari 12 alternatif.

## Relevansi untuk Paper SPK (AHP-WP Lokasi Toko Emas DIY)
- **Bagian yang Cocok Dikutip:** Pendahuluan (penerapan AHP dalam seleksi lokasi/spasial); Metode (skala Saaty 1–9 dan validasi $CR$); sekaligus acuan langsung gaya penyajian jurnal target **MALCOM**.
- **Poin Argumen yang Didukung:** Memperkuat penggunaan struktur hierarki AHP dan ambang batas $CR \le 0{,}10$ untuk memperoleh bobot prioritas kriteria yang terukur secara objektif pada kasus pemilihan lokasi.
