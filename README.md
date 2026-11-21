# Project 3 — Sistem Akademik (PHP OOP, Namespace)

Aplikasi Sistem Akademik PHP OOP menggunakan **namespace** (`App\`, `Inc\`).

## Fitur
- CRUD data mahasiswa
- Tampil data dosen dan matakuliah

## Struktur
- `inc/Koneksi.php` — koneksi PDO dalam namespace `Inc`
- `app/Mahasiswa.php` — model dalam namespace `App`
- `database.sql` — skema `tb_mhsw`, `tb_dosen`, `tb_matakuliah`
- `index.php` — halaman utama + router `?hal=...`

## Instalasi
1. Letakkan folder ini di `htdocs` XAMPP.
2. Buat database `pbwl_samples_3`, lalu import `database.sql`.
3. Koneksi sudah diatur ke `127.0.0.1`, port **3307**, user `root`, password kosong, database `pbwl_samples_3`.
4. Buka `http://localhost/pbwl-samples-3/`.
