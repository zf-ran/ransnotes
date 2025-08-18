# Sesi 1

> [!info] Detail
>
> -   **Tipe:** Pilihan ganda.
> -   **Jumlah:** 16 soal.
> -   **Waktu:** 90 menit.
> -   **Penilaian:**
>     -   Benar: +1
>     -   Kosong: 0
>     -   Salah: 0

> [!important] Pernyataan untuk Nomor 1–3
> Di sebuah pabrik perhiasan, kamu ditugaskan untuk merancang untaian kalung dari manik-manik berwarna putih dan hitam. Persediaan kedua warna ini sangat banyak, jadi kamu tidak perlu khawatir kehabisan bahan.
>
> Namun, ada dua aturan penting yang wajib dipatuhi dalam merangkai kalung.
>
> -   Tidak boleh ada **$k$ manik hitam berturut-turut** dalam satu kalung.
> -   Setiap kalung harus selalu **diawali dengan manik putih**.
>
> Tugasmu adalah menghitung berapa banyak cara berbeda untuk menyusun kalung dengan panjang $n$ (jumlah total manik), yang memenuhi dua aturan tersebut.

> [!question] Nomor 1
> Berapakah hasil jika $n = 8$ dan $k = 3$?
>
> -   [ ] 128
> -   [x] **81**
> -   [ ] 64
> -   [ ] 256
> -   [ ] 243

Kerjakan soal ini menggunakan konsep *dynamic programming* dengan menggunakan $n$ sebagai *state*-nya, lakukan transisi yaitu

$$
	\newcommand{\dp}{\mathrm{dp}}
	\dp[i] = \dp[i - 1] + \dp[i - 2] + \cdots + \dp[i - k]
$$

dengan base case $\dp[0] = 1$. Ide dari *dynamic programming* tersebut sebenarnya sederhana di mana setiap memasang manik hitam sebanyak $0$ hingga $k - 1$ kita letakkan manik putih terlebih dahulu sebagai sekat nya sehingga transisi yang dilakukan mulai dari $\dp[i - 1]$ hingga $\dp[i - k]$ dan didapati $\dp[8]$ akan bernilai 81.

---

> [!question] Nomor 2
> Berapakah hasil jika $n = 15$ dan $k = 5$?
>
> -   [ ] 13620
> -   [ ] 13621
> -   [ ] 13622
> -   [ ] 13623
> -   [x] **13624**

Sama seperti soal sebelumnya didapati $\dp[15]$ akan bernilai 13624.

---

> [!question] Nomor 3
> Berapakah hasil jika $n = 15$ dan $k = 5$?
>
> -   [x] **797495860**
> -   [ ] 797495861
> -   [ ] 797495862
> -   [ ] 797495863
> -   [ ] 797495864

Sedikit berbeda dengan 2 soal sebelumnya, kita harus membuat *code* untuk *constraint* sebesar ini dan dengan tambahan modulo untuk nilai $\dp$ nya. Ide tetap sama, soal ini menggunakan konsep *dynamic programming* dengan menggunakan $n$ sebagai *state*-nya, lakukan transisi yaitu

$$ \dp[i] = \dp[i - 1] + \dp[i - 2] + \cdots + \dp[i - k] $$

dengan base case $\dp[0] = 1$. Ide dari *dynamic programming* tersebut sebenarnya sederhana di mana setiap memasang manik hitam sebanyak $0$ hingga $k - 1$ kita letakkan manik putih terlebih dahulu sebagai sekat nya sehingga transisi yang dilakukan mulai dari $\dp[i - 1]$ hingga $\dp[i - k]$ dan $\dp[2000]$ akan bernilai 797495860.

---

> [!important] Pernyataan untuk Nomor 4–5
> Pak Dengklek memutuskan untuk merayakan gaji besarnya yang pertama dengan pergi ke restoran.
>
> Dia tinggal di dekat taman yang tidak biasa. Taman tersebut adalah pohon berakar yang terdiri dari $n$ simpul dengan akar di simpul 1. Simpul 1 juga berisi rumah Pak Dengklek. Sayangnya bagi pahlawan kita, taman tersebut juga terdapat anjing. Pak Dengklek sudah mengetahui simpul mana yang memiliki anjing di dalamnya.
>
> Simpul daun dari taman berisi restoran. Pak Dengklek ingin memilih restoran yang akan dia kunjungi, tetapi sayangnya dia sangat takut pada anjing, jadi tidak ada cara dia akan pergi ke restoran jika jalur dari restoran ke rumahnya mengandung lebih dari $m$ simpul berturut-turut dengan anjing.
>
> Tugas Anda adalah membantu Pak Dengklek menghitung jumlah restoran yang bisa dia kunjungi.

> [!question] Nomor 4
> Jika taman membentuk suatu _binary tree_ sempurna dengan total 1023 simpul (termasuk rumah Pak Dengklek), ada berapa banyak restoran yang tersedia?
>
> -   [ ] 256
> -   [ ] 258
> -   [x] **512**
> -   [ ] 128
> -   [ ] 126

Suatu *binary tree* sempurna memiliki $\frac{n+1}{2}$ *leaf*, sehingga terdapat 512 *leaf* atau restoran yang tersedia.

---

> [!question] Nomor 5
> Jika taman membentuk suatu line graph (1)—(2)—(3)—(4) dan seterusnya. Taman tersebut diketahui terdapat 1000 simpul. Jika setiap bilangan dengan banyak faktor genap terdapat anjing. Berapa nilai $m$ minimum agar Pak Dengklek dapat mengunjungi minimal 1 restoran?
>
> -   [ ] 63
> -   [ ] 62
> -   [ ] 61
> -   [x] **60**
> -   [ ] 59

Suatu bilangan memiliki banyak faktor ganjil jika bilangan itu merupakan bilangan kuadrat, dan sebaliknya genap jika bilangan tersebut bilangan bukan kuadrat. Sehingga, kita harus memastikan jarak bilangan kuadrat terbesar antara itu yaitu 900 dan 961 yang mana diantaranya akan terdapat 60 bilangan berurutan.

---

> [!important] Pernyataan untuk Nomor 6–7
> Pada OSN-P 2025 setiap peserta diberikan masing-masing sebanyak $n$ koin emas sebagai suatu tantangannya. Diketahui, dari $n$ koin emas tersebut terdapat 1 koin yang palsu. Koin palsu tersebut memiliki massa yang lebih ringan dibandingkan koin emas yang asli. Masing-masing peserta diberikan suatu neraca timbangan untuk mengecek manakah emas yang palsu. Pelatos sebagai salah satu murid unggulan tentunya mengerjakan tantangan tersebut dengan langkah paling optimal.

> [!question] Nomor 6
> Jika $n = 512$, berapa banyak penimbangan paling sedikit untuk mengetahui koin mana yang palsu?
>
> -   [ ] 511
> -   [ ] 256
> -   [ ] 9
> -   [x] **6**
> -   [ ] 3

Kita dapat melakukan operasi pembagian menjadi 3 bagian emas sehingga menyerupai algoritma *ternary search*. Sehingga, untuk jumlah 512 emas diperlukan 6 kali penimbangan saja untuk mengetahui emas mana yang palsu.

---

> [!question] Nomor 7
> Jika $n = 4096$, berapa banyak penimbangan paling sedikit untuk mengetahui koin mana yang palsu?
>
> -   [ ] 4095
> -   [ ] 2048
> -   [ ] 12
> -   [ ] 11
> -   [x] **9**

Seperti soal sebelumnya, hanya perlu dibagi menjadi 3 terus-menerus sehingga perlu 9 kali penimbangan saja.

---

> [!question] Nomor 8
> Pak Pelatos memiliki hobi dalam melukis. Pak Pelatos memiliki 3 buah palet yang menjadi kesayangannya. Palet pertama memiliki 3 warna, yaitu merah, biru, dan hijau. Palet kedua memiliki 4 warna, yaitu kuning, hijau, jingga, dan merah. Palet terakhir memiliki 5 warna, yaitu merah, biru, kuning, hijau, dan ungu.
>
> Pak Pelatos juga memiliki 5 buah kanvas yang belum memiliki warna pada awalnya. Berapa banyak konfigurasi warna pada kanvas jika Pak Pelatos memilih warna dari kanvas yang ia miliki dan Pak Pelatos hanya dapat memilih warna dari palet yang sama (jika kanvas 1 dari palet 1 maka kanvas 2–5 harus juga dari palet 1)?
>
> -   [x] **3906**
> -   [ ] 6930
> -   [ ] 9036
> -   [ ] 6039
> -   [ ] 3690

Gunakan prinsip inklusi-eksklusi untuk 3 palet yang ada, sehingga

$$ \begin{align*}
	&\quad P(A) + P(B) + P(C) - P(AB) - P(AC) - P(BC) + P(ABC) \\
	&= 5^5+4^5+3^5-3^5-3^5-2^5+2^5 \\
	&= 5^5+4^5-3^5 \\
	&= 3906.
\end{align*} $$

---

> [!question] Nomor 9
> Pelatos tersesat pada labirin yang menggunakan koordinat cartesius. Kebetulan, Pelatos sekarang berada pada titik $(0, 0)$ dan hanya dapat bergerak ke atas dan ke kanan. Hitunglah berapa banyak cara untuk mencapai titik $(5, 5)$ dari titik awal Pelatos?
>
> -   [x] **252**
> -   [ ] 504
> -   [ ] 126
> -   [ ] 1080
> -   [ ] 2160

Pada soal ini, untuk bergerak dari $(0, 0)$ ke $(5, 5)$ perlu dilakukan 5 gerakan ke kanan dan juga 5 gerakan ke atas. Tentunya jika begitu kita hanya perlu mengacak untuk 10 gerakan tersebut. Kita dapat anggap masing-masing dari 5 gerakan tersebut ialah string `KKKKKAAAAA` sehingga hanya perlu dihitung sebagai

$$ \frac{10!}{5! \times 5!} = 252 $$

karena ada 10 karakter dengan masing-masing 5 karakter kembar.

---

> [!question] Nomor 10
> Setelah menebak angka, sekarang peserta perlu menghitung berapa banyak kemungkinan untuk mengisi suatu lantai berukuran 1x15. Lantai dapat diisi dengan ubin-ubin berukuran 1x1, 1x2, dan 1x4.
>
> -   [ ] 2890
> -   [x] **2809**
> -   [ ] 3430
> -   [ ] 3403
> -   [ ] 1024

Dapat dilakukan *dynamic programming* dengan transisi

$$ \dp[i] = \dp[i - 1] + \dp[i - 2] + \dp[i - 4]. $$

Base case dari $\dp$ nya ialah ketika belum ada ubin sama sekali yang terpasang sehingga $\dp[0] = 1$. Sehingga, untuk $\dp[15] = 2809$.

---

> [!question] Nomor 11
> Berapakah banyak 0 di belakang 4045 faktorial?
>
> -   [x] **1009**
> -   [ ] 1010
> -   [ ] 1011
> -   [ ] 1012
> -   [ ] 1008

Kita hanya perlu menghitung

$$ \begin{align*}
	&\quad
		\left\lfloor\frac{4045}{5}\right\rfloor
		+ \left\lfloor\frac{4045}{25}\right\rfloor
		+ \left\lfloor\frac{4045}{125}\right\rfloor
		+ \left\lfloor\frac{4045}{625}\right\rfloor
		+ \left\lfloor\frac{4045}{3125}\right\rfloor \\
	&= 1009.
\end{align*} $$

---

> [!question] Nomor 12
> Evan membutuhkan pencahayaan yang maksimal untuk belajarnya, diketahui iya memerlukan semua lampu untuk menyala agar belajar yang ia lakukan maksimal. Namun, saklar di rumahnya sedikit unik dimana jika suatu saklar dipencet, akan berpengaruh tidak hanya pada saklar tersebut saja tapi juga untuk semua saklar dengan angka lebih besar dari yang diubah tersebut. Hitunglah berapa operasi minimum yang perlu dilakukan jika pada awalnya kondisi lampu seperti berikut!
>
> ![[OSA-P 2025 Sesi 1 Nomor 12.png]]
>
> -   [ ] 13
> -   [ ] 12
> -   [ ] 11
> -   [ ] 10
> -   [x] **9**

Setiap operasi saklar akan menyalakan setiap lampu yang memiliki angka lebih besar atau sama dengan saklar. Maka kita perlu menyalakan setiap lampu dari yang paling kecil agar saat merubah yang besar, angka-angka sebelumnya yang telah diubah tidak akan terpengaruh. Sehingga dapat dihitung bahwa operasi yang paling optimal ialah 9 operasi 1, 2, 4, 5, 6, 8, 11, 12, lalu 14.

---

> [!question] Nomor 13
> Setiap Pelatos diberikan 10 pasang tanda kurung `()`. Diketahui bahwa tanda-tanda kurung tersebut disusun secara bebas asalkan setiap `)` harus didahului oleh tanda `(`. Contoh susunan yang valid adalah `()()` dan `(())`. Sedangkan `)(()` dan `)()(` merupakan susunan yang tidak valid. Dari informasi yang beredar, setiap Pelatos menyusun tanda-tanda kurung tersebut dengan susunan yang berbeda. Berapa pelatos maksimal yang ikut berpartisipasi?
>
> -   [ ] 15796
> -   [ ] 16786
> -   [x] **16796**
> -   [ ] 19576
> -   [ ] 17956

Untuk 4 soal ini merupakan soal dengan penyelesaian kombinatorik *dynamic programming* ataupun Catalan *number*. Sehingga Catalan *number* ke-10 ialah 16796.

---

> [!question] Nomor 14
> Terdapat 2025 orang dengan pernyataan yang berbeda-beda.
>
> -   Orang pertama berkata 1 orang berkata bohong.
> -   Orang kedua berkata 2 orang berkata bohong.
> -   ⋮
> -   Orang ke-2025 berkata 2025 orang berkata bohong.
>
> Orang keberapa yang dipastikan jujur?
>
> -   [ ] 1013
> -   [ ] 1012
> -   [ ] 2025
> -   [x] **2024**
> -   [ ] 1

Tidak mungkin ada 2 orang atau lebih yang jujur karena semua pernyataan saling berlawanan sehingga benar ada tepat 1 orang yang jujur dan yang lainnya berbohong jadi jawabannya 2024.

---

> [!question] Nomor 15
> Dari 100000 buah bilangan bulat positif pertama, berapa banyak bilangan yang mengandung tepat 1 buah angka 2, 1 buah angka 4, dan 1 buah angka 6?
>
> -   [ ] 2490
> -   [x] **2940**
> -   [ ] 4920
> -   [ ] 4290
> -   [ ] 9420

Anggap dari 5 digit yang ada nanti ketika dibawah 5 digit-digit depan adalah 0. Dapat dianggap bahwa 3 angka pertama ada $5 \times 4 \times 3$ cara untuk mengisinya. Dan untuk 2 angka terakhir ada 7 angka yang dapat digunakan secara berulang mulai dari 0, 1, 2, 6, 7, 8, dan 9, sehingga hasilnya adalah 2940.

---

> [!question] Nomor 16
> Berapakah penjumlahan dari 2 digit terakhir penjumlahan berikut?
> $$1! + 2! + 3! + \cdots + 2023! + 2024!$$
>
> -   [ ] 8
> -   [ ] 12
> -   [x] **4**
> -   [ ] 6
> -   [ ] 10

Hitung saja 2 digit terakhir pada

$$ 1! + 2! + 3! + \cdots + 9! $$

karena pada $10!$ (dan seterusnya) dua digit terakhirnya adalah 00. Ditemukan 13 sebagai 2 digit terakhirnya, maka $1 + 3 = 4$.

---

# Sesi 2

> [!info] Detail
>
> -   **Tipe:** Benar/salah.
> -   **Jumlah:** 5 soal, 4 subsoal per soal.
> -   **Waktu:** 30 menit.
> -   **Penilaian:**
>     -   Benar: +1
>     -   Kosong: 0
>     -   Salah: 0

> [!question] Nomor 1
> Pak Dengklek menyukai angka keberuntungan. Semua orang tahu bahwa angka keberuntungan adalah bilangan bulat positif yang representasi desimalnya hanya mengandung digit keberuntungan 4 dan 7. Sebagai contoh, angka 47, 744, dam 4 adalah angka keberuntungan. Tetapi 5, 17, dan 467 bukan.
>
> Pak Dengklek menyebut sebuah angka hampir beruntung jika dapat dibagi habis oleh beberapa angka keberuntungan. Bantu dia untuk menentukan apakah angka $n$ yang diberikan beruntung atau hampir beruntung di mana $n \leq 1000$.
>
> |  B  |  S  | Pernyataan                                            |
> | :-: | :-: | ----------------------------------------------------- |
> |     |  ✓  | 777 adalah angka beruntung/hampir beruntung terbesar. |
> |  ✓  |     | Terdapat tepat 2 bilangan prima yang beruntung.       |
> |     |  ✓  | Terdapat tepat 3 bilangan prima yang beruntung.       |
> |  ✓  |     | 987 adalah bilangan beruntung/hampir beruntung.       |

- Angka 1000 adalah $n$ terbesar yang beruntung/hampir beruntung.
- Terdapat 2 bilangan prima yang beruntung yaitu 7 dan 47.
- Angka 987 termasuk bilangan beruntung/hampir beruntung karena habis dibagi 7.

---

> [!question] Nomor 2
> Seorang insinyur robotik sedang merancang robot eksplorasi untuk menjelajah labirin persegi berukuran $n \times n$. Robot memulai dari pojok kiri atas $(0, 0)$ dan harus mencapai pojok kanan bawah $(n − 1, n − 1)$. Robot hanya dapat bergerak ke kanan atau ke bawah. Beberapa petak merupakan dinding dan tidak bisa dilewati. Labirin diberikan dalam bentuk peta grid.
>
> |  B  |  S  | Pernyataan                                                                                                                                                           |
> | :-: | :-: | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
> |  ✓  |     | Jika tidak ada dinding, maka jumlah jalur berbeda yang dapat diambil oleh robot dari $(0, 0)$ ke $(n - 1, n - 1)$ adalah $\mathrm{C}_{n - 1}^{2n - 2}$.                    |
> |     |  ✓  | Menambahkan satu petak dinding di tengah dapat mengurangi jumlah jalur tepat satu.                                                                                   |
> |  ✓  |     | Algoritma pencarian seperti _depth-first search_ atau _backtracking_ dapat digunakan untuk menghitung jumlah semua jalur valid.                                      |
> |  ✓  |     | Jumlah jalur dari kiri atas ke kanan bawah dapat dihitung menggunakan metode _dynamic programming_ dengan kompleksitas waktu $O(n^2)$ jika semua sel bebas hambatan. |

Menambahkan penghalang di tengah tidak mengurangi satu jalur, tetapi banyak jalur menuju dinding tersebut dan banyak jalur dari dinding tersebut ke tujuan.

---

> [!question] Nomor 3
> Permainan Menara Hanoi biasanya dimainkan dengan 3 tiang. Namun, seorang peneliti tertarik pada versi dengan 4 tiang, di mana cakram harus dipindahkan dari tiang pertama ke tiang keempat dengan aturan yang sama: satu cakram dipindahkan dalam satu waktu, dan cakram lebih besar tidak boleh diletakkan di atas cakram lebih kecil.
>
> |  B  |  S  | Pernyataan                                                                                                  |
> | :-: | :-: | ----------------------------------------------------------------------------------------------------------- |
> |     |  ✓  | Untuk 4 tiang, sudah ada rumus pasti untuk langkah minimum secara umum.                                     |
> |  ✓  |     | Untuk tiga tiang, jumlah minimum langkah yang diperlukan adalah $2^n - 1$ di mana $n$ adalah banyak cakram. |
> |  ✓  |     | Penambahan tiang dapat menurunkan jumlah langkah minimum.                                                   |
> |  ✓  |     | Algoritma berbasis _dynamic programming_ digunakan dalam mencari solusi optimal dengan 4 tiang.             |

Sampai sekarang tidak ada rumus pasti untuk 4 tiang. Pernyataan lainnya sudah benar.

---

> [!question] Nomor 4
> Suatu wilayah terdiri dari $n$ kota yang ingin dihubungkan dengan jaringan transmisi energi. Setiap jaringan (kabel) memiliki biaya pemasangan. Pemerintah ingin menghemat biaya dengan hanya memasang jaringan sesedikit mungkin, tetapi tetap menjamin bahwa semua kota bisa saling terhubung (langsung atau tak langsung).
>
> Untuk efisiensi distribusi energi, ada pula bobot keandalan pada tiap kabel, yang menunjukkan seberapa andal kabel itu dalam kondisi ekstrem (misalnya badai). Pemerintah ingin memilih jaringan transmisi yang
>
> -   menghubungkan semua kota;
> -   memiliki biaya total minimum; serta
> -   di antara semua jaringan dengan biaya minimum, pemerintah ingin memilih yang paling andal, yaitu jumlah total bobot keandalan paling tinggi.
>
> Jaringan direpresentasikan sebagai graf tak berarah berbobot ganda. Setiap sisi memiliki bobot biaya dan keandalan.
>
> |  B  |  S  | Pernyataan                                                                                                                                     |
> | :-: | :-: | ---------------------------------------------------------------------------------------------------------------------------------------------- |
> |  ✓  |     | Algoritma Kruskal dengan prioritas utama pada bobot biaya dapat digunakan untuk mencari solusi awal berupa _minimum spanning tree_.            |
> |  ✓  |     | Jika terdapat lebih dari satu _minimum spanning tree_ dengan biaya total yang sama, maka kita dapat memilih berdasarkan bobot keandalan.       |
> |     |  ✓  | Algoritma Djikstra lebih cocok untuk menyelesaikan masalah ini karena mempertimbangkan bobot dan jalur terpendek.                              |
> |  ✓  |     | Struktur data _disjoint set union_ sangat berguna untuk mendeteksi siklus saat membangun _minimum spanning tree_ menggunakan Algoritma Kruskal |

Algoritma Dijkstra digunakan untuk jalur terpendek dari satu titik ke titik yang lain, bukan *spanning tree*.

---

> [!question] Nomor 5
> Sebuah pusat distribusi di kota Metrix menggunakan sistem penataan otomatis untuk mengurutkan kontainer sebelum dikirim ke pelanggan. Setiap kontainer memiliki nomor unik dari 1 hingga $n$, dan seluruh kontainer awalnya tersusun dalam urutan acak di sepanjang lintasan konveyor.
>
> Sistem hanya dapat melakukan pertukaran dua kontainer bersebelahan sekaligus dalam satu langkah. Tujuan sistem adalah menata ulang kontainer sehingga nomornya tersusun secara menaik, dari 1 sampai $n$, dengan jumlah pertukaran minimum.
>
> Karena keterbatasan waktu proses, teknisi sistem ingin menghitung seberapa cepat sistem bisa menyelesaikan tugas tersebut, dan sedang mempertimbangkan berbagai pendekatan algoritmis serta analisis teoritis.
>
> |  B  |  S  | Pernyataan                                                                                     |
> | :-: | :-: | ---------------------------------------------------------------------------------------------- |
> |  ✓  |     | Fenwick Tree dan Segment Tree bisa digunakan untuk menghitung jumlah _inversion_ pada _array_. |
> |  ✓  |     | Jumlah pertukaran minimum yang dilakukan sama dengan jumlah _inversion_ pada _array_.          |
> |     |  ✓  | Algoritma _bubble sort_ yang dilakukan memiliki kompleksitas terburuk $O(n \log n)$.           |
> |     |  ✓  | Jumlah pertukaran maksimal adalah $n^2$.                                                       |

Algoritma bubble sort memiliki worst case $O(n^2)$. Jumlah maksimal *swap* adalah $\frac{1}{2} (n-1)n$.

---

> [!question] Nomor 6
> Sebuah perusahaan ekspedisi di kota Techvalley sedang mengembangkan sistem pengambilan keputusan otomatis untuk menentukan barang mana saja yang harus dimasukkan ke dalam satu kendaraan pengantar.
>
> Terdapat $n$ buah barang, masing-masing dengan berat dan nilai ekonomi berbeda. Setiap kendaraan memiliki kapasitas maksimum $W$ (dalam satuan berat). Tujuan sistem adalah memilih kombinasi barang yang memaksimalkan nilai total tanpa melebihi kapasitas kendaraan.
>
> Karena ribuan pengambilan keputusan ini harus dilakukan setiap jam, insinyur perusahaan ingin tahu apakah strategi _greedy_ cukup baik, atau apakah harus menggunakan algoritma dinamis yang lebih kompleks.
>
> |  B  |  S  | Pernyataan                                                                                                                                                    |
> | :-: | :-: | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
> |  ✓  |     | Penyelesaian terbaik untuk _knapsack_ adalah _dynamic programming_.                                                                                           |
> |     |  ✓  | Strategi _greedy_ berdasarkan rasio nilai/berat selalu memberikan solusi optimal untuk _knapsack_.                                                            |
> |  ✓  |     | Kompleksitas waktu dari solusi _dynamic programming_ konvensional adalah $O(n \times W)$, di mana $n$ adalah banyak barang dan $W$ adalah kapasitas maksimum. |
> |  ✓  |     | Jika seluruh berat barang kelipatan bilangan tetap (misalnya 5), maka kita bisa melakukan kompresi state untuk menghemat memori dalam _dynamic programming_.  |

Tidak semua soal penyelesaian *dynamic programming* bisa diselesaikan dengan pendekatan Greedy.

---

# Sesi 3

> [!info] Detail
>
> -   **Tipe:** Pilihan ganda.
> -   **Jumlah:** 10 soal.
> -   **Waktu:** 60 menit.
> -   **Penilaian:**
>     -   Benar: +1
>     -   Kosong: 0
>     -   Salah: 0
> -   **Skor:** 10/15 (66.67%)

> [!important] Pernyataan untuk Nomor 1–3
> Perhatikan potongan kode berikut.
>
> ```cpp
> long long air(long long api, long long panas) {
> 	if (api == 0 || panas == 0) {
> 		return 1;
> 	}
>
> 	return air(api - 1, panas) + air(api, panas - 1);
> }
> ```

> [!question] Nomor 1
> Tentukan keluaran dari `air(3, 3)`.
>
> -   [x] **20**
> -   [ ] 6
> -   [ ] 12
> -   [ ] 30
> -   [ ] 18

Kita perlu mengetahui bahwa sejatinya soal ini merupakan *code dynamic programming bottom-up* yang tidak dimemoisasi, sehingga kita perlu membuat memoisasi tersendiri dengan transisi

$$ \dp[i][j] = \dp[i - 1][j] + \dp[i][j - 1] $$

dengan *base case* untuk masing-masing $i = 0$ dan $j = 0$,

$$ \dp[i][0] = 1, $$

$$ \dp[0][j] = 1, $$

dan ditemukan untuk $\dp[3][3] = 20$.

---

> [!question] Nomor 2
> Tentukan keluaran dari `air(6, 8)`.
>
> -   [ ] 1001
> -   [ ] 2002
> -   [x] **3003**
> -   [ ] 4004
> -   [ ] 5005

Sama dengan soal sebelumnya, ditemukan untuk $\dp[6][8] = 3003$. Transisi $\dp$ ini juga dapat dihitung dengan matematika, yaitu $\mathrm{C}_8^{8+6} = \mathrm{C}_8^{14} = 3003$.

---

> [!question] Nomor 3
> Tentukan keluaran dari `air(9, 5)`.
>
> -   [ ] 1001
> -   [ ] 2002
> -   [ ] 3003
> -   [ ] 4004
> -   [x] **5005**

Sama dengan soal sebelumnya, ditemukan untuk $\dp[9][5] = 2002$. Transisi $\dp$ ini juga dapat dihitung dengan matematika, yaitu $\mathrm{C}_5^{5+9} = \mathrm{C}_5^{14} = 2002$.

---

> [!question] Nomor 4
> Pak Dengklek sedang berlatih mengerjakan soal _binary search_ klasik karena ia akan mengikuti OSN-P 2040. Berikut adalah program yang ia buat.
>
> ```cpp
> #include <bits/stdc++.h>
> using namespace std;
>
> int main()
> {
> 	int N;
> 	cin >> N;
>
> 	int arr[N + 1];
> 	for (int i = 1; i <= N; i++)
> 		cin >> arr[i];
>
> 	int cari;
> 	cin >> cari;
>
> 	int kiri = 1;
> 	int kanan = N;
>
> 	bool ketemu = false;
>
> 	while (kiri <= kanan) {
> 		int tengah = (kiri + kanan) / 2;
>
> 		if (arr[tengah] == cari) {
> 			ketemu = true;
> 			break;
> 		} else if (arr[tengah] < cari) {
> 			kiri = tengah + 1;
> 		} else {
> 			kanan = tengah - 1;
> 		}
> 	}
>
> 	if (ketemu == false)
> 		cout << "Tidak ada\n";
> 	else
> 		cout << "Ada\n";
> }
> ```
>
> Namun program yang ia buat sering membuat kesalahan output. Program tersebut bisa mengoutput `Tidak ada` saat bilangan yang dicari sebenarnya ada dalam barisan tersebut. Baris apa yang seharusnya ditambahkan Pak Dengklek?
>
> -   [ ] `sort(arr, arr+N);`
> -   [x] **`sort(arr+1, arr+N+1);`**
> -   [ ] `sort(arr, arr+N, greater<int>());`
> -   [ ] `sort(arr+1, arr+N+1, greater<int>());`
> -   [ ] Tidak ada yang perlu ditambah, tetapi ada baris yang kurang tepat

Untuk menggunakan *binary search*, isi *array* harus terlebih dahulu diurutkan dari terkecil ke terbesar. Selain itu, *index array* yang diakses pada program tersebut adalah dari $1$ sampai $N$. Karena itu, diperlukan *function* `sort`, yaitu `sort(arr + 1, arr + N + 1)`.

Kode `sort(arr, arr+N)` hanya mengurutkan isi `arr[0]` hingga `arr[N-1]`.

---

> [!question] Nomor 5
> Pak Dengklek sedang membuat program untuk mencari banyaknya pasangan $(i, j)$ dengan $0 \leq i < j < N$ di mana $A_i \times A_j = A_i \mathbin{\text{or}} A_j$. Berikut adalah perintah program yang ia buat.
>
> ```cpp
> #include <bits/stdc++.h>
> using namespace std;
>
> int main()
> {
> 	int N;
> 	cin >> N;
>
> 	int A[N];
> 	for (int i = 0; i < N; i++)
> 		cin >> A[i];
>
> 	long long ans = 0;
> 	for (int i = 0; i < N; i++) {
> 		for (int j = i + 1; j < N; j++) {
> 			if (A[i] * A[j] == A[i] | A[j]) {
> 				ans++;
> 			}
> 		}
> 	}
>
> 	cout << ans << endl;
> 	return 0;
> }
> ```
>
> Namun, ketika ia mencoba untuk menjalan program tersebut, ia mendapatkan hasil yang tidak sesuai dengan jawaban yang sesungguhnya. Bantu Pak Dengklek untuk menentukan pada baris keberapa Pak Dengklek perlu memperbaiki programnya!
>
> -   [ ] 14
> -   [ ] 15
> -   [x] **16**
> -   [ ] 17
> -   [ ] Tidak ada yang perlu diperbaiki

Sesuai dengan *operator precedence*, operasi `==` akan dilakukan terlebih dahulu sebelum operasi `|`. Oleh karena itu, operasi tidak akan berjalan sesuai dengan yang diharapkan. Jadi, baris yang perlu kita perbaiki adalah baris ke-16.

---

> [!question] Nomor 6
> Hewan-hewan di hutan baru saja belajar bagaimana cara _coding_ menggunakan C++. Bersama-sama mereka membuat dua buah fungsi seperti berikut.
>
> ```cpp
> long long kucing(long long sapi, long long kerbau, long long beruang)
> {
> 	while (sapi >= beruang)
> 		sapi -= beruang;
>
> 	for (int i = 0; i < (kerbau / beruang); i++)
> 		kerbau = kerbau - beruang;
>
> 	return (sapi * kerbau) % beruang;
> }
>
> long long cantik(long long kuda, long long nil, long long berenang)
> {
> 	if (nil == 0)
> 		return 1;
>
> 	long long suka = cantik(kuda, nil >> 1, berenang);
> 	suka = kucing(suka, suka, berenang);
>
> 	if (nil & 1)
> 		return kucing(suka, kuda, berenang);
>
> 	return suka;
> }
> ```
>
> Singa Sang Raja Hutan pusing membaca program mereka, ia hanya ingin tahu berapa nilai keluaran dari `cantik(5, 7, 30)`. Dapatkah Anda membantu sang singa untuk menemukan jawabannya?
>
> -   [ ] 0
> -   [x] **5**
> -   [ ] 15
> -   [ ] 25
> -   [ ] Tidak ada keluaran

Perhatikan bahwa sebenarnya pada fungsi `kucing` yang kita lakukan hanyalah melakukan perkalian antara variabel `sapi` dan kerbau `kemudian` memodulokan dengan `beruang`.

Kemudian, fungsi `cantik` sebenarnya adalah fungsi *fast exponentiation* atau *modular exponentiation* (modex). Sehingga, `cantik(5, 7, 30)` artinya kita hanya perlu mencari $5^7 \bmod 30$, yaitu 5.

---

> [!question] Nomor 7
> Perhatikan potongan program berikut ini.
>
> ```cpp
> #include <bits/stdc++.h>
> using namespace std;
>
> int main()
> {
> 	int babi, sapi;
> 	std::cin >> babi >> sapi;
>
> 	while (babi != sapi) {
> 		if (babi > sapi) {
> 			int kuda = babi;
> 			babi = sapi;
> 			sapi = kuda;
> 		}
>
> 		sapi -= babi;
> 	}
>
> 	std::cout << babi << std::endl;
> }
> ```
>
> Berapakah keluaran jika masukannya adalah `17266 60431`?
>
> -   [ ] 1
> -   [ ] 89
> -   [ ] 97
> -   [x] **8633**
> -   [ ] Program tidak akan berakhir

Ingat *Euclidean algorithm*, $\mathrm{fpb}(A, B) = \mathrm{fpb}(A - B, B)$. Karena sifat ini, kita bisa simpulkan bahwa aslinya program ini adalah program mencari FPB. Jadi kesimpulannya, kita hanya perlu mencari FPB dari 17266 dan 60431, yang nilainya adalah 8633.

---

> [!question] Nomor 8
> Evan sedang membuat program untuk menghitung kombinasi. Berikut adalah potongan program yang telah ia buat.
>
> ```cpp
> const int LIM = 1e6;
> const int MOD = 1e9 + 7;
>
> long long fact[LIM + 5], invfact[LIM + 5];
>
> long long multiply(long long A, long long B)
> {
> 	return ((A % MOD) * (B % MOD)) % MOD;
> }
>
> long long modex(long long base, long long pow)
> {
> 	if (pow == 0)
> 		return 1;
> 	if (pow == 1)
> 		return base % MOD;
>
> 	long long res = modex(base, pow / 2);
>
> 	res = multiply(res, res);
> 	if(pow & 1) res = multiply(res, base);
>
> 	return res;
> }
>
> long long inv(long long x)
> {
> 	return modex(x , MOD - 2);
> }
>
> void pre_compute()
> {
> 	fact[0] = 1;
>
> 	for (int i = 1; i <= LIM; i++) {
> 		fact[i] = multiply(fact[i - 1], i);
> 	}
>
> 	for (int i = 1; i <= LIM; i++) {
> 		invfact[i] = inv(fact[i]);
> 	}
> }
>
> long long combinaton(long long n, long long r)
> {
> 	long long penyebut = multiply(invfact[r], invfact[n - r]);
> 	return multiply(fact[n], penyebut);
> }
> ```
>
> Namun, ketika Evan mencoba menggunakan fungsi `combination(977, 977)`, ia mendapatkan keluaran `0`, seharusnya $\mathrm{C}_{977}^{977} = 1$. Bantulah Evan untuk menentukan baris berapa yang menjadi sumber bug!
>
> -   [ ] 4
> -   [ ] 21
> -   [ ] 28
> -   [x] **39**
> -   [ ] 46

Masalah timbul pada baris ke-33, karena `invfact[0]` tidak diisi dan masih mempunyai *default value* yaitu 0. Jika `invfact[0]` mempunyai nilai 0, perhitungan $\mathrm{C}_{997}^{997}$ akan memiliki bug karena kita perlu mengakses `invfact[997 - 997]`, atau `invfact[0]`.

---

> [!important] Pernyataan untuk Nomor 9–10
> Perhatikan potongan kode berikut.
>
> ```cpp
> long long mod = 1e9 + 7;
>
> long long f(long long b, long long e) {
> 	long long res = 1;
>
> 	while (e > 0) {
> 		if (e & 1)
> 			res *= b;
> 		res %= mod;
> 		b *= b;
> 		b %= mod;
> 		e = e >> 1;
> 	}
>
> 	return res;
> }
> ```

> [!question] Nomor 9
> Berapakah hasil pemanggilan `f(2, 10)`?
>
> -   [ ] 2048
> -   [x] **1024**
> -   [ ] 512
> -   [ ] 256

Kode tersebut adalah potongan kode *binary exponentiation*, sehingga $2^{10} = 1024$.

---

> [!question] Nomor 10
> Berapakah hasil pemanggilan `f(2, 29)`?
>
> -   [x] **536870912**
> -   [ ] 53679012
> -   [ ] 53679102
> -   [ ] 50367912

Kode tersebut adalah potongan kode *binary exponentiation*, sehingga $2^{29} = 536870912$.