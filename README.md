<div align="center">
  <a href="https://samarindakota.go.id/" target="_blank">
    <img src="public/images/pemkot-samarinda.png" width="90" alt="Logo Pemkot Samarinda">
  </a>
  &nbsp;&nbsp;&nbsp;&nbsp;
  <h1>Jalan Peduli - Pelaporan Kerusakan Jalan Samarinda</h1>
  &nbsp;&nbsp;&nbsp;&nbsp;
  <a href="https://dpupr.samarindakota.go.id/" target="_blank">
    <img src="public/images/dinas-pupr-kota-samarinda.png" width="90" alt="Logo Dinas PUPR Samarinda">
  </a>
</div>

<p align="center">
  Platform web untuk melaporkan dan memantau kerusakan infrastruktur jalan di Kota Samarinda, dikembangkan untuk Dinas Pekerjaan Umum dan Penataan Ruang (PUPR) Kota Samarinda.
</p>

<p align="center">
  <a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
  <a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
  <a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
  <a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

---

## 📋 Tentang Proyek

**Jalan Peduli** adalah sebuah inisiatif digital yang menjembatani masyarakat Kota Samarinda dengan Dinas PUPR. Aplikasi ini mempermudah warga untuk melaporkan kerusakan jalan secara cepat dan efisien, serta memungkinkan dinas terkait untuk mengelola, memverifikasi, dan menindaklanjuti laporan dengan lebih terstruktur.

<br>

<p align="center">
  <img src="public/images/panduan_penggunaan.jpeg" width="800" alt="Panduan Penggunaan Aplikasi">
</p>

---

## ✨ Fitur Utama

* 📱 **Pelaporan Mudah:** Laporkan kerusakan jalan lengkap dengan detail lokasi (via peta atau geolokasi), deskripsi, dan unggah foto sebagai bukti.
* 🔍 **Cek Status Laporan:** Pantau progres perbaikan laporan Anda secara transparan hanya dengan menggunakan ID Laporan atau nomor telepon.
* 🗺️ **Peta Interaktif:** Lihat sebaran semua laporan kerusakan jalan yang telah diverifikasi oleh petugas di seluruh wilayah Samarinda.
* 📊 **Dasbor Statistik:** Akses data dan statistik laporan berdasarkan status (diterima, diproses, selesai), jenis, dan tingkat kerusakan.
* ❓ **FAQ:** Temukan jawaban atas pertanyaan yang sering diajukan mengenai proses pelaporan dan perbaikan.
* 🔒 **Panel Admin:** Sistem login terpisah bagi petugas PUPR untuk melakukan manajemen, validasi, dan pembaruan status laporan.

---

## 🛠️ Tech Stack

| Kategori            | Teknologi                                                                                                                                                                                                                                                                                            |
| ------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Backend** | <img src="https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white" alt="Laravel">                                                                                                                                                                                  |
| **Frontend** | <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind CSS"> <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript">                                    |
| **Database** | <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL">                                                                                                                                                                                      |
| **Library & Tools** | <img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white" alt="Vite"> <img src="https://img.shields.io/badge/Leaflet.js-199900?style=for-the-badge&logo=leaflet&logoColor=white" alt="Leaflet.js"> <img src="https://img.shields.io/badge/Chart.js-FF6384?style=for-the-badge&logo=chart.js&logoColor=white" alt="Chart.js"> <img src="https://img.shields.io/badge/Anime.js-F84646?style=for-the-badge&logo=anime.js&logoColor=white" alt="Anime.js"> |
| **Layanan Eksternal** | <img src="https://img.shields.io/badge/Cloudflare-F38020?style=for-the-badge&logo=Cloudflare&logoColor=white" alt="Cloudflare"> <img src="https://img.shields.io/badge/Maps-4285F4?style=for-the-badge&logo=google-maps&logoColor=white" alt="Google Maps"> <img src="https://img.shields.io/badge/MapTiler-5194F3?style=for-the-badge" alt="MapTiler"> |                                                           |

---

## 🚀 Instalasi & Konfigurasi

### Kebutuhan Sistem
* PHP >= 8.1
* Composer
* Node.js & NPM
* Database Server (cth: MySQL, MariaDB)

### 1. Penyiapan Lokal (Development)

1.  **Clone Repositori**
    ```bash
    git clone <URL_REPOSITORI_ANDA>
    cd <NAMA_FOLDER_PROJECT>
    ```

2.  **Instal Dependensi**
    ```bash
    composer install
    npm install
    ```

3.  **Konfigurasi Environment**
    Salin file `.env.example` menjadi `.env` dan sesuaikan nilainya.
    ```bash
    cp .env.example .env
    ```
    Pastikan Anda mengisi konfigurasi database (`DB_*`), URL aplikasi (`APP_URL`), dan kunci API layanan eksternal (opsional).

4.  **Setup Aplikasi**
    ```bash
    php artisan key:generate
    php artisan migrate --seed # Jalankan seeder jika ada
    php artisan storage:link
    ```

5.  **Jalankan Server Pengembangan**
    ```bash
    npm run dev    # Di satu terminal
    php artisan serve  # Di terminal lain
    ```
    Aplikasi dapat diakses di `http://127.0.0.1:8000`.

### 2. Replikasi di Produksi (Production)

1.  Clone repositori di server Anda.
2.  Instal dependensi untuk produksi: `composer install --no-dev --optimize-autoloader`.
3.  Konfigurasi file `.env` untuk lingkungan produksi (`APP_ENV=production`, `APP_DEBUG=false`).
4.  Jalankan `php artisan key:generate`.
5.  Jalankan migrasi: `php artisan migrate --force`.
6.  Build aset frontend: `npm install && npm run build`.
7.  Buat symlink: `php artisan storage:link`.
8.  Pastikan izin folder `storage` dan `bootstrap/cache` sudah benar (writable oleh web server).
9.  Arahkan web server (Nginx/Apache) ke direktori `public`.
10. Optimalkan konfigurasi dan route: `php artisan optimize`.

---

##  Usage

* **Masyarakat Umum:** Kunjungi URL publik aplikasi untuk mulai melaporkan kerusakan, melacak status laporan, atau melihat peta sebaran.
* **Petugas PUPR:** Akses rute `/login` untuk masuk ke panel admin menggunakan kredensial yang telah disediakan.

---

## 🤝 Kontribusi

Kontribusi Anda sangat kami harapkan! Jika Anda ingin membantu mengembangkan proyek ini, silakan fork repositori, buat branch baru untuk fitur Anda (`git checkout -b feature/NamaFitur`), dan kirim *Pull Request*.

## 📜 Lisensi

Proyek ini dirilis di bawah Lisensi MIT. Lihat file `LICENSE` untuk detail lebih lanjut.
