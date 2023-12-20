---
marp: true
theme: one
---

# State Management

---

# State Management di React

**Apa itu State?**

- State adalah data yang dikelola di dalam komponen React.
- Ini adalah bagian penting dalam aplikasi React untuk memastikan UI bereaksi terhadap perubahan data.

---

# State Management di React

**Mengapa State Management Penting?**

- Menjaga UI agar tetap konsisten dengan data yang ada.
- Memudahkan pengelolaan data, terutama di aplikasi yang kompleks.

<!-- **Catatan:** Gunakan analogi, seperti state adalah seperti catatan yang diperbarui untuk mencatat skor dalam permainan, untuk menjelaskan konsep state. -->

---

# Mengenal `useState`

`useState` adalah hook untuk menambahkan dan mengelola state lokal di dalam komponen fungsional.

**Contoh Kode:**

```javascript
const [count, setCount] = useState(0)
```

Ini mendefinisikan state `count` dengan nilai awal 0 dan fungsi `setCount` untuk memperbarui nilai tersebut.

<!-- **Catatan:** Berikan contoh sederhana seperti penggunaan `useState` untuk menampilkan dan memperbarui jumlah klik pada tombol. -->

---

# `useState`

**Membuat Counter dengan `useState`**

```javascript
function Counter() {
  const [count, setCount] = useState(0)

  return (
    <div>
      <p>Anda telah mengklik {count} kali</p>
      <button onClick={() => setCount(count + 1)}>Klik saya</button>
    </div>
  )
}
```

<!-- **Gambar:** Screenshot aplikasi penghitung.

<!-- **Catatan:** Ajak peserta untuk mencoba membuat aplikasi sederhana ini sendiri. --> -->

---

# Beralih ke `useReducer`

**Apa itu `useReducer`?**

`useReducer` adalah alternatif `useState` yang lebih cocok untuk mengelola state yang kompleks.

**Membandingkan useState dan `useReducer`**

`useState` ideal untuk state yang sederhana, sedangkan `useReducer` lebih sesuai untuk kasus dengan logika state yang lebih kompleks atau state yang terdiri dari beberapa nilai yang saling terkait.

---

# `useReducer`

```javascript
const [state, dispatch] = useReducer(reducer, initialState)
```

Penggunaan dasar `useReducer` dengan `reducer` dan `initialState`.

<!-- **Catatan:** Jelaskan skenario seperti formulir dengan banyak input atau interaksi data yang kompleks sebagai contoh penggunaan `useReducer`. -->

---

# `useReducer`

```javascript
const initialState = { count: 0 }

function reducer(state, action) {
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

# `useReducer`

```javascript
function Counter() {
  const [state, dispatch] = useReducer(reducer, initialState)
  return (
    <>
      Count: {state.count}
      <button onClick={() => dispatch({ type: 'increment' })}>+</button>
      <button onClick={() => dispatch({ type: 'decrement' })}>-</button>
    </>
  )
}
```

<!-- - **Gambar:** Screenshot aplikasi setelah refaktor.

<!-- **Catatan:** Dorong peserta untuk mengubah kode sebelumnya dengan menggunakan `useReducer` dan memahami perbedaan dalam pengelolaan state. --> -->

---

# Pengenalan Redux

**Konsep State Global**

Redux adalah pustaka yang memungkinkan pengelolaan state global, yang dapat diakses dan dimutasi oleh banyak komponen dalam aplikasi.

**Prinsip Dasar Redux**

- Konsep utama Redux meliputi Actions, Reducers, dan Store.
- Menggunakan pola Flux untuk memperbarui state.

```javascript
const store = createStore(reducer)
```

<!-- **Catatan:** Jelaskan bagaimana Redux membantu dalam mengelola state yang perlu dibagikan antar komponen, seperti data pengguna atau preferensi tema. -->

---

# Kompleksitas Redux

**Boilerplate dan Kompleksitas**

Salah satu tantangan menggunakan Redux adalah setup yang lebih rumit dan banyaknya boilerplate code yang diperlukan.

<!--- **Gambar:** Tampilkan contoh kode Redux yang lebih kompleks, seperti kombinasi beberapa reducers atau penerapan middleware.

 **Catatan:** Diskusikan tentang bagaimana kompleksitas Redux dapat menjadi hambatan, terutama untuk proyek yang lebih kecil atau bagi pengembang yang baru memulai dengan React. -->

---

# Redux Toolkit untuk Kemudahan

**Mengapa Redux Toolkit?**

Redux Toolkit dirancang untuk mempermudah setup Redux dan mengurangi jumlah boilerplate code.

**Perbandingan dengan Redux Tradisional**

Lebih sederhana dan efisien dalam penggunaan dibandingkan Redux tradisional.

```javascript
const store = configureStore({ reducer: rootReducer })
```

<!-- **Catatan:** Jelaskan bagaimana Redux Toolkit menyederhanakan pembuatan store, penambahan middleware, dan definisi reducers. -->

---

# Redux Toolkit

```javascript
const counterSlice = createSlice({
  name: 'counter',
  initialState,
  reducers: {
    increment: (state) => {
      state.value += 1
    },
    decrement: (state) => {
      state.value -= 1
    },
  },
})

const { actions, reducer } = counterSlice
const store = configureStore({ reducer })
```

<!--- **Gambar:** Screenshot aplikasi dengan Redux Toolkit.

 **Catatan:** Ajak peserta untuk mencoba mengimplementasikan Redux Toolkit dalam proyek mereka dan perhatikan perbedaan dalam penggunaan dibandingkan Redux tradisional. -->
