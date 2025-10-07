$$
	\newcommand{\b}[1]{\mathbf{#1}}
	\newcommand{\RR}{\mathbb{R}}
	\newcommand{\n}[1]{\|#1\|}
	\newcommand{\i}{\boldsymbol{\hat \imath}}
	\newcommand{\j}{\boldsymbol{\hat \jmath}}
	\newcommand{\k}{\boldsymbol{\hat k}}
$$

Besaran skalar adalah besaran yang hanya memiliki nilai.

Besaran vektor adalah besaran yang memiliki nilai dan arah.

# A. Notasi

Vektor ditandai dengan huruf kecil, dengan beberapa standar:

1. Tegak, **tebal**
	$$ \b v $$
2. *Miring*, dengan panah di $\vec{\text{atasnya}}$:
	$$ \vec v $$
3. Tegak, **tebal**, dengan panah di $\vec{\text{atasnya}}$:
	$$ \b{\vec{v}} $$

Notasi yang akan dipakai pada dokumen ini adalah nomor 1, tegak, **tebal**, tanpa panah di atasnya.

## A.1. Notasi Komponen

Ada beberapa cara untuk merepresentasikan vektor $\mathbb{R}^n$:

1. **Koordinat Polar**,  
	yaitu koordinat yang memiliki satu komponen panjang atau besaran ($r \in \RR^+$), dan $n - 1$ komponen sudut ($\angle \theta$). 
	
	Saya akan menulis koordinat polar dengan
	$$ \langle r, \theta_1, \theta_2, \dots \rangle $$
	di mana $r$ adalah besaran dan $\theta_1, \theta_2, \dots$ adalah sudut-sudut vektor.
	
	 Misalkan pada ruang $\RR^2$, koordinat polar akan memiliki satu besaran dan satu sudut, contohnya $\langle 3\;\mathrm{cm}, 45^\circ \rangle$.
1. **Koordinat Kartesius**,  
	yaitu koordinat yang memiliki komponen panjang pada sumbu-sumbu di ruang tersebut.
	
	Saya akan menulis koordinat kartesius dengan
	$$ (a_x, a_y, \dots) $$
	di mana $a_x$ adalah komponen $x$, dan $a_y$ adalah komponen $y$ dari vektor $\b a$.
	
	Misalkan pada ruang $\RR^2$, maka vektor akan memiliki komponen $(x, y)$. Pada ruang $\RR^3$ akan memiliki komponen $(x, y , z)$. Pada ruang $\RR^n$ akan memiliki komponen $(a_1, a_2, \dots, a_{n-1}, a_n)$.

## A.2. Mengubah Polar ke Kartesius

Diketahui vektor $\b v = \langle r, \theta \rangle$, maka

- komponen $x$-nya adalah $r \cos \theta$, karena
	$$ \cos = \frac{\text{samping}}{\text{miring}}. $$
- komponen $y$-nya adalah $r \sin \theta$, karena alasan yang sama.

Didapat

$$ \b v = (v_x, v_y) = (r \cos \theta, r \sin \theta). $$

## A.3. Mengubah Kartesius ke Polar

TK

## A.4. Vektor Satuan

Vektor satuan memiliki panjang satu satuan, ia digunakan untuk menunjukkan arah suatu vektor. Vektor satuan dilambangkan dengan tanda `^` di atasnya, seperti $\b{\hat v}$.

Selain menggunakan koordinat kartesius $(x, y, z)$, kita dapat membuat vektor satuan $\i$ yang melambangkan arah sumbu $x$, vektor satuan $\j$ yang melambangkan arah sumbu $y$, dan vektor satuan $\k$ yang melambangkan arah sumbu $z$:

$$ \i = (1, 0, 0), \quad \j = (0, 1, 0), \quad \k = (0, 0, 1). $$

Misalkan vektor $\b p = (3, 4, 5)$, maka kita dapat menulisnya sebagai

$$ \b p = 3\i + 4\j + 5\k. $$

# B. Norma

Norma vektor adalah besaran vektor. Misalkan vektor $\b a$, maka $\| \b a \|$ adalah besarannya.

Pada koordinat polar, norma vektor $\b v$ adalah komponen besarannya itu sendiri. Misalkan $\b v = \langle 17, \angle 30^\circ \rangle$, maka $\| \b v \| = 17$.

Pada koordinat kartesius, norma vektor $\b k$ adalah akar dari jumlah kuadrat komponennya.

Misal vektor dalam ruang $\RR^3$

$$ \b v = (10, 2, 11), $$

maka $\| \b v \|$ adalah

- akar
	$$ \sqrt{\square} $$
- jumlah
	$$ \square + \square + \square $$
- kuadrat
	$$ \square^2 $$
- komponen-komponennya
	$$ 10, 2, 11 $$

Diselesaikan

$$ \begin{align*}
	\| \b v \| &= \sqrt{10^2 + 2^2 + 11^2} \\
	&= \sqrt{225} \\
	&= 15.
\end{align*} $$

Dari mana asalnya? Dari teorema Pythagoras.

# C. Operasi Vektor

## C.1. Penjumlahan Dua Vektor

### C.1.1. Koordinat Kartesius

Pada penjumlahan vektor dalam bidang kartesius, cukup tambahkan komponen yang setempat.

$$ \begin{align*}
	\b a &= (a_x, a_y) \\
	\b b &= (b_x, b_y) \\
	\b a + \b b &= (a_x + b_x, a_y+b_y).
\end{align*} $$

Sama untuk vektor $\RR^3$ dan seterusnya.

### C.1.2. Koordinat Polar

Ada dua cara untuk mencari jumlah vektor, yaitu menggunakan trigonometri, atau mengubahnya menjadi koordinat kartesius.

#### C.1.2.1. Trigonometri

Misalkan ada dua vektor $\b a$ dan $\b b$ di ruang $\RR^2$,

$$ \begin{align*}
	\b a &= (a, \angle\theta_1) \\
	\b b &= (b, \angle\theta_2) \\
	\b a + \b b = \b r &= (r, \angle\Phi).
\end{align*} $$

Dan misalkan sudut $\psi$ adalah sudut yang mengapit kedua vektor tersebut, $\psi = \theta_1 - \theta_2$.

Maka didapat (dari aturan kosinus)

$$ r^2 = a^2 + b^2 + 2ab \cos \psi. $$

Bentuklah segitiga dengan sisi-sisi $\b a$, $\b b$, dan $\b r$. Misalkan sudut-sudut

- $\alpha$ berhadapan dengan $\b a$; dan
- $\beta$ berhadapan dengan $\b b$.

Maka sudut yang berhadapan dengan $\b r$ adalah $180 - \psi$.

Maka didapat (dari aturan sinus)

$$ \frac{r}{\sin(180^\circ - \psi)} = \frac{a}{\sin \alpha} = \frac{b}{\sin \beta}. $$

karena $\sin(180^\circ - x) = \sin x$, maka

$$ \frac{r}{\sin\psi} = \frac{a}{\sin \alpha} = \frac{b}{\sin \beta}. $$

Diketahui

$$ \Phi = \theta_1 - \beta = \theta_2 + \alpha, $$

$$ \therefore \alpha = \Phi - \theta_2, \quad \beta = \theta_1 - \Phi $$

Substitusikan $\alpha$ dan $\beta$.

$$ \frac{r}{\sin\psi} = \frac{a}{\sin(\Phi - \theta_2)} = \frac{b}{\sin(\theta_1 - \Phi)}. $$

Maka bentuk umum arah dari penjumlahan dua vektor adalah

$$ \Phi = \theta_2 + \sin^{-1}\left(\frac{a \sin \psi}{r}\right) = \theta_1 - \sin^{-1}\left(\frac{b \sin \psi}{r}\right). $$

Di dapat hasil akhir

$$ \b a + \b b = \langle r, \Phi \rangle. $$

#### C.1.2.2. Kartesius

Misalkan ada dua vektor $\b a$ dan $\b b$ di ruang $\RR^2$,

**Polar:**

$$ \begin{align*}
	\b a &= \langle a, \alpha \rangle \\
	\b b &= \langle b, \beta \rangle \\
	\b a + \b b = \b r &= \langle r, \Phi \rangle,
\end{align*} $$

**Kartesius:**

$$  \begin{align*}
	\b a &= (a_x, a_y) \\
	\b b &= (b_x, b_y) \\
	\b a + \b b = \b r &= (r_x, r_y).
\end{align*} $$

Pertama-tama, cari masing-masing komponen $x$ dan $y$ dari vektor $\b a$ dan $\b b$ (lihat: [[#A.2. Merubah Polar ke Kartesius]]).

$$ \begin{align*}
	a_x &= \n{\b a} \cos \alpha \\
	a_y &= \n{\b a} \sin \alpha, \\\\
	
	b_x &= \n{\b b} \cos \beta \\
	b_y &= \n{\b b} \sin \beta.
\end{align*} $$

Maka jumlahkan kedua vektor tersebut seperti cara menambahkan kedua vektor kartesius: *jumlahkan komponen-komponen yang setempat*.

$$ \begin{align*}
	r_x &= a_x + b_x \\
	r_y &= a_y + b_y \\
	\therefore \b r &= (a_x + b_x, a_y + b_y).
\end{align*} $$

Didapat panjang $\b r$ adalah normanya, yaitu

$$ \n{\b r} = r = \sqrt{r_x^2 + r_y^2}. $$

Sekarang untuk mencari sudutnya, gunakan $\tan$ (lebih tepat inversnya), karena $\tan = \text{depan}/\text{samping},$ di mana depan adalah $r_y$ dan samping adalah $r_x$.

$$ \begin{align*}
	\tan \Phi &= \frac{r_y}{r_x} \\
	&= \tan^{-1}\left(\frac{r_y}{r_x}\right).
\end{align*} $$

Namun, perlu hati-hati, karena $\tan^{-1}$ memiliki range di antara $-90^\circ$ dan $90^\circ$. Bisa jadi sudut kita lebih dari $90^\circ$ dan kurang dari $-90^\circ$.

Didapatlah hasil akhir

$$ \b r = \langle r, \Phi \rangle. $$

## C.2. Perkalian

Ada dua tipe perkalian, yaitu perkalian dengan skalar, dan dengan vektor lain.

Untuk perkalian vektor dengan vektor, ada dua tipe lagi, yaitu perkalian titik (*dot product*), dan perkalian silang *(cross product)*.

### C.2.1. Perkalian dengan Skalar

Untuk bilangan $k \in \RR$ dan vektor $\b v = (v_x, v_y) = \langle r, \theta \rangle$, maka

$$ k \b v = (kv_x, kv_y) = \langle kr, \theta \rangle. $$

### C.2.2. Perkalian Titik

> [!note] Perlu diperhatikan bahwa perkalian titik dua vektor menghasilkan sebuah skalar.

Perkalian titik menghasilkan panjang vektor pertama yang diproyeksikan ke vektor kedua dikali dengan panjang vektor kedua (atau sebaliknya, vektor kedua yang diproyeksikan ke vektor pertama).

Dalam koordinat kartesius, perkalian titik adalah jumlah dari perkalian komponen yang setempat.

$$ \begin{align*}
	\b a &= (a_x, a_y) = \langle a, \alpha \rangle \\
	\b b &= (b_x, b_y) = \langle b, \beta \rangle \\\\
	
	\b a \cdot \b b &= a_xb_x + a_yb_y = ab \cos \theta,
\end{align*} $$

di mana $\theta$ adalah sudut di antara kedua vektor, atau $\theta = \alpha - \beta$.

### C.2.3. Perkalian Silang

> [!note] Perkalian silang pada ruang $\RR^2$ akan menghasilkan vektor pada ruang $\RR^3$.

> [!warning] Perlu diperhatikan bahwa perkalian silang *tidak komutatif*: $\b a \times \b b = - \b b \times \b a.$

Perkalian silang $\b a \times \b b$ menghasilkan vektor yang tegak lurus dengan kedua vektor $\b a$ dan $\b b$ dengan panjang $\n{\b a} \n{\b b} \sin \theta$ di mana $\theta$ adalah sudut apit antara vektor $\b a$ dan $\b b$.

Untuk dua vektor $\b a = (a_x, a_y, a_z)$ dan $\b b = (b_x, b_y, b_z)$, perkalian silangnya adalah

$$ \begin{align*}
	\b a \times \b b &= \begin{vmatrix}
		\i & \j & \k \\
		a_x & a_y & a_z \\
		b_x & b_y & b_z
	\end{vmatrix} \\
	&= \begin{vmatrix} a_y & a_z \\ b_y & b_z \end{vmatrix} \i
	+ \begin{vmatrix} a_x & a_z \\ b_x & b_z \end{vmatrix} \j
	+ \begin{vmatrix} a_x & a_y \\ b_x & b_y \end{vmatrix} \i \\
	&= (a_yb_z - a_zb_y)\i + (a_xb_z - a_xb_x)\j + (a_xb_y - a_yb_x)\k.
\end{align*} $$

