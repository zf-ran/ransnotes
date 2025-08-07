---
sources:
  - https://docs.google.com/presentation/d/1kfwCfHw6bgogBirN1XXKfPlK4BxWhapQ/edit
---

# Kaidah Berhitung

## Kaidah Penjumlahan

Digunakan untuk menghitung banyak kemungkinan dari kejadian-kejadian yang saling lepas, yaitu kejadian-kejadian yang tidak bisa terjadi bersamaan.

## Kaidah Perkalian

Digunakan untuk menghitung banyak kemungkinan dari kejadian-kejadian yang terjadi bersamaan.

# Faktorial

Banyak cara menyusun $n$ objek adalah $n!$, di mana

%% `\P` and `\C` definition. %%
$$
	a! = a \times (a-1) \times (a-2) \times \cdots \times 2 \times 1.
	\newcommand{\P}{\mathrm{P}}
	\newcommand{\C}{\mathrm{C}}
$$

# Permutasi

Permutasi digunakan untuk menghitung banyak cara *menyusun* objek. Karena menghitung susunan objek, maka urutan diperhatikan.

Misalkan $\P_r^n$ adalah banyak cara menyusun $r$ dari $n$ objek, maka

$$ \P_r^n = \frac{n!}{(n-r)!} $$

di mana $0 \leq r \leq n$.

## Permutasi Siklis

Permutasi siklis digunakan untuk menghitung banyak cara *menyusun* objek secara siklis (melingkar; berulang).

Banyak cara menyusun $n$ objek secara siklis dapat dihitung dengan rumus

$$ (n-1)!. $$

Sedangkan banyak cara menyusun $r$ dari $n$ objek secara siklis dapat dihitung dengan cara

$$ (n-1)! \times \C_r^n. $$

## Permutasi Unsur Sama

Misal ada $n$ objek dengan beberapa unsur yang identik, maka banyak cara menyusun mereka adalah

$$ \frac{n!}{r_1! \; r_2! \; r_3! \cdots r_k!} $$

di mana $r_1$, $r_2$, ..., $r_k$ adalah banyak setiap unsur yang identik.

# Kombinasi

Kombinasi digunakan untuk menghitung banyak cara *memilih* objek (tanpa memperhatikan urutan).

Misalkan $\C_r^n$ adalah banyak cara memilih $r$ dari $n$ objek, maka

$$ \C_r^n = \binom{n}{r} = \frac{n!}{r!(n-r)!}. $$

di mana $0 \leq r \leq n$.

# *Derangement*

*Derangement* digunakan untuk menghitung banyak cara menyusun objek-objek tetapi objek-objeknya tidak boleh di tempat asalnya.

> [!quote] Notation
> *Derangement* $n$ objek biasanya ditulis dengan $!n$, $D_n$, $n¡$.

Rumus rekursifnya adalah

$$ D_n = (n-1) (D_{n-1} + D_{n-2}) $$

di mana $D_0 = 1$ dan $D_1 = 0$.

# *Pigeonhole Principle*

(Prinsip rumah burung) menyatakan bahwa jika $n$ objek diletakkan ke $m$ tempat, dan $n > m$, maka setidaknya ada satu tempat yang memiliki objek lebih dari satu.

# Stars and Bars

*Stars and bars* (bintang dan pembatas) adalah metode untuk menghitung banyak cara mengelompokkan beberapa objek identik ke tempat-tempat berbeda.

Banyak cara mengelokpokkan $n$ objek ke $k$ tempat dapat dihitung dengan cara

$$ \frac{(n + k-1)!}{n! ~ (k-1)!} $$

atau

$$ \frac{(n + p)!}{n! ~ p!} $$

di mana $p$ adalah banyak pembatas ($p = k-1$).

> [!question]- Berapa banyak kombinasi angka $a$, $b$, dan $c$ bilangan bulat nonnegatif sehingga jumlah mereka lebih kecil dari atau sama dengan 10?
> 
> Tambah satu angka lagi yang melengkapi jumlahnya menjadi 10.
> 
> $$ \begin{align*}
> 	a + b + c &\leq 10 \\
> 	a + b + c + t &= 10
> \end{align*} $$
>
> Kita punya 10 *objek* dan 4 *tempat*.
>
> $$ \begin{align*}
> 	\frac{(n + k-1)!}{n!(k-1)!}
> 	&= \frac{(10 + 4-1)!}{10! ~ (4-1)!} \\
> 	&= \frac{13!}{10! ~ 3!} \\
> 	&= \boxed{286}
> \end{align*} $$