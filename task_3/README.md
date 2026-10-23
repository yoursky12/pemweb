# TASK 3

* **Nama:** Frichintia Niken Gita Natasyah
* **NIM:** 124140106
* **Link Repository GitHub:** https://github.com/yoursky12/pemweb.git

---

## Tampilan Halaman Web (Screenshot)

### 1. Halaman Form Pendaftaran (`index.html`)
![alt text](image.png)

### 2. Halaman Detail Informasi Pendaftar (`informasi.html`)
![alt text](image-1.png)

---

## A. Penjelasan Kode `index.html`

1. **Struktur Utama & Header**
   * `<div class="card">` berfungsi sebagai wadah (*container*) utama tampilan pendaftaran
   * `<h2 id="form-title">` dan `<span class="sub-header">` menampilkan judul utama halaman serta keterangan nama tugas.

2. **Formulir Pendaftaran (`<form>`)**
   * `<form action="informasi.html" method="GET">` membuat formulir untuk mengirimkan data ke halaman `informasi.html`.
   * `method="GET"` menetapkan metode pengiriman data melalui URL dalam bentuk *query string*.

3. **Input Nama Lengkap & NIM**
   * `<label>` memberikan keterangan untuk setiap kolom input.
   * Input `nama` dan `nim` menggunakan `type="text"` untuk menerima masukan berupa teks atau angka dari pengguna.
   * Atribut `required` memastikan kolom wajib diisi sebelum formulir dapat dikirimkan.
   * Atribut `placeholder` menampilkan contoh teks petunjuk pengisian di dalam kolom.

4. **Input Email & Password**
   * `type="email"` digunakan untuk memasukkan alamat email dan memungkinkan browser memeriksa format email saat formulir dikirim.
   * `type="password"` digunakan untuk menyembunyikan karakter yang diketik oleh pengguna demi keamanan.

5. **Tombol Submit**
   * `<button type="submit" id="btn-submit">` membuat tombol pendaftaran yang berfungsi untuk mengirimkan seluruh data formulir ke halaman tujuan.

---

## B. Penjelasan Kode `informasi.html`

1. **Layout Container & Kolom**
   * `<div class="FormContainer">` membagi halaman menjadi dua bagian (*layout* 2 kolom), yaitu `.FormLeft` untuk informasi status pendaftaran dan `.FormRight` untuk menampilkan detail data mahasiswa.

2. **Tabel Detail Mahasiswa (`<table>`)**
   * `<table>` dengan kelas `.InfoTable` digunakan untuk menampilkan data pendaftar secara terstruktur.
   * `<th>` membuat sel judul kolom (*Kategori* dan *Detail Informasi*).
   * `<td>` menampilkan sel data biasa yang berisi ikon `Boxicons` beserta rincian informasi pendaftar (Nama Lengkap, NIM, Email, Jenis Kelamin, Prodi, dan Alamat).

3. **Status Pendaftaran & Tombol Kembali**
   * `<div class="info-box">` menampilkan kotak keterangan status verifikasi pendaftaran mahasiswa.
   * `<a href="index.html" class="back-button">` membuat tautan berbentuk tombol yang mengarahkan pengguna kembali ke halaman utama `index.html`.

---

## C. Penjelasan Kode `style.css`

1. **Element Selector**
   * `body`: Mengatur jenis huruf (*font*), warna latar belakang, serta memosisikan konten agar tepat berada di tengah layar (*flexbox*).
   * `label`: Mengatur tampilan teks label kolom input agar cetak tebal dan berwarna abu-abu.
   * `table`, `th`, `td`: Mengatur lebar tabel 100%, menghilangkan jarak antar sel (*border-collapse*), serta memberi garis pembatas antar baris data.

2. **Class Selector**
   * `.card`: Mengatur wadah form pada `index.html` dengan latar putih, batas tipis, dan efek bayangan (*box-shadow*).
   * `.FormContainer`: Mengatur tata letak kotak 2 kolom pada `informasi.html`.
   * `.FormLeft` & `.FormRight`: Mengatur panel kiri berwarna hitam dan panel kanan berisi tabel informasi.
   * `.form-group`: Memberikan jarak antar kolom input pada formulir.
   * `.back-button`: Mengubah tampilan tautan kembali menjadi tombol dengan garis pembatas tegas.

3. **ID Selector**
   * `#form-title`: Mengatur ukuran, ketebalan, dan warna judul utama formulir.
   * `#btn-submit`: Mengatur desain tombol *submit* berwarna hitam penuh dengan efek perubahan tingkat transparansi (*opacity*) saat kursor diarahkan ke atasnya (*hover*).