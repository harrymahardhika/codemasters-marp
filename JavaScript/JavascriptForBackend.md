---
theme: one
marp: true
---

# JavaScript untuk Pengembangan Backend

Mengenal Peran JavaScript dalam Dunia Backend

---

## Apa Itu JavaScript?

- **JavaScript** adalah bahasa pemrograman yang awalnya dikembangkan untuk pengembangan front-end.
- Namun, JavaScript sekarang juga digunakan dalam pengembangan backend dengan bantuan runtime seperti Node.js.
- JavaScript memungkinkan pengembang untuk membuat aplikasi web yang kuat di kedua sisi, frontend dan backend.

---

## JavaScript di Backend

JavaScript runtime (Node.js) memungkinkan pengembang untuk menciptakan aplikasi web dengan teknologi stack yang seragam dari sisi klien hingga server.

---

## Kenapa Pilih JavaScript di Backend?

- **Keseragaman (Uniformity)**: Menggunakan JavaScript di frontend dan backend mengurangi kompleksitas dalam mengelola arsitektur sistem.
- **Kinerja (Performance)**: JavaScript pada runtime server-side seperti Node.js memiliki kinerja yang sangat baik.
- **Komunitas (Community)**: Dukungan komunitas JavaScript sangat besar dan aktif.

---

## Contoh Kode Node.js

```javascript
// Contoh server sederhana menggunakan Node.js
const http = require("http");

const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader("Content-Type", "text/plain");
  res.end("Selamat datang di server Node.js!\n");
});

server.listen(3000, "localhost", () => {
  console.log("Server berjalan di http://localhost:3000/");
});
```
