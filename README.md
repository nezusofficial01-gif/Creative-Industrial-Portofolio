# Portfolio — Nabil Alfahmi Labib

Website portfolio Industrial Engineering / Manufacturing / Continuous Improvement.
Dibuat dengan HTML, CSS, dan JavaScript murni (tanpa framework, tanpa build tool), sehingga bisa langsung dipublikasikan di GitHub Pages.

## Struktur File

```
.
├── index.html      # Seluruh website (HTML + CSS + JS)
├── README.md       # Dokumen ini
└── assets/         # Gambar (buat folder ini sendiri)
    ├── foto-profil.jpg          # Foto di halaman awal (rasio 4:5)
    ├── 01-layout-1.jpg  ...-2  ...-3
    ├── 04-equipment-1.jpg ...-2 ...-3
    ├── 05-warehouse-1.jpg ...-2 ...-3
    ├── 03-vsm-1.jpg ...-2 ...-3
    └── 02-dashboard-1.jpg ...-2 ...-3
```

## Menjalankan Secara Lokal

Buka `index.html` langsung di browser. Tidak perlu instalasi apa pun.
Font dimuat dari Google Fonts, jadi diperlukan koneksi internet untuk tampilan font yang sesuai.

## Deploy ke GitHub Pages

1. Buat repository baru di GitHub (misalnya `portfolio`).
2. Upload `index.html`, `README.md`, dan folder `assets/`.
3. Buka **Settings → Pages**.
4. Pada **Build and deployment**, pilih **Deploy from a branch**, Branch `main`, folder `/ (root)`, lalu **Save**.
5. Tunggu 1–2 menit. Website tayang di `https://USERNAME.github.io/NAMA-REPO/`.

Untuk memperbarui website, edit file lalu commit. GitHub Pages akan memperbarui otomatis.

## Mengganti Konten

### Teks proyek

Buka `index.html`, cari `const P=[` di dalam tag `<script>`. Setiap proyek berisi:

| Field | Fungsi |
|---|---|
| `no` | Nomor proyek |
| `t` | Judul proyek |
| `cat` | Kategori |
| `st` | Label status yang tampil |
| `k` | Jenis untuk filter: `work`, `team`, atau `academic` |
| `d` | Deskripsi singkat di kartu |
| `r` | Peran singkat di kartu |
| `img` | Tiga path gambar (tiga kolom di samping slide) |
| `s` | Isi case study (per bagian) |

Pada `s`, bagian yang bernilai `null` akan menampilkan placeholder. Isi dengan teks (string) atau daftar (array) bila datanya sudah ada. Bagian yang tidak ada di `s` tidak akan ditampilkan.

### Teks lain

Hero, About, Experience, Skills, dan Contact ditulis langsung sebagai HTML biasa di bagian `<main>`. Cari teksnya dan edit.

### Warna

Semua warna ada di `:root` pada bagian `<style>`: `--blue` (#155687), `--ink`, `--mute`, `--tint`, `--line`.

## Menambahkan Foto dan Gambar

**Foto profil (halaman awal)**
1. Siapkan foto dengan rasio 4:5 (misalnya 800 x 1000 px), format JPG, di bawah 300 KB.
2. Simpan sebagai `assets/foto-profil.jpg` (atau `.png`, `.jpeg`, `.webp`; semuanya terbaca otomatis). Selama belum ada, tampil placeholder.

**Gambar proyek**
Format JPG, PNG, JPEG, dan WEBP dibaca otomatis, cukup samakan nama dasarnya. Setiap proyek tampil sebagai satu slide dengan tiga kolom gambar di sisi kanan. Simpan tiga gambar per proyek dengan nama sesuai nilai `img` pada data proyek, misalnya `assets/01-layout-1.jpg`, `-2`, `-3`.

- Tiap kolom berbentuk potret (rasio 3:5). Gambar dipotong otomatis agar pas. Untuk mengubah rasio, edit `aspect-ratio:3/5` pada `.imbox img` di bagian CSS.
- Teks "Gambar 1/2/3" di bawah kolom bisa diganti di fungsi `paint` pada JavaScript.

## Navigasi Slide

Berpindah slide dengan tombol panah, titik indikator, tombol panah keyboard (saat slide difokus), atau geser di layar sentuh. Penanda perpindahan: nomor sheet dan progress bar di bagian atas, garis biru yang menyapu slide, dan nomor project besar. Penanda juga muncul di judul tiap section (SECTION 02, 03, dst.).

## Logo

Logo software (SketchUp, AutoCAD, Google Sheets, Microsoft Office, WhatsApp, Gmail, LinkedIn, Google Drive) berasal dari Simple Icons (lisensi CC0) dan disisipkan langsung di `index.html`. Logo adalah merek dagang masing-masing pemiliknya dan hanya dipakai untuk menunjukkan software yang digunakan. ZW3D dan Looker Studio memakai ikon sederhana karena logo resminya tidak tersedia di sana. Untuk logo resmi, ganti isi `data-i` dengan elemen `<img>` Anda sendiri.

## Kerahasiaan Dokumen

Dokumen manufaktur dapat memuat informasi rahasia. Sebelum mengunggah gambar:

- Hapus atau blur nama pelanggan, nama perusahaan, kode part, dan data produksi internal.
- Sensor detail fasilitas dan drawing yang bersifat proprietary.
- Pastikan Anda berwenang mempublikasikan setiap gambar.

Nama perusahaan di halaman Experience saat ini sengaja ditulis netral. Ganti hanya jika sudah diizinkan.

## Checklist Sebelum Publikasi

- [ ] Link CV Google Drive terbuka dan aksesnya "Anyone with the link"
- [ ] Gambar proyek sudah disensor dan ditambahkan
- [ ] Semua teks "Belum ada data" sudah diisi atau dihapus
- [ ] Tidak ada angka hasil (penghematan, lead time, dll.) tanpa dokumen pendukung
- [ ] Link Email, WhatsApp, dan LinkedIn sudah dicoba
- [ ] Tampilan dicek di desktop dan HP

## Prinsip Konten

- Pekerjaan di tempat kerja, proyek tim, proyek akademik, dan solusi yang masih berupa rancangan dibedakan dengan jelas.
- Pada proyek tim, kontribusi pribadi dipisahkan dari hasil tim.
- Tidak ada klaim hasil terukur tanpa dokumentasi.

## Kontak

- Email: alfahmilabibnabil@gmail.com
- WhatsApp: https://wa.me/6285777324671
- LinkedIn: https://www.linkedin.com/in/nabil-alfahmi-labib-291751264/
