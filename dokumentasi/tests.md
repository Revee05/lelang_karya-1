# Dokumentasi Struktur Folder `tests`

Folder `tests` pada Laravel digunakan untuk menyimpan seluruh file pengujian (testing) aplikasi, baik pengujian unit maupun fitur. Berikut penjelasan detail setiap file dan subfolder di dalamnya:

---

## File Langsung di `tests/`
- **CreatesApplication.php**  
  Trait untuk bootstrap aplikasi Laravel saat testing.
- **TestCase.php**  
  Kelas dasar untuk semua test, mengatur environment dan helper umum.

---

## Subfolder

### 1. **Feature/**
  - **ExampleTest.php**  
    Contoh pengujian fitur (feature test), biasanya menguji alur aplikasi secara menyeluruh (end-to-end) seperti request HTTP dan response.

### 2. **Unit/**
  - **ExampleTest.php**  
    Contoh pengujian unit (unit test), menguji bagian kecil aplikasi secara terpisah, seperti fungsi atau metode tertentu.

---

## Kesimpulan

Folder `tests` memudahkan pengembangan aplikasi dengan memastikan setiap bagian berjalan sesuai harapan melalui pengujian otomatis, baik pada level unit maupun fitur.

---