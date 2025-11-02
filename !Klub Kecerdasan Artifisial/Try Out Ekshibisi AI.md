---
sources:
  - https://instagram.com/belajar.academy
---
# Logika

> [!QUESTION] Logika 1
> Pak Dengklek adalah seorang agen lapangan yang ditugaskan untuk menyabotase satu titik (node) dalam jaringan komunikasi drone musuh. Jaringan ini terdiri dari 7 drone utama yang saling terhubung. Misi Dengklek adalah melumpuhkan drone yang akan menyebabkan kerusakan strategis paling besar.
> 
> Untuk menentukan target, Pak Dengklek harus mengikuti protokol pemilihan yang telah ditetapkan markas.
> 
> ### Protokol Pemilihan Target
> 
> Target harus dipilih berdasarkan urutan prioritas berikut.
> 
> ![[Logika 1.png]]
> 
> - **Prioritas Utama (Memecah Jaringan)**
> 	- Target yang dipilih harus drone yang jika dihilangkan akan memecah jaringan menjadi dua atau lebih bagian terpisah (dalam teori graf, ini disebut _articulation point_ atau _cut vertex_). Jika ada beberapa drone yang memenuhi kriteria ini, lanjutkan ke prioritas kedua.
> - **Prioritas Kedua (Kerusakan Maksimal)**
> 	- Di antara para kandidat dari prioritas pertama, pilih drone yang jika dihilangkan akan memutus total kapasitas data paling besar. Total kapasitas dihitung dari jumlah semua bobot koneksi (angka pada garis) yang terhubung langsung ke drone target.
> - **Prioritas Ketiga (Subterfuge Alfabetis)**
> 	- Jika setelah kriteria kedua masih ada hasil yang imbang, pilih drone dengan nama yang paling awal secara alfabetis sebagai target akhir untuk menghindari pola.
> 
> Berdasarkan visualisasi graf dari kode di atas dan protokol pemilihan target, drone manakah yang harus Pak Dengklek sabotase?
> 
> *Tuliskan jawaban dalam bentuk <u>huruf kapital</u>, contoh **FOXTROT**.*

> [!SUCCESS] Jawaban
> DELTA

---

> [!QUESTION] Logika 2
> Pak Budi adalah seorang manajer logistik yang baru saja menerima tanggung jawab atas sebuah gudang baru berukuran 10x14 meter. Seluruh lantai gudang akan dipasangi dengan rak penyimpanan modular. Setiap rak penyimpanan membutuhkan ruang seluas 1x2 meter (bisa dipasang vertikal maupun horizontal).
> 
> Namun, di beberapa titik di lantai gudang terdapat pilar-pilar penyangga struktural yang tidak bisa digeser, sehingga area tersebut tidak bisa digunakan untuk meletakkan rak. Pak Budi ingin memaksimalkan kapasitas gudang dengan memasang rak sebanyak mungkin di area lantai yang tersedia.
> 
> Berikut adalah denah gudang dengan posisi pilar (area yang tidak bisa digunakan) ditandai dengan petak hitam.
> 
> ![[Logika 2.png]]
> 
> Secara lebih presisi, pilar-pilar tersebut berada di koordinat (baris, kolom) berikut.
> 
> - (2, 3), (2, 4);
> - (5, 8), (6, 8);
> - (9, 1); dan
> - (10, 12).
> 
> Berapa banyak rak penyimpanan maksimal yang dapat dipasang oleh Pak Budi di area gudang yang tersedia?
> 
> *Tuliskan jawaban dalam bentuk <u>huruf kapital</u>, contoh **FOXTROT**.*

> [!SUCCESS] Jawaban
> 62

---

# Statistika dan Probabilitas

## Soal 1

Sebuah pabrik mencatat waktu perakitan (dalam detik) untuk 15 produk secara berurutan sebagai berikut.

$$ 15, 17, 18, 18, 19, 20, 21, 22, 23, 24, 25, 26, 28, 30, 32 $$

> [!QUESTION] Pertanyaan 1
> Berapa median dari data waktu perakitan tersebut?

> [!SUCCESS] Jawaban
> 22

---

> [!QUESTION] Pertanyaan 2
> Berapa jangkauan dari data tersebut?

> [!SUCCESS] Jawaban
> 17

---

> [!QUESTION] Pertanyaan 3
> Seorang auditor ingin memilih 3 catatan waktu secara acak. Berapa banyak kombinasi pemilihan yang mungkin jika ketiga waktu yang terpilih harus memiliki nilai di atas median?

$$ \binom{7}{3} = 5040. $$

> [!SUCCESS] Jawaban
> 5040

---

> [!QUESTION] Pertanyaan 4
> Manajemen menetapkan standar bahwa waktu perakitan di atas 25 detik dianggap lambat. Berapa persentase produk yang perakitannya tergolong lambat?

$$ \frac{4}{15} \times 100\% = 26.67\% $$

> [!SUCCESS] Jawaban
> 26.67%

---

## Soal 2

Sebuah gudang *e-commerce* besar mencatat data pengiriman 400 paket terakhir berdasarkan kategori barang dan metode pengiriman yang dipilih pelanggan. Datanya adalah sebagai berikut.

| Kategori     | *Same-Day* | *Next-Day* | *Reguler* | Total   |
| ------------ | ---------- | ---------- | --------- | ------- |
| Elektronik   | 20         | 50         | 30        | **100**     |
| Fashion      | 10         | 40         | 80        | **130**     |
| Buku         | 5          | 15         | 50        | **70**      |
| Rumah Tangga | 15         | 25         | 60        | **100**     |
| **Total**    | **50**     | **130**    | **220**   | **400** |

> [!QUESTION] Pertanyaan 1
> Jika sebuah paket dipilih secara acak dan diketahui paket tersebut dikirim menggunakan metode *Same-Day*, berapa peluang bahwa isi paket tersebut adalah elektronik?

$$ \frac{20}{50} = 0.4. $$

> [!SUCCESS] Jawaban
> 0.4

---

> [!QUESTION] Pertanyaan 2
> Sebuah paket dipilih secara acak dan ternyata isinya adalah buku. Berapa peluang bahwa paket tersebut dikirim menggunakan metode pengiriman *reguler*?

$$ \frac{50}{70} = 0.714. $$

> [!SUCCESS] Jawaban
> 0.714

---

> [!QUESTION] Pertanyaan 3
> Perusahaan mendapatkan keuntungan berbeda untuk tiap metode pengiriman pada barang Fashion
> 
> - *Same-day* (Rp50.000)
> - *Next-day* (Rp30.000)
> - *Reguler* (Rp 20.000)
> 
> Berapa rata-rata keuntungan (*expected profit*) yang didapat perusahaan per paket untuk kategori Fashion?

$$ \frac{10}{130}\mathrm{Rp}50000 + \frac{40}{130}\mathrm{Rp}30000 + \frac{80}{130}\mathrm{Rp}20000 = \mathrm{Rp}25384.615 $$

> [!SUCCESS] Jawaban
> Rp25.384,615

---

## Soal 3

Seorang inspektur kualitas di sebuah pabrik bola lampu sedang memeriksa produk dari lini perakitan. Diketahui bahwa probabilitas sebuah bola lampu mengalami cacat adalah 8% atau 0,08. Inspektur akan memeriksa bola lampu satu per satu hingga ia menemukan yang cacat untuk pertama kalinya. Setiap pemeriksaan bersifat independen.

> [!QUESTION] Pertanyaan 1
> Berapa peluang inspektur tersebut perlu memeriksa setidaknya 5 bola lampu hingga menemukan bola lampu cacat yang pertama?

> [!SUCCESS] Jawaban
> 0,716

---

> [!QUESTION] Pertanyaan 2
> Jika diketahui 3 bola lampu pertama yang diperiksa dalam kondisi baik (tidak cacat), berapa peluang ia akan menemukan 3 bola lampu baik berikutnya secara berurutan sebelum menemukan yang cacat?

---

> [!QUESTION] Pertanyaan 3
> Berapa peluang inspektur tersebut menemukan bola lampu cacat pertama tepat pada pemeriksaan ke-10?
> 

---

> [!QUESTION] Pertanyaan 4
> Berapa rata-rata jumlah bola lampu yang perlu diperiksa sampai seorang inspektur menemukan bola lampu cacat yang pertama?

---

# Aljabar Linear

Seorang animator game, Budi, sedang membuat animasi untuk karakter 2D. Ia menggunakan transformasi matriks untuk memutar dan mengubah ukuran karakternya.

Diberikan matriks-matriks transformasi sebagai berikut.

$$ \mathbf{R} = \begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix}, \text{dan} $$

$$ \mathbf{P} = \begin{bmatrix} 2 & 0 \\ 0 & \frac{1}{2} \end{bmatrix}. $$

Sebuah titik karakter dilambangkan dengan vektor $\mathbf{v} = \begin{bmatrix}4\\6\end{bmatrix}$.

1. Tentukan $\mathbf{R}\mathbf{v}$.
2. Tentukan $\mathbf{P}^2\mathbf{v}$.
3. Tentukan bentuk umum $\mathbf{R}^n$ dan $\mathbf{P}^n$.

---

$$ \begin{align*}
	\mathbf{R}\mathbf{v} &= \begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix} \begin{bmatrix} 4 \\ 6 \end{bmatrix} \\
	&= \begin{bmatrix} -6 \\ 4 \end{bmatrix}.
\end{align*} $$

---

# Optimasi dan Kalkulasi

Citra akan membuka usaha jasa penitipan hewan "Pet Stay". Ia ingin menentukan struktur biaya yang optimal. Biaya total untuk pelanggan dihitung dari biaya administrasi sekali bayar ($a$) ditambah dengan biaya penitipan per hari ($b$).

Citra melakukan survei kecil kepada tiga calon pelanggannya untuk mengetahui ekspektasi mereka.

| Calon Pelanggan | Hewan  | Lama Titip | Perkiraan Budget |
| --------------- | ------ | ---------- | ---------------- |
| Fira            | Kucing | 5          | 400              |
| Gilang          | Anjing | 10         | 750              |
| Hana            | Kucing | 8          | 600              |

Citra ingin menetapkan harga $a$ dan $b$ sehingga total biaya riil yang dibayar pelanggan sedekat mungkin dengan perkiraan budget mereka.

Nilai kesalahan diukur sebagai kuadrat dari selisih antara budget pelanggan dengan biaya riil yang harus mereka bayar, 

$$ a + (\text{lama titip}) \times b. $$

Nilai kesalahan total ($S$) adalah jumlah dari kesalahan untuk ketiga pelanggan tersebut.

Contohnya jika Citra menetapkan $a = 50$ dan $b = 70$, biaya riil untuk Gilang (10 hari) adalah $50 + 10×70 = 750$. Kesalahan untuk Gilang adalah $(750−750)^2=0$.

1. Jika Citra mencoba menetapkan biaya administrasi $a = 50$ dan biaya per hari $b = 70$, berapakah total nilai kesalahan ($S$) yang didapatkan?
2. Cari nilai $a$ dan $b$ ($a, b \geq 0$) yang menghasilkan nilai kesalahan total ($S$) paling kecil. Kemudian laporkan nilai kesalahan minimum tersebut ($S_\text{min}$​) dan pasangan $(a, b)$ yang mencapainya.