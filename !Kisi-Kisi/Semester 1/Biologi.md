# 1—Keanekaragaman Hayati {#bab-1}

<style>
.markdown-document img{background:white;}
figure{
background:var(--background-accent);
border-radius:8px;
padding:4px;
float:right;
clear:right;
display:flex;
flex-direction:column;
gap:4px;
margin:0;
margin-left:1em;
margin-block:.2em;
}
figure img{
border-radius:4px;
}
figure figcaption{
font-size:small;
line-height:1;
text-align:center;
}
</style>

- **(1<sub>MJD</sub>)** *Pembagian fauna di Indonesia.*
	- **Asiatis**: Sumatra, Kalimantan, Jawa, Bali.
		- *Karakteristik*
			- Mamalia besar.
			- Banyak jenis kera dan ikan air tawar.
			- Banyak jenis reptil.
			- Hutan hujan tropis.
			- Hutan bakau/mangrove.
		- *Contoh*
			- **Harimau**.
			- **Gajah**.
			- **Badak**.
			- Beruang madu.
			- Macan tutul.
			- Orangutan.
			- **Kera/monyet**.
			- Burung merak.
			- Ikan mujair.
			- Ikan arwana.
			- **Pohon meranti**.
			- **Pohon jati**.
			- Pohon mahoni.
			- *Rafflesia arnoldii*.
	- **Peralihan**: Sulawesi, Lombok, Nusa Tenggara, Maluku. <figure style="width:30%"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQBoWskJCmcVyiLWUUHya45KA4pe3e7vTtrRdMBh2aJ3-aTIZ1PmFeJhpTg8WmOZM0q_V0Lry7DUB0EVegr-LPmhmPsjYV3iBlQY8DVEFQ&s=10"><figcaption>Anoa</figcaption></figure> <figure style="width:30%"><img src="https://upload.wikimedia.org/wikipedia/id/thumb/d/d0/Kuskus_tutul.jpg/250px-Kuskus_tutul.jpg"><figcaption>Kuskus</figcaption></figure> <figure style="width:30%"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRr5g4YmLA0ow-u5joaZS7f9gU8C3svj0h_e271k--N9se4New_er-6C0kmq7VYMeG3DODscB5xSr-BHnD3JdWn_m_TwMbZN7YBYURxS0M&s=10"><figcaption>Tarsius</figcaption></figure>
		- *Karakteristik*
			- Pertengahan antara Asiatis dan Australis.
			- Ukuran tanaman tidak terlalu tinggi.
			- Vegetasi **sabana** dan **stepa**.
			- Hewannya **endemik**.
		- *Contoh*
			- Cengkeh.
			- Eboni.
			- Cendana.
			- Anggrek.
			- Kayu manis.
			- Akasia.
			- Komodo.
			- Babi rusa.
			- Anoa.
			- Kuskus.
			- Tarsius.
	- **Australis**: Papua. <figure style="width:30%"><img src="https://upload.wikimedia.org/wikipedia/commons/6/64/Lesser_Bird_of_Paradise.jpg"><figcaption>Cendrawasih</figcaption></figure> <figure style="width:30%"><img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhXV5lNOo_NdSnCPfOye3GAafqen7RB5Tj2ll43gq9oTXCHpt-LfwOu0tzAwSthcpRgYpxnsaQX1dn0FXMnYI-eM_kx_LqGr31FF5TggvvnS4safIl8i4ESYV54Z7Ura8IoHdG7shx8dtF2/s600/cassowary+beach.jpg"><figcaption>Kasuari</figcaption></figure> <figure style="width:30%"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT5DiQ2o4AeXmONDOsaWUDpSGV3F7ozjCTNkupR8PvrbX2lakgN0OgpJxseKNpK9ZijE1Q1aRrj_E6xL5eP7ofDGyYDICH8TPNKfPMaIw&s=10"><figcaption>Walabi</figcaption></figure>
		- *Karakteristik*
			- Sebagian besar hutan hujan tropis.
			- Ada tundra alpin di puncak Gunung Jayawijaya.
			- Sabana.
			- Padang rumput.
			- Berdaun sklerofilus (*sclerophyllus*), keras dan kecil, karena kering.
			- Hewan berkantung.
			- Mamalia kecil.
			- Burung-burung endemik.
			- Burung berwarna cerah.
		- *Contoh*
			- Kanguru.
			- Burung cendrawasih.
			- Walabi.
			- Burung kakatua raja.
- **(2)** *Kenanekaragaman hayati tingkat gen.*
	- Pada ragaman tingkat gen, genetiknyalah yang berbeda, taksonnya masih sama.
	- Contohnya **mangga harum manis** dan **mangga kuini**. Keduanya masih mangga: *Mangifera indica*.
	- Contoh lainnya.
		- **Durian** musang king, petruk, merah.
		- **Rambutan** binjai, rapiah, nona.
		- Perbedaan **warna** pada rambut hewan: kucing, anjing.
		- Perbedaan warna mata, kulit, tinggi badan, golongan darah pada manusia.
- **(3<sub>MJD</sub>)** *Hewan akuatik dan tempat hidupnya.*
- **(4<sub>BS</sub>)** *Kunci determinasi.*
	- Digunakan untuk mengelompokkan makluk hidup (**taksonomi**), melalui banyak *if-else statements*.
	- Setiap **nomor** ada **dua** pasang pernyataan yang saling **berlawanan**.
	- Jika suatu pernyataan terpenuhi, maka lanjut ke nomor yang diberikan, atau berakhir di situ.
	- Contoh yang *sangat* sederhana:
		> 1. a. Hewan bertulang belakang **(2)**
		> 	b. Hewan tidak bertulang belakang **(3)**
		> 2. a. Alat gerak berupa sirip **(Ikan)**
		> 	b. Alat gerak bukan sirip **(4)**
		> 3. a. Tubuh tidak berbuku-buku **(Bekicot)**
		> 	b. Tubuh berbuku-buku **(5)**
		> 4. a. Menyusui **(Kelinci)**
		> 	b. Tidak menyusui **(Ayam)**
		> 5. a. Mengalami metamorfosis **(Kupu-kupu)**
		> 	b. Tidak mengalami metamorfosis **(Laba-laba)**
- **(5)** *Persamaan dan perbedaan tingkatan taksonomi hewan: pada ordo, kelas, famili, dan lain-lain.*
- **(6<sub>BS</sub>)** *Penulisan nama ilmiah (binomial nomenklatur).*
	- Terdiri dari **2 kata**: genus dan spesies.
	- *2 kata: <u>**bi**</u>nomial*
	- Genus diawali **huruf kapital**.
	- Spesies diawali **huruf kecil**.
	- Nama ilmiah ini wajib dicetak miring (atau digarisbawahi).
	- Inisial penemu pertama ditulis di akhir dan **tidak** dicetak miring. Nama yang dipakai adalah **nama belakang** penemu. Misalnya Carolus Linnaeus menjadi L..
	- Genus **boleh** disingkat.
	- Contoh yang **tepat**:
		- *Homo sapiens*.
		- *Panthera tigris*.
		- *Oryza sativa*.
		- *Felis catus*.
		- *H. sapiens*.
		- *S. cerevisiae*.
		- <u>Rhizopus oryzae</u>.
		- *Musa paradisiaca* L., pemberi nama ilmiahnya adalah Carolus <u>**L**</u>innaeus.
	- Contoh yang **tidak** tepat:
		- *homo sapiens*.
		- *Escherechia Coli*.
		- Saccharomyces cerevisiae.
- **(7)** *Kelompok hewan yang memiliki tingkatan takson yang sama.*
- **(8)** *Bagaimana Taman Nasional dapat membantu pelestarian makhluk hidup?*
	- Menjadi tempat konservasi *in situ*, yaitu pada habitat alami mereka.
	- Menjaga flora dan fauna endemik dan yang hampir punah.
	- Minim aktivitas manusia, sehingga flora dan fauna terlindungi.
	- Menjadi tempat penelitian.
- **(9)** *Tumbuhan yang dipakai untuk sandang, beserta nama Latin.*
	| Bahan Baku | Nama Ilmiah           |
	| ---------- | --------------------- |
	| Kapas      | *Gossypium hirsutum*  |
	| Rami       | *Boehmeria nivea*     |
	| Nanas      | *Ananas cosmosus*     |
	| Flax/linen | *Linum usitatissimum* |
- **(10)** *Tindakan melestarikan terumbu karang.*
	- Menghindari penangkapan ikan dengan bom/racun.
	- Menjaga kebersihan air.
	- Penanaman karang.

# 2—Virus {#bab-2}

- **(11)** *Virus RNA dan DNA.*
- **(12<sub>BS</sub>)** *HIV: RNA atau DNA, menyerang apa, reaksi imun tubuh, dan grafik.*
	- HIV (*Human immunodeficiency virus*) adalah virus RNA.
	- HIV menyerang sistem kekebalan tubuh manusia (limfoid).
		- Khususnya sel darah putih CD4.
	- Nama penyakitnya adalah AIDS (*Acquired immunodeficiency syndrome*).
	- Grafik perjalanan infeksi HIV. ![Time Course](https://upload.wikimedia.org/wikipedia/commons/thumb/0/09/HIV-timecourse_simple.svg/1024px-HIV-timecourse_simple.svg.png)
		- Pada minggu ke-3 sampai ke-9 setelah infeksi, terjadi lonjakan pada jumlah HIV. Fase ini disebut sebagai **fase infeksi akut**.
			- Virus bereplikasi sangat cepat.
			- Oleh karena itu, sel CD4 turun **drastis**.
			- Muncul gejala awal seperti flu.
				- Demam.
				- Sakit tenggorokan.
				- Nyeri otot.
				- Pembengkakan kelenjar getah bening.
				- Ruam kulit.
				- Sakit kepala.
				- Kelelahan ekstrem.
			- Tubuh akan memproduksi banyak antibodi.
		- Setelah itu, terjadi masa **laten klinis**, selama 5–10 tahun.
			- Hampir **tidak** ada gejala.
			- HIV bereplikasi perlahan demi perlahan.
			- Karena itu, CD4 juga perlahan-lahan menurun.
			- Virus mulai merusak sistem imun secara kronis.
		- Lalu fase terakhir, **fase AIDS**.
			- Pada fase ini, kadar CD4 kurang dari $\pu{200 sel/mm3}$.
			- Sistem imun **rusak** sepenuhnya.
			- Infeksi ringan sekalipun tubuh tak mampu lagi.
			- Karena itu, banyak infeksi yang biasa bisa menjadi mematikan.
			- Penyebab kematian sebenarnya **bukanlah** AIDS-nya, namun infeksi yang memanfaatkan kelemahan imun yang disebabkan oleh HIV.
				- Pneumonia.
				- Tuberkulosis.
				- Meningitis.
				- Sepsis.
- **(13<sub>BS</sub>)** *Grafik dosis vaksin.*
	- Menambah dosis meningkatkan imun tubuh.
	- *Booster* dapat mempengaruhi memori imun (lebih baik).
- **(14<sub>MJD</sub>)** *Struktur virus.*
	- Struktur *Orthocoronavirinae*. ![Struktur Sars-CoV-2](https://www.biophysics.org/Portals/0/BPSAssets/Blog/2020/CaseFigure_Coronavirus%20Structure%20and%20Protein%20Visualization-2.jpg?ver=2020-05-11-195753-593)
		- **Spike**.
			- Mengikat reseptor sel inang ACE2.
			- Memicu fusi membran.
			- Target utama antibodi.
		- **Nukleokapsid**.
			- Membungkus RNA virus.
			- Membantu replikasi.
			- Mengatur transkripsi RNA selama infeksi.
		- **Membran**.
			- Menentukan bentuk virus.
			- Rangka luar.
		- **Envelop**.
			- Pembentukan selubung virus.
	- Struktur bakteriofag. ![Sturktur Bakteriofag](https://awsimages.detik.net.id/community/media/visual/2022/11/22/modul-pembelajaran-biologi-kemendikbud.jpeg?w=600&q=90)
- **(15<sub>MJD</sub>, 16<sub>BS</sub>)** *Reproduksi virus: tahapan, litik dan lisogenik.*
	- Reproduksi Bakteriofag. ![Reproduksi Bakteriofag](https://media.geeksforgeeks.org/wp-content/uploads/20220623130852/C5.png)
		1. **Adsorbsi**, fag menempel pada inang.
		2. **Penetrasi**, fag memasukkan materi genetiknya.
		3. **Litik**:
			1. **Sintesis**, materi genetik fag mengambil alih inang. Alih-alih membuat salinan genetik sendiri, inang akan menyalin genetik fag.
			2. **Lisis**, enzim **lisozim** yang dibuat virus akan merusak dinding inang. Sehingga fag baru dapat keluar.
		4. **Lisogenik**:
			1. Genetik fag bergabung dengan genetik inang, menjadi **profag**.
			2. Ketika inang membelah diri, gen fag ikut bereplikasi ke sel-sel inang berikutnya.
			3. Pada kondisi tertentu, profag dapat terpisah dari gen inang dan menjadi aktif. Dan memulai siklus litik.
- **(17)** *Karakteristik virus.*
	- Virus **bukanlah** sel, sehingga disebut **aseluler**.
	- Hanya dapat berkembang biak di dalam sel inang yang hidup.
	- Ukuran yang **kecil** *banget*, $\pu{20 nm}$ sampai $\pu{300 nm}$.
	- Tidak punya metabolisme sendiri.
	- Hanya memiliki **satu** jenis materi genetik, antara DNA atau RNA.
	- Seperti benda mati di luar sel inang, seperti makhluk hidup di dalam sel inang.
- **(18)** *Grafik terkait gejala penyakit campak.*
	- Gejala awal (1–4 hari setelah infeksi).
		- Demam tinggi, $(> \pu{40 \celsius})$.
		- Batuk kering.
		- Pilek.
		- Mata merah, berair, sensitif terhadap cahaya.
		- Lemas.
		- Sakit tenggorokan.
	- Gejala lanjut.
		- Bintik putih keabuan (1–2 hari).
		- Ruam merah (3–5 hari).
- **(19<sub>BS</sub>)** *Penemu virus; poliomielitis menyerang apa; apakah gondok disebabkan virus; virus merupakan parasit intraseluler obligat.*
	- *Penemu virus*.
		- **Adolf Mayer** (1883) menemukan penyakit mosaik pada tembakau. Namun belum menyebut itu sebagai virus, hanya bakteri yang sangat kecil.
		- **Dmitri Ivanovsky** (1892) mendapati agen infeksi mosaik tersebut menembus saringan bakteri, berarti ukurannya lebih kecil dari bakteri. Sehingga ia berkesimpulan itu adalah partikel baru yang sangat kecil.
		- **Martinus Beijerinck** (1898) melanjutkan penelitian Ivanovsky dan berhasil **mengisolasi** agen infeksi mosaik tembakau. Ia menyebutnya sebagai *contagium vivum fluidium* (cairan hidup menular) karena agen infeksi tersebut dapat berkembang biak, tapi **tak bisa tumbuh pada cawan petri**.
		- **Wendell Stanley** (1935) berhasil mengkristalkan virus mosaik tembakau (TMV). Berarti virus memiliki sifat benda mati, yaitu dapat dikristalkan. Tidak selayaknya sel hidup yang tidak dapat dikristalkan.
	- Polio atau *poliomielitis* menyerang **sistem saraf pusat**, terutama yang mengontrol gerak motorik.
	- Gondok disebabkan oleh virus *Paramyxovirus*.
	- Virus adalah parasit intraseluler obligat ✅.
- **(20<sub>MJD</sub>)** *Jodohkan virus dari cacar, campak, sapi gila, rabies, tumor ayam, penyakit mulut dan kuku.*
	- Cacar — *Poxvirus*.
	- Campak — *Paramyxoviridae*.
	- Sapi gila — Prion, bukan virus.
	- Rabies — *Rhabdoviridae*.
	- Tumor ayam — *Rous sarcoma virus*.
	- PMK — *Aphthovirus*.

# 3—Bioteknologi {#bab-3}

- **(21)** *Kultur jaringan: prinsip dan tekniknya, modern atau konvensional.*
	- Menggunakan prinsip **totipotensi sel**.
	- Alurnya adalah
		- eksplan;
		- sterilisasi;
		- media;
		- kalus;
		- planlet; dan
		- aklimatisasi.
	- Termasuk *in vitro* (“pada tabung”).
	- Termasuk bioteknologi **modern**.
- **(22)** *Alasan penggunaan makhluk hidup pada bioteknologi.*
	- Mudah diperoleh dan dikembangbiakkan.
	- Memiliki sifat yang bisa diubah dengan rekayasa genetika.
	- Mikroorganisme berkembang biak secara cepat dan banyak.
	- Menambah nilai gizi dan rasa pada makanan/minuman.
- **(23<sub>BS</sub>)** *Produk bioteknologi: bahan baku dan mikroorganisme.*
	- B.: bakteri.
	- J.: jamur.
	- Keju — B. *Lactobacillus bulgaricus*; B. *Streptococcus thermophilus*.
	- Yogurt — B. *Lactobacillus bulgarocus*; B. *Streptococcus thermophilus*.
	- Roti — J. *Saccharomyces cerevisiae*.
	- Bir — J. *Saccharomyces ccerevisiae*.
	- Tempe — J. *Rhizopus oryzae*.
	- Kecap — J. *Aspergillus wentii*.
	- Cuka — B. *Acetobacter aceti*.
	- Nata de coco — B. *Acetobacter xylinum*.
	- Oncom — J. *Neurospora sitophila*; J. *Rhizopus oligosporus*.
	- Tapai — J. *Aspergillus sp.*; J. *Saccharomyces cerevisiae*.
	- Kimchi — B. *Lactobacillus kimchii*.
- **(24<sub>MJD</sub>)** *Mikroorganisme pada PST, pembuatan antibiotik, pembasmi hama (biopestisida), pengekstrak biji tembaga, bioremediasi.*
	- Mikroorganisme pada protein sel tunggal (PST).
		- *Spirulina sp.*.
		- *Chlorella sp.*.
		- *Scenedesmus acutus*.
		- *Saccharomyces cerevisiae*.
		- *Candida utilis*.
		- *Fusarium graminearum*.
		- *Bacillus sp.*.
	- Antibiotik.
		- *Penicillum*, penghasil penisilin.
		- *Cephalosporium*, penghasil sefalosporin.
- **(25)** *Tahapan kloning.*
	- *Domba dolly, transfer inti.*
	- Ambil sel **ovum** dari betina.
	- Ambil sel **tubuh**.
	- **Buang** inti sel ovum $(n)$.
	- **Pindahkan** inti sel tubuh $(2n)$ ke dalam ovum, menggunakan sengatan listrik.
	- Stimulasi pembelahan, memberi rangsangan pada sel ovum untuk memicu pertumbuhan.
	- Embrio dikultur di laboratorium hingga tahap tertentu.
	- Lalu embrio dipindakan ke rahim induk.
	- Maka akan dilahirkan domba yang sama dengan domba yang diambil **sel tubuh**nya.
- **(26<sub>BS</sub>)** *Membaca data kloning.*
	- Individu hasil kloning identik dengan yang diambil sel tubuhnya.
	- Umur individu baru tidak lama, karena sel yang dipakai *technically* sudah berumur (dari sel donor).
- **(27<sub>MJD</sub>)** *Menjodohkan gambar eksplan, kalus, planlet, dan aklimatisasi.*
	- Eksplan.  
	  Bagian manapun dari tumbuhan yang masih aktif membelah.
	- Kalus.  
	  ![Kalus](https://upload.wikimedia.org/wikipedia/commons/thumb/1/18/Callus1.jpg/500px-Callus1.jpg)
	- Planlet.  
	  ![Planlet](https://www.kenhose.com/images/product%20planlet1.jpg)
	- Aklimatisasi.  
	  Penyesuaian tanaman pada lingkungan baru,  
	  ![Aklimatisasi](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQy8srThdh_vBW9tgkuuwfbO3SZyy3cPF_XqA&s)
- **(28<sub>BS</sub>)** *Dampak: supergulma, kloning, bioinsektisida. Beda tempe dan oncom.*
	- Supergulma (gulma liar) muncul akibat rekayasa genetika.
	- Kloning menimbulkan kontroversi etis.
	- Bioinsektisida tidak memiliki dampak buruk pada lingkungan.
	- Tetapi bioinsektisida dapat memengaruhi organisme nontarget.
	- Tempe menggunakan *Rhizopus* sedangkan oncom menggunakan *Neurospora*.
- **(29)** *Karakteristik teknik kultur jaringan.*
	- Menggunakan kondisi steril.
	- Mengandalkan totipotensi.
	- Menghasilkan tanaman yang banyak dan identik.
- **(30<sub>MJD</sub>)** *Fungsi enzim ligase dan restriksi. E. coli sebagai sel wadah dan plasmid.*<sup>Hal. 185–186</sup>
	- Enzim ligase — menyambung dua molekul DNA yang putus, dengan membentuk ikatan fosfodiester.
	- Enzim restriksi — memotong DNA pada lokasi spesifik.
	- *E. coli* banyak dipakai sebagai vektor pada rekayasa genetika. Gen-gen yang diinginkan disisipkan pada *E. coli*. *E. coli* dipilih karena pertumbuhannya yang cepat dan mudah.
	- Plasmid adalah molekul DNA kecil yang terpisah dari kromosom bakteri. Plasmid ini dipakai untuk menyisipkan gen yang diinginkan untuk diperbanyak. Contohnya insulin.