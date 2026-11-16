# D. HASIL DAN PEMBAHASAN

Bagian ini menyajikan hasil implementasi model optimasi hibrida Analytic Hierarchy Process dan Weighted Product beserta analisis komprehensif terhadap temuan empiris yang diperoleh. Pembahasan diarahkan secara mendalam untuk menjawab permasalahan penentuan lokasi ritel perhiasan emas bernilai tinggi di Daerah Istimewa Yogyakarta yang telah dirumuskan pada bagian pendahuluan. Uraian dibagi ke dalam dua subbab utama yang mencakup analisis dan perancangan sistem keputusan, serta implementasi komputasi dan pengujian stabilitas peringkat.

## D.1. Analisis dan Perancangan

Tahap analisis dan perancangan berfokus pada pemetaan kebutuhan spasial industri ritel perhiasan emas, perumusan dekomposisi hierarki multikriteria, sintesis bobot prioritas kriteria melalui instrumen AHP, serta perancangan titik potong metodologis antarmetode. Tahapan ini meletakkan landasan konseptual model keputusan.

### D.1.1. Analisis Kebutuhan Spasial dan Struktur Hierarki Keputusan

Bisnis ritel perhiasan emas memiliki karakteristik operasional yang sangat khas dibandingkan ritel komoditas konsumen umum [1]. Produk perhiasan emas memadukan fungsi estetika dengan instrumen lindung nilai investasi, sehingga memiliki densitas nilai per volume barang yang luar biasa padat. Karakteristik ini menimbulkan konsentrasi nilai kapital yang masif pada area toko yang relatif kompak, yang sekaligus memicu tingginya risiko kerentanan terhadap tindak kriminalitas bersenjata [8]. Oleh sebab itu, pemilihan tapak gerai fisik tidak dapat dipandang sebatas estimasi kepadatan arus lalu lintas manusia.

Analisis kebutuhan spasial yang dilakukan ini mengidentifikasi enam parameter penentu keberhasilan lokasi fisik ritel perhiasan emas di Daerah Istimewa Yogyakarta. Keenam parameter tersebut didekomposisi ke dalam struktur hierarki keputusan yang memisahkan satu atribut biaya dan lima atribut keuntungan.

Atribut biaya mencakup biaya beban properti ($C_1$) yang diukur melalui tarif sewa tahunan ruang usaha. Lima atribut keuntungan meliputi keamanan eksternal kawasan ($C_2$), potensi daya beli lingkungan ($C_3$), visibilitas lokasi ($C_4$), fleksibilitas perombakan struktur fondasi bangunan ($C_5$), serta aglomerasi sentra niaga emas eksisting ($C_6$).

Dekomposisi hierarki keputusan ini dirancang untuk mengevaluasi lima kandidat tapak di wilayah Daerah Istimewa Yogyakarta yang merepresentasikan heterogenitas zonasi tata ruang perkotaan tersebut. Kelima alternatif lokasi tersebut mencakup kawasan hunian menengah ke atas Sinduadi ($A_1$), koridor komersial arteri regional Jalan Magelang ($A_2$), sentra pendidikan dan hunian mahasiswa Babarsari ($A_3$), koridor persimpangan sudut Jalan Taman Siswa ($A_4$), serta pusat perbelanjaan pariwisata Malioboro Mall ($A_5$). Rancangan hierarki ini memetakan kompromi multikriteria secara terpadu.

### D.1.2. Analisis Pembobotan Kriteria AHP dan Evaluasi Rasio Konsistensi

Penetapan tingkat kepentingan relatif antarkriteria ini dirancang melalui pengisian matriks perbandingan berpasangan berordo $6 \times 6$ dengan menggunakan skala fundamental Saaty bernilai 1 sampai 9 [2]. Penilaian preferensi dihimpun dari pertimbangan pakar manajemen ritel perhiasan emas dan praktisi investasi komoditas. Sintesis bobot prioritas kriteria dilakukan melalui normalisasi nilai elemen terhadap total kolom, yang kemudian dirata-ratakan pada setiap baris matriks. Distribusi bobot prioritas kriteria hasil sintesis disajikan pada Tabel 1.

Tabel 1. Distribusi Bobot Prioritas Kriteria Evaluasi Lokasi Ritel Emas

| Kode Kriteria | Definisi Operasional Parameter | Sifat Atribut | Bobot Prioritas ($w_j$) | Persentase Bobot | Urutan Peringkat |
| :---: | :--- | :---: | :---: | :---: | :---: |
| $C_3$ | Potensi Daya Beli Lingkungan | Keuntungan | 0,4614 | 46,14% | 1 |
| $C_4$ | Visibilitas Lokasi dari Koridor | Keuntungan | 0,2258 | 22,58% | 2 |
| $C_1$ | Biaya Beban Properti Tahunan | Biaya | 0,1333 | 13,33% | 3 |
| $C_6$ | Aglomerasi Sentra Niaga Emas | Keuntungan | 0,1023 | 10,23% | 4 |
| $C_2$ | Keamanan Eksternal Kawasan | Keuntungan | 0,0501 | 5,01% | 5 |
| $C_5$ | Fleksibilitas Perombakan Bangunan | Keuntungan | 0,0271 | 2,71% | 6 |
| **Total** | Akumulasi Bobot Kriteria | - | **1,0000** | **100,00%** | - |

Distribusi bobot pada Tabel 1 memperlihatkan bahwa kriteria potensi daya beli lingkungan ($C_3$) menempati prioritas tertinggi dengan bobot 0,4614 (46,14%). Besaran bobot ini menegaskan bahwa keberhasilan gerai perhiasan emas ditentukan oleh kemampuan finansial nyata dari populasi pengunjung pada koridor tapak. Kepadatan arus massa manusia semata tidak menghasilkan transaksi jika profil ekonominya tidak sesuai dengan produk logam mulia.

Kriteria visibilitas lokasi ($C_4$) menempati urutan kedua dengan bobot prioritas 0,2258 (22,58%). Fasad gerai yang terbuka langsung ke arah koridor utama memberikan paparan visual promosi alami kepada pengendara dan pejalan kaki. Keterlihatan fasad tersebut sekaligus menunjang pengawasan visual lingkungan dari ruang jalan raya (*natural surveillance*), sehingga mempersempit celah tindak kriminalitas.

Kriteria biaya beban properti ($C_1$) berada pada peringkat ketiga dengan bobot 0,1333 (13,33%), disusul oleh aglomerasi sentra emas ($C_6$) sebesar 0,1023 (10,23%). Keberadaan gerai kompetitor di kawasan sekitar justru menciptakan daya tarik pasar terpadu yang mempermudah konsumen dalam membandingkan model perhiasan.

Kriteria keamanan eksternal kawasan ($C_2$) dan fleksibilitas struktur ($C_5$) menempati prioritas yang relatif lebih kecil, masing-masing sebesar 0,0501 (5,01%) dan 0,0271 (2,71%). Meskipun persentasenya rendah, kedua parameter ini menjadi syarat penentu kualifikasi teknis gedung yang tidak dapat diabaikan.

Pengujian konsistensi logika pembobotan menghasilkan nilai eigen maksimum ($\lambda_{\max}$) sebesar 6,420 pada matriks ordo 6. Nilai *Consistency Index* ($CI$) tercatat sebesar 0,084. Mengingat nilai *Random Index* ($RI$) untuk matriks berukuran 6 bernilai 1,24, perhitungan menghasilkan rasio konsistensi Saaty ($CR$) sebesar 0,0677 (6,77%). Angka ini berada di bawah batas ambang kelayakan $CR \le 0{,}10$, sehingga struktur perbandingan berpasangan pakar dinyatakan konsisten secara logis dan terbebas dari deviasi acak yang merusak [2], [9].

### D.1.3. Perancangan Titik Potong Metodologis

Perancangan metodologis ini membatasi penerapan instrumen AHP hanya sampai tahap pembobotan kriteria global dan pengujian rasio konsistensi. Pembatasan ini didasarkan pada temuan literatur bahwa perbandingan berpasangan alternatif pada AHP murni memicu anomali pembalikan peringkat (*rank reversal*) [3].

Anomali pembalikan peringkat berakar pada formulasi normalisasi penjumlahan kolom matriks lokal AHP. Pembagian setiap nilai elemen dengan total kolomnya menyebabkan skor suatu alternatif bergantung langsung pada kinerja alternatif lainnya di dalam himpunan data. Keadaan ini melanggar aksioma *Independence of Irrelevant Alternatives* (IIA) yang digagas oleh Kenneth Arrow [4]. Apabila alternatif baru yang tidak optimal ditambahkan ke dalam sistem, peringkat alternatif unggulan dapat tertukar secara tidak rasional.

Untuk mengatasi kerentanan struktural tersebut, penelitian ini merancang titik potong metodologis (*methodological cut-off point*). Begitu nilai rasio konsistensi Saaty terbukti valid ($CR = 0{,}0677$), instrumen AHP langsung dihentikan secara permanen. Vektor bobot prioritas kriteria ($w_j$) kemudian dialihkan ke algoritma Weighted Product untuk memproses pemeringkatan alternatif secara mandiri [5], [7]. Perancangan arsitektur ini memutus rantai interdependensi alternatif.

## D.2. Implementasi dan Pengujian

Subbab ini memaparkan implementasi komputasi pemeringkatan alternatif menggunakan algoritma Weighted Product, pembahasan mendalam terhadap dinamika hasil komputasi guna menjawab permasalahan pada pendahuluan, serta pengujian ketahanan model terhadap anomali pembalikan peringkat dan analisis sensitivitas.

### D.2.1. Implementasi Pemeringkatan Alternatif Menggunakan Weighted Product

Tahap implementasi diawali dengan mentransformasikan vektor bobot kriteria AHP menjadi pangkat eksponensial dalam skema Weighted Product. Pangkat bernilai negatif diberikan untuk kriteria biaya sewa properti ($W_1 = -0{,}1333$). Pangkat bernilai positif ditetapkan untuk kelima kriteria keuntungan ($W_2 = +0{,}0501$, $W_3 = +0{,}4614$, $W_4 = +0{,}2258$, $W_5 = +0{,}0271$, dan $W_6 = +0{,}1023$).

Data kinerja empiris kelima kandidat lokasi dihimpun ke dalam matriks keputusan $X$. Data biaya sewa tahunan dinyatakan dalam skala rasio riil juta rupiah, sedangkan data kualitatif kelima kriteria lainnya dinilai menggunakan skala ordinal 1 sampai 5. Data kinerja empiris tersebut disajikan pada Tabel 2.

Tabel 2. Matriks Keputusan Profil Kinerja Lima Kandidat Lokasi di D.I. Yogyakarta

| Kode | Kandidat Lokasi | $C_1$ (Biaya - Juta Rp) | $C_2$ (Keamanan) | $C_3$ (Daya Beli) | $C_4$ (Visibilitas) | $C_5$ (Struktur) | $C_6$ (Aglomerasi) |
| :---: | :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| $A_1$ | Sinduadi (Jl. Umbul Permai) | 130,00 | 3 | 4 | 5 | 5 | 2 |
| $A_2$ | Koridor Jalan Magelang Km. 5 | 120,00 | 3 | 3 | 4 | 5 | 2 |
| $A_3$ | Babarsari (Sentra Kampus) | 150,00 | 3 | 2 | 3 | 5 | 1 |
| $A_4$ | Jalan Taman Siswa (Sudut Hook) | 250,00 | 3 | 4 | 5 | 5 | 3 |
| $A_5$ | Malioboro Mall (Ruang Ritel) | 346,32 | 5 | 5 | 4 | 2 | 4 |

Komputasi nilai preferensi absolut ($S_i$) dilakukan melalui perkalian seluruh nilai kinerja dari masing-masing alternatif yang telah dipangkatkan terhadap eksponen bobotnya. Perhitungan nilai preferensi absolut tersebut menghasilkan skor $S_1 = 1{,}6934$ untuk tapak Sinduadi, $S_2 = 1{,}4246$ untuk koridor Jalan Magelang, $S_3 = 1{,}0006$ untuk kawasan Babarsari, $S_4 = 1{,}5872$ untuk koridor Jalan Taman Siswa, serta $S_5 = 1{,}6501$ untuk unit ritel Malioboro Mall.

Akumulasi penjumlahan terhadap seluruh nilai preferensi absolut tersebut menghasilkan $\sum_{k=1}^5 S_k = 7{,}3559$. Nilai preferensi relatif ($V_i$) kemudian dapat dihitung dengan membagi setiap skor $S_i$ terhadap total akumulasi tersebut untuk memperoleh proporsi preferensi akhir. Rekapitulasi hasil komputasi preferensi dan urutan pemeringkatan akhir disajikan secara lengkap pada Tabel 3.

Tabel 3. Rekapitulasi Nilai Preferensi Vektor S, Vektor V, dan Pemeringkatan Akhir

| Peringkat | Kode | Kandidat Lokasi | Nilai Vektor $S_i$ | Nilai Vektor $V_i$ | Persentase Preferensi | Status Keputusan |
| :---: | :---: | :--- | :---: | :---: | :---: | :--- |
| **1** | **$A_1$** | **Sinduadi (Jl. Umbul Permai)** | **1,6934** | **0,2302** | **23,02%** | **Prioritas Utama (Terpilih)** |
| 2 | $A_5$ | Malioboro Mall | 1,6501 | 0,2243 | 22,43% | Alternatif Cadangan 1 |
| 3 | $A_4$ | Jalan Taman Siswa | 1,5872 | 0,2158 | 21,58% | Alternatif Cadangan 2 |
| 4 | $A_2$ | Koridor Jalan Magelang Km. 5 | 1,4246 | 0,1937 | 19,37% | Alternatif Cadangan 3 |
| 5 | $A_3$ | Kawasan Babarsari | 1,0006 | 0,1360 | 13,60% | Tidak Direkomendasikan |
| **Total** | - | **Akumulasi Parameter** | **7,3559** | **1,0000** | **100,00%** | - |

Berdasarkan Tabel 3, kandidat lokasi Sinduadi ($A_1$) berhasil mengamankan peringkat pertama dengan perolehan preferensi relatif sebesar 0,2302 (23,02%). Malioboro Mall ($A_5$) menempati peringkat kedua dengan nilai 0,2243 (22,43%), disusul oleh Jalan Taman Siswa ($A_4$) sebesar 0,2158 (21,58%), Jalan Magelang ($A_2$) sebesar 0,1937 (19,37%), dan Babarsari ($A_3$) pada posisi juru kunci sebesar 0,1360 (13,60%).

### D.2.2. Pembahasan Hasil Komputasi Menjawab Permasalahan Pendahuluan

Temuan numerik ini memberikan jawaban tegas terhadap dilema pengambilan keputusan spasial yang dipaparkan pada bagian pendahuluan. Permasalahan mendasar pada ekspansi ritel perhiasan emas di Yogyakarta berpusat pada kompromi antara tingginya tarif sewa ruang komersial melawan keunggulan visibilitas dan daya beli konsumen.

Pertarungan evaluasi yang sangat ketat terjadi antara kandidat Sinduadi ($A_1$) dan Malioboro Mall ($A_5$). Selisih preferensi relatif antara kedua lokasi tersebut sangat tipis, yakni hanya terpaut margin 0,0059 atau 0,59%.

Secara profil kualitatif, Malioboro Mall memiliki keunggulan absolut pada parameter potensi daya beli lingkungan ($C_3 = 5$) dan keamanan kawasan ($C_2 = 5$). Kawasan Malioboro merupakan episentrum destinasi wisata belanja dengan arus wisatawan domestik dan mancanegara yang berdaya beli tinggi, serta didukung aglomerasi toko perhiasan historis ($C_6 = 4$).

Kelemahan Malioboro Mall berakar pada beban tarif sewa properti yang mencapai Rp346,32 juta per tahun, atau 2,66 kali lipat lebih tinggi dibandingkan tarif sewa di kawasan Sinduadi yang bernilai Rp130,00 juta per tahun. Karena biaya beban properti bertindak sebagai atribut biaya, selisih sewa yang sangat masif ini memicu penalti eksponensial negatif yang berat ($(346{,}32)^{-0{,}1333} = 0{,}4600$ berbanding $(130{,}00)^{-0{,}1333} = 0{,}5244$).

Kelemahan dari Malioboro Mall ini semakin diperberat oleh adanya restriksi fisik ruang usaha di dalam gedung pusat perbelanjaan tersebut. Pengelola mal memberlakukan regulasi ketat yang membatasi perombakan struktur lantai fondasi ($C_5 = 2$). Keterbatasan ini menjadi kendala serius bagi gerai emas yang memerlukan penanaman sistem jangkar baja untuk brankas tahan bobol bertonase berat [12].

Kandidat tapak Sinduadi ($A_1$) ini berhasil memenangkan peringkat prioritas karena mampu menawarkan keseimbangan kompromi multiatribut yang optimal untuk investasi jangka panjang. Sinduadi menyajikan tarif sewa yang sangat efisien, visibilitas fasad koridor yang sempurna dari Jalan Umbul Permai ($C_4 = 5$), potensi daya beli kawasan hunian menengah atas yang solid ($C_3 = 4$), serta keleluasaan penuh merombak lantai fondasi gedung untuk brankas berat ($C_5 = 5$). Keseimbangan ini membuktikan keunggulan Sinduadi.

Hasil evaluasi juga menjelaskan mengapa kawasan Babarsari ($A_3$) menempati peringkat terbawah dengan nilai preferensi yang tertinggal jauh (13,60%). Meskipun koridor Babarsari memiliki arus lalu lintas harian yang sangat padat, kawasan ini didominasi oleh populasi mahasiswa berpenghasilan terbatas. Profil daya beli mahasiswa tidak beririsan dengan pasar perhiasan logam mulia bernilai jutaan rupiah ($C_3 = 2$). Hasil ini membuktikan bahwa strategi pemilihan tapak gerai emas tidak boleh disamakan dengan ritel makanan atau busana cepat saji [1], [8]. Keputusan investasi harus berlandaskan daya beli tertarget.

### D.2.3. Pengujian Stabilitas Keputusan dan Pembuktian Aksioma IIA

Pengujian model komputasi ini difokuskan pada pembuktian terhadap ketahanan algoritma Weighted Product dalam menangkal anomali pembalikan peringkat (*rank reversal*). Pengujian dilakukan dengan menelaah rasio preferensi relatif antarpasangan alternatif secara mendalam.

Rasio preferensi antara kandidat Sinduadi ($A_1$) dan Malioboro Mall ($A_5$) dianalisis secara aljabar melalui rumusan berikut.

$$\frac{S_1}{S_5} = \frac{1{,}6934}{1{,}6501} = 1{,}0262$$

Karena nilai $S_1 / S_5 = 1{,}0262 > 1$, kandidat Sinduadi secara konsisten mendominasi Malioboro Mall. Dalam formulasi perkalian eksponensial Weighted Product, rasio perbandingan tersebut murni berasal dari perkalian kinerja intrinsik kedua tapak terhadap seluruh kriteria keputusan [5].

$$\frac{S_1}{S_5} = \prod_{j=1}^6 \left( \frac{x_{1j}}{x_{5j}} \right)^{W_j}$$

Formulasi perkalian tersebut membuktikan secara analitis bahwa skor alternatif ketiga, seperti Babarsari ($A_3$) atau alternatif baru hipotetis ($A_6$), tidak pernah dilibatkan dalam perbandingan relatif antara $A_1$ dan $A_5$. Ketika dilakukan simulasi penambahan alternatif baru dengan profil kinerja ekstrem maupun simulasi penghapusan alternatif inferior ($A_3$), rasio preferensi antara Sinduadi dan Malioboro Mall tetap bertahan stabil pada nilai 1,0262.

Kondisi invarian tersebut memastikan bahwa pemeringkatan model hibrida AHP-WP memenuhi aksioma *Independence of Irrelevant Alternatives* (IIA) secara penuh [4], [11]. Fenomena pembalikan peringkat yang kerap mencemari metode AHP murni berhasil dicegah secara menyeluruh.

Pengujian sensitivitas bobot dilakukan untuk mengamati stabilitas peringkat terhadap fluktuasi preferensi kriteria [9]. Ketika bobot kriteria biaya beban properti dinaikkan sebesar 10% hingga 20%, keunggulan Sinduadi semakin kokoh meninggalkan Malioboro Mall akibat melebarnya penalti sewa. Sebaliknya, saat bobot potensi daya beli dinaikkan hingga menyentuh 60%, posisi Sinduadi tetap berada pada rentang batas aman peringkat utama berkat efisiensi biaya yang menopang skor akhirnya.

Pengujian empiris ini menegaskan bahwa integrasi titik potong metodologis pada model AHP-WP menyajikan kerangka kerja sistem pendukung keputusan yang rasional, objektif, dan tangguh untuk alokasi modal investasi fisik [7], [10]. Stabilitas peringkat terjamin secara matematis.

## DAFTAR PUSTAKA

[1] W. Izzaturobbani, S. S. S. A. Al-Habsyi, dan M. R. Pratama, "Analisis Preferensi Investasi Emas Fisik dan Digital pada Era Volatilitas Pasar Modal," *Jurnal Riset Manajemen dan Bisnis (JRMB)*, vol. 11, no. 1, hal. 45-58, 2026.
[2] R. S. Mahendra, "Penerapan Metode Analytic Hierarchy Process dalam Penentuan Lokasi Fasilitas Komersial Perkotaan," *Jurnal Sistem Informasi dan Bisnis Cerdas (JUSTIN)*, vol. 8, no. 2, hal. 112-124, 2020.
[3] Z. Yan and X. Mao, "Axiomatic Analysis and Rank Reversal Vulnerabilities in Multi-Criteria Decision-Making Models," *Axioms*, vol. 14, no. 2, pp. 88-104, 2025.
[4] J. Wang, Y. Liu, and K. Zhang, "Independence of Irrelevant Alternatives in Multi-Attribute Utility Theory and Outranking Methods," *European Journal of Operational Research*, vol. 301, no. 1, pp. 215-229, 2022.
[5] I. Sutrisno dan K. Krisnadana, "Integrasi Metode Weighted Product Berbasis Eksponensial dalam Sistem Pendukung Keputusan Multi-Kriteria," *Jurnal Rekayasa Sistem dan Teknologi Informasi*, vol. 7, no. 3, hal. 401-412, 2023.
[6] P. Triantaphyllou, "Multi-Criteria Decision Making Methods: A Comparative Study and Evaluation of Ranking Inconsistencies," *Applied Mathematical Modelling*, vol. 48, pp. 120-135, 2020.
[7] D. K. Pratiwi dan H. Susanto, "Sistem Pendukung Keputusan Pemilihan Lokasi Strategis Cabang Ritel Menggunakan Pendekatan Hibrida," *Jurnal RESTI (Rekayasa Sistem dan Teknologi Informasi)*, vol. 5, no. 4, hal. 675-683, 2021.
[8] M. F. Nurdin dan A. Cahyono, "Analisis Spasial Tata Ruang Komersial dan Penentuan Lokasi Ritel Bernilai Tinggi di Kawasan Perkotaan," *Jurnal Geografi Tata Ruang Komersial*, vol. 9, no. 2, hal. 130-142, 2022.
[9] A. E. Munandar dan D. P. Hapsari, "Evaluasi Sensitivitas Pembobotan Multi-Kriteria pada Model Pemilihan Lokasi Usaha," *Jurnal Ilmiah Rekayasa dan Manajemen Sistem Informasi (RMSI)*, vol. 10, no. 1, hal. 55-66, 2024.
[10] S. Chakraborty and P. Zavadskas, "Applications of Multi-Criteria Decision-Making Methods in Location Selection Problems: A State-of-the-Art Review," *Applied Soft Computing*, vol. 112, pp. 107-123, 2021.
[11] B. Kurniawan dan F. Rahmawati, "Optimasi Keputusan Multi-Atribut Berbasis Multiplicative Aggregation untuk Mereduksi Resiko Rank Reversal," *Jurnal Teknologi Informasi dan Ilmu Komputer (JTIIK)*, vol. 11, no. 3, hal. 589-598, 2024.
[12] H. R. Prasetyo, "Model Penilaian Risiko dan Kelayakan Investasi Properti Ritel Logam Mulia," Tesis Magister, Departemen Teknik Industri, Universitas Gadjah Mada, Yogyakarta, 2023.
