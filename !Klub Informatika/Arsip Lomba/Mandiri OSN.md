---
date: 2025-12-22
---

**Soal 1.** Pak Dengklek memiliki 5 pintu kandang, yaitu $A$, $B$, $C$, $D$, dan $E$. Masing-masing pintu memiliki sensor yang mencatat $M - X$, di mana $M$ adalah banyak bebek yang masuk, dan $X$ adalah banyak bebek yang keluar. Pada awalnya, semua bebek di dalam kandang, dan pada akhirnya, semua bebek kembali ke dalam kandang. Sensor $E$ rusak. Pintu $A$ sampai $D$ memiliki data

- $A = +5$;
- $B = -3$;
- $C = +1$; dan
- $D = -6$.

Berapa angka yang seharusnya ada pada sensor $E$?

- [ ] $+4$
- [ ] $+3$
- [ ] $+2$
- [ ] $+1$
- [ ] $0$

**Soal 2.** Sebuah *string* biner$^\ast$ “$\mathtt{1100101}$” akan diproses agar menjadi palindrom$^\dagger$. Pada satu langkah, Anda dapat mengubah satu karakter yang awalnya $\mathtt{1}$ menjadi $\mathtt{0}$, atau yang awalnya $\mathtt{0}$ menjadi $\mathtt{1}$. Berapa langkah paling sedikit yang dapat Anda lakukan?

$^\ast$*string* biner adalah *string* yang hanya berisi karakter $\mathtt{0}$ atau $\mathtt{1}$.

$^\dagger$sebuah *string* dikatakan palindrom jika dan hanya jika *string* tersebut sama dengan kebalikannya.

- [ ] 1
- [ ] 2
- [ ] 3
- [ ] 4
- [ ] 5

**Soal 3.** Diberikan larik $[3, 1, 4, 1, 5, 9, 2, 6]$. Larik tersebut ingin dibagi menjadi dua sublarik sehingga selisih dari jumlah elemen masing-masing larik minimal. Setelah pembagian, kedua sublarik tidak boleh kosong. Berapakah selisih minimal tersebut?

- [ ] 0
- [ ] 1
- [ ] 2
- [ ] 3
- [ ] 4

**Soal 4.** Setiap hari, bebek bertambah $3$ kali lipat. Lalu Pak Dengklek menjual 5 bebek. Pada hari ke-3, tersisa 97 bebek. Berapa banyak bebek mula-mula?

- [ ] 5
- [ ] 6
- [ ] 7
- [ ] 8
- [ ] 9

**Soal 5.** Dalam sebuah pesta, setiap orang berjabat tangan dengan orang lain tepat sekali. Jika terjadi 45 jabat tangan, berapa orang yang ada di pesta tersebut?

- [ ] 8
- [ ] 9
- [ ] 10
- [ ] 11
- [ ] 12

**Soal 6.** Diberikan grid berukuran $5 \times 5$. Kotak $(1, 1)$ berada di atas kiri dan kotak $(5, 5)$ berada di kanan bawah. Berapa banyak jalur berbeda yang dapat dilalui dari $(1, 1)$ ke $(5, 5)$ tanpa melalui $(2, 2)$?

- [ ] 4
- [ ] 6
- [ ] 19
- [ ] 15
- [ ] 30

**Soal 7.** Empat orang $A$, $B$, $C$, dan $D$ memiliki nilai ujian yang berbeda-beda. Nilai mereka terdapat pada $\{80, 85, 90, 95\}$. Diketahui $A > B$, $B < C$, dan $C > D$. Manakah pernyataan di bawah ini yang pasti benar?

- [ ] $A > D$
- [ ] $C > A$
- [ ] $D > B$
- [ ] $A = 95$
- [ ] $B = 80$

**Soal 8.** Pak Budi memiliki 7 gelas ukur berukuran $\pu{8000 mL}$, $\pu{4000 mL}$, $\pu{2000 mL}$, $\pu{1000 mL}$, $\pu{500 mL}$, $\pu{250 mL}$, $\pu{125 mL}$. Lalu Pak Budi mengisi gelas $\pu{2000 mL}$, $\pu{1000 mL}$, $\pu{250 mL}$, $\pu{125 mL}$ dengan air sampai penuh.

Bu Sari memiliki 7 gelas ukur yang sama, dan ia mengisi gelas $\pu{4000 mL}$, $\pu{500 mL}$, $\pu{125 mL}$ dengan air sampai penuh.

Pak Joko juga memiliki 7 gelas ukur yang sama, yang awalnya kosong. Semua air di gelas-gelas Pak Budi dan Bu Sari akan dituang ke gelas-gelas Pak Joko sehingga setiap gelas terisi penuh atau kosong (tidak ada yang terisi setengah), dan tidak ada air yang terbuang.

Berapa banyak gelas ukur Pak Joko yang terisi penuh?

- [ ] 1
- [ ] 2
- [ ] 3
- [ ] 4
- [ ] 5

**Soal 9.** Pak Joko dan Pak Bambang main dengan kartu bernomor $1$ sampai $10$. Pak Joko mengambil 5 kartu dan membuang sisanya. Lalu Pak Bambang membuang 3 kartu dari 5 kartu tersebut. Terdapat 2 kartu yang tersisa. Selisih 2 kartu tersebut menjadi penentu: Pak Joko ingin selisih yang besar, dan Pak Bambang ingin selisih yang kecil. Jika keduanya bermain sebaik mungkin, berapa selisih akhirnya?

- [ ] 1
- [ ] 2
- [ ] 3
- [ ] 4
- [ ] 5

**Soal 10.** (graf)

**(Soal 11–13)** Perhatikan potongan program berikut.

```
int ember[100];

int hitung(int x) {
	if (x == 0) return 0;
	return (x % 2) + hitung(x / 2);
}

int main() {
	int n;
	cin >> n;
	
	for (int x = 0; x < (1 << n); x++) {
		int temp = hitung(x);
		ember[temp]++;
	}
}
```

**Soal 11.** Jika di bagian akhir program ditambahkan kode

```
for (int i = 0; i <= n; i++) {
	cout << ember[i] << " ";
}
```

 dan diberikan masukan `3`, apa keluaran program tersebut?

**Soal 12.** Jika di bagian akhir program ditambahkan kode

```
int a = 0;
int b = 0;

for (int i = 0; i <= n; i++) {
	if (i % 2 == 0) a += ember[i];
	else b += ember[i];
}

cout << a - b << endl;
```

dan diberikan masukan `20`, apa keluaran program tersebut?

**Soal 13.** Agar nilai `ember[5]` bisa menjadi $252$, berapakah masukan yang harus diberikan?

**Soal 14.** Apa keluaran dari program berikut?

```
void fungsi(int a, int b) {
	a = b + 2;
	b = a * 2;
}

int main() {
	int x = 3, y = 4;
	
	fungsi(x, y)
	
	cout << x;
	return 0;
}
```

**Soal 15.** Apa keluaran dari program berikut?

```
void fungsi(int &a, int b) {
	a = b + 2;
	b = a * 2;
}

int main() {
	int x = 3, y = 4;
	
	fungsi(x, y)
	
	cout << x;
	return 0;
}
```

**Soal 16.** Apa keluaran program di bawah?

```
#include <iostream>
using namespace std;

int arr[7] = {3, 5, 2, 1, 1, 7, 2};
int cnt[11] = {0};

int main() {
	for (int i = 0; i < 7; i++)
		cnt[arr[i]]++;
	
	for (int i = 1; i <= 10; i++)
		for (int j = 0; j < cnt[i]; j++)
			cout << i;
}
```

**Soal 17.** Berapa nilai dari `arr[9]` setelah program selesai?

```
#include <iostream>
using namespace std;

int main() {
	int arr[11];
	
	for (int i = 1; i <= 10; i++)
		arr[i] = i + 1;
	
	for (int i = 1; i <= 10; i++) {
		for (int j = i + 1; j <= 10; j++) {
			if (arr[i] == -1)
				break;
			
			int s = arr[j] / arr[i];
			
			if (s * arr[i] == arr[j]) {
				arr[i] = arr[i] + arr[j];
				arr[j] = arr[i] - arr[j];
				arr[i] = arr[i] - arr[j];
				
				arr[i] = -1;
			}
		}
	}
	
	for (int i = 1; i <= 10; i++)
		cout << arr[i] << " ";
}
```

**Soal 18.** Apa keluaran program berikut?

```
#include <iostream>
using namespace std;

int main() {
	int merpati = 2018;
	
	if (merpati % 100 > 20)
		merpati = merpati + 1;
	else
		merpati = merpati + 2;
	
	cout << merpati + merpati;
	return 0;
}
```

**Soal 19.** Perhatikan program berikut.

```
#include <iostream>
using namespace std;

int main() {
	long int n, r;
	cin >> n >> r;
	
	long int c = 0;
	
	for (int i = 1; i <= n; i++) {
		long int d = 1;
		for (int j = 1; j <= i; j++)
			d = d * r;
		
		c += d;
	}
	
	cout << c;
	return 0;
}
```

Jika diberi masukan `20 2`, maka keluaran program adalah ….

**Soal 20.** Perhatikan kode berikut.

```
#include <iostream>
using namespace std;

int main()
{
	long int n;
	cin >> n;
	
	long int c = 0;
	
	for (int i = 1; i <= n; i++)
		c += i;
	
	cout << c;
	return 0;
}
```

Jika diberi masukan `10`, apa keluaran program?