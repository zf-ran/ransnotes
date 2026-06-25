---
date: 2026-01-20
---

# Soal 1–3. Lampu Ramadan Pak Udin

#dynamic-programming 

Menyambut bulan suci Ramadan, Pak Udin ingin menghias halaman masjid di kampungnya dengan lampu-lampu hias. Lampu akan dipasang berderet lurus, satu demi satu, untuk mempercantik suasana malam Ramadan.

Ada dua jenis lampu.

- Lampu merah, yaitu lampu biasa yang boleh dipasang kapan saja.
- Lampu putih, yaitu lampu spesial Ramadan yang harus dipasang dengan rapi.

Pak Udin punya aturan khusus agar hiasan terlihat serasi.

- Lampu putih hanya boleh dipasang dalam subsegmen<sup>[?]</sup> yang terdiri dari tepat $k$ lampu putih berturut-turut.
- Lampu merah bebas dipasang satu persatu, tanpa batasan.

Lampu merah akan dilambangkan dengan $\mathtt{M}$ dan lampu putih dilambangkan dengan $\mathtt{P}$.

**Soal 1.** Saat ini, sementara Pak Udin sedang merahasiakan nilai dari $k$. Manakah susunan lampu berikut yang mungkin dipasang oleh Pak Udin? (Jawaban boleh lebih dari satu). %% YYYNYY %%

- [ ] $\mathtt{MMMM}$
- [ ] $\mathtt{PPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPP}$
- [ ] $\mathtt{MPMPMPMP}$
- [ ] $\mathtt{MMMPPMMMPPPMMMPPMMM}$
- [ ] $\mathtt{MMPMMMPMMMMPMMMMP}$
- [ ] $\mathtt{PM}$

**Soal 2.** Jika diberikan $k = 1$ sedangkan banyaknya lampu yang akan disusun oleh Pak Udin sejumlah $5$, tentukan banyaknya lampu yang dapat dipasang oleh Pak Udin. %% 13 %%

**Soal 3.** Saat ini Pak Udin menoleransi nilai $k$, di mana nilai $k$ bisa bernilai 2 buah bilangan. Jika $k = [2, 5]$, tentukan banyaknya lampu yang dapat disusun jika Panjang susunan lampu adalah $10$. %% 59 %%

---

# Soal 4–6. Pengumpulan Kartu Nilai di Kelas Matematika

#greedy #dynamic-programming

Di sebuah kelas matematika SD LB, guru memberikan sebuah kegiatan pengumpulan kartu nilai kepada siswa. Setiap siswa membawa beberapa kartu angka.

Setiap kartu berisi satu bilangan bulat positif. Guru ingin mengajak siswa berpikir strategis, bukan sekadar menghitung cepat, karena kalau semisal hanya cepat maka kalkulator murahan pun tentunya bisa saja dengan mudah melakukan hal tersebut.

Siswa boleh melakukan beberapa langkah. Pada setiap langkah, siswa akan melakukan hal berikut.

- Siswa memilih satu nilai bilangan $x$ yang masih ada.
- Semua kartu yang bernilai $x - 1$, $x$, dan $x + 1$ akan dikumpulkan kepada sang guru.
- Siswa memperoleh nilai sebesar $x$ poin **untuk setiap** kartu bernilai $x$ yang diambil pada langkah tersebut.

Kegiatan berakhir jika tidak ada kartu yang tersisa di papan.

**Soal 4.** Jika diberikan $5$ buah kartu dengan masing-masing memiliki nilai $[1, 2, 3, 4, 5]$, tentukan berapakah nilai maksimal yang akan didapat oleh siswa. %% 9 %%

**Soal 5.** Jika diberikan $16$ buah kartu dengan masing-masing memiliki nilai

$$ [4, 3, 3, 2, 3, 6, 6, 6, 3, 3, 6, 6, 2, 5, 5, 7], $$

tentukan berapakah nilai maksimal yang akan didapat. %% 45 %%

**Soal 6.** Jika kartu tertulis semua bilangan mulai dari $2$ hingga $15$ dengan banyaknya kartu pada masing-masing bilangan tersebut sejumlah bilangan bulat terbesar yang lebih kecil dari bilangan tersebut dan dapat membagi bilangan tersebut, maka tentukanlah nilai maksimal yang bisa didapat. %% 280 %%