<div align="center">

# 🎓 Sistem Akademik Project 3

**Project 3 · Pemrograman Berbasis Web Lanjutan**

Aplikasi **Sistem Akademik** berbasis **PHP OOP** tanpa framework, dengan CRUD Mahasiswa serta halaman Dosen dan Matakuliah.

![PHP](https://img.shields.io/badge/PHP-8.0%2B-777BB4?logo=php&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-MariaDB-4479A1?logo=mysql&logoColor=white) ![PDO](https://img.shields.io/badge/PDO-database-6C7A89?logo=php&logoColor=white) ![Composer](https://img.shields.io/badge/Composer-PSR--4-885630?logo=composer&logoColor=white) ![License](https://img.shields.io/badge/License-MIT-green.svg) ![Status](https://img.shields.io/badge/status-selesai%20%26%20teruji-brightgreen)

</div>

## 📖 Deskripsi

Menggunakan **namespace** `App\` dan `Inc\` sehingga class tidak saling tabrakan. Alurnya sengaja dibuat polos agar alur OOP + PDO terlihat jelas: `index.php` menerima parameter `?page=`, lalu menyertakan file halaman yang bersangkutan, yang memanggil class model.

## 📸 Tampilan

<table>
 <tr>
 <td width="50%"><img src="docs/screenshots/01-dashboard.png" alt="Dashboard"><br><sub>Dashboard</sub></td>
 <td width="50%"><img src="docs/screenshots/02-mahasiswa.png" alt="Daftar Mahasiswa"><br><sub>Daftar Mahasiswa</sub></td>
 </tr>
 <tr>
 <td width="50%"><img src="docs/screenshots/03-form-input.png" alt="Form Input Mahasiswa"><br><sub>Form Input Mahasiswa</sub></td>
 <td width="50%"><img src="docs/screenshots/04-dosen.png" alt="Daftar Dosen"><br><sub>Daftar Dosen</sub></td>
 </tr>
</table>

## ✨ Fitur

- 📋 Daftar mahasiswa dari tabel `tb_mhsw`
- ➕ Tambah mahasiswa (NIM, nama, alamat)
- ✏️ Ubah & 🗑️ hapus mahasiswa
- 👨‍🏫 Halaman data dosen (`tb_dosen`)
- 📚 Halaman data matakuliah (`tb_matakuliah`)
- 🔗 Routing sederhana lewat `index.php?page=...`
- 🎨 Tampilan sidebar + tabel rapi (aset CSS lokal)

## 🧱 Teknologi

| Lapisan | Teknologi |
| --- | --- |
| Bahasa | PHP 8.0+ (OOP, tanpa framework) |
| Database | MySQL / MariaDB (PDO) |
| Koneksi | `inc/Koneksi.php` |
| Routing | Query string `?page=` |
| Tampilan | HTML + CSS lokal |

## 🏗️ Arsitektur

```mermaid
flowchart TD
 A[Browser] -->|index.php?page=mhsw| B[index.php]
 B -->|include| C[mhsw.php]
 C --> D[App\Mahasiswa]
 D --> E[Koneksi - PDO]
 E --> F[(pbwl_samples_3)]
 C --> G[Browser]
```

## 🚀 Instalasi

1. Pastikan folder ada di `htdocs` XAMPP.
2. Buat database `pbwl_samples_3` lalu import `database.sql`.
3. DSN sudah diarahkan ke `127.0.0.1`, port **3307**, database `pbwl_samples_3`.
4. Buka **http://localhost/pbwl-samples-3/**.

## 🗂️ Struktur

```
pbwl-samples-3/
├── app/
│ ├── Koneksi.php # (project 3: model di app/)
│ └── Mahasiswa.php
├── inc/ # koneksi (project 2 & 3)
├── assets/css/style.css
├── database.sql
├── index.php # router ?page=
├── main.php # dashboard
├── mhsw.php, mhsw_input.php, mhsw_edit.php, mhsw_proses.php
├── dosen.php, matkul.php
└── README.md
```

## 🗄️ Database

Database **`pbwl_samples_3`** di MySQL/MariaDB port **3307** (user `root`, password kosong).

File `database.sql` sudah diimpor. Jika perlu import ulang:

```bash
mysql -h 127.0.0.1 -P 3307 -u root pbwl_samples_3 < database.sql
```

> Database lain di XAMPP (termasuk `dbakademik`) sengaja tidak disentuh.

## ✅ Verifikasi

- `/` → 200
- `/index.php?page=mhsw` → 200
- `/index.php?page=dosen` → 200
- `/index.php?page=matkul` → 200

## 🔗 Tautan

- GitHub: https://github.com/Neuron700/pbwl-samples-3
- Aplikasi: http://localhost/pbwl-samples-3/

## 📄 Lisensi

MIT
