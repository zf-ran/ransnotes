# Keterbagian

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