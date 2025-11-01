$\newcommand{\b}[1]{\mathbf{#1}}$

Matriks adalah susunan bilangan (entri) dalam kolom dan baris, variabel matriks ditulis dengan huruf kapital tebal. Matriks dapat ditulis dengan $[\dots]$ atau $(\dots)$. Misalnya matriks $\b A$,

$$ \b A = \begin{bmatrix} a & b & c \\ x & y & z \end{bmatrix}. $$

Matriks $\b A$ memiliki 2 baris dan 3 kolom, maka matriks $\b A$ **berukuran** (berordo) $2 \times 3$, atau dapat ditulis $\b A_{2\times3}$. Ukuran matriks $\b M$ ditulis sebagai $\b M_{\text{baris}\times\text{kolom}}$.

# Matriks Persegi

Sebuah matriks disebut sebagai **matriks persegi** jika banyak baris dan banyak kolomnya sama, contohnya matriks $\b M_{3\times3}$,

$$ \b M = \begin{bmatrix} a & b & c \\ d & e & f \\ g & h & i \end{bmatrix}. $$

# Matriks Identitas

Untuk matriks persegi $\b A$, ada sebuah **matriks identitas** $\b I$ yang di mana

$$ \b I \b A = \b A \b I = \b A. $$

Notasi $\b I \b A$ melambangkan perkalian matriks $\b I$ dan matriks $\b A$,  (lihat: [[#Perkalian Matriks dengan Matriks]]).

Matriks identitas tersebut adalah matriks yang entri pada diagonal utama (dari kiri atas ke kanan bawah) bernilai $1$, dan selainnya $0$.

Didapat identitas matriks $2\times2$ adalah

$$ \b I_{2\times2} = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}. $$

Dan untuk identitas matriks $3\times3$ adalah

$$ \b I_{3\times3} = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}. $$

# Operasi Matriks

Notasi entri matriks $\b A$ pada baris $i$ dan kolom $j$ akan ditulis sebagai $\b A_{i,j}$, atau dapat dijabarkan sebagai berikut.

$$ \b A_{n \times m} =
\begin{bmatrix}
	\b A_{1,1} & \b A_{1,2} & \b A_{1,3} & \cdots & \b A_{1,m} \\
	\b A_{2,1} & \b A_{2,2} & \b A_{2,3} & \cdots & \b A_{2,m} \\
	\b A_{3,1} & \b A_{3,2} & \b A_{3,3} & \cdots & \b A_{3,m} \\
	\vdots & \vdots & \vdots & \ddots & \vdots \\
	\b A_{n,1} & \b A_{n,2} & \b A_{n,3} & \cdots & \b A_{n,m}
\end{bmatrix}. $$

## Transpos Matriks

Transpos matriks adalah sebuah operator yang mengubah setiap baris menjadi kolom, dan setiap kolom menjadi baris. Transpos matriks $M$ adalah $M^\top$.

Misalkan matriks $\b M$ adalah

$$ \b M = \begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix}, $$

maka transpos matriks $\b M$ adalah

$$ \b M^\top = \begin{bmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{bmatrix}. $$

> [!info] Sifat
> - $(\b A \b B)^\top = \b B^\top \b A^\top$

## Penjumlahan Matriks

Syarat untuk menjumlahkan dua matriks adalah kedua matriks tersebut berukuran sama. Misalkan matriks $\b A_{n \times n}$, matriks $\b B_{n \times n}$, dan matriks $\b R = \b A + \b B$, maka

$$ \b R_{i,j} = \b A_{i,j} + \b B_{i,j}. $$

Sifat ini juga berlaku untuk pengurangan.

> [!summary] Penjumlahan Dua Matriks
> Misal matriks $\b A_{n \times m}$ dan matriks $\b B_{n \times m}$, maka $\b A + \b B$ adalah
> 
> $$ \begin{bmatrix}
> 	\b A_{1,1} & \b A_{1,2} & \cdots \\
> 	\b A_{2,1} & \b A_{2,2} & \cdots \\
> 	\vdots  & \vdots  & \ddots
> \end{bmatrix} + \begin{bmatrix}
> 	\b B_{1,1} & \b B_{1,2} & \cdots \\
> 	\b B_{2,1} & \b B_{2,2} & \cdots \\
> 	\vdots  & \vdots  & \ddots
> \end{bmatrix} = \begin{bmatrix}
> 	\b A_{1,1} + \b B_{1,1} & \b A_{1,2} + \b B_{1,2} & \cdots \\
> 	\b A_{2,1} + \b B_{2,1} & \b A_{2,2} + \b B_{2,2} & \cdots \\
> 	\vdots  & \vdots  & \ddots
> \end{bmatrix}. $$

## Perkalian Matriks

### Perkalian Matriks dengan Bilangan

Misalkan matriks $\b M$, bilangan $k$, dan matriks $\b N$ sehingga $\b N = k \b M$, maka

$$ \b N_{i,j} = k \b M_{i,j}. $$

> [!summary] Perkalian Matriks dengan Bilangan
> Untuk matriks $\b M$ dan bilangan $k$, maka $k \b M$ adalah
> 
> $$ k \begin{bmatrix}
> 	\b M_{1,1} & \b M_{1,2} & \cdots \\
> 	\b M_{2,1} & \b M_{2,2} & \cdots \\
> 	\vdots  & \vdots  & \ddots
> \end{bmatrix} = \begin{bmatrix}
> 	k \b M_{1,1} & k \b M_{1,2} & \cdots \\
> 	k \b M_{2,1} & k \b M_{2,2} & \cdots \\
> 	\vdots  & \vdots  & \ddots
> \end{bmatrix}. $$

### Perkalian Matriks dengan Matriks

Syarat untuk mengalikan dua matriks $\b A$ dan $\b B$ adalah banyak ***kolom*** matriks $\b A$ **harus sama** dengan banyak ***baris*** matriks $\b B$,

- $\b A_{p \times q}$
- $\b B_{q \times r}$.

Misalkan hasil perkalian matriks $\b A$ dan $\b B$ adalah matriks $\b R$, maka $\b R$ berukuran $p \times r$.

$$ \b R_{i,j} = \b A_{i,1} \b B_{1,j} + \b A_{i,2} \b B_{2,j} + \cdots + \b A_{i,n} \b B_{n,j}. $$

Pada baris $i$ kolom $j$ matriks $\b C$, fokuslah pada baris $i$ pada matriks $\b A$ dan kolom $j$ pada matriks $\b B$.

> [!warning] Perlu diperhatikan bahwa $AB$ tidak selalu sama dengan $BA$.

> [!summary] Perkalian Matriks 3×2 dengan Matriks 2×3
> $$ \begin{bmatrix}
> 	a_{1,1} & a_{1,2} \\
> 	a_{2,1} & a_{2,2} \\
> 	a_{3,1} & a_{3,2}
> \end{bmatrix} \begin{bmatrix}
> 	b_{1,1} & b_{1,2} & b_{1,3} \\
> 	b_{2,1} & b_{2,2} & b_{2,3}
> \end{bmatrix} \\ 
> = \begin{bmatrix}
> 	a_{1,1}b_{1,1} + a_{1,2}b_{2,1} & a_{1,1}b_{1,2} + a_{2,2}b_{2,2} & a_{1,1}b_{1,3} + a_{1,2}b_{2,3} \\
> 	a_{2,1}b_{1,1} + a_{2,2}b_{2,1} & a_{2,1}b_{1,2} + a_{2,2}b_{2,2} & a_{2,1}b_{1,3} + a_{2,2}b_{2,3} \\
> 	a_{3,1}b_{1,1} + a_{3,2}b_{2,1} & a_{3,1}b_{1,2} + a_{3,2}b_{2,2} & a_{3,1}b_{1,3} + a_{3,2}b_{2,3} \\
> \end{bmatrix} $$

# Determinan Matriks

Determinan matriks persegi $\b M$ ditulis sebagai $\det \b M$ atau $|\b M|$.

Untuk matriks $2 \times 2$, misalkan matriks $\b M$ adalah

$$ \b M = \begin{bmatrix}
	a & b \\
	c & d
\end{bmatrix}, $$

maka determinan matriks $\b M$ adalah

$$ |\b M| = ad - bc. $$

Misalkan $\b N$ adalah matriks $3 \times 3$,

$$ \b N = \begin{bmatrix}
	a & b & c \\
	d & e & f \\
	g & h & i
\end{bmatrix}. $$

Tambah 2 kolom bantu di paling kanan, yaitu kolom 1 dan kolom 2,

$$ \b N' = \begin{bmatrix} \begin{array}{ccc|cc}
	a & b & c & a & b \\
	d & e & f & d & e \\
	g & h & i & g & h
\end{array} \end{bmatrix} $$

Determinannya adalah jumlah diagonal-diagonal utama dikurang jumlah diagonal-diagonal sekundernya[^diagonal-sekunder],

[^diagonal-sekunder]: Diagonal dari kanan bawah ke kiri atas.

$$ |\b N| = (aei + bfg + cdh) - (gec + hfa + idb). $$

> [!info] Sifat
> - $|\b A \b B| = |\b A| \cdot |\b B|$

# Invers Matriks

Misalkan matriks persegi $\b M$ dan inversnya $\b M^{-1}$ sehingga

$$ \b M^{-1}\b M = \b M \b M^{-1} = \b I $$

di mana $\b I$ adalah matriks identitas.

> [!info] Sifat
> - $(\b A \b B)^{-1} = \b B^{-1} \b A^{-1}$

## Invers Matriks 2×2

Misalkan matriks $\b A$ adalah

$$ \b A = \begin{bmatrix}
	a & b \\
	c & d
\end{bmatrix}, $$

maka invers matriks $\b A$ adalah

$$ \b A^{-1} = \frac{1}{|\b A|} \begin{bmatrix}
	d & -b \\
	-c & a
\end{bmatrix}. $$

## Invers Matriks 3×3

Misalkan matriks $\b M$ berukuran $3 \times 3$. Pertama-tama, kita cari minor dari matriks $\b M$, misalkan $\operatorname{minor}(\b M)$.

Minor dari suatu matriks adalah matriks berisi determinan-determinan dengan kolom dan baris yang hilang.

Misalkan $\operatorname{minor}(\b M)$,

$$ \operatorname{minor}(\b M) = \begin{bmatrix}
	x_{1,1} & x_{1,2} & x_{1,3} \\
	x_{2,1} & x_{2,2} & x_{2,3} \\
	x_{3,1} & x_{3,2} & x_{3,3}
\end{bmatrix}. $$

Maka (sebagai contoh),

$$ x_{1,1} = \begin{vmatrix}
	\b M_{2,2} & \b M_{2,3} \\
	\b M_{3,2} & \b M_{3,3}
\end{vmatrix} $$

di mana baris 1 dan kolom 1 hilang ($\b M_{1,\square}$ dan $\b M_{\square,1}$).

Maka

$$ x_{1,3} = \begin{vmatrix}
	\b M_{2,1} & \b M_{2,2} \\
	\b M_{3,1} & \b M_{3,2}
\end{vmatrix}. $$

Setelah mencari $\operatorname{minor}(\b M)$, kita cari kofaktor dari matriks $\b M$, $\operatorname{cof}(\b M)$.

$$ \operatorname{cof}(\b M)_{i,j} = (-1)^{i+j} \times x_{i,j}. $$

Atau pada matriks $3 \times 3$,

$$ \operatorname{cof}(\b M) = \begin{bmatrix}
	x_{1,1} & -x_{1,2} & x_{1,3} \\
	-x_{2,1} & x_{2,2} & -x_{2,3} \\
	x_{3,1} & -x_{3,2} & x_{3,3}.
\end{bmatrix} $$

Lalu, carilah adjugat[^adjugat] (atau adjoint) matriks $\b M$, $\operatorname{adj}(\b M)$.

[^adjugat]:Adjugat dari suatu matriks $\b M$ adalah transpos dari kofaktor matriks $\b M$. Atau dapat dibilang

	$$ \operatorname{adj}(\b M) = \operatorname{cof}(\b M)^\top $$

Maka invers matriks $\b M$ adalah

$$ \b M^{-1} = \frac{1}{|\b M|} \operatorname{adj}(\b M). $$

# Sistem Persamaan Linear

Misalkan matriks $\b K$, vektor $\b x$, dan vektor $\b h$ sehingga

$$ \b K \b x = \b h, $$

maka

$$ \b x = \b K^{-1} \b h, $$

di mana

- matriks $\b K$ adalah matriks koefisien dari variabel-variabel;
- vektor $\b x$ adalah vektor variabel-variabel; dan
- vektor $\b h$ adalah hasil dari persamaan-persamaan,

di mana

- $\b K \in \mathbb{R}^{n \times n}$; dan
- $\b x , \b h \in \mathbb{R}^n$,

di mana $n$ adalah banyak variabel.

Misalkan persamaan

- $2x + 3y = 11$; dan
- $3x - 2y = 10$.

Ubah ke bentuk matriks,

$$ \begin{bmatrix}
	2 & 3 \\
	3 & -2
\end{bmatrix}
\begin{bmatrix}
	x \\
	y
\end{bmatrix} =
\begin{bmatrix}
	11 \\
	10
\end{bmatrix}. $$

Maka carilah invers dari matriks koefisien, sehingga

$$ \begin{align*}
	\begin{bmatrix}
		x \\
		y
	\end{bmatrix} &=
	\begin{bmatrix}
		2 & 3 \\
		3 & -2
	\end{bmatrix}^{-1}
	\begin{bmatrix}
		11 \\
		10
	\end{bmatrix} \\
	&= \frac{1}{-13} \begin{bmatrix}
		-2 & -3 \\
		-3 & 2
	\end{bmatrix} \begin{bmatrix}
		11 \\
		10
	\end{bmatrix} \\
	\begin{bmatrix}
		x \\
		y
	\end{bmatrix} &= \begin{bmatrix}
		4 \\
		1
	\end{bmatrix}
\end{align*} $$

Maka didapat hasilnya $x = 4$, dan $y = 1$.

---

# Sifat-Sifat Operasi Matriks

Diketahui matriks $\b A, \b B, \b C$, dan bilangan $k, \ell \in \mathbb{R}$:

- $\b A + \b B = \b B + \b A$
- $(\b A + \b B) + \b C = \b A + (\b B + \b C)$
- $k(\b A + \b B) = k \b A + k \b B$
- $(k + \ell) \b A = k \b A + \ell \b A$
- $\b A(\b B + \b C) = \b A \b B + \b A \b C$
- $(\b A \b B) \b C = \b A (\b B \b C)$
- $k(\b A \b B) = \b A (k \b B)$

Misalkan matriks

$$ \b 0 = \begin{bmatrix}
	0 & 0 & \cdots & 0 \\
	0 & 0 & \cdots & 0 \\
	\vdots & \vdots & \ddots & \vdots \\
	0 & 0 & \cdots & 0
\end{bmatrix}. $$

- $\b 0 + \b M = \b M + \b 0$
- $\b 0 \b M = \b M \b 0 = \b 0$

Untuk $n, m \in \mathbb{N}$:

- $(A^\top)^\top = A$
- $(\b A + \b B)^\top = \b A^\top + \b B^\top$
- $(k \b A)^\top = k \b A^\top$
- $(\b A \b B)^\top = \b B^\top \b A^\top$
- $\b A^n \b A^m = \b A^{n + m}$

Untuk matriks $\b M, \b N$ yang memiliki invers:

- $(\b M^{-1})^{-1} = \b M$
- $(\b M^n)^{-1} = (\b M^{-1})^n$
- $(k \b M)^{-1} = \frac{1}{k} \b M^{-1}$
- $(\b M^\top)^{-1} = (\b M^{-1})^\top$
- $(\b M \b N)^{-1} = \b N^{-1} \b M^{-1}$