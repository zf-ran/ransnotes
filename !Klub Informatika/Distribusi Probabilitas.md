# Diskrit

## Binomial

Misalkan variabel acak $X$ mengikuti distribusi binomial dengan

- $n$ percobaan Bernoulli;
- $k$ kejadian sukses;
- $p$ sebagai peluang kejadian sukses; dan
- $q$ sebagai peluang kejadian gagal, atau $q = 1 - p$,

maka

$$ \operatorname{P}(X = k) = \binom{n}{k} p^k q^{n-k}. $$

Contoh,  
Berapa peluang mata dadu yang dilempar 10 kali menghasilkan tepat 6 kali bilangan kelipatan 3?

Misalkan himpunan $S$ sebagai ruang sampel mata dadu,

$$ S = \{1, 2, 3, 4, 5, 6\}. $$

Misalkan himpunan $A$ sebagai kejadian kelipatan 3,

$$ A = \{3, 6\}. $$

Maka peluang mendapat dadu kelipatan 3 adalah

$$ p = \frac{|A|}{|S|} = \frac{2}{6} = \frac{1}{3}. $$

Diketahui dari soal bahwa banyak percobaan adalah 10 dan banyak kesuksesan adalah 6,

$$ n = 10, k=6. $$

Maka peluangnya adalah

$$ \begin{align*}
	\operatorname{P}(X = k) &= \binom{10}{k} p^k (1 - p)^{n-k} \\
	\operatorname{P}(X = 6) &= \frac{10!}{6! \times 4!} \left(\frac{1}{3}\right)^6 \left(\frac{2}{3}\right)^4 \\
	&\approx 0.05690189504 \\
	&\approx 5.69\%
\end{align*} $$

# Kontinu