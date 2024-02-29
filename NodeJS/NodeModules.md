---
marp: true
theme: one
---

# Format Ekspor Modul Node.js

---

# Export Satu Nilai atau Fungsi

- Sederhana dan langsung
- Ideal untuk modul dengan satu fungsionalitas utama

```javascript
// myModule.js
function sayHello(name) {
  return `Hello, ${name}!`
}

export default sayHello
```

---

# Export Satu Nilai atau Fungsi

**Penggunaan di file lain**

```javascript
import sayHello from './myModule.js'

console.log(sayHello('Alice'))
```

---

# Export Beberapa Fungsi/Variabel

- Pendekatan yang serbaguna dan fleksibel
- Memungkinkan ekspor selektif dari beberapa fungsi atau variabel

```javascript
// myModule.js
export function sayHello(name) {
  return `Hello, ${name}!`
}

export function sayGoodbye(name) {
  return `Goodbye, ${name}!`
}
```

---

# Export Beberapa Fungsi/Variabel

**Penggunaan di file lain**

```javascript
import { sayHello, sayGoodbye } from './myModule.js'

console.log(sayHello('Alice'))
console.log(sayGoodbye('Bob'))
```

---

# Export Beberapa Fungsi/Variabel

```javascript
// myModule.js
function sayHello(name) {
  return `Hello, ${name}!`
}

function sayGoodbye(name) {
  return `Goodbye, ${name}!`
}

export { sayHello, sayGoodbye }
```

---

# Export Class

- Ideal untuk pemrograman berorientasi objek
- Mengenkapsulasi fungsionalitas dalam struktur kelas

```javascript
// myModule.js
export class Greeter {
  sayHello(name) {
    return `Hello, ${name}!`
  }
  sayGoodbye(name) {
    return `Goodbye, ${name}!`
  }
}
```

---

# Export Class

**Penggunaan di file lain**

```javascript
import { Greeter } from './myModule.js'

const greeter = new Greeter()
console.log(greeter.sayHello('Alice'))
```

---

# Ekspor Default (Sintaks ES6)

- Mempermudah penyajian entitas utama tunggal
- Menyederhanakan sintaks impor di modul lain

```javascript
// myModule.js
export default function sayHello(name) {
  return `Hello, ${name}!`
}
```

**Penggunaan di file lain**

```javascript
import sayHello from './myModule.js'

console.log(sayHello('Alice'))
```

---

# Export Objek Literal

- Ideal untuk ekspor banyak fungsi yang terkait
- Memungkinkan ekspor selektif dari beberapa fungsi atau variabel

```javascript
// myModule.js
const myModule = {
  sayHello(name) {
    return `Hello, ${name}!`
  },
  sayGoodbye(name) {
    return `Goodbye, ${name}!`
  },
}

export default myModule
```

---

# Export Objek Literal

**Penggunaan di file lain**

```javascript
import myModule from './myModule.js'

console.log(myModule.sayHello('Alice'))
console.log(myModule.sayGoodbye('Bob'))
```
