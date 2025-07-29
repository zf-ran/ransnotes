Modulo adalah sisa bagi.

> [!quote] Notasi
> $a \bmod m = b$
> 
> atau
> 
> $a \equiv b \pmod m$

Diketahui

$$ a = b \bmod m, $$

maka

$$ a = km + b $$

di mana $k \in \mathbb{Z}$

# Sifat-Sifat

# Fermat's Little Theorem

Bila ada bilangan prima $p$ dan bilangan bulat $a$, maka

$$ a^p \equiv a \pmod p $$

atau dapat diturunkan

$$ a^{p-1} \equiv 1 \pmod p $$

# Wilson's Theorem

# Euler's Theorem

Diberikan bilangan $a$ dan $m$ yang saling prima[^coprime] dan $\varphi$ adalah *Euler's totient function*, maka

$$ a^{\varphi(m)} \equiv 1 \pmod m, $$

atau dapat diturunkan menjadi

$$ a^n \equiv a^{n \bmod \varphi(m)} \pmod m $$

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