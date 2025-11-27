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
		return false; // 0 dan 1 bukanlah prima.
		
	int root = sqrt(n);
		
	for (int i = 2; i <= root; i++)
		// Jika ada suatu bilangan yang membagi n,
		// maka bilangan n bukan prima.
		if (n % i == 0)
			return false;
	
	// Jika tiada, maka n prima.
	return true;
}
```
## A.3. Mencari Bilangan Prima: *Sieve of Eratosthenes*

Jika ingin mencari prima ke-$n$, atau semua prima dari $1$ sampai $n$, gunakan *sieve of Eratosthenes*.

Berikut algoritmanya untuk mencari semua bilangan prima dari $1$ sampai $n$.

1. Buat sebuah *list* angka bulat dari $2$ sampai $n$.
2. Awalnya, misalkan $p := 2$.
3. Coret semua kelipatan $p$ pada *list* tersebut, **kecuali** $p$ itu sendiri.
	- Coret $2p, 3p, 4p, ...$$^\dagger$ sampai $n$.
4. Cari bilangan terkecil yang lebih besar dari $p$ yang **tidak** dicoret:
	- Jika tidak ada, berhenti.
	- Jika ada, maka misalkan $p :=$ bilangan baru ini (yakni bilangan prima selanjutnya). Lanjutkan langkah ke-3.
5. Maka semua bilangan yang tidak dicoret pada *list* tersebut adalah bilangan prima.

$^\dagger$ Sebenarnya cukup mulai dari $p^2$, karena bilangan-bilangan sebelumnya **pasti** sudah tercoret. Misalkan $p = 5$, kita tidak perlu mencoret $20$ (di mana $20 < 5^2$) karena $20 = 5 \times 2^2$, sudah dicoret oleh $2$.

Kompleksitasnya $O(n \log (\log n))$.

```cpp title:"Algoritma Sieve of Eratosthenes: Mencari Bilangan Prima hingga N"
vector<int> primes_up_to(int N) {
	// Buat array untuk mengecek keprimaan suatu bilangan.
	// Di mana is_prime[p] = true jika p prima, dan sebaliknya.
	bool is_prime[N + 1];
	
	is_prime[0] = 0;
	is_prime[1] = 0;
	
	// Asumsikan semua bilangan prima.
	for (int p = 2; p <= N; p++)
		is_prime[p] = true;
	
	int root = sqrt(N);
	for (int p = 2; p <= root; p++) { // Cukup cek hingga √N.
		if (is_prime[p]) { // Jika p tidak tercoret,
			for (int i = p*p; i <= N; i += p) {
				is_prime[i] = false; // coret setiap kelipatan p.
			}
		}
	}
	
	vector<int> primes;
	
	// Ekstrak semua bilangan prima dari array.
	for (int p = 2; p <= N; p++)
		if (is_prime[p])
			primes.push_back(p);
	
	return primes;
}
```

> [!important] Soal Latihan
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

# B. Faktor Bilangan

Misalkan $a$ adalah suatu bilangan yang habis membagi $b$, maka dapat disebut: $a$ adalah faktor dari $b$.

## B.1. Faktorisasi Prima

Semua bilangan asli lebih dari satu dapat kita tulis menjadi hasil kali dari faktor prima penyusunnya.

Berikut contohnya.

- $6 = 2 \times 3$
- $84 = 2^2 \times 3 \times 7$
- $300 = 2^2 \times 3 \times 5^2$

## B.2. Banyak Faktor

Untuk mencari banyak faktor dari $N$, maka nyatakan $N$ dalam bentuk faktorisasi primanya:

$$ N = p_1^{e_1} \times p_2^{e_2} \times \cdots \times p_n^{e_n}, $$

di mana $p_i$ adalah bilangan prima, dan $e_i$ adalah bilangan bulat $(e_i \geq 0)$.

Maka banyak faktor dari $N$ adalah

$$ (e_1 + 1)(e_2 + 1) \cdots (e_n + 1) $$

atau dapat dinyatakan dalam notasi pi,

$$ \prod_{i=1}^n e_i + 1. $$

Berikut contohnya.

- Misalkan $N = 60 = 2^2 \times 3 \times 5$, maka banyak faktornya adalah $$ (2 + 1)(1 + 1)(1 + 1) = 12. $$

## B.3. Jumlah Faktor

Sama dengan mencari banyak faktor dari $N$, nyatakan $N$ dalam bentuk faktorisasi primanya. Maka jumlah faktor-faktor dari $N$ adalah

$$ (1 + p_1 + p_1^2 + \cdots + p_1^{e_1})(1 + p_2 + p_2^2 + \cdots + p_2^{e_2}) \cdots (1 + p_n + p_n^2 + \cdots + p_n^{e_n}), $$

atau dapat ditulis menjadi

$$ \prod_{i=1}^n \sum_{j=0}^{e_i} p_i^j. $$

> [!important] Soal Latihan
> **Soal 1.** Banyaknya faktor positif dari bilangan $13230$ adalah ….
> 
> - [ ] 12
> - [ ] 24
> - [ ] 36
> - [ ] 48
> - [ ] 60
> 
> **Soal 2.** Banyaknya faktor positif dari bilangan $360360$ yang merupakan kelipatan 10 adalah ….
> 
> - [ ] 12
> - [ ] 24
> - [ ] 48
> - [ ] 60
> - [ ] 72
> 
> **Soal 3.** Berapakah hasil perkalian dari semua bilangan bulat positif yang habis membagi $100$?
> 
> - [ ] $\pu{10000}$
> - [ ] $\pu{100000}$
> - [ ] $\pu{100000000}$
> - [ ] $\pu{1000000000}$
> - [ ] $\pu{10000000000}$
> 
> **Soal 4.** Jumlah faktor positif dari $360360$ adalah ….
> 
> - [ ] $\pu{1572480}$
> - [ ] $\pu{1572386}$
> - [ ] $\pu{1572384}$
> - [ ] $\pu{1572382}$
> - [ ] $\pu{1572380}$
> 
> **Soal 5.** (OSP 2018 Soal A22) Pak Dengklek menyatakan suatu bilangan disebut **bagus** apabila bilangan tersebut habis dibagi 3. Pak Dengklek menyatakan suatu bilangan disebut **cantik** apabila bilangan tersebut memiliki banyak faktornya ganjil. Jika Pak Dengklek memiliki suatu bilangan $X$, berapakah minimum nilai $N$ supaya **banyaknya** bilangan dari $1$ sampai $N$ yang bagus atau cantik **lebih besar dari atau sama dengan** $X$ jika diberikan nilai $X = 100$?