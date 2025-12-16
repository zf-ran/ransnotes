---
date: 2025-12-10
---

# Soal 1–3. Pak Dengklek dan Ujian Sekolah

Di sebuah SMA Negeri di Jawa Timur, ada seorang guru Matematika bernama Pak Dengklek. Selama satu tahun ajaran, sekolah mengadakan $n$ ujian. Setiap ujian ke-$i$ memiliki tingkat kesulitan $K_i$.

$$ K = [K_1, K_2, \dots, K_n] $$

Ada seorang siswa bernama Bima, yang sangat suka pola angka. Bima merasa tidak nyaman jika dua ujian yang berturutan memiliki tingkat kesulitan dengan FPB yang sangat kecil, dalam hal ini $\operatorname{FPB}(K_i, K_{i+1}) = 1$, Karena menurutnya, “dua ujian yang sulitnya tidak ada hubungannya pasti bikin pusing.” Banyak pasangan ujian berurutan dengan FPB-nya $1$ ini disebut sebagai **Tingkat Kekacauan Soal**.

Pak Dengklek boleh mengubah nilai kesulitan ujian tertentu menjadi $0$, karena $0$ mungkin dapat membuat FPB berubah. Tetapi untuk menjaga standar sekolah, ia hanya boleh melakukan ini maksimal $k$ kali.

Perlu diperhatikan bahwa $\operatorname{FPB}(0, a) = a$ untuk bilangan bulat positif $a$, dan $\operatorname{FPB}(0, 0) = 0$.

**Soal 1.** Diberikan tingkat kesulitan ujian $K = [6, 10, 7, 25, 12, 9]$. Jika Pak Denglek belum merubah sama sekali tingkat kesulitan soal, maka tentukanlah nilai dari Tingkat Kekacauan Soal.

**Soal 2.** Diberikan tingkat kesulitan ujian $K = [6, 10, 7, 25, 12, 9]$. Jika Pak Denglek boleh merubah **maksimal** satu ujian, maka tentukanlah nilai dari Tingkat Kekacauan Soal.

**Soal 3.** Di suatu semester yang cukup jenuh, terdapat $20$ ujian dengan tingkat kesulitan awal

$$ K = [1, 1, 2, 3, 4, 5, 5, 6, 6, 7, 8, 9, 10, 1, 1, 1, 2, 3, 1, 1]. $$

Jika Pak Denglek dapat mengubah **maksimal** 7 ujian, maka tentukan Tingkat Kekacauan Soal pada semester tersebut.

---

# Soal 4–6. Pak Lurah dan Tiga Hadiah Desa

Di sebuah desa di lereng pegunungan Jawa, ada tradisi tahunan bernama *Sedekah Desa Tiga Warna*. Dalam tradisi ini, Pak Lurah ingin membagikan tiga bingkisan hadiah kepada warga yang telah ditentukan sebelumnya.

Hadiah-hadiah ini harus memenuhi syarat sebagai berikut.

- Nilai masing-masing nilai hadiah adalah bilangan positif.
- Semua nilai hadiah harus berbeda.
- Tidak ada hadiah yang nilai angkanya habis dibagi $3$, karena angka itu dianggap “kurang membawa rezeki” menurut kepercayaan setempat.
- Jika nilai ketiga hadiah tersebut dijumlahkan, totalnya harus sama dengan angka yang ditetapkan panitia, yaitu $n$.

Terkadang total $n$ memungkinkan dibuat menjadi tiga hadiah seperti ini, terkadang tidak. Tugasmu sebagai panitia muda adalah menentukan apakah Pak Lurah bisa membuat tiga hadiah berbeda yang semuanya **bukan** kelipatan 3, dengan jumlah total $n$.

**Soal 4.** <u>**BENAR** atau **SALAH**</u>: Jika $n = 9$ maka *Sedekah Desa Tiga Warna* dapat dilakukan.

**Soal 5.** Jika $n = 11$, tentukan ada berapa banyak cara membagikan *Sedekah Tiga Warna* kepada 3 warga yang sudah ditentukan Pak Lurah?

**Soal 6.** Jika nilai $n = 30$, tentukan ada berapa banyak cara membagikan *Sedekah Tiga Warna* kepada 3 warga yang sudah ditentukan Pak Lurah?