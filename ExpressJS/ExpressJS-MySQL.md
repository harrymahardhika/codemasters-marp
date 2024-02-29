---
marp: true
theme: one
class:
  - invert
---

# Express.js 🤝️ mysql2

---

# Menggunakan Express.js dengan mysql2

- `mysql2` adalah pustaka MySQL untuk Node.js yang memungkinkan kita berinteraksi dengan database MySQL.

- Menggabungkan Express.js dengan `mysql2` memungkinkan pembuatan aplikasi web yang berinteraksi dengan database MySQL.

---

# Penggunaan

```bash
npm install mysql2
```

```javascript
const mysql = require('mysql2')

const db = mysql.createConnection({
  host: 'localhost',
  user: 'root',
  password: 'password',
  database: 'mydb',
})
```

---

# mysql2 ❤️ dotenv

```env
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=bookstore
DB_USERNAME=harry
DB_PASSWORD=secret
```

```javascript
const db = mysql.createConnection({
  host: process.env.DB_HOST,
  port: process.env.DB_PORT || 3306,
  user: process.env.DB_USERNAME,
  password: process.env.DB_PASSWORD,
  database: process.env.DB_DATABASE,
})
```

---

# Query

```javascript
db.query('SELECT * FROM users', (error, results, fields) => {
  if (error) throw error
  console.log(results)
})
```

---

# Query dengan Parameter

```javascript
const newUser = { name: 'John', email: 'john@example.com' }

db.query('INSERT INTO users SET ?', newUser, (error, results) => {
  if (error) throw error
  console.log('Data telah ditambahkan:', results.insertId)
})
```

---

# Latihan

### Latihan 1

Buatlah aplikasi REST API sederhana yang dapat menampilkan data dari database `indonesian_area` yang telah dibuat pada latihan sebelumnya.

Berikut daftar API endpoint yang perlu dibuat:

- `GET /provinces` : menampilkan seluruh data provinsi
- `GET /provinces/{id}` : menampilkan data provinsi dengan id tertentu, dan daftar kota yang berada di provinsi tersebut

---

# Latihan

### Latihan 2

Buat Rest API untuk mengelola data buku dari database `bookstore`, berdasarkan rancangan basis data yang telah dibuat pada latihan sebelumnya.

Berikut daftar API endpoint yang perlu dibuat:

- `GET /books` : menampilkan seluruh data buku
- `GET /books/{id}` : menampilkan data buku dengan id tertentu
- `POST /books` : menambahkan data buku baru
- `PUT /books/{id}` : mengubah data buku dengan id tertentu
- `DELETE /books/{id}` : menghapus data buku dengan id tertentu

---

# Latihan

### Latihan 3

Buat Rest API sederhana untuk proses belanja, berdasarkan rancangan basis data yang telah dibuat pada latihan sebelumnya.

Fungsi yang perlu dibuat meliputi:

- Menampilkan seluruh produk
- Menambahkan produk ke dalam keranjang belanja
- Menampilkan seluruh produk dalam keranjang belanja
- Menghapus produk dari keranjang belanja
- Checkout produk dalam keranjang belanja
- Menampilkan seluruh pesanan
