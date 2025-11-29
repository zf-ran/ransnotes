Pada permainan ini, terdapat dua pemain, misalkan Asep dan Budi. Setiap pemain memiliki sebuah larik dengan panjang $2$. Pada awal permainan, Asep dan Budi diberi larik $[1, 1]$.

Misalkan $A$ adalah larik Asep, dan $B$ adalah larik Budi.

Untuk larik $M$, misalkan $M_L$ adalah elemen pertama larik $M$; dan $M_R$ adalah elemen kedua larik $M$. Atau dapat ditulis $M = [M_L, M_R]$.

Permaian ini bergilir, dan anggap saja Asep mulai duluan.

Pada setiap giliran, misalkan $S$ adalah larik pemain yang dalam giliran, dan $E$ adalah larik lawan. Pemain dapat melakukan **salah satu** operasi berikut.

- **Langkah defensif**: pilih sebuah bilangan buat $r$ $(r \neq 0)$ dan misalkan $S' = [S_L + r, S_R - r]$ sehingga $S'$ **bukan** permutasi[^1] dari $S$ dan $0 \leq S'_L, S'_R < K$. Setelah itu, ubah $S := S'$.
- **Langkah ofensif**: pilih sebuah elemen dari $S$ yang tidak nol, misalkan $p$. Lalu tambahkan $p$ kepada salah satu elemen $E$ yang tidak nol. Setelah itu, ubah $E_L := E_L \bmod K$ dan $E_R := E_R \bmod K$.

[^1]: Sebuah larik $M'$ disebut sebagai permutasi dari $M$ jika semua elemen $M'$ dapat disusun ulang menjadi $M$. Sebagai contoh, $[4, 2]$ merupakan permutasi $[2, 4]$. Namun $[2, 2]$ bukan permutasi dari $[2, 4]$.

Jika pada suatu saat sebuah elemen mencapai $0$, maka elemen itu dibilang “mati”. Sebagai contoh, misalkan $A = [0, 3]$, maka $A_L$ mati.

Elemen yang mati dapat dihidupkan kembali menggunakan langkah defensif. Sebagai contoh, misalkan $A = [3, 0]$ dan $r = -2$, maka $A' = [1, 2]$, di mana $A_R$ hidup kembali.

Pemain pertama kali yang memiliki $[0, 0]$ akan kalah.

Pada umumnya, permainan ini menggunakan $K = 5$.

> [!example] Berikut contoh permainan dengan $K = 5$.
> 
> Misalkan $A = [2, 4]$, $B = [3, 1]$, dan sekarang giliran Asep. Asep dapat melakukan langkah defensif dengan $r = 1$ sehingga $A := [3, 3]$.
> 
> Lalu giliran Budi, ia memilih untuk melangkah ofensif. Budi memiliki $B_L$ dan menambahkannya ke $A_R$. Sehingga $A := [3, 6]$. Lalu modulokan semua bilangan $A$ sehingga $A := [3, 1]$.
> 
> Pada giliran Asep, ia memilih untuk langkah defensif lagi dengan $r = 1$ sehingga $A := [4, 0]$.
> 
> Lalu pada giliran Budi, ia memiliki langkah ofensif. Budi memilih $B_R$. Budi **tidak** dapat menambahkan $B_R$ ke $A_R$, karena $A_R$ sedang mati. Maka Budi menambahkannya ke $A_L$, mengubah $A := [5, 0]$. Setelah memodulokan larik $A$, Asep sekarang memiliki $[0, 0]$.