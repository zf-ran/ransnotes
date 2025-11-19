# A. Bilangan Prima

Bilangan prima adalah suatu bilangan bulat positif yang memiliki tepat 4 faktor (2 faktor positif, dan 2 faktor negatif). Yakni bilangan tersebut, $1$, $-1$, dan negatif bilangan tersebut.

## A.1. Sifat-Sifat

Untuk bilangan prima $p$:

- Jika $p \mid ab$ maka $p \mid a$ **atau** $p \mid b$; untuk $a, b \in \mathbb Z$
	1. Contohnya, $3 \mid 54$. 
		- $54 = 6 \times 9$.
		- $3 \mid 6$ dan juga $3 \mid 9$.
	2. Contohnya, $5 \mid 20$.
		- $20 = 5 \times 4$.
		- $5 \mid 5$, tapi $5 \nmid 4$.
- Jika $p \mid a^n$ maka $p \mid a$, dan juga $p^n \mid a^n$; untuk $a \in \mathbb Z$ dan $n \in \mathbb R$.
- Untuk setiap $n > 1$, terdapat **minimal** satu bilangan prima $p$ sedemikian sehingga $n < p < 2n$.
- Misalkan $p_n$ adalah bilangan prima ke-$n$, maka $p_{n + 1} < 2p_n$. Atau dengan kata lain, suatu bilangan prima lebih kecil dari dua kali prima sebelumnya.

## A.2. Pengecekan Bilangan Prima

Misalkan ada suatu bilangan $n$, dan kita perlu mengecek apakah bilangan tersebut prima atau tidak.

### A.2.1. *Brute-force*

Cara yang naif, yaitu mengecek seluruh bilangan dari $2$ sampai $n - 1$.

- Jika ada suatu bilangan $i$ yang habis membagi $n$ $(2 \leq i < n)$, maka $n$ **bukan** prima.
- Jika tidak, maka $n$ prima.

Kompleksitasnya $O(n)$.

### A.2.2. Cek Hingga $\sqrt n$

Kenapa cukup hingga $\sqrt n$? Karena jika ada suatu pasang $a, b$ sehingga $a \times b = n$, maka salah satu dari $a$ atau $b$ lebih kecil atau sama dengan $\sqrt n$.

Jika tidak ada pembagi di bawah $\sqrt n$, maka juga tak ada pembagi di atasnya.

Caranya sama dengan *brute-force*, tapi batasannya adalah $\sqrt n$.

- Jika ada suatu bilangan $i$ yang habis membagi $n$ $(2 \leq i \leq \sqrt n)$, maka $n$ **bukan** prima.
- Jika tidak, maka $n$ prima.

Kompleksitasnya $O(\sqrt n)$.

```cpp title:"Algoritma mengecek bilangan prima"
bool is_prime(int n) {
	if (n <= 1)
		return false;
		
	int root = sqrt(n);
		
	for (int i = 2; i <= root; i++)
		if (n % i == 0)
			return false;
			
	return true;
}
```
## A.3. Mencari Bilangan Prima: *Sieve of Eratosthenes*

Jika ingin mencari prima ke-$n$, atau semua prima dari $1$ sampai $n$, gunakan *sieve of Eratosthenes*.

Berikut algoritmanya untuk mencari semua bilangan prima dari $1$ sampai $n$.

1. Buat sebuah *list* angka bulat dari $2$ sampai $n$.
2. Awalnya, misalkan $p := 2$.
3. Coret semua kelipatan $p$ pada *list* tersebut, **kecuali** $p$ itu sendiri.
	- Coret $2p, 3p, 4p, ...$ sampai $n$.
4. Cari bilangan terkecil yang lebih besar dari $p$ yang **tidak** dicoret:
	- Jika tidak ada, berhenti.
	- Jika ada, maka misalkan $p :=$ bilangan baru ini (yakni bilangan prima selanjutnya). Lanjutkan langkah ke-3.
5. Maka semua bilangan yang tidak dicoret pada *list* tersebut adalah bilangan prima.

Kompleksitasnya $O(n \log (\log n))$.

> [!quote] Practice Problems
> Terdapat seorang penyihir yang dapat mengubah bilangan menjadi bilangan lain, dengan cara mengalikan bilangan awal dengan suatu bilangan. Misalnya, ia dapat mengubah $7$ menjadi $28$, dengan mengalikannya dengan $4$.
> 
> **Soal 1.** Jika di lemari penyihir terdapat bilangan prima $[2, 3, 5, 7, 11, 13, \dots]$, ada berapa bilangan yang dapat diubah menjadi $3660$?
> 
> - [ ] 1
> - [ ] 2
> - [ ] 3
> - [ ] 4
> - [ ] 5
> 
> **Soal 2.** Jika di lemari penyihir terdapat bilangan kuadrat $[1, 4, 9, 16, \dots]$, ada berapa bilangan yang dapat diubah menjadi $3200$?
> 
> - [ ] 2
> - [ ] 4
> - [ ] 6
> - [ ] 8
> - [ ] 10
> 
> **Soal 3.** \_\_\_, diubah menjadi $2025^5$?