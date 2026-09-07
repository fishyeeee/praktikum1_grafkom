# Graphics Playground 🎮

Graphics Playground adalah aplikasi web interaktif berbasis **HTML5 Canvas** yang dibuat untuk mendemonstrasikan konsep dasar Grafika Komputer, seperti sistem koordinat 2D, primitive drawing, pewarnaan, animasi, keyboard interaction, mouse interaction, boundary checking, dan collision detection.

## 📌 Deskripsi

Aplikasi ini menampilkan beberapa objek grafis dasar pada sebuah canvas berukuran **720 × 460 pixel**. Selain menampilkan primitive seperti rectangle, line, circle, dan triangle, aplikasi memiliki elemen interaktif berupa player, bola yang bergerak otomatis, serta mini-game **Collector Mini-Game**.

Pada challenge tersebut, player harus digerakkan untuk mengambil coin. Setiap coin yang berhasil diambil akan menambah skor dan menghasilkan coin baru pada posisi acak.

## ✨ Fitur

- Menampilkan primitive grafis:
  - Rectangle
  - Line
  - Circle
  - Triangle
- Sistem koordinat 2D dan grid pada canvas
- Player berbentuk persegi yang dapat digerakkan
- Bola yang bergerak dan memantul pada batas canvas
- Pergantian warna player
- Pause dan resume animasi
- Reset posisi player dan skor
- Mouse coordinate display
- Spawn coin melalui klik mouse
- Collision detection antara player dan coin
- Sistem skor pada Collector Mini-Game
- Boundary checking agar player tetap berada di dalam canvas

## 🎮 Kontrol

| Input | Fungsi |
|---|---|
| `W` / `↑` | Bergerak ke atas |
| `A` / `←` | Bergerak ke kiri |
| `S` / `↓` | Bergerak ke bawah |
| `D` / `→` | Bergerak ke kanan |
| `C` | Mengganti warna player |
| `R` | Reset posisi player dan skor |
| `Space` | Pause / resume animasi |
| Klik canvas | Spawn coin pada posisi mouse |

Player dapat bergerak secara diagonal dengan menekan dua tombol arah secara bersamaan.

## 🧩 Konsep Grafika Komputer

### 1. Coordinate System

Canvas menggunakan sistem koordinat 2D dengan titik `(0, 0)` berada di pojok kiri atas. Posisi objek disimpan menggunakan koordinat `x` dan `y`.

### 2. Primitive Drawing

Beberapa primitive dasar yang digunakan:

- **Rectangle** menggunakan `fillRect()` dan `strokeRect()`
- **Line** menggunakan `moveTo()` dan `lineTo()`
- **Circle** menggunakan `arc()`
- **Triangle** dibentuk menggunakan tiga titik koordinat melalui path

### 3. Animation

Animasi menggunakan `requestAnimationFrame()` untuk menjalankan game loop secara berulang. Pada setiap frame, posisi objek diperbarui kemudian seluruh canvas digambar kembali.

### 4. Keyboard Interaction

Movement player menggunakan pendekatan **state-based input**, sehingga tombol yang sedang ditekan disimpan dan diperiksa pada setiap frame.

Tombol `C`, `R`, dan `Space` menggunakan **event-based input** untuk aksi yang dilakukan ketika tombol ditekan.

### 5. Mouse Interaction

Posisi mouse dihitung relatif terhadap canvas dan ditampilkan pada Info Panel. Klik pada canvas digunakan untuk membuat coin baru pada posisi yang diklik.

### 6. Boundary Checking

Posisi player dibatasi agar tidak keluar dari area canvas. Bola juga menggunakan pengecekan batas untuk menghasilkan efek bouncing.

### 7. Collision Detection

Collision detection digunakan untuk mengetahui apakah player menyentuh coin. Ketika terjadi collision:

1. Skor bertambah 1.
2. Skor diperbarui pada Info Panel.
3. Coin baru dibuat pada posisi acak.

## 🛠️ Teknologi

- HTML5
- CSS3
- JavaScript
- HTML5 Canvas 2D API

Project ini tidak membutuhkan framework atau library eksternal.

## 📁 Struktur Project

```text
.
└── index.html
```

Seluruh HTML, CSS, dan JavaScript berada dalam satu file sehingga project dapat dijalankan secara langsung melalui browser.


## 🎯 Challenge

### Collector Mini-Game

Tujuan challenge adalah menggerakkan player untuk mengumpulkan coin yang muncul di dalam canvas.

Setiap kali player bertabrakan dengan coin, skor bertambah dan coin berikutnya muncul secara otomatis.
