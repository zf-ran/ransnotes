Modulo adalah sisa bagi.

> [!quote] Notasi Modulo
> $$ a \bmod m = b $$
> 
> bermakna sisa pembagian $a$ dengan $m$ adalah $b$.

> [!quote] Notasi Aritmatika Modular
> $$ a \equiv b \pmod m $$
> 
> bermakna $a$ dan $b$ itu kongruen pada modulo $m$, atau dapat juga ditulis dengan
> 
> $$ a \bmod m = b \bmod m. $$

# Sifat-Sifat

## Modulo

## Kekongruenan

Jika $a \equiv b \pmod m$ dan $k \in \mathbb{Z}$, maka:

- $a + k \equiv b + k \pmod m$.
- $ka \equiv kb \pmod m$.
- $ka \equiv kb \pmod {km}$.
- $a^k \equiv b^k \pmod m$.

Jika $a_1 \equiv b_1 \pmod m$ dan $a_2 \equiv b_2 \pmod m$, maka:

- $a_1 + a_2 \equiv b_1 + b_2 \pmod m$.
- $a_1 a_2 \equiv b_1 b_2 \pmod m$.

# Fermat's Little Theorem

> [!info]
> Bila ada bilangan prima $p$ dan bilangan bulat $a$, maka
> 
> $$ a^p \equiv a \pmod p $$
> 
> atau dapat diturunkan
> 
> $$ a^{p-1} \equiv 1 \pmod p $$

# Wilson's Theorem

> [!info] Teorema Wilson
> Untuk bilangan prima $p$ maka
>
> $$ (p - 1)! \equiv -1 \pmod p. $$
>
> Pernyataan di atas dapat diturunkan menjadi
> 
> $$ (p - 2)! \equiv 1 \pmod p. $$

# Euler's Theorem

> [!info] Teorema Euler
> Diberikan bilangan $a$ dan $m$ yang saling prima[^coprime] dan $\varphi$ adalah *Euler's totient function*, maka
> 
> $$ a^{\varphi(m)} \equiv 1 \pmod m, $$
> 
> atau dapat diturunkan menjadi
> 
> $$ a^n \equiv a^{n \bmod \varphi(m)} \pmod m. $$

[^coprime]: Faktor persekutuan terbesar mereka bernilai 1.

## Euler's Totient Function

(Fungsi phi Euler) $\varphi(n)$ adalah fungsi yang menghitung banyak bilangan yang saling prima dengan $n$ dari 1 sampai $n$.

- Diberikan bilangan prima $p$ dan bilangan asli $n$, maka
	$$ \varphi(p^n) = p^n - p^{n-1}. $$
- Jika $m$ dan $n$ saling prima, maka
	$$ \varphi(mn) = \varphi(m) \varphi(n). $$

Fungsi phi Euler bisa dihitung dengan memfaktorisasi prima $n$ menjadi $p_1^{e_1} p_2^{e_2} p_3^{e_3} \cdots p_i^{e_i}$.

$$ \begin{align*}
	\varphi(n) &= \varphi(p_1^{e_1} p_2^{e_2} p_3^{e_3} \cdots p_i^{e_i}) \\
	&= \varphi(p_1^{e_1}) \varphi(p_1^{e_1}) \varphi(p_2^{e_2}) \varphi(p_3^{e_3}) \cdots \varphi(p_i^{e_i}) \\
	&= (p^{e_1} - p^{e_1 - 1}) (p^{e_2} - p^{e_2 - 2}) \cdots (p^{e_i} - p^{e_i - 1})
\end{align*} $$

# Chinese Remainder Theorem