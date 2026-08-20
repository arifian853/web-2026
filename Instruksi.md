# Instruksi Penggunaan Git

Panduan singkat untuk menghubungkan project lokal ke repository cloud seperti GitHub.

## 1. Inisialisasi Repository Lokal

Buka terminal di folder project, lalu jalankan:

```bash
git init
```

Perintah ini membuat repository Git baru di dalam folder project.

## 2. Konfigurasi Git Pertama Kali

Langkah ini cukup dilakukan satu kali di komputer yang digunakan:

```bash
git config --global user.name "Nama Kamu"
git config --global user.email "email@example.com"
```

Periksa konfigurasi yang tersimpan dengan:

```bash
git config --list
```

## 3. Hubungkan ke Repository Cloud

Buat repository baru di GitHub, lalu hubungkan repository tersebut ke project lokal:

```bash
git remote add origin <link-repository>
```

Contoh:

```bash
git remote add origin https://github.com/username/nama-project.git
```

Pastikan remote sudah benar:

```bash
git remote -v
```

## 4. Masukkan File ke Staging Area

Tambahkan seluruh file project yang ingin di-commit:

```bash
git add .
```

## 5. Buat Commit

Simpan perubahan dengan pesan yang menjelaskan isi perubahan:

```bash
git commit -m "Tambahkan halaman utama"
```

## 6. Push ke Repository Cloud

Kirim commit ke branch repository. Gunakan nama branch yang sesuai, misalnya `main` atau `master`:

```bash
git push -u origin main
```

Untuk push berikutnya, perintahnya dapat digunakan tanpa opsi `-u`:

```bash
git push origin main
```

## Catatan Autentikasi

Jika GitHub meminta password saat menggunakan HTTPS, gunakan **Personal Access Token (PAT)** sebagai pengganti password biasa. Jangan menuliskan token di dalam file project atau membagikannya kepada orang lain.

## Alur Singkat

```bash
git init
git config --global user.name "Nama Kamu"
git config --global user.email "email@example.com"
git remote add origin <link-repository>
git add .
git commit -m "Pesan commit"
git push -u origin main
```
