# AI Log

## Penggunaan AI pada Pekan 3

AI digunakan sebagai alat bantu selama proses analisis keamanan CyberShield. Penggunaan AI difokuskan pada membantu menyusun dan meninjau dokumentasi, bukan sebagai pengganti keputusan akhir dalam analisis keamanan.

### 1. Asset Inventory

AI membantu:
- meninjau daftar aset CyberShield;
- mengelompokkan aset berdasarkan data, layanan, secrets, backup, log, dan akun admin;
- memberikan saran pemberian ID aset;
- membantu memberikan penilaian CIA (Confidentiality, Integrity, Availability);
- membedakan aset yang sudah aktif pada prototype v0.1 dengan aset yang masih berupa rencana pengembangan.

Hasil akhir disesuaikan dengan kondisi CyberShield v0.1.

### 2. Data Flow Diagram (DFD)

AI membantu:
- menyusun identitas elemen DFD;
- memberikan ID untuk external entity, process, data store, dan data flow;
- membantu menambahkan trust boundary;
- mengidentifikasi aliran data yang perlu diperhatikan dari sisi keamanan;
- membantu menandai status perlindungan kriptografi pada data.

DFD akhir disesuaikan dengan arsitektur CyberShield yang berjalan pada prototype v0.1.

### 3. Threat Modeling

AI membantu mengidentifikasi threat menggunakan metode STRIDE.

Threat yang dianalisis kemudian dikaitkan dengan:
- elemen DFD;
- data flow;
- aset yang terdampak;
- kategori STRIDE.

AI juga membantu menyusun alasan setiap threat berdasarkan kondisi CyberShield v0.1, seperti penggunaan client-side analysis dan belum adanya backend, autentikasi, serta centralized logging.

### 4. Risk Assessment

AI membantu:
- menentukan skala likelihood dan impact;
- menghitung risk score menggunakan rumus:

`Risk Score = Likelihood × Impact`

- menyusun alasan likelihood dan impact berdasarkan kondisi prototype;
- membantu memilih lima risiko prioritas.

Penilaian akhir tetap mempertimbangkan karakteristik dan kondisi aktual CyberShield v0.1.

### 5. Security Control Plan

AI membantu menyusun rencana kontrol untuk lima risiko prioritas.

Kontrol yang direncanakan antara lain:
- server-side validation;
- server-side analysis;
- server-side detection rules;
- access control;
- HTTPS;
- data minimization.

Kontrol tersebut merupakan rencana pengembangan dan **belum seluruhnya diimplementasikan pada CyberShield v0.1**.

## Batasan Penggunaan AI

AI digunakan sebagai alat bantu brainstorming, penyusunan struktur dokumentasi, dan review keamanan. Keputusan mengenai aset, threat, tingkat risiko, prioritas, serta kontrol disesuaikan dengan kondisi aktual produk.

AI tidak digunakan untuk mengklaim bahwa fitur keamanan yang belum diimplementasikan sudah tersedia pada CyberShield v0.1.

## Kesimpulan

Penggunaan AI membantu mempercepat proses penyusunan threat model, risk register, dan security control plan. Hasil akhir tetap ditinjau dan disesuaikan agar merepresentasikan kondisi aktual CyberShield pada Pekan 3.