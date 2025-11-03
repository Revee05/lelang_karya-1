# Dokumentasi Struktur Folder `routes`

Folder `routes` pada Laravel berisi file-file yang mendefinisikan seluruh rute (endpoint) aplikasi, baik untuk web, API, maupun console. Setiap file di sini mengelompokkan rute berdasarkan fungsinya. Berikut penjelasan detail setiap file di dalamnya:

---

- **web.php**  
  Mendefinisikan rute utama aplikasi berbasis web (HTTP), biasanya untuk frontend dan backend yang membutuhkan session, CSRF protection, dan fitur web lainnya.

- **api.php**  
  Mendefinisikan rute untuk API (biasanya berbasis REST), menggunakan middleware `api` yang lebih ringan dan stateless.

- **admin.php**  
  Mendefinisikan rute khusus untuk fitur admin, biasanya dengan prefix dan middleware otorisasi admin.

- **account.php**  
  Mendefinisikan rute khusus untuk fitur akun pengguna (user), seperti profil, alamat, pesanan, dsb.

- **channels.php**  
  Mendefinisikan rute untuk broadcasting channel (misal: event real-time dengan Laravel Echo).

- **console.php**  
  Mendefinisikan rute untuk perintah artisan berbasis closure, biasanya untuk command kustom yang tidak diakses melalui HTTP.

---

## Kesimpulan

Folder `routes` berfungsi untuk mengelola seluruh endpoint aplikasi secara terpisah berdasarkan jenis akses dan fitur.  
Struktur ini memudahkan pengelolaan, pemeliharaan, dan pengembangan rute aplikasi secara modular dan terorganisir.
