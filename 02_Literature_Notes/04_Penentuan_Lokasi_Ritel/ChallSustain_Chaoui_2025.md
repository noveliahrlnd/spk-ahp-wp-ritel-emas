# Chaoui et al. (2025) — Integrasi Geospasial dan MCDA untuk Penataan Ruang Kota

- **Sitasi IEEE:** G. Chaoui, R. Yaagoubi, and M. Mastere, “Integrating Geospatial Technologies and Multi-Criteria Decision Analysis for Sustainable and Resilient Urban Planning,” *Challenges in Sustainability*, vol. 13, no. 1, pp. 122–134, 2025, doi: 10.56578/cis130109.
- **PDF Lokal:** `../papers/ChallSustain_Chaoui_2025.pdf`
- **Tahun:** 2025
- **Topik Utama:** Kerangka konseptual berbasis data geospasial dan *Multi-Criteria Decision Analysis* (MCDA) untuk menyeimbangkan konflik tujuan antara efisiensi dan redundansi dalam perencanaan ruang perkotaan.

## Ringkasan Inti
- **Permasalahan & Tujuan:** Urbanisasi global yang diproyeksikan mencapai $68\%$ pada tahun 2050 (termasuk kebutuhan ekspansi lahan urban sebesar $7.000$ hektare/tahun di Maroko pada 2030) memicu konflik antara efisiensi pemanfaatan lahan (*sustainability*) dan redundansi ruang (*resilience*). Penelitian ini mengusulkan kerangka evaluasi terpadu berbasis geospasial dan MCDA agar perencana dapat menyeimbangkan kedua tujuan yang saling bertentangan sesuai konteks lokal.
- **Metode / Pendekatan:** Kerangka kerja menggabungkan dua pilar: (1) pemetaan indikator spasial dari citra satelit (menggunakan model *machine learning* Random Forest, SVM, dan Minimum Distance), data OpenStreetMap, serta data demografi; dan (2) kerangka pembobotan multikriteria (MCDA) adaptif untuk menyelaraskan dimensi efisiensi dan redundansi.
- **Temuan Kunci:**
  - Merumuskan 3 indikator efisiensi tata guna lahan: keragaman penggunaan lahan (*Entropy Index*), rasio konsumsi lahan terhadap pertumbuhan penduduk (*LCRPGR* SDG 11.3.1, dengan ambang efisien $0 \le \text{LCRPGR} \le 1$, tidak efisien $1 < \text{LCRPGR} < 2$, dan sangat tidak efisien $>2$), serta densifikasi urban (*urban infill*).
  - Merumuskan 3 indikator redundansi ruang: rasio lahan cadangan (*reserve areas*), ketersediaan dan aksesibilitas ruang publik terbuka (*Open Public Space* SDG 11.7.1 dalam radius berjalan kaki $400\text{ m}$), serta struktur polisentris (*Moran's I Index*).
  - Mengidentifikasi *trade-off* struktural antara efisiensi ruang dan fleksibilitas/redundansi spasial sehingga kebijakan kaku tidak memadai dan diperlukan sistem pembobotan MCDA yang adaptif terhadap karakteristik wilayah (implementasi empiris pada studi kasus diagendakan sebagai riset lanjutan).

## Relevansi untuk Paper SPK (AHP-WP Lokasi Toko Emas DIY)
- **Bagian yang Cocok Dikutip:** Pendahuluan; Hasil dan Pembahasan (Evaluasi *Trade-off* Kriteria).
- **Poin Argumen yang Didukung:** Memberikan landasan literatur internasional mutakhir (2025) bahwa keputusan spasial dan pemanfaatan ruang perkotaan selalu mengandung konflik objektif (*conflicting objectives* dan *trade-off*) antarindikator—seperti efisiensi biaya/kepadatan versus fleksibilitas ruang dan aksesibilitas—sehingga menuntut kerangka evaluasi MCDA berbobot yang kontekstual.
