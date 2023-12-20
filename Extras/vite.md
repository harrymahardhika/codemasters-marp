---
marp: true
theme: one
---

# Vite.js

Modern Frontend Build Tools

---

# Apa itu Vite.js?

Vite.js (https://vitejs.dev) adalah modern frontend build tool yang dirancang untuk mempercepat proses pengembangan web.

- **Fast Cold Start**: Memulai project dengan cepat.
- **Hot Module Replacement (HMR)**: Perubahan instan pada kode.
- **Optimized Build**: Membangun aplikasi dengan efisiensi tinggi.

---

# Fitur Utama Vite.js

Vite.js menawarkan beberapa fitur unggulan yang membuatnya menonjol di antara build tools lainnya.

- **Server Development yang Cepat**: Memanfaatkan ES modules untuk server development yang lebih cepat.
- **Plugin yang Kaya**: Mendukung berbagai plugin untuk memperluas fungsionalitas.
- **Integrasi Framework**: Kompatibel dengan framework populer seperti Vue, React, dan Svelte.
- **Optimized Build**: Membangun aplikasi dengan efisiensi tinggi.

---

# Manual Setup

1. Buat folder project dan inisialisasi project Node.js.
2. Instalasi Vite.js sebagai dependency development.

```bash
mkdir vite-app
cd vite-app
npm init -y
npm install vite --save-dev
```

---

# Manual Setup

Tambahkan script `dev` dan `build` ke `package.json`.

```json
{
  "scripts": {
    "dev": "vite",
    "build": "vite build"
  }
}
```

---

# Manual Setup

Tambahkan file `index.html`.

```html
<!-- ./index.html -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Vite App</title>
  </head>
  <body>
    <script type="module" src="/src/main.js"></script>
  </body>
</html>
```

---

# Manual Setup

Tambahkan file `style.css`.

```css
body {
  background-color: aquamarine;
}
```

Tambahkan file `main.js`.

```js
import './style.css'

console.log('hello world')
```

---

# Manual Setup

Jalanakan perintah `npm run dev` untuk memulai server development, kemudian buka `http://localhost:5173` di browser.

```bash
npm run dev

# Shortcuts
press r + enter to restart the server
press u + enter to show server url
press o + enter to open in browser
press c + enter to clear console
press q + enter to quit
```

---

# Using `create-vite`

```bash
npm init vite@latest vite-app
# ikuti prompt yang muncul
# pilih preset yang diinginkan
# kali ini kita pilih Vanilla JavaScript
cd vite-app
npm install
npm run dev
```

---

# Available `create-vite` Presets

| JavaScript | TypeScript |
| ---------- | ---------- |
| vanilla    | vanilla-ts |
| vue        | vue-ts     |
| react      | react-ts   |
| preact     | preact-ts  |
| lit        | lit-ts     |
| svelte     | svelte-ts  |
| solid      | solid-ts   |
| qwik       | qwik-ts    |

---

# Configuration

Vite.js menggunakan berkas `vite.config.js` untuk mengkonfigurasi project.

**Lokasi Default `index.html`**:

Lokasi default untuk berkas `index.html` dalam project Vite adalah root direktori project.

**Direktori Output Hasil Build Default**:

Direktori default untuk output hasil build di Vite adalah folder bernama `dist` di root directory project.

---

# Configuration

**Mengatur Lokasi `index.html`**:

Untuk mengubah lokasi berkas `index.html` Anda, Anda dapat mengatur opsi `root` di `vite.config.js`.

```javascript
// vite.config.js
export default {
  root: 'src', // Direktori root kustom
  // konfigurasi lainnya...
}
```

---

# Configuration

Dalam contoh ini, Vite akan mencari berkas `index.html` di dalam direktori `src`.

**Mengatur Direktori Output Hasil Build**:

Untuk mengubah direktori output untuk pembangunan produksi Anda, Anda dapat mengatur opsi `outDir` di dalam konfigurasi `build` di `vite.config.js`.

```javascript
// vite.config.js
export default {
  // konfigurasi lainnya...
  build: {
    outDir: 'build', // Direktori output hasil build kustom
  },
}
```

---

# Configuration

```js
import { defineConfig } from 'vite'

export default defineConfig({
  root: 'src',
  plugins: [],
  resolve: {
    alias: {
      '@': '/src',
    },
  },
  server: {
    port: 3000,
  },
  build: {
    outDir: 'dist',
  },
})
```

---

# Experimentasi: Vite.js with SCSS

```bash
npm install -D sass
```

```scss
// style.scss
body {
  background-color: aquamarine;

  h1 {
    color: red;
  }

  p {
    color: blue;
  }
}
```
