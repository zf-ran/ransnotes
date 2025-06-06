Memiliki bentuk dasar

$$ a \bmod b = c $$

- dengan $a$ adalah yang dibagi,
- $b$ adalah pembagi, dan
- $c$ adalah sisa dari pembagian $a$ dengan $b$.

Ada juga bentuk ekuivalensi,

$$ a \equiv c \pmod b. $$
# Sifat-Sifat

- $(a + b) \bmod n = ((a \bmod n) + (b \bmod n)) \bmod n$.
- $(ab) \bmod n = ((a \bmod n)(b \bmod n)) \bmod n$.
- $a^b \bmod n = (a \bmod n)^b \bmod n$.

## Wilson’s Theorem

> $$ (p - 1)! \bmod p = p-1 $$
> 
> dengan $p$ adalah bilangan prima.

Dari teorema di atas dapat diturunkan,

$$ (p-2)! \bmod p = 1, $$

dan

$$ (p-1)! \equiv -1 \pmod p $$

## Fermat’s Little Theorem

> $$ a^p \equiv a \pmod p $$
> 
> dengan $a$ dan $p$ relatif prima dan $p$ adalah bilangan prima.

Dapat ditulis juga seperti

$$ a^{p-1} \equiv 1 \pmod p $$

> [!info]- Pembuktian
> Misalkan bilangan $a$ dan $p$ relatif prima, dan $p$ adalah bilangan prima.
> 
> Misalkan himpunan
> $$ S = \{a, 2a, 3a, \ldots, (p-2)a, (p-1)a, pa\}. $$
> 
> Karena semua anggota himpunan $S$ saling inkongruen (mod $p$), maka hasil bagi semua anggota $S$ dengan $p$ menghasilkan angka-angka yang berbeda, yaitu $0$ sampai $p-1$. Misalkan himpunan $S'$ adalah sisa bagi dari semua anggota $S$ dibagi $p$,
> $$ S' = \{0, 1, 2, 3, \ldots, p-2, p-1\} $$
> 
> Dapat disimpulkan $S \equiv S' \pmod p$.
> 
> Misalkan himpunan
> $$ S_1' = S' \setminus \{0\}. $$
> 
> Karena $0 \equiv pa \pmod p$, maka himpunan $S_1$ yang kongruen dengan $S_1'$ (mod $p$) adalah
> $$ S_1 = S \setminus \{pa\} $$
> 
> Himpunan $S_1$ kongruen dengan himpunan $S_1'$ (mod $p$). Maka hasil kali semua anggota $S_1$ dan hasil kali semua anggota $S_1'$ kongruen (mod $p$).
> $$ \begin{align*}
> 	a\cdot(2a)\cdot(3a)\ldots(p-2)a\cdot(p-1)a &\equiv 1\cdot2\cdot3\cdots(p-2)\cdot(p-1) \pmod p \\
> 	a^{p-1} \cdot (p-1)! &\equiv (p-1)! \pmod p \\
> 	a^{p-1}(p-1)! - (p-1)! &\equiv 0 \pmod p \\
> 	(p-1)!(a^{p-1} - 1) &\equiv 0 \pmod p
> \end{align*} $$
> 
> Maka antara $p \mid (p-1)!$ atau $p \mid a^{p-1} - 1$. Karena $p$ adalah prima dan tidak memiliki faktor persekutuan dengan $(p-1)!$ kecuali $1$, tentu saja tidak dapat membagi $(p-1)!$. Maka didapatlah
> $$ p \mid a^{p-1} - 1, $$
> 
> atau dapat ditulis seperti
> $$ \begin{align*}
> 	a^{p-1} - 1 &\equiv 0 \pmod p \\
> 	\Aboxed{a^{p-1} &\equiv 1 \pmod p}.
> \end{align*} $$

## Euler’s Totient Theorem

> $$ a^{\varphi(n)} \equiv 1 \pmod n $$
> di mana $a$ dan $n$ relatif prima, dan $\varphi(n)$ sama dengan banyak bilangan bulat positif yang relatif prima dengan $n$ dan yang lebih kecil dari $n$.

Bisa dirumuskan

$$ \varphi(n) = A^{a-1}(A-1) \times B^{b-1}(B-1) \times \cdots \times Z^{z-1}(Z-1) $$

dengan $A^a B^b \cdots Z^z$ adalah faktorisasi prima dari $n$.