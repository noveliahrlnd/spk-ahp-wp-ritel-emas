# Jiang, Liao, & De Baets (2024) — Simulasi Probabilitas Rank Reversal, Tie Making, dan Tie Breaking pada Metode MCDM

- **Sitasi IEEE:** L. Jiang, H. Liao, and B. De Baets, "A simulation study on the probabilities of rank reversal, tie making, and tie breaking for multiple criteria decision making methods," *Omega*, vol. 125, Jun. 2024, Art. no. 103033, doi: 10.1016/j.omega.2023.103033.
- **PDF Lokal:** `../papers/Omega_Jiang_Liao_DeBaets_2024.pdf`
- **Tahun:** 2024
- **Topik Utama:** Evaluasi probabilitas *rank reversal*, *tie making*, dan *tie breaking* pada 30 versi dari 12 metode MCDM melalui simulasi skala besar.

## Ringkasan Inti
- **Permasalahan & Tujuan:** Studi simulasi *rank reversal* terdahulu masih mencakup sedikit metode MCDM, belum menelaah pengaruh posisi peringkat alternatif yang dihapus, serta mengabaikan fenomena peringkat seri (*ties*). Penelitian ini membandingkan secara menyeluruh probabilitas *rank reversal* sekaligus memperkenalkan dua fenomena baru, yakni *tie making* (preferensi ketat menjadi seri) dan *tie breaking* (seri menjadi preferensi ketat).
- **Metode / Pendekatan:** Eksperimen simulasi dijalankan pada dua kategori input dengan 1.000 replikasi per skenario: 42 skenario data perbandingan berpasangan (CIS: AHP_RE, AHP_LGP, AHP_LLSM, QSP, BWM) dan 224 skenario data evaluasi berkriteria (EIS: SWM, MEW/WP, DNMA, GLDS, 5 versi PROMETHEE II, 12 versi TODIM, dan 4 versi TOPSIS). Pengaruh 6 faktor simulasi (jumlah alternatif 3–15, jumlah kriteria 2–30, konsistensi, skala rasio maks. 5/7/9, distribusi data, dan tipe bobot) dianalisis menggunakan regresi *step-wise*.
- **Temuan Kunci:**
  - Pada data perbandingan berpasangan (CIS), matriks yang konsisten menghasilkan probabilitas *rank reversal*, *tie making*, dan *tie breaking* tepat `0` untuk AHP_RE, AHP_LGP, dan AHP_LLSM; konsistensi menurunkan probabilitas *rank reversal* AHP_RE secara signifikan ($\theta_3 = -0{,}7384$, $p = 0$).
  - Pada data evaluasi (EIS), bobot independen-evaluasi tidak meningkatkan probabilitas *rank reversal* dibanding bobot dependen-evaluasi (CRITIC). Khusus untuk MEW (Weighted Product, $\theta_7 = 0{,}3458$) dan SWM ($\theta_7 = 0{,}3873$), operasi penambahan atau penghapusan alternatif tidak memengaruhi probabilitas *rank reversal* ($\theta_4 = 0$).
  - Penghapusan alternatif peringkat pertama atau terakhir memicu probabilitas *rank reversal* lebih rendah daripada alternatif tengah pada metode perbandingan berpasangan (kurva "$\wedge$"), tetapi justru lebih tinggi pada metode data evaluasi (kurva "$\vee$"), kecuali SWM dan MEW saat memakai bobot independen-evaluasi.

## Relevansi untuk Paper SPK (AHP-WP Lokasi Toko Emas DIY)
- **Bagian yang Cocok Dikutip:** Pendahuluan, Metode (Desain Penelitian), serta Hasil dan Pembahasan (Evaluasi: stabilitas peringkat terhadap *rank reversal* / aksioma IIA).
- **Poin Argumen yang Didukung:** Memberikan bukti empiris mutakhir bahwa kombinasi pembobotan AHP yang konsisten (independen terhadap data evaluasi) dan pemeringkatan eksponensial WP/MEW memiliki ketahanan unggul terhadap anomali *rank reversal* saat alternatif lokasi ditambah atau dihapus.
