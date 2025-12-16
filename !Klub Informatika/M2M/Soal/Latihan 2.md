---
date: 2025-11-18
---

# Soal 1–3. Mbah Dukun Penyantet Angka

Ada mbah dukun yang saat ini memiliki sebuah barisan angka yang terletak pada brankas rahasia $A$. Ada $N$ buah bilangan dengan indeks terurut mulai dari $i = 1$ hingga $i = N$ pada brankas tersebut, atau

$$ A = [A_1, A_2, \dots, A_N]. $$

Mbah dukun ini berbeda dari biasanya, bukannya menyantet orang, malahan ia menyantet suatu angka tertentu menjadi penjumlahan angka tersebut dengan 2025, atau dengan kata lain mbah dukun tersebut dapat memilih satu index $i$​ dan mengubah nilainya menjadi $A_i + 2025$, atau secara formal ubah $A_i := A_i + 2025$.

Mbah dukun ingin memaksimalkan banyaknya *subarray*[^subarray] yang mengandung **setidaknya satu** bilangan genap. Untuk memaksimalkan banyak *subarray* tersebut, Mbah dukun dapat menyantet **paling banyak** satu angka di brankas $A$. Bantulah mbah dukun untuk mencari banyaknya *subarray* maksimal!

[^subarray]: *subarray* adalah bagian bersebelahan/berturutan dari sebuah *array*. Misalkan *array* $M = [1, 2, 3, 4, 5]$. Maka $[1, 2]$, $[2, 3, 4]$, $[2, 3, 4, 5]$ adalah *subarray* dari $M$. Sedangkan $[1, 3, 5]$, $[2, 5]$ **bukanlah** *subarray* dari $M$.

**Soal 1.** Jika dalam brankas rahasia mbah dukun berisi sebanyak 6 buah bilangan yang semuanya genap, tentukan banyaknya *subarray* yang mengandung setidaknya satu bilangan genap.

**Soal 2.** Jika dalam brankas rahasia mbah dukun berisi sebanyak 6 buah bilangan terurut sebagai berikut $A = [4, 3, 6, 1, 5, 10]$, tentukan banyaknya sub array yang mengandung setidaknya satu bilangan genap.

**Soal 3.** Jika dalam brankas rahasia mbah dukun berisi sebanyak 20 buah bilangan terurut sebagai berikut $A = [2, 1, 6, 1, 3, 1000, 3, 5, 7, 9, 13, 21, 1, 8, 6, 5, 3, 4, 2, 1]$, tentukan banyaknya *subarray* yang mengandung setidaknya satu bilangan genap.

---

# Soal 4–6. Sihir Penghalang **Seorang** **Mbah Dukun** Jahat

Di sebuah dunia magis, terdapat $N$ gua misterius yang diberi nomor dari $1$ hingga $N$. Awalnya, setiap pasang gua terhubung dengan **jalur sihir**, sehingga ada total $\frac{N(N-1)}{2}$ jalur sihir yang tersedia.

Namun, **mbah dukun jahat** datang dan menggunakan sihir penghalangnya! Ia dapat **menghancurkan** beberapa jalur sihir sehingga perjalanan antar gua menjadi semakin sulit.

Setiap gua ke-$i$ memiliki **tingkat energi mistis** yang dinyatakan dengan bilangan $G_i$. Jika mbah dukun memutus jalur sihir antara gua $i$ dan gua $j$, maka energi sihir yang diperlukan adalah $G_i + G_j$. Namun, mbah dukun hanya bisa menghancurkan jalur sihir dengan total energi maksimal tertentu.

Untungnya, **petualang sakti** tinggal diantara gua tersebut dan ingin tetap bisa menjelajahi sebanyak mungkin gua yang tersisa serta mbah dukun **tidak mengetahui** dimana posisi petualang sakti. Jika kamu petualangan sakti tersebut jawablah pertanyaan berikut dengan benar.

**Soal 4.** Jika hanya terdapat 3 buah goa dengan energi mistis $G = [200, 400, 500]$. Tentukan total energi mistis minimal yang harus dipunyai oleh seorang mbah dukun jahat agar petualang sakti tidak dapat berpindah dari goanya.

**Soal 5.** Jika terdapat 10 goa mistis dengan semua energi mistisnya sebesar 1. Tentukan **jumlah minimum gua yang masih bisa dijangkau** termasuk guamu saat ini setelah mbah dukun menghancurkan jalur sihir yang ada jika mbah dukun jahat tersebut memiliki sebanyak 50 buah energi mistis. Tentunya Mbah dukun adalah orang yang juga pintar.

**Soal 6.** Ternyata suatu hari ada seorang pahlawan super, agar mbah dukun jahat tersebut tidak terlalu banyak merusah energi sihir dengan kekuatan supernya ia jalur sihir yang semula mbah dukun bisa memutus dengan energi sihir $G_i + G_j$ diubah menjadi $G_i \times G_j$. Jika pada saat ini hanya tersisa 6 buah goa dengan masing-masing energinya $G = [35, 15, 10, 25, 10, 5]$, serta energi mistis yang dimiliki oleh mbah dukun jahat tersebut sudah sebesar $1300$ maka tentukanlah minimum gua yang masih bisa dijangkau termasuk goa saat ini jika petualang sakti saat ini berada di goa pertama.

---

# Soal 7–9. Wow

Perhatikan kode berikut.

```
int Wow(int n) {
    int res = 1;
    for (int i = 2; i * i <= n; i++) {
        if (n % i == 0) {
            int cnt = 0;
            while (n % i == 0) {
                n /= i;
                cnt++;
            }
            res *= (cnt + 1);
        }
    }
    if (n > 1) res *= 2;
    return res;
}
```

**Soal 7.** Tentukan nilai dari `Wow(31)`.

**Soal 8.** Tentukan nilai dari `Wow(1000)`

**Soal 9.** Jika nilai dari `Wow(n)` adalah 12, tentukan nilai dari $n$ terkecil.

---

# Soal 10–11. Bunga

Perhatikan kode berikut.

```
int Bunga(int x) {
    if (x == 0) {
        return 1;
    } else {
        int Bungai = 0;
        for (int i = 0; i < x; i++) {
            Bungai += Bunga(i);
        }
        return Bungai;
    }
}
```

**Soal 10.** Tentukan nilai dari `bunga(4)`.

**Soal 11.** Tentukan nilai dari `bunga(22)`.