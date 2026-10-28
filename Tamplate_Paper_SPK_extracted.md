Integrasi Metode AHP dan Weighted Product pada Penentuan Lokasi Strategis Bisnis Ritel Perhiasan 
1Novelia Harlinda,  2Auliah Qorinaya,  3Muhammad Adin Dwi Ramadhan,  4Muhammad Riski, 5Rafael Aga Pratama
1Program Studi Pendidikan Teknik Informatika, Fakultas Teknik, Universitas Negeri Yogyakarta 
Email: 1noveliahrlnd@gmail.com, 2qorinayaaulia@gmail.com,  3madindwir@gmail.com, 4muhamaddriski098@gmail.com, 5rafaelagapratama0@gmail.com 
ABSTRAK (huruf besar, 10pt, tebal, dan ditengah)
Tempatkan abstrak Bahasa Indonesia pada bagian ini. Abstrak memberikan gambaran umum tentang isi makalah dan harus ditulis dengan Times New Roman 10 dalam format satu kolom. Panjang ideal sebuah abstrak adalah 150 sampai 250 kata. Jika terdapat istilah-istilah asing yang belum dibakukan ditulis italic.
Kata kunci: kata kunci sedapat mungkin menjelaskan isi tulisan, ditulis dengan huruf kecil kecuali singkatan, maksimum enam kata, masing-masing dipisahkan dengan koma, Times New Roman 10pt, italic
Abstract (10pt, italic, tebal, dan ditengah)
Tempatkan abstrak berbahasa Inggris pada bagian ini. Gunakan font Times New Roman 10pt, italic.
(1 baris kosong, 10pt)
Keywords: kata kunci sedapat mungkin menjelaskan isi tulisan, ditulis dengan huruf kecil kecuali singkatan, maksimum enam kata, masing-masing dipisahkan dengan koma, Times New Roman 10, italic
(1 baris kosong, 10pt)
PENDAHULUAN (huruf besar, 10pt, tebal)
Komoditas emas mencatatkan rekor lonjakan harga tertinggi pada tahun 2025 sebagai refleksi langsung dari ketidakpastian ekonomi global dan pelemahan nilai tukar rupiah. Meskipun harga mengalami volatilitas yang tajam, emas secara konsisten dipertahankan oleh masyarakat sebagai aset pelindung nilai (safe haven) utama di tengah gejolak pasar. Fenomena lonjakan harga ini secara empiris tidak menyurutkan minat beli, melainkan memicu pergeseran strategi transaksi ke produk yang lebih fleksibel, di mana 41,7% masyarakat beralih pada produk cicil emas dan 25% memilih tabungan emas. Tingginya adaptabilitas dan resiliensi permintaan pasar ini berdampak langsung pada urgensi ekspansi industri ritel perhiasan dan layanan fisik emas. Dalam manajemen operasional, agresivitas pembukaan cabang toko emas baru menuntut penyelesaian masalah Multiple Criteria Decision Making (MCDM) yang presisi untuk menentukan penempatan lokasi strategis. Pengambil keputusan atau investor dihadapkan pada struktur kalkulasi yang mewajibkan kalibrasi matematis antara atribut biaya, seperti beban harga sewa properti, dengan atribut keuntungan yang meliputi tingkat keamanan eksternal kawasan, potensi daya beli lingkungan, visibilitas lokasi, dan aglomerasi sentra perhiasan.
Analytic Hierarchy Process (AHP) merupakan salah satu alat komputasi yang secara luas diaplikasikan dalam penyelesaian masalah MCDM penentuan lokasi. Namun, penerapan AHP di dunia nyata memiliki celah kontroversial yang secara akademis sering dikritik, yaitu anomali rank reversal atau perubahan peringkat secara tidak logis. Masalah rank reversal ini terjadi ketika peringkat preferensi dari dua alternatif opsi dalam kumpulan awal mengalami pembalikan posisi mutlak hanya karena adanya intervensi penambahan satu opsi baru ke dalam matriks set perhitungan. Secara operasional, fenomena ini mendisrupsi stabilitas pengambilan keputusan investasi dan memicu keraguan terhadap validitas kerangka kerja matematis AHP secara keseluruhan apabila diaplikasikan hingga tahap akhir penilaian.
Ketidakstabilan peringkat pada metode AHP murni bukanlah artifak perhitungan kasual, melainkan properti struktural dari pemodelan keputusan itu sendiri. Berbagai pengujian literatur terdahulu membuktikan bahwa anomali pergeseran peringkat tersebut tetap bertahan meskipun skema normalisasi yang ditingkatkan telah diterapkan ke dalam komputasi. Mengingat tingginya risiko presisi kapital pada pembukaan cabang toko emas baru, penggunaan AHP pada penelitian ini dibatasi secara mutlak dan diisolasi hanya pada fase komputasi pembobotan kriteria spasial. Fase reduksi ini memanfaatkan prinsip perbandingan berpasangan murni guna memperoleh Eigen Vector pembobot yang objektif, yang mana validitas transitifnya dikalibrasi melalui Consistency Ratio dengan batas toleransi di bawah 0,1.
Untuk menutupi celah struktural dari fase penilaian alternatif pada AHP murni, penelitian ini mengintegrasikan algoritma Weighted Product (WP) sebagai penyelesai tahap akhir. Komputasi nilai preferensi akhir dan pemeringkatan kandidat lokasi toko emas didelegasikan sepenuhnya pada permodelan WP. Pendekatan perkalian eksponensial dalam algoritma WP secara matematis mengunci stabilitas rasio perbandingan antar alternatif lokasi, sehingga sistem secara struktural diamankan dari risiko anomali pergeseran rank reversal. Pembangunan kerangka matematis hibrida AHP-WP ini bertujuan untuk merumuskan landasan pengambilan keputusan penentuan lokasi ritel emas yang objektif, terkalibrasi secara konsistensi rasio, bebas dari distorsi peringkat, serta relevan dengan dinamika adaptasi ekspansi pasar logam mulia saat ini.
LANDASAN TEORI
Persamaan Matematika
Penentuan bobot prioritas kriteria dilakukan dengan menormalisasi matriks perbandingan berpasangan dan menghitung nilai rata-rata dari setiap baris. Persamaan (1) merupakan penulisan persamaan untuk mencari bobot kriteria atau Eigen Vector pada algoritma Analytic Hierarchy Process (AHP).
Pada persamaan (1),  merupakan bobot prioritas untuk kriteria ke-. Variabel  adalah ordo matriks atau jumlah kriteria yang dievaluasi. Simbol  merupakan nilai intensitas preferensi antara kriteria ke- terhadap kriteria ke- berdasarkan skala fundamental, sedangkan  merupakan jumlah total nilai pada kolom ke- dalam matriks perbandingan berpasangan.
Validasi terhadap tingkat konsistensi preferensi pengambil keputusan dievaluasi menggunakan Consistency Ratio (CR). Persamaan (2) merupakan penulisan persamaan untuk menghitung nilai rasio konsistensi matriks AHP. 
Pada persamaan (2),  merupakan Consistency Ratio yang persyaratannya tidak boleh melebihi nilai 0,1.  adalah Consistency Index, sedangkan  merupakan Random Index yang nilainya berupa konstanta bergantung pada ordo matriks . Variabel  merupakan nilai eigen maksimum yang diperoleh dari rata-rata hasil pembagian antara vektor jumlah tertimbang dengan Eigen Vector.
Tahap penilaian alternatif lokasi dilakukan menggunakan metode Weighted Product (WP) melalui proses perkalian eksponensial. Persamaan (3) merupakan penulisan persamaan untuk mencari nilai preferensi alternatif atau Vektor S. 
Pada persamaan (3),  merupakan nilai preferensi alternatif ke-. Simbol  adalah operasi perkalian eksponensial dari seluruh kriteria. Variabel  merupakan nilai parameter dari alternatif ke- pada kriteria ke-, sedangkan  merupakan bobot kriteria ke- yang diperoleh dari hasil komputasi AHP. Nilai bobot  ditetapkan bernilai negatif untuk kriteria biaya (cost) dan bernilai positif untuk kriteria keuntungan (benefit).
Penentuan peringkat akhir alternatif lokasi didapatkan melalui proses normalisasi Vektor S. Persamaan (4) merupakan penulisan persamaan untuk menghitung nilai preferensi relatif atau Vektor V.
Pada persamaan (4),  merupakan nilai preferensi relatif alternatif ke- yang akan diurutkan dari nilai tertinggi hingga terendah untuk menentukan rekomendasi akhir. Variabel  merupakan nilai preferensi (Vektor S) pada alternatif ke-, sedangkan  merupakan akumulasi atau jumlah keseluruhan nilai Vektor S dari seluruh alternatif yang terlibat dalam model komputasi. 
Penulisan Tabel (judul 10 pt, isi 8 pt)
Nomor dan judul tabel ditulis diposisi kiri kolom (left alignment). Tabel dinomori dengan angka arab sesuai dengan urutannya. Judul tabel ditulis dibagian atas tabel dengan cara title case, kecuali untuk kata sambung dan kata depan. Ukuran huruf untuk judul tabel 10 (sepuluh) dan isi tabel adalah 8 (delapan). Sisi paling luar tabel tidak boleh melebihi batas margin kolom. Jika ukuran tabel tidak cukup ditulis dalam lebar 1 (satu), maka penulisannya dapat melintasi 2 kolom. Jarak baris yang digunakan antara tabel dengan kalimat diatasnya dan dibawahnya adalah 1 (satu) baris kosong. Tabel wajib menggunakan layout sesuai dengan Tabel 1 tanpa menggunakan garis lurus/vertikal. Setiap tabel harus diacu dalam tulisan dengan disertai nomor tabel dan diawali dengan huruf besar, misalnya Tabel 1.
Tabel 1. Hasil uji black box aplikasi navigasi berbasis mobile
Smartphone
Sistem Operasi Mobile
Tingkat Keberhasilan
Lenovo A610 Plus
Android OS, V5.0
100 %
Samsung Galaxy
Android OS, V5.0
100 %
Xiaomi Redmi 3s
Android OS, V6.01
100 %
Samsung Galaxy ACE3
Android OS, V4.2 
100 %
Asus Zenfone 2 Laser
Android OS, V5.0 
100 %
Oppo Mirror 5
Android OS, V5.1 
100 %
Oppo NEO 7
Android OS, V5.1
100 %
Asus Zenfone 5
Android OS, V5.0
100 %
Huawei Y6
Android OS, V5.1
100 %
Asus Z007
Android OS, V.4.4.2
100 %
Rata-rata
100 %
Penggunaan Gambar
Nomor dan judul gambar ditulis diposisi tengah kolom (center alignment). Nomor gambar ditulis sesuai dengan urutannya menggunakan angka arab. Judul gambar ditulis dibagian bawah gambar dengan cara title case, kecuali untuk kata sambung kata sambung dan kata depan. Judul gambar menggunakan ukuran huruf 10 (sepuluh). Gambar tidak boleh melebihi batas margin dari tiap kolom, kecuali jika ukuran gambar yang besar tidak cukup dalam 1 kolom, maka dapat melintasi 2 kolom.
Gambar 1. Contoh penggunaan gambar (10pt, ditengah)
(1 baris kosong, 10pt)
Jarak baris yang digunakan antara gambar dengan kalimat diatasnya dan dibawahnya adalah 1 (satu) baris kosong. Usahakan gambar tidak berwarna/hitam putih (kecuali penggunaan warna pada gambar sangat diperlukan/tidak bisa dihindari) dan jika dicetak dalam hitam putih bisa dibedakan. Jika gambar berupa grafik harus jelas perbedaan antara satu sama lain dengan menggunakan jenis line dan marker yang berbeda-beda. Setiap gambar harus diacu dalam tulisan dengan disertai nomor gambar dan diawali dengan huruf besar, misalnya Gambar 1.
METODE PENELITIAN
Metode Penelitian memberikan penjelasan tentang langkah-langkah, data, lokasi penelitian, metode evaluasi yang digunakan serta penjelasan terstruktur tentang algoritma atau metode dari penelitian yang dibahas.
HASIL DAN PEMBAHASAN
Sub Bab 1
Bagian Hasil dan Pembahasan memuat hasil-hasil dari penelitian serta pembahasan menyeluruh dari masing-masing hasil yang didapatkan dari penelitian yang dibahas. Berikan pembahasan yang mendetail tentang hasil-hasil yang didapatkan hingga dapat menjawab permasalahan yang disebutkan di bagian Pendahuluan.
Pada sub bab 1 dapat dibahas analisa dan perancangan dan pada sub bab 2 dapat dibahas mengenai implementasi dan pengujian
Sub Bab 2
Sumber pustaka/rujukan sedapat mungkin merupakan pustaka-pustaka terbitan 10 tahun terakhir. Pustaka yang diutamakan adalah naskah-naskah penelitian dalam jurnal, konferensi dan/atau majalah ilmiah. Pustaka lain dapat berupa buku teks atau laporan penelitian (termasuk Skripsi/Tugas Akhir, Tesis, dan Disertasi), akan tetapi diusahakan tidak melebihi 20% dari seluruh jumlah sumber pustaka
Penggunaan materi dari halaman web sangat tidak disarankan. Penulisan daftar pustaka mengikuti bentuk penulisan IEEE dengan urutan artikel/ pustaka dari yang paling pertama muncul (dikutip) di artikel ini hingga yang paling akhir
KESIMPULAN 
Bagian ini memberikan simpulan yang singkat tentang penelitian yang dibahas di artikel ini disertai dengan saran untuk pengembangan atau lanjutan penelitian berikutnya.
REFERENSI
Penulis1 A, Penulis2 B. Judul Artikel. Nama Jurnal. tahun; vol(no): halaman.
Penulis1 A, Penulis2 B. Judul Artikel. Nama Konferensi. Kota. Tahun; vol: halaman.
Penulis1 A, Penulis2 B. Judul Buku. Edisi. Kota: Penerbit. tahun: halaman.
Penulis. Judul Tesis/ Disertasi. Tesis/ Disertasi. Kota & Nama Kampus; Tahun.
Penuils1 A, Penulis2 B. Judul. Nomor Paten (Paten). Tahun Publikasi.
Institusi. Nomor standar. Judul. Tempat Publikasi. Penerbit. Tahun Publikasi.
Penulis/Editor (Jika editor tambahkan (ed./eds.) setelah nama). Judul. Organisasi. Nomor Laporan: no. Tahun.
