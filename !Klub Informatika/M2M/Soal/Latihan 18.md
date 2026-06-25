---
date: 2026-02-05
---

# Soal 1–3. Formasi Energi di Dunia Kultivasi

Di dunia kultivasi, Tianxuan, terdapat $N$ kultivator yang sedang mengikuti Ujian Formasi Energi. Setiap kultivator berdiri di atas pilar *qi*, dan tiap pilar memiliki tingkat energi tertentu. Semakin tinggi angkanya, semakin kuat energi *qi*-nya.

Para kultivator ingin membentuk ikatan qi antar sesama untuk memperkuat formasi. Namun, Ketua Sekte memberi peringatan keras yaitu tidak boleh ada tiga kultivator berbeda $A$, $B$, dan $C$ dengan tingkat energi $A \leq B \leq C$, sehingga $A$ terikat *qi* dengan $B$ dan $B$ terikat *qi* dengan $C$. Menurut kitab kuno, susunan seperti itu akan menciptakan “Aliran *Qi* Bertingkat” yang membuat formasi meledak.

**Soal 1.** Jika terdapat 4 kultivator dengan tingkat energi 2, 3, 1, dan 2, maka maksimal hanya akan terdapat sebanyak 3 ikatan *qi* yang mungkin. Tentukan ada berapa banyak formasi yang dapat dibentuk. %% 4 %%

**Soal 2.** Jika terdapat 12 kultivator dengan tingkat energi 7, 2, 4, 9, 1, 4, 6, 3, 7, 4, 2, dan 3, tentukan banyaknya ikatan *qi* maksimal yang mungkin dibentuk.

**Soal 3.** Tentukan banyaknya kultivator minimal agar minimal terdapat sebanyak 2026 ikatan *qi* yang terbentuk!

---

# Soal 4–6. Legenda Pohon Hitam Kerajaan Daiyu

Di Kerajaan Daiyu, terdapat sebuah pohon suci, Namun karena kutukan kuno, semua desa yang terletak di simpul pada pohon itu awalnya berwarna hitam. Para Ketua Sekte ingin memurnikan pohon tersebut, sehingga seluruh desa berubah menjadi putih kembali.

Untuk melakukan pemurnian, Ketua hanya mengizinkan satu jenis ritual khusus. Dalam satu ritual, kamu boleh:

- memilih suatu desa ke-$i$;
- memilih sebuah jarak bilangan bulat $d$; lalu
- semua desa yang jaraknya tepat $d$ dari desa ke-$i$ akan berubah menjadi desa putih.

Jarak antara dua desa adalah jumlah jalan terpendek di antara keduanya. Desa yang sudah putih tetap putih jika terkena ritual lagi. Tugasmu adadalam menentukan Banyaknya ritual sesedikit mungkin agar seluruh desa di pohon berubah menjadi putih.

**Soal 4.** Pohon Suci tersebut berada di desa 1. Desa-desa terhubung dengan keterangan berikut.

- Desa ke-$1$ terhubung ke desa ke-$2$ dan desa ke-$3$.
- Desa ke-$2$ terhubung ke desa ke-$4$.
- Desa ke-$3$ terhubung ke desa ke-$5$.
- Desa ke-$4$ terhubung ke desa ke-$6$.

Tentukan banyaknya ritual minimal agar semua desa menjadi berwarna putih. %% 4 %%

**Soal 5.** Ada 7 desa dengan keterhubungan sebagai berikut.

- Desa ke-${} 5$ terhubung ke desa ke-$6$.
- Desa ke-$2$ terhubung ke desa ke-$4$ dan desa ke-$7$.
- Desa ke-$1$ terhubung ke desa ke-$3$ dan desa ke-$2$.
- Desa ke-$4$ terhubung ke desa ke-$5$.

Tentukan ritual minimal yang diperlukan agar semua desa menjadi desa putih. %% 4 %%

**Soal 6.** Jika terdapat 20 desa dengan keterhubungan sebagai berikut.

Untuk baris ke-$i$ pada tabel di bawah menyatakan bahwa $a_i$ terhubung dengan $b_i$.

| $a_i$ | $b_i$ |
| ----- | ----- |
| 8     | 14    |
| 1     | 4     |
| 10    | 15    |
| 6     | 12    |
| 4     | 8     |
| 2     | 6     |
| 1     | 3     |
| 9     | 16    |
| 5     | 11    |
| 4     | 5     |
| 12    | 18    |
| 3     | 7     |
| 7     | 13    |
| 6     | 10    |
| 10    | 17    |
| 11    | 19    |
| 2     | 20    |
| 1     | 2     |
| 14    | 16    |

Tentukan berapa banyak ritual khusus yang diperlukan untuk membuat semua desa menjadi desa putih!

---

# Soal 7–8. Makan Ayam Goreng

Perhatikan potongan kode berikut.

```
int ayam = 0;

void Makan(int n, int m) {
    ayam++;
	
    int goreng;
    
    if (n < m) {
        cout << "Enak\n";
        
        goreng = (m + n) / 2;
        
        Makan(n, goreng);
        Makan(goreng + 1, m);
    } else {
        cout << "Enak\n";
    }
}

int kecap(int zzz){
    for (int i = 0; i <= zzz; i++)
        Makan (1, i);
    
    return ayam;
}
```

**Soal 7.** Jika dipanggil $\mathtt{Makan}(1, 10)$, maka akan ada berapa buah baris yang tercetak? %% 19 %%

**Soal 8.** Tentukan nilai $n$ terkecil agar $\mathtt{kecap}(n) > 1000$. %% 31? %%