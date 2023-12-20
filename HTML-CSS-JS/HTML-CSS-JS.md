---
theme: one
marp: true
---

# HTML, CSS, dan JavaScript

---

# Apa Itu HTML?

- **HTML** (Hypertext Markup Language) adalah bahasa yang digunakan untuk membuat struktur halaman web.
- Digunakan untuk menentukan judul, paragraf, gambar, tautan, dan elemen-elemen lain dalam halaman web.

---

### Elemen HTML

- `<!DOCTYPE html>`: Deklarasi tipe dokumen.
- `<html>`: Elemen root (akar) dari halaman web.
- `<head>`: Metadata dan tautan ke sumber daya eksternal.
- `<title>`: Mengatur judul halaman web (ditampilkan di tab peramban).
- `<body>`: Berisi konten yang terlihat.
- `<h1>`, `<h2>`, `<h3>`: Heading (1 adalah yang terbesar, 3 lebih kecil).

---

### Elemen HTML

- `<p>`: Paragraf.
- `<a href="URL">`: Tautan.
- `<img src="image.jpg" alt="Deskripsi">`: Gambar.
- `<ul>`, `<ol>`, `<li>`: Daftar (tak terurut, terurut, item daftar).
- `<div>`: Kontainer untuk elemen lain (digunakan untuk penataan dan tata letak).
- `<span>`: Kontainer dalam baris untuk elemen lain (digunakan untuk penataan dan tata letak).
- `<button>`: Tombol yang dapat diklik.

---

### Elemen HTML

- `<form>`: Kontainer untuk elemen formulir.
- `<input type="text">`: Bidang input teks.
- `<input type="email">`: Bidang input email.
- `<input type="password">`: Bidang input sandi.
- `<input type="radio">`: Tombol radio.
- `<input type="checkbox">`: Kotak centang.
- `<input type="submit">`: Tombol kirim.
- `<select>`, `<option>`: Menu dropdown.
- `<textarea>`: Bidang input teks panjang.

---

# Komponen-Komponen dari Sebuah Tag HTML

Sebuah tag HTML terdiri dari beberapa komponen utama yang mempengaruhi cara tag tersebut bekerja.

- **Tag Pembuka**: Merupakan awal dari tag dan didefinisikan dengan nama tag.
- **Tag Penutup**: Menandakan akhir dari tag dan memiliki nama yang sama dengan tag pembuka, tetapi dengan tanda "/" di depannya (misalnya, `</nama_tag>`).
- **Isi Tag**: Konten yang dilingkupi oleh tag.
- **Atribut**: Informasi tambahan yang ditempatkan dalam tag dan sering digunakan untuk mengatur atau memberi tag karakteristik tertentu.

---

# Komponen-Komponen dari Sebuah Tag HTML

```html
<a href="https://www.example.com" target="_blank">Tautan Contoh</a>
```

- Tag Pembuka: `<a>`
- Atribut: `href="https://www.example.com"` dan `target="_blank"`
- Isi Tag: `Tautan Contoh`
- Tag Penutup: `</a>`

---

# Contoh HTML Dasar

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Judul Halaman</title>
  </head>
  <body>
    <h1>Selamat Datang di Web Saya</h1>
    <p>Ini adalah contoh halaman web.</p>
    <img src="gambar.jpg" alt="Deskripsi Gambar" />
    <a href="https://www.example.com">Tautan</a>
  </body>
</html>
```

---

# Apa Itu CSS?

- **CSS (Cascading Style Sheets)** adalah bahasa yang digunakan untuk mengatur tampilan halaman web.
- Mengontrol warna, jenis huruf, margin, dan tata letak elemen HTML.

---

# Contoh CSS Dasar

```css
/* Styles.css */
body {
  font-family: Arial, sans-serif;
  background-color: #f2f2f2;
}

h1 {
  color: #333;
}

p {
  font-size: 16px;
  margin: 10px;
}
```

---

# Komponen-Komponen dari Sebuah Aturan CSS

Sebuah aturan CSS terdiri dari beberapa komponen yang mengatur tampilan elemen HTML.

- **Selector**: Bagian aturan yang menentukan elemen HTML yang akan diatur.
- **Property**: Sifat atau gaya yang akan diberikan ke elemen.
- **Value**: Nilai yang diberikan kepada sifat tersebut.
- **Declaration Block**: Terdiri dari property dan value yang dikelilingi oleh kurung kurawal (`{}`).

---

# Contoh Komponen Aturan CSS

```css
p {
  color: blue;
  font-size: 16px;
}
```

- Selector: `p`
- Property: `color` dan `font-size`
- Value: `blue` dan `16px`
- Declaration Block: `{ color: blue;
font-size: 24px; font-size: 16px; }`

---

# HTML ❤️ CSS

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Halaman Web Saya</title>
    <style>
      h1 {
        color: blue;
        font-size: 24px;
      }
      p {
        font-size: 16px;
        margin-top: 20px;
      }
    </style>
  </head>
  <body>
    <h1>Selamat Datang</h1>
    <p>Ini adalah halaman web saya.</p>
  </body>
</html>
```

---

# HTML ❤️ CSS

```html
<!-- index.html -->

<!DOCTYPE html>
<html>
  <head>
    <title>Halaman Web Saya</title>
    <link rel="stylesheet" type="text/css" href="style.css" />
  </head>
  <body>
    <h1>Selamat Datang</h1>
    <p>Ini adalah halaman web saya.</p>
  </body>
</html>
```

---

# HTML ❤️ CSS

```css
/* style.css */

h1 {
  color: blue;
  font-size: 24px;
}

p {
  font-size: 16px;
  margin-top: 20px;
}
```

---

# HTML ❤️ CSS

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Halaman Web Saya</title>
    <style>
      #title {
        color: blue;
        font-size: 24px;
      }
      .paragraph {
        font-size: 16px;
        margin-top: 20px;
      }
    </style>
  </head>
  <body>
    <h1 id="title">Selamat Datang</h1>
    <p class="paragraph">Ini adalah halaman web saya.</p>
    <p class="paragraph">Ini adalah paragraf lain.</p>
  </body>
</html>
```

---

# Perbedaan Antara Class dan ID dalam CSS

- Dalam CSS, kita dapat menggunakan selector class dan selector ID untuk merujuk ke elemen-elemen HTML.
- Kedua selector ini memiliki perbedaan utama dalam penggunaan dan aplikasi.

---

# Selector Class

- **Selector Class** digunakan untuk mengelompokkan beberapa elemen dengan properti yang sama.
- Anda dapat menggunakan selector class pada beberapa elemen.
- Contoh: `.button { background-color: blue;
font-size: 24px; }`

```html
<button class="button">Klik Saya</button>
<a class="button" href="#">Tautan</a>
<p class="button">Teks Contoh</p>
```

Dalam contoh di atas, tiga elemen HTML menggunakan selector class yang sama untuk mengatur latar belakangnya menjadi biru.

---

# Selector ID

- **Selector ID** digunakan untuk merujuk ke elemen yang memiliki ID unik.
- Anda harus menggunakan ID hanya pada satu elemen dalam satu halaman HTML.
- Contoh: `#title { font-size: 24px; }`

```html
<h1 id="title">Judul Utama</h1>
<p>Paragraf biasa.</p>
```

Dalam contoh di atas, elemen `<h1>` memiliki ID unik "title" untuk mengubah ukuran fontnya.

---

# Kesimpulan

- Gunakan **Selector Class** jika Anda ingin mengatur beberapa elemen dengan properti yang sama.
- Gunakan **Selector ID** jika Anda ingin merujuk ke elemen dengan ID unik.
- Jika memungkinkan, hindari penggunaan ID yang berlebihan karena hanya satu elemen yang boleh memiliki ID unik dalam satu halaman.

---

# Apa Itu JavaScript?

- **JavaScript** adalah bahasa pemrograman yang digunakan untuk membuat interaktivitas di halaman web.
- Contoh penggunaan: menangani tindakan pengguna, validasi formulir, dan lainnya.

---

# HTML 🤝️ JavaScript

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Contoh Web</title>
    <link rel="stylesheet" type="text/css" href="styles.css" />
    <script>
      function greetings() {
        var name = prompt('Siapa nama Anda?')
        alert('Halo, ' + name + '!')
      }
    </script>
  </head>
  <body>
    <h1>Selamat Datang</h1>
    <p>Klik tombol di bawah.</p>
    <button onclick="greetings()">Klik Saya</button>
  </body>
</html>
```

---

# HTML 🤝️ JavaScript

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Contoh Web</title>
    <link rel="stylesheet" type="text/css" href="styles.css" />
    <script src="script.js"></script>
  </head>
  <body>
    <h1>Selamat Datang</h1>
    <p>Klik tombol di bawah.</p>
    <button onclick="greetings()">Klik Saya</button>
  </body>
</html>
```

---

# Latihan HTML

### Membuat Halaman Web Sederhana

Buatlah halaman web sederhana yang berisi judul, paragraf, dan gambar. Tambahkan tautan ke halaman web Anda yang mengarah ke website lain.

### Membuat Daftar

Buat daftar dengan menggunakan tag HTML yang sesuai, termasuk daftar tak terurut dan daftar terurut.

---

# Latihan HTML

### Menggunakan Gambar Latar (Background Image)

Gantilah latar belakang halaman web dengan gambar latar yang Anda pilih.

### Menggunakan Formulir

Buatlah formulir sederhana dengan beberapa elemen seperti kotak teks dan tombol kirim.

---

# Latihan CSS

### Merubah Warna Teks (Text Color)

Ubah warna teks pada halaman web Anda menggunakan CSS.

### Mengatur Lebar dan Tinggi Elemen

Atur lebar dan tinggi elemen pada halaman web Anda menggunakan CSS.

### Menggunakan CSS untuk Membuat Border

Tambahkan border pada elemen halaman web Anda menggunakan CSS.

---

# Latihan CSS

### Menggunakan CSS untuk Merubah Font Teks

Ubah jenis font dan ukuran teks pada halaman web.

### Merubah Latar Belakang (Background)

Ubah latar belakang halaman web dengan warna atau gambar menggunakan CSS.
