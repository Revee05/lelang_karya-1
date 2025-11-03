# Dokumentasi Struktur Folder `config`

Folder `config` pada Laravel berisi file konfigurasi utama aplikasi. Setiap file di sini mengatur berbagai aspek dan layanan yang digunakan aplikasi. Berikut penjelasan detail setiap file di dalamnya:

---

- **app.php**  
  Konfigurasi utama aplikasi, seperti nama, environment, timezone, locale, dan provider.

- **auth.php**  
  Pengaturan autentikasi, guard, provider user, dan reset password.

- **broadcasting.php**  
  Konfigurasi broadcasting event (misal: Pusher, Redis, log).

- **cache.php**  
  Pengaturan sistem cache, driver yang digunakan (file, redis, dsb).

- **database.php**  
  Konfigurasi koneksi database (MySQL, SQLite, SQL Server, dsb).

- **dompdf.php**  
  Pengaturan library DomPDF untuk generate file PDF.

- **filesystems.php**  
  Pengaturan storage file, driver lokal, public, dan cloud (seperti S3).

- **flare.php**  
  Konfigurasi integrasi dengan Flare untuk error tracking.

- **hashing.php**  
  Pengaturan algoritma hashing password (bcrypt, argon).

- **logging.php**  
  Pengaturan sistem logging aplikasi (stack, single, daily, slack, dsb).

- **mail.php**  
  Konfigurasi pengiriman email (driver, host, port, encryption, dsb).

- **midtrans.php**  
  Pengaturan integrasi pembayaran dengan Midtrans.

- **queue.php**  
  Pengaturan sistem queue (antrian pekerjaan), driver, koneksi, dsb.

- **rajaongkir.php**  
  Konfigurasi integrasi API RajaOngkir untuk ongkos kirim.

- **services.php**  
  Pengaturan layanan eksternal lain (misal: mailgun, stripe, dsb).

- **session.php**  
  Pengaturan session aplikasi (driver, lifetime, cookie, dsb).

- **view.php**  
  Pengaturan sistem view/template (path, cache, dsb).

---

## Kesimpulan

Folder `config` berfungsi untuk mengelola seluruh pengaturan aplikasi dan layanan eksternal secara terpusat.  
Setiap file dapat diubah sesuai kebutuhan tanpa harus mengubah kode utama aplikasi, sehingga memudahkan pengelolaan dan deployment di berbagai lingkungan.
