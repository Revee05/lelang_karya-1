# Dokumentasi Struktur Folder `app`

Folder `app` pada Laravel adalah inti dari logika aplikasi. Berikut penjelasan detail setiap file dan subfolder di dalamnya:

---

## Model (File Langsung di `app/`)
- **Bid.php, Checkout.php, Kabupaten.php, Karya.php, Kategori.php, Kecamatan.php, Kelengkapan.php, Order.php, Posts.php, ProductImage.php, Products.php, Provinsi.php, Setting.php, Shipper.php, Sliders.php, Tags.php, User.php, UserAddress.php**
  - Setiap file ini adalah model Eloquent yang mewakili tabel pada database. Model ini mengatur relasi, validasi, dan logika bisnis terkait data masing-masing entitas (misal: user, produk, kategori, alamat, penawaran, dll).

---

## Subfolder

### 1. **Console/**
- **Kernel.php**  
  Mengatur jadwal dan pendaftaran command artisan kustom.
- **Commands/**  
  - **EndDate.php, NotificationBid.php, SendEmails.php, TestCheckout.php**  
    Berisi perintah artisan kustom yang dapat dijalankan via terminal, seperti mengirim notifikasi, email, atau proses otomatis lain.

### 2. **Events/**
- **BidSent.php, MessageSent.php**  
  Mendefinisikan event yang dipicu dalam aplikasi, misal saat bid dikirim atau pesan dikirim pada chat.

### 3. **Exceptions/**
- **Handler.php**  
  Menangani pengecualian (error) aplikasi secara global.

### 4. **Http/**
- **Kernel.php**  
  Mengatur middleware HTTP aplikasi.
- **Controllers/**  
  - **BidController.php, BlogsController.php, Controller.php, DaftarPemenangController.php, DaftarPenawaranController.php, DashboardController.php, KabupatenController.php, KaryaController.php, KategoriController.php, KecamatanController.php, KelengkapanController.php, PostsController.php, ProductsController.php, ProvinsiController.php, SettingController.php, ShipperController.php, SlidersController.php, TagsController.php, UserAddressController.php, UsersController.php**  
    Controller utama untuk mengelola request dan response pada berbagai fitur aplikasi.
  - **Account/**  
    - **AddressController.php, CheckoutController.php, MemberController.php, OrderController.php, PaymentCallbackController.php**  
      Controller untuk fitur akun pengguna, checkout, order, dan pembayaran.
  - **Auth/**  
    - **ConfirmPasswordController.php, ForgotPasswordController.php, LoginController.php, RegisterController.php, ResetPasswordController.php, VerificationController.php**  
      Controller untuk autentikasi dan otorisasi pengguna.
  - **Web/**  
    - **BlogController.php, ChatsController.php, HomeController.php**  
      Controller untuk halaman publik seperti blog, chat, dan home.
- **Middleware/**  
  - **Authenticate.php, CheckForMaintenanceMode.php, EncryptCookies.php, IsAdmin.php, IsMember.php, RedirectIfAuthenticated.php, TrimStrings.php, TrustProxies.php, VerifyCsrfToken.php**  
    Middleware untuk memfilter dan mengatur request, seperti autentikasi, role, keamanan, dan maintenance.

### 5. **Jobs/**
- **SendNotifacationBid.php**  
  Mendefinisikan job (pekerjaan) yang dapat dijalankan secara asynchronous, misal mengirim notifikasi bid.

### 6. **Mail/**
- **BidNotification.php, OrderShipped.php**  
  Kelas untuk mengirim email notifikasi terkait bid dan pengiriman order.

### 7. **Prints/**
- **TransaksiPrint.php**  
  Kelas untuk menangani proses cetak data transaksi.

### 8. **Product/**
- **Uploads.php**  
  Kelas untuk menangani upload file/gambar produk.

### 9. **Providers/**
- **AppServiceProvider.php, AuthServiceProvider.php, BroadcastServiceProvider.php, EventServiceProvider.php, RouteServiceProvider.php**  
  Service provider untuk mendaftarkan layanan, event, dan binding pada aplikasi Laravel.

### 10. **Services/**
- **CallbackService.php, CreateSnapTokenService.php, Midtrans.php**  
  Service class untuk logika khusus, seperti integrasi pembayaran (Midtrans) dan callback pembayaran.

---

## Kesimpulan

Folder `app` adalah pusat logika backend aplikasi Laravel.  
- Model: merepresentasikan data dan relasi database.
- Controller: mengelola request, response, dan proses bisnis.
- Middleware: memfilter request.
- Event, Job, Mail, Print, Service: mendukung fitur tambahan seperti event, queue, email, cetak, dan integrasi pihak ketiga.
- Provider: mendaftarkan layanan dan event aplikasi.

Struktur ini memudahkan pengembangan, pemeliharaan, dan pengelolaan fitur aplikasi secara modular.
