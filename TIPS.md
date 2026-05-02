# 📘 Latihan Pertama: Distribusi Normal

Misalkan Anda ingin membuat catatan tentang Distribusi Normal. Berikut adalah urutan langkah yang bisa Anda coba sekarang juga sebagai latihan pertama:

---

## 1. Persiapan "Ruang Galeri" (di GitHub)

- Buka akun GitHub Anda di browser.
- Klik tombol New (atau ikon + di pojok kanan atas) untuk membuat Repository.
- Beri nama: `latihan-pertama`.
- Centang "Add a README file".
- Klik Create repository.

Sekarang Anda punya satu folder kosong di "awan" (GitHub).

---

## 2. Menghubungkan ke "Meja Kerja" (di Komputer)

Sekarang, kita ingin agar folder di awan itu ada di komputer Anda.

- Di halaman repositori tadi, klik tombol hijau **Code**, lalu salin (copy) alamatnya (yang berakhir dengan `.git`).
- Buka folder di komputer Anda di mana Anda ingin menyimpan tugas ini.
- Klik kanan di folder tersebut, pilih **Git Bash Here** (karena Anda sudah instal Git).
- Ketik perintah ini:

```bash
git clone [tempel-alamat-tadi-di-sini]
git clone https://github.com/namaanda/latihan-pertama.git
```
# ✨ Perintah Sakti

Buka Git Bash di dalam folder tersebut dan ketik 3 perintah ini secara berurutan:

## 🧾 Perfile
```bash
git add README.md
git commit -m "Menambahkan penjelasan rumus matematika di README"
git push
```
Bash (TANDA TITIK BERARTI SEMUA)

```
git add .
git commit -m "menambahkan grafik hasil model"
git push
```
Cara pull dari web ke komputer
```
git pull origin main
```
## Cek Perubahan 

Sebelum kita mengirimnya, mari gunakan satu perintah baru yang sangat berguna untuk mengecek apa yang sedang terjadi. Buka **Git Bash** (pastikan posisinya sudah di dalam folder `latihan-pertama` dan ada tanda `(main)` atau `(master)`), lalu ketik:

Bash

```
git status
```

_Anda akan melihat tulisan berwarna merah bertuliskan `modified: analisis.md`. Git sangat pintar, dia tahu bahwa file tersebut baru saja Anda ubah dan belum disimpan ke sistemnya._

## SHORTCUT
### Jalan Pintas: Langsung Commit

Jika Anda malas mengetik `git add` satu per satu, Anda bisa menggabungkan perintahnya dengan menambahkan kode `-a` (artinya _all_) pada saat commit.

Ketik perintah ini di Git Bash:

Bash

```
git commit -am "catatan perubahan anda"
```

- **`-a`**: Secara otomatis melakukan "add" untuk semua file yang **sudah pernah terdaftar** di Git sebelumnya.
    
- **`-m`**: Pesan commit Anda.
    

> **Peringatan Penting:** Jalan pintas ini **tidak akan berhasil** untuk file yang baru saja Anda buat (file baru). File baru tetap harus di-`add` secara manual satu kali agar Git mulai "mengenali" keberadaannya.


### Cara Men-track (Melihat Jejak)
- **Lewat GitHub (Visual):** Klik tulisan **"Commits"** di halaman depan repositori Anda. GitHub akan menampilkan daftar semua "foto" (snapshot) yang pernah Anda ambil, siapa yang mengubahnya, dan apa catatannya.
    
- **Lewat Git Bash (Teks):** Ketik perintah ini untuk melihat daftar riwayat di komputer Anda:
    
    Bash
    
    ```
    git log --oneline
    ```
    
    _Anda akan melihat daftar kode unik dan pesan commit Anda dari yang terbaru ke yang terlama._

### Buat Cabang Baru
Ketik di Git Bash:
    
    Bash
    
    ```
    git checkout -b eksperimen-rumus
    ```
    
    _(Sekarang Anda berada di dunia "eksperimen-rumus". Tanda di Git Bash akan berubah dari `(main)` menjadi `(eksperimen-rumus)`)._
    
2. **Lakukan Perubahan:** Buka `analisis.md`, ubah rumusnya sesuka hati, lalu simpan.
    
3. **Simpan di Cabang Tersebut:**
    
    Bash
    
    ```
    git add .
    git commit -m "mencoba rumus alternatif yang lebih kompleks"
    ```
    
4. **Kembali ke Dunia Aman (Main):**
    
    Bash
    
    ```
    git checkout main
    ```
    
    _Ajaib! Buka file `analisis.md` Anda sekarang. Rumus kompleks tadi menghilang dan file kembali ke versi aman. Itulah kekuatan Branch._
    

---

### Kapan Peneliti Menggunakan Branch?

- **Mencoba Algoritma Baru:** Satu cabang untuk GRU biasa, satu cabang untuk GRU dengan optimasi berbeda.
    
- **Pembersihan Data:** Satu cabang untuk mencoba teknik _imputation_ data yang berbeda.
    
- **Revisi Dosen:** Membuat cabang khusus untuk mengerjakan revisi tanpa menghapus draf asli Anda.
## GAMBAR
**Letak Gambar:** Secara otomatis, gambar akan diletakkan di sebelah kiri. Jika Anda ingin gambar berada di tengah (center), Anda bisa menggunakan sedikit kode HTML di dalam file `.md` Anda seperti ini:

HTML

```
<p align="center">
  <img src="images/grafik_gru.png" width="500">
</p>
```
# FOLDER
- **Cek daftar folder yang ada:** Ketik perintah ini untuk melihat ada folder apa saja di posisi Anda sekarang:
    
    Bash
    
    ```
    ls
    ```
    
    _(Anda akan melihat nama folder penelitian Anda muncul di sana)._
    
- **Masuk ke dalam folder penelitian:** Gunakan perintah `cd` (_Change Directory_). Misalnya nama folder yang Anda buat tadi adalah `Analisis-Skripsi`, maka ketik:
    
    Bash
    
    ```
    cd Analisis-Skripsi
    ```
    
    _(**Tips:** Ketik `cd` lalu tulis 3-4 huruf awal folder Anda dan tekan tombol **Tab** di keyboard, maka Git Bash akan otomatis melengkapi namanya untuk Anda)._
    
- **Perhatikan tandanya:** Jika Anda sudah berada di folder yang benar, di layar Git Bash Anda biasanya akan muncul teks berwarna biru atau kuning di ujung baris yang bertuliskan **`(main)`** atau **`(master)`**. Itu adalah tanda bahwa Git sudah "siap tempur".
