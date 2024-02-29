---
theme: one
marp: true
---

# Panduan Entity Relationship Diagram (ERD)

---

# Relasi dalam ERD

- Menjelaskan hubungan antara dua entitas.
- Direpresentasikan sebagai garis yang menghubungkan entitas, biasanya dengan label yang menjelaskan hubungan tersebut.
- Jenis-jenis relasi:
  - One to one: Satu record dari suatu entitas berhubungan langsung dengan satu record dari entitas lain.
  - One to many: Satu record dari suatu entitas berhubungan dengan banyak record dari entitas lain.
  - Many to many: Banyak record dari suatu entitas dapat berhubungan dengan banyak record dari entitas lain.

---

# Atribut

- Properti dari suatu entitas, digunakan untuk mendeskripsikannya.
- Jenis-jenis atribut:
  - Simple: Tidak dapat dibagi menjadi atribut lain.
  - Composite: Dapat dibagi menjadi atribut lain.
  - Derived: Dihitung atau ditentukan dari atribut lain.
  - Atribut juga dapat berupa single-value atau multi-value.

---

# Kardinalitas

- Merepresentasikan jumlah instance dari suatu entitas yang ada dalam suatu relasi.
- Diekspresikan sebagai angka atau simbol.
- Nilai kardinalitas yang umum adalah zero, one, atau many.

---

# Bahasa Alami dalam ERD

- Membantu menerjemahkan deskripsi menjadi diagram.
- Elemen kunci:
- Noun (kata benda): Merepresentasikan entitas.
- Verb (kata kerja): Merepresentasikan relasi.
- Adjective (kata sifat): Merepresentasikan atribut.

---

# Simbol dan Notasi

- Terdapat beberapa standar notasi yang mendefinisikan simbol-simbol yang digunakan dalam ERD.
- Contoh: Chen notation, Crow’s Foot notation, Bachman notation, IDEF1X notation, dan Barker notation.

---

# Model Konseptual, Logis, dan Fisik

ERD dapat digambarkan dalam tiga tingkatan berbeda:

- Conceptual: Menunjukkan objek-objek bisnis dan hubungannya.
- Logical: Menambahkan atribut pada entitas dan detail lebih lanjut.
- Physical: Paling detail, mendefinisikan tabel, kolom, kunci, dan tipe data.

---

# Membuat Entity Relationship Diagram

Langkah-langkah membuat ERD:

1. Tuliskan deskripsi tentang data yang ingin disimpan.
2. Daftarkan objek-objek (noun) dan informasi yang ingin disimpan untuk masing-masing (atribut).
3. Jelaskan hubungan antara objek-objek.
4. Gambarkan diagram.

---

# Alat untuk Membuat ERD

- Terdapat berbagai aplikasi yang tersedia untuk membuat ERD.
- Contoh: LucidChart, Visio, dan database IDEs.

---

# Tips untuk Membuat ERD

- Tentukan tingkat detail yang tepat berdasarkan tujuan.
- Tinjau kembali entitas dan atribut untuk memastikan kelengkapan.
- Gunakan penamaan dan simbol yang konsisten.

---

# Referensi

**Database Star: A Guide to the Entity Relationship Diagram (ERD)**
This guide provides a comprehensive overview of ERDs, explaining their components like entities, attributes, relationships, and cardinality. It also discusses different ERD notations like Chen, Crow’s Foot, Bachman, IDEF1X, and Barker, and the levels of data models – conceptual, logical, and physical.
[Read more on Database Star](https://www.databasestar.com/entity-relationship-diagram/)

---

# Referensi

**Visual Paradigm: What is Entity Relationship Diagram (ERD)?**
Visual Paradigm's guide offers an in-depth look at ERDs, covering entities, attributes, primary and foreign keys, relationships, and cardinality. It also details the different data models (conceptual, logical, physical) and provides practical examples of ER diagrams for various systems.
[Explore Visual Paradigm's guide](https://www.visual-paradigm.com/guide/data-modeling/what-is-entity-relationship-diagram/)

---

# Referensi

**Lucidchart: ER Diagram (ERD) - Definition & Overview**
Lucidchart's article provides a historical background on ERDs and their use in database design, troubleshooting, and business information systems. It explains the components and features of ER diagrams, including entity types, keys, relationships, attributes, and cardinality, and also covers the limitations and uses of ER diagrams in different data models.
[Learn more on Lucidchart](https://www.lucidchart.com/pages/er-diagrams)
