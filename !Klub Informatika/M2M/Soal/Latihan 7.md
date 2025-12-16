---
date: 2025-12-14
---

# Soal 1–3. Pak Alam dan Masalah di Asrama PKU

Pak Alam adalah kepala asrama PKU di Sekolah Sains Amatir yang memiliki asrama dengan $n$ kamar. Setiap kamar ditempati oleh tepat satu siswa. Kumpulan kamar tersebut berbentuk pohon dan saling terhubung dengan kamar lainnya yang bersebelahan secara langsung.

Malam ini, ada tiga tipe siswa di asrama, yaitu

- siswa yang ingin berpesta dan memutar musik keras (ditandai dengan $\mathtt{P}$);
- siswa yang ingin tidur dan menikmati ketenangan (ditandai dengan $\mathtt{S}$); dan
- siswa yang tidak peduli dengan suara musik (ditandai dengan $\mathtt{C}$).

Nantinya Anda akan diberikan *string* $S$ dengan $n$ karakter di mana $S_i$ melambangkan tipe siswa pada kamar ke-$i$ yang berupa karakter $\mathtt{P}$, $\mathtt{S}$, atau $\mathtt{C}$.

Awalnya, semua dinding antar kamar merupakan dinding tipis, sehingga suara musik melewati semua kamar. Jadi, jika ada siswa yang berpesta dan memutar musik, **semua** siswa di asrama bisa mendengarnya.

Namun, Pak Alam bisa memasang **dinding tebal** di antara beberapa kamar. Dinding tebal ini akan menghalangi suara musik melewati batas tersebut.

Anda akan diberikan larik $A$ dengan panjang $n - 1$ yakni $[A_2, A_3, A_4, \dots, A_n]$, di mana $A_i$ menunjukkan bahwa kamar ke-$i$ terhubung **langsung** dengan kamar $A_i$.

Sebagai contoh jika diberikan larik dengan panjang $2$: $A = [1, 1]$; artinya di sana terdapat 3 kamar dengan

- kamar ke-$2$ terhubung langsung ke kamar ke-$1$; dan
- kamar ke-$3$ terhubung langsung ke kamar ke-$1$.
- Dalam hal ini juga diketahui bahwa kamar ke-$2$ dan kamar ke-$3$ **tidak** terhubung langsung.

Pak Alam ingin memasang **jumlah minimum dinding tebal** sehingga setiap siswa yang berpesta dapat memutar musiknya **tanpa** mengganggu siswa yang ingin tidur.

**Soal 1.** Jika diberikan $n = 3$, $S = \mathtt{CSP}$, dan $A = [1, 1]$. Tentukan banyaknya sekat minimum yang diperlukan agar yang memutar musik tidak mengganggu siswa lainnya.

**Soal 2.** Jika diberikan $n = 8$, $S = \mathtt{CSPSPSPC}$, dan $A = [1, 1, 2, 2, 4, 4, 4]$. Tentukan banyaknya sekat minimum yang diperlukan agar yang memutar musik tidak mengganggu siswa lainnya.

**Soal 3.** Jika diberikan $n = 15$, $S = \mathtt{CSPSPSPCSPPPPSC}$, dan

$$ A = [1, 1, 2, 2, 4, 4, 4, 3, 3, 3, 7, 10, 7, 10]. $$

Tentukan banyaknya sekat minimum yang diperlukan agar yang memutar musik tidak mengganggu siswa lainnya.

---

# Soal 4–6. Membangun Candi

Di sebuah kerajaan kuno, para arsitek sedang membangun sebuah candi megah di atas tanah dengan luas yang tak terbatas. Mereka menggunakan cetakan batu berbentuk persegi berukuran $m \times m$ untuk menyusun struktur candi.

Awalnya, cetakan batu pertama diletakkan di sudut kiri bawah tanah pembangunan, yaitu sudut kiri bawah cetakan batu diletakkan di titik $(0, 0)$. Para arsitek telah merancang sebuah rencana pembangunan yang terdiri dari $n$ langkah. Rencana pembangunan ini akan direpresentasikan dalam sebuah larik $Q$ dengan panjang $n$.

Setiap langkah ke-$i$ dilakukan sebagai berikut.

Geser cetakan batu sejauh $x_i$ unit ke kanan dan $y_i$ unit ke atas dari titik sebelumnya. Tempelkan cetakan batu pada posisi saat ini, menambahkan bagian baru pada struktur candi.

Perlu diperhatikan bahwa semua perpindahan memiliki batasan khusus, yakni $1 \leq x_i, y_i \leq m - 1$. Hal ini agar candi tersebut dapat terhubung dengan baik.

Setelah semua langkah dilakukan, bentuk akhir dari candi yang terbentuk akan menjadi satu kesatuan yang terhubung.

Sebagai contoh jika diberikan $m = 3$, $n =4$, dan $Q = [(1, 1), (2, 2), (2, 1), (1, 2)]$, akan diperoleh struktur bangunan candi seperti gambar pada *Soal 4*.

**Soal 4.** Tentukan keliling dari kerangka candi pada gambar berikut.

![Soal 4](https://lh7-rt.googleusercontent.com/formsz/AN7BsVDT6ph0lNAnI0fWP2wouziEQhwWiLxDtDuzwQ6I2BM0SVQUfoa4S1CR-ykJmg6bSWqD1dmqVAXS2dITxatBQdfsvqEBpN2nAuDyqWG7ayYtV1SIl33a2IplTU-Mcky9EFSDgaAHvmGWWa7_y234P7Zxk3t1sbow0poPapX__Jjw8Q34f-wVBs0PlHnhSzRJ3_JiHjods8ry6UzA=w268?key=zotSQBEKEVgESRIqhHUNUA)

**Soal 5.** Diberikan $m = 10$, $n = 4$, dan $Q = [(1,1), (2,2), (3,3), (4,4)]$. Tentukan keliling dari kerangka candi yang terbentuk.

**Soal 6.** Diberikan $m = 11$, $n = 10$, dan

$$ Q = [(1, 10), (2, 9), (3, 8), (4, 7), \dots, (10, 1)]. $$

Tentukan keliling dari kerangka candi yang terbentuk.

---

# Soal 7–9. Rahasia

Perhatikan kode berikut.

```
#include <iostream>
using namespace std;

void rahasia(int angka, vector<char>& hasil)
{
	if (angka < 0) {
		hasil.push_back('P');
		rahasia(-angka, hasil);
	} else if (angka > 1) {
		rahasia(angka / 2, hasil);
		hasil.push_back((angka % 2) ? 'O' : 'R');
	} else {
		hasil.push_back('N'); // perhatikan baris ini
	}
}

void tampil(const vector<char>& hasil)
{
	for (char c : hasil) {
		cout << c;
	}
	
	cout << endl;
}

int main()
{
	int n;
	cin >> n;
	
	vector<char> hasil;
	
	rahasia(n, hasil);
	tampil(hasil);
}
```

**Soal 7.** Apa yang akan dicetak jika diberikan masukan `10`.

**Soal 8.** Jika `hasil.push_back('N');` pada baris ke-13 diubah menjadi `hasil.push_back('N' + angka);`, tentukan apa yang dicetak jika diberikan masukan `-21`.

**Soal 9.** Tentukan bilangan bulat **terkecil** yang dapat jadikan masukan agar mengeluarkan tepat 10 buah karakter yang dicetak.