# UTS Pemrograman Web - Bexa Studios Catalog

## 1. Identitas
- **Nama:** Farrel Andhika Pratama
- **NIM:** 025A00200008
- **Kelas:** [A2-3B]

## 2. Deskripsi Singkat Tema
Proyek ini adalah Website Profil & Katalog Dinamis untuk UMKM Bexa Studios. Website ini menampilkan informasi profil studio beserta katalog paket layanan fotografi (seperti Graduation, Pre-wedding, dan Wedding) yang dirender secara dinamis menggunakan array multidimensi pada PHP.

## 3. Cara Menjalankan di Localhost
1. Clone repositori ini atau unduh dalam bentuk ZIP.
2. Ekstrak folder proyek ke dalam direktori server lokal (misalnya `www` pada Laragon atau `htdocs` pada XAMPP).
3. Pastikan web server (Apache/Nginx) sudah berjalan.
4. Buka browser dan akses URL: `http://localhost/uts-pemweb-025A00200008` (sesuaikan dengan nama folder proyek).

## 4. Daftar Fitur & Logika Penanganan
- **Render Katalog Dinamis:** Menampilkan daftar paket layanan studio. Ditangani di `katalog.php` dengan perulangan `foreach`.
- **Status Tutup/Buka Studio:** Menampilkan banner peringatan "Sorry, WE ARE CLOSED" jika studio sedang tutup sementara. Ditangani di `katalog.php` menggunakan kondisi `if/match`.
- **Label Fully Booked:** Mengubah tampilan kartu paket yang sudah penuh (abu-abu/redup). Ditangani di `katalog.php` dengan pengecekan nilai boolean `slot_tersedia` menggunakan `if`.
- **Format Harga:** Memformat angka integer menjadi format string Rupiah. Ditangani oleh fungsi buatan `formatRupiah()` di file `functions.php`.
- **Proteksi Data (XSS):** Mengamankan setiap output teks ke HTML. Ditangani oleh fungsi buatan `e()` di `functions.php`.

## 5. Daftar Fungsi Array Bawaan
- `array_column()`: Digunakan untuk mengekstrak seluruh nilai dari atribut `harga` pada array katalog menjadi satu array tunggal.
- `array_sum()`: Digunakan untuk menjumlahkan seluruh harga paket guna mendapatkan estimasi total nilai aset/layanan studio.
- `count()`: Digunakan untuk menghitung total keseluruhan item paket yang tersedia di dalam katalog.
- `array_filter()`: Digunakan untuk memfilter dan mengelompokkan paket-paket yang status slotnya sudah penuh (`slot_tersedia == false`).

## 6. Tangkapan Layar (Screenshots)
<!-- Ganti path gambar di bawah dengan path screenshot aslimu ketika antarmuka sudah selesai -->
### Halaman Profil (`index.php`)
![Profil Bexa Studios](assets/screenshots/profil.png)

### Halaman Katalog (`katalog.php`)
![Katalog Bexa Studios](assets/screenshots/katalog.png)

## 7. Sumber Referensi & Penggunaan AI
- **Referensi:** PHP Manual (php.net) untuk panduan dokumentasi fungsi bawaan array.
- **Penggunaan AI:** Menggunakan bantuan AI untuk brainstorming pemilihan tema, merancang kerangka awal struktur `data.php` dan `functions.php`, serta membuat draf kerangka `README.md` ini. Seluruh baris kode yang dihasilkan telah diuji, dimodifikasi, dan dipahami alur logikanya secara mandiri.