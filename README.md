yolks - Pterodactyl Egg & Installer Images with Indonesia Timezone
Selamat datang di repositori yolks! Repositori ini berisi kustomisasi image Docker untuk Pterodactyl Panel, khususnya untuk game Grand Theft Auto: San Andreas Multiplayer (GTA: SA-MP), serta image installer untuk berbagai distribusi Linux (Alpine, Debian, Ubuntu), yang semuanya telah dikonfigurasi dengan zona waktu Asia/Jakarta (WIB).

Dikembangkan oleh Bennnn2708.

Daftar Image Docker
Berikut adalah daftar image Docker yang tersedia dan fungsinya:

1. Image Utama Aplikasi (Game SA-MP)
Nama Image: benigaming27/samp:latest
Fungsi: Ini adalah image Docker utama yang akan menjalankan server game GTA: SA-MP Anda. Image ini telah dikonfigurasi untuk memastikan server berjalan dengan zona waktu yang benar, yaitu Asia/Jakarta.
Penggunaan di Pterodactyl Panel:
Pada konfigurasi Egg untuk GTA: SA-MP, di bagian "Docker Images", masukkan:
benigaming27/samp:latest
2. Image Installer - Alpine Linux
Nama Image: benigaming27/installer-alpine:latest
Fungsi: Image ini dirancang sebagai "Script Container" untuk Pterodactyl Panel, yang akan digunakan untuk menjalankan script instalasi game (mengunduh, mengekstrak, dll.) di lingkungan Alpine Linux. Image ini juga sudah menyertakan pengaturan zona waktu Asia/Jakarta.
Penggunaan di Pterodactyl Panel:
Pada konfigurasi Egg untuk GTA: SA-MP, di bagian "Script Container" (dalam "Install Script"), Anda bisa memilih untuk menggunakan image ini dengan memasukkan:
benigaming27/installer-alpine:latest
Catatan: Pilih ini jika Anda ingin lingkungan instalasi yang sangat ringan.
3. Image Installer - Debian
Nama Image: benigaming27/installer-debian:latest
Fungsi: Sama seperti installer Alpine, namun ini adalah versi berbasis Debian. Image ini digunakan sebagai "Script Container" untuk menjalankan script instalasi game di lingkungan Debian, dengan zona waktu Asia/Jakarta.
Penggunaan di Pterodactyl Panel:
Pada konfigurasi Egg untuk GTA: SA-MP, di bagian "Script Container" (dalam "Install Script"), Anda bisa memilih untuk menggunakan image ini dengan memasukkan:
benigaming27/installer-debian:latest
Catatan: Ini mungkin pilihan yang baik jika Anda membutuhkan kompatibilitas yang lebih luas dengan tool Debian.
4. Image Installer - Ubuntu
Nama Image: benigaming27/installer-ubuntu:latest
Fungsi: Image ini juga berfungsi sebagai "Script Container" untuk menjalankan script instalasi game di lingkungan Ubuntu. Sama seperti installer lainnya, image ini juga telah dikonfigurasi dengan zona waktu Asia/Jakarta.
Penggunaan di Pterodactyl Panel:
Pada konfigurasi Egg untuk GTA: SA-MP, di bagian "Script Container" (dalam "Install Script"), Anda bisa memilih untuk menggunakan image ini dengan memasukkan:
benigaming27/installer-ubuntu:latest
Catatan: Ubuntu adalah pilihan populer dan sering digunakan.
Cara Menggunakan (Ringkasan Proses)
Akses Pterodactyl Panel: Login ke panel admin Pterodactyl Anda.
Edit Egg yang Sesuai: Navigasi ke Nests > [Pilih Nest yang sesuai] > [Pilih Egg GTA: SA-MP].
Update Docker Images:
Di bagian "Docker Images", ganti nilai default dengan benigaming27/samp:latest.
Update Script Container (Opsional, tapi disarankan):
Di bagian "Install Script", cari kolom "Script Container".
Ganti nilai default (misalnya ghcr.io/parkervcp/installers:debian) dengan salah satu image installer kustom Anda, misalnya: benigaming27/installer-debian:latest.
Simpan Perubahan: Pastikan Anda menyimpan semua perubahan konfigurasi Egg.
Buat/Reinstall Server: Ketika membuat server baru atau me-reinstall server yang sudah ada menggunakan Egg ini, server akan otomatis menggunakan image Docker yang sudah Anda kustomisasi dengan zona waktu Asia/Jakarta.
Struktur Repositori
yolks/
├── games/
│   └── samp/
│       └── Dockerfile             # Dockerfile untuk image aplikasi utama SA-MP
├── installers/
│   ├── alpine/
│   │   └── Dockerfile             # Dockerfile untuk installer berbasis Alpine
│   ├── debian/
│   │   └── Dockerfile             # Dockerfile untuk installer berbasis Debian
│   └── ubuntu/
│       └── Dockerfile             # Dockerfile untuk installer berbasis Ubuntu
└── README.md                      # File ini
Kontribusi & Lisensi
Jika Anda menemukan masalah atau memiliki saran, jangan ragu untuk membuka Issue atau Pull Request.

Lisensi yang digunakan adalah MIT License. Lihat file LICENSE untuk detail lebih lanjut.
