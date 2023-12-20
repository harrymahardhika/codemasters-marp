---
marp: true
theme: one
---

# Routing

With React Router v6

---

# What is Routing?

Routing adalah fitur yang memungkinkan aplikasi ReactJS menampilkan komponen yang berbeda sesuai dengan URL yang diakses pengguna. Ini seperti peta jalan yang mengarahkan pengguna ke halaman yang tepat berdasarkan alamat web yang mereka masukkan.

---

# React Router

- Sebuah pustaka untuk mengelola _routing_ dalam aplikasi React.
- Memungkinkan navigasi antar komponen yang berbeda.

## Fitur Utama:

- API yang Disederhanakan: Membuat pengembangan lebih mudah dan intuitif.
- Link dan Rute Relatif: Memudahkan pengelolaan rute dalam aplikasi.
- Peringkat Rute Otomatis: Mengatur rute secara otomatis berdasarkan pola dan prioritas.

---

# Installation

```bash
npm install react-router-dom
```

---

# Basic Setup

- Import `BrowserRouter` and wrap your application in it.
- Use `Routes` and `Route` to define paths and components.

```jsx
import { BrowserRouter, Routes, Route } from 'react-router-dom'

function App() {
  return (
    <BrowserRouter>
      <Routes>
        <Route path="/" element={<HomePage />} />
        <Route path="about" element={<AboutPage />} />
      </Routes>
    </BrowserRouter>
  )
}
```

---

# Navigating Between Routes

**Using the `Link` Component**

- Replace `<a>` tags with `Link` for in-app navigation.
- Prevents page reloads and maintains application state.

```jsx
import { Link } from 'react-router-dom'

const Navigation = () => (
  <nav>
    <Link to="/">Home</Link>
    <Link to="/about">About</Link>
  </nav>
)
```

---

# Practice Exercise

Create a simple book listing app with the following routes:

- Home (`/`)
- About (`/about`)
- Book List (`/books`)
- Book Details (`/books/:bookId`)

Implement dynamic routing for the Book Details page, where `bookId` is a variable in the URL.

---

# Advanced Routing

- Direkomendasikan untuk menggunakan `createBrowserRouter` untuk aplikasi web.
- https://reactrouter.com/en/main/routers/picking-a-router
- https://reactrouter.com/en/main/routers/create-browser-router

---

# Advanced Routing

```jsx
// router.js
import { createBrowserRouter } from 'react-router-dom'
import ParentComponent from './ParentComponent.jsx'
import ChildComponent from './ChildComponent.jsx'

const router = createBrowserRouter([
  {
    path: '/',
    Component: ParentComponent,
    children: [
      {
        path: 'child/:id',
        Component: ChildComponent,
      },
    ],
  },
])

export default router
```

---

# Advanced Routing

```jsx
// ParentComponent.jsx
import { Outlet, Link } from 'react-router-dom'

const ParentComponent = () => {
  return (
    <div>
      <h1>Parent Component</h1>
      <nav>
        <Link to="/">Home</Link>
        <Link to="/child/1">Child 1</Link>
        <Link to="/child/2">Child 2</Link>
      </nav>
      <main>
        <Outlet />
      </main>
    </div>
  )
}
```

---

# Advanced Routing

```jsx
// ChildComponent.jsx
import { useParams } from 'react-router-dom'

const ChildComponent = () => {
  const params = useParams()

  return (
    <div>
      <h1>Child Component</h1>
      <p>Child ID: {params.id}</p>
    </div>
  )
}
```

---

# Advanced Routing

```jsx
// main.js
import App from './App.jsx'
import router from './router.js'
import { RouterProvider } from 'react-router-dom'

ReactDOM.createRoot(document.getElementById('root')).render(
  <React.StrictMode>
    <RouterProvider router={router}>
      <App />
    </RouterProvider>
  </React.StrictMode>
)
```

---

# Advanced Routing

```jsx
// main.js
import { RouterProvider } from 'react-router-dom'
import router from './router.js'

const App = () => {
  return <RouterProvider router={router} />
}

export default App
```

---

# Advanced Routing

- Dapat digunakan untuk membuat aplikasi yang lebih kompleks.
- Membantu dalam penyusunan komposisi dan layout aplikasi.

---

# Advanced Routing

```jsx
const router = createBrowserRouter([
  {
    path: '/',
    Component: AppLayout,
    children: [
      { path: 'child', Component: ChildComponent },
      { path: 'other-child', Component: OtherChildComponent },
    ],

    path: '/admin',
    Component: AdminLayout,
    children: [
      { path: 'child-admin/', Component: ChildAdminComponent },
      { path: 'other-child-admin/', Component: OtherChildAdminComponent },
    ],
  },
])
```

---

# Advanced Routing

```jsx
// AppLayout.jsx
import { Outlet } from 'react-router-dom'

const AppLayout = () => {
  return (
    <div>
      <h1>App Layout</h1>
      <nav>
        <Link to="/">Home</Link>
        <Link to="/child">Child</Link>
        <Link to="/other-child">Other Child</Link>
      </nav>
      <main>
        <Outlet />
      </main>
    </div>
  )
}
```
