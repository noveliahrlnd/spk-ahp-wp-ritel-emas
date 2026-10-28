---
title: Draf Pendahuluan - Integrasi Metode AHP dan Weighted Product pada Penentuan Lokasi Strategis Bisnis Ritel Perhiasan
created: 2026-10-28
status: Ready for Manuscript
target_journal: Template UIN SUSKA (Jurnal Ilmiah Rekayasa dan Manajemen Sistem Informasi)
tags:
  - draft
  - pendahuluan
  - ahp-wp
  - lokasi-ritel-emas
---

# PENDAHULUAN

Komoditas emas mencatatkan rekor lonjakan harga tertinggi pada tahun 2025 sebagai refleksi langsung dari ketidakpastian ekonomi global dan pelemahan nilai tukar rupiah. Meskipun harga mengalami volatilitas yang tajam, emas secara konsisten dipertahankan oleh masyarakat sebagai aset pelindung nilai (*safe haven asset*) utama di tengah gejolak pasar [[1]]. Fenomena lonjakan harga ini secara empiris tidak menyurutkan minat beli, melainkan memicu pergeseran preferensi transaksi ke produk yang lebih fleksibel, di mana 41,7% masyarakat beralih pada produk cicil emas dan 25% memilih tabungan emas fisik. Tingginya adaptabilitas dan resiliensi permintaan pasar ini berdampak langsung pada urgensi ekspansi industri ritel perhiasan dan layanan fisik emas. Dalam manajemen operasional, pembukaan cabang gerai toko emas baru menuntut penyelesaian masalah *Multi-Criteria Decision Making* (MCDM) yang presisi untuk menentukan penempatan lokasi strategis. Investor dihadapkan pada struktur kalkulasi yang mewajibkan kalibrasi matematis simultan antara atribut biaya (*cost*), seperti beban harga sewa properti tahunan, dengan atribut keuntungan (*benefit*) yang meliputi tingkat keamanan eksternal kawasan, potensi daya beli lingkungan, visibilitas lokasi, fleksibilitas modifikasi struktur bangunan, dan aglomerasi sentra perhiasan.

*Analytic Hierarchy Process* (AHP) merupakan salah satu alat komputasi yang secara luas diaplikasikan dalam pemodelan hierarki keputusan multikriteria spasial karena kemampuannya menyusun prioritas bobot melalui perbandingan berpasangan (*pairwise comparison*) dan memvalidasi konsistensi logis penilai melalui *Consistency Ratio* (CR) dengan batas toleransi $CR \le 0{,}10$ [[2]]. Namun, penerapan AHP secara tunggal hingga tahap pemeringkatan alternatif memiliki celah struktural yang secara akademis menuai kritik luas, yaitu kerentanan terhadap anomali *rank reversal* [[3]]. Masalah pembalikan peringkat ini terjadi ketika urutan preferensi dari alternatif yang sudah ada mengalami perubahan posisi secara tidak logis semata-mata akibat penambahan atau eliminasi alternatif identik atau alternatif baru yang tidak relevan ke dalam gugus keputusan. Dalam konteks investasi gerai fisik perhiasan berkapital tinggi, ketidakstabilan peringkat tersebut mendisrupsi kepastian bisnis dan berisiko fatal pada alokasi modal operasional.

Studi teoretis membuktikan bahwa anomali *rank reversal* pada AHP murni berakar dari skema normalisasi penjumlahan aditif dan interdependensi lokal antaralternatif dalam matriks [[3], [4]]. Untuk memitigasi kerentanan tersebut, penelitian ini membatasi peran AHP secara ketat hanya pada fase penentuan bobot kriteria global. Guna mengevaluasi dan meranking kandidat lokasi toko emas secara objektif dan stabil, metode *Weighted Product* (WP) diintegrasikan sebagai mesin perankingan tahap akhir [[5]]. Metode WP memanfaatkan operasi perkalian eksponensial di mana nilai kinerja setiap alternatif dipangkatkan secara langsung dengan bobot kriteria AHP yang bersangkutan (pangkat negatif untuk atribut biaya dan pangkat positif untuk atribut keuntungan). 

Karakteristik perkalian eksponensial pada metode WP menjamin terpenuhinya prinsip *Independence of Irrelevant Alternatives* (IIA), sehingga rasio perbandingan preferensi antaralternatif bersifat invarian dan kebal terhadap distorsi pembalikan peringkat [[5], [6]]. Integrasi hibrida AHP-WP ini dirancang secara matematis murni untuk menghasilkan kerangka keputusan pemilihan lokasi ritel perhiasan yang terkalibrasi secara konsistensi rasio, adil terhadap kompromi biaya-manfaat (*trade-off*), serta memiliki reliabilitas komputasi tinggi guna mendukung ekspansi strategis gerai ritel perhiasan emas.
