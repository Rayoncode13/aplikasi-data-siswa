# Proyek CRUD Data Siswa Sederhana

Ini adalah proyek aplikasi web sederhana yang mengimplementasikan fungsionalitas **CRUD (Create, Read, Update, Delete)** untuk manajemen data siswa. Aplikasi ini dibangun menggunakan PHP natif (prosedural) dan Bootstrap 5 untuk tampilan antarmuka.

Proyek ini sangat cocok untuk pemula yang ingin mempelajari dasar-dasar pengembangan web dengan PHP, interaksi dengan database MySQL, dan penggunaan framework CSS seperti Bootstrap.

  
*(Saran: Ganti link di atas dengan screenshot aplikasi Anda untuk membuatnya lebih menarik)*

## 🚀 Fitur Utama

  - **Create:** Menambahkan data siswa baru ke dalam database melalui form.
  - **Read:** Menampilkan semua data siswa yang tersimpan dalam format tabel yang rapi.
  - **Update:** Mengubah atau memperbarui data siswa yang sudah ada.
  - **Delete:** Menghapus data siswa dari database.

## 💻 Teknologi yang Digunakan

  - **Backend:** PHP (Native/Prosedural)
  - **Frontend:** HTML, CSS
  - **Framework CSS:** Bootstrap 5
  - **Database:** MySQL / MariaDB
  - **Web Server:** Apache (biasanya bagian dari XAMPP, LAMP, atau MAMP)

## 📂 Struktur Folder

```
sekolah/
│
├── css/                  # File CSS Bootstrap
│   ├── bootstrap.min.css
│   └── ...
│
├── js/                   # File JavaScript Bootstrap
│   ├── bootstrap.bundle.min.js
│   └── ...
│
├── add-student.php       # Halaman form untuk menambah siswa
├── connection.php        # Script untuk koneksi ke database
├── edit-siswa.php        # Halaman form untuk mengedit data siswa
├── hapus-siswa.php       # Script untuk memproses penghapusan data
├── index.php             # Halaman utama (menampilkan data siswa)
├── save-siswa.php        # Script untuk memproses penyimpanan data baru
└── update-siswa.php      # Script untuk memproses pembaruan data
```

## 🛠️ Instalasi dan Konfigurasi

Ikuti langkah-langkah berikut untuk menjalankan proyek ini di komputer lokal Anda.

### 1\. Prasyarat

Pastikan Anda sudah menginstal software berikut:

  - Web Server seperti XAMPP, LAMP, atau MAMP (yang sudah termasuk Apache, PHP, dan MySQL).

### 2\. Clone Repositori

```bash
git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name
```

### 3\. Setup Database

1.  Buka **phpMyAdmin** (`http://localhost/phpmyadmin`).

2.  Buat database baru dengan nama `db_sekolah` (atau nama lain sesuai keinginan Anda).

3.  Pilih database yang baru dibuat, lalu buka tab **SQL**.

4.  Jalankan query SQL berikut untuk membuat tabel `tb_siswa`:

    ```sql
    CREATE TABLE tb_siswa (
        id INT AUTO_INCREMENT PRIMARY KEY,
        nama VARCHAR(100) NOT NULL,
        nis VARCHAR(20) NOT NULL,
        jurusan VARCHAR(50),
        alamat TEXT,
        tanggal_input TIMESTAMP DEFAULT CURRENT_TIMESTAMP
    );
    ```

### 4\. Konfigurasi Koneksi

1.  Buka file `connection.php`.

2.  Sesuaikan detail koneksi database dengan pengaturan lokal Anda.

    ```php
    <?php
    $host = "localhost";    // Biasanya tetap "localhost"
    $user = "root";         // User default XAMPP
    $pass = "";             // Password default XAMPP kosong
    $db   = "db_sekolah";   // Nama database yang Anda buat

    $conn = mysqli_connect($host, $user, $pass, $db);

    if (!$conn) {
        die("Koneksi Gagal: " . mysqli_connect_error());
    }
    ?>
    ```

### 5\. Jalankan Aplikasi

1.  Pindahkan folder proyek `sekolah` ke dalam direktori `htdocs` (jika menggunakan XAMPP) atau `www` (jika menggunakan WAMP/LAMP).
2.  Buka browser Anda dan akses `http://localhost/sekolah`.

-----

