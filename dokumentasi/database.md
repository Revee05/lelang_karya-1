# Dokumentasi Struktur Folder `database`

Folder `database` pada Laravel digunakan untuk mengelola struktur, data awal, dan pengujian database aplikasi. Berikut penjelasan detail setiap file dan subfolder di dalamnya:

---

## File Langsung di `database/`
- **.gitignore**  
  Mengatur file/folder mana yang diabaikan oleh Git, biasanya untuk menghindari file sementara atau hasil build.

---

## Subfolder

### 1. **factories/**
Berisi file factory untuk membuat data dummy (pengujian atau seeding).
- **OrderFactory.php, UserFactory.php**  
  Mendefinisikan blueprint pembuatan data palsu untuk tabel `orders` dan `users` menggunakan Faker.

### 2. **migrations/**
Berisi file migrasi yang mendefinisikan struktur tabel database.
- **2014_10_12_000000_create_users_table.php**  
  Membuat tabel `users`.
- **2014_10_12_100000_create_password_resets_table.php**  
  Membuat tabel `password_resets`.
- **2019_08_19_000000_create_failed_jobs_table.php**  
  Membuat tabel `failed_jobs` untuk menyimpan job yang gagal.
- **2023_02_16_135956_create_kategoris_table.php**  
  Membuat tabel `kategoris`.
- **2023_03_03_163828_create_setting_table.php**  
  Membuat tabel `setting`.
- **2023_03_17_150343_create_user_address_table.php**  
  Membuat tabel `user_address`.
- **2023_03_17_150357_create_products_table.php**  
  Membuat tabel `products`.
- **2023_03_17_150412_create_product_images_table.php**  
  Membuat tabel `product_images`.
- **2023_03_17_150445_create_shipper_table.php**  
  Membuat tabel `shipper`.
- **2023_03_17_154238_create_bid_table.php**  
  Membuat tabel `bid`.
- **2023_03_17_154433_create_checkout_table.php**  
  Membuat tabel `checkout`.
- **2023_03_17_161157_create_provinsi_table.php**  
  Membuat tabel `provinsi`.
- **2023_03_17_161208_create_kabupaten_table.php**  
  Membuat tabel `kabupaten`.
- **2023_03_17_161217_create_kecamatan_table.php**  
  Membuat tabel `kecamatan`.
- **2023_03_23_023927_create_karya_table.php**  
  Membuat tabel `karya`.
- **2023_04_01_134233_create_posts_table.php**  
  Membuat tabel `posts`.
- **2023_04_28_143932_create_orders_table.php**  
  Membuat tabel `orders`.
- **2023_05_12_005717_create_sliders_table.php**  
  Membuat tabel `sliders`.
- **2023_05_12_084546_create_kelengkapan_table.php**  
  Membuat tabel `kelengkapan`.
- **2023_05_12_084806_create_kelengkapan_product_table.php**  
  Membuat tabel pivot `kelengkapan_product`.
- **2023_06_13_055206_create_tags_table.php**  
  Membuat tabel `tags`.
- **2023_06_13_060004_create_post_tag_table.php**  
  Membuat tabel pivot `post_tag`.
- **2023_07_16_223011_create_jobs_table.php**  
  Membuat tabel `jobs` untuk queue.

### 3. **seeds/**
Berisi file seeder untuk mengisi data awal ke dalam tabel database.
- **DatabaseSeeder.php**  
  Seeder utama yang menjalankan seeder lain.
- **kabupaten.sql, kecamatan.sql, provinsi.sql**  
  File SQL untuk mengisi data wilayah Indonesia.
- **KaryaSeeder.php, KategoriSeeder.php, KelengkapanSeeder.php, ProductsSeeder.php, ProdukSeeder.php, SettingSeeder.php, ShipperSeeder.php, UserSeeder.php**  
  Seeder untuk mengisi data awal pada tabel terkait (karya, kategori, kelengkapan, produk, setting, shipper, user).

---

## Kesimpulan

Folder `database` berfungsi untuk:
- Mendefinisikan struktur tabel database (migrations)
- Membuat data dummy untuk pengujian (factories)
- Mengisi data awal ke database (seeds)
- Menyimpan file SQL untuk data wilayah

Struktur ini memudahkan pengelolaan database secara otomatis, konsisten, dan dapat diulang pada berbagai lingkungan pengembangan atau produksi.
