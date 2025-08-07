# Keterbagian

Berikut ciri-ciri angka yang habis membagi $n$.

1. $n = 2$
	+ Bilangan genap.
2. $n = 3$  
	+ Jumlah digit-digitnya habis dibagi tiga.
3. $n = 4$
	+ Dua digit terakhirnya habis dibagi empat.
4. $n = 5$
	+ Satuannya 0 atau 5.
5. $n = 7$
	+ **Pisahkan** digit satuannya, lalu kalikan **dua**.
	+ **Kurangkan** dengan sisa digitnya.
	+ Jika hasil tersebut habis dibagi tujuh, maka bilangan tersebut habis dibagi tujuh.
	+ *Contoh:* $343$.
		+ Pisahkan digit satuannya.
			$$ 34 \quad 3 $$
		+ Lalu kalikan digit satuannya dengan dua.
			$$ 3 \times 2 = 6 $$
		+ Kurangkan dengan sisa digitnya.
			$$ 34 - 6 = 28 $$
		+ 28 habis dibagi 7, maka 343 juga habis dibagi tujuh.
6. $n = 9$
	+ Jumlah digit-digitnya habis dibagi sembilan.
7. $n = 11$
	+ Selisih jumlah digit pada urutan ganjil dan jumlah digit pada urutan genap habis dibagi 11.
	+ *Contoh:* $25806$
		+ Pisahkan digit pada urutan ganjil dan genap.
			$$ 286 \quad 50 $$
		+ Jumlahkan digit-digit pada masing-masing kelompok.
			$$ 16 \quad 5 $$
		+ Cari selisih mereka.
			$$ 16 - 5 = 11 $$
		+ 11 habis dibagi 11, maka 25806 juga habis dibagi 11.
8. $n = 13$
	+ **Pisahkan** digit satuannya, lalu **kalikan 4**.
	+ **Tambah** dengan sisa digitnya.
	+ Jika hasil tersebut habis dibagi 13, maka bilangan sebelumnya habis dibagi 13.

## Pangkat Umum

1. $n = 2^k$
	+ Jika $k$ digit terakhirnya habis dibagi $n$, maka bilangan sebelumnya juga habis dibagi $n$.

# Legendre's Formula

Metode untuk mencari eksponen tertinggi dari basis yang prima dari $n!$. 

Misalkan $\nu_p(n)$ adalah eksponen terbesar $p$ yang habis membagi $n$. Formalnya $p^{\nu_p(n)} \mid n$. Maka 

$$ \nu_p(n!) = \sum_{i=1}^\infty \left\lfloor \frac{n}{p^i} \right\rfloor. $$

# Shoelace Theorem

Digunakan untuk menghitung luas dari poligon sederhana[^simple-polygon].

[^simple-polygon]: Poligon yang tidak berpotongan dan tidak berlubang.

Diberikan poligon sisi $N$ sederhana dengan titik-titik $P_i$ yang diurutkan secara berlawanan arah jarum jam, dengan $P_i = (x_i, y_i)$ dan $1 \leq i \leq N$. Maka luas poligon tersebut dapat dihitung dengan cara

$$ \frac{\left( x_1y_2 + x_2y_3 + \cdots + x_ny_1 \right) - \left( y_1x_2 + y_2x_3 + \cdots + y_nx_1 \right)}{2}, $$

yang dapat diilustrasikan sebagai berikut.

![[Shoelace Theorem Illustration.png]]