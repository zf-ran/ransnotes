> [!question] Soal
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

---

> [!question] Soal
> #logika
> **(OSK 2022)** Perhatikan operasi logika berikut!
> 
> $$ \begin{align*}
> 	P &= ((\neg A) \wedge B) \vee (((\neg C) \vee D) \wedge E) \\
> 	Q &= ((\neg A) \vee B) \wedge (((\neg C) \wedge (\neg D)) \vee (\neg E)) \\
> 	R &= P \wedge Q.
> \end{align*} $$
> 
> Diketahui nilai
> 
> - $A = 1$,
> - $B = 1$,
> - $C = 1$,
> - $D = 1$, dan
> - $E = 0$.
> 
> Tentukan nilai $P$, $Q$, dan $R$ berturut-turut!

$$ \begin{align*}
	P &= ((\neg A) \wedge B) \vee (((\neg C) \vee D) \wedge E) \\
	&= ((\neg 1) \wedge 1) \vee (((\neg 1) \vee 1) \wedge 0) \\
	&= (0 \wedge 1) \vee 0 \\
	&= 0 \wedge 0 \\
	\Aboxed{P &= 0}
\end{align*} $$