# Malik (2023) — SPK Pemilihan Lokasi Bisnis UMKM Berbasis AHP

- **Sitasi IEEE:** A. R. Malik, "Sistem Pendukung Keputusan Untuk Pemilihan Lokasi Bisnis Umkm Menggunakan Metode Analytic Hierarchy Process (AHP)," *Riau Jurnal Teknik Informatika (RJTI)*, vol. 2, no. 3, pp. 62–66, 2023, doi: 10.61876/rjti.v2i3.2901.
- **PDF Lokal:** `../papers/RJTI_Malik_2023.pdf`
- **Tahun:** 2023
- **Topik Utama:** Penerapan metode *Analytic Hierarchy Process* (AHP) dalam penentuan prioritas kriteria dan pemeringkatan lokasi bisnis UMKM di Kota Pekanbaru.

## Ringkasan Inti
- **Permasalahan & Tujuan:** Mengidentifikasi serta memprioritaskan kriteria pemilihan lokasi bisnis UMKM di Kota Pekanbaru, sekaligus merancang dan mengimplementasikan SPK berbasis web menggunakan metode AHP agar keputusan penentuan lokasi lebih objektif dan terstruktur.
- **Metode / Pendekatan:** Perancangan sistem menggunakan metode *waterfall* (*Context Diagram*, DFD level 0, ERD, dan *flowchart*) yang dipadukan dengan pemodelan AHP untuk mengevaluasi 5 kriteria (harga sewa, visibilitas, persaingan, jumlah penduduk, dan akses transportasi) pada 6 alternatif lokasi.
- **Temuan Kunci:**
  - Pengujian konsistensi matriks perbandingan berpasangan kriteria menghasilkan nilai *Consistency Ratio* $CR = 0{,}05 < 0{,}10$ sehingga bobot prioritas dinyatakan konsisten dan dapat diterima.
  - Pada tabel hasil perhitungan akhir (Tabel 4), kriteria berprioritas tertinggi adalah jumlah penduduk ($0{,}37668$) dan harga sewa ($0{,}33002$), diikuti akses transportasi ($0{,}16143$), visibilitas ($0{,}12880$), dan persaingan ($0{,}00308$).
  - Hasil pemeringkatan 6 alternatif menempatkan Jl. Air Dingin di peringkat 1 ($0{,}179185$), diikuti tiga lokasi bernilai seri yaitu Karya 1, Jl. Pahlawan Kerja, dan Pasir Putih (masing-masing $0{,}17135$), Taman Aerosport ($0{,}160912$), serta Marpoyan Damai ($0{,}145855$).

## Relevansi untuk Paper SPK (AHP-WP Lokasi Toko Emas DIY)
- **Bagian yang Cocok Dikutip:** Pendahuluan dan Metode (referensi kriteria lokasi & alasan hibridisasi AHP-WP).
- **Poin Argumen yang Didukung:** Mendukung relevansi kriteria biaya sewa dan visibilitas serta validitas AHP untuk pembobotan lokasi ritel/UMKM, sekaligus menunjukkan keterbatasan AHP tunggal yang rentan terhadap skor alternatif seri (*tie*) dan ketergantungan perbandingan berpasangan antaralternatif sehingga memotivasi integrasi AHP-WP pada penelitian ini.
