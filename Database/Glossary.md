---
marp: true
theme: one
---

# Glosarium Istilah Database

---

# Entity (Entitas)

Objek atau konsep yang dapat diidentifikasi secara unik dan memiliki data yang disimpan. Dalam database, ini sering merepresentasikan tabel.

---

# Attribute (Atribut)

Ciri atau detail yang mendefinisikan atau menjelaskan entitas dalam database. Ini seringkali merupakan kolom dalam tabel.

---

# Primary Key

Atribut atau kombinasi atribut yang unik mengidentifikasi setiap baris atau rekaman dalam sebuah tabel.

---

# Foreign Key

Atribut dalam satu tabel yang merupakan Primary Key di tabel lain. Digunakan untuk membuat relasi antar tabel.

---

# Relational Database (Database Relasional)

Database yang menggunakan model relasional, di mana data disimpan dalam tabel dan relasi antar data direpresentasikan oleh kunci.

---

# SQL (Structured Query Language)

Bahasa standar untuk mengelola dan mengakses data dalam database relasional.

---

# Normalization (Normalisasi)

Proses mendesain skema database untuk mengurangi redundansi dan meningkatkan integritas data.

---

# Index (Indeks)

Struktur data yang meningkatkan kecepatan operasi dalam sebuah database.

---

# Database Engine (Mesin Database)

Komponen perangkat lunak yang bertanggung jawab untuk penyimpanan, manipulasi, dan pengambilan data dari database.

**Contoh**:

**InnoDB**: Mesin database default untuk MySQL. Mendukung transaksi, row locking, dan integritas referensial.

**MyISAM**: Mesin database yang lebih lama untuk MySQL. Optimal untuk baca cepat, tapi tidak mendukung transaksi dan table locking .

---

# Table Locking (Penguncian Tabel)

Mekanisme di mana seluruh tabel dikunci saat transaksi database berlangsung.

**Ciri-Ciri**:

- Sederhana dan membutuhkan lebih sedikit overhead.
- Kurang efektif dalam lingkungan dengan banyak transaksi karena meningkatkan waktu tunggu.
- Contoh Penggunaan: MyISAM di MySQL.

---

# Row Locking (Penguncian Baris)

Mekanisme di mana hanya baris data tertentu yang dikunci selama transaksi.

**Ciri-Ciri**:

- Memungkinkan akses simultan ke bagian lain dari tabel, meningkatkan performa dalam lingkungan multi-pengguna.
- Lebih kompleks dan membutuhkan lebih banyak overhead daripada penguncian tabel.
- Contoh Penggunaan: InnoDB di MySQL.
