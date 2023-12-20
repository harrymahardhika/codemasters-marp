---
marp: true
theme: one
---

# Creating a React App

---

# Project Setup

```bash
npm init vite@latest learn-react
# > choose React
# > choose JavaScript

cd learn-react
npm install
npm run dev
```

---

# Components

```jsx
import React from 'react'

function App() {
  return (
    <div>
      <h1>Hello World!</h1>
    </div>
  )
}

export default App
```

---

# JSX

- HTML-like syntax
- Transpiled to JavaScript

---

# Props

```jsx
function App() {
  return (
    <div>
      <Hello name="John" />
      <Hello name="Jane" />
    </div>
  )
}
```

```jsx
function Hello(props) {
  return <h1>Hello {props.name}!</h1>
}
```
