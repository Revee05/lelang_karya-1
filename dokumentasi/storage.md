# Dokumentasi Struktur Folder `storage`

Folder `storage` pada Laravel digunakan untuk menyimpan file yang dihasilkan atau digunakan aplikasi selama runtime. Berikut penjelasan umum struktur dan fungsinya:

---

- **app/**  
  Menyimpan file aplikasi yang tidak boleh diakses publik, seperti file upload sementara atau file yang diproses.

- **framework/**  
  Menyimpan cache framework, session, view yang sudah di-compile, dan file temporary lain yang dibutuhkan Laravel.

- **logs/**  
  Menyimpan file log aplikasi, seperti error, info, dan aktivitas aplikasi.

- **public/**  
  Menyimpan file upload yang dapat diakses publik melalui symbolic link dari `public/storage`.

---

## Kesimpulan

Folder `storage` sangat penting untuk operasi aplikasi, menyimpan data sementara, cache, log, dan file upload.  
Pastikan folder ini dapat ditulis oleh server dan tidak diekspos langsung ke publik kecuali melalui symbolic link yang aman.
