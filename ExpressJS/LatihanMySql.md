# Latihan

Buatlah aplikasi REST API sederhana yang dapat menampilkan data buku dari database `bookstore`.

Table `books` memiliki struktur sebagai berikut:

- `id` (int, primary key, auto increment)
- `title` (varchar)
- `author_id` (int, foreign key)
- `category_id` (int, foreign key)
- `publisher_id` (int, foreign key)
- `published_year` (int)
- `isbn` (varchar)
- `synopsis` (text)

Table `authors` memiliki struktur sebagai berikut:

- `id` (int, primary key, auto increment)
- `name` (varchar)

Table `categories` memiliki struktur sebagai berikut:

- `id` (int, primary key, auto increment)
- `name` (varchar)

Table `publishers` memiliki struktur sebagai berikut:

- `id` (int, primary key, auto increment)
- `name` (varchar)

API melayani request dengan format JSON dan memiliki endpoint sebagai berikut:

API endpoint books:

- `GET /books` : menampilkan seluruh data buku
- `GET /books/{id}` : menampilkan data buku dengan id tertentu
- `POST /books` : menambahkan data buku baru
- `PUT /books/{id}` : mengubah data buku dengan id tertentu

API endpoint authors:

- `GET /authors` : menampilkan seluruh data penulis
- `GET /authors/{id}` : menampilkan data penulis dengan id tertentu
- `POST /authors` : menambahkan data penulis baru
- `PUT /authors/{id}` : mengubah data penulis dengan id tertentu

API endpoint categories:

- `GET /categories` : menampilkan seluruh data kategori
- `GET /categories/{id}` : menampilkan data kategori dengan id tertentu
- `POST /categories` : menambahkan data kategori baru
- `PUT /categories/{id}` : mengubah data kategori dengan id tertentu
- `DELETE /categories/{id}` : menghapus data kategori dengan id tertentu

API endpoint publishers:

- `GET /publishers` : menampilkan seluruh data penerbit
- `GET /publishers/{id}` : menampilkan data penerbit dengan id tertentu
- `POST /publishers` : menambahkan data penerbit baru
- `PUT /publishers/{id}` : mengubah data penerbit dengan id tertentu
- `DELETE /publishers/{id}` : menghapus data penerbit dengan id tertentu

## Petunjuk

- Gunakan `dotenv` untuk menyimpan konfigurasi database.
- Gunakan script untuk membuat tabel-tabel di atas.
- Gunakan prinsip modularisasi untuk memisahkan kode berdasarkan concern-nya.
- Gunakan prinsip inheritance untuk menghindari duplikasi kode.
