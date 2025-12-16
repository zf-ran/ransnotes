---
date: 2025-11-09
---

# Soal 1–3. Permen Pak Dengklek

Pak Dengklek membawa sejumlah permen ke kelasnya. Ia ingin membagikan permen kepada $N$ siswa yang sedang berbaris. Setiap siswa punya permintaan jumlah permen yang berbeda-beda. Pak Dengklek ingin membagikan permen kepada siswa dari depan ke belakang. Jika permennya tidak cukup untuk memenuhi permintaan siswa berikutnya, maka ia akan melewatkan siswa tersebut dan lanjut ke siswa berikutnya. Proses berhenti jika semua siswa sudah diperiksa atau permen Pak Denglek sudah habis. Tentukan berapa banyak siswa yang berhasil menerima permen sesuai permintaannya.

**Soal 1.** Pak Dengklek membawa 30 permen. Permintaan dari 10 siswa berturut-turut adalah 4, 5, 10, 3, 6, 2, 1, 7, 2, 4. Berapa siswa yang mendapat permen?

**Soal 2.** Pak Dengklek membawa 25 permen. Permintaan 7 siswa adalah 3, 8, 5, 2, 11, 2, 1. Namun sekarang jika permen tidak cukup, siswa boleh meminta ulang dengan jumlah setengah permintaan awal dibulatkan ke atas, tapi hanya sekali. Berapa siswa yang berhasil diberi permen?

**Soal 3.** Diberikan daftar permintaan permen dari beberapa siswa, kita boleh mengatur ulang urutan mereka supaya sebanyak mungkin siswa bisa menerima permen, asalkan total permen yang dimiliki Pak Dengklek tidak berubah. Sekarang Pak denglek memiliki sejumlah 2025 permen, uniknya lagi dari 1000 siswa yang berbaris, permintaan mereka adalah 1000 bilangan pertama dengan **semua penyusun angkanya tidak ada angka yang sama**. Tentukan berapa banyak siswa yang mendapatkan permen!

---

# Soal 4–6. Festival Lampion

Setiap tahun, Kota Binary mengadakan Festival Lampion. Warga kota menghias rumah dengan **lampu berwarna merah** (R) atau **biru** (B). Di setiap jalan, lampu-lampu dinyalakan dalam barisan dari kiri ke kanan.

Panitia festival memberikan beberapa aturan agar lampion terlihat indah:

Tidak boleh ada dua warna yang sama berdampingan lebih dari dua kali. Contah yang tidak valid adalah RRR dan BBB. Contoh yang valid adalah RR, BB, dan BR. Setiap susunan lampu harus memiliki jumlah lampu genap. Warga boleh memilih sendiri urutan warnanya selama aturan dipatuhi.

**Soal 4.** Panitia sedang membuat sistem pengecekan otomatis. Mereka menyusun algoritma berikut: “Mulai dari indeks ke-$1$, periksa setiap tiga lampu berturut-turut sebelumnya. Jika ditemukan pola yang semuanya sama (RRR atau BBB), tolak barisan lampu.”

Diberikan barisan 10 lampu,

$$ \texttt{B B R R R B R B B R} $$

Apakah algoritma akan menolak barisan ini? Jika iya, di indeks ke berapa ditemukan pelanggaran pertama?

- [ ] Tidak ada pelanggaran.
- [ ] Pelanggaran di indeks ke-2.
- [ ] Pelanggaran di indeks ke-3.
- [ ] Pelanggaran di indeks ke-5.

**Soal 5.** Seorang warga ingin menghias rumah dengan lampu sepanjang 8 unit. Ia ingin menghitung jumlah susunan berbeda yang mematuhi semua aturan festival. Berapa banyak kombinasi yang mungkin?

**Soal 6.** Kwak sekarang membantu warga menghias rumah secara otomatis. Tapi, ia hanya bisa menyimpan 3 warna terakhir di memorinya. Jika Kwak ingin memastikan bahwa setiap lampu yang ia tambahkan tidak membuat 3 warna yang sama berturut-turut, dan panjang target barisan adalah 12, berapa jumlah maksimum kombinasi valid yang Kwak bisa hasilkan dengan memorinya yang terbatas?

- [ ] Sama seperti jumlah kombinasi total.
- [ ] Lebih sedikit karena keterbatasan memori.
- [ ] Tidak bisa lebih dari 8 kombinasi.
- [ ] Harus menghentikan proses di lampu ke-6.

---

# Soal 7–9. ZLR

Perhatikan kode berikut.

```
int Z(int l, int r) {
    if (l < r) {
        int mid = (l + r) / 2;
        return Z(l, mid - 1) + Z(mid + 1, r) + 1;
    } else if (l == r) {
        return 1;
    } else {
        return 0;
    }
}
```
  
**Soal 7.** Tentukan hasil dari pemanggilan `Z(2, 8)`.

**Soal 8.** Tentukan nilai dari $a$ terkecil sehingga `Z(a, 2*a)` lebih besar dari $2^{10}$.

**Soal 9.** <u>**BENAR** atau **SALAH**</u>: Pemanggilan program tersebut sama dengan pemanggilan program dibawah ini.

```
int Z(int l, int r) {
    if (l >= r) return 1;
    int mid = (l + r) / 2;
    return Z(l, mid) + Z(mid + 1, r);
}
```

---

# Soal 10–11. >> <<

Perhatikan kode berikut.

```
int main() {
    int a, b, hasil = 0, temp = 1;
    cin >> a >> b;
    while (a > 0 || b > 0) {
        if ((a % 2) != (b % 2))
	        hasil += temp;

        a = a >> 1;
        b = b >> 1;
        temp = temp << 1;
    }
    cout << hasil << endl;
    return 0;
}
```

**Soal 10.** Apabila program di atas diberi masukan `8 2`, berapakah output yang dihasilkan oleh program tersebut?

**Soal 11.** Apabila program di atas diberi masukan `120 30`, berapakah output yang dihasilkan oleh program tersebut?