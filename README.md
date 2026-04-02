# SNBT Generator (FAKE) 2026

Generator tampilan pengumuman hasil SNBT untuk simulasi desain, konten kreatif, dan latihan front-end.

## Disclaimer
- Proyek ini bukan website resmi SNPMB.
- Hanya untuk simulasi, hiburan, dan pembelajaran.
- Dilarang digunakan untuk tindakan penipuan/pemalsuan.

## Fitur Utama
- Mode hasil `Lulus (biru)` / `Tidak Lulus (merah)`.
- Input data peserta:
  - Nomor peserta
  - Nama
  - Tanggal lahir
  - Kode/Nama kampus
  - Kode/Nama prodi
- Randomize nomor peserta.
- QR code pada kartu hasil.
- Tombol sosial:
  - Instagram
  - LinkedIn
- Popup konfirmasi custom (Uiverse style) dengan tombol `YA` / `TIDAK`.
- Pada layar kecil, menu otomatis disembunyikan setelah `GENERATE` agar fokus ke hasil.

## Teknologi
- HTML
- CSS
- JavaScript (vanilla)
- Library QR code (`../snbp-fake/qrcode-engine-snbt.js`)

## Dependensi Antar Folder
Halaman ini memakai beberapa file dari folder `snbp-fake`:
- `../snbp-fake/ui-shell.css`
- `../snbp-fake/vendor-grid.min.css`
- `../snbp-fake/qrcode-engine-snbt.js`

Pastikan struktur folder tetap sejajar seperti ini:

```text
repo-root/
  snbp-fake/
  snbt-generator/
```

## Struktur File Penting
- `index.html` -> halaman utama SNBT generator
- `js_snbt.js` -> logic input, popup custom, action tombol, generate + auto-hide menu mobile
- `css-snbt.css` -> styling kartu hasil SNBT
- `../snbp-fake/logo-snpmb.png` -> logo pada header hasil (diambil dari folder snbp-fake)
- `image.png` -> favicon

## Menjalankan Secara Lokal
1. Pastikan folder `snbp-fake` dan `snbt-generator` berada dalam parent yang sama.
2. Buka:
   - `snbt-generator/index.html`
3. Isi data peserta lalu klik `GENERATE`.

## Deploy ke GitHub Pages
Deploy dari root repository agar path relatif antar-folder tetap valid.

Endpoint yang dipakai:
- `/snbt-generator/`
- `/snbp-fake/`

## Catatan Pengembangan
- Jika ingin ubah teks popup sosial:
  - `alertAuthor()`
  - `alertLinkedIn()`
- Jika ingin ubah perilaku tombol generate mobile:
  - `generateThenAutoHideMenu()` di `js_snbt.js`
