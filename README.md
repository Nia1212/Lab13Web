| Nama          | Nia Dwi Rahayu |
|-------------- | ---------------|
| NIM           | 312010298      |
| Kelas         | TI.20.A2       |
| Matkul        | Pemograman web |

# Pratikum 13 : Framework Lanjutan (Modul Login)

## Langkah-langkah Praktikum

### 1. Membuat Model User

Selanjutnya adalah membuat Model untuk memproses data Login. Buat file baru pada
direktori app/Models dengan nama UserModel.php

![ss1](img/ss1.png)

### 2. Membuat Controller User

Buat Controller baru dengan nama User.php pada direktori app/Controllers.
Kemudian tambahkan method index() untuk menampilkan daftar user, dan method
login() untuk proses login.

![ss2](img/ss2.png)

### 3. Membuat View Login

Buat direktori baru dengan nama user pada direktori app/views, kemudian buat file
baru dengan nama login.php.

![ss3](img/ss3.png)

### 4. Membuat Database Seeder

Database seeder digunakan untuk membuat data dummy. Untuk keperluan ujicoba modul
login, kita perlu memasukkan data user dan password kedaalam database. Untuk itu buat
database seeder untuk tabel user. Buka CLI, kemudian tulis perintah berikut:

        php spark make:seeder UserSeeder

![ss4](img/ss4.png)

### Uji Coba Login
Selanjutnya buka url http://localhost:8080/user/login seperti berikut:

![ujicoba1](img/ujicoba1.png)

### 5. Menambahkan Auth Filter
Selanjutnya membuat filer untuk halaman admin. Buat file baru dengan nama Auth.php
pada direktori app/Filters.

![ss5](img/ss5.png)

Selanjutnya buka file app/Config/Filters.php tambahkan kode berikut:
        'auth' => App\Filters\Auth::class

![ss6](img/ss6.png)

Selanjutnya buka file app/Config/Routes.php dan sesuaikan kodenya.

![ss7](img/ss7.png)

### Pertanyaan dan Tugas
Selesaikan programnya sesuai Langkah-langkah yang ada. Anda boleh melakukan improvisasi.

Membuat Tombol Home pada bagian login
pada bagian views\user\login.php tembahkan tombol untuk kembali ketampilan awal.

![ss8](img/ss8.png)

Tampilan

![ss10](img/ss10.png)

### Membuat Tombol Logout
Memberikan tombol logout pada bagian admin

![ss11](img/ss11.png)

Tampilan

![ss12](img/ss12.png)