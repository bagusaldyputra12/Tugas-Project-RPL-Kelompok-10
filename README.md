# Sistem Informasi Pelaporan Kerusakan Fasilitas Gerai Alfamidi

Aplikasi web sederhana untuk simulasi pelaporan dan pengelolaan kerusakan fasilitas pada gerai Alfamidi. Aplikasi menyediakan tampilan dan menu berdasarkan peran pengguna, yaitu **Pelapor**, **Admin**, dan **Teknisi**.

## 1. Fitur Aplikasi

Fitur yang tersedia pada aplikasi meliputi:

- Login berdasarkan akun dan peran pengguna.
- Dashboard ringkasan.
- Pelapor: membuat laporan kerusakan dan melihat laporan miliknya.
- Admin: mengelola laporan, data master, statistik dan analisis, serta profil.
- Teknisi: melihat tugas perbaikan dan riwayat penanganan.
- Penyimpanan data pada browser menggunakan `localStorage`.
- Pengaturan tampilan tema terang/gelap.

> **Catatan:** Versi pada repositori ini merupakan aplikasi sisi-klien (frontend). Data disimpan di browser masing-masing melalui `localStorage`; belum menggunakan server backend atau database terpusat. Karena itu, data tidak otomatis tersinkron antarperangkat atau antarbrowser.

## 2. Teknologi yang Digunakan

- HTML5 untuk struktur halaman.
- CSS3 untuk tampilan.
- JavaScript untuk interaksi dan pengelolaan data di sisi browser.
- Chart.js untuk grafik statistik.
- Lucide Icons untuk ikon.
- Google Fonts (Inter) untuk jenis huruf.

Chart.js, Lucide Icons, dan Google Fonts dimuat dari CDN sehingga koneksi internet diperlukan agar seluruh elemen eksternal tersebut dapat dimuat.

## 3. Persyaratan Menjalankan Aplikasi

- Komputer atau laptop.
- Browser modern, seperti Google Chrome, Microsoft Edge, atau Mozilla Firefox.
- Visual Studio Code (disarankan, tetapi tidak wajib).
- Ekstensi **Live Server** pada VS Code (disarankan).
- Koneksi internet untuk memuat library dan font dari CDN.

## 4. Cara Menjalankan Aplikasi

### Cara A — Menggunakan Live Server (disarankan)

1. Unduh atau salin folder project ke komputer.
2. Ekstrak file ZIP jika project masih berbentuk ZIP.
3. Buka Visual Studio Code.
4. Pilih **File → Open Folder**.
5. Pilih folder `TUGAS PROYEK RPL KELOMPOK 10` yang berisi `index.html`, `style.css`, dan `script.js`.
6. Pastikan ekstensi **Live Server** sudah terpasang. Jika belum, buka Extensions (`Ctrl + Shift + X`), cari `Live Server`, lalu instal.
7. Klik kanan file `index.html`.
8. Pilih **Open with Live Server**.
9. Browser akan terbuka dan menampilkan halaman login aplikasi.

### Cara B — Membuka langsung melalui browser

1. Buka folder project.
2. Klik dua kali file `index.html`, atau klik kanan lalu pilih browser.
3. Halaman aplikasi akan terbuka.

Jika ada fitur atau tampilan yang tidak termuat dengan benar, jalankan kembali menggunakan Live Server dan pastikan koneksi internet aktif.

## 5. Akun Demo untuk Login

Gunakan salah satu akun bawaan berikut untuk mencoba aplikasi.

| Peran | Email | Password |
|---|---|---|
| Admin | `admin@alfamidi.com` | `admin123` |
| Pelapor | `pegawai@alfamidi.com` | `pegawai123` |
| Teknisi | `teknisi@alfamidi.com` | `teknisi123` |
| Teknisi | `andi@alfamidi.com` | `teknisi123` |

Setiap akun akan diarahkan ke menu sesuai perannya. Akun dan data awal tersebut didefinisikan di dalam `script.js`.

**Penting:** Akun di atas adalah akun demo untuk keperluan pengujian, bukan akun produksi. Jangan gunakan password tersebut untuk layanan lain.

## 6. Susunan Folder dan File

Susunan folder project yang benar adalah sebagai berikut:

```text
TUGAS PROYEK RPL KELOMPOK 10/
│
├── index.html
│
├── style.css
│
├── script.js
│
├── README.md
│
└── alfamidi-vector-logo-seeklogo/
    └── Logo Alfamidi.png
```

### Fungsi setiap file dan folder

| File/Folder | Keterangan |
|---|---|
| `index.html` | Halaman utama aplikasi, berisi struktur HTML, form login, area aplikasi, dan pemanggilan file CSS serta JavaScript. |
| `style.css` | Mengatur desain, warna, tata letak, responsivitas, dan tampilan komponen aplikasi. |
| `script.js` | Mengatur proses login, navigasi menu, data demo, interaksi, dan penyimpanan data pada `localStorage`. |
| `README.md` | Dokumentasi project dan panduan menjalankan aplikasi. |
| `alfamidi-vector-logo-seeklogo/` | Folder aset gambar logo yang digunakan pada halaman login. |
| `Logo Alfamidi.png` | Gambar logo yang ditampilkan pada aplikasi. |

**Jangan memisahkan** `index.html`, `style.css`, `script.js`, dan folder logo dari susunan tersebut. Nama file dan folder sebaiknya tetap sama karena sudah dipanggil melalui alamat relatif di dalam kode.

## 7. Penyimpanan dan Reset Data

Aplikasi menggunakan `localStorage` browser untuk menyimpan data dan sesi. Data tersimpan pada browser dan perangkat yang digunakan.

Untuk mengakhiri sesi, klik tombol **Logout** pada aplikasi.

Jika ingin menghapus seluruh data lokal aplikasi untuk memulai pengujian dari kondisi awal:

1. Buka aplikasi di browser.
2. Tekan `F12` untuk membuka Developer Tools.
3. Pilih tab **Application** (pada sebagian browser berada di bagian **Storage**).
4. Buka **Local Storage**, lalu pilih alamat halaman aplikasi.
5. Hapus data yang tersimpan untuk halaman tersebut, atau jalankan perintah berikut pada tab **Console**:

```javascript
localStorage.clear();
location.reload();
```

Perintah tersebut menghapus seluruh `localStorage` untuk origin/halaman yang sedang dibuka, bukan hanya data aplikasi ini. Gunakan hanya jika memang ingin mereset data pengujian.

## 8. Troubleshooting

- **Halaman tidak tampil sempurna:** pastikan file `style.css` dan `script.js` berada satu folder dengan `index.html`.
- **Logo tidak muncul:** pastikan folder `alfamidi-vector-logo-seeklogo` dan file `Logo Alfamidi.png` tidak dipindahkan atau diubah namanya.
- **Ikon atau grafik tidak muncul:** periksa koneksi internet karena library dimuat dari CDN.
- **Login gagal:** periksa kembali email dan password demo pada tabel akun.
- **Data sebelumnya masih muncul:** data mungkin masih tersimpan di `localStorage`; lakukan reset sesuai langkah pada bagian 7 jika ingin memulai dari awal.

## 9. Pengembangan Selanjutnya

Untuk penggunaan nyata, aplikasi masih perlu dikembangkan dengan backend, database terpusat, autentikasi yang aman, pengelolaan hak akses di sisi server, serta mekanisme unggah dan penyimpanan berkas yang sesuai. Penyimpanan password dan data pengguna di sisi browser pada versi demo ini tidak ditujukan untuk lingkungan produksi.

---

**Project:** Sistem Informasi Pelaporan Kerusakan Fasilitas Gerai Alfamidi  
**Kelompok:** 10  
