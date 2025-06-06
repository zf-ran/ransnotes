$\newcommand{\true}{\mathrm{T}} \newcommand{\false}{\mathrm{F}}$
# Pernyataan

Sebagai contoh,

$$ p = \text{botol itu merah}. $$

# Ingkaran atua Negasi (Not)

Dilambangkan dengan $\sim$ atau $\neg$ . Seperti $\neg p$: “tidak $p$”.

Sebagai contoh,

$$ p = \text{hari ini hujan} $$

maka negasi $p$ adalah

$$ \neg p = \text{hari ini tidak hujan}. $$

## *Truth Table* Negasi

| $p$ | $\neg p$ |
| --- | --------- |
| T   | F         |
| F   | T         |

# Pernyataan Majemuk

Gabungan dari dua pernyataan atau lebih, dan dihubungkan dengan kata hubung.

Jenis-jenis kata hubung sebagai berikut.

## Konjungsi (dan) ($\wedge$)

| $p$ | $q$ | $p \wedge q$ |
| --- | --- | ------------ |
| F   | F   | F            |
| F   | T   | F            |
| T   | F   | F            |
| T   | T   | T            |

## Disjungsi (atau) ($\vee$)

| $p$ | $q$ | $p \vee q$ |
| --- | --- | ------------ |
| F   | F   | F            |
| F   | T   | T            |
| T   | F   | T            |
| T   | T   | T            |

## Implikasi (jika …, maka …) ($\implies$)

| $p$ | $q$ | $p \implies q$ |
| --- | --- | -------------- |
| F   | F   | T              |
| F   | T   | T              |
| T   | F   | F              |
| T   | T   | T              |

## Biimplikasi (jika dan hanya jika …, maka …) ($\iff$)

| $p$ | $q$ | $p \iff q$ |
| --- | --- | ---------- |
| F   | F   | T          |
| F   | T   | F          |
| T   | F   | F          |
| T   | T   | T          |

# Sifat-Sifat

## Konjungsi dan Disjungsi

- $p \wedge q \equiv q \wedge p$.
- $(p \wedge q) \wedge r \equiv p \wedge (q \wedge r)$.

Berlaku untuk disjungsi juga.
### Hukum De Morgan

- $\neg (p \wedge q) \equiv \neg p \vee \neg q$, dan sebaliknya.
## Implikasi

- $p \implies q \equiv \neg p \vee q$.

# Penarikan Kesimpulan

## Modus Ponens

Diketahui $p \implies q$ dan $p = \true$. Maka didapatkan $q = \true$.

> [!example] Contoh
> - Jika *sudah malam*, maka *dia tidur*
> - Hari *sudah malam*.
> 
> Didapatkan kesimpulan bahwa **dia tidur**.

> [!info]- Pembuktian
> 
> $$ \begin{align*}
> 	(p \implies q) &= \neg p \vee q \\
> 	\true &= \neg \true \vee q \\
> 	\true &= \false \vee q \\
> 	\true &= q \\
> 	\Aboxed{q &= \true}
> \end{align*} $$
> 
> Atau juga bisa melihat *truth table* dari implikasi. Saat $p \implies q$ itu benar dan diketahui $p$ itu benar, maka $q$ sudah pasti benar.

## Modus Tollens

Diketahui $p \implies q$ dan $q = \false$. Maka didapatkan $p = \false$.


> [!example] Contoh
> - Jika hari ini hari kerja, maka saya sekolah.
> - Saya tidak sekolah.
> 
> Dapat ditarik kesimpulan bahwa **hari ini *bukan* hari kerja**.


> [!info]- Pembuktian
> $$ \begin{align*}
> 	(p \implies q) &= \neg p \vee q \\
> 	\true &= \neg p \vee \false \\
> 	\true &= \neg p \vee \false \\
> 	\true &= \neg p \\
> 	\Aboxed{p &= \false}
> \end{align*} $$

## Silogisme

Diketahui $p \implies q$ dan $q \implies r$. Maka $p \implies r$.

