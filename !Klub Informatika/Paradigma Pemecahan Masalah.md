---
sources:
  - https://drive.google.com/file/d/1xP65xczwD8UxNe2PIxkQh_UZe31TAkO1/view
  - https://drive.google.com/file/d/129gzJ1SoPGuIEcZNUwV7ILJoMUngb2bo/view
---

> [!question]
> Terdapat 8 buah lampu yang berjejer dari kiri ke kanan yang dilabeli A, B, C, D, E, F, G, dan H. Pada awalnya, semua lampu dalam kondisi mati.
> 
> Ada 10 bebek Pak Dengklek yang ingin bermain dengan lampu-lampu tersebut. Diketahui bahwa masing-masing dari mereka memiliki lampu favorit yang ditandai dengan ✓ pada tabel berikut.
> 
> | Bebek |  A  |  B  |  C  |  D  |  E  |  F  |  G  |  H  |
> | :---: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
> |   1   |  ✓  |     |  ✓  |  ✓  |     |  ✓  |     |  ✓  |
> |   2   |     |  ✓  |  ✓  |     |  ✓  |     |  ✓  |  ✓  |
> |   3   |  ✓  |     |     |  ✓  |     |  ✓  |     |  ✓  |
> |   4   |     |  ✓  |  ✓  |     |     |  ✓  |  ✓  |     |
> |   5   |  ✓  |     |  ✓  |     |  ✓  |  ✓  |     |     |
> |   6   |     |     |  ✓  |  ✓  |     |  ✓  |  ✓  |  ✓  |
> |   7   |  ✓  |  ✓  |     |  ✓  |  ✓  |     |  ✓  |  ✓  |
> |   8   |  ✓  |  ✓  |     |     |  ✓  |     |  ✓  |     |
> |   9   |     |  ✓  |     |  ✓  |  ✓  |     |     |     |
> |  10   |  ✓  |     |  ✓  |     |     |  ✓  |  ✓  |     |
> 
> Pak Dengklek hanya memliki 9 dari 10 bebeknya. Untuk setiap bebek yang terpilih, ia akan membalikkan seluruh status lampu-lampu favoritnya.
> 
> Jika pada kondisi akhir, hanya lampu A dan G yang menyala, bebek nomor berapa yang tidak dipilih oleh Pak Dengklek?

Jika semua bebek dipilih, maka diketahui status-status lampu sebagai berikut. Untuk setiap-setiap lampu, jika jumlah bebeknya genap, maka status akhir lampu mati; jika jumlah bebeknya ganjil, maka lampu menyala.

|          |   A   |   B   |  C  |   D   |   E   |  F  |   G   |   H   |
| -------: | :---: | :---: | :-: | :---: | :---: | :-: | :---: | :---: |
| Sekarang |       |   ✓   |     |   ✓   |   ✓   |     |       |   ✓   |
|   Target |   ✓   |       |     |       |       |     |   ✓   |       |
|  **XOR** | **✓** | **✓** |     | **✓** | **✓** |     | **✓** | **✓** |

Agar hanya lampu A dan G yang menyala, kita perlu meninggalkan bebek yang menyukai A, B, D, E, G, dan H. Yaitu bebek nomor 7.

> [!done] Answer
> Bebek nomor 7.

---

> [!question] 
> Dalam sebuah pertandingan sepak bola, terdapat beberapa tim yang saling bertanding satu sama lain. Tim-tim tersebut diberi indeks berupa huruf alfabet (A–Z), dan setiap pasang tim akan saling bertanding tepat satu kali. Dalam setiap pertandingan, tim yang menang (tim yang mencetak gol lebih banyak) akan mendapatkan 3 poin. Jika ternyata pertandingan berakhir seri, maka kedua tim mendapatkan 1 poin.
> 
> Anda akan diberikan hasil beberapa pertandingan. Tugas Anda adalah menentukan tim mana yang memimpin klasemen (tim dengan poin tertinggi). Jika ada lebih dari satu tim yang memiliki poin tertinggi, pilih tim dengan indeks terkecil secara alfabetis.
> 
> Diketahui bahwa di seluruh pertandingan hasilnya adalah sebagai berikut.
> 
> - Jika indeks kedua tim sama-sama vokal atau sama-sama konsonan, tim dengan indeks terkecil secara alfabetis selalu menang.
> - Jika indeks salah satu vokal dan yang lain konsonan, maka pertandingan seri.
> 
> Tim manakah yang memimpin klasemen?

| Tim    | Vokal    | Konsonan | Total  |
| ------ | -------- | -------- | ------ |
|        | *menang* | *seri*   |        |
| A (1)  | 4 × 3    | 21       | **33** |
| E (5)  | 3 × 3    | 21       | **30** |
| ⋮      |          |          |        |
| U (21) | 0 × 3    | 21       | **21** |

| Tim    | Vokal  | Konsonan | Total  |
| ------ | ------ | -------- | ------ |
|        | *seri* | *menang* |        |
| B (2)  | 5      | 20 × 3   | **65** |
| C (3)  | 5      | 19 × 3   | **62** |
| ⋮      |        |          |        |
| J (10) | 5      | 11 × 3   | **38** |
| ⋮      |        |          |        |
| Z (26) | 5      | 0 × 3    | **5**  |

Didapat semakin kebelakang, skor masing-masing vokal dan konsonan semakin menurun. Kita perlu mengecek vokal dan konsonan pertama, yaitu A dan B.

> [!done] Answer
> Tim B.

---

> [!question] 
> Beaver wants to buy a pair of shoes. All the shoes have a different size and width. Beaver will have to try on shoes until he finds a pair which is the right size and width.
> 
> Whenever he tries on a shoe, he can feel both
> 
> - if it is too wide, the right width, or too narrow; and
> - if it is too big, the right size, or too small.
> 
> The shoes in the store are arranged in increasing order of size (A–H) and width (1–8).
> 
> Beaver uses a method that guarantees that he will know which shoe size fits him in $n$ tries, even if he hasn't tried the shoe that fits yet.
> 
> What is the smallest possible value of $n$?

---

> [!question] 
> Kitty dan Dogo sedang melakukan ekspedisi ke bulan. Sesampainya di sana, terdapat tambang emas yang dinyatakan dalam sebuah peta seperti tabel berikut.
> 
> |     |     |     |     |     |
> | --- | --- | --- | --- | --- |
> | 10  | 8   | 6   | 8   | 9   |
> | 3   | 4   | 14  | 1   | 6   |
> | 🐱  | 16  | 5   | 15  | 0   |
> | 🐶  | 11  | 13  | 0   | 11  |
> 
> Angka pada setiap sel menunjukkan banyaknya emas pada sel tersebut. Ketika sel tersebut sudah dilalui, maka banyaknya emas di sel tersebut menjadi 0;
> 
> Ketika Kitty memilih suatu arah, maka Dogo akan mengikuti. Perlu dicatat, Dogo selalu berada di bawah Kitty.
> 
> Rute mana yang membuat Dogo mengumpulkan emas lebih banyak dari Kitty?
> 
> - [ ] →→→↑
> - [ ] →↑↑→
> - [ ] →→↑→
> - [ ] →→↑↑

| Rute | Kitty | Dogo |
| :--: | :---: | :--: |
| →→→↑ |  37   |  24  |
| →↑↑→ |  34   |  25  |
| →→↑→ |  36   |  39  |
| →→↑↑ |   –   |  –   |

> [!done] Answer
> →→↑→.

---

> [!question] 
> Standard paper sizes can be deduced from the size of paper size A0 by splitting it in half one or more times.
> 
> When A0 is split in half, it becomes A1. When A1 is split in half, it becomes A2. And so on.
> 
> We have eight sheets of paper, that is paper size A1, A2, A3, A4, A5, A6, A7, and A8.
> 
> We would like to produce 19 business cards with the size of A8.
> 
> We don't want to waste paper, so we only use complete sheets.
> 
> Which entire sheets must we use?
> 
> - [ ] A4, A7, and A8.
> - [ ] A5, A6, and A8.
> - [ ] A3 and A7.
> - [ ] A4 and A6.

| Size | A8 produced |
| ---- | ----------- |
| A7   | $2$         |
| A6   | $2^2$       |
| A5   | $2^3$       |
| ⋮    |             |
| A0   | $2^8$       |

As we can see, the paper sizes form the pattern of binary number. So by converting 19 into binary, we get 10011. From left to right A8 to A0. Therefore

| A4  | A5  | A6  | A7  | A8  |
| :-: | :-: | :-: | :-: | :-: |
|  ✓  |     |     |  ✓  |  ✓  |

> [!done] Answer
> A4, A7, and A8.

---

> [!question] 
> On a TV show in Germany, contestants have to solve many interesting puzzles. One of these problems is to ind a word in a grid like the one below, where all the letters are different.
> 
> |     |     |     |
> | :-: | :-: | :-: |
> |  L  |  E  |  H  |
> |  C  |     |  D  |
> |  R  |  I  |  N  |
> 
> The contestants choose one of the eight letters as a starting point. Then they have to create a word of exactly eight letters by performing seven consecutive knight's moves (2×1 or 1×2). A letter in the grid has to be visited *exactly* once.
> 
> How many eight-letter combinations can be found using this way?

Choose a starting letter, for example R. We could choose 2 letter after that, E and D. Let's choose E, we couldn't go back to R, so we only have one letter, that is N. After that, we also get one choice until the eighth letter.

So for every letter, there's only 2 choices. Since there are 8 letters, therefore there are 8×2 choices.

> [!done] Answer
> 16 choices.

---

> [!question] 
> Terdapat meja lingkar yang terletak 9 piring di pinggir-pinggirnya. Yang di mana piring-piring tersebut searah jarum jam berukuran 6, 4, 5, 1, 5, 3, 5, 3, dan 2.
> 
> Sebagai karyawan restoran, Pak Dengklek akan mengambil seluruh piring tersebut untuk dicuci. Karena alasan keselamatan kerja, Pak Dengklek harus mengambil piring dari yang ukurannya paling besar sehingga piring yang diambil harus urut dari ukuran 6 hingga 1. Setiap berpindah untuk mengambil piring lain yang bersebelahan membutuhkan satu langkah. Pak Dengklek hanya bisa melangkah antara dua piring yang bersebelahan. Berapa paling sedikit langkah Pak Dengklek untuk mengambil seluruh piring tersebut?
> 
> - [ ] 18
> - [ ] 19
> - [ ] 20
> - [ ] 21
> - [ ] 22

> [!done] Answer
> 19.

---

> [!question] 
> #binary-search 
> 
> Miko memiliki penggaris dengan panjang 20 satuan.
> 
> Saat pembuatan penggaris, terdapat kesalahan yaitu salah satu angka dari 1–20 terlewat sehingga angka terakhir di penggaris adalah 21.
> 
> Untuk mencari angka yang terlewat, anda dapat bertanya:
> 
> - sebuah bilangan bulat $X$, menyatakan panjang sisi sebuah persegi;
> - sistem akan menjawab luas dari persegi dengan pengukuran penggaris;
> 
> Misalnya angka yang terlewat adalah 6,
> 
> - jika $X = 5$, maka sistem menjawab 25.
> - jika $X = 6$, maka sistem menjawab 49.
> 
> Berapa jumlah pertanyaan paling sedikit agar anda dapat menebak angka yang hilang pada penggaris.

> [!done] Answer
> 5.

---

%% Paradigma Pemecahan Masalah 2 %%

> [!question] 
> #dynamic-programming #grid-dp
> 
> Tara the Beaver wants to go home. She can just move up or move to the right on the following map.
> 
> |     |     |     |     |     |
> | :-: | :-: | :-: | :-: | :-: |
> | 1🪙 | 2👺 | 3🪙 | 3🪙 | 🏁  |
> | 2👺 | 1🪙 | 2👺 | 1👺 | 2🪙 |
> | 2🪙 | 2👺 | 2🪙 | 3🪙 | 1👺 |
> | 3🪙 | 1👺 | 1👺 | 1👺 | 1🪙 |
> | 🦫  | 2🪙 | 2🪙 | 2👺 | 2🪙 |
> 
> On a square there are either monsters or coins. Tara collects all the coins along the path that she follows when she walks on a square with monsters, she needs to give each monster a coin. If she doesn't have enough coins, she will need to give it to them later when she has enough.
> 
> Which route should Tara take to make sure she ends up with the most coins?

Max coin table for each square and from where.

|        |        |        |         |             |
| :----: | :----: | :----: | :-----: | :---------: |
|   ↓4   |   ~2   |   ↓6   | ==↓==10 | **==←==10** |
|   ↓3   |   ~4   |   ↓3   | ==↓==7  |     ~9      |
| ==↓==5 | ==←==3 | ==~==5 | ==←==8  |     ←7      |
| ==↓==3 |   ←2   | ==↓==3 |   ←2    |     ↓5      |
|   🦫   | ==←==2 | ==←==4 |   ←2    |     ←4      |
|        |        |        |         |             |

There are two routes.

> [!done] Answer(s)
> - ↑↑→→→↑↑→.
> - →→↑↑→↑↑→.

---

> [!question] 
> #dynamic-programming #grid-dp 
> 
> Kitty (`K`) sedang bermain "Menangkap Tikus". Kitty dapat bergerak melalui tali-tali yang terhubung. Panjang dari setiap tali yang terhubung adalah sama. Sayangnya, ada beberapa tali yang putus karena ulah Tikus (`T`) sehingga tidak dapat dilewati. Bantulah Kitty mencari berapa banyak cara ia dapat menangkap tikus dengan menempuh jarak terpendek!
> 
> ```
> ┌──┬──┬─   ─┬──┬──T
> │  │  │  │  │  │  │
> ├──┼──┼──┼──┼──┼──┤
> │  │  │  │  │  │  │
> ├──┼─   ─┼──┼──┼──┤
> │  │  │  │  │  │  │
> K──┴──┴──┴─   ─┴──┘
> ```

Karena Kitty harus melalui jalan terpendek, maka pilihannya hanya ada bergerak ke atas, atau ke kanan.

Banyak cara menuju suatu *node* adalah banyak cara dari kiri ditambah banyak cara dari bawah, atau

$$ \mathrm{dp}[r][c] = \mathrm{dp}[r-1][c] + \mathrm{dp}[r][c-1]. $$

Berikut tabel berisi banyak cara menuju suatu *node*. Kita isi mulai dari kiri bawah, *start*-nya Kitty.

|       |     |     |     |     |     |        |
| ----- | --- | --- | --- | --- | --- | ------ |
| 1     | 4   | 7   | 0   | 5   | 11  | **18** |
| 1     | 3   | 3   | 4   | 5   | 6   | 7      |
| 1     | 2   | 0   | 1   | 1   | 1   | 1      |
| **1** | 1   | 1   | 1   | 0   | 0   | 0      |

> [!done] Answer
> Ada 18 cara terpendek.

---

> [!question] 
> When an aircraft lands or takes off from an airport, they are assigned corridors to avoid accidents. These are designated airspaces which separate each aircrafts.
> 
> At the Bebrasland airport, aircraft cannot have the same corridor if they are landing or taking off within 15 minutes.
> 
> Below is a timetable provided with arrival and departure times for flights.
> 
> | Flight | Arrivals | Departures |
> | ------ | :------: | :--------: |
> | 9W2400 |   7:00   |            |
> | EK427  |          |    7:03    |
> | SG147  |   7:12   |            |
> | AI620  |   7:18   |            |
> | AI561  |          |    7:20    |
> | 9W1321 |          |    7:21    |
> 
> What is the minimum number of corridors needed to ensure that all the flights land and take off savely?

| Corridor | Time       |
| -------- | ---------- |
| 1        | 7:00, 7:18 |
| 2        | 7:03, 7:20 |
| 3        | 7:12       |
| 4        | 7:21       |


> [!done] Answer
> There needs to be at least 4 corridors.

---

> [!question] 
> #dynamic-programming #tile-dp 
> 
> Pak Dengklek memiliki lahan yang berukuran 1×10 yang nantinya akan ditempatkan tiga jenis kandang dengan ukuran berbeda, yaitu ukuran 1×1, 1×2, dan 1×4.
> 
> Jika jumlah kandang tidak terbatas, ada berapa banyak cara yang bisa dilakukan oleh Pak Dengklek untuk menyusun kandang-kandang tersebut?

Untuk lahan berukuran 1×N, maka ada tiga kasus,

- `[====N-1====][1]`;
- `[===N-2===][=2=]`; dan
- `[=N-4=][===4===]`.

Misalkan $f(n)$ adalah banyak cara mengisi kandang berukuran $1 \times n.$ Maka dapat dirumuskan

$$ f(n) = f(n-1) + f(n-2) + f(n-4). $$

| $n$ | $f(n)$ |
| --- | ------ |
| 1   | 1      |
| 2   | 2      |
| 3   | 3      |
| 4   | 6      |
| 5   | 10     |
| 6   | 18     |
| 7   | 31     |
| 8   | 55     |
| 9   | 96     |
| 10  | 169    |

> [!done] Answer
> Ada 169 cara.

---

All uniforms used at a tomato festival 