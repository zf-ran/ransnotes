# I. *Problem Solving*

Aio berhasil merancang dua robot yang pintar bermain logika, bernama Robobar dan Robokol. Untuk menguji menguji kecerdasan logika keduanya. Aoi meminta kedua robot bermain teka-teka berikut ini.

Aio memiliki sebuah papan berukuran $6 \times 6$ petak. Papan ini terdiri dari 6 baris yang diberi label 1, 2, 3, 4, 5, dan 6; serta 6 kolom yang diberi label A, B, C, D, E, dan F. Pada papan tersebut juga terdapat beberapa bintang yang diletakkan sebagai berikut.


|     | A   | B   | C   | D   | E   | F   |
| --- | --- | --- | --- | --- | --- | --- |
| 1   |     |     | ★   |     | ★   |     |
| 2   |     | ★   |     | ★   |     |     |
| 3   | ★   |     |     |     | ★   |     |
| 4   |     | ★   |     | ★   |     | ★   |
| 5   |     |     | ★   |     |     |     |
| 6   | ★   |     |     | ★   |     | ★   |

Aoi telah memilih tepat salah satu bintang secara **rahasia**, yang dinamakan **Bintang Aoi**. Aoi ingin kedua robot menemukan di mana letak Bintang Aio. Untuk membantu mereka, Aoi akan memberikan informasi berikut secara terpisah dan sembunyi-sembunyi.

- Aoi memberi tahu **baris** Bintang Aoi kepada **Robobar**.
- Aoi memberi tahu **kolom** Bintang Aoi kepada **Robokol**.

Setelah itu, secara berurutan, terjadi percakapan antarkedua robot sebagai berikut.

- Robobar: Aku tidak tahu di mana letak Bintang Aoi.
- Robokol: Aku tidak tahu di mana letak Bintang Aoi.
- Robobar: Aku tidak tahu di mana letak Bintang Aoi.
- Robokol: Aku tidak tahu di mana letak Bintang Aoi.
- Robobar: Kita bisa saja meneruskan percakapan ini selamanya, bergantian mengatakan "Aku tidak tahu di mana letak Bintang Aoi" dan tidak mungkin ada dari kita yang dapat mengetahui di mana letak Bintang Aoi sesungguhnya.
- Robokol: Aku sekarang tahu di mana letak Bintang Aoi.

Dengan mengasumsikan bahwa kedua robot Aoi dapat berpikir logis secara sempurna, di petak manakah sebenarnya letak Bintang Aoi? Jelaskan!

*Catatan:* Anda tetap akan mendapatkan nilai parsial meskipun pada akhirnya Anda tidak berhasil menemukan secara persis letak Bintang Aoi, namun berhasil mengeliminasi beberapa opsi yang tidak mungkin merupakan Bintang Aoi.

---

# II. *Decision Plot*

Berikut adalah hasil visualisasi *rule-based classifier* sederhana dengan tiga kelas ($0$, $1$, dan $2$) berdasarkan dua fitur $(x_1, x_2)$.

(Gambar plot)

**Soal 2.1.** Tentukan kelas dari titik data yang berada pada koordinat $(8, 3)$.

**Soal 2.2.** Tentukan nilai $x_2$ yang berfungsi sebagai batas pemisah antara kelas $1$ dan kelas $2$. Tuliskan dua angka di belakang koma.

**Soal 2.3.** Diberikan *list* $\mathtt{data}$ berukuran $N = 8$ berikut.


| $x_1$ | $x_2$ |
| ----: | ----: |
|  5.86 |  3.62 |
|  0.53 |  6.51 |
|  9.50 |  5.93 |
|  5.69 |  7.46 |
|  6.28 |  6.20 |
|  2.53 |  1.52 |
|  6.42 |  0.85 |
|  9.29 |  4.36 |

Tentukan masing-masing

- banyaknya titik pada data yang masuk kelas $0$;
- banyaknya titik pada data yang masuk kelas $1$; dan
- banyaknya titik pada data yang masuk kelas $2$.

**Soal 2.4.** Jika sebuah titik dipilih secara acak $(0 \leq x_1, x_2 \leq 10)$, hitung probabilitas bahwa titik tersebut berada pada

- kelas $0$;
- kelas $1$; dan
- kelas $2$.

Tuliskan dua angka di belakang koma.

---

# III. *Squared Hinge Loss*

Tim balap **DeltaRacing** menganalisis **deviasi lateral** mobil terhadap *racing line* pada lima tikungan.

Deviasi lateral adalah jarak penyimpangan mobil secara horizontal dan jalur ideal (*racing line*). Nilai positif berarti mobil terlalu ke kenan, nilai negatif berarti berarti terlalu ke kiri, dan nilai nol berarti mobil tepat berada di jalur ideal.

Nilai deviasi (dalam meter) kita sebut $x$. *Engineer* memberi label biner sebagai berikut.

$$ y = \begin{cases}
	+1, \quad \text{keadaan berbahaya (deviasi terlalu besar)} \\
	-1, \quad \text{keadaan aman (deviasi kecil)}
\end{cases} $$

Singkatnya, berbahaya bisa terjadi jika mobil terlalu ke kiri atau terlalu ke kanan.

## Data

Gunakan data berikut

| $x$    | $y$  |
| ------ | ---- |
| $-2.1$ | $+1$ |
| $-0.7$ | $-1$ |
| $+0.2$ | $-1$ |
| $+0.8$ | $-1$ |
| $+2.2$ | $+1$ |

## Notasi dan Definisi

Model linear satu dimensi

$$ f(x) = wx + b, $$

di mana $w$ dan $b$ adalah bilangan riil, dan $y \in \{-1, +1\}$.

***Squared hinge loss*** per sampel adalah

$$ \ell_i(w, b) = \max\{0, 1  - y_if(x_i)\}^2. $$

*Loss* rata-rata pada $n = 5$ data

$$ L(w, b) = \frac{1}{5} \sum_{i=1}^5 \ell_i(w, b). $$

Aturan pembaruan ***gradient descent*** dengan laju belajar $\eta$

$$
	w' = w - \eta \frac{\partial L}{\partial w}, \quad
	b' = b - \eta \frac{\partial L}{\partial b}.
$$

**Soal 3.1.** Dengan $w = 0$ dan $b = 0$, hitung nilai $L(w, b)$ pada data di atas.

**Soal 3.2.** Turunkan $\frac{\partial L}{\partial w}$ dan $\frac{\partial L}{\partial b}$ untuk *squared hinge loss* pada model $f(x) = wx + b$. Jelaskan perhitungannya.

**Soal 3.3.** Lakukan **satu** langkah *gradient descent* dengan $\eta = 1$ dari $w = 0$ dan $b = 0$. Nyatakan parameter hasil *update* $(w, b)$ dan nilai *loss*-nya setelah *update*.

**Soal 3.4.** Nilai *loss* model saat ini masih $L > 0$. Jika langkah *gradient descent* dilanjutkan berkali-kali, apakah bisa mencapai $L = 0$? Jelaskan alasan Anda secara konseptual.

**Soal 3.5.** Sekarang ganti fitur menjadi $z = x^2$ dan model menjadi $f(z) = wz + b$. Apakah mungkin mencapai $L = 0$? Jelaskan alasan Anda secara singkat.

**Soal 3.6.** *Notasi iterasi.* Gunakan notasi $w^{(t)}$ dan $b^{(t)}$ untuk menyatakan parameter setelah $t$ pembaruan *gradient descent*. Misal $w^{(1)}$ adalah setelah satu pembaruan.

Mulai dari $w^{(0)} = 0$ dan $b^{(0)}$ pada ruang fitur $z = x^2$ seperti Soal 5 dan gunakan $\eta = 1$. Lakukan *gradient descent* sebanyak 2 iterasi dan hitung $w^{(t)}$, $b^{(t)}$, dan $L\left(w^{(t)}, b^{(t)}\right)$ untuk $t = 1$ dan $t = 2$.

---

# IV. *Probability*

Dalam bidang Kecerdasan Buatan, sebuah model dapat memprediksi kata berikutnya dalam sebuah kalimat berdasarkan pola probabilitas. Prinsip dasarnya sama dengan teori peluang: menghitung kemungkinan suatu kejadian berdasarkan data sebelumnya.

Misalnya, jika dalam banyak kalimat berbahasa Indonesia kata *saya* sering diikuti kata *makan*, maka peluang munculnya kata *makan* setelah *saya* akan lebih tinggi dibanding kata lain. Konsep ini mirip dengan statistik frekuensi kata, yang dapat dianalisis dengan aturan peluang bersyarat (*conditional probability*).

Seorang arkeolog menemukan naskah bahasa kuno yang akan dianalisis polanya menggunakan sebuah model. Ia juga menemukan bahwa kemunculan sebuah kata hanya bergantung pada kata sebelumnya, dan tidak pada kata-kata lebih awal. Sang arkeolog mencatat frekuensi urutan kata sebagai berikut.

- Kata *lura* diikuti oleh
	- *domi* pada 48 kalimat;
	- *salu* pada 27 kalimat; dan
	- *tano* pada 25 kalimat.
- Kata *kira* diikuti oleh
	- *domi* pada 42 kalimat;
	- *raka* pada 33 kalimat; dan
	- *salu* pada 25 kalimat.

**Soal 4.1.** Pada suatu naskah, ada kalimat di mana kata pertama disembunyikan, dan hanya kata kedua yang terlihat.

- Jika kata kedua adalah *domi*, berapakah peluang kata pertama yang tersembunyi adalah *lura*?
- Jika kata kedua adalah *salu*, berapakah peluang kata pertama yang tersembunyi adlaah *kira*?

**Soal 4.2.** Arkeolog kemudian mengambil secara acak 10 kalimat dari naskah. Diketahui bahwa setiap kalimat tersebut memiliki kata kedua *domi*. Berapakah peluang bahwa tepat 6 kalimat memiliki kata pertama *lura*?

---

# V. *Feature Extraction*

Dalam sebuah eksperimen *computer vision*, setiap gambar disimpan sebagai matriks biner berukuran $5 \times 5$, di mana nilai $1$ menandai piksel berwarna putih dan nilai $0$ menandai piksel berwarna hitam.

Pada eksperimen tersebut, dua buah gambar dipilih menjadi acuan (*anchor*), yakni $A_1$ dan $A_2$. Selain itu, eksperimen tersebut juga memiliki sepuluh gambar uji, $T_1$, $T_2$, ..., $T_{10}$, di mana setiap gambar uji pasti berasal dari salah satu kelas $A_1$ atau $A_2$. Perhatikan bahwa gambar uji mungkin mengalami rotasi, pergeseran, atau kesalahan akibat *noise*.

Anda diberi tugas oleh ketua peneliti untuk merancang fitur-fitur numerik sederhana dari matriks dan menggunakannya untuk menentukan *anchor* mana yang paling sesuai bagi tiap gambar uji.

## Contoh Ekstraksi Fitur

Sebuah fitur sederhana bernama **kolom penuh bernilai satu** menandakan kelima entri pada kolom tersebut bernilai $1$. Secara formal, kolom ke-$j$ disebut penuh jika

$$ \sum_{i=1}^5 M_{i,j} = 5. $$

Tentu, **baris penuh bernilai nol** dapat dihitung menggunakan rumus

$$ \sum_{j=1}^5 M_{i,j} = 0. $$

Anda bebas mendefinisikan fitur sederhana lain yang berguna, selama dihitung langsung dari entri-entri matriks.

**Soal 5.1.** Untuk setiap gambar uji $T_i$ putuskan apakah ia termasuk kelas $A_1$ atau $A_2$.

**Soal 5.2.** Daftarkan fitur-fitur yang benar-benar Anda gunakan saat membuat keputusan.

**Soal 5.3.** Tuliskan aturan keputusan Anda secara tepat dalam kalimat atau rumus singkat. Jelaskan bagaimana label $A_1$ atau $A_2$ dipilih untuk tiap-tiap $T_i$ saat diberikan nilai-nilai fitur-fitur yang sudah Anda buat.

## *Anchors*

$$ \begin{gather*}
	A_1 = \begin{bmatrix}
		1 & 0 & 1 & 0 & 1 \\
		1 & 0 & 1 & 0 & 1 \\
		1 & 0 & 1 & 0 & 1 \\
		1 & 0 & 1 & 0 & 1 \\
		1 & 0 & 1 & 0 & 1
	\end{bmatrix}, \\
	
	A_2 = \begin{bmatrix}
		1 & 0 & 1 & 0 & 1 \\
		0 & 1 & 0 & 1 & 0 \\
		1 & 0 & 1 & 0 & 1 \\
		0 & 1 & 0 & 1 & 0 \\
		1 & 0 & 1 & 0 & 1
	\end{bmatrix}
\end{gather*} $$

## *Tests*

[TODO]

---

# VI. *Confusion Matrix*

## Binary Classification Overview

Dalam masalah klasifikasi biner, model AI memberikan skor antara $0$ sampai $1$ untuk setiap data. Skor ini menunjukkan seberapa besar kemungkinan data tersebut termasuk ke kelas positif (misalnya pasien sakit). Untuk mengambil keputusan, kita menentukan ***treshold*** (ambang batas). Jika *treshold* adalah $0.5$, maka data dengan skor yang lebih besar dari $0.5$ diklasifikasi sebagai positif, sisanya negatif. Pemilihan *treshold* harus disesuaikan dengan konteks nyata, terutama saat data tidak seimbang. Evaluasi model dilakukan menggunakan berbagai metrik berikut.

## Struktur *Confusion Matrix*

|                | Prediksi Positif                 | Prediksi Negatif                 |
| -------------- | -------------------------------- | -------------------------------- |
| Aktual Positif | *True Positive* $(\mathrm{TP})$  | *False Negative* $(\mathrm{FN})$ |
| Aktual Negatif | *False Positive* $(\mathrm{FP})$ | *True Negative* $(\mathrm{TN})$  |

## Metrik Evaluasi

- ***Accuracy*.** Proposisi prediksi yang benar secara keseluruhan.
	$$ \text{Accuracy} = \frac{\mathrm{TP} + \mathrm{TN}}{\mathrm{TP} + \mathrm{TN} + \mathrm{FP} + \mathrm{FN}}. $$
- ***Precision*.** Proposisi prediksi positif yang benar-benar benar.
	$$ \text{Precision} = \frac{\mathrm{TP}}{\mathrm{TP} + \mathrm{FP}}. $$
- ***Recall* (*Sensitivity*).** Kemampuan model mengenali semua kasus positif yang sebenarnya.
	$$ \text{Recall} = \frac{\mathrm{TP}}{\mathrm{TP} + \mathrm{FN}}. $$
- **F1-*score*.** Rata-rata harmonik antara *precision* dan *recall*. Berguna ketika kita ingin menyeimbangkan kedua metrik *precision* dan *recall*.
	$$ \text{F1} = 2 \times \frac{\text{Precision} \times \text{Recall}}{\text{Precision} + \text{Recall}}. $$
- **F1-*macro*.** Rata-rata aritmatika dari skor F1 untuk setiap kelas secara individual dalam tugas klasifikasi multikelas, dengan memberikan bobot yang sama untuk semua kelas.
	$$ \text{F1}\_\text{macro} = \frac{\text{F1}\_\text{positif} + \text{F1}\_\text{negatif}}{2}. $$
- **F1-*micro*.** Menghitung F1 secara global berdasarkan total TP, FP, dan FN dari seluruh kelas, sehingga mempertimbangkan komtribusi setiap kelas sesuai dengan jumlah datanya.
	$$ \text{F1}\_\text{micro} = \frac{2 \times \text{TP}\_\text{total}}{2 \times \text{TP}\_\text{total} + \text{FP}\_\text{total} + \text{FN}\_\text{total}}. $$

Sebuah rumah sakit sedang mengembangkan sistem AI untuk membantu dokter dalam mendeteksi penyakit langka namun berbahaya berdasarkan hasil tes darah. Sistem AI ini memberikan diagnosis awal, berupa dua kemungkinan.

1. Sakit (Positif).
2. Sehat (Negatif).

Kondisi penyakit ini **sangat langka**. Secara statistik, dari 1000 pasien yang diperiksa,

- hanya sekitar **10 pasien** yang benar-benar menderita penyakit tersebut; dan
- sebanyak **990** pasien lainnya dalam kondisi sehat.

Setelah dilakukan pengujian awal terhadap sistem AI, ditemukan dua masalah kritis sebagai berikut.

- **Diagnostis terlewat (fatal).** Beberapa pasien yang sebenarnya sakit justru didiagnosis sehat oleh sistem AI. Hal ini sangat berbahaya karena pasien tidak akan mendapatkan pengobatan yang diperlukan sehingga penyakitnya dapat berkembang lebih parah.
- **Diagnosis salah (merugikan).**  Sebaliknya, terdapat pula pasien yang sebenarnya sehat tetapi didiagnosis sakit. Kesalahan ini dapat menyebabkan stres emosional, biaya lanjutan yang tinggi (misalnya tes lanjutan seperti biopsi), serta risiko efek samping dari pengobatan yang tidak perlu.

Rumah sakit membutuhkan cara untuk mengukur performa sistem AI secara adil sehingga kedua jenis kesalahan di atas dapat diperhatikan secara seimbang. Metrik evaluasi apa yang paling tepat digunakan untuk mengukur kinerja sistem AI ini agar kedua masalah tersebut dapat diminimalkan? Jelaskan alasanmu.

---

# VII. *Matrices*

Perhatikan beberapa konsep dan definisi terkait matriks berikut. $\newcommand{\v}[1]{\mathbf{#1}}$

**Vektor eigen dan nilai eigen.** Misal ada sebuah matriks persegi berukuran $n \times n$, $A$, dan juga ada sebuah vektor tidak kosong $\v v$ yang mempunyai panjang $n$. Jika persamaan

$$ A \v v = \lambda \v v $$

terpenuhi, dengan $\lambda$ adalah sebuah skalar, maka $\v v$ disebut dengan **vektor eigen** (*eigenvector*) dan $\lambda$ disebut sebagai **nilai eigen** (*eigenvalue*).

Sebagai contoh, untuk matriks

$$ A = \begin{bmatrix}
	-6 & 3 \\
	4 & 5
\end{bmatrix}, $$

ada dua pasang vektor eigen dan nilai eigen dari $A$, yaitu

$$ \begin{gather*}
	\v v_1 = \begin{bmatrix}
		1 \\
		4
	\end{bmatrix}, \quad \lambda_1 = 6; \\
	\v v_2 = \begin{bmatrix}
		-3 \\
		1
	\end{bmatrix}, \quad \lambda_2 = -7.
\end{gather*} $$

Jadi, vektor eigen dan nilai eigen dari sebuah matriks bersifat tidak unik atau bisa lebih dari satu pasang. Dalam Aljabar Linear, proses perkalian matriks dengan vektor seperti $A\v v$ sebenarnya disebut dengan **transformasi linier**, yaitu melakukan pemindahan vektor $\v v$ ke ruang vektor lain dengan tetap menjaga struktur liniernya. Dalam konteks vektor eigen, vektor eigen adalah sebuah vektor yang jika dilakukan transformasi linier dengan matriks $A$, ia **tidak berubah arah**, hanya memanjang atau memendek saja.

**Matriks diagonal.** Sebuah matriks persegi $A$ adalah matriks diagonal jika sebuah entri bernilai $0$ kecuali bagian diagonal utama. Berikut adalah beberapa contoh matriks diagonal.

$$
	I = \begin{bmatrix}
		1 & 0 \\
		0 & 1
	\end{bmatrix}, \quad
	A = \begin{bmatrix}
		6 & 0 & 0 \\
		0 & 5 & 0 \\
		0 & 0 & 3
	\end{bmatrix}, \quad
	B = \begin{bmatrix}
		1 & 0 & 0 & 0 \\
		0 & 9 & 0 & 0 \\
		0 & 0 & 3 & 0 \\
		0 & 0 & 0 & 5
	\end{bmatrix}.
$$

**Diagonalisasi matriks.** Matriks persegi $A$ berukuran $n \times n$ dapat didiagonalisasi jika dan hanya jika terdapat matriks singular (memiliki *inverse*) $P$ sehingga

$$ A = PDP^{-1}, $$

dengan $D$ adalah matriks diagonal.

**Soal 7.1.** Carilah vektor eigen dan nilai eigen dari matriks

$$ \begin{bmatrix}
	1 & 2 \\
	5 & 4
\end{bmatrix}. $$

Petunjuk.

$$ \begin{align*}
	A \v v &= \lambda \v v \\
	A \v v - \lambda \v v &= \v 0 \\
	(A - \lambda I) \v v &= \v 0
\end{align*} $$

Karena $\v v$ bukanlah vektor $\v 0$, maka

$$ |A - \lambda I| = 0, $$

di mana

- $I$ adalah matriks identitas $n \times n$;
- $|M|$ adalah determinan matriks $M$;
- $\v 0$ adalah vektor berisi $0$.

**Soal 7.2.** Buktikan bahwa jika sebuah matriks $A$ berukuran $2 \times 2$ dapat didiagonalisasi dengan $A = PDP^{-1}$ atau jika dijabarkan,

$$ \begin{bmatrix}
	a_{1,1} & a_{1,2} \\
	a_{2,1} & a_{2,2}
\end{bmatrix} = \begin{bmatrix}
	p_{1,1} & p_{1,2} \\
	p_{2,1} & p_{2,2}
\end{bmatrix} \begin{bmatrix}
	d_1 & 0 \\
	0 & d_2
\end{bmatrix} \begin{bmatrix}
	p_{1,1} & p_{1,2} \\
	p_{2,1} & p_{2,2}
\end{bmatrix}^{-1}, $$

di mana $\begin{bmatrix} p_{1,1} \\ p_{2,1} \end{bmatrix}$ dan $d_1$; serta $\begin{bmatrix} p_{1,2} \\ p_{2,2} \end{bmatrix}$ dan $d_2$ adalah pasangan vektor eigen dan nilai eigen dari matriks $A$.

*Pembuktian.* Untuk nilai eigen $d_1$, didapati

$$ A \begin{bmatrix}
	p_{1,1} \\
	p_{2,1}
\end{bmatrix} = d_1 \begin{bmatrix}
	p_{1,1} \\
	p_{2,1}
\end{bmatrix}. $$

Bila dijabarkan,

$$ \begin{align*}
	\begin{bmatrix}
		a_{1,1} & a_{1,2} \\
		a_{2,1} & a_{2,2}
	\end{bmatrix} \begin{bmatrix}
		p_{1,1} \\
		p_{2,1}
	\end{bmatrix} &= d_1 \begin{bmatrix}
		p_{1,1} \\
		p_{2,1}
	\end{bmatrix} \\
	\begin{bmatrix}
		a_{1,1} p_{1,1} + a_{1,2} p_{2,1} \\
		a_{2,1} p_{1,1} + a_{2,2} p_{2,1}
	\end{bmatrix} &= \begin{bmatrix}
		d_1 p_{1,1} \\
		d_1 p_{2,1}
	\end{bmatrix}
\end{align*} $$

Sekarang, untuk nilai eigen $d_2$, didapati

$$ A \begin{bmatrix}
	p_{1,2} \\
	p_{2,2}
\end{bmatrix} = d_2 \begin{bmatrix}
	p_{1,2} \\
	p_{2,2}
\end{bmatrix}. $$

Jabarkan seperti sebelumnya,

$$ \begin{align*}
	\begin{bmatrix}
		a_{1,1} p_{1,2} + a_{1,2} p_{2,2} \\
		a_{2,1} p_{1,2} + a_{2,2} p_{2,2}
	\end{bmatrix} &= \begin{bmatrix}
		d_2 p_{1,2} \\
		d_2 p_{2,2}
	\end{bmatrix}
\end{align*} $$

Jika kedua vektor sama, maka entri-entri yang bersesuaian tentu sama.

$$ \begin{cases}
	a_{1,1} p_{1,1} + a_{1,2} p_{2,1} = d_1 p_{1,1} \\
	a_{2,1} p_{1,1} + a_{2,2} p_{2,1} = d_1 p_{2,1} \\
	a_{1,1} p_{1,2} + a_{1,2} p_{2,2} = d_2 p_{1,2} \\
	a_{2,1} p_{1,2} + a_{2,2} p_{2,2} = d_2 p_{2,2}
\end{cases} $$


Pada persamaan $A = PDP^{-1}$, kalikan matriks $P$ kedua sisi. Menjadi $AP = PDP^{-1}P$, karena $P^{-1}P = I$, maka $AP = PD$. Bila dijabarkan,

$$ \begin{align*}
	\begin{bmatrix}
		a_{1,1} & a_{1,2} \\
		a_{2,1} & a_{2,2}
	\end{bmatrix}
	\begin{bmatrix}
		p_{1,1} & p_{1,2} \\
		p_{2,1} & p_{2,2}
	\end{bmatrix} &=
	\begin{bmatrix}
		p_{1,1} & p_{1,2} \\
		p_{2,1} & p_{2,2}
	\end{bmatrix}
	\begin{bmatrix}
		d_1 & 0 \\
		0 & d_2
	\end{bmatrix} \\
	\begin{bmatrix}
		a_{1,1} p_{1,1} + a_{1,2} p_{2,1} &
		a_{1,1} p_{1,2} + a_{1,2} p_{2,2} \\
		a_{2,1} p_{1,1} + a_{2,1} p_{2,1} &
		a_{2,1} p_{1,2} + a_{2,2} p_{2,2}
	\end{bmatrix} &= \begin{bmatrix}
		d_1 p_{1,1} & d_2 p_{1,2} \\
		d_1 p_{2,1} & d_2 p_{2,2}
	\end{bmatrix}.
\end{align*} $$

Entri-entri pada matriks di ruas kiri dapat disubstitusikan seperti persamaan-persamaan di atas, menjadi sama dengan ruas kanan.