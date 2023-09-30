# Modul 4 (Basic Routing & Migration)

Nama: Irfan Hanif Habibi <br>
NIM: 215150701111025

## Basic Routing

### GET
Menambahkan endpoint dengan method GET pada aplikasi dengan menambahkan baris berikut pada file `web.php`:
```
$router->get('/get', function() {
    return 'GET';
});
```
> ![](./Dokumentasi/pi_1_1.PNG)

Pengaksesan endpoint yang telah dibuat dengan menggunakan browser.
> ![](./Dokumentasi/pi_1_1_2.PNG)

### POST, PUT, PATCH, DELETE, dan OPTIONS
Menambahkan endpoint-endpoint lain dengan method POST, PUT, PATCH, DELETE, dan OPTIONS pada aplikasi dengan menambahkan baris berikut pada file `web.php`:
```
$router->post('/post', function () {
    return 'POST';
});

$router->put('/put', function () {
    return 'PUT';
});

$router->patch('/patch', function () {
    return 'PATCH';
});

$router->delete('/delete', function () {
    return 'DELETE';
});

$router->options('/options', function () {
    return 'OPTIONS';
});
```
> ![](./Dokumentasi/pi_1_2.PNG)

### Instal Ektensi Thunder Client pada VS Code
Penginstalan ekstensi dengan membuka panel extensions lalu mencari Thunder Client dan logonya akan ditampilkan pada activity bar VS Code.
> ![](./Dokumentasi/pi_1_2_a_b.PNG)

Pembuatan request baru dengan menekan "New Request" pada ekstensi dan memasukkan method dan URL API yang ingin kita tes.
> ![](./Dokumentasi/pi_1_2_c.PNG)
> ![](./Dokumentasi/pi_1_2_d.PNG)

Pengaksesan beberapa URL dan method yang telah kita buat sebelumnya.
1. POST
	> ![](./Dokumentasi/pi_1_2_e_1.PNG)
2. PUT
	> ![](./Dokumentasi/pi_1_2_e_2.PNG)
3. PATCH
	> ![](./Dokumentasi/pi_1_2_e_3.PNG)
4. DELETE
	> ![](./Dokumentasi/pi_1_2_e_4.PNG)
5. OPTIONS
	> ![](./Dokumentasi/pi_1_2_e_5.PNG)
## Migrasi Database

Memastikan server database aktif kemudian sudah membuat database dengan nama `lumenapi`.
> ![](./Dokumentasi/pi_1_3_a.PNG)

Mengubah beberapa konfigurasi database pada file .env menjadi seperti ini:
```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=lumenapi
DB_USERNAME=root
DB_PASSWORD=
```
> ![](./Dokumentasi/pi_1_3_b.PNG)

Menghidupkan kembali beberapa library bawaan dari lumen dengan membuka file app.php pada folder
bootstrap dan mengganti segmen kode menjadi berikut:
```
$app->withFacades();

$app->withEloquent();
```
> ![](./Dokumentasi/pi_1_3_c.PNG)

Menjalankan command berikut ini untuk pembuatan file migrasi:
```
php artisan make:migration create_users_table 
php artisan make:migration create_products_table
```
> ![](./Dokumentasi/pi_1_3_d.PNG)

Mengubah fungsi `up` pada file migrasi `create_users_table` dengan kode berikut:
```
public function up(): void
    {
        Schema::create('users', function (Blueprint $table) {
            $table->id();
            $table->timestamps();
            $table->string('name');
            $table->string('email');
            $table->string('password');
        });
    }
```
> ![](./Dokumentasi/pi_1_3_e.PNG)

Mengubah fungsi `up` pada file migrasi `create_products_table` dengan kode berikut:
```
public function up(): void
    {
        Schema::create('products', function (Blueprint $table) {
            $table->id();
            $table->timestamps();
            $table->string('name');
            $table->integer('category_id');
            $table->string('slug');
            $table->integer('price');
            $table->integer('weight');
            $table->text('description');
        });
    }
```
> ![](./Dokumentasi/pi_1_3_f.PNG)

Menjalankan command berikut untuk melakukan migrasi database berdasarkan file migrasi `create_users_table.php` dan `create_products_table.php` yang telah dibuat sebelumnya:
```
php artisan migrate
```
> ![](./Dokumentasi/pi_1_3_g.PNG)
