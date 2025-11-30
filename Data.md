Buka tautan CBT masing-masing, misalkan <https://cbt-man1pekanbaru.sch.id>.

Gunakan peramban Chrome (atau berbasis Chromium serupa).

Pertama-tama, buka DevTools dengan *shortcut* `F12`.

Lalu cari *tab* **Application**. Jika tidak ketemu, coba klik “»”.

![Contoh Tampilan DevTools](https://developer.chrome.com/static/docs/devtools/overview/image/elements-panel-546127ed29eac_856.png)

Berikut tampilan *tab* **Application**.

![Tampilan Tab Application](https://developer.chrome.com/static/docs/devtools/overview/image/the-application-panel-th-c4e7482ef8e4c_856.png)

Lalu klik **Local storage**.

![Tampilan Local Storage](https://developer.chrome.com/static/docs/devtools/storage/localstorage/image/the-key-value-pairs-yout-49ffa01e91c7d_856.png)

Jika belum ada, tambahkan data:

| Key            | Value                                                                                                                                                   |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `token`        | `eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6IiIsImhha0Frc2VzIjoiYWRtaW4iLCJpYXQiOjIwMDAwMDAwMDB9.B5q3v5hEx20iRWmf50SpCrNUucKBIauZ8zGv9jKWLRE` |
| `202412-token` | `eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6IiIsImhha0Frc2VzIjoiYWRtaW4iLCJpYXQiOjIwMDAwMDAwMDB9.B5q3v5hEx20iRWmf50SpCrNUucKBIauZ8zGv9jKWLRE` |

Jika di-*decode*, token tersebut bermakna:

```json
{
  "username": "",
  "hakAkses": "admin",
  "iat": 2000000000
}
```

Ya, *developer*-nya dungu sekali jika membolehkan pengguna untuk melakukan ini.

Setelah itu, pergi ke tautan <https://cbt-man1pekanbaru.sch.id/#/admin/database>.

Pilih ujian yang ingin dibuka dengan mengeklik ikon orang di paling kanan (biru muda).

![Tampilan Database CBT](https://res.cloudinary.com/dhrdz68re/image/upload/v1764417968/enotes/how-to-break-bimasoft-cbt/tampilan_database_cbt.png)

Berikut tampilan data siswa.

![Tampilan Data Siswa CBT](https://res.cloudinary.com/dhrdz68re/image/upload/v1764418334/enotes/how-to-break-bimasoft-cbt/tampilan_data_siswa_cbt.png)

Sekian untuk mengecek nilai.

---

Untuk melihat soal, kembali ke tampilan Database. Klik ikon koran (warna kuning).