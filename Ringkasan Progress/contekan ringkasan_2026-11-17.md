# 🗣️ CONTEKAN BICARA — 17 November 2026
**Hanya untuk presenter. Baca sebelum maju.**

---

## PENDAHULUAN

### 📌 Paragraf 1 — Latar Belakang Finansial

> *"Bapak/Ibu dan teman-teman, penelitian kami berangkat dari fenomena tahun 2025. Saat ekonomi global bergejolak, harga emas justru menembus rekor tertinggi karena statusnya sebagai safe haven. Menariknya, minat beli masyarakat tidak turun, melainkan bergeser ke instrumen adaptif: 41,7% memilih cicil emas dan 25% memilih tabungan fisik. Tingginya transaksi ini mendorong pelaku usaha memperluas gerai fisik. Mengapa harus toko fisik di era digital? Karena bisnis perhiasan emas punya tiga hal yang wajib hadir langsung: pembeli butuh cek kadar di tempat, butuh penyimpanan brankas berkualifikasi khusus, dan butuh jaminan uang cair saat itu juga."*

---

### 📌 Paragraf 2 — Konteks DIY & MCDM

> *"Kebutuhan ekspansi gerai fisik itu nyata dirasakan di Yogyakarta. DIY karakternya sangat unik dan kompleks. Kalau buka di Malioboro, pengunjungnya luar biasa banyak, tapi harga sewanya sangat mahal. Kalau di Jalan Magelang atau Sinduadi, visibilitas jalan utamanya bagus dengan harga sewa yang lebih masuk akal. Di Babarsari atau Taman Siswa, pasarnya padat mahasiswa yang profil daya beli emasnya berbeda. Karena toko emas inventarinya miliaran rupiah, salah pilih lokasi bisa langsung membuat bisnis rugi besar. Masalah ini tidak bisa diputuskan pakai tebak-tebakan — ini adalah masalah MCDM spasial yang harus menyeimbangkan beban biaya sewa gedung melawan lima faktor keuntungan: keamanan, daya beli, keterlihatan toko dari jalan, izin perombakan lantai untuk brankas tonase berat, dan kepadatan sentra emas."*

---

### 📌 Paragraf 3 — AHP & Cacat Rank Reversal

> *"Untuk menyelesaikan masalah multikriteria tadi, metode yang paling umum di literatur adalah Analytic Hierarchy Process atau AHP. AHP sangat bagus karena mampu menguji apakah logika pengambil keputusan konsisten atau tidak lewat angka Consistency Ratio di bawah 0,10. Namun, kami menemukan kelemahan mendasar: jika AHP dipakai sampai tahap menentukan peringkat akhir lokasi, ada cacat bawaan bernama rank reversal. Artinya begini: misalnya Toko A awalnya juara 1 dan Toko B juara 2. Ketika investor memasukkan satu kandidat toko baru, posisi Toko A dan B bisa mendadak terbalik tanpa alasan logis. Bagi investor dengan modal besar, ketidakstabilan peringkat ini tentu sangat berbahaya."*

---

### 📌 Paragraf 4 — Akar Matematis & Isolasi AHP

> *"Secara matematis, kenapa AHP bisa oleng seperti itu? Karena rumus normalisasi AHP membagi nilai sel dengan total penjumlahan kolom. Akibatnya, skor satu toko menjadi tergantung pada ada-tidaknya toko lain. Ini melanggar aksioma independensi yang dirumuskan Kenneth Arrow, dikenal sebagai IIA. Oleh karena itu, posisi metodologis penelitian kami sangat jelas dan tegas: instrumen AHP kami isolasi dan kami hentikan fungsinya HANYA sampai tahap pembobotan kriteria dan validasi konsistensi. Kami tidak memakai AHP untuk meranking alternatif lokasi."*

---

### 📌 Paragraf 5 — WP sebagai Solusi & Tujuan Riset

> *"Sebagai gantinya, pemeringkatan akhir diserahkan kepada metode Weighted Product atau WP. Mengapa WP? Karena WP menghitung skor preferensi lewat perkalian eksponensial. Secara aljabar, rasio perbandingan antara Toko A dan Toko B — Sa dibagi Sb — hanya dipengaruhi oleh nilai Toko A dan Toko B sendiri. Ada atau tidaknya toko ketiga tidak akan mengubah perbandingan keduanya. Dengan sifat invarian ini, aksioma IIA terpenuhi dan sistem kebal mutlak dari rank reversal. Maka, tujuan penelitian kami adalah membangun dan menguji model integrasi hibrida AHP-WP untuk penentuan lokasi ritel perhiasan emas di DIY yang teruji konsisten, adil terhadap kompromi biaya-manfaat, dan stabil secara matematis."*

---

## LANDASAN TEORI — PERSAMAAN MATEMATIKA

### 📌 Blok 1 — Matriks Keputusan (MCDM)

> *"Model kami dimulai dari merepresentasikan seluruh data kandidat lokasi ke dalam satu matriks keputusan X. Baris-barisnya adalah kandidat lokasi, kolom-kolomnya adalah kriteria penilaian. Elemen x-ij itu nilai kinerja lokasi ke-i pada kriteria ke-j. Di penelitian kami, matriks ini berukuran m kali n — m alternatif, n kriteria."*

---

### 📌 Blok 2 — AHP: Bobot Kriteria (Persamaan 1)

> *"Fase pertama adalah AHP. Pengambil keputusan mengisi matriks perbandingan berpasangan — skala Saaty 1 sampai 9. Angka 1 artinya sama penting, angka 9 artinya satu kriteria jauh lebih dominan. Setelah matriks terisi, bobot setiap kriteria dihitung menggunakan Persamaan 1: normalisasi kolom lalu rata-rata baris. Kriteria yang paling sering dinilai lebih penting akan dapat bobot tertinggi."*

---

### 📌 Blok 3 — AHP: Uji Konsistensi (Persamaan 2)

> *"Tapi bobot saja tidak cukup. Kita harus pastikan logika penilainya konsisten. Untuk itu dihitung Consistency Index pakai Persamaan 2a, lalu dibagi Random Index Saaty sesuai ukuran matriks menggunakan Persamaan 2b untuk dapat Consistency Ratio. Kalau CR di bawah 0,10, penilaian dinyatakan konsisten dan kita boleh lanjut. Kalau tidak, penilai diminta mengisi ulang matriks perbandingannya."*

---

### 📌 Blok 4 — WP: Vektor S (Persamaan 3)

> *"Fase kedua adalah WP. Bobot dari AHP tadi dipakai sebagai pangkat eksponen — positif untuk kriteria benefit, negatif untuk kriteria cost. Lalu skor setiap lokasi dihitung dengan mengalikan semua nilai kinerjanya yang sudah dipangkatkan bobotnya masing-masing. Hasilnya disebut Vektor S. Ini yang membuat WP kebal rank reversal — karena perkalian, rasio antara dua lokasi murni hanya bergantung pada nilai kedua lokasi itu, bukan pada alternatif lain."*

---

### 📌 Blok 5 — WP: Peringkat Akhir via Vektor V (Persamaan 4)

> *"Langkah terakhir, Vektor S masing-masing lokasi dibagi total semua S untuk mendapat Vektor V. Ini normalisasi supaya nilainya jadi persentase yang mudah dibandingkan. Lokasi dengan V tertinggi adalah rekomendasi utama. Total semua V harus sama dengan 1 atau 100%."*

---

## LANDASAN TEORI — PENULISAN TABEL & TEMUAN NUMERIK

### 📌 Blok 6 — Alur 4 Tabel Manuskrip

> *"Bapak/Ibu, seluruh data dan komputasi kami rangkum ke dalam empat tabel terstruktur. Tabel 1 adalah matriks perbandingan berpasangan AHP ordo 6 kali 6. Dari Tabel 1, kita hitung bobot kriteria dan uji konsistensi di Tabel 2. Hasilnya: kriteria potensi daya beli lingkungan menempati bobot tertinggi 46,14%, disusul visibilitas lokasi 22,58%, dan biaya sewa 13,33%. Nilai CR tercatat 0,0677, artinya penilaian logis dan konsisten karena di bawah 0,10. Lalu di Tabel 3, kita sajikan matriks keputusan 5 kali 6 berisi data riil lima kandidat lokasi di DIY. Terakhir, Tabel 4 merangkum skor akhir Vektor S dan Vektor V hasil pemeringkatan Weighted Product."*

---

### 📌 Blok 7 — Insight Pemenang: Mengapa Sinduadi Juara 1 Mengalahkan Malioboro?

> *"Hal paling menarik dari temuan kami ada pada pertarungan antara Sinduadi di peringkat 1 (23,02%) dan Malioboro Mall di peringkat 2 (22,43%). Malioboro memang juara di daya beli dan keamanan — dua-duanya dapat skor sempurna 5. Namun, harga sewa Malioboro mencapai 346 juta rupiah per tahun, alias 2,6 kali lipat lebih mahal dari Sinduadi. Karena biaya sewa adalah atribut cost, angka sewa yang mahal memicu penalti eksponensial negatif yang sangat berat pada rumus WP. Sebaliknya, Sinduadi menawarkan efisiensi sewa yang moderat (130 juta), visibilitas jalan utama yang sangat tinggi (skor 5), dan keleluasaan merombak lantai untuk brankas tonase berat. Kompromi biaya-manfaat inilah yang membuat Sinduadi keluar sebagai rekomendasi lokasi paling strategis."*

---

## LANDASAN TEORI — PENGGUNAAN GAMBAR (VISUALISASI)

### 📌 Blok 8 — Peran 3 Gambar Manuskrip

> *"Untuk memudahkan pemahaman reviewer dan pembaca, kami menyajikan tiga gambar visual. Gambar 1 adalah diagram struktur hierarki keputusan tiga level: sasaran di Level 1, enam kriteria di Level 2, dan lima kandidat lokasi di Level 3. Gambar 2 adalah diagram alir algoritma hibrida kami — di sini terlihat jelas adanya titik potong metodologis, di mana AHP dihentikan setelah uji CR lolos di angka 0,0677, lalu estafet pemeringkatan diserahkan ke perkalian eksponensial WP. Terakhir, Gambar 3 menyajikan grafik distribusi Vektor V yang memperlihatkan secara visual betapa ketatnya kompetisi antara Sinduadi 23,02% dan Malioboro 22,43% dengan selisih tipis hanya 0,59%."*

---

## METODOLOGI PENELITIAN

### 📌 Blok 9 — Enam Tahapan Operasional Riset

> *"Bapak/Ibu, Bab Metodologi Penelitian kami jalankan melalui enam tahapan kerja yang terstruktur dan terukur. Dimulai dari Tahap 1, identifikasi masalah spasial industri emas dan dekomposisi kriteria hierarki. Tahap 2, seleksi tapak dan akuisisi data empiris di lima kawasan DIY melalui survei lapangan dan wawancara pemilik gedung. Tahap 3, pembobotan kriteria AHP skala 1 sampai 9. Tahap 4, gerbang uji konsistensi Saaty — begitu CR terbukti 0,0677 di bawah 0,10, kami langsung berlakukan 'titik potong metodologis' untuk menghentikan AHP. Tahap 5, pembobotan dialihkan menjadi eksponen WP guna menghitung preferensi absolut Vektor S dan preferensi relatif Vektor V. Terakhir, Tahap 6, analisis sensitivitas dan penetapan rekomendasi lokasi terbaik."*

---

### 📌 Blok 10 — Karakteristik 5 Lokasi & Data Kriteria

> *"Dalam menentukan alternatif tapak di DIY, kami tidak asal pilih, melainkan mengambil lima sampel yang mewakili heterogenitas zonasi tata ruang perkotaan. Ada kawasan hunian atas di Sinduadi, arteri komersial regional di Jalan Magelang, kawasan kampus di Babarsari, posisi sudut hook di Taman Siswa, dan pusat perbelanjaan pariwisata di Malioboro Mall. Terhadap kelima lokasi ini, kami evaluasi satu kriteria biaya berupa tarif sewa riil per tahun, serta lima kriteria keuntungan: keamanan, daya beli, visibilitas, fleksibilitas renovasi brankas, dan aglomerasi sentra emas. Data kuantitatif biaya sewa dan data kualitatif skala 1 sampai 5 bisa langsung diproses oleh perkalian eksponensial WP tanpa perlu penyeragaman skala di awal."*

---

### 📌 Blok 11 — Prosedur 9 Langkah Algoritma Hibrida

> *"Alur komputasi hibrida kami rincikan secara matematis ke dalam sembilan langkah berurutan. Langkah 1 sampai 3 menyusun matriks pairwise, normalisasi kolom, dan sintesis vektor bobot wj. Langkah 4 menguji CR Saaty. Langkah 5 adalah kunci arsitektur riset kami: titik potong metodologis. Di sini AHP distop permanen agar tidak meranking alternatif. Langkah 6, tanda bobot disesuaikan: pangkat negatif untuk biaya sewa, pangkat positif untuk lima kriteria keuntungan. Langkah 7, matriks keputusan empiris disusun. Langkah 8, Vektor S dihitung via perkalian eksponensial mandiri. Terakhir, Langkah 9, Vektor V dihitung dengan membagi skor S tiap lokasi terhadap total seluruh lokasi untuk mendapatkan persentase preferensi final."*

---

### 📌 Blok 12 — Validasi Konsistensi & Pembuktian IIA

> *"Untuk menjamin keabsahan ilmiah, metodologi kami memiliki dua lapis validasi. Lapis pertama adalah validasi konsistensi logika pembobotan Saaty, di mana matriks kami lolos dengan CR 0,0677. Lapis kedua adalah pembuktian aksiomatis kekebalan rank reversal. Pada metode penjumlahan seperti SAW atau AHP, skor satu alternatif terikat pada alternatif lain sehingga peringkat bisa jungkir balik saat opsi ditambah. Sedangkan pada Weighted Product, rasio perbandingan Sa dibagi Sb murni merupakan perkalian rasio kinerja kedua alternatif tersebut. Kami membuktikan bahwa rasio ini invarian terhadap kandidat baru, sehingga aksioma Independence of Irrelevant Alternatives terpenuhi secara mutlak."*

---

## HASIL DAN PEMBAHASAN

### 📌 Blok 13 — Analisis & Perancangan (Bobot Kriteria & CR)

> *"Bapak/Ibu, masuk ke Bab Hasil dan Pembahasan, pada Subbab D.1 kami memaparkan hasil analisis kebutuhan dan sintesis bobot kriteria AHP. Hasilnya membuktikan bahwa kriteria potensi daya beli lingkungan menempati urutan pertama yang paling dominan dengan bobot 46,14%, disusul oleh visibilitas lokasi sebesar 22,58%, dan biaya beban properti sebesar 13,33%. Evaluasi konsistensi Saaty menghasilkan nilai eigen maksimum 6,420 dan rasio konsistensi CR 0,0677 di bawah 0,10. Begitu bobot ini terbukti konsisten secara matematis, titik potong metodologis langsung diaktifkan untuk menghentikan operasional AHP dan menyerahkan proses pemeringkatan kepada Weighted Product."*

---

### 📌 Blok 14 — Implementasi & Temuan Pemenang (Sinduadi vs Malioboro)

> *"Pada Subbab D.2, implementasi algoritma Weighted Product menghasilkan Vektor S absolut dan Vektor V relatif. Peringkat 1 dimenangkan oleh kandidat Sinduadi dengan skor preferensi 23,02%, mengungguli Malioboro Mall di peringkat 2 dengan skor 22,43% dengan margin tipis 0,59%. Temuan ini menjawab tuntas rumusan masalah di pendahuluan: mengapa Malioboro kalah padahal skor daya beli dan keamanannya sempurna bernilai 5? Jawabannya ada pada penalti eksponensial biaya sewa tahunan Malioboro sebesar Rp346,32 juta yang 2,66 kali lipat lebih mahal dari Sinduadi, ditambah restriksi pengelola mal yang membatasi renovasi lantai fondasi untuk brankas baja berat. Sinduadi keluar sebagai pemenang karena menyajikan trade-off paling rasional: sewa efisien Rp130 juta, visibilitas fasad 12 meter sempurna, dan kebebasan penuh merombak brankas berat. Sementara itu, Babarsari berada di juru kunci dengan 13,60% karena segmen mahasiswa tidak cocok untuk komoditas logam mulia bernilai tinggi."*

---

### 📌 Blok 15 — Stabilitas Peringkat, Uji Aksioma IIA & Daftar Pustaka IEEE

> *"Terakhir, kami menguji stabilitas keputusan. Rasio perbandingan preferensi antara Sinduadi dan Malioboro tercatat sebesar 1,0262. Kami buktikan bahwa rasio ini tetap bernilai 1,0262 meskipun ada penambahan kandidat baru atau penghapusan alternatif lain, membuktikan terpenuhinya aksioma IIA dan kekebalan 100% dari anomali rank reversal. Seluruh analisis dalam naskah kami juga didukung oleh 12 rujukan ilmiah standar IEEE, dengan 100% terbitan 10 tahun terakhir (2020 sampai 2026), 91,7% berupa artikel jurnal bereputasi, dan tanpa rujukan halaman web bebas."*

---

## 🛡️ ANTISIPASI PERTANYAAN DOSEN

### ❓ "Kenapa studi kasusnya toko emas? Kenapa bukan kafe atau ritel pakaian?"
> *"Karena ritel perhiasan emas punya sifat high value-to-volume density dan beban kapital inventori yang sangat masif, Pak/Bu. Kalau salah pilih lokasi, risikonya bukan sekadar sepi pengunjung, melainkan risiko keamanan perampokan dan biaya sewa yang tidak menutup perputaran modal barang mewah. Toko emas juga butuh spesifikasi fisik khusus seperti izin membongkar lantai untuk brankas tonase berat — sesuatu yang tidak dimiliki ritel biasa. Karakteristik ekstrem inilah yang membuat trade-off multikriterianya sangat tajam untuk diuji dalam SPK."*

---

### ❓ "Kenapa sangat yakin AHP murni tidak boleh dipakai sampai meranking?"
> *"Secara teoretis, normalisasi AHP membagi setiap nilai sel dengan total kolom. Ini menciptakan interdependensi semu: skor alternatif A menjadi sangat tergantung pada ada-tidaknya alternatif B, C, atau D. Kalau pemilik gerai nantinya ingin menambah kandidat baru, peringkat lokasi yang lama bisa bertukar posisi secara acak — itulah rank reversal. Ini melanggar aksioma Independence of Irrelevant Alternatives dari Kenneth Arrow. Kami ingin sistem pendukung keputusan yang stabil, bukan yang hasilnya berubah-ubah saat opsi ditambah."*

---

### ❓ "Mengapa pilih WP? Kenapa bukan SAW atau TOPSIS?"
> *"SAW masih mengandalkan penjumlahan linier berbobot sehingga memiliki kelemahan kompensatori yang mirip AHP. Sedangkan WP memakai agregasi perkalian eksponensial. Ketika kita bandingkan rasio dua alternatif Sa dibagi Sb, suku dari alternatif lain saling meniadakan — hasilnya murni invarian dan kebal 100% terhadap rank reversal. Di sisi lain, WP tidak punya fitur pembobotan berpasangan dan uji konsistensi logika, sehingga kombinasi AHP untuk mencari bobot dan WP untuk meranking saling melengkapi sempurna."*

---

### ❓ "Apa bedanya CR dan CI?"
> *"CI itu ukuran mentah seberapa jauh penilaian kita menyimpang dari konsistensi sempurna — dihitung dari nilai eigen terbesar dikurangi ukuran matriks, dibagi n minus 1. Tapi CI ini tidak punya referensi perbandingan, jadi kita bagi dengan RI — Random Index Saaty — yang nilainya bergantung pada ukuran matriks. Hasilnya CR. CR yang di bawah 0,10 artinya penyimpangan konsistensi kita masih dalam batas wajar dan dapat diterima."*

---

### ❓ "Kenapa data sewa jutaan rupiah tidak dinormalisasi linier dulu sebelum masuk rumus WP?"
> *"Karena sifat pemangkatan eksponensial pada algoritma Weighted Product secara alami membatalkan disparitas skala pengukuran, Pak/Bu. Saat kita menghitung Vektor V, pembagian Si terhadap jumlah total Sk mengekstraksi kontribusi relatif setiap parameter tanpa mempermasalahkan satuan aslinya. Normalisasi linier tambahan di awal justru akan mendistorsi disparitas rasio riil yang sebenarnya sudah dimiliki data biaya."*

---

### ❓ "Kenapa Malioboro yang skornya tinggi di daya beli dan keamanan justru kalah dari Sinduadi?"
> *"Karena metode Weighted Product memperhitungkan penalti biaya (cost) secara eksponensial negatif, Pak/Bu. Sewa tahunan di Malioboro mencapai Rp346,32 juta, sedangkan di Sinduadi hanya Rp130 juta. Selisih biaya sebesar 2,6 kali lipat ini mendegradasi nilai Vektor S Malioboro secara signifikan. Selain itu, toko di dalam mal memiliki keterbatasan izin fisik untuk renovasi lantai brankas baja tonase berat (skor 2), sementara Sinduadi memiliki izin dan struktur independen yang leluasa (skor 5). Jadi secara trade-off keseluruhan, Sinduadi jauh lebih menguntungkan dan realistis bagi investor."*

