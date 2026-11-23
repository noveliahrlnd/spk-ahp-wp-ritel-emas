# Starczewski (2025) — Galat Pembulatan pada Matriks Perbandingan Berpasangan AHP dengan Analisis Monte Carlo

- **Sitasi IEEE:** T. Starczewski, "Rounding errors in pairwise comparisons matrices by Monte Carlo analysis," *J. Appl. Math. Comput. Mech.*, vol. 24, no. 2, pp. 71–85, 2025, doi: 10.17512/jamcm.2025.2.06.
- **PDF Lokal:** `../papers/JAMCM_Starczewski_2025.pdf`
- **Tahun:** 2025
- **Topik Utama:** Kuantifikasi galat pembulatan (*rounding errors*) skala diskret Saaty 1–9 dan evaluasi keandalan empat indeks inkonsistensi AHP via Monte Carlo.

## Ringkasan Inti
- **Permasalahan & Tujuan:** Pembatasan nilai perbandingan berpasangan AHP ke skala diskret 1–9 dan kebalikannya menimbulkan galat pembulatan (*Rounding Error*/ROE) yang tidak terhindarkan meskipun pengambil keputusan menilai secara sempurna. Artikel ini mengukur besaran ROE pada matriks perbandingan berpasangan (PCM) dan vektor prioritas (PV), serta menguji apakah ambang batas konsistensi standar AHP (0,1 dari rata-rata matriks acak) secara keliru menolak PCM yang sebenarnya valid.
- **Metode / Pendekatan:** Simulasi Monte Carlo dijalankan sebanyak $N = 10.000$ iterasi untuk setiap ukuran matriks $n = 3, 4, \dots, 10$ dengan membangkitkan vektor prioritas sejati acak, membentuk matriks rasio ideal (MPR), membulatkannya ke skala Saaty 1–9, lalu menghitung bobot melalui metode *Geometric Mean* (GM). Galat absolut (AE), galat relatif (RE), serta distribusi empat indeks inkonsistensi—*Saaty's Index* (SI), *Koczkodaj's Index* (KI), *Average Triad Index* (ATI), dan *Salo-Hamalainen Index* (SHI)—dibandingkan terhadap ambang batas konsistensinya.
- **Temuan Kunci:**
  - Pembulatan ke skala Saaty menghasilkan rata-rata RE pada PCM selalu $> 10\%$ (dan $> 20\%$ untuk $n > 6$); khusus pada $n = 6$, rata-rata RE PCM mencapai `19,7%` (maks. `129%`), sedangkan pada vektor prioritas rata-rata RE sebesar `13,9%` dengan rata-rata AE `0,0147` (maks. `0,0832`).
  - Hanya *Saaty's Index* (SI) yang nilai rata-ratanya selalu jauh di bawah ambang batas konsistensi untuk seluruh $n$ (pada $n = 6$, rata-rata SI $= 0{,}025$ vs ambang batas $0{,}125$), meskipun nilai maksimumnya (`0,163`) terkadang tetap dapat melampaui ambang tersebut.
  - Pada KI, ATI, dan SHI, baik nilai rata-rata maupun maksimumnya melebihi ambang konsistensi (misalnya untuk $n = 6$: rata-rata KI $= 0{,}556$ vs ambang $0{,}099$; ATI $= 0{,}218$ vs $0{,}077$; SHI $= 0{,}126$ vs $0{,}076$), sehingga ambang tradisional berbasis matriks acak menyebabkan mayoritas PCM yang benar ikut ditolak.

## Relevansi untuk Paper SPK (AHP-WP Lokasi Toko Emas DIY)
- **Bagian yang Cocok Dikutip:** Metode (Desain Penelitian: uji konsistensi AHP) serta Hasil dan Pembahasan (Perhitungan AHP).
- **Poin Argumen yang Didukung:** Menjustifikasi penggunaan indeks konsistensi Saaty ($CI/CR \le 0{,}10$) untuk matriks kriteria $n = 6$ dibanding indeks alternatif yang terlalu ketat, sekaligus menjelaskan secara matematis bahwa nilai inkonsistensi kecil yang diperoleh ($CR = 0{,}0679$) merupakan konsekuensi wajar dari diskretisasi skala rasio 1–9 Saaty dan tetap berada dalam batas validitas tinggi.
