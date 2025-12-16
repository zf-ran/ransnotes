---
date: 2025-12-09
---

# Soal 1–3. Padepokan Tari Sekar Arum

Di sebuah desa di lereng Gunung Merapi, terdapat sebuah padepokan tari bernama Sekar Arum. Pimpinan padepokan, Mbakyu Ira, ingin menyiapkan sebuah pertunjukan khusus bernama *Tari Golek Candra Kinasih*. Untuk pertunjukan ini, ia harus memilih tepat $m$ penari dari $n$ murid. Para murid ini dinomori mulai dari 1 hingga $n$.

Murid ke-$i$ memiliki tingkat kematangan tari (level) yang dicatat sebagai angka $L_i$.
Tarian ini sangat sakral, sehingga hanya formasi penari tertentu yang dianggap sempurna.

Sebuah formasi dinyatakan sempurna jika semua syarat berikut terpenuhi.

- Tepat $m$ murid dipilih.
- **Tidak boleh** ada dua murid dengan tingkat kematangan yang sama.
- Selisih tingkat tertinggi dan terendah di antara penari harus kurang dari $m$. Dengan kata lain $\max(L) - \min(L) < m$.

**Soal 1.** <u>**BENAR** atau **SALAH**:</u> Di padepokan, Mbakyu Ira akan memilih $3$ murid dari $10$ murid dengan tingkat kematangan tari $L = [2, 4, 5, 7, 8, 4, 1, 4, 7, 8]$. *Tari Golek Candra Kinasih* dapat dilakukan.

**Soal 2.** Saat ini di padepokan, Mbakyu Ira akan memilih $2$ murid saja dari $8$ murid dengan tingkat kematangan tari $L = [1, 5, 2, 2, 3, 1, 3, 3]$. Ada berapa banyak cara Mbakyu Ira akan memilih murid jika $m = 2$.

**Soal 3.** Dengan sering viralnya *Tari Golek Candra Kinasih* ini, pada saat ini padepokan Mbakyu Ira memiliki murid yang sangat banyak, lebih tepatnya murid dengan tingkat kematangan $i$ berjumlah banyaknya faktor positif dari $i$, dengan nilai $i$ mulai dari $4$ hingga $10$, jika Mbakyu Ira akan memilih penari dengan jumlah $m = 5$, ada berapa banyak cara Mbakyu Ira memilih murid tersebut?

---

# Soal 4–6. Liga Fiktif Nusantara I

Di Liga Fiktif Nusantara I, kompetisi fiktif di Jawa, terdapat sebuah rumor bahwa beberapa pertandingan di fase *playoff* telah diatur sedemikian rupa sehingga jalur kemenangan beberapa klub terlihat “terlalu rapi”.

Panitia investigasi ingin melakukan simulasi komputasional untuk menilai apakah suatu skenario playoff tertentu mungkin tercapai secara natural atau mungkin mencurigakan. Anehnya Liga menggunakan format *playoff* eliminasi tunggal berisi $2^k$ klub. Klub diberi nomor kekuatan sebagai berikut.

- Klub 1 adalah klub terkuat.
- Klub $2^k$ adalah klub terlemah.

Klub berperingkat lebih tinggi selalu menang jika pertandingan berjalan normal. Bracket playoff menggunakan sistem seeding:

- *Seed* 1 vs *Seed* 2
- *Seed* 3 vs *Seed* 4
- *Seed* 5 vs *Seed* 6

Namun, sebagian posisi seed sudah “terisi” oleh klub tertentu, sebagian lagi kosong (belum diketahui). Kamu ingin menghitung berapa banyak cara penempatan seed yang masih tersisa sehingga hasil akhir playoff tepat mengikuti pola eliminasi tertentu (pola yang dicurigai sebagai ‘rekayasa’). Dalam artian

- Klub 1 meraih peringkat 1
- Klub 2 meraih peringkat 2
- Klub 3 dan 4 kalah pada semifinal meraih peringkat 3
- Klub 5, 6, 7, dan 8 yang kalah pada quarterfinal meraih peringkat 5

**Soal 4.** Apakah mungkin hasil akhir *playoff* sesuai dengan yang diharapkan untuk 4 tim jika tim 1 menempati *seed* 1, tim 2 menempati *seed* 2, tim 3 menempati *seed* 3, dan tim 4 menempati *seed* 4?

**Soal 5.** Ada berapa banyak penempatan seed yang mungkin memenuhi hasil akhir *playoff*, jika terdapat 4 tim yang bertanding dan *seed* 3 ditempati oleh tim 4.

**Soal 6.** Saat ini terdapat sebanyak 8 tim yang akan bertanding serta hanya terdapat 1 tim yang sudah mengisi seed, yakni tim 2 mengisi *seed* 5. Tentukan berapa banyak cara penempatan *seed* sehingga hasil akhir *playoff* sesuai dengan yang diharapkan.