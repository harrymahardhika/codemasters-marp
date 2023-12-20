---
marp: true
theme: one
---

# Git

---

# Introduction to Git

- Version Control System (VCS)
- Dasar-dasar Git
- Perintah Git Umum
- Bekerja dengan Repositori Remote
- Praktik Terbaik

---

# What is Version Control?

- Sistem yang mencatat perubahan pada file dari waktu ke waktu.
- Memungkinkan untuk melihat versi spesifik dari file.
- Memfasilitasi kolaborasi antara beberapa kontributor.

---

# Why Use Version Control?

- Melacak Perubahan
- Kolaborasi
- Kembali ke State Tertentu
- Percabangan untuk Pengembangan Fitur
- Integritas Kode

---

# Basics of Git

**Repository (Repo):**
Berisi file proyek dan riwayat versi (version history).

**Working Directory:**
Ruang kerja lokal di mana perubahan dilakukan.

**Staging Area:**
Area perantara sebelum melakukan commit perubahan.

**Commit:**
Snapshot perubahan yang disimpan dalam riwayat versi (version history).

---

# Common Git Commands

`git init` Menginisialisasi repositori Git baru.

`git add` Menambahkan perubahan ke area staging.

`git commit` Melakukan commit perubahan.

`git status` Menampilkan status perubahan.

`git log` Menampilkan riwayat commit.

---

# Branching in Git

**Branch:** Independent line of development.

**`git branch`** Lists all branches.

**`git checkout`** Switches to a different branch.

**`git merge`** Combines changes from different branches.

---

# Working with Remote Repositories

**Repositori Remote:** Versi repositori yang dihosting.

**`git remote`** Menampilkan daftar repositori remote.

**`git clone`** Membuat salinan lokal dari repositori remote.

**`git push`** Mengunggah perubahan ke repositori remote.

**`git pull`** Mengunduh perubahan dari repositori remote.

---

# Git Workflow

1. **Clone Repositori:** `git clone <url-repositori>`

2. **Lakukan Perubahan:** Modifikasi file di direktori kerja.

3. **Tambahkan dan Commit:** `git add <file>` dan `git commit -m "Pesan commit"`

4. **Push Perubahan:** `git push origin <nama-branch>`

---

# Best Practices

- **Commit Sesering Mungkin:** Lakukan commit kecil dan sering.

- **Tulis Pesan Commit yang Deskriptif:** Jelaskan dengan jelas perubahan yang dilakukan.

- **Gunakan Branch:** Buat branch untuk fitur baru atau perbaikan bug.

- **Pull Sebelum Push:** Perbarui repositori lokal sebelum melakukan push perubahan.

- **Review Perubahan Sebelum Commit:** Gunakan `git diff` untuk meninjau modifikasi.
