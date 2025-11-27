# Soal 1–3: Kontraktor GBK (Gedung Bebek Kampungan)

Di sebuah negeri jauh bernama Pondok CP, terdapat sebuah kompetisi tahunan yang sangat bergengsi: Lomba Rancang Gedung Bebek Kampungan (LRGBK). Setiap tahun, para kontraktor bebek dari seluruh penjuru negeri berlomba-lomba untuk menciptakan gedung paling unik, paling tinggi, dan paling aneh, agar mendapatkan gelar prestisius “Gedung Bebek Terindah Sedunia”.

Tahun ini, panitia LRGBN membuat aturan baru yang cukup membingungkan pada bebek:

- Gedung harus memiliki tinggi total tepat 23 meter.  
- Setiap lantai hanya boleh dibuat dengan tinggi $\pu{2 m}$, $\pu{5 m}$, atau $\pu{10 m}$.  
- Kombinasi lantai boleh bervariasi, selama jumlah total tingginya tetap 23 meter.  
- Urutan lantai dianggap berbeda (misalnya lantai $\pu{2 m} + \pu{5 m} + \pu{10 m}$ berbeda dengan $\pu{5 m} + \pu{2 m} + \pu{10 m}$).

Seorang kontraktor bernama Pak Dengklek diminta merancang prototipe gedung ini.  
  
**Soal 1.** Pak Dengklek ingin tahu desain yang hemat biaya. Biaya terbesar datang dari jumlah lantai, karena makin banyak lantai makin banyak pintu lift yang harus dipasang. Dari semua variasi untuk tinggi 23 meter, berapa banyaknya lantai minimum yang mungkin?

**Soal 2.** Panitia tiba-tiba menambahkan aturan: lantai pertama (paling bawah) harus $\pu{2 m}$, karena dianggap lebih kokoh, sedangkan lantai terakhir (paling atas) harus $\pu{2 m}$, agar terlihat lebih imut. Dengan aturan baru ini, untuk tinggi $\pu{23 m}$, berapa banyak variasi yang dapat dibuat?

**Soal 3.** Tim operasional memperkirakan waktu pembersihan rutin per lantai untuk setiap regu kebersihan adalah sebagai berikut:

- 2 m → 26 menit.
- 5 m → 60 menit.
- 10 m → 125 menit.

Ada 3 regu kebersihan yang dapat bekerja paralel pada lantai berbeda, tetapi satu regu tidak boleh meloncat lewat lantai yang sedang dipakai regu lain (untuk menghindari selang dan kabel melintang di tangga). Regu boleh mulai dari bawah/atas sesuka hati, dan boleh berhenti di lantai mana pun. Tentukan berapa lama waktu minimumnya untuk tinggi $\pu{23 m}$.

---

# Soal 4–6: Tali Layang-Layang Pak Dengklek  

Di Festival Layang-Layang Nusantara, Pak Dengklek membuka stan “Bagi Tali”. Ada $N$ anak yang mengantri, dinomori dari anak ke-$1$ sampai anak ke-$N$. Setiap anak, anak ke-$P$ hanya mau menerima tali dengan panjang tepat $P$ meter untuk menerbangkan layang-layangnya.  

Di stan itu, Pak Dengklek hanya punya dua papan ukur:

- Papan ukur A selalu mengukur tepat $X$ meter.
- Papan ukur B selalu mengukur tepat $Y$ meter.

Ketentuan festival:
  
1. Setiap kali Pak Dengklek memotong tali, potongan itu langsung diberikan kepada satu anak yang sedang dilayani (tidak boleh disimpan untuk anak lain).  
2. Pak Dengklek tidak bisa mengukur sebagian dari papan, tidak ada “setengah $X$” atau “sepertiga $Y$”, dan sebagainya.

Akibatnya, anak ke-$P$ bisa dilayani jika dan hanya jika Pak Dengklek bisa mengukur tali sehingga mendapatkan **tepat** $P$ meter. Jika tidak ada cara mencapai tepat $P$ meter, maka anak ke-$P$ tidak bisa dilayani.  

Sebagai contoh jika $X = 2$ dan $Y = 5$ maka anak ke-5, ke-6 (2 + 2 + 2), dan ke-7 (2 + 5) bisa dilayani Pak Dengklek, namun anak ke-1 dan ke-3 tidak bisa dilayani.
  
**Soal 4.** Diberikan $N = 10$, dengan papan ukur $X = 3$ dan $Y = 5$. Tentukan ada berapa anak yang bisa menerima tali layangan dari Pak Dengklek?

**Soal 5.** Diberikan $N = 30$, dengan papan ukur $X = 6$ dan $Y = 4$. Tentukan ada berapa anak yang tidak bisa menerima tali layangan dari Pak Dengklek?

**Soal 6.** Diberikan $N = 1000$, dengan papan ukur $X = 6$ dan $Y = 15$. Tentukan ada berapa anak yang tidak bisa menerima tali layangan dari Pak Dengklek?

---

# Soal 7–9:  Eksplorasi Pesawat Ruang Angkasa

Di Galaksi ICIC, terdapat zona yang dipenuhi asteroid yang tidak aman untuk dimasuki. Peta galaksi direpresentasikan dalam sistem koordinat Kartesius 2D. Zona tersebut berbentuk poligon bersisi $N$. Setiap sudut diberi nomor dari $1$ hingga $N$. Sudut ke-$i$ terletak di $(X_i, Y_i)$. Pada setiap saat, Anda tidak boleh berada di dalam poligon ini; namun, aman untuk menyentuh sisi poligon.

Terdapat $Q$ skenario (dinomori dari $1$ hingga $Q$). Dalam skenario ke-$j$, Anda ingin pergi dari titik awal di $(A_j, B_j)$ ke titik akhir di $(C_j, D_j)$. Anda akan menaiki pesawat ruang angkasa khusus yang hanya dapat bergerak dalam garis lurus. Pertama, Anda mengatur arah pesawat ruang angkasa, kemudian pesawat akan mulai bergerak dalam arah tersebut. Selama perjalanan, Anda hanya diperbolehkan mengubah arah paling banyak satu kali. Mengubah arah berarti Anda menghentikan pesawat, mengatur arah baru, dan kemudian mulai bergerak lagi dalam arah baru.

**Soal 7.** Jika terdapat zona asteroid berbentuk poligon segi empat dengan masing masing titiknya berada pada koordinat $(0, 0)$, $(0,6)$, $(6, 6)$, $(6, 0)$. Tentukan jarak perjalanan terdekat yang bisa dilakukan dari koordinat $(0,2)$ menuju $(6,4)$. Tulis $-1$ jika perjalanan tersebut tidak dapat dilakukan.

**Soal 8.** Terdapat zona asteroid berbentuk poligon segi lima dengan masing masing titiknya berada pada koordinat $(0, 2)$, $(2, 0)$, $(4, 0)$, $(4, 4)$, $(2, 4)$. Tentukan luas dari zona asteroid tersebut.

**Soal 9.** Pada zona asteroid sebelumnya jika terdapat 4 skenario perjalanan yakni dari $(6, 1)$ menuju $(6, 3)$, dari $(3, 6)$ menuju $(0, 0)$, dari $(1, 4)$ menuju $(4, 1)$, dan dari $(3, 4)$ menuju $(3, 0)$. Tentukan total jarak perjalanan terdekat yang bisa dilakukan, jarak bernilai $-1$ jika perjalanan tersebut tidak dapat dilakukan.

---

# Soal 10–12: Panggil

```
int panggil(int n) {
    if (n == 2 || n == 1 || n == 0)
	    return n;
	
    return panggil(n - 1) + panggil(n - 3);
}
```

**Soal 10.** Berapa kalikah `panggil(2)` dipanggil saat pemanggilan `panggil(7)`?

**Soal 11.** Tentukan hasil dari pemanggilan `panggil(10)`.

**Soal 12.** Tentukan $n$ terkecil sehingga hasil dari pemanggilan `panggil(n)` merupakan bilangan prima yang bukan satu digit?

---

# **Soal 13–15: bebek-kebeb**

```
int N = 9;
int A[9] = {1, -2, 3, 4, 5, 4, 3, -2, 1};

int B[10];
B[0] = 0;

for (int i = 1; i <= N; i++) {
    B[i] = B[i - 1] + A[i - 1];
}

int bebek = 0;

for (int i = 1; i <= N; i++) {
    for (int j = i; j <= N; j++) {
        int kebeb = B[j] - B[i - 1];
        bebek = max(bebek, kebeb);
    }
}
```

**Soal 13.** Nilai `B[6]` adalah ….

~~**Soal 14.** Nilai `B[10] - B[8]` adalah ….~~ (Tidak ada jawaban)

**Soal 15.** Nilai akhir `bebek` adalah ….