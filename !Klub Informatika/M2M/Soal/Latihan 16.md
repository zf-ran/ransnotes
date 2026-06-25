# Soal 1–3. Kalender Suku Ayam

Di sebuah daerah pegunungan, hiduplah Suku Ayam, sebuah suku yang memiliki sistem penanggalan unik. Mereka menggunakan Kalender Suku Ayam yang berputar setiap 1024 hari. Setiap hari diberi nomor dari $0$ sampai $1023$.

Hari bernomor $0$ disebut **Hari Istirahat Ayam**, yaitu hari libur besar di mana seluruh ayam tidak boleh bekerja, selain itu juga ada beberapa hari libur besar hanya saja sebagian saja yang mungkin mengetahuinya.

Hari dengan nomor lain adalah hari biasa.

Suatu hari, batu kalender suku ini bergeser dan beberapa hari menunjukkan angka yang keliru.

Tetua Suku Ayam meminta bantuan untuk menjadikan beberapa hari tersebut menjadi Hari Istirahat Ayam yaitu mengubahnya menjadi $0$.

Namun, batu kalender hanya bisa diubah dengan dua ritual khusus. Misal saat ini kalender menunjukkan angka $k$.

- Ritual Melangkah: Tetua ayam berkokok sepuluh kali, menjadikan satu hari ke depan $(k + 1) \bmod 1024$.
- Ritual Menggandakan: Seluruh ayam berkokok bersamaan sehingga hari menjadi dua kali lipat $(2k) \bmod 1024$.

Semua perhitungan selalu dilakukan modulo 1024 karena kalender pada suku ayam ini hanya memiliki angka mulai dari $0$ hingga $1023$.

**Soal 1.** Jika sebuah tanggal menunjukkan angka $15$, berapa kali ritual khusus minimal yang diperlukan agar tanggal tersebut menjadi Hari Istirahat Ayam? %% 7 %%

**Soal 2.** Diberikan beberapa tanggal berikut, tentukan manakah tanggal yang paling sedikit memerlukan ritual sehingga tanggal yang diberikan menjadi Hari Istirahat Ayam! %% 765 %%

- [ ] $3$
- [ ] $997$
- [ ] $765$
- [ ] $252$
- [ ] $16$
- [ ] $15$
- [ ] $14$
 
**Soal 3.** Jika $x$ adalah nilai terbesar dari semua angka yang memerlukan jumlah langkah paling sedikit untuk mencapai Hari Istirahat Ayam, maka berapakah nilai $x$? %% 0 %%

---

# Soal 4–6. Lampu Gedung Kota

Aan tinggal di sebuah kota kecil yang hanya memiliki satu jalan utama yang sangat panjang.

Di sepanjang jalan itu terdapat gedung yang berdiri berjajar dari kiri ke kanan. Setiap gedung memiliki lampu hias di atapnya. Tinggi gedung menentukan seberapa terang lampu terlihat dari kejauhan.

Aan mendapat tugas dari wali kota untuk membuat kota tampak lebih indah saat malam hari. Sebuah gedung disebut gedung sorotan utama jika

- lampunya lebih tinggi dan lebih terang daripada gedung di sebelah kiri; dan
- lampunya lebih tinggi dan lebih terang daripada gedung di sebelah kanan.

Gedung seperti ini terlihat menonjol di antara dua tetangganya dan membuat jalan kota tampak hidup. Aan boleh menaikkan tinggi lampu di beberapa gedung dengan cara menambahkan lantai di beberapa gedung. Menambah tinggi Gedung tentunya memerlukan biaya, jadi Aan tidak ingin berlebihan. Membuat jumlah gedung sorotan utama sebanyak mungkin, namun wali kota menginginkan banyak Gedung sorotan utama banyaknya semaksimal mungkin yang bisa.

**Soal 4.** Jika terdapat 100 gedung maka maksimal akan ada berapa banyak Gedung sorotan utama yang dapat dibuat. %% 49 %%
 
**Soal 5.** Berapa jumlah minimum total banyaknya lantai yang harus ditambahkan agar jumlah gedung sorotan utama menjadi maksimal pada rangkaian 8 gedung dengan ketinggian berturut-turut $[4, 2, 1, 3, 5, 3, 6, 1]$. %% 3 %%
 
**Soal 6.** Berapa jumlah minimum total banyaknya lantai yang harus ditambahkan agar jumlah gedung sorotan utama menjadi maksimal pada rangkaian 32 gedung dengan ketinggian berturut-turut

$$ [3, 5, 2, 3, 4, 5, 8, 3, 6, 2, 1, 4, 6, 7, 3, 6, 7, 9, 3, 7, 3, 5, 3, 1, 4, 5, 1, 3, 1, 4, 2, 2]. $$

%% 26 %%

---

# Soal 7–9. Mencari $N$

Perhatikan kode berikut.

```
int mencari(int N) {
    int hasil = 0;
    
    for (int i = 1; i <= N; i++) {
        int j = 1, z = 0;
        
        while (j <= i) {
            if (i % j == 0)
	            z++;
	        
            j++;
        }
        
        if (z % 2 != 0)
            hasil++;
    }
    
    return hasil;
}
```


**Soal 7.** Berapakah nilai yang dihasilkan dari pemanggilan $\mathtt{mencari}(10)$? %% 3 %%
 
**Soal 8.** Berapakah nilai yang dihasilkan dari pemanggilan $\mathtt{mencari}(2026)$? %% 45 %%

**Soal 9.** Jika hasil dari pemanggilan $\mathtt{mencari}(N) - \mathtt{mencari}(M) = 2026$ dan $1 \leq M \leq 10$, tentukan nilai $N - M$ terbesar yang mungkin. %% 4120890 %%