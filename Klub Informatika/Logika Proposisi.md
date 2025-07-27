---
sources:
  - https://drive.google.com/file/d/1SLmRtdwNGGCXW9sZ640S-81JS4zB2TPv/view
  - https://drive.google.com/file/d/12vxPyFD_UeGhsIZMvkPVZpD4IQFIF9yd/view
---

# Aturan Proposisi

Proposisi ...

- adalah pernyataan, bisa bernilai benar atau salah.
	+ **Benar** dapat dinyatakan dengan `true`, `1`, $\top$.
	+ **Salah** dapat dinyatakan dengan `false`, `0`, $\bot$.
- tidak menimbulkan perdebatan.
- bukan kalimat tanya.
- bukan kalimat perintah.
- bukan kalimat terbuka.
	+ Kalimat yang memiliki variabel, dan kebenaran kalimat bergantung pada variabel tersebut.
	+ Persamaan $x + 5 = 7$ bukanlah proposisi.

# Operator Logika

*(Logical operators)*

Tabel kebenaran operator-operator logika dapat dilihat di [[Logika Matematika]].

## Negasi (NOT)

Dilambangkan dengan $\neg$, `!`, $\sim$.

Negasi adalah operator uner (*unary*) hanya memerlukan satu operand (input), seperti $\neg p$. Tidak seperti konjungsi operasi yang lain, seperti $q \vee r$.

## Konjungsi (AND)

Dilambangkan dengan $\wedge$, `&&`.

## Disjungsi (OR)

Dilambangkan dengan $\vee$, `||`.

### Disjungsi Eksklusif (XOR)

Dilambangkan dengan $\oplus$, `^`.

## Implikasi

Dilambangkan dengan $\implies$.

Implikasi tidak memiliki sifat komutatif, $a \implies b$ tidak sama dengan $b \implies a$

Proposisi

$$ a \implies b $$

bermakna *jika $a$ maka $b$*.

### Konvers, Invers, dan Kontraposisi

$$ p \implies q $$

- Konvers: $q \implies p$.
- Invers: $\neg p \implies \neg q$.
- Kontraposisi: $\neg q \implies \neg p$.

## Biimplikasi

Dilambangkan dengan $\iff$.

Biimplikasi memiliki sifat komutatif

$$ a \iff b \equiv b \iff a, $$

tidak seperti implikasi.

Proposisi

$$ a \iff b $$

bermakna *$a$ jika dan hanya jika $b$*.

# Kalimat Berkuantor

## Kuantifikasi Semesta

Atau *universal quantifier*. Dilambangkan dengan $\forall$.

> [!quote] Notasi
> Kalimat yang mengandung kuantifikasi semesta disebut sebagai kalimat universal.
>
> $$ \forall x ~P(x) $$
>
> *Untuk setiap $x$, pernyataan $P(x)$ bernilai benar.*

> [!info] Kata Kunci 
> - Semua.
> - Setiap.
> - Tidak ada.

Proposisi universal adalah proposisi yang melibatkan seluruh anggotanya, seperti

> *Semua* pensil Asep adalah pensil 2B.

Semua pensil Asep harus 2B. Jika ada ***satu*** saja yang bukan 2B, maka proposisi tersebut bernilai salah.

Negasi dari kuantifikasi semesta adalah kuantifikasi eksistensial.

$$ \neg \forall x ~P(x) \equiv \exists x ~\neg P(x) $$

> [!EXAMPLE] Contoh
> - $p$ = semua kucing Budi berwarna putih.
> - $\neg p$ = beberapa kucing Budi tidak berwarna putih.

## Kuantifikasi Eksistensial

Atau *existential quantification*. Dilambangkan dengan $\exists$.

> [!quote] Notasi
> Kalimat yang mengandung kuantifikasi eksistensial disebut sebagai kalimat partikular.
>
> $$ \exists x ~P(x) $$
>
> Ada $x$, sehingga $P(x)$ bernilai benar.

> [!info] Kata Kunci 
> - Ada.
> - Sebagian.
> - Beberapa.

Proposisi yang melibatkan setidaknya **satu** anggotanya, seperti

> Pena Asep ada yang berwarna biru.

Setidaknya harus ada **satu** pena Asep yang berwarna biru untuk proposisi di atas bernilai benar. Untuk proposisi di atas bernilai salah, **semua** pena Asep harus tidak berwarna biru.

Negasi dari kuantifikasi eksistensial adalah kuantifikasi semesta.

$$ \neg \exists x ~P(x) \equiv \forall x ~\neg P(x) $$

> [!EXAMPLE] Contoh
> - $q$ = sebagian kelinci Budi berwarna hitam.
> - $\neg q$ = semua kelinci Budi tidak berwarna hitam.

# Sifat-Sifat Operator Logika

## Komutatif

$$ p \vee q \equiv q \vee p $$

- Konjungsi.
- Disjungsi.
- Biimplikasi.

## Asosiatif

$$ (p \vee q) \vee r \equiv p \vee (q \vee r) $$

- Konjungsi.
- Disjungsi.
- Biimplikasi.

## Distributif

$$ p \wedge (q \vee r) \equiv (p \wedge q) \vee (p \wedge r) $$

$$ p \vee (q \wedge r) \equiv (p \vee q) \wedge (p \vee r) $$

## De Morgan

$$ \neg(p \wedge q) = \neg p \vee \neg q $$

$$ \neg(p \vee q) = \neg p \wedge \neg q $$

# Penarikan Kesimpulan

## Modus Ponens

$$ 
	(
		(p \implies q) 
		\wedge 
		{\color{magenta} p}
	)
	\implies
	{\color{magenta} q}
$$

Diketahui pernyataan-pernyataan berikut benar.

- $p \implies q$.
- $q$.

Maka didapat kesimpulan $q$.

## Modus Tollens

$$ 
	(
		(p \implies q) 
		\wedge 
		{\color{magenta} \neg q}
	)
	\implies
	{\color{magenta} \neg p}
$$
Diketahui pernyataan-pernyataan berikut benar.

- $p \implies q$.
- $\neg q$.

Maka didapat kesimpulan $\neg p$.

> [!example]- Contoh
> Misalkan:
> - $p$ adalah “saya sakit”, dan
> - $q$ adalah “saya tidak sekolah”.
> 
> Diketahui $p \implies q$:
> 
> > Jika saya sakit, maka saya tidak sekolah.
> 
> Diketahui $\neg q$:
> 
> > Saya sekolah.
> 
> Maka dapat ditarik kesimpulan $\neg p$:
> 
> > Saya tidak sakit.

## Silogisme

$$ 
(
	({\color{magenta} p \implies q})
	\wedge
	({\color{magenta} q \implies r})
)
\implies
({\color{magenta} p \implies r})
$$

Diketahui pernyataan-pernyataan berikut benar.

- $p \implies q$.
- $q \implies r$.

Maka didapat kesimpulan $p \implies r$.

Silogisme bisa dirantai.

- $p \implies q$.
- $q \implies r$.
- $r \implies s$.
- $s \implies t$.

Maka $p \implies t$.