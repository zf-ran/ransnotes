# Kombinatorika dan Peluang

Selengkapnya di [[Kombinatorika]].

## Permutasi

$$ \newcommand{\P}{\mathrm{P}} \P_r^n = \frac{n!}{(n-r)!}. $$

## Kombinasi

$$ \newcommand{\C}{\mathrm{C}} \C_r^n = \frac{n!}{(n-r)!\;r!} = \frac{\P_r^n}{r!}. $$

## Peluang Bersyarat

Peluang kejadian $A$ jika diketahui $B$ terjadi.

$$ P(A \mathbin| B) = \frac{P(A \cap B)}{P(B)}. $$

### Teorema Bayes

$$ P(A \mathbin| B) = \frac{P(B \mathbin| A) \; P(A)}{P(B)}. $$

# Statistika

Misalkan data

$$ \mathbf x = [x_1, x_2, x_3, \dots, x_n]. $$

- Rerata (mean)
	$$ \bar x = \frac{1}{n} \sum_{i=1}^n x_i. $$
- Varians
	$$ s^2 = \frac{1}{n} \sum_{i=1}^n (x_i - \bar x)^2. $$
- Standar deviasi
	$$ s = \sqrt{s^2} = \sqrt{\frac{1}{n} \sum_{i=1}^n (x - \bar x)^2}. $$
## Normalisasi Data

### Min–Max

$$ x'_i = \frac{x_i - \min (x)}{\max(x) - \min(x)}, $$

sehingga data akan berada pada rentang $[0, 1]$, di mana nilai maksimal akan menjadi 1, dan minimum akan menjadi 0.

### Z-Score

$$ x'_i = \frac{x_i - \bar x}{s}, $$

di mana $\bar x$ adalah mean, dan $s$ adalah standar deviasi.

Pada *z-score normalization*, mean akan menjadi 0, dan standar deviasi akan menjadi 1.

# Aljabar Linear

Selengkapnya di [[Matriks]].

# Kalkulus dan Optimasi

## Turunan Fungsi

Berikut aturan-aturan turunan.$\newcommand{\d}[1]{\frac{\mathrm d}{\mathrm d #1}}\newcommand{\dd}[2]{\frac{\mathrm d #1}{\mathrm d #2}}$

**Aturan dasar:**

- Turunan konstanta 
	$$ \d{x} k = 0, \qquad (k \in \mathbb{R}) $$
- Turunan linear
	$$ \d{x} x = 1 $$
- Perpangkatan
	$$ \d{x} x^n = nx^{n-1} $$
- Eksponen natural
	$$ \d{x} e^x = e^x $$
- Logaritma natural
	$$ \d{x} \ln(x) = \frac 1 x, \qquad (x > 0) $$

**Untuk $y$ sebagai fungsi $x$, dan $k \in \mathbb{R}$:**

- Perkalian dengan konstanta
	$$ \d{x} ky = k \d{x} y $$

**Untuk $u, v$ sebagai fungsi $x$:**

- Penjumlahan dua fungsi
	$$ \d{x} u + v = \d{x} u + \d{x} v $$
- Perkalian dua fungsi
	$$ \d{x} uv = u'v + uv' $$
- Pembagian dua fungsi
	$$ \d{x} \frac u v = \frac{u'v - uv'}{v^2} $$

**Untuk $y, u$ fungsi $x$ dan $y$ fungsi $u$:**

- Aturan rantai
	$$ \dd{y}{x} = \dd{y}{u} \dd{u}{x} $$
	atau, misalkan $f, g$ adalah fungsi:
	$$ \d{x} f(g(x)) = f'(g(x)) \cdot g'(x) $$