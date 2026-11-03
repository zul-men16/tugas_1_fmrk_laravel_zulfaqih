# laravel-mvc-genre-author

Aplikasi web sederhana berbasis Framework Laravel yang mengimplementasikan arsitektur Model-View-Controller (MVC) untuk menampilkan data Genre dan Author dari array Model ke dalam antarmuka berbasis Bootstrap 5.

Proyek ini dibuat sebagai tugas praktikum Pemrograman PHP / Framework Laravel untuk memahami alur kerja MVC secara mendasar tanpa menggunakan database MySQL.

---

## 🎯 Tujuan Proyek

1. Memahami konsep arsitektur Model-View-Controller (MVC) pada Framework Laravel.
2. Memisahkan logika pengelolaan data (Model), pengendali alur aplikasi (Controller), dan tampilan antarmuka (View).
3. Mengimplementasikan routing Laravel yang menghubungkan URL ke Controller dan View.
4. Menampilkan data array dari Model ke dalam tabel HTML modern dan responsif menggunakan Laravel Blade dan Bootstrap 5.

---

## 📁 Struktur Folder MVC Proyek

```text
laravel-mvc-genre-author/
│
├── app/
│   ├── Http/
│   │   └── Controllers/
│   │       ├── Controller.php
│   │       ├── GenreController.php
│   │       └── AuthorController.php
│   │
│   └── Models/
│       ├── Genre.php
│       └── Author.php
│
├── resources/
│   └── views/
│       ├── layouts/
│       │   └── app.blade.php
│       ├── genres/
│       │   └── index.blade.php
│       ├── authors/
│       │   └── index.blade.php
│       └── home.blade.php
│
├── routes/
│   └── web.php
│
├── .gitignore
├── artisan
├── composer.json
└── README.md
```

### Penjelasan Fungsi File MVC

| File | Komponen | Deskripsi Fungsi |
| :--- | :--- | :--- |
| `app/Models/Genre.php` | Model | Menyimpan array 5 data genre buku dan menyediakan method `getAll()` untuk mengambil seluruh data genre. |
| `app/Models/Author.php` | Model | Menyimpan array 5 data penulis buku dan menyediakan method `getAll()` untuk mengambil seluruh data author. |
| `app/Http/Controllers/GenreController.php` | Controller | Menghubungkan Model Genre dengan View, memanggil data lalu mengirimkannya ke view `genres.index`. |
| `app/Http/Controllers/AuthorController.php` | Controller | Menghubungkan Model Author dengan View, memanggil data lalu mengirimkannya ke view `authors.index`. |
| `resources/views/layouts/app.blade.php` | Layout View | Layout utama yang memuat navbar Bootstrap 5 dan struktur template agar tampilan seluruh halaman konsisten. |
| `resources/views/home.blade.php` | View | Halaman beranda dengan judul Laravel MVC Genre & Author serta tombol navigasi menuju halaman Genre dan Author. |
| `resources/views/genres/index.blade.php` | View | Template Blade untuk menampilkan tabel data Genre (ID dan Nama Genre) secara responsif. |
| `resources/views/authors/index.blade.php` | View | Template Blade untuk menampilkan tabel data Author (ID dan Nama Author) secara responsif. |
| `routes/web.php` | Routing | Mendefinisikan rute `/`, `/genres`, dan `/authors` yang dihubungkan ke Controller yang sesuai. |

---

## 📊 Data Studi Kasus

### 1. Data Genre (`Genre.php`)
| ID | Nama Genre |
| :---: | :--- |
| 1 | Fiction |
| 2 | Romance |
| 3 | Mystery |
| 4 | Science Fiction |
| 5 | Fantasy |

### 2. Data Author (`Author.php`)
| ID | Nama Author |
| :---: | :--- |
| 1 | Andrea Hirata |
| 2 | Tere Liye |
| 3 | Dee Lestari |
| 4 | Pramoedya Ananta Toer |
| 5 | Ahmad Fuadi |

---

## 🚀 Fitur Aplikasi

- **Arsitektur MVC Standar Laravel**: Mengikuti struktur resmi Laravel tanpa modifikasi di luar standar.
- **Routing Laravel**: Rute web terstruktur rapi menghubungkan URL ke masing-masing Controller.
- **Blade Templating**: Menggunakan `@extends`, `@section`, dan `@yield` dengan layout utama tunggal.
- **Desain Modern & Responsif**: Berbasis Bootstrap 5 CDN dan Bootstrap Icons.
- **Tanpa Database**: Data dikelola langsung menggunakan array di dalam class Model.
- **Bebas Komentar**: Seluruh kode program bebas dari komentar sesuai instruksi tugas praktikum.

---

## 💻 Cara Menjalankan Aplikasi

### Prasyarat
- PHP versi 8.2 atau lebih tinggi.
- Composer.

### Langkah Menjalankan:

1. Buka terminal atau Command Prompt pada direktori utama proyek.
2. Jalankan perintah server bawaan Laravel:

```bash
php artisan serve
```

3. Buka browser dan akses alamat berikut:
   - **Halaman Utama (Beranda)**: `http://127.0.0.1:8000/`
   - **Halaman Data Genre**: `http://127.0.0.1:8000/genres`
   - **Halaman Data Author**: `http://127.0.0.1:8000/authors`

---

## 🛠️ Panduan Push ke GitHub

Untuk mengunggah proyek ke repository GitHub:

```bash
git init
git add .
git commit -m "Initial commit - Laravel MVC Genre and Author"
git branch -M main
git remote add origin https://github.com/<username-anda>/laravel-mvc-genre-author.git
git push -u origin main
```
