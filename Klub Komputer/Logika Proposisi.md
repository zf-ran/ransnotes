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

### Proposisi Universal

- Kata kunci: *Semua, seluruh, tidak ada, setiap.*

Proposisi yang melibatkan seluruh anggotanya, seperti

> Semua pensil Asep 2B.

Semua pensil Asep harus 2B. Jika ada **satu** saja yang bukan 2B, maka proposisi tersebut bernilai salah.

Negasi dari proposisi universal adalah proposisi partikular.

> [!EXAMPLE] Contoh
> $p$ = semua kucing Budi berwarna putih.
> 
> $\neg p$ = beberapa kucing Budi tidak berwarna putih.

### Proposisi Partikular

- Kata Kunci: *Ada, sebagian, beberapa, tidak semua.*

Proposisi yang melibatkan setidaknya **satu** anggotanya, seperti

> Pena Asep ada yang berwarna biru.

Setidaknya harus ada **satu** pena Asep yang berwarna biru untuk proposisi di atas bernilai benar. Untuk proposisi di atas bernilai salah, **semua** pena Asep harus tidak berwarna biru.

> [!EXAMPLE] Contoh
> $q$ = sebagian kelinci Budi berwarna hitam.
> 
> $\neg q$ = semua kelinci Budi tidak berwarna hitam.

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

## Biimplikasi

Dilambangkan dengan $\iff$.

Biimplikasi memiliki sifat komutatif

$$ a \iff b \equiv b \iff a, $$

tidak seperti implikasi.

Proposisi

$$ a \iff b $$

bermakna *$a$ jika dan hanya jika $b$*.

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

## Kontraposisi

$$ (p \implies q) \implies (\neg q \implies \neg p) $$

Misalkan:
- $p$ adalah “saya sakit”, dan
- $q$ adalah “saya tidak sekolah”.

Diketahui $p \implies q$:

> Jika saya sakit, maka saya tidak sekolah.

maka $\neg q \implies \neg p$:

> Jika saya sekolah, maka saya tidak sakit.

---

$$ \newcommand{\true}{\mathrm{T}} \newcommand{\false}{\mathrm{F}} $$

# Contoh Soal

> **(OSK 2022)** Pak Dengklek menemukan sebuah kotak mainan di dalam gudang rumahnya. Ternyata, kotak tersebut milik lima bebek Pak Dengklek: Kwak, Kwik, Kwuk, Kwek, dan Kwok. Terdapat lima buah bebek karet berwarna merah, biru, hijau, kuning, dan ungu. Diketahui bahwa setiap bebek karet dimiliki oleh tepat satu bebek. Diketahui juga bahwa setiap bebek pasti memiliki bebek karet dengan warna yang sesuai dengan salah satu warna kesukaannya. Jika diberikan informasi sebagai berikut:
> - Kwok hanya menyukai warna oranye, hijau dan kuning.
> - Kwuk menyukai semua warna selain oranye, ungu, kuning, dan biru.
> - Kwak hanya menyukai warna hijau, oranye, dan biru.
> - Kwek hanya menyukai warna merah dan ungu.
> - Kwik menyukai semua warna selain biru, ungu, hijau, dan merah.
> 
> Siapa pemilik bebek karet berwarna hijau?

| Kw_k | Merah | Biru  | Hijau | Kuning | Ungu  |
| ---- | ----- | ----- | ----- | ------ | ----- |
| A    |       | ==T== | ~~T~~ |        |       |
| I    |       |       |       | ==T==  |       |
| U    | ==T== |       | ~~T~~ |        |       |
| E    | ~~T~~ |       |       |        | ==T== |
| O    |       |       | ==T== | ~~T~~  |       |

**Kwok.**


**(OSK 2022)** Perhatikan operasi logika berikut!

$$ \begin{align*}
	P &= ((\neg A) \wedge B) \vee (((\neg C) \vee D) \wedge E) \\
	Q &= ((\neg A) \vee B) \wedge (((\neg C) \wedge (\neg D)) \vee (\neg E)) \\
	R &= P \wedge Q.
\end{align*} $$

Jika nilai

$$ \begin{align*}
	A = \true \\
	B = \true \\
	C = \true \\
	D = \true \\
	E = \false,
\end{align*} $$

tentukan nilai $P$, $Q$, dan $R$ berturut-turut.

$$ \begin{align*}
	P &= ((\neg A) \wedge B) \vee (((\neg C) \vee D) \wedge E) \\
	&= ((\neg \true) \wedge \true) \vee (((\neg \true) \vee \true) \wedge \false) \\
	&= (\false \wedge \true) \vee \false \\
	&= \false \wedge \false \\
	\Aboxed{P &= \false}
\end{align*} $$