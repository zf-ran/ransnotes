> [!example]+ Detail
> - **Total poin:** 1000
> - **Jumlah soal:** 40

# Pemecahan Masalah

**Soal 1** *(40 poin)* Bilangan rasional adalah bilangan yang dapat dinyatakan sebagai hasil bagi dua bilangan bulat $\frac{p}{q}$​ dengan $q \neq 0$. Jika ditulis dalam bentuk desimal, bilangan rasional selalu memiliki representasi desimal yang berhenti (*terminating*) atau berulang (*repeating*). Contoh bilangan rasional: −8, 42.314, dan 42.

Nesy dan Nyoo sedang bermain dengan garis bilangan. Pada sebuah interval inklusif $[0, n]$, dengan bilangan bulat $n \geq 4$. Mereka akan bermain secara bergantian. Nesy mulai terlebih dahulu, yaitu dia akan memilih sebuah bilangan rasional pada rentang $[0, n]$. Pemain selanjutnya hanya boleh memilih bilangan rasional lain yang berjarak lebih dari 1 dari semua angka yang sudah dipilih sebelumnya oleh salah satu pemain. Permainan akan berlanjut, hingga seorang pemain yang tidak dapat memilih bilangan rasional dinyatakan kalah. 

**Contoh:** Jika $n = 8$ dan Nesy memilih bilangan pertamanya adalah 6, maka Nyoo tidak boleh memilih bilangan rasional pada rentang $[5, 7]$. Misal Nyoo memilih angka 1, akibatnya Nesy tidak boleh memilih bilangan pada rentang $[0, 2]$ dan $[5, 7]$.

Jika kedua pemain bermain secara optimal, mana pernyataan yang paling benar?

- [ ] Nyoo selalu menang.
- [ ] Nesy selalu menang.
- [x] Nesy menang jika dan hanya jika $n$ adalah bilangan ganjil.
- [ ] Nyoo menang jika dan hanya jika $n$ adalah bilangan ganjil.
- [ ] Nyoo menang jika dan hanya jika $n \geq 8$.

---

**Soal 2** *(80 poin)* Diberikan sebuah papan grid berukuran $7 \times 7$ yang diisi oleh huruf `I`, `O`, dan `A`. Anda sangat menyukai kata IOAI, dan penasaran ada berapa banyak kata IOAI yang dapat dibentuk pada papan ini?

```
I I I I I I I
I O A O O A I
I O A A A A I
I O O I A O I
I O O O O O I
I O A A A O I
I I I I I I I
```

Untuk menjawab pertanyaan ini, kita perlu mendefinisikan apa yang dimaksud dengan sebuah path “4 huruf” pada papan.

1. Mulai dari suatu petak.
2. Bergerak ke salah satu petak tetangga dari 8 arah (atas, bawah, kiri, kanan, atau diagonal).
3. Bergerak lagi ke salah satu dari 8 tetangga.
4. Bergerak sekali lagi ke salah satu dari 8 tetangga, lalu berhenti.

Sehingga path menghasilkan tepat 4 huruf dari petak awal sampai petak akhir. Perhatikan bahwa suatu petak **boleh** dikunjungi lebih dari satu kali. Sebagai ilustrasi, berikut merupakan contoh pembentukan kata IOAI ~~yang sudah ditandai berwarna merah cetak tebal~~ <u>yaitu dari baris 1 kolom 1 hingga baris 1 kolom 4</u>.

> [!important] Format jawaban dalam bentuk angka

> [!success] 169

---

# Logika Matematika

**Soal 3–4** Tim peneliti melakukan pengambilan sampel berat badan terhadap $N$ orang yang berasal dari suatu populasi mahasiswa. Variansi sampel dari berat badan $N$ orang ini adalah $X$. Keesokan harinya, hasil kajian lebih lanjut menunjukkan bahwa mereka perlu mengambil sampel tambahan sebanyak $N$ orang lagi pada pengambilan sampel _batch_ kedua. Kebetulan, sampel berat badan dari semua $N$ orang pada _batch_ kedua adalah sama persis dengan berat badan pada sampel _batch_ pertama. Variansi gabungan semua sampel yang baru (berat badan dari $2N$ orang) adalah $Y$.

**Soal 3** *(40 poin)* Manakah pertanyaan yang benar?

- [ ] $X < Y$
- [ ] $X = Y$
- [x] $X > Y$
- [ ] Tidak bisa ditentukan antara $X < Y$ atau $X > Y$
- [ ] $X = 2Y$
- [ ] $Y = 2X$

**Soal 4** *(80 poin)* Misal, peneliti tersebut mengambil kembali sampel data pada *batch* ketiga sebanyak $M$ orang, dengan rataan adalah setengah dari rataan data yang sudah dikumpulkan dari _batch_ pertama dan kedua (sebanyak $2N$ orang). Jika digabung, yaitu sebanyak $2N + M$ orang, rataan baru menjadi $\frac{3}{4}$​ dari rataan data gabungan batch pertama dan kedua.

Berapakah nilai $M$?

> [!important]- Format Jawaban
> - Jika melibatkan perkalian konstan dengan variabel $N$, jawaban ditulis seperti `8N`,  `9N`, `13N`, dst.
> - Jika melibatkan penjumlahan atau pengurangan, jawaban ditulis seperti `7N+3`, `4N−5`, `4N+1`, dst.
> - Tidak boleh ada *white-space* pada jawaban.

> [!success] 2N

---

# Probabilitas

**Soal 5–7** Di sebuah bioskop, terdapat 3 jenis film: film aksi (🔫), film keluarga (👨‍👩‍👧‍👦), dan film horor (👻). Berdasarkan data pengunjung, probabilitas menonton masing-masing film adalah.

- P(🔫) = 40%
- P(👨‍👩‍👧‍👦) = 35%
- P(👻) = 25%

Bioskop ini juga menyediakan 2 jenis snack: *popcorn* (🍿) dan *soft drink* (🥤). Data pembelian snack berdasarkan jenis film yang ditonton adalah sebagai berikut.

| Jenis Film                | Tidak Membeli *Snack* | Hanya Membeli *Popcorn* | Hanya Membeli *Soft Drink* | Membeli Popcorn dan *Soft Drink* |
| ------------------------- | --------------------- | ----------------------- | -------------------------- | -------------------------------- |
| Film Aksi 🔫              | 30%                   | 20%                     | 10%                        | 40%                              |
| Film Keluarga 👨‍👩‍👧‍👦 | 45%                   | 20%                     | 15%                        | 20%                              |
| Film Horor 👻             | 50%                   | 10%                     | 10%                        | 30%                              |

> [!important]- Format Jawaban
> **Tuliskan jawaban dalam bentuk bilangan bulat tanpa persentase.**
> 
> Jika hasil probabilitas dinyatakan dalam persen desimal, **bulatkan ke bawah**. Misalkan jawabannya $64.71\%$, tulislah `64`

**Soal 5** *(40 poin)* Kemungkinan pengunjung yang membeli *popcorn*. P(🍿) = ….

> [!success] 48

**Soal 6** *(40 poin)* Kemungkinan pengunjung yang menonton film aksi bersamaan dengan membeli *popcorn* atau *soft drink*. P(🔫 ∧ (🍿 ∨ 🥤)) = ….

> [!success] 28

**Soal 7** *(65 poin)* Jika diketahui pengunjung hanya membeli *soft drink* saja, berapa kemungkinan ia menonton film horor? P(👻|🥤) = ….

> [!success] 21

---

# Model Linier

**Soal 8–9** Seorang peneliti ingin membuat model prediksi skor UTBK seorang anak SMA berdasarkan nilai rapor Matematika (berkisar dari 0–100).

Model yang digunakan adalah persamaan linier adalah

$$ f(M; \alpha, \beta) = a + \beta M $$

dengan

- $M$ adalah nilai rapor Matematika ($0 \leq M \leq 100$).
- $\alpha, \beta$ adalah parameter yang harus dicari (dioptimasi).

Berikut adalah data siswa yang diberikan.

| Siswa ke-$i$ | Nilai Matematika ($M$) | Skor UTBK ($y$) |
| ------------ | ---------------------- | --------------- |
| 1            | 95                     | 785             |
| 2            | 86                     | 790             |
| 3            | 68                     | 600             |

Kemudian, kriteria yang digunakan untuk mencari $\alpha$ dan $\beta$ adalah dengan meminimalkan nilai fungsi loss $L(\alpha, \beta)$ berikut.

$$ L(\alpha, \beta) = \frac{1}{n} \sum_{i=1}^n (y_i - (\alpha + \beta M_i))^2 \newcommand{\b}[1]{\mathbf{#1}} $$

dengan $n = 3$ pada konteks ini.

**Soal 8** *(20 poin)* Hitung nilai fungsi $L(\alpha, \beta)$ ketika $\alpha = 227$ dan $\beta = 6.0$.

> [!important]- Format Jawaban
> **Tuliskan jawaban dengan presisi 1 angka di belakang tanda desimal (titik).**
>
> Sebagai contoh:
>
> - $19.35$, ditulis `19.4`
> - $72.71$, ditulis `72.7`
> - $0.68$, ditulis `0.7`

> [!success] 1192.7

**Soal 9** *(80 poin)* Carilah nilai $\alpha$ dan $\beta$ yang meminimalkan fungsi $L(\alpha, \beta)$.

**Catatan penting:** Cari nilai $\alpha$ dan $\beta$ yang menghasilkan $L(\alpha, \beta)$ **sekecil mungkin terlebih dahulu,** baru kemudian dibulatkan sesuai permintaan soal. Saat sudah dibulatkan, solusinya belum tentu menjadi yang paling optimal lagi di presisi tersebut.

> [!important]- Format Jawaban
> **Tuliskan jawaban Anda dalam format** `X.X; Y.Y`
>
> Dengan
>
> - `X.X` adalah presisi 1 angka di belakang koma dari nilai $\alpha$; dan
> - `Y.Y` adalah nilai $\beta$ dengan presisi 1 angka di belakang koma.
> 
> Sebagai contoh:
> - Jika $\alpha = 19.35, \beta = 72.71$, maka tuliskan `19.4; 72.7`

> [!success] 112.4; 7.4

---

# Kemiripan Vektor

**Soal 10–21** Dalam bidang *Natural Language Processing* (NLP) modern, sebuah token atau kata biasanya direpresentasikan dalam bentuk vektor di ruang berdimensi tinggi. Misalnya, diberikan representasi vektor dari beberapa kata berikut.

$$ \begin{align*}
	\text{senang} &= (21, 10) \\
	\text{pria} &= (6, 29) \\
	\text{wanita} &= (30, 24) \\
	\text{ayah} &= (11, 26) \\
	\text{ibu} &= (36, 19) \\
	\text{raja} &= (8, 36) \\
	\text{ratu} &= (32, 29) \\
	\text{sedih} &= (18, 19) \\
	\text{menang} &= (26, 8) \\
	\text{kalah} &= (23, 16)
\end{align*} $$

Vektor-vektor ini bisa dimanipulasi dengan operasi tambah dan kurang.  

Contoh terkenal:

$$ \text{raja} + \text{wanita} − \text{pria} \approx \text{ratu}, \quad \text{ayah} + \text{wanita} − \text{pria} \approx \text{ibu}. $$

Artinya ada vektor translasi ($\text{wanita} - \text{pria}$) yang bisa mengubah kata maskulin menjadi versi feminin.

**Soal 10** *(10 poin)* Berapakah jarak Euclidean dari vektor $\text{raja}$ dan $\text{kalah}$?

Rumus Euclidean distance dari dua buah vektor $(x_1,y_1)$ dan $(x_2, y_2)$ adalah

$$ \sqrt{(x_1 − x_2)^2 + (y_1 − y_2)^2}. $$

> [!important] Format jawaban dalam bentuk angka

> [!success] 25

**Soal 11** *(15 poin)* Berapa nilai vektor $\text{senang} + \text{kalah} - \text{menang}$?

> [!important] Format jawaban dalam bentuk `A B`, di mana hasil vektornya adalah $(A, B)$

> [!success] 18 18

**Soal 12–21** Aji, seorang peneliti bahasa multi galaksi, menemukan bahasa alien kuno dengan 10 kata sebagai berikut.

$$ \begin{align*}
	\text{Gohok} &= (34, 37) \\
	\text{Subi} &= (28, 29) \\
	\text{Matot} &= (14, 35) \\
	\text{Befar} &= (38, 31) \\
	\text{Dursit} &= (38, 40) \\
	\text{Gien} &= (29, 19) \\
	\text{Ibakuz} &= (24, 20) \\
	\text{Gelon} &= (11, 46) \\
	\text{Wazuke} &= (10, 42) \\
	\text{Nusgen} &= (22, 30).
\end{align*} $$

Diketahui bahwa ke-10 kata ini adalah terjemahan persis dari ke-10 kata bahasa Indonesia di atas (senang, pria, wanita, …, kalah). Namun, Aji tidak tahu pasangan tepatnya.

Temukan pasangan kata antara bahasa alien dan bahasa Indonesia, dengan memanfaatkan fakta bahwa struktur vektor antar kata di bahasa alien sama seperti di bahasa Indonesia.

> [!important] Format jawaban huruf kecil semua

**Soal 12** *(13 poin)* Gohok

> [!success] wanita

**Soal 13** *(13 poin)* Subi

> [!success] kalah

**Soal 14** *(13 poin)* Matot

> [!success] ayah

**Soal 15** *(13 poin)* Befar

> [!success] ibu

**Soal 16** *(13 poin)* Dursit

> [!success] ratu

**Soal 17** *(13 poin)* Gien

> [!success] menang

**Soal 18** *(13 poin)* Ibakuz

> [!success] senang

**Soal 19** *(13 poin)* Gelon

> [!success] raja

**Soal 20** *(13 poin)* Wazuke

> [!success] pria

**Soal 21** *(13 poin)* Nusgen

> [!success] sedih

---

**Soal 22–25** Sebuah citra digital $\b I$ dapat direpresentasikan sebagai matriks berukuran $x \times y$, dimana setiap elemen matriks $\b I_{i,j}$​ menyatakan nilai piksel pada baris ke-$i$ dan kolom ke-$j$.

**Kernel** adalah matriks kecil (misalnya $3 \times 3$ atau $5 \times 5$) yang digeser di atas citra. Kernel $\b K$ adalah sebuah matriks kecil berukuran $m \times n$ yang berfungsi untuk mengekstrak pola tertentu dari citra $\b I$, dimana kernel $\b K$ biasanya berukuran lebih kecil dibandingkan dengan citra $\b I$, yakni $x \geq m$ dan $y \geq n$.

**Konvolusi** adalah operasi _dot product_ (yakni, perkalian antarelemen di kedua matriks yang kemudian dijumlahkan) antara kernel $\b K$ dan potongan citra dari $\b I$, yakni *patch* (submatriks) $\b J$, dimana ukuran patch $\b J$ sama dengan kernel $\b K$. Jika ada dua vektor dengan panjang yang sama,

$$ \b a = [a_1, a_2, \dots, a_n], \quad \b b = [b_1, b_2, ..., b_n]. $$

Maka *dot product* didefinisikan sebagai

$$ \b a \cdot \b b = \sum_{i=1}^n a_i b_i = a_1 b_1 + a_2 b_2 + \cdots + a_n b_n. $$

Proses konvolusi sendiri dapat didefinisikan sebagai berikut. Konvolusi pada keseluruhan citra $\b I$ menggunakan kernel $\b K$ bisa dinotasikan sebagai $\b K * \b I$, di mana hasilnya akan menghasilkan citra keluaran $\b S$.

Dari gambar terlihat bahwa proses dot product terjadi antara kernel $\b K$ dan patch $\b J$ dimana masing-masing elemen dari $\b K$ dan $\b J$ dikalikan, kemudian hasilnya dijumlahkan.  

Berikut merupakan contoh ukuran gambar input $3 \times 4$ dan kernel $2 \times 2$ yang menghasilkan ukuran gambar output $2 \times 3$.

![[Contoh Konvolusi.png]]

**Hubungan Konvolusi dengan Stride dan Padding**

Proses konvolusi tidak lepas dari stride dan padding.  

**Stride** adalah seberapa jauh kernel bergeser tiap langkah. Contohnya:

- Jika `stride = 1`, kernel bergeser 1 piksel.
- Jika `stride = 2`, kernel bergeser 2 piksel.
- Jika `stride = n`, kernel bergeser `n` piksel.

Berikut merupakan contoh `stride = 1` dan `stride = 2` dengan ukuran gambar input $5 \times 5$ dan kernel $3 \times 3$.

![[Contoh Stride.png]]

**Padding** adalah penambahan lapisan piksel di tepi gambar untuk menjaga ukuran output. Contohnya:

- Jika `padding = 0`, tidak ada penambahan piksel, maka **ukuran gambar output lebih kecil dari ukuran gambar input**.
- Jika `padding = “same”`, maka **ukuran gambar output sama dengan ukuran gambar input** (asumsi `stride = 1`).
- Jika `padding = n`, terdapat **penambahan `n` piksel di setiap sisi gambar** (kiri, kanan, atas, bawah), sehingga total bertambah $2n$ piksel. Jadi total penambahan ukuran gambar adalah sebanyak $2n$ piksel (karena kiri + kanan dan atas + bawah).

Berikut merupakan contoh `padding = “same”` dan `stride = 1` dengan ukuran gambar input $5 \times 5$ dan kernel $3 \times 3$.

![[Contoh Padding.png]]

Anda diminta untuk memprediksi ukuran akhir citra setelah melalui beberapa lapisan konvolusi dengan ukuran kernel, stride, dan padding yang berbeda.  

> [!important]- Format Jawaban
> Tulis jawaban dalam format `A x B`
>
> Di mana
>
> - `A` adalah banyak baris citra $\b S$; dan
> - `B` adalah banyak kolom citra $\b S$.
> 
> Contohnya:
> 
> - Citra $\b S$ berukuran $7 \times 8$, tulislah `7 x 8`

**Soal 22** *(20 poin)* Ukuran awal citra $\b I$ adalah $32 \times 32$.

- Konvolusi 1: kernal $3 \times 3$, `padding = “same”`, `stride = 1`.

Berapakah ukuran citra akhir $\b S$?

> [!success] `32 x 32`

**Soal 23** *(30 poin)* Ukuran citra awal $\b I$ adalah $32 \times 32$.

- Konvolusi 1: kernel $3 \times 3$, `padding = “same”`, `stride = 1`.
- Konvolusi 2: kernel $5 \times 5$, `padding = 0`, `stride = 2`.

Berapakah ukuran citra akhir $\b S$?

> [!success] `14 x 14`

**Soal 24** *(40 poin)* Ukuran citra awal $\b I$ adalah $64 \times 64$.

- Konvolusi 1: kernel $7 \times 7$, `padding = 3`, `stride = 2`.
- Konvolusi 2: kernel $3 \times 3$, `padding = “same”`, `stride = 2`.
- Konvolusi 3: kernel $1 \times 1$, `padding = 0`, `stride = 1`.

Berapakah ukuran citra akhir $\b S$?

> [!success] `16 x 16`

**Soal 25** *(75 poin)* Ukuran citra awal $\b I$ adalah $128 \times 64$.

- Konvolusi 1: kernel $7 \times 3$, `padding = (3, 1)`, `stride = (2, 1)`.
- Konvolusi 2: kernel $5 \times 5$, `padding = 2`, `stride = 2`.
- Konvolusi 3: kernel $3 \times 3$, `padding = “same”`, `stride = 1`.
- Konvolusi 4: kernel $1 \times 7$, `padding = (0, 3)`, `stride = (1, 2)`.
- Konvolusi 5: kernel $3 \times 3$, `padding = 0`, `stride = 2`.

Berapakah ukuran citra akhir $\b S$?

> [!success] `32 x 32`

---

**Soal 26–40** Barisan DNA tersusun oleh urutan nukleotida yang terdiri dari empat basa nitrogen: adenin (A), timin (T), guanin (G), dan sitosin (C). Diketahui sampel DNA dari 3 spesies berbeda sebagai berikut.

| Urutan DNA   | Spesies |
| ------------ | ------- |
| `GATTATAAAGCA` | Kucing  |
| `AATCTAATTATG` | Kucing  |
| `ACAAAAAATTTC` | Kucing  |
| `CATAAAGAAATA` | Kucing  |
| `ACGACGCGATCG` | Bebek   |
| `CGCGAGAGAGCG` | Bebek   |
| `GCTGCGTGTCAG` | Bebek   |
| `CGAGCTAGCAGC` | Bebek   |
| `CCAGGGGAGCCC` | Ikan    |
| `TTAGGTCAAGGC` | Ikan    |
| `CGGTCCCCAAAG` | Ikan    |
| `AGCCGGGGCAAG` | Ikan    |

Anda diminta untuk membuat sebuah sistem yang dapat memprediksi spesies berdasarkan DNA yang diberikan dengan memanfaatkan data latih yang tersedia.

Namun, karena sedang berlibur, Anda tidak memiliki waktu untuk membangun sistem kecerdasan buatan dari awal.

Anda pun meyakini bahwa pola kemunculan basa nitrogren pada untaian DNA dari masing-masing spesies cukup berbeda sehingga sebenarnya dapat diklasifikasikan bahkan tanpa bantuan mesin atau komputer sekalipun.

Diberikan beberapa untaian DNA berikut, tentukanlah spesiesnya (Kucing, Bebek, atau Ikan). 

> [!important] Format pengisian hanya Kucing, Bebek, atau Ikan

**Soal 26** *(13 poin)* CCGGCTCGTAAG

> [!success] Ikan

**Soal 27** *(13 poin)* CATGAAAATATA

> [!success] Kucing

**Soal 28** *(13 poin)* TAATAACACATA

> [!success] Kucing

**Soal 29** *(13 poin)* TCGCTCGCACGT

> [!success] Bebek

**Soal 30** *(13 poin)* GCACGCGCAGAT

> [!success] Ikan

**Soal 31** *(13 poin)* TTTCCCGCTGGG

> [!success] Bebek

**Soal 32** *(13 poin)* CGGGCTTCCCGG

> [!success] Ikan

**Soal 33** *(13 poin)* GTCACTATCACG

> [!success] Bebek

**Soal 34** *(13 poin)* CGAAATTTATTA

> [!success] Kucing

**Soal 35** *(13 poin)* GCGCTATATGCG

> [!success] Ikan

**Soal 36** *(13 poin)* GGCAGGTAGCCC

> [!success] Ikan

**Soal 37** *(13 poin)* ACAAATAAACCA

> [!success] Kucing

**Soal 38** *(13 poin)* ATGAGGGCCCCG

> [!success] Ikan

**Soal 39** *(13 poin)* AAAAACTATTAT

> [!success] Kucing

**Soal 40** *(13 poin)* CGCTCTAGCGCA

> [!success] Bebek