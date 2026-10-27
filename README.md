**Undangan Pernikahan Digital** 

Website undangan pernikahan digital interaktif dan responsif yang dibuat menggunakan HTML5, CSS3, Bootstrap 5, dan JavaScript. Proyek ini dirancang elegan dengan fitur penyesuaian nama tamu otomatis, audio musik latar, hitung mundur (countdown), galeri foto, hingga formulir integrasi RSVP berbasis Google Sheets.

**Fitur Utama**

1. Cover & Personalisasi Tamu: Menampilkan nama tamu undangan secara kustom melalui parameter URL (?n=Nama&p=Bapak/Ibu/Saudara/i).
2. Musik Latar Autoplay: Efek pemutaran audio otomatis setelah tombol "Lihat Undangan" diklik, lengkap dengan kontrol putar/jeda melayang (floating icon).
3. Hitung Mundur (Countdown Timer): Penghitung waktu mundur secara real-time menuju hari pernikahan menggunakan library simplyCountdown.js.
4. Kisah Cinta (Love Story Timeline): Tampilan garis waktu (timeline) perjalanan hubungan pasangan yang responsif.
5. Galeri Foto: Pop-up galeri foto berkualitas tinggi menggunakan bs5-lightbox.
6. Formulir RSVP (Integrasi Google Sheets): Tamu dapat mengonfirmasi kehadiran dan data langsung tersimpan ke Google Sheets tanpa butuh backend server tambahan.
7. Amplop Digital / Hadiah: Informasi rekening bank dan kode QR Saweria untuk penyerahan tanda kasih secara online.
8. Desain Fully Responsive: Tampilan optimal di perangkat seluler, tablet, maupun desktop.

**Teknologi yang Digunakan**

- HTML5 & CSS3 (Custom Styling & Variables)
- Bootstrap v5.3.0 (Grid System, Navbar, Cards, Modals)
- Bootstrap Icons
- JavaScript (ES6)
- Libraries External:
  - simplyCountdown.js (Timer hitung mundur)
  - bs5-lightbox (Lightbox galeri)
- Google Apps Script (GAS) (Backend gratisan untuk formulir RSVP ke Google Sheets)

** Struktur Folder Proyek**
 
```text
├── audio/
│   └── save-and-sound.mp3
├── countdown/
│   ├── simplyCountdown.min.js
│   └── simplyCountdown.theme.default.css
├── img/
│   ├── gallery/
│   │   ├── thumbnail/
│   │   │   ├── 1.png
│   │   │   ├── 2.png
│   │   │   ├── 3.png
│   │   │   ├── 4.png
│   │   │   ├── 5.png
│   │   │   └── 6.png
│   │   ├── 1.png
│   │   ├── 2.png
│   │   ├── 3.png
│   │   ├── 4.png
│   │   ├── 5.png
│   │   └── 6.png
│   ├── 1.png
│   ├── 2.png
│   ├── 3.png
│   ├── 4.png
│   ├── 5.png
│   ├── 6.png
│   ├── alex.png
│   ├── bg-prewed.jpg
│   ├── plaza.jpg
│   ├── sabrina.png
│   ├── saweria.png
│   ├── serius.jpg
│   └── tunangan.jpg
├── index.html
├── style.css
└── README.md
```

**Penjelasan Komponen Utama**

- audio/: Menyimpan aset suara untuk musik latar yang diputar saat tombol buka undangan diklik.
- countdown/: Berisi library JavaScript dan CSS pendukung untuk menampilkan hitung mundur waktu acara.
- img/: Berisi seluruh aset gambar, termasuk foto pasangan, latar belakang, foto galeri, serta barcode pembayaran/hadiah.
- index.html: Halaman web utama yang mencakup seluruh bagian (Hero, Profil, Story, Galeri, Informasi Acara, RSVP, dan Gift).
- style.css: Pengaturan tampilan kustom (warna, layout responsif, animasi, serta penyesuaian Bootstrap).

  
**Cara Penggunaan & Pemasangan**

- Clone Repositori Ini
    git clone https://github.com/username/repository-name.git
- Buka File index.html
    langsung di browser favorit Anda atau gunakan ekstensi Live Server di Visual Studio Code.

**Fitur Link Undangan Khusus Tamu**

Anda dapat mengirimkan link khusus ke tamu undangan agar nama mereka tertera langsung di halaman depan (hero section) dan terisi otomatis pada form RSVP.
Format URL:
- https://new-roan-five.vercel.app/?n=NamaTamu#home

**Konfigurasi Integrasi RSVP (Google Sheets)**

Formulir RSVP pada proyek ini memanfaatkan Google Apps Script sebagai webhook:

- Buat Google Sheets baru.
- Buka Extensions / Ekstensi > Apps Script.
- Tempelkan script penerima data POST dari form (seperti nama, jumlah, status).
- Deploy sebagai Web App dan setel akses ke "Anyone" (Siapa Saja).
- Salin URL Web App yang dihasilkan dan ganti atribut action pada <form id="my-form"> di index.html.

**Kredit & Lisensi**

- Desain & Pengembangan: @aldiokhasy.s_
- Dipublikasikan di bawah lisensi MIT. Bebas digunakan dan dimodifikasi untuk keperluan personal maupun komersial.
