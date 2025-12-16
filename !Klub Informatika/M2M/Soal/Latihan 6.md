---
date: 2025-12-11
---

# Soal 1–3. Liga Faktor Nusantara

Di Indonesia, Liga Faktor Nusantara dikenal sebagai liga yang paling unik. Selain kekuatan pemain dan strategi pelatih, ada satu hal aneh yang selalu dilakukan oleh Komite Liga sebelum kompetisi dimulai, mereka menentukan Nomor Tanpa Buntut $N$. Nomor Tanpa Buntut inilah yang akan memengaruhi jadwal pertandingan, format grup, dan distribusi hadiah.

Tidak ada yang tahu pasti bagaimana Nomor Tanpa Buntut bekerja dalam sistem tanding, tapi rumor mengatakan, bahwa semakin banyak faktor dari angka tertentu, semakin besar kemungkinan grup itu mendapatkan jadwal yang menguntungkan.

Oleh Karena itu, Komite Liga boleh memilih sebuah angka $K$ yang merupakan pembagi dari $N$, dengan syarat sebagai berikut.

- $K$ harus lebih besar dari $1$.
- Mereka lalu membuat angka baru $M = \frac{N}{K}$.
- $M$ memiliki sebanyak mungkin faktor.
- Jika terdapat lebih dari satu nilai $M$ yang memiliki banyak faktor yang sama, maka ambil yang terkecil.

Alasan teknisnya hanya dipahami oleh matematikawan liga, tetapi para suporter percaya, semakin banyak faktor $M$, makin fleksibel jadwal pertandingan.

**Soal 1.** Jika diberikan $N = 12$ tentukan nilai $M$.

**Soal 2.** Jika diperbolehkan untuk memilih lebih dari satu nilai $M$, maka ada berapa banyak nilai $M$ yang memenuhi jika diberikan nilai $N = 210$?

**Soal 3.** Diberikan nilai $N = 10!$, tentukan banyaknya faktor dari $M$.

---

# Soal 4–6. Pak Dengklek dan Papan Tulis Ajaib

Pada SMA Harapan Bangsa, ada seorang guru Matematika terkenal bernama Pak Dengklek. Pak Dengklek memiliki sebuah papan tulis ajaib yang bisa memanipulasi angka-angka yang tertulis padanya dengan cara yang tidak biasa.

Pada suatu hari, Pak Dengklek menuliskan $n$ bilangan positif di papan tulis

$$A = [A_1, A_2, \dots, A_n],$$

di mana setiap angka berada dalam rentang $1$ sampai $n$.

Pak Dengklek ingin membuat papan tulis itu memiliki **tingkat keindahan** setinggi mungkin. Tingkat keindahan adalah faktor persekutuan terbesar (FPB) yang dapat membagi semua angka yang tersisa di papan tulis.

Agar siswanya paham konsep FPB secara mendalam, Pak Dengklek memperbolehkan dua jenis operasi sebagai berikut.

1. **Operasi Hapus**
	- Pak Dengklek memilih satu angka dari papan tulis dan menghapusnya.
	- Operasi ini hanya boleh dilakukan maksimal $k$ kali.
	- Jika ada angka kembar, menghapus satu angka hanya menghapus satu di antara mereka.
2. **Operasi Pecah**
	- Jika ada angka $x$ $(x \geq 3)$ di papan tulis, Pak Dengklek dapat memecahnya menjadi tiga angka positif $a$, $b$, dan $c$, dengan syarat $a + b + c = x$ dan $1 \leq a \leq b \leq c$.
	- Angka $x$ dihapus dari papan tulis.
	- Hanya $a$ dan $c$ yang ditulis kembali.
	- Sementara $b$ dibuang.
	- Operasi ini boleh dilakukan sebanyak mungkin.

Sebagai siswa terbaik di kelas, kamu diminta oleh Pak Dengklek untuk membantu menentukan, Berapa **nilai maksimum** tingkat keindahan yang dapat dicapai dari angka-angka yang tersisa di papan tulis setelah melakukan paling banyak $k$ operasi hapus dan beberapa operasi pecah.

**Soal 4.** Jika dipapan tulis terdapat bilangan $A = [4,  9,  6, 8, 2, 6, 7, 8, 2]$, dan diberikan nilai $k = 1$, tentukan maksimum tingkat keindahan yang mungkin.

**Soal 5.** Jika dipapan tulis terdapat bilangan $A = [4,  9,  6, 8, 2, 6, 7, 8, 2, 7]$, dan diberikan nilai $k = 1$, tentukan maksimum tingkat keindahan yang mungkin.

**Soal 6.** Jika dipapan tulis terdapat bilangan

$$ A = [14, 12, 7, 12, 9, 9, 12, 4, 3, 1, 3, 6, 9, 13] $$

dan diberikan nilai $k = 3$, tentukan maksimum tingkat keindahan yang mungkin.