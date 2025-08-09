---
sources:
  - https://drive.google.com/file/d/1eShtTYSPjr-WK5uCJMEJHkoOg6sXDe-B/view
  - https://drive.google.com/file/d/1tghjmR2MtAtjz1ZBXz1tUkTIdjzn5W94/view
---

> [!question]
> #dynamic-programming
> 
> Sepuluh peserta lomba sedang duduk sebaris untuk bermain gim, sehingga siswa pertama duduk berdampingan dengan siswa kedua, siswa kedua bersampingan dengan siswa ketiga, dan seterusnya.
> 
> Dalam gim tersebut, setiap siswa dapat memilih antara `true` atau `false`. Suatu gim dianggap menyenangkan jika hasil operasi OR dari setiap siswa yang duduk berdampingan adalah `true`. Tentukan banyak cara suatu game dianggap menyenangkan.

Karena hasil operasi OR yang bersebelahan harus `true`, maka tidak boleh ada dua `false` berturut-turut.

Misalkan $f(n)$ adalah banyak cara suatu gim dengan $n$ pemain dianggap menyenangkan.

Kita mulai dengan $f(1)$. Ada dua cara, yaitu `F` dan `T`.

Pada $f(2)$, jika pemain terakhir memilih `T`, maka pemain pertama terserah memilih apa. Jika pemain terakhir memilih `F`, maka pemain pertama harus memilih `T`. Maka ada 3 cara, `xT` dan `TF`.

Pada $f(3)$, bisa `xxT` dan `xFT`. Pada $f(4)$, bisa `xxxT` dan `xxFT`. Begitu seterusnya.

Didapat rumusnya

$$ f(n) = f(n-1) + f(n-2) $$

di mana $f(1) = 2$ dan $f(2) = 3$.

| $n$ | $f(n)$  |
| --- | ------- |
| 1   | ***2***       |
| 2   | ***3***       |
| 3   | 5       |
| 4   | 8       |
| 5   | 13      |
| 6   | 21      |
| 7   | 34      |
| 8   | 55      |
| 9   | 89      |
| 10  | **144** |

> [!done] Answer
> Ada 144 gim menyenangkan yang mungkin.

---

> [!question] 
> There are 42 hedgehogs that store their bedding in 5 warehouses. The first hedgehog stores her bedding in the first warehouse, the second in the second warehouse, the sixth once again in the first warehouse, and so on.
> 
> One day, the hedgehogs built a new warehouse, warehouse number 6. They decided to move their bedding between warehouses to make their distribution simple again: the first hedgehog stores her bedding in the first warehouse, the second in the second warehouse, the seventh in the first warehouse, and so on.
> 
> How many hedgehogs that didn't need to move their bedding between warehouses?

We need to find the hedgehogs numbered 1 to 5 in modulo 5 and 6, that is modulo 30.

- The hedgehogs numbered 1 (mod 30) is #1 and #31.
- The hedgehogs numbered 2 (mod 30) is #2 and #32.
- And so on.

| $n \pmod {30}$ | Hedgehogs |     |
| :------------: | --------- | --- |
|       1        | #1<br>#31 |     |
|       2        | #2<br>#32 |     |
|       3        | #3<br>#33 |     |
|       4        | #4<br>#34 |     |
|       5        | #5<br>#35 |     |

> [!done] Answer
> There are 10 hedgehogs that wouldn't need to move.

---

> [!question] 
> Terdapat 10 tim yang akan bertanding di liga sepak bola. Masing-masing tim dinomori dari 1–10. Nilai kekuatan dari 10 tim tersebut seperti tabel berikut.
> 
> | Tim | Kekuatan |
> | --- | -------- |
> | 1   | 12       |
> | 2   | 8        |
> | 3   | 17       |
> | 4   | 9        |
> | 5   | 35       |
> | 6   | 14       |
> | 7   | 19       |
> | 8   | 3        |
> | 9   | 42       |
> | 10  | 21       |
> 
> Untuk mencari pemenangnya, akan diadakan 9 pertandingan sebagai berikut.
> 
> - **Pertandingan #1:** Tim #1 vs Tim #2.
> - **Pertandingan #2:** Pemenang pertandingan #1 vs Tim #3.
> - *dan seterusnya.*
> 
> Diketahui juga pemenang dari suatu pertandingan adalah tim dengan kekuatan yang lebih besar.
> 
> Jika tim sepak bola Charlie berada di nomor 7 dan Charlie dapat menukar nomor timnya dengan nomor tim lain paling banyak satu kali. Charlie tidak peduli dengan pemenang liga ini, ia hanya ingin timnya memenangkan pertandingan sebanyak mungkin. Berapa banyak pertandingan maksimal yang bisa dimenangkan tim Charlie?

- **#1 (12)** vs #2 (8)
- #1 (12) vs **#3 (17)**
- **#3 (17)** vs #4 (9)
- #3 (17) vs **#5 (35)**
- **#5 (35)** vs #6 (14)
- **#5 (35)** vs #7 (19)
- **#5 (35)** vs #8 (3)
- #5 (35) vs **#9 (42)**
- **#9 (42)** vs #10 (21)

Pemenang paling banyak adalah tim dengan jarak terjauh dari tim yang lebih kuat. Jika kita ingin memindahkan tim #7 (19), cari yang terjauh dari tim #5 (35), #9 (42), dan #10 (21). Nomor tim terjauh dari ketiga tim kuat tersebut adalah tim #1. Di mana tim #1[~7] (19) akan memenangi tiga pertandingan.

> [!done] Answer
> Tiga pertandingan.

---

> [!question] 
> We define a basic operation as one of the following.
> 
> - Inserting one character into a word.
> - Removing one character from a word.
> - Replace one character with another.
> 
> We define the distance between two words as the minimum number of basic operation which allows us to change the first word into the second.
> 
> What is the minimum distance between *length* and *french*?

- `LENGTH`
- `RENGTH`
- `RENTH`
- `RENCH`
- `FRENCH`

> [!done] Answer
> The distance between `LENGTH` and `FRENCH` is 4.

---

> [!question] 
> Pak Dengklek sedang belajar membuat biskuit. Ia membuat beberapa tipe biskuit berbeda yang masing-masing tipe diletakkan pada stoples-stoples yang berbeda. Karena bahan-bahan yang diperlukan untuk membuat masing-masing tipe biskuit berbeda, bisa jadi tiap stoples berisi banyak butir biskuit yang berbeda pula.
> 
> Pak Dengklek kemudian mengundang bebek-bebeknya untuk mencicipi biskuit-biskuit buatannya. Satu per satu, para bebek bebas mengambil satu butir biskuit mana pun yang mereka ingin cicipi.
> 
> Agar Pak Dengklek mendapatkan ulasan yang cukup konkret, ia ingin semua tipe biskuit pernah dicicipi oleh sekian ekor bebek. Pak Dengklek ingin mencari tahu minimal bebek yang perlu diundang untuk mencicipi biskuit-biskuitnya.
> 
> 1. Asumsikan Pak Dengklek sudah membuat 7 tipe biskuit yang berbeda, yang masing-masing tipe ada 5 butir biskuit.
> 	
> 	Jika Pak Dengklek ingin semua tipe biskuit pernah dicicipi oleh setidaknya 1 ekor bebek, berapa minimal bebek yang perlu diundang oleh Pak Dengklek?
> 2. Asumsikan Pak Dengklek sudah membuat 100 tipe biskuit berbeda. Biskuit tipe 1 terdiri dari 10 butir, tipe 2 terdiri dari 20 butir, tipe 3 terdiri dari 30 butir, begitu seterusnya sampai tipe 100 yang terdiri dari 1000 butir.
> 	
> 	Jika Pak Dengklek ingin semua tipe biskuit pernah dicicipi oleh setidaknya 5 ekor bebek, berapa minimal bebek yang perlu diundang oleh Pak Dengklek?
> 3. Asumsikan Pak Dengklek sudah membuat 3 tipe biskuit berbeda. Biskuit tipe 1 terdiri dari $A$ butir, biskuit tipe 2 terdiri dari $B$ butir, dan biskuit tipe 3 terdiri dari $C$ butir. Diketahui bahwa total biskuit yang telah dibuat Pak Dengklek adalah 25.
> 	
> 	Jika diketahui juga bahwa Pak Dengklek perlu mengundang minimal 20 ekor bebek agar semua tipe biskuit pernah dicicipi oleh setidaknya seekor bebek, maka berapa banyak pasangan nilai $(A, B, C)$ yang mungkin?

**Nomor 1**

Kita cari *worst case scenario*, di mana 5 biskuit dari 6 tipe diambil semua oleh bebek-bebek. Maka masih ada tipe 7 yang belum dicicipi, kita perlu satu bebek lagi untuk memilih tipe 7. Maka jawabannya $5 \times 6 + 1$.

> [!done] Answer 1
> Setidaknya perlu mengundang 31 bebek.

**Nomor 2**

Kita cari lagi *worst case scenario*-nya, di mana

- 1000 biskuit tipe 100 diambil semua,
- 990 biskuit tipe 99 diambil semua,
- *dan seterusnya*
- 20 biskuit tipe 2 diambil semua.

Semua tipe biskuit telah terpilih setidaknya 5 kali, kecuali tipe 1. Kita perlu 5 bebek lagi untuk memenuhi syarat.

$$ \begin{align*}
	&\quad (1000 + 990 + 980 + \cdots + 40 + 30 + 20) + 5 \\
	&= \left(\frac{99(20 + 1000)}{2}\right) + 5 \\
	&= (99 \times 510) + 5 \\
	&= \boxed{50495}.
\end{align*} $$

> [!done] Answer 2
> Setidaknya perlu 50495 bebek yang diundang.

**Nomor 3**

#stars-and-bars

Ada 20 biskuit dan 3 tipe, setidaknya 1 biskuit perlu dicoba oleh 1 bebek.

Maka

$$ A + B + C = 20 $$

di mana $A, B, C \geq 1$.

Bisa kita tulis ulang menjadi

$$ (A - 1) + (B - 1) + (C - 1) = 17 $$

Ada 17 "bintang" dan 2 "pembatas",

$$ \begin{align*}
	&\quad \frac{(17+2)!}{17! \times 2!} \\
	&= \frac{19 \times 18}{2} \\
	&= \boxed{171}
\end{align*} $$

> [!done] Answer 3
> Ada 171 pasang $(A, B, C)$.

---

> [!question]
> Di akhir pekan ini, Pak Dengklek mendapatkan 5 email dari koleganya yang harus dia baca satu per satu sesuai dengan aturan berikut.
> 
> - Email Pak Adi akan dibaca paling akhir.
> - Email Pak Budi akan dibaca lebih dahulu sebelum email Pak Adi, tetapi bukan email yang pertama kali dibaca.
> - Email Pak Carli dan Pak Dudung dibacakan secara berurutan antara Email Pak Eman dan Pak Budi.

|  1   |   2   |   3    |  4   |  5  |
| :--: | :---: | :----: | :--: | :-: |
| Eman | Carli | Dudung | Budi | Adi |

> [!done] Answer
> Pak Eman.