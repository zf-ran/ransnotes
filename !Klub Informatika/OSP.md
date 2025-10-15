# Soal Olimpiade Sains Pemuda

> [!abstract] Detail
> - **Tanggal:** Minggu, 12 Oktober 2025
> - **Waktu:** 14.00–15.00
> - **Jumlah Soal:** 50

1. Apa hasil yang dikembalikan dari menjalankan fungsi `seru(asik(15, 9, 2000), 9, 2000)`?
	- [ ] 18006
	- [ ] 19009
	- [ ] 10024
	- [ ] 13000
	- [ ] 18000
2. Kwak bertanya pada 120 orang untuk menebak sebuah angka yang merupakan permutasi dari 12345 yang sedang dipikirkannya. Setiap orang mencoba menebak permutasi yang benar. Ada 10 orang yang menebak sebuah permutasi yang berbeda dengan pikiran Kwak dalam 5 tempat. Ada 45 orang yang menebak sebuah permutasi yang berbeda dengan pikiran Kwak dalam 4 tempat. Ada 45 orang yang menebak sebuah permutasi yang berbeda dengan pikiran Kwak dalam 3 tempat. Ada 15 orang yang menebak dan berbeda dalam 2 tempat. Ada $M$ orang yang menebak dengan tepat. Ada $N$ orang yang menebak dan berbeda dalam 1 tempat.
	
	Berapa nilai $M - N$?
	- [ ] 5
	- [ ] 4
	- [ ] 3
	- [ ] 2
	- [ ] 1
3. Pak dengklek sangat suka makan bakso. Oleh karena itu, pada suatu hari ia berpikir jika ia ingin memotong sebuah bakso sebanyak 3 kali, berapa paling banyak jumlah potongan yang bisa ia dapat?
	- [ ] 6
	- [ ] 7
	- [ ] 8
	- [ ] 9
	- [ ] 10
4. Perhatikan program berikut!
	```pascal
	function yolo(x, y: integer): integer;
	begin
		if (y = 0) then yolo := x
		else yolo := yolo(y, x mod y) * yolo(y mod x, x mod y) * y;
	end;
	
	begin
		writeln(yolo(19, 5));
	end;
	```
	Bila fungsi `yolo(9, y)` dipanggil dan fungsi tersebut mengembalikan nilai 4, maka berapakah nilai `y`?
	- [ ] 1
	- [ ] 2
	- [ ] 3
	- [ ] 4
	- [ ] 5
5. Panitia penyelenggara OSN bagian akomodasi mengatur penempatan para delegasi wakil-wakil provinsi di sebuah hotel. Delegasi-delegasi itu masing-masing dengan anggota yang jumlahnya bervariasi, dan rencana kedatangannya pun tidak bersamaan. Para anggota delegasi yang sama diasumsikan datang bersamaan. Karena jumlah kamar di hotel itu agak terbatas, panitia menetapkan suatu pengaturan. Selama kamar-kamar kosong masih tersedia, setiap kamar kosong ditempati oleh dua orang dari delegasi yang sama. Jika jumlahnya ganjil, yang satu orang itu pun ditempatkan di kamar yang kosong. Saat tidak ada kamar kosong tersisa, setiap orang yang baru datang akan ditempatkan di kamar yang baru ditempati sendirian.

	Jika ada beberapa pilihan kamar kosong, selalu dipilih kamardengan nomor yang paling kecil. Jika tidak ada lagi kamar kosong, tapi ada beberapa kamar yang masih satu orang, juga dipilih mulai dari kamar dengan nomor terkecil. Sekarang Anda ketahui ada 8 kamar di hotel itu dan ada 8 delegasi yang akan datang yang jumlahnya berturut-turut sesuai dengan urutan waktu kedatangan adalah 3, 1, 3, 2, 1, 3, 2, 1. Jika kamar dinomori dari 1 sampai 8, dan delegasi dinomori sesuai dengan urutan kedatangan dari 1 sampai 8, dengan siapakah anggota delegasi provinsi ke-8 akan sekamar?
	- [ ] 5
	- [ ] 9
	- [ ] 6
	- [ ] 7
	- [ ] ?
6. Perhatikan potongan algoritma berikut!
	```pascal
	for i := 1 to n do
		for j := 1 to n do
			XX(i, j);
	```
	Misalnya `XX(i, j)` dijalankan dengan nilai berapa pun bersifat konstan, dan potongan algoritma itu dengan nilai $n = 100$ diperlukan waktu rata-rata 1 detik. Kira-kira berapa detik potongan algoritma ini dijalankan untuk nilai $n = 2000$?
	- [ ] 400
	- [ ] 500
	- [ ] 600
	- [ ] 700
	- [ ] 800
7. Iwan selalu berbohong pada hari Senin, Selasa, dan Rabu; serta berkata jujur pada hari-hari lainnya. Di lain pihak, Budi selalu berbohong pada hari Kamis, Jumat, dan Sabtu; serta berkata jujur pada hari-hari lainnya. Pada suatu hari terjadi percakapan berikut.
	
	- Iwan: “Kemarin saya berbohong.”
	- Budi: “Saya juga.”
	
	Pada hari apa percakapan tersebut terjadi?
	- [ ] Senin
	- [ ] Selasa
	- [ ] Rabu
	- [ ] Kamis
	- [ ] Jumat
8. Diberikan sebuah array.
	$$ A = [1, 4, 5, 2, 3, 7, 5, 9, 10, 6, 7]. $$
	
	Tentukan berapakah panjang dari *longest increasing subsequence*!
	
	*Subsequence* adalah himpunan bagian terurut dari *array* tersebut, di mana mereka tidak harus bersebelahan. Contoh *subsequence* dari $A$ adalah $[1, 2, 3],$ $[4, 5, 10],$ dan $[7, 6, 7]$. Namun $[5, 6, 7, 8]$ bukan *subsequence* dari $A$.
	- [ ] 9
	- [ ] 4
	- [ ] 7
	- [ ] 6
	- [ ] 5
9. Berapa banyaknya cara mengubah susunan kata “MINUMAIR” jika huruf N dan R harus saling berdampingan?
	- [ ] 4250
	- [ ] 2520
	- [ ] 2650
	- [ ] 2720
	- [ ] 2820
10. Perhatikan program berikut!
	```pascal
	a := 21;
	b := 12;
	
	while (a >= b) do begin
		a := a - 2;
		b := b + 1;
		c := a + b;
	end;
	
	writeln(a + b + c);
	```
	Output dari potongan program di atas adalah ….
	- [ ] 52
	- [ ] 54
	- [ ] ?
	- [ ] ?
	- [ ] ?
11. Perhatikan program berikut!
	```pascal
	function cimi(x, y: integer): integer;
	begin
		if (x + y = 0) then begin
			cimi := 0;
		end else if (x > y) then begin
			y + cimi(x - 1, y);
		end else begin
			cimi := x + cimi(x, y - 1);
		end;
	end;
	```
	Nilai dari `cimi(5, 8` adalah ….
	- [ ] 40
	- [ ] 50
	- [ ] 60
	- [ ] ?
	- [ ] ?
12. Dalam sebuah pertandingan renang antar RW terdapat 8 orang peserta, yaitu A, B, C, D, E, F, G, dan H. Setelah pertandingan dilakukan secara tertutup, Pak Lurah yang merupakan juri mengumumkan hasilnya. Ia tidak mengumumkan urutan peringkat dari 1 sampai 8, tetapi hanya memberikan beberapa fakta mengenai pertandingan, yaitu sebagai berikut.
	- E berada 3 peringkat di bawah B, dan 4 peringkat di atas F.
	- Peringkat A lebih baik dari D, dan peringkat D lebih baik dari H.
	- Selisih peringkat A dan D sama dengan selisih peringkat D dan H.
	
	Ada berapakah banyaknya kemungkinan peringkat yang sesuai dengan fakta di atas?
	- [ ] 8
	- [ ] 7
	- [ ] 6
	- [ ] 5
	- [ ] 4
13. Iwang dan Bimo sedang bermain sebut bilangan. Pada permainan ini, pemain akan bergantian menyebutkan barisan bilangan yang banyak bilangannya adalah lebih satu dari banyak bilangan yang disebutkan sebelumnya. Mereka sepakat bahwa Iwang akan bermain pertama dan selalu menyebutkan bilangan ganjil, sementara Bimo akan selalu menyebutkan bilangan genap. Sehingga permainan awalnya adalah Iwang akan menyebutkan 1, kemudian Bimo 2, 4. Lalu Iwang menyebutkan 3, 5, 7. Bimo melanjutkan dengan menyebut 6, 8, 10, 12. Begitu seterusnya. Bilangan ke-2019 yang disebutkan adalah ….
	- [ ] 1990
	- [ ] 1890
	- [ ] 1780
	- [ ] 1680
	- [ ] 1580
14. Andi menemukan suatu permainan yang memiliki 10 pertanyaan di dalamnya. Beberapa pertanyaan hanya dapat dijawab apabila sudah berhasil menyelesaikan salah satu pertanyaan lain. Jika suatu pertanyaan $A$ memiliki syarat $B, C, D$, maka Andi baru dapat menjawab pertanyaan $A$ jika sudah berhasil menyelesaikan salah satu dari $B$, $C$, dan $D$. Syarat ini dituliskan dalam notasi $A: [B, C, D]$.

	Selengkapnya, permainan itu mempunyai syarat sebagai berikut.
	- $1: [2, 3]$
	- $2: [5, 7]$
	- $3: [5, 9]$
	- $4: [7, 8]$
	- $5: [6, 10]$
	- $6: [3, 9]$
	- $7: [10]$
	- $8: [9, 10]$
	- $9: [7]$
	- $10 : []$
	
	Pertanyaan nomor $10$ dapat dijawab tanpa harus menyelesaikan pertanyaan lainnya. Berapakah banyak pertanyaan minimum yang harus dijawab sebelumnya agar Andi dapat menjawab pertanyaan nomor $1$?

Berikut deskripsi untuk soal 16–17.

Terdapat $N$ kota dengan $N$ nama berbeda. Setiap kota memiliki populasi penduduk masing-masing. Pemerintah negara tersebut pusing karena terdapat terlalu banyak kota. Pemerintah tersebut berencana menggabungkan kota-kota tersebut hingga hanya tersisa satu kota. Caranya begini. Selama masih ada 2 kota atau lebih, pemerintah memilih 2 kota sesuka dia, kemudian menggabungkan kedua kota tersebut, Nama kota yang baru tersebut ialah nama salah satu kota dari kedua kota asalnya yang memiliki jumlah penduduk lebih banyak. Apabila jumlah penduduknya sama, namanya boleh yang mana saja.

Tugas Anda pada soal ini ialah menghitung ada berapa nama kota berbeda dari kota terakhir yang mungkin terjadi dengan asumsi pemerintahnya memilih kedua kota tersebut secara acak.

16. Misalkan $N = 8$, dan jumlah penduduk masing-masing kota adalah 2, 50, 24, 21, 1, 9, 15, dan 5 orang. Setelah seluruh kota berhasil digabung menjadi 1 kota, ada berapa nama kota berbeda dari kota yang mungkin?
	- [ ] 12
	- [ ] 509
	- [ ] 5
	- [ ] 7
	- [ ] 180
17. Misalkan $N = 100$, dan tiap kota diberi nomor 1 sampai 100. Jumlah penduduk di kota ke-$i$ adalah $i^2$. Ada berapa nama kota berbeda dari kota yang mungkin?
	- [ ] 121
	- [ ] 509
	- [ ] 55
	- [ ] 97
	- [ ] 180

Perhatikan potongan program di bawah untuk digunakan pada soal nomor 20 dan 21!

```pascal
function mencari(N: integer): integer;
var i, j, z: integer;
begin
	mencari := 0;
	for i := 1 to N do
	begin
		j := 1;
		z := 0;
		
		while (j <= i) do
		begin
			if (i mod j = 0) then inc(z);
			inc(j);
		end;
		if (z mod 2 <> 0) then
			mencari := mencari + 1;
	end;
end;
```

20. Berapakah nilai yang dihasilkan dari pemanggilan `mencari(50)`?
	- [ ] 11
	- [ ] ?
	- [ ] ?
	- [ ] ?
	- [ ] ?
21. Berapakah nilai yang dihasilkan dari pemanggilan `mencari(9000)`?
	- [ ] 151
	- [ ] 103
	- [ ] 94
	- [ ] 86
	- [ ] 35
22. Bila $z$ bilangan bulat positif terkecil yang memberikan sisa 5 jika dibagi dengan 13, dan memberikan sisa 3 jika dibagi dengan 13. Berapa sisa $z$ dibagi dengn 11?
	- [ ] 2
	- [ ] 4
	- [ ] 6
	- [ ] 5
	- [ ] 7
23. Ada berapa himpunan bagian dari $\{1, 2, 3, 4, 5, 6, 7, 8, 9\}$ sedemikian sehingga tidak ada dua anggota yang berurutan?
	
	Misalkan himpunan $\{1, 4, 5\}$ dilarang, karena memiliki dua anggota 4 dan 5 yaitu dua bilangan yang berurutan. Himpunan $\{2, 4, 8\}$ boleh.
	- [ ] 151
	- [ ] 103
	- [ ] 94
	- [ ] 86
	- [ ] 89
20. Nilai dari ekspresi *boolean*
	$$ (\neg A) \vee (B \wedge C) \vee (A \wedge \neg B \wedge C) \vee (A \wedge B) $$
	
	akan selalu berlawanan dengan ekspresi ….
	- [ ] $(\neg (C \vee \neg A)) \wedge \neg B \vee \neg A$
	- [ ] $(A \wedge (B \vee C)) \vee C \vee (\neg A \wedge \neg C)$
	- [ ] $(A \wedge (B \vee C)) \vee C \vee (A \wedge C)$
	- [ ] $\neg B \vee (\neg (A \wedge B \wedge \neg C))$
	- [ ] $\neg (C \vee \wedge A) \wedge \neg B$
