---
marp: true
theme: one
---

# Logika

---

## Apa itu Logika?

Logika adalah cabang ilmu pengetahuan yang mempelajari prinsip-prinsip berpikir dan penalaran yang benar.

Dalam konteks pemrograman, logika digunakan untuk memodelkan hubungan dan aturan dalam suatu sistem.

Logika juga digunakan untuk menghasilkan solusi atau hasil yang konsisten dan benar berdasarkan aturan dan informasi yang tersedia.

---

## Proposisi

Proposisi adalah pernyataan yang dapat dinyatakan benar atau salah. Proposisi dapat berupa pernyataan tunggal atau majemuk.

**Proposisi tunggal** adalah proposisi yang hanya terdiri dari satu subjek dan satu predikat. Misalnya, "Anjing adalah hewan peliharaan" adalah proposisi tunggal.

**Proposisi majemuk** adalah proposisi yang terdiri dari dua atau lebih proposisi tunggal yang digabungkan menggunakan operator logika. Misalnya, "Anjing adalah hewan peliharaan dan kucing adalah hewan peliharaan" adalah proposisi majemuk.

---

## Logika Proposisional

Logika proposisional adalah logika yang digunakan untuk memodelkan hubungan antara proposisi. Proposisi dapat berupa pernyataan tunggal atau majemuk.

---

## Tabel kebenaran

Tabel kebenaran adalah tabel yang menunjukkan nilai kebenaran dari suatu proposisi atau proposisi majemuk berdasarkan nilai kebenaran dari proposisi-proposisi yang membentuknya.

Berikut adalah tabel kebenaran untuk operator logika proposisional:

| Operator | Notasi | Penjelasan                                            |
| -------- | ------ | ----------------------------------------------------- |
| AND      | `&&`   | Kedua proposisi harus benar agar hasilnya benar.      |
| OR       | `\|\|` | Salah satu proposisi harus benar agar hasilnya benar. |
| NOT      | `!`    | Membalik nilai kebenaran proposisi.                   |

---

## Penerapan Logika dalam Pemrograman

**Kondisi:** ekspresi yang digunakan untuk menentukan apakah suatu blok kode akan dijalankan atau tidak. Misalnya, kondisi `if` digunakan untuk menjalankan suatu blok kode jika kondisi tersebut terpenuhi.

```js
// AND
if (x > 0 && x < 10) {
  // Code to be executed if both conditions are true
}

// OR
if (x > 0 || x < 10) {
  // Code to be executed if either condition is true
}
```

---

## Penerapan Logika dalam Pemrograman

**Pengulangan:** adalah struktur kontrol yang digunakan untuk menjalankan suatu blok kode beberapa kali. Misalnya, struktur kontrol for digunakan untuk menjalankan suatu blok kode selama kondisi tertentu terpenuhi.

```js
for (let i = 0; i < 10; i++) {
  // Code to be executed

  // Break the loop if i is 5
  if (i == 5) {
    break;
  }
}
```

---

## Penerapan Logika dalam Pemrograman

**Fungsi:** Fungsi adalah blok kode yang dapat digunakan kembali untuk melakukan tugas tertentu. Fungsi dapat digunakan untuk memodelkan hubungan antara objek dan atributnya. Misalnya, fungsi `isPrime()` dapat digunakan untuk menentukan apakah suatu bilangan adalah bilangan prima atau bukan.

---

## Penerapan Logika dalam Pemrograman

```js
function isPrime(n) {
  if (n <= 1) {
    return false;
  }

  for (let i = 2; i < n; i++) {
    if (n % i == 0) {
      return false;
    }
  }

  return true;
}
```
