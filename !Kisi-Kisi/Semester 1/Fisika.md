> [!important] Catatan Penting
> Saya akan menulis: $\newcommand{\m}[1]{\mathsfup{#1}}\newcommand{\v}[1]{\mathbf{#1}}$
> 
> - **variabel** dengan serif miring, seperti $v$, $F$, $A$.
> - **satuan** dengan serif tegak, seperti $\pu{m}$, $\pu{kg}$, $\pu{N}$.
> - **dimensi** dengan sans-serif tegak, seperti $\m L$, $\m M$, $\m \Theta$.
> - **dimensi dari suatu besaran** $B$ dengan $[B]$. Sebagai contoh, misalkan $F$ adalah gaya, maka $[F] = \pu{\m L \m M \m T-2}$.
> - **satuan SI dari suatu besaran** $B$ dengan $\{B\}$. Sebagai contoh, misalkan $v$ adalah kecepatan, maka $\{v\} = \pu{m/s}$.
> - **vektor** dengan serif tebal tegak, seperti $\v v$, $\v r$.
> - **pemisah ribuan** dengan spasi, seperti $\pu{20034582}$.
> - **pemisah desimal** dengan titik, seperti $\pu{4.5}$.

# 1—Besaran, Satuan, dan Pengukuran {#bab-1}

## 1.1—Besaran, Satuan, dan Dimensi

Besaran-besaran pokok meliputi **7 besaran** berikut. 

| Nama              | Dimensi     | Satuan SI | Simbol Satuan SI |
| ----------------- | ----------- | --------- | ---------------- |
| Panjang           | $\m L$      | meter     | $\pu{m}$         |
| Massa             | $\m M$      | kilogram  | $\pu{kg}$        |
| Waktu             | $\m T$      | detik     | $\pu{s}$         |
| Kuat Arus         | $\m I$      | ampere    | $\pu{A}$         |
| Suhu              | $\m \Theta$ | kelvin    | $\pu{K}$         |
| Jumlah zat        | $\m N$      | mol       | $\pu{mol}$       |
| Intensitas cahaya | $\m J$      | kandela   | $\pu{cd}$        |

Besaran turunan meliputi segala kombinasi perkalian (atau pembagian) dari besaran pokok.

Misalnya kecepatan, bersatuan $\pu{m/s}$ atau dapat ditulis seperti $\pu{m s-1}$, yaitu kombinasi antara $\m L$ dan $\m T$; yaitu $\pu{\m L \m T-1}$.

Besaran **selain** 7 besaran pokok di atas merupakan **besaran turunan**.

Berikut beberapa besaran **turunan** umum.

| Nama        | Dimensi                  | Satuan SI        | Keterangan       |
| ----------- | ------------------------ | ---------------- | ---------------- |
| Luas        | $\pu{\m L2}$             | $\pu{m2}$        |                  |
| Volume      | $\pu{\m L3}$             | $\pu{m3}$        |                  |
| Massa jenis | $\pu{\m L-3 \m M}$       | $\pu{kg/m3}$     |                  |
| Kecepatan   | $\pu{\m L \m T-1}$       | $\pu{m/s}$       |                  |
| Percepatan  | $\pu{\m L \m T-2}$       | $\pu{m/s2}$      |                  |
| Gaya        | $\pu{\m L \m M \m T-2}$  | $\pu N$ (newton) | $\pu{kg . m/s2}$ |
| Usaha       | $\pu{\m L2 \m M \m T-2}$ | $\pu{J}$ (joule) | $\pu{kg.m2/s2}$  |
| Daya        | $\pu{\m L2 \m M \m T-3}$ | $\pu{W}$ (watt)  | $\pu{kg.m2/s3}$  |
| Momentum    | $\pu{\m L \m M \m T-1}$  | $\pu{kg.m/s}$    |                  |

Satuan-satuan tersebut dapat ditambahkan awalan (prefiks) untuk mengubah “ukuran”-nya, dengan kelipatan $10$.

Ada **6 prefiks** utama: kilo, hekto, deka, desi, senti, dan mili.

| Nama  | Simbol    | Faktor    |
| ----- | --------- | --------- |
| kilo  | $\pu{k}$  | $10^3$    |
| hekto | $\pu{ha}$ | $10^2$    |
| deka  | $\pu{da}$ | $10$      |
| —     | —         | $1$       |
| desi  | $\pu{d}$  | $10^{-1}$ |
| senti | $\pu{c}$  | $10^{-2}$ |
| mili  | $\pu{m}$  | $10^{-3}$ |

Ada lagi prefiks untuk yang lebih besar dan kecil, namun jarang digunakan (kecuali tera, giga, mega, dan mikro). Berikutlah jika penasaran. Tidak terlalu penting untuk dihafal.

| Nama  | Simbol   | Faktor     |
| ----- | -------- | ---------- |
| yotta | $\pu{Y}$ | $10^{24}$  |
| zetta | $\pu{Z}$ | $10^{21}$  |
| eksa  | $\pu{E}$ | $10^{18}$  |
| peta  | $\pu{P}$ | $10^{15}$  |
| tera  | $\pu{T}$ | $10^{12}$  |
| giga  | $\pu{G}$ | $10^9$     |
| mega  | $\pu{M}$ | $10^6$     |
| —     | —        | —          |
| mikro | $\pu{µ}$ | $10^{-6}$  |
| nano  | $\pu{n}$ | $10^{-9}$  |
| piko  | $\pu{p}$ | $10^{-12}$ |
| femto | $\pu{f}$ | $10^{-15}$ |
| atto  | $\pu{a}$ | $10^{-18}$ |
| zepto | $\pu{z}$ | $10^{-21}$ |
| yocto | $\pu{y}$ | $10^{-24}$ |

Untuk menggunakan prefiks tersebut, letakkan prefiks sebelum satuan yang ingin dipakai. Sebagai contoh, kilo dan watt, maka menjadi kilowatt. Dan untuk simbolnya, gabungkan tanpa spasi, sebagai contoh $\pu{kW}$.

Ambil contoh tadi, kilowatt: $\pu{kW}$. Karena satu “kilo-” itu $10^3$, maka satu kilowatt itu $\pu{10^3 W}$ atau $\pu{1000 W}$.

Contoh lain, sentimeter: $\pu{cm}$. Karena satu “senti-” itu $10^{-2}$, maka satu sentimeter itu $\pu{10^{-2} m}$ atau $\pu{\frac{1}{100} m}$.

Jadi semua istilah gigabyte, megabyte, terabyte itu datangnya dari prefiks SI.

## 1.2—Pengukuran

Pada suatu pengukuran, akan **pasti** terjadi ketidakpastian. Tidak ada pengukuran yang akurat. Seakurat apapun pengukurnya, pasti akan ada ketidakpastian, dalam skala $10^{-100}$ sekalipun.

Maka dari itu, kesalahan pengukuran tersebut ada penulisan tertentu.

Secara umum, kesalahan pengukuran ditulis sebagai

$$ x \pm \Delta x $$

di mana

- $x$ adalah hasil pengukuran yang didapat; dan
- $\Delta x$ adalah ketidakpastian.

### 1.2.1—Pengukuran Tunggal

Pada pengukuran tunggal, ketidakpastian adalah setengah dari skala terkecil:

$$ \Delta x = \frac 1 2 \times (\text{nst}) $$

di mana $\text{nst}$ adalah nilai skala terkecil.

#### 1.2.1.1—Penggaris

Lihat penggaris kalian, umumnya skala terkecilnya adalah $\pu{1 mm}$.

Anggaplah kita sedang mengukur lebar ponsel. Kita mendapati lebar ponsel di angka $\pu{7.9 cm}$ atau $\pu{79 mm}$. Nah, dengan prinsip tadi, hasil pengukuran adalah

$$\pu{(79 \pm 0.5) mm} $$

di mana $\pu{0.5}$ di dapat dari setengah skala terkecil penggaris.

#### 1.2.1.2—Jangka Sorong

[otw]

### 1.2.2—Pengukuran Berulang

Untuk lebih akurat lagi, kita dapat mengukur berkali-kali, dan merata-ratakan setiap hasil pengukuran.

Misalkan kita sudah melakukan $n$ pengukuran, dan hasil pengukuran ke-$i$ adalah $x_i$.

Misalkan $\bar x$ adalah rata-rata pengukuran:

$$ \bar x = \frac{x_1 + x_2 + \cdots + x_n}{n}. $$

Misalkan $s$ adalah **simpangan baku**, yaitu rata-rata seberapa jauh pengukuran dari pengukuran rata-rata:

$$ s = \sqrt{\frac 1 {n-1} \sum_{i=1}^n (x_i - \bar x)^2} $$

atau lebih mudah

$$ s = \sqrt{\frac{n\sum_i x_i^2 - (\sum_i x_i)^2}{n(n-1)}}. $$

Maka hasil pengukuran akan ditulis sebagai

$$ \boxed{\bar x \pm s}. $$

Misalkan kita mengukur lebar buku 10 kali menggunakan jangka sorong. Dan berikut hasilnya.

| Lebar $(\pu{cm})$ |
| ----------------: |
|             15.23 |
|             15.27 |
|             15.20 |
|             15.30 |
|             15.18 |
|             15.25 |
|             15.22 |
|             15.26 |
|             15.19 |
|             15.24 |

Didapat

- jumlah adalah $\pu{152.34 cm}$;
- rata-ratanya adalah $\pu{15.234 cm}$; dan
- jumlah kuadrat adalah $\pu{2320.7604 cm}$.

Masukkan ke rumus simpangan baku.

$$ \begin{align*}
	s &= \sqrt{\frac{n\sum_i x_i^2 - (\sum_i x_i)^2}{n(n-1)}} \\
	&= \sqrt{\frac{10 (\pu{2320.7604 cm2}) - (\pu{152.340 cm})^2}{10 \cdot 9}} \\
	s &= \pu{0.03777124 cm}.
\end{align*} $$

Sekarang, kita perlu membulatkan $s$, karena $s$ hanyalah perkiraan, agak menipu kesannya jika kita memberi **7 angka penting**.

Biasanya, simpangan baku dibulatkan menjadi 1 hingga 2 angka penting. Maka pada kasus ini, $s = \pu{0.038 cm}$.

Dan jumlah desimal $\bar x$ juga mengikuti $s$. Pada kasus ini, $\bar x$ sudah memiliki 3 angka desimal.

Maka hasil pengukuran adalah

$$ \boxed{\pu{(15.234 \pm 0.038) cm}}. $$

- **(1)** *Besaran turunan yang ada dalam wacana.*
	- Seperti di atas, selain 7 besaran pokok maka besaran turunan.
- **(2)** *Besaran dengan dimensi sama yang ada dalam wacana.*
- **(3)** *Satuan salah satu dari besaran turunan yang ada dalam wacana.*
- **(4)** *Dimensi dari besaran turunan yang ada dalam wacana.*
- **(5<sub>BS</sub>)** *Hasil pengukuran dengan aturan angka penting.*
- **(6)** *Massa jenis benda dengan menerapkan aturan angka penting.*
- **(7<sub>MJD</sub>)** *Objek variabel bebas, variabel terikat, dan variabel control.*
- **(8<sub>BS</sub>)** *Membaca hasil pengukuran, rata-rata hasil pengukuran, dan menafsirkan hasil pengukuran menggunakan mikrometer sekrup.*

# 2—Energi Alternatif {#bab-2}

*no hitung-hitung* 😞.

- **(9)** *Karakteristik utama sumber energi alternatif.*
- **(10<sub>BS</sub>)** *Konversi energi alternatif dan alat konversinya, sebagai contoh sel surya.*
- **(11)** *Bandingkan kelebihan sumber energi terbarukan dengan sumber energi fosil.*
- **(12<sub>BS</sub>)** *Teknologi dan cara pemanfaatan sumber energi terbarukan.*
- **(13)** *Wacana desain perusahaan pemanfaatan sumber energi terbarukan, cari solusi terbaik dari kendala yang ada dalam wacana.*
- **(14)** *Wacana ketersediaan sumber energi terbaru, pilih jenis sumber energi paling tepat dan sesuai.*
- **(15<sub>MJD</sub>)** *Wacana rencana pemanfaatan sumber energi, tentukan cara/teknik pemanfaatan sumber energi dalam wacana.*

# 3—Vektor {#bab-3}

## 3.1—Operasi Vektor

### 3.1.1—Penjumlahan

Diberikan vektor $\newcommand{\v}[1]{\mathbf{#1}}\v v_1 = \begin{bmatrix} x \\ y \end{bmatrix}$ dan $\v v_2 = \begin{bmatrix} a \\ b \end{bmatrix}$, maka $\v v_1 + \v v_2 = \begin{bmatrix} x + a \\ y + b \end{bmatrix}$.

- **(16)** *Gambar vektor perjalanan kapal.*
- **(17)** *Operasi penjumlahan vektor dari diagram poligon vektor.*
- **(18)** *Jumlah angka secara aturan besaran vektor dengan berbagai sudut.*
- **(19)** *Cerita tentang 3 buah vektor, hubungan magnitudo ketiga vektor.*
- **(20)** *Operasi resultan vektor 3 dimensi secara analisis.*
- **(21)** *Hasil operasi perkalian silang (*cross product*) vektor 3 dimensi.*
- **(22<sub>BS</sub>)** *Resultan 3 vektor dengan metode proyeksi.*
- **(23)** *Perjalanan pertualangan, tentukan resultan perpindahan petuangan.*

# 4—Energi {#bab-4}

- **(24)** *Usaha pada angkat barbel baik ketika mengangkat maupun ketika menahan barbel.*
- **(25)** *Konversi energi kinetik, energi potensial dan energi mekanik pada gerak vertikal.*
- **(26)** *Menentukan usaha pada …*<sup>?</sup> *berdasarkan definisi usaha.*
- **(27<sub>MJD</sub>)** *Wacana kajian akademik topik fisika, tentukan konsep usaha.*
- **(28)** *Besar usaha pada gambar balok ditarik dengan sudut tertentu.*
- **(29<sub>BS</sub>)** *Wacana bola didorong pada bidang datar, usaha pada bola.*
- **(30)** *Konsep teorema usaha dan energi dalam menentukan energi benda.*