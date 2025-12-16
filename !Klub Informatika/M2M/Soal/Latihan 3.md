---
date: 2025-11-21
---

# Soal 1–3. Laboratorium Geometri

Kamu sedang berada dalam sebuah laboratorium geometri yang mempelajari bangun beraturan. Di depanmu terdapat sebuah poligon beraturan yang memiliki $N$ sisi. Pada setiap sisi, para peneliti telah meletakkan beberapa titik khusus. Titik-titik ini berada di sepanjang sisi dan membagi sisi tersebut menjadi bagian-bagian yang sama panjang. Untuk setiap sisi ke-$i$, ada sebanyak $A_i$ titik khusus; dan sisi-sisi diurutkan secara searah jarum jam.

Tugas penelitianmu adalah membangun **sebanyak mungkin** segitiga yang tidak saling berpotongan. Setiap segitiga harus memakai 3 titik khusus yang berbeda, dan setiap titik hanya boleh dipakai 1 kali. Segitiga harus *non-degenerate*, artinya luasnya harus positif. Jadi, ketiga titiknya tidak boleh berada pada garis lurus yang sama.

Sebagai contoh jika $A = [3, 1, 4, 6]$ maka kita dapat membuat sebanyak 4 buah segitiga seperti pada gambar.

![[Latihan 3 Soal 1–3.png]]

**Soal 1.** <u>**BENAR** atau **SALAH**</u>: Misalkan terdapat suatu poligon yang tidak diketahui ukurannya, namun diketahui terdapat sebanyak 18 titik khusus pada sisi-sisinya. Titik-titik di sekeliling poligon diberi nomor dari 1 sampai 18 secara berurutan searah jarum jam. Segitiga pertama memakai titik $[2, 7, 12]$. Segitiga kedua yang memakai titik $[3, 4, 5]$ **pasti** tidak memotong segitiga pertama.

**Soal 2.** Jika diberikan $A = [1, 6, 3, 6, 2]$ maka ada berapa banyak segitiga yang dapat dibuat?

**Soal 3.** Sebuah poligon memiliki total 31 titik khusus. Namun saat ini, pada masing-masing sisi tidak boleh dipakai lebih dari 4 titik secara total dalam semua segitiga. Jika pada salah satu sisi terdapat 11 titik, berapa banyak segitiga maksimum yang tetap bisa dibuat?

---

# Soal 4–6. Kecantikan Kandang Bebek

Di sebuah peternakan besar, Pak Ganesh memelihara $n$ ekor bebek yang dinomori mulai dari $1$ hingga $n$, dan setiap bebek memiliki:

- Kebutuhan pakan harian yang dicatat dalam *array* $K = [K_1, K_2, \dots, K_n]$. Di mana $K_i$ menyatakan kebutuhan pakan harian bebek ke-$i$.
- Jumlah pakan yang benar-benar diberikan oleh pekerja kandang dicatat dalam *array* $P = [P_1, P_2, \dots, P_n]$. Di mana $P_i$ menyatakan pakan yang benar benar diberikan oleh pekerja kepada bebek ke-$i$.

Untuk menilai seberapa “cantik” manajemen kandang pada hari itu, Pak Ganesh mendefinisikan Nilai Kecantikan Kandang sebagai

$$ \sum_{i=1}^{n} |K_i - P_i| = |K_1 - P_1| + |K_2 - P_2| + \cdots + |K_n - P_n|, $$

atau dengan kata lain, jumlah dari selisih-selisih antara pakan seharusnya dan sebenarnya.

Semakin besar Nilai Kecantikan Kandang, semakin “unik” pula kandang tersebut. Karena artinya, banyak selisih yang ekstrem antara kebutuhan dan pemberian pakan. Pak Ganesh ini kandangnya **seunik** mungkin.

Ternyata, pekerja kandang terkadang salah menaruh pakan di antara bebek. Oleh karena itu, Pak Ganesh boleh menukar pakan dua bebek maksimal satu kali, karena jika lebih dikhawatirkan para pekerja tersinggung jika Pak Ganesh banyak menukar pakan yang sudah dengan lelah mereka berikan kepada para bebek.

Dengan kata lain, pilih dua indeks $i$ dan $j$ $(i \neq j)$, kemudian tukar $P_i$ dan $P_j$.

**Soal 4.** Diberikan kebutuhan pakan bebek $K = [3, 5, 2]$, dan pakan sebenarnya $P = [4, 1, 2]$. Hitung Nilai Kecantikan Kandang maksimum.

**Soal 5.** Diberikan kebutuhan pakan bebek $K = [1, 5, 4, 20]$, dan pakan sebenarnya $P = [4, 2, 10, 7]$. Hitung Nilai Kecantikan Kandang maksimum.

**Soal 6.** <u>**BENAR** atau **SALAH**</u>: Jika kedua *array* sudah diurut menaik, maka pertukaran acak **selalu** membuat Nilai Kecantikan Kandang menurun.