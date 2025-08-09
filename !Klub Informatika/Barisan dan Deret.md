---
sources:
  - https://drive.google.com/file/d/11EBIUuFiJaOPQCKTuno7GJu-QkOib6iI/view
---


**Barisan** adalah kumpulan bilangan berurut dengan aturan-aturan tertentu.

Sedangkan **deret** adalah jumlah dari anggota-anggota sebuah barisan.

# Aritmetika

## Barisan

Barisan aritmetika adalah barisan bilangan di mana selisih dua suku berturutan[^berturutan] sama.

[^berturutan]: Berturut-turut, misalnya $U_3$ dengan $U_4$.

Misalkan $U_n$ adalah suku ke-$n$ dari suatu barisan aritmetika, maka

$$ U_n = U_1 + (n-1)b $$

dengan $b$ adalah selisih dari anggota yang berdekatan.

Nilai $b$ dapat dicari dengan $U_n - U_{n-1}$.

Barisan bilangan

$$ 3, 7, 11, 15, 19, \dots $$

merupakan barisan aritmetika, karena selisih dua suku berturutan sama

$$ 7 - 3 = 11 - 7 = 15 -11 = \dots = 4. $$

Bentuk umum dari barisan aritmetika dapat dinyatakan seperti

$$ U_1, U_1 + b, U_1 + 2b, U_1 + 3b, \dots. $$

## Deret

Misalkan $S_n$ adalah jumlah $n$ suku pertama dari suatu barisan aritmetika, maka

$$ S_n = \frac{n}{2} (U_1 + U_n), $$

atau bisa dijabarkan menggunakan rumus $U_n$ seperti

$$ S_n = \frac{n}{2} (2U_1 + (n-1)b). $$

# Geometri

## Barisan

Barisan geometri adalah barisan bilangan di mana rasio (perbandingan) dua suku berturutan[^berturutan] sama.

Misalkan $U_n$ adalah suku ke-$n$ dari suatu barisan geometri, maka

$$ U_n = ar^{n-1} $$

di mana $r$ adalah rasio dua suku berturutan.

Nilai $r$ dapat dicari dengan rumus

$$ r = \frac{U_n}{U_{n-1}}. $$

Bentuk umum barisan geometri dapat dinyatakan dengan

$$ a, a r, a r^2, a r^3, \dots $$

di mana $a$ adalah suku pertama.

## Deret

Misalkan $S_n$ adalah jumlah $n$ suku pertama dari barisan geometri, maka

$$ S_n = \frac{a (r^n - 1)}{r - 1}. $$

Untuk deret tak hingga,

$$ S_\infty = \frac{a}{1 - r} $$

di mana $-1 < r < 1$.

> [!summary]- Asal-usul
> $$ \begin{align*}
> 	S_n &= \frac{a(r^n - 1)}{r - 1} \\
> 	\lim_{n \rightarrow \infty} S_n &= \lim_{n \rightarrow \infty} \frac{a (r^n - 1)}{r - 1} \\
> 	S_\infty &= \lim_{n \rightarrow \infty} \frac{a (r^n - 1)}{r - 1}
> \end{align*} $$
> 
> Untuk $-1 < r < 1$, dapat dilihat $r^n$ semakin mendekat ke 0 saat $n$ menuju tak hingga.
>
> $$ \begin{align*}
> 	S_\infty &= \frac{a (0 - 1)}{r - 1} \\
> 	&= \frac{-a}{r-1} \\
> 	&= -\frac{a}{r-1} \\
> 	&= \frac{a}{-(r-1)} \\
> 	&= \frac{a}{-r + 1} \\
> 	\Aboxed{S_\infty &= \frac{a}{1 - r}}
> \end{align*} $$

# Deret Spesial

- **Deret bilangan asli**
	$$ \boxed{\sum_{i=1}^n i = \frac{n(n+1)}{2}.} $$
- **Deret bilangan ganjil**
	$$ \sum (2n - 1) = 1 + 3 + \cdots + (2n - 1) = n^2. $$

- **Deret bilangan kuadrat**
	$$ \sum i^2 = \frac{n(n+1)(2n+1)}{6}. $$
- **Deret bilangan genap kuadrat:** $2^2 + 4^2 + \cdots + (2n)^2$.
	$$ \sum (2i)^2 = 4\left[\sum i^2 \right] = \frac{2n(n+1)(2n+1)}{3}. $$
- **Deret bilangan ganjil kuadrat:** $1^2 + 3^2 + \cdots + (2n-1)^2$.
	$$ \sum (2i - 1)^2 = \frac{n(2n - 1)(2n + 1)}{3}. $$

- **Deret bilangan kubik**
	$$ \sum i^3 = \left[\sum i\right]^2 = \left[\frac{n(n+1)}{2}\right]^2 $$
- **Deret bilangan pangkat empat**
	$$ \sum i^4 = \frac{1}{30} n(n+1)(2n+1)(3n^2 + 3n - 1) $$