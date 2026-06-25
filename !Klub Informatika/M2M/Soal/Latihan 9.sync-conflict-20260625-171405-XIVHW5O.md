---
date: 2025-12-18
---

# Soal 1–3. Revolusi Angka Volodya

Di sebuah kerajaan angka yang jauh di ujung bilangan, tinggallah seorang pemuda bernama Volodya. Volodya bukan orang biasa. Ia dikenal sebagai pemikir *nyeleneh*, seorang nonkonformis. Ia merasa dunia telah terlalu lama hidup di bawah aturan kuno. Urutan bilangan asli!

“Kenapa harus 1, 2, 3, 4, 5, …?” gerutu Volodya suatu pagi sambil memandangi barisan bilangan di buku aritmatikanya.

“Kenapa harus genap dan ganjil bercampur seperti itu? Ini tidak estetik! Tidak berjiwa!”

Dengan semangat revolusi, Volodya mengumumkan sebuah reformasi besar-besaran.

“Mulai hari ini, aku akan menyusun ulang urutan bilangan asli! Dunia harus tahu bahwa keadilan numerik dimulai dari estetika!” Dan dimulailah revolusi angka Volodya.

Volodya mengeluarkan aturan penyusunan baru.

- Kumpulkan dulu semua bilangan ganjil dari $1$ hingga $n$, lalu tulis mereka secara berurut dari yang paling kecil ke paling besar.
- Setelah itu, kumpulkan semua bilangan genap dari $1$ hingga $n$, dan tulis setelah semua bilangan ganjil, juga berurut dari yang paling kecil ke paling besar.

Sebagai contoh, jika $n = 10$, maka barisannya menjadi

$$ 1, 3, 5, 7, 9, 2, 4, 6, 8, 10. $$

Keren? Volodya merasa ini adalah mahakaryanya.

Namun, dunia tidak hanya butuh keindahan, dunia butuh jawaban.

Rakyat mulai bertanya kepada Velodya terkait dengan bilangan yang ia gunakan. Volodya memikirkan ini dengan serius. Sebagai orang jenius, bantulah Velodya menjawab pertanyaan rakyat!

**Soal 1.** <u>**BENAR** atau **SALAH**</u>: Dalam aturan Velodya, terdapat barisan bilangan sebagai berikut.

$$ 2, 4, 6, 8, 10, 12, 14, 1, 3, 5, 7, 9, 11, 13 $$

**Soal 2.** Jika terdapat sebanyak 100 buah bilangan, bilangan berapakah yang tertulis dalam barisan Velodya pada urutan ke-78?

**Soal 3.** Jika terdapat sebanyak 100 buah bilangan pada barisan Velodya, maka tentukan total selisih pada masing masing urutan yang ditulis oleh Velodya dengan bilangan asli yang sudah kita kenal.

---

# Soal 4–6. *Bineron Galaxy*

Di galaksi jauh, terdapat planet Bineron yang dihuni oleh makhluk-makhluk digital. Setiap tahun, mereka mengadakan seleksi untuk memilih Pemimpin Kode, sosok yang diyakini mampu membaca pola biner dan mengambil keputusan dalam sekejap.

Untuk itu, para kandidat harus menjalani ujian dari Oracle Binaris, sistem kecerdasan kuno yang menguji melalui papan biner rahasia. Papan ini awalnya diisi oleh kode utama, yaitu sebuah *string* biner$^\dagger$ $s$ sepanjang $n$.

Lalu, Oracle membuat $n$ versi modifikasi dari kode tersebut: masing-masing dibuat dengan membalik tepat satu bit dari posisi yang berbeda, satu per baris. Setiap modifikasi akan menguji kemampuan kandidat dalam mengenali pola perubahan dan menganalisis efek dari satu perubahan kecil. Setiap modifikasi akan disimpan pada larik $A$.

Contohnya jika $s = \mathtt{101}$, maka $A = [\mathtt{001}, \mathtt{111}, \mathtt{100}]$.

$^\dagger$*string* biner adalah *string* yang hanya berisi $\mathtt{1}$ atau $\mathtt{0}$.

**Soal 4.** Jika diberikan $s = \mathtt{0011}$, tentukan banyaknya $\mathtt{1}$ yang muncul pada larik $A$.

**Soal 5.** Jika diberikan $s = \mathtt{10101010}$, tentukan banyaknya $\mathtt{1}$ yang muncul pada larik $A$.

**Soal 5.** Jika diberikan $s$ adalah digit biner dari angka $2025$, tentukan banyaknya angka $\mathtt{1}$ yang muncul pada larik $A$.

---

# Soal 7–9. Proses

Perhatikan potongan program di bawah.

```
int proses(int a) {
    int b = 4;
    
    while (a > 0) {
        b += a % 10;
        a /= 10;
    }
    
    return a + b;
}
```

**Soal 7.** Tentukan hasil dari pemanggilan `proses(142)`.

**Soal 8.** Manakah dari masukan berikut yang menghasilkan keluaran dapat dibagi oleh $9$?

- [ ] 2020
- [ ] 2021
- [ ] 2022
- [ ] 2023
- [ ] 2024
- [ ] 2025

**Soal 9.** Tentukan bilangan **terkecil** yang lebih besar dari $2025$ sehingga hasilnya adalah bilangan paling kecil yang mungkin.