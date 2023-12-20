---
marp: true
theme: one
---

# Penggunaan `useReducer` di React

---

# Apa Itu `useReducer`?

- `useReducer` adalah hook di React untuk mengelola logika state yang kompleks.
- Alternatif untuk `useState`, sangat berguna untuk logika state yang lebih kompleks.
- Lebih efektif ketika state berikutnya bergantung pada state sebelumnya atau ketika ada sub-nilai state yang beragam.

---

# Fungsi Reducer

- Fungsi reducer menerima state saat ini dan sebuah action.
- Mengembalikan state baru berdasarkan tipe action.
- Action biasanya adalah objek yang mengandung tipe dan data tambahan.

---

# Contoh Penggunaan

```jsx
function counterReducer(state, action) {
  switch (action.type) {
    case 'increment':
      return { count: state.count + 1 }
    case 'decrement':
      return { count: state.count - 1 }
    default:
      throw new Error()
  }
}
```

---

# Implementasi `useReducer`

```jsx
function Counter() {
  const [state, dispatch] = useReducer(counterReducer, { count: 0 })

  return (
    <>
      Count: {state.count}
      <button onClick={() => dispatch({ type: 'increment' })}>+</button>
      <button onClick={() => dispatch({ type: 'decrement' })}>-</button>
    </>
  )
}
```

---

# Keuntungan `useReducer`

- Transisi state lebih terprediksi dengan tipe action yang eksplisit.
- Memudahkan pengelolaan logika state yang kompleks.
- Meningkatkan kemudahan dalam pemeliharaan dan skalabilitas.
- Lebih mudah diuji dan didebug.

---

# Kapan Menggunakan `useReducer`

- Ketika logika state Anda cukup kompleks dengan sub-nilai beragam.
- Ketika state berikutnya tergantung pada state sebelumnya.
- Untuk menyentralisasi logika state agar lebih mudah dibaca dan dipelihara.

---

# Kesimpulan

- `useReducer` menyediakan cara yang lebih terstruktur dan skalabel untuk menangani state yang kompleks dalam komponen React Anda.
- Membuat kode Anda lebih dapat diprediksi dan mudah dipahami.
