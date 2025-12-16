# MusicAppCLI (CLI Music Player with Audio)

MusicAppCLI adalah aplikasi *pemutar musik berbasis Command Line Interface (CLI)* yang dikembangkan menggunakan bahasa pemrograman *Python*.  
Aplikasi ini mampu *memutar file audio (.mp3) secara langsung* menggunakan library `pygame` serta mendukung pengelolaan lagu dan playlist.

Aplikasi ini menerapkan beberapa struktur data seperti *Doubly Linked List, Stack, dan Binary Search Tree (BST)* untuk mendukung fitur pencarian dan navigasi lagu.
MusicAppCLI dirancang untuk membantu pengguna mengelola koleksi lagu dan playlist melalui terminal.  
Aplikasi memiliki dua peran pengguna:

- **Admin** → Mengelola data lagu
- **User** → Mengelola playlist dan memutar lagu

File lagu disimpan dalam folder `songs/` dengan format nama: `<ID_LAGU>.mp3`

---

## Fitur Aplikasi

### Mode Admin
- Login admin
- Melihat seluruh lagu
- Menambahkan lagu baru
- Mengubah data lagu
- Menghapus lagu
- Penyimpanan data lagu ke file Excel

Password admin default: `admin123`

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
- Play
- Stop
- Next
- Prev

Pemutaran lagu menggunakan **pygame.mixer** dan mendukung file audio `.mp3`.

---

## Struktur Data yang Digunakan

- **Doubly Linked List**  
  Digunakan untuk menyimpan urutan lagu di library dan playlist

- **Binary Search Tree (BST)**  
  Digunakan untuk pencarian lagu berdasarkan judul

- **Stack**  
  Digunakan sebagai riwayat pemutaran lagu (fitur Prev)

---

## Penyimpanan Data

Data aplikasi disimpan menggunakan file Excel dengan library `openpyxl`:

- `songs.xlsx` → data lagu
- `playlists.xlsx` → daftar playlist
- `playlist_songs.xlsx` → relasi playlist dan lagu

---

## Struktur Folder

```markdown
project/
│── FinalTugbes+Lagu.py
│── database/
│   ├── songs.xlsx
│   ├── playlists.xlsx
│   └── playlist_songs.xlsx
│── Songs/
│   ├── S001.mp3
│   └── S002.mp3
│   ├── S003.mp3
│   └── S004.mp3
...
```
## Cara Menjalankan Program

### 1️. Persyaratan
- Python **3.8 atau lebih baru**
- File lagu berformat `.mp3`
- Nama file lagu harus sesuai dengan `song_id` di `songs.xlsx`

### 2️. Instalasi Dependency
Install library yang dibutuhkan:
```bash
pip install openpyxl 
pip install pygame
```

---

## Daftar Anggota Kelompok
1. Aghna Shava Akyela Wahjudi - (103102400028)

2. Luluk Nabilah Putri - (103102400057)

3. Amanda Faiza Agustin - (103102400060)


