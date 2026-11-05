---
title: Bab Landasan Teori - Integrasi Metode AHP dan Weighted Product pada Penentuan Lokasi Ritel Perhiasan
created: 2026-11-03
status: Ready for Manuscript
target_journal: Template UIN SUSKA (Jurnal Ilmiah Rekayasa dan Manajemen Sistem Informasi)
format: LaTeX / Markdown
tags:
  - landasan-teori
  - mcdm
  - ahp
  - weighted-product
  - rank-reversal
  - lokasi-ritel-emas
---

# LANDASAN TEORI

## 1. Multi-Criteria Decision Making (MCDM)

*Multi-Criteria Decision Making* (MCDM) merupakan sub-disiplin fundamental dalam riset operasi (*operations research*) yang berfokus pada perancangan model komputasi dan pemecahan masalah keputusan kompleks dengan melibatkan sekumpulan kriteria yang saling bertentangan (*conflicting criteria*). Dalam teori optimasi klasik, model pengambilan keputusan sering kali mengasumsikan keberadaan fungsi tujuan tunggal yang homogen. Namun, sistem operasional riil menuntut integrasi tujuan ganda di mana perbaikan performa pada suatu parameter sering kali mengorbankan parameter lainnya secara signifikan (*trade-off*).

Dalam taksonomi riset operasi, MCDM diklasifikasikan ke dalam dua kategori utama: *Multi-Objective Decision Making* (MODM) dan *Multi-Attribute Decision Making* (MADM). MODM beroperasi pada ruang keputusan kontinu dengan jumlah alternatif tak terhingga yang dibatasi oleh formulasi kendala linear atau non-linear. Sebaliknya, MADM berfokus pada ruang keputusan diskrit, di mana pengambil keputusan mengevaluasi gugus alternatif berhingga $A = \{A_1, A_2, \dots, A_m\}$ terhadap sekumpulan atribut atau kriteria evaluasi $C = \{C_1, C_2, \dots, C_n\}$. Secara matematis, konfigurasi ini direpresentasikan melalui matriks keputusan $X$:

$$
X = [x_{ij}]_{m \times n} = 
\begin{pmatrix}
x_{11} & x_{12} & \dots & x_{1n} \\
x_{21} & x_{22} & \dots & x_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
x_{m1} & x_{m2} & \dots & x_{mn}
\end{pmatrix}
\tag{1}
$$

di mana $x_{ij}$ menyatakan nilai kinerja alternatif ke-$i$ pada kriteria ke-$j$. Tantangan analitis dalam MADM terletak pada kenyataan bahwa kriteria-kriteria keputusan bersifat *incommensurable* (memiliki satuan ukur yang tidak sepadan) dan melibatkan gabungan antara variabel kuantitatif (seperti biaya sewa dalam satuan moneter) serta variabel kualitatif preferensial (seperti tingkat keamanan kawasan dan persepsi visibilitas). Oleh karena itu, pendekatan MCDM tidak mencari solusi absolut, melainkan menyintesis preferensi pembuat keputusan guna menemukan solusi kompromi terbaik (*compromise solution*) yang memenuhi prinsip non-dominasi Pareto.

---

## 2. Teori Lokasi Ritel Premium (Toko Emas)

Penentuan lokasi fasilitas komersial berakar kuat pada teori ekonomi tata ruang (*spatial retail economics*). Dua fondasi teoretis utama yang melandasinya adalah *Central Place Theory* dari Walter Christaller dan Model Diferensiasi Spasial dari Harold Hotelling. Dalam perspektif *Central Place Theory*, ritel perhiasan emas diklasifikasikan sebagai penyedia barang berorde tinggi (*high-order goods*). Komoditas ini memiliki nilai transaksi per unit yang sangat besar dengan frekuensi pembelian yang relatif rendah, sehingga menuntut ambang batas populasi (*population threshold*) yang spesifik dan jangkauan spasial (*spatial range*) yang luas. Konsumen bersedia menempuh jarak perjalanan yang lebih jauh untuk menjangkau toko emas dibandingkan barang kebutuhan sehari-hari (*low-order goods*).

Lebih lanjut, teori aglomerasi ekonomi (*agglomeration economies*) yang diinisiasi oleh Alfred Marshall dan dielaborasi dalam model persaingan spasial Hotelling menjelaskan kecenderungan gerai-gerai perhiasan untuk saling berdekatan dan membentuk sentra atau klaster pasar terpusat. Aglomerasi gerai sejenis secara empiris menurunkan biaya pencarian konsumen (*consumer search cost*), memfasilitasi transaksi perbandingan harga dan model (*comparative shopping*), serta meningkatkan volume kunjungan terarah (*targeted traffic*) ke kawasan tersebut.

Karakteristik operasional ritel toko emas memiliki keunikan struktural yang membedakannya secara tajam dari ritel komersial pada umumnya:
1. **Rasio Nilai terhadap Volume yang Ekstrem (*High Value-to-Volume Density*)**: Tingginya konsentrasi nilai kapital per unit ruang menyebabkan toko emas rentan terhadap eksposur kejahatan kekerasan dan penjarahan. Kebutuhan mitigasi risiko menuntut kehadiran atribut keamanan eksternal kawasan yang ketat, kedekatan dengan instalasi aparat penegak hukum, serta visibilitas koridor yang tinggi guna mendukung pengawasan alami (*natural surveillance*).
2. **Kendala Struktural Properti**: Penyimpanan inventori emas fisik memerlukan instalasi brankas baja tahan api dengan bobot tonase berat, partisi kaca anti-peluru, serta sistem keamanan lapis ganda. Kondisi ini mewajibkan fleksibilitas modifikasi struktur bangunan dari pemilik properti.

Dengan demikian, optimalisasi lokasi toko emas bukanlah masalah minimasi biaya properti murni. Terdapat tarik-ulur (*trade-off*) tajam antara atribut biaya (*cost*)—seperti beban harga sewa properti komersial tahunan yang eksorbitan pada lokasi primer—dengan gugus atribut keuntungan (*benefit*) yang mencakup jaminan keamanan lingkungan, densitas daya beli masyarakat sekitar, keterlihatan fisik gerai, dan kekuatan aglomerasi sentra niaga perhiasan. Formulasi komputasi multikriteria menjadi imperatif untuk menghindari bias persepsi pengambil keputusan.

---

## 3. Analytic Hierarchy Process (AHP) dan Aksioma Konsistensi

*Analytic Hierarchy Process* (AHP), yang dikembangkan oleh matematikawan Thomas L. Saaty, adalah metode pengukuran melalui perbandingan berpasangan (*pairwise comparison*) yang bergantung pada penilaian pakar untuk menetapkan skala prioritas rasio. Dalam kerangka penelitian ini, AHP digunakan secara **eksklusif hanya untuk penentuan bobot kriteria global**, dan tidak diikutsertakan dalam perankingan alternatif. Pembatasan fungsional ini didasarkan pada keunggulan metodologis AHP dalam mereduksi kompleksitas persepsi manusia melalui struktur hierarki linier sekaligus mengevaluasi derajat konsistensi logis penilai.

### 3.1. Struktur Matriks Perbandingan Berpasangan
Penentuan bobot prioritas dimulai dengan mengonstruksi matriks perbandingan berpasangan $A = [a_{ij}]_{n \times n}$ berordo $n$, di mana $n$ adalah jumlah kriteria yang dievaluasi:

$$
A = 
\begin{pmatrix}
a_{11} & a_{12} & \dots & a_{1n} \\
a_{21} & a_{22} & \dots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{n1} & a_{n2} & \dots & a_{nn}
\end{pmatrix}
\tag{2}
$$

Matriks perbandingan berpasangan $A$ wajib memenuhi **Aksioma Resiprokal (*Reciprocal Axiom*)**:

$$
a_{ji} = \frac{1}{a_{ij}} \quad \text{dan} \quad a_{ii} = 1 \quad \forall i, j \in \{1, 2, \dots, n\}
\tag{3}
$$

Intensitas preferensi relatif $a_{ij}$ dinilai menggunakan skala fundamental Saaty (1 sampai 9), di mana nilai 1 merepresentasikan tingkat kepentingan yang sama (*equal importance*), sedangkan nilai 9 merepresentasikan tingkat kepentingan mutlak (*extreme importance*).

### 3.2. Pencarian Vektor Bobot Prioritas (Eigen Vector)
Vektor bobot prioritas kriteria $w = [w_1, w_2, \dots, w_n]^T$ secara eksak diperoleh melalui formulasi nilai eigen dan vektor eigen (*principal eigenvector*):

$$
A w = \lambda_{\max} w
\tag{4}
$$

di mana $\lambda_{\max}$ adalah nilai eigen terbesar (*principal eigenvalue*) dari matriks $A$. Dalam komputasi praktis, bobot prioritas relatif kriteria ke-$j$ ($w_j$) disintesis melalui rata-rata baris dari matriks yang dinormalisasi terhadap jumlah kolomnya:

$$
w_j = \frac{1}{n} \sum_{k=1}^n \frac{a_{jk}}{\sum_{i=1}^n a_{ik}} \quad \forall j \in \{1, 2, \dots, n\}
\tag{5}
$$

dengan batasan konstrain normalisasi:

$$
\sum_{j=1}^n w_j = 1
\tag{6}
$$

### 3.3. Aksioma Konsistensi dan Batas Toleransi Consistency Ratio ($CR < 0{,}10$)
Kelemahan kognitif manusia menyebabkan penilaian perbandingan berpasangan rentan terhadap inkonsistensi transitif. Secara teoretis, jika kriteria $A$ dinilai dua kali lebih penting daripada kriteria $B$ ($a_{AB} = 2$), dan kriteria $B$ dinilai tiga kali lebih penting daripada kriteria $C$ ($a_{BC} = 3$), maka preferensi yang konsisten secara sempurna menuntut kriteria $A$ bernilai enam kali lebih penting daripada kriteria $C$ ($a_{AC} = 6$). Jika pengambil keputusan menetapkan nilai yang bertentangan, terjadi deviasi kardinal.

Matriks $A$ dikatakan konsisten sempurna jika dan hanya jika $\lambda_{\max} = n$. Apabila terdapat pertimbangan inkonsisten, nilai $\lambda_{\max} > n$. Nilai $\lambda_{\max}$ diestimasi melalui rata-rata elemen vektor konsistensi:

$$
\lambda_{\max} = \frac{1}{n} \sum_{i=1}^n \frac{(A \cdot w)_i}{w_i}
\tag{7}
$$

Penyimpangan konsistensi dievaluasi menggunakan *Consistency Index* ($CI$):

$$
CI = \frac{\lambda_{\max} - n}{n - 1}
\tag{8}
$$

Guna menentukan apakah deviasi tersebut dapat diterima secara ilmiah, Saaty merumuskan *Consistency Ratio* ($CR$) dengan membandingkan $CI$ terhadap *Random Index* ($RI$), yaitu rata-rata indeks konsistensi dari simulasi matriks acak berordo $n$:

$$
CR = \frac{CI}{RI}
\tag{9}
$$

Nilai empiris standar $RI$ Saaty disajikan pada Tabel 1:

**Tabel 1. Nilai Random Index ($RI$) Berdasarkan Ordo Matriks ($n$)**
| $n$ | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **$RI$** | 0{,}00 | 0{,}00 | 0{,}58 | 0{,}90 | 1{,}12 | 1{,}24 | 1{,}32 | 1{,}41 | 1{,}45 | 1{,}49 |

Dalam teori AHP, batas toleransi inkonsistensi ditetapkan secara rigid:

$$
CR \le 0{,}10 \quad (10\%)
\tag{10}
$$

**Argumen Teoretis Penetapan Batas $CR \le 0{,}10$:**
1. **Validasi Rasionalitas Keputusan**: Ambang batas 10% menjamin bahwa matriks perbandingan tidak dihasilkan dari tebakan spekulatif atau fluktuasi acak (*random errors*). Nilai $CR \le 0{,}10$ membuktikan adanya koherensi logis dalam pemikiran pengambil keputusan.
2. **Kekebalan Transitivitas Preferensi**: Deviasi di bawah 0,10 mempertahankan relasi transitif antar-kriteria, sehingga struktur prioritas kriteria tidak mengalami pertentangan hierarki.
3. **Integritas Input Komputasi Sekuensial**: Bobot kriteria $w_j$ yang dihasilkan akan digunakan sebagai eksponen dalam algoritma *Weighted Product*. Menjamin $CR \le 0{,}10$ adalah syarat mutlak agar bobot yang dialirkan ke tahap perankingan memiliki reliabilitas ilmiah yang teruji. Jika $CR > 0{,}10$, matriks wajib ditolak dan proses perbandingan berpasangan harus diulang.

---

## 4. Weighted Product (WP) dan Ketahanan Terhadap Rank Reversal

### 4.1. Celah Struktural AHP Murni: Anomali *Rank Reversal*
Meskipun AHP unggul dalam penentuan bobot kriteria, penerapannya pada fase pemeringkatan alternatif menuai kritik tajam dalam literatur riset operasi akibat anomali *rank reversal*. Anomali ini merujuk pada fenomena matematis di mana urutan preferensi relatif antara dua alternatif yang sudah ada (misalnya $A_1 > A_2$) mengalami pembalikan peringkat ($A_2 > A_1$) semata-mata karena adanya penambahan atau penghapusan alternatif baru yang identik atau tidak relevan (*irrelevant alternative*).

Secara aljabar, kelemahan ini berakar dari mekanisme normalisasi penjumlahan aditif lokal pada AHP murni:

$$
\bar{a}_{ik} = \frac{a_{ik}}{\sum_{i=1}^m a_{ik}}
\tag{11}
$$

Penyebut $\sum_{i=1}^m a_{ik}$ merupakan fungsi linear dari seluruh alternatif yang dievaluasi. Masuknya alternatif baru $A_{m+1}$ mengubah nilai penyebut untuk setiap baris, mendistorsi rasio perbandingan preferensi lokal antar-alternatif yang ada. Fenomena ini secara eksplisit melanggar aksioma *Independence of Irrelevant Alternatives* (IIA) yang dirumuskan oleh Kenneth Arrow. Dalam investasi gerai fisik bernilai kapital tinggi, ketidakstabilan peringkat tersebut sangat berbahaya karena rekomendasi lokasi terbaik dapat bergeser secara artifisial hanya akibat penambahan opsi lokasi kandidat baru ke dalam sistem kalkulasi.

### 4.2. Mekanisme Multiplikatif Non-Linear Weighted Product (Vektor S)
Untuk mengatasi kelemahan mendasar tersebut, algoritma *Weighted Product* (WP) diintegrasikan sebagai mesin komputasi perankingan alternatif menggantikan sintesis aditif AHP. Metode WP mengevaluasi sekumpulan alternatif melalui operasi perkalian multiplikatif non-linear, di mana kinerja setiap alternatif dipangkatkan secara eksponensial terhadap bobot kriteria yang bersangkutan.

Sebelum dioperasikan, bobot kriteria $w_j$ hasil sintesis AHP dinormalisasi kembali guna memastikan total pangkat bernilai satu:

$$
W_j = \frac{w_j}{\sum_{k=1}^n w_k} \quad \text{sehingga} \quad \sum_{j=1}^n W_j = 1
\tag{12}
$$

Nilai preferensi absolut setiap alternatif dihitung melalui formulasi **Vektor $S_i$**:

$$
S_i = \prod_{j=1}^n \left( x_{ij} \right)^{W_j^*} \quad \forall i \in \{1, 2, \dots, m\}
\tag{13}
$$

di mana $x_{ij}$ adalah nilai kinerja alternatif ke-$i$ pada kriteria ke-$j$, dan pemangkatan $W_j^*$ dikondisikan secara tegas berdasarkan polaritas atribut:

$$
W_j^* = 
\begin{cases} 
+W_j, & \text{jika kriteria } j \text{ berkarakter keuntungan (benefit)} \\
-W_j, & \text{jika kriteria } j \text{ berkarakter biaya (cost)}
\end{cases}
\tag{14}
$$

Pada kriteria keuntungan (*benefit*), pemangkatan dengan eksponen positif mempertahankan hubungan monotonik naik: semakin tinggi nilai $x_{ij}$, semakin besar kontribusinya terhadap $S_i$. Sebaliknya, pada kriteria biaya (*cost*), pemangkatan dengan eksponen negatif secara matematis ekuivalen dengan operasi pembagian:

$$
x_{ij}^{-W_j} = \frac{1}{x_{ij}^{W_j}}
\tag{15}
$$

Formulasi ini secara proporsional mendiskon nilai preferensi alternatif apabila nilai biaya propertinya semakin tinggi.

### 4.3. Pembuktian Matematis Ketahanan Terhadap Rank Reversal
Kekebalan metode WP terhadap distorsi *rank reversal* terletak pada sifat pemangkatan eksponensial dalam perhitungan Vektor $S$. Berdasarkan Persamaan (13), perbandingan rasio preferensi antara dua alternatif sebarang, $A_a$ dan $A_b$, dirumuskan sebagai berikut:

$$
\frac{S_a}{S_b} = \frac{\prod_{j=1}^n \left( x_{aj} \right)^{W_j^*}}{\prod_{j=1}^n \left( x_{bj} \right)^{W_j^*}} = \prod_{j=1}^n \left( \frac{x_{aj}}{x_{bj}} \right)^{W_j^*}
\tag{16}
$$

Persamaan (16) membuktikan bahwa rasio preferensi $\frac{S_a}{S_b}$ **bersifat invarian murni**. Rasio tersebut hanya ditentukan secara eksklusif oleh nilai kinerja internal $A_a$ dan $A_b$ serta vektor bobot kriteria $W_j^*$. Formulasi ini sama sekali tidak melibatkan variabel kinerja dari alternatif ketiga ($A_c$) atau alternatif baru yang ditambahkan ke dalam gugus keputusan ($x_{kj}, k \notin \{a, b\}$).

Jika alternatif $A_a$ mendominasi alternatif $A_b$ sehingga $\frac{S_a}{S_b} > 1$, maka relasi $\frac{S_a}{S_b} > 1$ akan selalu berlaku secara absolut, berapapun jumlah kandidat lokasi baru yang ditambahkan atau dieliminasi dari sistem. Dengan demikian, metode WP menjamin terpenuhinya aksioma *Independence of Irrelevant Alternatives* (IIA) dan secara mutlak mengeliminasi anomali *rank reversal*.

### 4.4. Perhitungan Nilai Preferensi Relatif (Vektor V)
Untuk menghasilkan rekomendasi akhir, dihitung nilai preferensi relatif komprehensif melalui **Vektor $V_i$**:

$$
V_i = \frac{S_i}{\sum_{k=1}^m S_k} = \frac{\prod_{j=1}^n \left( x_{ij} \right)^{W_j^*}}{\sum_{k=1}^m \prod_{j=1}^n \left( x_{kj} \right)^{W_j^*}} \quad \forall i \in \{1, 2, \dots, m\}
\tag{17}
$$

dengan batasan probabilistik:

$$
\sum_{i=1}^m V_i = 1
\tag{18}
$$

Tahap normalisasi pada Persamaan (17) membagi seluruh nilai $S_i$ dengan skalar akumulatif yang identik ($\sum S_k$). Karena pembagian dengan skalar positif bersifat strictly monotonic, urutan peringkat preferensi akhir sepenuhnya terkunci:

$$
V_a > V_b \iff S_a > S_b
\tag{19}
$$

Nilai $V_i$ tertinggi ($V_{\max} = \max \{V_1, V_2, \dots, V_m\}$) mengidentifikasi kandidat lokasi toko emas yang paling optimal, menyajikan keputusan yang adil terhadap kompromi biaya-manfaat (*trade-off*), terbebas dari bias kognitif melalui validasi konsistensi AHP, serta kokoh secara metodologis dari gangguan distorsi peringkat.

