---
date: 2026-02-03
---

# Soal 1–3. Jaringan Folder Rahasia

Di sebuah komputer milik lembaga riset, terdapat sistem folder rahasia. Struktur folder ini berbentuk pohon (*tree*).

Setiap folder hanya punya satu folder induk (kecuali folder utama yang tidak memiliki folder induk). Tidak ada folder yang terhubung membentuk siklus.

Seorang teknisi keamanan bernama Bebras ingin memetakan seluruh folder untuk keperluan audit sandi. Namun, sistem komputer ini memiliki keterbatasan unik. Bebras memiliki daftar koneksi folder (misalnya: folder $A$ terhubung langsung ke folder $B$). Daftar ini disimpan dalam urutan tertentu.

Sistem bekerja seperti berikut.

- Awalnya, hanya folder utama (folder $1$) yang sudah dikenali. Sistem akan memindai seluruh daftar koneksi dari atas ke bawah.
- Saat menemukan koneksi:
	- Jika satu folder sudah dikenali dan folder lainnya belum, maka folder yang belum dikenali langsung dikenali dan ditambahkan ke peta.
- Setelah satu kali pemindaian selesai:
	- Jika masih ada folder yang belum dikenali, sistem mengulang pemindaian dari awal.
	- Proses berhenti jika semua folder sudah dikenali.

Setiap kali sistem memindai seluruh daftar koneksi dari awal sampai akhir, itu disebut satu kali pemindaian.

**Soal 1.** Berapa kali sistem memindai 3 koneksi folder berikut?

- Folder $3$ terhubung dengan folder $4$.
- Folder $2$ terhubung dengan folder $3$.
- Folder $1$ terhubung dengan folder $2$.

**Soal 2.** Berapa kali sistem memindai 5 koneksi folder berikut?

- Folder $4$ terhubung dengan folder $5$.
- Folder $1$ terhubung dengan folder $3$.
- Folder $1$ terhubung dengan folder $2$.
- Folder $3$ terhubung dengan folder $4$.
- Folder $1$ terhubung dengan folder $6$.

**Soal 3.** Berapa kali sistem memindai 20 koneksi folder berikut? Tuliskan $-1$ jika tidak mungkin.

- Folder $8$ terhubung dengan folder $14$.
- Folder $1$ terhubung dengan folder $4$.
- Folder $10$ terhubung dengan folder $15$.
- Folder $6$ terhubung dengan folder $12$.
- Folder $4$ terhubung dengan folder $8$.
- Folder $2$ terhubung dengan folder $6$.
- Folder $1$ terhubung dengan folder $3$.
- Folder $9$ terhubung dengan folder $16$.
- Folder $5$ terhubung dengan folder $11$.
- Folder $4$ terhubung dengan folder $5$.
- Folder $12$ terhubung dengan folder $18$.
- Folder $3$ terhubung dengan folder $7$.
- Folder $7$ terhubung dengan folder $13$.
- Folder $6$ terhubung dengan folder $10$.
- Folder $10$ terhubung dengan folder $17$.
- Folder $11$ terhubung dengan folder $19$.
- Folder $2$ terhubung dengan folder $20$.
- Folder $1$ terhubung dengan folder $2$.

---

# Soal 4–6. Kibor Sempurna

Polycarp ingin membuat *keyboard* satu baris yang berisi semua huruf ‘a’ sampai ‘z’ tepat sekali masing-masing. Ia juga punya sebuah kata sandi $s$ yang selalu ia gunakan. Agar mengetik kata sandi itu mudah, setiap dua huruf yang bersebelahan dalam $s$ harus bersebelahan juga pada *keyboard* yang dibuat. Tidak ada dua huruf sama yang bersebelahan di $s$.

Contoh, jika $s = \mathtt{abacaba}$, maka *keyboard*

$$ \mathtt{c a b d e f g h i j k l m n o p q r s t u v w x y z} $$

valid karena

- $\mathtt{a}$ bersebelahan dengan $\mathtt{c}$ pada $s$ dan pada *keyboard*;
- $\mathtt{a}$ bersebelahan dengan $\mathtt{b}$ pada $s$ dan pada *keyboard*; dan seterusnya.

**Soal 4.** <u>**BENAR** atau **SALAH**</u>: Ada suatu *keyboard* yang memudahkan sandi $s = \mathtt{abcda}$.

**Soal 5.** <u>**BENAR** atau **SALAH**</u>: Ada suatu *keyboard* yang memudahkan sandi $s = \mathtt{adadapururtekismsikekism}$.

**Soal 6.** Berapa banyak *keyboard* yang memudahkan sandi $s = \mathtt{adadabcefghijklmnop}$ dan *string* $\mathtt{rstuvw}$.

---

# Soal 7–9. Peternakan

Perhatikan potongan kode berikut.

```
int hitungKandang(int ayam, int bebek) {
	int kambing = 1, sapi = ayam;
	
	while (sapi > bebek) {
		kambing *= sapi;
		--sapi;
	}
	
	int kuda = ayam - bebek;
	
	while (kuda > 1) {
		kambing /= kuda;
		--kuda;
	}
	
	return kambing;
}
 
int hitungBanyakKandang(int ayam, int bebek, int itik) {
	int totalDomba = 0;
	int domba = bebek;
	
	while (domba <= itik) {
		totalDomba += hitungKandang(ayam, domba);
		++domba;
	}
	
	return totalDomba;
}
```

**Soal 7.** Tentukan hasil dari pemanggilan $\mathtt{hitungKandang}(10, 2)$.

**Soal 8.** Tentukan hasil dari pemanggilan $\mathtt{hitungBanyakKandang}(6, 2, 4)$.

**Soal 8.** Tentukan hasil dari pemanggilan $\mathtt{hitungBanyakKandang}(11, 2, 9)$.