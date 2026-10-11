# Asset Inventory CyberShield

## 1. Data

| Aset | C | I | A | Alasan |
|---|---:|---:|---:|---|
| URL yang dianalisis | 2 | 3 | 2 | URL dapat mengandung informasi sensitif dan hasil analisis harus tetap akurat. |
| Hasil analisis URL | 2 | 3 | 2 | Hasil analisis menjadi dasar rekomendasi keamanan sehingga integritasnya penting. |
| Aturan deteksi URL | 2 | 3 | 2 | Perubahan aturan dapat memengaruhi hasil deteksi sehingga harus dijaga integritasnya. |
| Mock/sample URL | 1 | 2 | 2 | Data digunakan untuk demonstrasi dan pengujian sehingga dampak kebocorannya rendah. |

## 2. Layanan

| Aset | C | I | A | Alasan |
|---|---:|---:|---:|---|
| Halaman analisis URL | 1 | 3 | 3 | Layanan utama CyberShield harus tersedia dan memberikan hasil analisis yang benar. |
| Mesin analisis URL | 1 | 3 | 3 | Kesalahan atau perubahan proses analisis dapat menghasilkan penilaian risiko yang tidak tepat. |
| Website CyberShield | 1 | 3 | 3 | Website merupakan antarmuka utama yang digunakan pengguna untuk mengakses layanan. |

## 3. Secrets

| Aset | C | I | A | Alasan |
|---|---:|---:|---:|---|
| Secret/API key | 3 | 3 | 2 | Jika integrasi eksternal ditambahkan, API key harus dirahasiakan dan tidak boleh dimanipulasi. |

> Catatan: Pada versi prototype v0.1 belum terdapat API key atau secret eksternal yang digunakan.

## 4. Backup

| Aset | C | I | A | Alasan |
|---|---:|---:|---:|---|
| Backup source code | 2 | 3 | 2 | Source code perlu dijaga agar dapat dipulihkan jika terjadi kehilangan atau perubahan yang tidak diinginkan. |
| Backup konfigurasi aplikasi | 2 | 3 | 2 | Konfigurasi diperlukan untuk memulihkan aplikasi ke kondisi yang benar. |

## 5. Log

| Aset | C | I | A | Alasan |
|---|---:|---:|---:|---|
| Log aktivitas analisis | 2 | 3 | 2 | Log dapat digunakan untuk audit dan harus tetap akurat serta tidak dimanipulasi. |
| Log error aplikasi | 1 | 3 | 2 | Log error membantu proses debugging dan pemeliharaan aplikasi. |

> Catatan: Logging terpusat belum diimplementasikan pada prototype v0.1.

## 6. Akun Admin

| Aset | C | I | A | Alasan |
|---|---:|---:|---:|---|
| Akun admin | 3 | 3 | 2 | Akun admin berpotensi memiliki hak pengelolaan sistem sehingga kredensial dan aksesnya harus dilindungi. |

> Catatan: Fitur akun admin belum diimplementasikan pada prototype v0.1 dan dicatat sebagai aset yang perlu dipertimbangkan pada pengembangan berikutnya.

## Rating

- **C (Confidentiality/Kerahasiaan)**
  - 1 = rendah
  - 2 = sedang
  - 3 = tinggi
- **I (Integrity/Integritas)**
  - 1 = rendah
  - 2 = sedang
  - 3 = tinggi
- **A (Availability/Ketersediaan)**
  - 1 = rendah
  - 2 = sedang
  - 3 = tinggi

## Mekanisme Kriptografi

Pada prototype CyberShield v0.1 belum terdapat penyimpanan password maupun komunikasi dengan backend yang menggunakan mekanisme kriptografi secara eksplisit.

Data yang perlu dilindungi dengan kriptografi pada pengembangan berikutnya antara lain:

- Password akun admin → disimpan menggunakan **password hashing**, bukan plaintext.
- Secret/API key → disimpan secara aman dan tidak dimasukkan ke source code.
- Data sensitif yang disimpan → dapat menggunakan **enkripsi**.
- Data atau catatan penting yang perlu dibuktikan keasliannya → dapat menggunakan **digital signature/message authentication**.
