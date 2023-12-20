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

## Predikat

Predikat adalah pernyataan yang menghubungkan objek dengan atributnya. Predikat dapat berupa pernyataan tunggal atau majemuk.

**Predikat tunggal** adalah predikat yang hanya terdiri dari satu objek dan satu atribut. Misalnya, "Anjing memiliki bulu" adalah predikat tunggal.

**Predikat majemuk** adalah predikat yang terdiri dari dua atau lebih objek dan atribut yang digabungkan menggunakan operator logika. Misalnya, "Anjing yang memiliki bulu adalah mamalia" adalah predikat majemuk.

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

## Contoh Kode

```js
// AND
if (x > 0 && x < 10) {
  // Code to be executed if both conditions are true
}

// OR
if (x > 0 || x < 10) {
  // Code to be executed if either condition is true
}

// NOT
if (!isLoggedIn) {
  redirectToLoginPage();
}
```

---

## Logika Predikat

Logika predikat adalah logika yang digunakan untuk memodelkan hubungan antara objek dan atributnya. Predikat dapat berupa pernyataan tunggal atau majemuk.

---

## Operator logika predikat

Operator logika predikat adalah simbol yang digunakan untuk menghubungkan proposisi atau predikat. Berikut adalah beberapa operator logika predikat yang umum digunakan:

---

## Operator logika predikat

| Operator   | Penjelasan                                                                |
| ---------- | ------------------------------------------------------------------------- |
| AND        | Kedua proposisi atau predikat harus benar agar hasilnya benar.            |
| OR         | Salah satu proposisi atau predikat harus benar agar hasilnya benar.       |
| NOT        | Membalik nilai kebenaran proposisi atau predikat.                         |
| IMPLIKASI  | Jika proposisi pertama benar, maka proposisi kedua juga harus benar.      |
| EKIVALENSI | Proposisi pertama dan proposisi kedua memiliki nilai kebenaran yang sama. |

---

## Penerapan Logika dalam Pemrograman

Logika dapat diterapkan dalam pemrograman dengan menggunakan berbagai cara, seperti:

- **Kondisi:** Kondisi adalah ekspresi yang digunakan untuk menentukan apakah suatu blok kode akan dijalankan atau tidak. Misalnya, kondisi `if` digunakan untuk menjalankan suatu blok kode jika kondisi tersebut terpenuhi.
- **Pengulangan:** Pengulangan adalah struktur kontrol yang digunakan untuk menjalankan suatu blok kode beberapa kali. Misalnya, struktur kontrol for digunakan untuk menjalankan suatu blok kode selama kondisi tertentu terpenuhi.

---

## Penerapan Logika dalam Pemrograman

- **Fungsi:** Fungsi adalah blok kode yang dapat digunakan kembali untuk melakukan tugas tertentu. Fungsi dapat digunakan untuk memodelkan hubungan antara objek dan atributnya. Misalnya, fungsi `is_prime()` dapat digunakan untuk menentukan apakah suatu bilangan adalah bilangan prima atau bukan.

---

## Contoh

```js
// Implication Operator
function implication(p, q) {
  return !p || q;
}

// Example usage
const raining = true;
const groundWet = true;

const implicationResult = implication(raining, groundWet);
console.log(implicationResult); // Output: true
```

---

## Contoh

```js
// Equivalence Operator
function equivalence(p, q) {
  return (p && q) || (!p && !q);
}

const allCatsAreAnimals = true;
const allAnimalsAreCats = false;

const result = equivalence(allCatsAreAnimals, allAnimalsAreCats);
console.log(result); // Output: false
```
