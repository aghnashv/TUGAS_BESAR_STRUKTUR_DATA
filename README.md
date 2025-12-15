# MusicAppCLI — Aplikasi Pemutar Musik Berbasis CLI (Python)

MusicAppCLI adalah aplikasi pemutar musik berbasis *Command Line Interface* (CLI) yang dibuat menggunakan bahasa pemrograman Python. Aplikasi ini mendukung manajemen lagu, playlist, pencarian lagu, serta simulasi pemutaran musik dengan penerapan berbagai struktur data.

## Fitur Utama

### Mode Admin
- Login admin dengan password
- Menambahkan lagu ke library
- Melihat seluruh lagu
- Mengubah data lagu
- Menghapus lagu dari library
- Data tersimpan otomatis ke file Excel

Password admin default:
admin123

### Mode User
- Membuat playlist
- Menambahkan lagu ke playlist
- Menghapus lagu dari playlist
- Melihat playlist
- Menghapus playlist
- Mencari lagu berdasarkan artis
- Mencari lagu berdasarkan judul
- Memutar lagu dari library
- Memutar lagu dari playlist

### Player Control
- Stop
- Next
- Prev (riwayat pemutaran)

## Struktur Data yang Digunakan

1. **Doubly Linked List**
   - Menyimpan urutan lagu di library
   - Menyimpan lagu di playlist
   - Mendukung navigasi next dan prev

2. **Binary Search Tree (BST)**
   - Digunakan untuk pencarian lagu berdasarkan judul
   - Key berupa judul lagu (lowercase)
   - Value berupa list song_id

3. **Stack**
   - Digunakan sebagai history pemutaran lagu
   - Mendukung fitur Prev

## Penyimpanan Data

Data disimpan menggunakan file Excel dengan library openpyxl:
- `songs.xlsx` : menyimpan data lagu
- `playlists.xlsx` : menyimpan daftar playlist
- `playlist_songs.xlsx` : menyimpan relasi playlist dan lagu

Semua file disimpan di dalam folder `database`.

## Struktur Folder

```markdown
project/
│── Final_Tugbes.py
│── database/
│   ├── songs.xlsx
│   ├── playlists.xlsx
│   └── playlist_songs.xlsx
```

## Cara Menjalankan Program

1. Pastikan Python versi 3.8 atau lebih baru sudah terinstal
2. Install dependency:
   `pip install openpyxl`
3. Jalankan program:
   `python Final_Tugbes.py`

## Menu Utama

1. Login Admin
2. Login User
0. Keluar

## Menu Admin

1. Tambah Lagu
2. Lihat Semua Lagu
3. Ubah Data Lagu
4. Hapus Lagu
0. Kembali

## Menu User

1. Buat playlist
2. Tambah lagu ke playlist
3. Hapus lagu dari playlist
4. Lihat playlist
5. Cari lagu
6. Play lagu dari library
7. Play lagu dari playlist
8. Hapus playlist
0. Kembali

## Pencarian Lagu

- Cari berdasarkan artis (substring)
- Cari berdasarkan judul:
  - Pencarian exact menggunakan BST
  - Jika tidak ditemukan, menggunakan substring search
