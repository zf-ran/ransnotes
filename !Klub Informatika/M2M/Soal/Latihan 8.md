# Soal 1–3. Wowogi dan Makan Siang Bergizi Gratis yang Rumit

Wowogi sedang mengadakan program makan siang bergizi gratis untuk anak-anak di sekolah. Ada $N$ siswa yang datang satu per satu ke kantin untuk mengambil makanan. Kita menomori siswa-siswa ini dari $1$ sampai $N$ berdasarkan urutan kedatangan mereka.

Di kantin, para siswa duduk berbaris di meja panjang tanpa ada celah kosong di antara mereka. Saat siswa ke-$i$ tiba, dia harus duduk tepat di sebelah kanan siswa bernomor $A_i$. Jika $A_i = 0$, berarti ia duduk di ujung paling kiri barisan.

Namun, ada masalah. Karena siswa harus duduk bersebelahan tanpa celah, ketika seorang siswa baru ingin duduk, harus ada tempat duduk yang dibuat. Ini bisa dilakukan dengan

- menggeser semua siswa di sebelah kiri dari posisi tersebut ke kiri sejauh satu kursi; atau
- menggeser semua siswa di sebelah kanan dari posisi tersebut ke kanan sejauh satu kursi.

Wowogi ingin tahu, berapa banyak pergeseran tempat duduk minimum yang dibutuhkan agar semua siswa bisa duduk dengan benar tanpa ada celah kosong.

Sebagai contoh jika ada 5 orang dan $A = [0, 1, 2, 1, 4]$.

- Siswa $1$, $2$, dan $3$ duduk tanpa perlu geser.
	- Barisan kursi menjadi $[\dots, 1, 2, 3, \dots]$.
- Siswa $4$ ingin duduk di sebelah kanan siswa $1$.
	- Bisa dengan menggeser siswa $1$ ke kiri atau siswa $2$ dan $3$ ke kanan.
	- Pilih opsi pertama, karena langkah paling sedikit, sehingga barisan kursi menjadi $[\dots, 1, 4, 2, 3, \dots]$.
- Siswa $5$ ingin duduk di sebelah kanan siswa keempat.
	- Harus menggeser dua siswa, baik ke kiri maupun ke kanan.
	- Barisan kursi menjadi $[\dots, 1, 4, 5, 2, 3, \dots]$.

Sehingga barisan kursi 5 orang ini diperoleh dengan 3 langkah minimum.

**Soal 1.** Jika terdapat sebanyak 5 orang dengan diberikan urutan $A = [0, 0, 0, 0, 0]$, tentukan berapa banyak pergeseran tempat duduk minimum yang dibutuhkan agar semua siswa bisa duduk.

**Soal 2.** Jika terdapat sebanyak 8 orang dengan diberikan urutan $A = [0, 1, 2, 0, 1, 2, 0, 2]$, tentukan berapa banyak pergeseran tempat duduk minimum yang dibutuhkan agar semua siswa bisa duduk.

**Soal 3.** Jika terdapat sebanyak 10 orang dengan $A_1 = 0$ dan nilai $A_i$ adalah faktor positif **terbesar** $i$ yang **bukan** $i$. Tentukan berapa banyak pergeseran tempat duduk minimum yang dibutuhkan agar semua siswa bisa duduk.

---

# Soal 4–6. Seekor Katak di Rawa

Di sebuah rawa yang luas, hiduplah seekor katak petualang bernama Takak. Takak bukanlah katak biasa, ia sangat mahir melompat dan menaklukkan berbagai rintangan di lingkungannya.

Suatu hari, Takak bertekad untuk mencapai permukaan daun tertinggi di rawa tersebut. Namun, ia tidak ingin menggunakan jalur biasa, melainkan ingin menguji kemampuannya dengan melompat langsung dari satu daun ke daun lainnya.

Takak menemukan sebuah batang terendam yang menjulang ke atas, membentuk struktur persegi panjang yang terdiri dari n tingkat horizontal. Setiap tingkat memiliki m segmen, yang beberapa di antaranya memiliki daun tempat Takak dapat mendarat. Daun-daun ini akan menjadi tempat beristirahatnya dalam perjalanan mendaki rawa.

Sebagai katak yang cerdas, Takak ingin menghitung jumlah rute yang dapat ia gunakan untuk mencapai daun tertinggi. Sebuah rute dianggap sah jika memenuhi syarat berikut.

- Lompat pertama harus dimulai dari daun di tingkat **paling bawah**. Lompat terakhir harus mendarat di daun di tingkat **paling atas**.
- Setiap lompatan hanya boleh **naik** atau tetap di ketinggian yang **sama**. Setiap tingkat harus memiliki setidaknya **satu** daun yang digunakan dalam rute tersebut.
- Tidak lebih dari dua daun boleh digunakan dalam satu tingkat. Takak dapat melompat dari satu daun ke daun lainnya jika jaraknya tidak melebihi kemampuan lompatannya, yaitu sejauh $d$.

Jarak antara dua daun bertitik $(i_1, j_1)$ dan $(i_2, j_2)$ diukur menggunakan rumus

$$ \sqrt{(i_1  - i_2 )^2  + (j_1  - j_2 )^2}. $$

Tugasmu adalah menghitung jumlah rute unik yang dapat diambil Takak untuk mencapai tujuan. Dua rute dianggap berbeda jika terdapat perbedaan dalam daftar daun yang digunakan atau urutan lompatan yang dilakukan.

**Soal 4.** Jika $\mathtt{O}$ adalah representasi daun dan $\mathtt{X}$ bukan daun, tentukan banyaknya kemungkinan jumlah daun yang mungkin dilompati Takak jika Takak memiliki kemampuan meloncat sejauh $d = 2$ dan diberikan rute daun berukuran $3 \times 4$ sebagai berikut.

$$ \begin{gather*}
	\mathtt{OXOX} \\
	\mathtt{XOXO} \\
	\mathtt {OXOX}
\end{gather*} $$

**Soal 5.** Dengan berlatih, kemampuan meloncat Takak bisa bertambah, sekarang ia memiliki kemampuan meloncat sejauh $d = 5$. Jika diberikan rute seperti soal sebelumnya, maka berapa kemungkinan rute unik yang dapat diambil Takak untuk mencapai tujuan?

**Saol 6.** Dengan bertambahnya usia kemampuan Takak yang sebelumnya bisa meloncat sejauh 5, sekarang kemampuannya menjadi hanya sebesar 2 kembali. Tentukan berapa kemungkinan rute unik yang dapat diambil Takak untuk mencapai tujuan.

---

# Soal 7–9: ZZ-ABC

```
#include <iostream>
using namespace std;

char D[] = { 'A', 'B', 'C', 'D', 'E', 'F', 'G' };
const int SIZE = 7;

void swap(int a, int b)
{
	char tmp = D[a];
	D[a] = D[b];
	D[b] = tmp;
}

void printArray()
{
	for (int i = 0; i < SIZE; i++) {
		cout << D[i];
	}
	
	cout << endl;
}

void ZZ(int m)
{
	if (m <= 0) {
		printArray();
	} else {
		ZZ(m - 1);
		
		for (int i = m - 2; i >= 0; i--) {
			swap(i, m - 1);
			ZZ(m - 1);
			swap(i, m - 1);
		}
	}
}
```

**Soal 7.** Pada pemanggilan `ZZ(3)`, berapa kali fungsi `printArray()` akan dipanggil?

**Soal 8.** Pada pemanggilan `ZZ(3)`, apakah yang akan tercetak pada baris ketiga dari pemanggilan tersebut?

**Soal 9.** Misalkan `ZZ(7)` dijalankan di suatu komputer yang sudah cukup sepuh selama 1 detik, kira-kira berapa lama `ZZ(10)` dijalankan?