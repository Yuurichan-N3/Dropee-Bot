
## Dropee Telegram Bot

Bot otomatis untuk game Dropee yang terhubung dengan Telegram. Bot ini mengelola token, sinkronisasi game, melakukan tapping otomatis, dan membeli upgrade untuk meningkatkan keuntungan dalam game.

## 🛠️ Fitur Utama

Login Otomatis: Mengambil token melalui data Telegram dan menyimpannya.

Verifikasi Keanggotaan Telegram: Memastikan pengguna bergabung di grup Telegram tertentu sebelum melanjutkan.

Sinkronisasi Game: Mengambil data terbaru seperti koin, energi, dan status tugas.

Auto Tap: Menggunakan energi untuk tapping otomatis dan mengumpulkan koin.

Auto Buy Upgrade: Membeli upgrade berdasarkan ROI tertinggi secara otomatis.

Manajemen Token: Mengecek kadaluwarsa token dan memperbaruinya jika perlu.


## 🔁 Alur Kerja Skrip

1. Menampilkan Banner
Saat skrip dijalankan, akan muncul banner selamat datang di terminal.


2. Memasukkan Telegram User ID
Pengguna diminta untuk memasukkan Telegram User ID mereka.


3. Verifikasi Keanggotaan Grup Telegram

Bot mengecek apakah pengguna sudah bergabung di grup Telegram tertentu.

Jika belum, pengguna akan diminta untuk join grup dan mengirimkan pesan ke bot.

Bot mengirimkan password verifikasi yang harus dimasukkan ke terminal.



4. Mengambil Token (Jika Ada)

Bot mengecek apakah sudah ada token yang tersimpan.

Jika token ada dan masih valid, langsung digunakan.

Jika token kadaluwarsa, bot akan login ulang menggunakan data inisialisasi.



5. Sinkronisasi Game
Setelah login berhasil, bot mengakses API untuk mengambil status terbaru pemain:

Jumlah koin

Energi yang tersedia

Status onboarding

Daftar tugas dan upgrade



6. Proses Auto Tap

Jika ada energi yang cukup (minimal 10), bot otomatis melakukan tap dalam beberapa batch.

Setiap batch menghasilkan koin yang langsung ditampilkan ke terminal.



7. Auto Buy Upgrade

Setelah tapping selesai, bot mengecek daftar upgrade yang tersedia.

Menghitung ROI (Return on Investment) untuk setiap upgrade.

Membeli upgrade dengan ROI tertinggi jika koin mencukupi.

Proses ini diulang hingga koin tidak cukup lagi untuk upgrade.



8. Menyimpan Data

Token terbaru disimpan ke file token.json.

Data pengguna yang terverifikasi disimpan ke verified_users.json.



9. Mengakhiri Program

Setelah semua proses selesai, bot menampilkan ringkasan hasil tapping dan belanja upgrade.

Terminal akan otomatis tertutup, atau menunggu input jika ada error.




## 🚀 Cara Menjalankan

1. Clone Repository


```
git clone https://github.com/Yuurichan-N3/Dropee-Bot.git
cd Dropee-Bot
```


2. Instal Dependensi


```
npm install
```


3. Jalankan Skrip


```
node bot.js
```



4. Ikuti Instruksi di Terminal
Masukkan User ID, verifikasi grup, dan tunggu hingga proses tapping dan upgrade selesai!



## 📘 Konfigurasi File

token.json: Menyimpan token pengguna yang sudah login.

verified_users.json: Menyimpan data pengguna yang sudah diverifikasi.

data.txt: Menyimpan data inisialisasi yang dibutuhkan untuk login pertama kali.


## 📜 Lisensi  

Script ini didistribusikan untuk keperluan pembelajaran dan pengujian. Penggunaan di luar tanggung jawab pengembang.  

Untuk update terbaru, bergabunglah di grup **Telegram**: [Klik di sini](https://t.me/sentineldiscus).


---

## 💡 Disclaimer
Penggunaan bot ini sepenuhnya tanggung jawab pengguna. Kami tidak bertanggung jawab atas penyalahgunaan skrip ini.
