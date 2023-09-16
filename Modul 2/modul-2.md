Nama: Irfan Hanif Habibi
NIM: 215150701111025

## MongoDB Compass

> Penyambungan koneksi ke MongoDB menggunakan connection string
> ![](./Dokumentasi/pi_1_1.png)

> Pembuatan database "bookstore" dengan collection "books".
> ![](./Dokumentasi/pi_1_2.png)

> Menambahkan data buku dengan operasi insert dokumen.
> ![](./Dokumentasi/pi_1_3.png)

> Menambahkan data buku kedua dengan operasi insert dokumen yang sama.
> ![](./Dokumentasi/pi_1_4.png)

> Melakukan pencarian buku dengan author "Osamu Dazai".
> ![](./Dokumentasi/pi_1_5.png)

> Mengubah properti "summary" pada buku "No Longer Human" dengan melakukan operasi update dokumen.
> ![](./Dokumentasi/pi_1_6.png)

> Menghapus buku "I Am a Cat" dengan melakukan operasi delete dokumen.
> ![](./Dokumentasi/pi_1_7.png)

## MongoDB Shell

> Penyambungan koneksi ke MongoDB Server dengan menggunakan perintah `mongosh` dalam CMD.
> ![](./Dokumentasi/pi_2_1.png)

> Pengecekan daftar database dalam server mongoDB dengan perintah `show dbs`.
> ![](./Dokumentasi/pi_2_2.png)

> Pindahkan terminal ke dalam database `bookstore` dengan perintah `use bookstore`.
> ![](./Dokumentasi/pi_2_2_2.png)

> Mengecek daftar collection yang ada dalam database dengan perintah `show collections` .
> ![](./Dokumentasi/pi_2_2_3.png)

> Menambahkan buku "Overlord I" ke dalam collection `books` dengan perintah `db.books.insertOne(<data>)`.
> ![](./Dokumentasi/pi_2_3.png)

> Menambahkan buku "The Setting Sun" dan "Hujan" ke dalam collection `books` dengan perintah `db.books.insertMany(<data>)`.
> ![](./Dokumentasi/pi_2_4.png)

> Pencarian semua buku dalam collection `books` dengan perintah `db.books.find()`.
> ![](./Dokumentasi/pi_2_5.png)

> Pencarian buku dengan author "Osamu Dazai" dalam collection `books` dengan perintah `db.books.find(<filter>)`.
> ![](./Dokumentasi/pi_2_6.png)

> Melakukan perubahan properti `summary` pada buku "Hujan" dalam collection `books` dengan perintah `db.books.UpdateOne(<filter>, {$set: {<data>}})`.
> ![](./Dokumentasi/pi_2_7.png)

> Melakukan perubahan properti `publisher` pada buku-buku dengan author "Osamu Dazai" dalam collection `books` dengan perintah `db.books.UpdateMany(<filter>, {$set: {<data>}})`.
> ![](./Dokumentasi/pi_2_8.png)

> Penghapusan buku berjudul "Overlord I" dalam collection `books` dengan perintah `db.books.deleteOne(<argumen>)`.
> ![](./Dokumentasi/pi_2_9.png)

> Penghapusan buku dengan author "Osamu Dazai" dalam collection `books` dengan perintah `db.books.deleteMany(<argumen>)`.
> ![](./Dokumentasi/pi_2_10.png)
