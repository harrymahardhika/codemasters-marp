---
marp: true
theme: one
---

# Express.js 🤝️ mysql2

---

# Menggunakan Express.js dengan mysql2

- mysql2 adalah pustaka MySQL untuk Node.js yang memungkinkan kita berinteraksi dengan database MySQL.

- Menggabungkan Express.js dengan mysql2 memungkinkan pembuatan aplikasi web yang berinteraksi dengan database MySQL.

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

Buat kode untuk membuat tabel `books` dengan kolom-kolom:

- `id` (int, primary key, auto increment)
- `title` (varchar)
- `author` (varchar)
- `year` (int)
- `isbn` (varchar)

### Latihan 2

Buat kode untuk menghapus tabel `books`
