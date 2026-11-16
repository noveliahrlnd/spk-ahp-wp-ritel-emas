# B. LANDASAN TEORI

## B.1. Persamaan Matematika

Penelitian ini menerapkan suatu pendekatan hibrida sekuensial yang membagi proses komputasi ke dalam dua fase: fase pembobotan kriteria menggunakan *Analytic Hierarchy Process* (AHP) dan fase pemeringkatan alternatif menggunakan *Weighted Product* (WP). Kedua metode dipadukan secara komplementer sehingga kelemahan struktural yang muncul jika hanya satu metode dipakai hingga tahap akhir dapat dihindari.

Pemilihan lokasi gerai ritel perhiasan emas dimodelkan sebagai persoalan *Multi-Criteria Decision Making* (MCDM) yang mengevaluasi sejumlah alternatif diskret $A = \{A_1, A_2, \dots, A_m\}$ berdasarkan sekumpulan kriteria $C = \{C_1, C_2, \dots, C_n\}$ yang saling bertentangan dan memiliki satuan ukur yang tidak sepadan (*incommensurable*). Seluruh data kinerja awal direpresentasikan ke dalam matriks keputusan $X$ berordo $m \times n$, dengan elemen $x_{ij}$ menyatakan nilai kinerja alternatif ke-$i$ pada kriteria ke-$j$. Struktur matriks ini menjadi landasan bagi seluruh proses komputasi selanjutnya.

> $$
> X = [x_{ij}]_{m \times n} =
> \begin{pmatrix}
> x_{11} & x_{12} & \dots & x_{1n} \\
> x_{21} & x_{22} & \dots & x_{2n} \\
> \vdots & \vdots & \ddots & \vdots \\
> x_{m1} & x_{m2} & \dots & x_{mn}
> \end{pmatrix}
> $$

Metode AHP digunakan untuk menyintesis bobot prioritas kriteria melalui matriks perbandingan berpasangan (*pairwise comparison*) $A = [a_{ik}]_{n \times n}$ [2]. Elemen $a_{ik}$ merepresentasikan tingkat kepentingan relatif kriteria ke-$i$ terhadap kriteria ke-$k$ menurut skala Saaty yang bernilai 1 hingga 9, dengan aturan bahwa nilai yang lebih tinggi mencerminkan dominasi yang lebih kuat dari kriteria baris atas kriteria kolom. Agar seluruh pertimbangan konsisten secara matematis, matriks tersebut wajib memenuhi aksioma resiprokal [2]. Sifat ini memastikan keterbalikan logis antara setiap pasang kriteria.

> $$
> a_{ki} = \frac{1}{a_{ik}} \quad \text{dan} \quad a_{ii} = 1 \quad \forall i, k \in \{1, 2, \dots, n\}
> $$

Bobot prioritas kriteria ($w_j$) diperoleh dengan menormalisasi setiap elemen sel terhadap total kolomnya, lalu merata-ratakan nilai baris sesuai Persamaan (1). Kriteria yang secara konsisten dinilai lebih penting pada perbandingan antarbaris akan menghasilkan bobot yang lebih besar.

> $$
> w_j = \frac{1}{n} \sum_{k=1}^n \frac{a_{jk}}{\sum_{i=1}^n a_{ik}} \quad \forall j \in \{1, 2, \dots, n\}
> \tag{1}
> $$

Pada Persamaan (1), notasi $w_j$ menyatakan bobot prioritas kriteria ke-$j$ dengan batas akumulasi $\sum_{j=1}^n w_j = 1$, sedangkan $n$ menunjukkan jumlah kriteria yang dianalisis. Elemen $a_{jk}$ mencerminkan nilai perbandingan kriteria ke-$j$ terhadap kriteria ke-$k$, sementara penyebut $\sum_{i=1}^n a_{ik}$ mencerminkan jumlah total nilai pada kolom ke-$k$ dalam matriks perbandingan berpasangan.

Tingkat konsistensi logika penilaian diuji melalui perhitungan *Consistency Index* ($CI$) dan *Consistency Ratio* ($CR$) sesuai Persamaan (2) [2]. Matriks dinyatakan konsisten apabila $CR \le 0{,}10$.

> $$
> CI = \frac{\lambda_{\max} - n}{n - 1}
> \tag{2a}
> $$

> $$
> CR = \frac{CI}{RI}
> \tag{2b}
> $$

Pada Persamaan (2a), simbol $\lambda_{\max}$ menyatakan nilai eigen terbesar yang dihitung dari rata-rata pembagian vektor jumlah berbobot terhadap bobot prioritas, sedangkan pada Persamaan (2b), $RI$ adalah indeks acak Saaty yang nilainya bergantung pada ordo matriks $n$ dan diperoleh dari tabel standar Saaty. Nilai $RI$ meningkat seiring bertambahnya ordo matriks.

Metode WP memeringkatkan alternatif lokasi melalui perkalian eksponensial yang menghubungkan nilai kinerja setiap kriteria dengan bobotnya [3]. Tahap awal komputasi WP dimulai dengan penyesuaian pangkat bobot kriteria sesuai Persamaan (3a), sehingga jumlah seluruh pangkat bobot tetap terstandardisasi.

> $$
> W_j = \frac{w_j}{\sum_{k=1}^n w_k} \quad \text{sehingga} \quad \sum_{j=1}^n W_j = 1
> \tag{3a}
> $$

Selanjutnya, nilai preferensi absolut setiap alternatif dihitung melalui Vektor $S_i$ pada Persamaan (3b). Tanda pangkat eksponen $W_j^*$ ditentukan oleh sifat atribut kriteria: bertanda positif untuk kriteria *benefit* dan bertanda negatif untuk kriteria *cost*.

> $$
> S_i = \prod_{j=1}^n (x_{ij})^{W_j^*} \quad \forall i \in \{1, 2, \dots, m\}
> \tag{3b}
> $$

> $$
> W_j^* =
> \begin{cases}
> +W_j, & \text{apabila kriteria } j \text{ bersifat keuntungan (benefit)} \\
> -W_j, & \text{apabila kriteria } j \text{ bersifat biaya (cost)}
> \end{cases}
> $$

Pada Persamaan (3b), notasi $m$ menyatakan jumlah alternatif dan $n$ menunjukkan jumlah kriteria, sedangkan $x_{ij}$ adalah nilai kinerja alternatif ke-$i$ pada kriteria ke-$j$. Sifat multiplikatif ini menjamin bahwa rasio $S_a / S_b$ antara dua alternatif bersifat konstan tanpa dipengaruhi kehadiran alternatif ketiga. Metode ini karena itu kebal terhadap anomali pembalikan peringkat (*rank reversal*) [5].

Rekomendasi lokasi optimal ditetapkan berdasarkan nilai preferensi relatif Vektor $V_i$ yang diperoleh melalui normalisasi skor $S_i$ terhadap total akumulasi preferensi seluruh alternatif sesuai Persamaan (4), dengan alternatif yang memiliki nilai $V_i$ terbesar dipilih sebagai prioritas utama.

> $$
> V_i = \frac{S_i}{\sum_{k=1}^m S_k} = \frac{\prod_{j=1}^n (x_{ij})^{W_j^*}}{\sum_{k=1}^m \prod_{j=1}^n (x_{kj})^{W_j^*}} \quad \forall i \in \{1, 2, \dots, m\}
> \tag{4}
> $$

Pada Persamaan (4), notasi $V_i$ menyatakan nilai preferensi relatif alternatif ke-$i$ dengan batas akumulasi $\sum_{i=1}^m V_i = 1$. Karena pembagi $\sum S_k$ bernilai positif konstan, urutan nilai $V_i$ bersifat monotonik terhadap $S_i$. Peringkat yang dihasilkan kedua vektor tersebut karena itu selalu identik.
