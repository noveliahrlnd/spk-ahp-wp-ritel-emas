# Susanti et al. (2023) — Metode WP dan Uji Sensitivitas Penentuan Lokasi Promosi

- **Sitasi IEEE:** E. Susanti, I. W. J. Pradnyana, Y. P. Oktavia, and R. Y. Ariyana, “Penerapan Metode Weighted Product (WP) Pada Penentuan Lokasi Promosi Calon Mahasiswa Baru,” *Techno.COM*, vol. 22, no. 4, pp. 949–959, Nov. 2023, doi: 10.33633/tc.v22i4.9050.
- **PDF Lokal:** `../papers/TechnoCom_Susanti_2023.pdf`
- **Tahun:** 2023
- **Topik Utama:** Penerapan metode Weighted Product (WP) dengan kriteria *benefit-cost*, uji sensitivitas bobot, dan perbandingan terhadap TOPSIS pada pemilihan lokasi di wilayah DIY dan sekitarnya.

## Ringkasan Inti
- **Permasalahan & Tujuan:** Pemilihan lokasi promosi penerimaan mahasiswa baru secara intuitif tidak lagi relevan di tengah persaingan ketat perguruan tinggi swasta. Penelitian ini bertujuan menerapkan metode WP beserta uji sensitivitas untuk menentukan prioritas lokasi promosi IST AKPRIND Yogyakarta sekaligus membandingkannya dengan hasil metode TOPSIS terdahulu.
- **Metode / Pendekatan:** Sebanyak 25 alternatif wilayah kabupaten/kota (R1–R25) dievaluasi berdasarkan 3 kriteria: jumlah pendaftar periode sebelumnya ($C_1$, *benefit*, bobot awal 5 → $W_1 = 0,417$), jumlah sekolah ($C_2$, *benefit*, bobot awal 4 → $W_2 = 0,333$), dan jumlah siswa SMA/K ($C_3$, *cost*, bobot awal 3 → $W_3 = -0,25$). Evaluasi dilengkapi uji sensitivitas dengan mengubah vektor bobot awal `[5, 4, 3]` menjadi `[4, 3, 5]`.
- **Temuan Kunci:**
  - Total nilai vektor $\sum S = 36,148$; lima wilayah prioritas teratas yang dilaporkan penulis mencakup Kota Yogyakarta (R1, $V_1 = 0,061$), Kab. Bantul (R2, $V_2 = 0,065$), Kab. Sleman (R3, $V_3 = 0,060$), Kab. Blora (R4, $V_4 = 0,053$), dan Kab. Cilacap (R6, $V_6 = 0,050$), dengan dominasi wilayah DIY dan Jawa Tengah.
  - Uji sensitivitas bobot `[4, 3, 5]` menggeser urutan 5 besar menjadi Kab. Bantul ($V = 0,055$), Kab. Sleman ($V = 0,052$), Kota Yogyakarta ($V = 0,050$), Kab. Blora ($V = 0,050$), dan Kab. Purworejo ($V = 0,045$), membuktikan kepekaan pemeringkatan WP terhadap perubahan preferensi bobot.
  - Dibandingkan metode TOPSIS pada data yang sama, WP menghasilkan himpunan 5 lokasi terbaik yang sama meski berbeda urutan, dengan keunggulan komputasi lebih sederhana serta akomodasi langsung pangkat *benefit* ($+1$) dan *cost* ($-1$).

## Relevansi untuk Paper SPK (AHP-WP Lokasi Toko Emas DIY)
- **Bagian yang Cocok Dikutip:** Pendahuluan; Metode (Perhitungan WP); Hasil dan Pembahasan (Evaluasi / Uji Sensitivitas).
- **Poin Argumen yang Didukung:** Mendukung argumentasi bahwa penentuan lokasi berbasis intuisi tidak memadai dan bahwa WP unggul dalam memproses kombinasi atribut *benefit* dan *cost* secara ringkas di konteks spasial DIY. Selain itu, studi ini menegaskan urgensi uji sensitivitas bobot untuk menguji fleksibilitas hasil pemeringkatan WP, sekaligus menyoroti perlunya pembobotan formal seperti AHP agar bobot awal tidak ditetapkan secara arbitrer.
