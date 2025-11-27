# 1—Eksponen

Berikut sifat-sifat eksponen.

- $a^0 = 1$ untuk semua $a \neq 0$.
- $a^1 = a$.
- $a^{m+n} = a^m a^n$.
- $a^{m-n} = \dfrac{a^m}{a^n}$.
- $(a^m)^n = a^{mn}$.
- $(ab)^n = a^n b^n$.
- $a^{-n} = \dfrac{1}{a^n}$.
- $a^{m/n} = \sqrt[n]{a^m}$.
- $a^{-m/n} = \dfrac{1}{\sqrt[n]{a^m}}$.

> [!question] Practice Problems
> Coba sederhanakan bentuk berikut.
> 
> 1. $(x^8)^3$.
> 2. $(x^3 y^4 z)^2$.
> 3. $(5a^2b)^6 \times a^3b^4$.
> 4. $\left( \dfrac 2 5 ab \right)^5 \div \left( \dfrac 1 3 ab \right)^3$.

Dari sifat eksponon, dapat diturunkan sifat akar.

- $\sqrt{a}^2 = a$.
- $\sqrt{ab} = \sqrt{a}\sqrt{b}$.
- $\sqrt{\dfrac{a}{b}} = \dfrac{\sqrt a}{\sqrt a}$.

Sederhanakan bentuk berikut.

$$ 2\sqrt{175} - 5\sqrt{343} + \sqrt{63} - \sqrt{112}. $$

Caranya bisa dengan mencari faktorisasi prima bilangan-bilangan yang ada di dalam akar.

$$ 2 \sqrt{5^2 \cdot 7} - 5\sqrt{7^3} + \sqrt{3^2 \cdot 7} - \sqrt{2^4 \cdot 7}. $$

Lalu, jika pangkatnya lebih dari dua, keluarkan. Dan pangkatnya jadi 1. Dan biarkan sisanya di dalam akar.

$$ \begin{align*}
	&\rightarrow 2(5)\sqrt{7} - 5\sqrt{7^2 \cdot 7} + (3)\sqrt{7} - \sqrt{(2^2)^2 \cdot 7} \\
	&= 10\sqrt7 - 5(7)\sqrt7 + 3\sqrt7 - (2^2)\sqrt7 \\
	&= 10\sqrt7 - 35\sqrt7 + 3\sqrt7 - 4\sqrt7 \\
	&= (10 -35 + 3 - 4)\sqrt7 \\
	&= -26\sqrt7.
\end{align*} $$

# 2—Barisan dan Deret

## 2.1—Aritmetika

**Soal 1/67.** Suku ke-15 dari barisan aritmetika 70, 61, 52, … adalah ….

Diketahui

- $a = 70$;
- $b = 61 - 70 = -9$; dan
- $n = 15$.

$$ \begin{align*}
	U_n &= a + (n - 1)b \\
	U_{15} &= 70 + (14)(-9) \\
	U_{15} &= -56.
\end{align*} $$

Maka suku ke-15-nya adalah $-56$.

**Soal 3/67.** $U_5 = 4$, $U_{25} = 14$. Berapa nilai $U_{21}$?

$$ \begin{align*}
	U_5 &= a + 4b \\
	U_{25} &= a + 24b
\end{align*} $$

Maka didapat sistem persamaan linear dua variabel (SPL2V).

$$ \begin{cases}
a + 4b = 4 \\
a + 24b = 14
\end{cases} $$

Selesaikan dengan cara kalian masing-masing. Akan didapat $b = 1/2$ dan $a = 2$.

$$ \begin{align*}
	U_{21} &= a + 20b \\
	&= 2 + 20 \left(\frac 1 2\right) \\
	&= 2 + 10 \\
	&= 12.
\end{align*} $$

# 3—Trigonometri

**Soal 1/115.** Diketahui segitiga $ABC$ siku-siku di titik $A$ dengan $AB = \pu{3 cm}$ dan $BC = \pu{6 cm}$. Berapa nilai $\sin B$?

Jika bingung, gambarkanlah segitiga tersebut.

Nilai sinus adalah depan per miring. Pada konteks ini, sudutnya adalah $\angle B$, maka depannya adalah sisi $AC$.

Karena siku di $A$, maka sisi miringnya adalah $BC$.

Maka didapaat persamaan $AB^2 + AC^2 = BC^2$ menggunakan teorema Pythagoras. Didapat sisi $AC = 3\sqrt3$.

Maka

$$ \sin B = \frac{AC}{BC} = \frac{3\sqrt3}{6} = \frac 1 2 \sqrt3. $$

**Soal 4/115.** Diketahui $\tan \alpha = p$. Nilai $\sin \alpha$ dalam $p$ adalah ….

Diketahui $\tan \theta = \dfrac{\sin \theta}{\cos \theta}$. Tapi $\cos$-nya apa?

Diketahui $\sin^2 \theta + \cos^2 \theta = 1.$ Maka didapat $\cos \theta = \sqrt{1 - \sin^2 \theta}$.

Mari substitusikan.

$$ \begin{align*}
	\tan \alpha &= \frac{\sin \alpha}{\cos \alpha} \\
	p &= \frac{\sin \alpha}{\sqrt{1 - \sin^2 \alpha}} \\
	p^2 &= \frac{\sin^2 \alpha}{1 - \sin^2 \alpha} \\
	p^2 - p^2 \sin^2 \alpha &= \sin^2 \alpha \\
	p^2 &= \sin^2 \alpha + p^2 \sin^2 \alpha \\
	p^2 &= (1 + p^2) \sin^2 \alpha \\
	\frac{p^2}{1+ p^2} &= \sin^2 \alpha \\
	\Aboxed{\frac{p}{\sqrt{1 + p^2}} &= \sin \alpha}.
\end{align*} $$

Sudut elevasi adalah sudut menaik, sedangkan sudut depresi adalah sudur menurun.