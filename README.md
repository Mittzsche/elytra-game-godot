# Elytra - Space Shooter Game

[![Godot Engine](https://img.shields.io/badge/Godot_Engine-4.x-blue.svg)](https://godotengine.org/)
[![C++](https://img.shields.io/badge/Language-C%2B%2B-blue.svg)](https://isocpp.org/)
[![GDExtension](https://img.shields.io/badge/Godot_GDExtension-v4.x-green.svg)](https://docs.godotengine.org/en/4.4/tutorials/scripting/gdextension/gdextension_cpp_example.html)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

**Elytra** adalah game bergenre *space shooter* yang dikembangkan menggunakan **Godot Engine 4.x** dan **bahasa pemrograman C++** melalui sistem **GDExtension**. Dalam game ini, pemain mengendalikan sebuah pesawat luar angkasa untuk menembak musuh dan menghindari berbagai rintangan. Proyek ini merupakan studi kasus pengembangan game sederhana berbasis open-source yang mengintegrasikan performa tinggi dari C++ dengan fleksibilitas engine Godot.

---

## 🎮 Deskripsi Game

Elytra berlatar di luar angkasa dengan gaya seni **pixel art**. Pemain mengontrol pesawat kecil berwarna biru-ungu untuk menghadapi gelombang musuh berupa pesawat, asteroid, hingga bos raksasa.

### 🧠 Fitur Utama

* **Musuh beragam**: termasuk pesawat musuh, asteroid, dan bos (seperti "GARGANTUA").
* **Antarmuka intuitif**:

  * Health bar dengan blok hijau solid.
  * Skor dinamis (`SCORE:`) dan skor tertinggi (`HIGH:`).
  * Ikon skill heksagonal: perisai, boost, dan serangan khusus.
* **Beberapa layar utama**:

  * Menu Utama: `PLAY`, `SETTINGS`, `CREDITS`, `QUIT`
  * Pengaturan: fullscreen dan kontrol volume
  * Credits: menampilkan nama dan peran pengembang
  * Victory dan Game Over: menampilkan skor akhir dan opsi `RETRY` / `MAIN MENU`

---

## 🛠️ Teknologi yang Digunakan

* **Game Engine**: [Godot Engine 4.x](https://godotengine.org/)
* **Bahasa Pemrograman**: C++ (untuk logika dan optimasi performa)
* **Ekstensi**: GDExtension (integrasi C++ native ke Godot Engine)

---

## 🗂️ Struktur Proyek

```
ELYTRA/
├── .godot/            # File internal Godot
├── assets/            # Asset (sprite, audio, font)
├── bin/               # Output binary hasil kompilasi GDExtension
├── demo/              # Scene utama dan logika berbasis Godot
├── entities/          # Entitas game (player, enemy)
├── model/             # File besar seperti musik
├── script/            # Skrip tambahan
├── src/               # Kode sumber C++ (GDExtension)
├── ui/                # Komponen UI
├── world/             # Scene dunia dan level
├── project.godot      # File utama proyek Godot
└── elytra.gdextension # Konfigurasi GDExtension
```

---

## ▶️ Cara Menjalankan Game

1. **Unduh Godot Engine 4.x**
   [Download di sini](https://godotengine.org/download/)

2. **Kloning repositori ini**:

   ```bash
   git clone https://github.com/Mittzsche/elytra-game-godot.git
   cd elytra-game-godot
   ```

3. **Setup GDExtension (C++)**
   Lanjut ke bagian [pengembangan](#️cara-mengembangkan-setup-gdextension-c) untuk langkah-langkahnya.

4. **Buka proyek di Godot**
   Buka `project.godot` dari editor Godot.

5. **Tekan Play** (ikon ▶️) untuk menjalankan game.

---

## 🔧 Cara Mengembangkan (Setup GDExtension C++)

Untuk menjalankan kode C++ di Godot, proyek ini menggunakan [`godot-cpp`](https://github.com/godotengine/godot-cpp). Langkah setup:

### 1. Kloning `godot-cpp`:

```bash
git clone --recursive https://github.com/godotengine/godot-cpp src/godot-cpp
```

> Opsi `--recursive` wajib agar submodul ikut terunduh.

### 2. Kompilasi Binding:

Pastikan sudah menginstal `scons`.

```bash
# Untuk Arch Linux
sudo pacman -S scons

# Lalu compile:
cd src/godot-cpp
scons platform=linux generate_bindings=yes
```

> Ganti `platform` sesuai OS Anda (`windows`, `linux`, `macos`).

### 3. Kompilasi Kode C++ Game:

```bash
cd ../../
scons platform=linux
```

Library hasil kompilasi akan muncul di `bin/`, dan digunakan otomatis oleh `elytra.gdextension`.

---

## 🎓 Catatan Akademik

Game ini dikembangkan sebagai bagian dari proyek tugas akhir matakuliah *Teknik Pemrograman Terstruktur 2* di **Universitas Gunadarma**. Dokumen lengkap pengembangannya dapat ditemukan pada [makalah ini](https://github.com/Mittzsche/elytra-game-godot/blob/main/Makalah%20Pengaplikasian%20C%2B%2B%20-%20Game.docx).

---

## 📄 Lisensi

Proyek ini dilisensikan di bawah [MIT License](https://opensource.org/licenses/MIT). Bebas digunakan dan dimodifikasi untuk kebutuhan pembelajaran maupun pengembangan lebih lanjut.

---
