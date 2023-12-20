---
marp: true
theme: one
---

# Apa itu Pemrograman?

---

## Apa itu Pemrograman?

Pemrograman adalah pembuatan program komputer yang dapat dieksekusi untuk mencapai tugas tertentu. Proses ini melibatkan penggunaan bahasa pemrograman untuk berkomunikasi instruksi kepada komputer.

---

## Konsep Pemrograman

- **Variabel:** Lokasi penyimpanan simbolis yang menyimpan nilai data.
- **Alur Kontrol:** Urutan eksekusi pernyataan, dikendalikan oleh kondisi dan perulangan.
- **Fungsi:** Blok kode yang dapat digunakan kembali untuk tugas tertentu.
- **Tipe Data:** Klasifikasi data yang menentukan nilai variabel (contoh: angka, string).

---

## Struktur Dasar Program

- **Input:** Mendapatkan data dari pengguna, file, sensor, atau sumber lain.
- **Kontrol:** Mengatur alur eksekusi program berdasarkan kondisi dan perulangan.
- **Proses:** Melakukan operasi pada data, seperti perhitungan matematika atau manipulasi data.
- **Output:** Menampilkan data yang telah diproses kepada pengguna, atau menyimpannya ke file atau sumber lain.

---

## Istilah Pemrograman

- **Program:** Serangkaian instruksi yang dieksekusi oleh komputer untuk menyelesaikan tugas tertentu.
- **Kode:** Instruksi yang ditulis dalam bahasa pemrograman.
- **Kompilasi:** Proses menerjemahkan kode menjadi kode mesin yang dapat dieksekusi.
- **Eksekusi:** Proses menjalankan kode mesin oleh komputer.
- **Debugging:** Proses mengidentifikasi dan memperbaiki kesalahan dalam kode.

---

## Bahasa Pemrograman

Seperangkat aturan yang memfasilitasi komunikasi antara manusia dan komputer. Komponen kunci termasuk sintaksis, semantik, variabel, struktur kontrol, fungsi, dan pustaka/kerangka kerja.

---

## Bahasa Pemrograman Populer

| Web Development | Mobile Development | Data Science | Systems Programming | Game Development |
| --------------- | ------------------ | ------------ | ------------------- | ---------------- |
| JavaScript      | Java (Android)     | Python       | C++                 | C++              |
| TypeScript      | Swift (iOS)        | R            | Rust                | C#               |
| PHP             | Kotlin (Android)   | Julia        | Go                  |                  |
| Ruby            | Objective-C (iOS)  |              |                     |                  |
| Python          | Dart (Flutter)     |              |                     |                  |
| Go              |                    |              |                     |                  |
| Dart            |                    |              |                     |                  |

---

## Komponen Kunci Bahasa Pemrograman

- **Sintaksis:** Aturan yang mengatur struktur program.
- **Semantik:** Arti di balik sintaksis, menentukan perilaku program.
- **Variabel dan Tipe Data:** Mendefinisikan dan memanipulasi data.
- **Struktur Kontrol:** Mengelola alur program.
- **Fungsi atau Prosedur:** Unit kode modular untuk tugas tertentu.
- **Pustaka dan Kerangka Kerja:** Kode pra-ditulis untuk fungsionalitas umum.

---

## Contoh Sintaks Bahasa Pemrograman

```js
// JavaScript: Print "Hello, World!"
console.log("Hello, World!");

// JavaScript: Conditional statement
let y = 8;
if (y > 5) {
  console.log("y is greater than 5");
} else {
  console.log("y is not greater than 5");
}

// JavaScript: Loop
for (let j = 0; j < 3; j++) {
  console.log(j);
}
```

---

## Contoh Sintaks Bahasa Pemrograman

```python
# Python: Print "Hello, World!"
print("Hello, World!")

# Python: Conditional statement
x = 10
if x > 5:
    print("x is greater than 5")
else:
    print("x is not greater than 5")

# Python: Loop
for i in range(3):
    print(i)
```

---

## Contoh Sintaks Bahasa Pemrograman

```java
// Java: Print "Hello, World!"
System.out.println("Hello, World!");

// Java: Conditional statement
int z = 7;
if (z > 5) {
    System.out.println("z is greater than 5");
} else {
    System.out.println("z is not greater than 5");
}

// Java: Loop
for (int k = 0; k < 3; k++) {
    System.out.println(k);
}
```

---

## Contoh Sintaks Bahasa Pemrograman

```c
// C: Print "Hello, World!"
printf("Hello, World!");

// C: Conditional statement
int a = 6;
if (a > 5) {
    printf("a is greater than 5");
} else {
    printf("a is not greater than 5");
}

// C: Loop
for (int b = 0; b < 3; b++) {
    printf("%d", b);
}
```

---

## Contoh Fungsi Bahasa Pemrograman

```js
// JavaScript: Function definition
function greet(name) {
  return `Hello, ${name}!`;
}

// JavaScript: Function call
let result = greet("Bob");
console.log(result);
```

---

## Contoh Fungsi Bahasa Pemrograman

```python
# Python: Function definition
def greet(name):
    return f"Hello, {name}!"

# Python: Function call
result = greet("Alice")
print(result)
```

---

## Contoh Fungsi Bahasa Pemrograman

```java
// Java: Function definition
public class Greeting {
    static String greet(String name) {
        return "Hello, " + name + "!";
    }

    public static void main(String[] args) {
        // Java: Function call
        String result = greet("Charlie");
        System.out.println(result);
    }
}

```

---

## Perbedaan Antara Library dan Framework

|                | Library                                                                 | Framework                                                                         |
| -------------- | ----------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| **Definisi**   | Kumpulan kode yang dapat digunakan kembali oleh program-program berbeda | Seperangkat aturan, konvensi, dan tools yang mengatur struktur dan alur aplikasi  |
| **Penggunaan** | Untuk tugas spesifik, dipilih fleksibel                                 | Membangun struktur aplikasi secara besar, struktur dan interaksi sudah ditentukan |
| **Kontrol**    | Pengembang memiliki lebih banyak kontrol atas alur program              | Pengembang menyerahkan sejumlah besar kontrol kepada framework.                   |
| **Contoh**     | React, VueJS, JQuery                                                    | Next.js, Nuxt.js, Express.js                                                      |

---

## Jenis Bahasa Pemrograman

- **Low Level Language:** Lebih dekat ke kode mesin (contoh: Assembly).
- **High Level Language:** Menyediakan abstraksi untuk memudahkan manusia dalam membaca maupun menulis kode (contoh: Python, Java).
- **Compiled Language:** Kode diterjemahkan menjadi kode mesin sebelum eksekusi untuk kinerja lebih cepat (contoh: C, C++).
- **Interpreted Language:** Kode dieksekusi baris per baris saat runtime (contoh: Python, JavaScript).

---

## Assembly Language

```asm

section .data
    hello db 'Hello, World!',0

section .text
    global _start

_start:
    ; write system call
    mov eax, 4
    mov ebx, 1
    mov ecx, hello
    mov edx, 13
    int 0x80

    ; exit system call
    mov eax, 1
    xor ebx, ebx
    int 0x80
```

---

## Paradigma Pemrograman

Paradigma pemrograman adalah gaya atau pendekatan pemrograman, yang mendefinisikan cara seorang programmer mendesain solusi untuk suatu masalah. Paradigma ini menyediakan seperangkat aturan dan panduan untuk menyusun kode, menentukan alur program, dan mengimplementasikan sebuah algoritma.

---

## Paradigma Pemrograman Umum

- **Pemrograman Fungsional:** Menggunakan fungsi untuk mengubah data (contoh: Haskell, Clojure).
- **Pemrograman Berorientasi Objek:** Mengandalkan objek, kelas, dan metode (contoh: Java, C++).
- **Pemrograman Prosedural:** Menggunakan prosedur atau rutin untuk operasi data (contoh: C, Pascal).

---

## Paradigma Pemrograman Umum (lanjutan)

- Pemilihan bahasa dan paradigma pemrograman bergantung pada sifat proyek, persyaratan kinerja, dan preferensi tim pengembangan.

- Sebagian besar bahasa pemrograman mendukung lebih dari satu paradigma pemrograman.
