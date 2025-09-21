$\newcommand{\tp}{\mathrm{T}}$
Matriks adalah susunan bilangan (entri) dalam kolom dan baris, variabel matriks ditulis dengan huruf kapital. Matriks dapat ditulis dengan $[\dots]$ atau $(\dots)$. Misalnya matriks $A$,

$$ A = \begin{bmatrix} a & b & c \\ x & y & z \end{bmatrix}. $$

Matriks $A$ memiliki 2 baris dan 3 kolom, maka matriks $A$ **berukuran** (berordo) $2 \times 3$, atau dapat ditulis $A_{2\times3}$. Ukuran matriks $M$ ditulis sebagai $M_{\text{baris}\times\text{kolom}}$.

# Matriks Persegi

Sebuah matriks disebut sebagai **matriks persegi** jika banyak baris dan banyak kolomnya sama, contohnya matriks $M$,

$$ M_{3\times3} = \begin{bmatrix} a & b & c \\ d & e & f \\ g & h & i \end{bmatrix}. $$

# Matriks Identitas

Untuk matriks persegi $A$, ada sebuah **matriks identitas** $I$ yang di mana

$$ IA = A. $$

Notasi $IA$ melambangkan perkalian matriks $I$ dan matriks $A$, [[#Perkalian Matriks dengan Matriks]].

Matriks identitas tersebut adalah matriks yang entri pada diagonal utama (dari kiri atas ke kanan bawah) bernilai $1$, dan selainnya $0$.

Didapat identitas matriks $2\times2$ adalah

$$ I_{2\times2} = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}. $$

Dan untuk identitas matriks $3\times3$ adalah

$$ I_{3\times3} = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}. $$

# Operasi Matriks

Notasi entri matriks $A$ pada baris $i$ dan kolom $j$ akan ditulis sebagai $A_{i,j}$, atau dapat dijabarkan sebagai berikut.

$$ A_{n \times m} =
\begin{bmatrix}
	A_{1,1} & A_{1,2} & A_{1,3} & \cdots & A_{1,m} \\
	A_{2,1} & A_{2,2} & A_{2,3} & \cdots & A_{2,m} \\
	A_{3,1} & A_{3,2} & A_{3,3} & \cdots & A_{3,m} \\
	\vdots & \vdots & \vdots & \ddots & \vdots \\
	A_{n,1} & A_{n,2} & A_{n,3} & \cdots & A_{n,m}
\end{bmatrix}. $$

## Transpos Matriks

Transpos matriks adalah sebuah operator yang mengubah setiap baris menjadi kolom, dan setiap kolom menjadi baris. Transpos matriks $M$ adalah $M^\tp$.

Misalkan matriks $M$ adalah

$$ M = \begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix}, $$

maka transpos matriks $M$ adalah

$$ M^\tp = \begin{bmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{bmatrix}. $$

> [!info] Sifat
> - $(AB)^\tp = B^\tp A^\tp$

## Penjumlahan Matriks

Syarat untuk menjumlahkan dua matriks adalah kedua matriks tersebut berukuran sama. Misalkan matriks $A_{n \times n}$, matriks $B_{n \times n}$, dan matriks $C = A + B$, maka

$$ C_{i,j} = A_{i,j} + B_{i,j}. $$

Sifat ini juga berlaku untuk pengurangan.

> [!summary] Penjumlahan Dua Matriks
> Misal matriks $A_{n \times m}$ dan matriks $B_{n \times m}$, maka $A + B$ adalah
> 
> $$ \begin{bmatrix}
> 	A_{1,1} & A_{1,2} & \cdots \\
> 	A_{2,1} & A_{2,2} & \cdots \\
> 	\vdots  & \vdots  & \ddots
> \end{bmatrix} + \begin{bmatrix}
> 	B_{1,1} & B_{1,2} & \cdots \\
> 	B_{2,1} & B_{2,2} & \cdots \\
> 	\vdots  & \vdots  & \ddots
> \end{bmatrix} = \begin{bmatrix}
> 	A_{1,1} + B_{1,1} & A_{1,2} + B_{1,2} & \cdots \\
> 	A_{2,1} + B_{2,1} & A_{2,2} + B_{2,2} & \cdots \\
> 	\vdots  & \vdots  & \ddots
> \end{bmatrix}. $$

## Perkalian Matriks

### Perkalian Matriks dengan Bilangan

Misalkan matriks $M$, bilangan $k$, dan matriks $N$ sehingga $N = kM$, maka

$$ N_{i,j} = kM_{i,j}. $$

> [!summary] Perkalian Matriks dengan Bilangan
> Untuk matriks $M$ dan bilangan $k$, maka $kM$ adalah
> 
> $$ k \begin{bmatrix}
> 	M_{1,1} & M_{1,2} & \cdots \\
> 	M_{2,1} & M_{2,2} & \cdots \\
> 	\vdots  & \vdots  & \ddots
> \end{bmatrix} = \begin{bmatrix}
> 	kM_{1,1} & kM_{1,2} & \cdots \\
> 	kM_{2,1} & kM_{2,2} & \cdots \\
> 	\vdots  & \vdots  & \ddots
> \end{bmatrix}. $$

### Perkalian Matriks dengan Matriks

Syarat untuk mengalikan dua matriks $A$ dan $B$ adalah banyak ***kolom*** matriks $A$ **harus sama** dengan banyak ***baris*** matriks $B$,

- $A_{p \times q}$
- $B_{q \times r}$.

Misalkan hasil perkalian matriks $A$ dan $B$ adalah matriks $C$, maka $C$ berukuran $p \times r$.

$$ C_{i,j} = A_{i,1}B_{1,j} + A_{i,2}B_{2,j} + \cdots + A_{i,n}B_{n,j}. $$

Pada baris $i$ kolom $j$ matriks $C$, fokuslah pada baris $i$ pada matriks $A$ dan kolom $j$ pada matriks $B$.

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

Determinan matriks persegi $M$ ditulis sebagai $\det M$ atau $|M|$.

Untuk matriks $2 \times 2$, misalkan matriks $M$ adalah

$$ M_{2\times2} = \begin{bmatrix}
	a & b \\
	c & d
\end{bmatrix}, $$

maka determinan matriks $M$ adalah

$$ |M| = ad - bc. $$

Misalkan $N$ adalah matriks $3 \times 3$,

$$ N_{3\times3} = \begin{bmatrix}
	a & b & c \\
	d & e & f \\
	g & h & i
\end{bmatrix}. $$

Tambah 2 kolom bantu di paling kanan, yaitu kolom 1 dan kolom 2,

$$ N' = \begin{bmatrix} \begin{array}{ccc|cc}
	a & b & c & a & b \\
	d & e & f & d & e \\
	g & h & i & g & h
\end{array} \end{bmatrix} $$

Determinannya adalah jumlah diagonal-diagonal utama dikurang jumlah diagonal-diagonal sekundernya[^diagonal-sekunder],

[^diagonal-sekunder]: Diagonal dari kanan bawah ke kiri atas.

$$ |N| = (aei + bfg + cdh) - (gec + hfa + idb). $$

> [!info] Sifat
> - $|AB| = |A| \cdot |B|$

# Invers Matriks

Misalkan matriks persegi $M$ dan inversnya $M^{-1}$ sehingga

$$ M^{-1}M = M M^{-1} = I $$

di mana $I$ adalah matriks identitas.

> [!info] Sifat
> - $(AB)^{-1} = B^{-1} A^{-1}$

## Invers Matriks 2×2

Misalkan matriks $A$ adalah

$$ A = \begin{bmatrix}
	a & b \\
	c & d
\end{bmatrix}, $$

maka invers matriks $A$ adalah

$$ A^{-1} = \frac{1}{|A|} \begin{bmatrix}
	d & -b \\
	-c & a
\end{bmatrix}. $$

## Invers Matriks 3×3

Misalkan matriks $M$ berukuran $3 \times 3$. Pertama-tama, kita cari minor dari matriks $M$, anggap $M_\text{min}$.

Minor dari suatu matriks adalah matriks berisi determinan-determinan dengan kolom dan baris yang hilang.

Misalkan $M_\text{min}$,

$$ M_\text{min} = \begin{bmatrix}
	x_{1,1} & x_{1,2} & x_{1,3} \\
	x_{2,1} & x_{2,2} & x_{2,3} \\
	x_{3,1} & x_{3,2} & x_{3,3}
\end{bmatrix}. $$

Maka (sebagai contoh),

$$ x_{1,1} = \begin{vmatrix}
	M_{2,2} & M_{2,3} \\
	M_{3,2} & M_{3,3}
\end{vmatrix} $$

di mana baris 1 dan kolom 1 hilang ($M_{1,\square}$ dan $M_{\square,1}$).

Maka

$$ x_{1,3} = \begin{vmatrix}
	M_{2,1} & M_{2,2} \\
	M_{3,1} & M_{3,2}
\end{vmatrix}. $$

Setelah mencari $M_\text{min}$, kita cari kofaktor dari matriks $M$, $M_\text{cof}$.

$$ M_{\text{cof}(i, j)} = (-1)^{i+j} \times x_{i,j}. $$

Atau pada matriks $3 \times 3$,

$$ M_\text{cof} = \begin{bmatrix}
	x_{1,1} & -x_{1,2} & x_{1,3} \\
	-x_{2,1} & x_{2,2} & -x_{2,3} \\
	x_{3,1} & -x_{3,2} & x_{3,3}.
\end{bmatrix} $$

Lalu, carilah adjugat[^adjugat] matriks $M$, $\operatorname{adj}(M)$.

[^adjugat]:Adjugat dari suatu matriks $M$ adalah transpos dari kofaktor matriks $M$. Atau dapat dibilang

	$$ \operatorname{adj}(M) = (M_\text{cof})^\mathrm{T} $$

Maka invers matriks $M$ adalah

$$ M^{-1} = \frac{1}{|M|} \operatorname{adj}(M). $$

# Sistem Persamaan Linear

Misalkan matriks-matriks $A$, $B$, dan $X$ sehingga

$$ AX = B, $$

maka

$$ X = A^{-1}B. $$

Misalkan persamaan

- $2x + 3y = 11$
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

$$ \begin{bmatrix}
	x \\
	y
\end{bmatrix} =
\begin{bmatrix}
	2 & 3 \\
	3 & -2
\end{bmatrix}^{-1}
\begin{bmatrix}
	11 \\
	10
\end{bmatrix}. $$