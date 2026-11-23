# Putra & Purnomo (2025) — SPK Kelayakan Kredit UMKM Berbasis AHP-WP

- **Sitasi IEEE:** A. F. S. Putra and A. S. Purnomo, “Sistem Pendukung Keputusan Penentuan Kelayakan Pemberian Kredit UMKM Menggunakan Metode AHP dan Weighted Product,” *Bulletin of Computer Science Research*, vol. 5, no. 5, pp. 1261–1271, Aug. 2025, doi: 10.47065/bulletincsr.v5i5.646.
- **PDF Lokal:** `../papers/BulletinCSR_Putra_Purnomo_2025.pdf`
- **Tahun:** 2025
- **Topik Utama:** Integrasi metode hibrida AHP untuk pembobotan kriteria dan Weighted Product (WP) untuk pemeringkatan alternatif pada studi kasus keuangan mikro UMKM.

## Ringkasan Inti
- **Permasalahan & Tujuan:** Evaluasi kelayakan kredit UMKM di Koperasi Simpan Pinjam (KSP) Makmur Jaya masih dilakukan secara manual dan subjektif sehingga rentan inkonsistensi dan risiko kredit bermasalah. Penelitian ini bertujuan merancang SPK berbasis kombinasi AHP dan WP untuk menghasilkan pemeringkatan calon debitur yang objektif, terukur, dan konsisten.
- **Metode / Pendekatan:** AHP diterapkan dengan skala perbandingan berpasangan 1–9 dan uji konsistensi ($RI = 1,12$ untuk 5 kriteria: Kelayakan Usaha, Riwayat Kredit, Potensi Pendapatan, Jaminan, dan Analisis Pasar) untuk memperoleh bobot prioritas. Bobot tersebut selanjutnya dimasukkan ke dalam metode WP melalui perhitungan Vektor $S_i$ dan normalisasi Vektor $V_i$ terhadap 5 alternatif (A1–A5) berskala 1–5.
- **Temuan Kunci:**
  - Pembobotan AHP menempatkan Analisis Pasar sebagai kriteria paling dominan ($0,50$), diikuti Jaminan ($0,30$), Potensi Pendapatan ($0,10$), Riwayat Kredit ($0,07$), dan Kelayakan Usaha ($0,03$), yang dinyatakan lolos konsistensi oleh penulis ($CR < 0,10$, dengan nilai terlapor $CI = -0,14$ dan $CR = -0,12$ dari $\lambda_{\max} = 4,43$).
  - Pemeringkatan WP menetapkan A5 (UMKM E) pada peringkat pertama ($S_5 = 4,3453$; $V_5 = 0,2270$), disusul A1 ($V_1 = 0,2158$), A2 ($V_2 = 0,2094$), A3 ($V_3 = 0,1894$), dan A4 terendah ($V_4 = 0,1584$).
  - Hasil pemeringkatan sistem menunjukkan kesesuaian $100\%$ terhadap perhitungan manual serta penilaian historis koperasi, sehingga mempercepat proses evaluasi dan meningkatkan akuntabilitas keputusan.

## Relevansi untuk Paper SPK (AHP-WP Lokasi Toko Emas DIY)
- **Bagian yang Cocok Dikutip:** Pendahuluan; Metode (Desain Penelitian).
- **Poin Argumen yang Didukung:** Memperkuat bukti empiris terkini (2025) bahwa arsitektur hibrida AHP-WP efektif menjembatani pembobotan hierarkis terstruktur dengan pemeringkatan perkalian proporsional yang transparan dan dapat diaudit pada keputusan bisnis multikriteria. Perlu dicatat bahwa studi ini hanya memakai kriteria bertipe *benefit* tanpa uji sensitivitas, sehingga mempertegas kebaruan analisis *cost-benefit* dan uji sensitivitas pada paper lokasi toko emas DIY.
