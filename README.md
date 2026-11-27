# GaransiKu

Aplikasi Android untuk mencatat produk elektronik yang dimiliki, memantau masa garansi, dan menyimpan riwayat servis beserta dokumen pembeliannya.

| | |
|---|---|
| Nama | Ramiza Kamala Tatsuru |
| NIM | 20220140006 |
| Kelas | C |
| Program Studi | Teknologi Informasi |
| Mata Kuliah | Pengembangan Aplikasi Mobile |
| Universitas | Universitas Muhammadiyah Yogyakarta |

## 1. Deskripsi Aplikasi

GaransiKu membantu pengguna mencatat produk elektronik yang dimiliki beserta nomor seri, tanggal pembelian, dan durasi garansi. Aplikasi menghitung tanggal berakhir garansi, menampilkan produk yang garansinya segera berakhir, menyimpan salinan nota pembelian atau kartu garansi, serta mencatat riwayat servis tiap produk.

Aplikasi terdiri atas dua bagian yang dipisahkan menjadi dua repositori:

- **Mobile** (repositori ini): aplikasi Android berbasis Kotlin dan Jetpack Compose.
- **API**: layanan backend Laravel beserta basis data MySQL, berada pada repositori `0006_API_GaransiKu`.

Dokumen kebutuhan perangkat lunak tersedia pada folder [`doc`](doc/GaransiKu_SRS_0006.pdf).

## 2. Teknologi

| Bagian | Teknologi |
|---|---|
| Aplikasi Android | Kotlin, Jetpack Compose, Navigation Compose, MVVM, Retrofit, Coil |
| Layanan REST API | PHP 8.2, Laravel 11, autentikasi JWT |
| Basis data | MySQL 8.0 |

## 3. Daftar Fitur

| No | Fitur | Keterangan | Status |
|---|---|---|---|
| 1 | Autentikasi | Pendaftaran akun, masuk, dan pembaruan access token | Belum |
| 2 | Otorisasi peran | Peran pengguna dan admin, pembatasan menu dan endpoint | Belum |
| 3 | Pengelolaan kategori produk | CRUDS kategori, khusus admin | Belum |
| 4 | Pengelolaan produk | CRUDS produk beserta pencarian dan penyaringan | Belum |
| 5 | Dokumen garansi | Penyimpanan dan pembacaan berkas nota atau kartu garansi | Belum |
| 6 | Riwayat servis | Pencatatan, perubahan, dan pencarian riwayat servis | Belum |
| 7 | Status masa garansi | Perhitungan sisa masa garansi dan penanda produk yang segera berakhir | Belum |
| 8 | Pengelolaan akun | Daftar akun, perubahan peran, dan penghapusan akun, khusus admin | Belum |

Keterangan status: **Belum**, **Proses**, **Selesai**.

## 4. Progress Mingguan (Weekly Progress)

Berikut adalah linimasa pengembangan proyek GaransiKu yang direkonstruksi secara riil berdasarkan riwayat git commit pada 0006_GaransiKu (Mobile), mulai dari pertemuan 9 hingga pertemuan 16 sesuai pedoman Bagian C.

📅 Pertemuan 9 (17 – 23 Nov 2026) — 0006_GaransiKu

Repositori belum memuat commit pada pertemuan ini; penyiapan judul dan penyusunan dokumen kebutuhan berlangsung sebelum repositori diinisialisasi.

📅 Pertemuan 10 (24 – 30 Nov 2026) — 0006_GaransiKu

- **Penempatan Dokumen Perancangan** (`3acb520`): Menyusun dokumen SRS versi 0.2 beserta diagram hubungan antar-entitas dan diagram use case, kemudian menempatkan berkas PDF-nya pada folder `doc`.
- **Struktur Repositori dan README** (`e209653`): Membuat README yang memuat deskripsi aplikasi, teknologi yang dipakai, daftar fitur beserta statusnya, dan format catatan progress mingguan.
- **Diagram Aktivitas per Fitur** (`4720e78`): Menambahkan delapan diagram aktivitas pada Lampiran B.4 dokumen SRS beserta rujukannya pada setiap fitur di Bab 3, kemudian memperbarui berkas PDF pada folder `doc`.
- **Penyesuaian Mekanisme Autentikasi** (`037c57d`): Menyesuaikan SRS menjadi versi 0.3 — access token tanpa masa berlaku, refresh token per sesi yang dicabut saat keluar, kolom `refresh_token` pada tabel akun, serta pembaruan diagram hubungan antar-entitas dan diagram aktivitas autentikasi.
