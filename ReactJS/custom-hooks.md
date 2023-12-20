---
marp: true
theme: one
---

# Custom Hooks

---

# What is a Hooks?

- Hooks adalah fitur di ReactJS yang memungkinkan Anda menggunakan fungsionalitas React di luar komponen.

- Custom Hooks memperluas kemampuan ini dengan memungkinkan Anda membuat Hooks sendiri yang dapat digunakan kembali untuk logika kompleks atau fitur umum di seluruh aplikasi Anda.

---

# Key Features

- **Berfungsi seperti Hooks bawaan**: dalam fungsi JavaScript dan mirip dengan Hooks bawaan seperti `useState` atau `useEffect`.
- **Reusable**: digunakan untuk logika berulang yang digunakan di beberapa komponen agar kode lebih bersih dan efisien.
- **Modular**: membantu menyusun ulang kode Anda menjadi unit yang lebih kecil dan terfokus, meningkatkan maintainability.
- **Menyembunyikan kompleksitas**: Anda dapat menyembunyikan logika kompleks di dalam Custom Hooks, membuat komponen lebih sederhana dan mudah dipahami.
- **Tidak spesifik komponen**: tidak terikat pada komponen tertentu, sehingga dapat digunakan di mana saja dalam aplikasi Anda.

---

# Contoh Custom Hooks

```jsx
// hooks/useDocumentTitle.js
import { useEffect } from 'react'

function useDocumentTitle(title) {
  useEffect(() => {
    document.title = title
  }, [title])
}
```

---

# Contoh Custom Hooks

```jsx
// App.jsx
import React from 'react'
import useDocumentTitle from './hooks/useDocumentTitle'

function App() {
  useDocumentTitle('My Awesome App')

  return (
    <div>
      <h1>Welcome to My Awesome App!</h1>
    </div>
  )
}
```

---

# Key Points

- Custom Hooks menawarkan cara untuk mengimplementasikan logika yang berulang.
- Penamaan fungsi harus dimulai dengan `use` dan dapat menggunakan Hooks lain di dalamnya.
- Custom Hooks dapat menerima argumen dan mengembalikan nilai, sama seperti fungsi biasa.
