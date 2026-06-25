# Platform Permainan

Setiap tim akan maju ke depan kelas dan akan mengerjakan kuis dengan iTBoard. Tampilan pertama adalah tempat mengisi nama tim dan jumlah anggota. Misalkan $N$ adalah jumlah anggota.

Selanjutnya akan ada pilihan tingkat kesulitan soal, mulai dari mudah, sedang, dan sulit. Pada masing-masing tingkatan soal, terdapat skor masing-masing soal. Setiap soal memiliki skor benar $K$. Setiap soal adalah isian singkat yang terdiri dari 1 sampai 2 kata. Waktu pengerjaan untuk setiap tim adalah **5 menit**.

(Pada setiap saat, bagian atas layar akan menunjukkan skor dari tim tersebut.)

Setelah tim memilih tingkatan soal, waktu dimulai dan soal akan ditampilkan. Di bagian atas layar akan ditampilkan pertanyaan. Di bagian bawah layar akan ditampilkan papan tik yang telah diacak dan dibagi menjadi $N$ bagian. Setiap anggota tim bertanggung jawab pada bagian mereka masing-masing.

Papan tik terdiri dari huruf-huruf kapital, spasi, *backspace*, dan *submit* yang letaknya tentu akan diacak.

Setelah tim men-*submit* jawaban mereka, sistem akan mengecek apakah jawaban mereka benar atau tidak. Jika jawaban mereka benar, maka tim akan mendapat skor $K$ dan akan lanjut ke soal selanjutnya. Jika jawaban mereka salah, maka jawaban akan dihapus dan tim mengulangi soal **tanpa pengurangan nilai**. Jika tim memilih untuk menyerah pada suatu soal, maka mereka akan mendapat skor $-\frac{1}{2}K$ dan akan dilanjutkan ke soal berikutnya.

Pada pertanyaan terakhir, jika tim tidak dapat menjawab tepat waktu, maka akan terhitung menyerah dan mendapatkan skor $-\frac{1}{2}K$.

Setelah semua tim selesai, *leaderboard* akan menampilkan

- nama tim;
- total skor; dan
- banyak soal terjawab (baik yang benar maupun salah): mudah, sedang, sulit dipisah;

# Untuk *Developer*

Setiap soal akan dibentuk dalam objek JSON dengan template sebagai berikut.

```json
{
	"question": "",
	"difficulty": 0,
	"full_score": 1000,
	"answer": ""
}
```

*Key* `"question"` adalah sebuah *string* merepresentasikan pertanyaan. *Key* `"difficulty"` adalah sebuah angka 0, 1, atau 2 yang melambangkan sudah, sedang, dan sulit, berturut-turut. *Key* `"full_score"` adalah skor maksimum untuk sebuah soal (skor benar). *Key* `"answer"` adalah *string* jawaban yang hanya terdiri dari huruf kapital dan spasi.