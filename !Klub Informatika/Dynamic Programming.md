---
date: 2025-07-29
---

*Dynamic programming* (pemrograman dinamis) disingkat DP, adalah metode untuk menyederhanakan masalah menjadi submasalah yang lebih kecil.

Ada dua cara penyelesaian *dynamic programming*, yaitu

- *top-down* (*memoization*), dan
- *bottom-up* (*tabulation*).

Berikut beberapa bentuk *dynamic programming* yang sering muncul.

- DP ubin (*tile DP*).
- DP string.
- DP *knapsack*.
- DP koin.

Tujuan kita menggunakan *dynamic programming* adalah untuk efisiensi dan performa.

Ada beberapa hal penting pada *dynamic programming*, yaitu sebagai berikut.

- ***State***  
	adalah representasi masalah, seperti `dp[i]` atau $F_n$.
- ***Transition***  
	adalah cara untuk berpindah dari satu *state* ke *state* yang lain, atau dapat disebut sebagai rumus, seperti $F_n = F_{n-1} + F_{n-2}$.
- ***Base case***  
	adalah masalah terkecil yang dapat diselesaikan tanpa perlu menyelesaikan submasalah lain, seperti $F_0$ dan $F_1$.

# Fibonacci

Barisan bilangan

$$ 1, 1, 2, 3, 5, 8, 13, \dots $$

adalah barisan Fibonacci, yang di mana suku ke-$n$ adalah jumlah suku sebelumnya dan suku kedua sebelumnya,

$$ F_n = F_{n-1} + F_{n-2} $$

di mana $F_n$ adalah Fibonacci ke-$n$.

Bentuk ini sering muncul di soal-soal yang menggunakan *dynamic programming*.

---

# Contoh Soal

> [!question] 
> #dynamic-programming #tile-dp
> 
> Pak Dengklek memiliki ubin 1×1 dan 1×2 yang masing-masing jumlah ubin tersebut tak terbatas. Jika Pak Dengklek perlu menutupi lantai berukuran 1×10, maka berapa banyak cara untuk menyusun ubin-ubin tersebut agar menutupi lantai tanpa tumpang-tindih?

Pertama definisikan *state*-nya, misalkan $f(n)$ adalah banyak cara untuk menutupi lantai berukuran $1 \times n$. Lalu cari *transition*-nya.

Misal lantai berukuran $1 \times n$, `|...||||`, bisa kita pecah menjadi

- `|...|||` dan `|`; serta
- `|...||` dan `||`;

karena kita memiliki dua ukuran ubin, yaitu 1×1 dan 1×2. Maka jumlahkanlah cara menyusun dengan ubin 1×1 terakhir, dan 1×2 terakhir.

Maka didapat *transition*-nya

$$ f(n) = f(n-1) + f(n-2). $$

Lanjut, *base case*-nya. Untuk $f(1)$ hanya ada satu cara, yaitu menggunakan ubin 1×1. Untuk $f(2)$, ada dua cara: menggunakan 2 ubin 1×1, atau 1 ubin 1×2. 

Yang ditanya adalah lantai berukuran 1×10, maka kita perlu mencari $f(10)$.

| $n$ | $f(n)$  |
| --- | ------- |
| 1   | ***1*** |
| 2   | ***2*** |
| 3   | 3       |
| 4   | 5       |
| 5   | 8       |
| 6   | 13      |
| 7   | 21      |
| 8   | 34      |
| 9   | 55      |
| 10  | 89      |

> [!done] Answer
> Ada 89 cara untuk menutupi lantai tersebut.