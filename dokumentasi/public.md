# Dokumentasi Struktur Folder `public`

Folder `public` pada Laravel adalah root direktori yang diakses langsung oleh web server. Semua file di sini dapat diakses publik dan berisi aset yang sudah siap digunakan oleh browser. Berikut penjelasan detail setiap file dan subfolder di dalamnya:

---

## File Utama di `public/`
- **.htaccess, web.config**  
  File konfigurasi server (Apache dan IIS) untuk mengatur URL rewriting, keamanan, dsb.
- **index.php**  
  Entry point aplikasi Laravel, meneruskan semua request ke framework.
- **mix-manifest.json**  
  File manifest hasil kompilasi Laravel Mix, mengatur versi file aset.
- **robots.txt**  
  Mengatur akses robot mesin pencari ke situs.

---

## Subfolder & Konten

### 1. **assets/**
  - Berisi template admin (seperti SB Admin 2), file HTML statis, CSS, JS, SCSS, gambar, dan vendor library (Bootstrap, Chart.js, DataTables, FontAwesome, jQuery, Summernote, dsb).
  - **css/**: File CSS hasil kompilasi template.
  - **img/**: Gambar-gambar untuk template.
  - **js/**: File JavaScript untuk interaktivitas template.
  - **scss/**: Sumber file SCSS untuk styling.
  - **vendor/**: Library pihak ketiga yang digunakan oleh template.

### 2. **css/**
  - **app.css**: File CSS utama aplikasi hasil kompilasi dari SASS/SCSS.

### 3. **fonts/**
  - Font yang digunakan aplikasi, termasuk dari vendor seperti Bootstrap.

### 4. **js/**
  - **app.js**: File JavaScript utama aplikasi.
  - **jquery.chained.min.js, select2.min.js**: Plugin tambahan untuk interaktivitas form.

### 5. **theme/**
  - Berisi file dan aset untuk tema frontend, seperti HTML, CSS, JS, dan plugin carousel (owlcarousel).

### 6. **uploads/**
  - Folder untuk menyimpan file upload pengguna, seperti gambar produk, blog, logo, slider, dsb.
  - Struktur berdasarkan tahun/bulan untuk pengelolaan file yang lebih rapi.

---

## Kesimpulan

Folder `public` adalah satu-satunya folder yang dapat diakses langsung oleh pengguna melalui browser.  
Berisi:
- Entry point aplikasi (`index.php`)
- File konfigurasi server
- Aset statis (CSS, JS, gambar, font, tema)
- File hasil kompilasi dan upload pengguna

Semua file dari proses build (SASS, JS, dsb) dan file upload akan tersedia di sini agar dapat diakses oleh frontend aplikasi.
