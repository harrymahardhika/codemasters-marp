---
marp: true
theme: one
---

# Prinsip Pengembangan Perangkat Lunak

---

# Pentingnya Prinsip Desain dalam Pengembangan Perangkat Lunak

1. **Memastikan Kualitas Kode:** Prinsip desain membantu pengembang menulis kode yang tidak hanya berfungsi dengan baik tetapi juga mudah dipahami, diuji, dan dipelihara. Ini penting untuk memastikan kualitas jangka panjang dari suatu aplikasi atau sistem.
2. **Mengurangi Kompleksitas:** Dengan mengikuti prinsip seperti SRP dan SoC, kompleksitas dalam kode dapat dikurangi. Ini membuatnya lebih mudah untuk mengidentifikasi, mengisolasi, dan memperbaiki bug, serta memperbarui atau memodifikasi fungsi tanpa mengganggu keseluruhan sistem.

---

# Pentingnya Prinsip Desain dalam Pengembangan Perangkat Lunak

3. **Meningkatkan Fleksibilitas dan Skalabilitas:** Prinsip seperti OCP dan DIP memungkinkan sistem menjadi lebih fleksibel dan skalabel, memudahkan integrasi fitur baru dan adaptasi terhadap kebutuhan yang berubah.
4. **Memfasilitasi Kolaborasi:** Dalam lingkungan kerja tim, prinsip desain memastikan bahwa kode yang ditulis oleh satu orang dapat dengan mudah dipahami dan digunakan oleh orang lain, yang penting untuk kerjasama yang efisien.

---

# Tujuan dari Penggunaan Prinsip-Prinsip Desain

1. **Meningkatkan Efisiensi Pengembangan:** Dengan mengurangi waktu yang dibutuhkan untuk memahami dan memodifikasi kode, prinsip desain membantu meningkatkan efisiensi dalam proses pengembangan.
2. **Mendorong Reusability:** Prinsip seperti DRY mendorong pengembangan komponen yang dapat digunakan kembali, mengurangi pengulangan kerja dan mempercepat proses pembangunan fitur.

---

# Tujuan dari Penggunaan Prinsip-Prinsip Desain

3. **Mengurangi Biaya Pemeliharaan:** Kode yang ditulis dengan baik dan terstruktur dengan baik memerlukan lebih sedikit pemeliharaan dan perbaikan, yang berarti mengurangi biaya jangka panjang.
4. **Mempersiapkan Aplikasi untuk Masa Depan:** Dengan menggunakan prinsip desain yang baik, aplikasi menjadi lebih mudah untuk diperbarui dan disesuaikan dengan teknologi yang muncul dan kebutuhan pasar yang berubah.

Dengan memahami dan menerapkan prinsip-prinsip desain ini, pengembang dapat menciptakan perangkat lunak yang tidak hanya berfungsi dengan baik tetapi juga mudah dipelihara dan diperbarui, serta memuaskan kebutuhan pengguna saat ini dan masa depan.

---

# Prinsip Pengembangan Perangkat Lunak

**SOLID Principles**

- SRP - Single Responsibility Principle
- OCP - Open/Closed Principle
- LSP - Liskov Substitution Principle
- ISP - Interface Segregation Principle
- DIP - Dependency Inversion Principle

---

# SOLID

## Single Responsibility Principle (SRP)

- Setiap kelas atau modul harus memiliki satu tanggung jawab yang jelas dan terdefinisi dengan baik.
- Manfaat: Mempermudah pemahaman, pemeliharaan, dan pengujian kode.

---

# SOLID

## Open/Closed Principle (OCP)

- Entitas perangkat lunak (kelas, modul, fungsi) harus terbuka untuk ekstensi, tetapi tertutup untuk modifikasi.
- Manfaat: Memungkinkan penambahan fungsionalitas baru tanpa mengubah kode yang ada.

---

# SOLID

## Liskov Substitution Principle (LSP)

- Subtipe harus dapat menggantikan tipe dasarnya tanpa mengubah kebenaran program.
- Manfaat: Objek dapat diganti dengan subtipe-nya tanpa merusak fungsionalitas.

---

# SOLID

## Interface Segregation Principle (ISP)

- Klien tidak seharusnya dipaksa untuk bergantung pada antarmuka yang tidak mereka gunakan.
- Manfaat: Memecah antarmuka besar menjadi lebih kecil dan spesifik.

---

# SOLID

## Dependency Inversion Principle (DIP)

- Bergantung pada abstraksi, bukan konkrit.
- Manfaat: Kode harus bergantung pada antarmuka dan kelas abstrak, bukan implementasi konkrit.

---

# Prinsip Pengembangan Perangkat Lunak

**General Principles**

- DRY - Don't Repeat Yourself
- KISS - Keep It Simple, Stupid
- YAGNI - You Aren't Gonna Need It
- SSOT - Single Source of Truth
- SoC - Separation of Concerns

---

# Don't Repeat Yourself (DRY)

- Hindari menduplikasi kode.
- Manfaat: Jika Anda membutuhkan fungsionalitas yang sama di beberapa tempat, refaktor menjadi fungsi, kelas, atau modul yang dapat digunakan kembali.

---

# Keep It Simple, Stupid (KISS)

- Berusaha untuk membuat kode yang sederhana dan mudah dipahami.
- Manfaat: Hindari kompleksitas yang tidak perlu dan pilih solusi yang mudah dipahami dan dipelihara.

---

# Keep It Simple, Stupid (KISS)

```javascript
// Sebelum menerapkan KISS
function joinStrings(stringsArray) {
  let result = ''
  for (let i = 0; i < stringsArray.length; i++) {
    result += stringsArray[i]
    if (i < stringsArray.length - 1) {
      result += ', '
    }
  }
  return result
}

// Setelah menerapkan KISS
function joinStrings(stringsArray) {
  return stringsArray.join(', ')
}
```

---

# You Aren't Gonna Need It (YAGNI)

- Jangan menulis kode untuk fitur yang Anda tidak butuhkan saat ini.
- Manfaat: Fokus pada pembangunan fitur yang Anda butuhkan terlebih dahulu, lalu tambahkan lainnya sesuai kebutuhan.

---

# You Aren't Gonna Need It (YAGNI)

```javascript
// Sebelum menerapkan YAGNI
function calculateArea(width, height, unit) {
  // Kode untuk mengkonversi unit tidak diperlukan saat ini
  // Konversi unit
  if (unit === 'cm') {
    width = width / 100
  }

  if (unit === 'm') {
    width = width * 100
  }

  return width * height
}
```

---

# You Aren't Gonna Need It (YAGNI)

```javascript
// Setelah menerapkan YAGNI
function calculateArea(width, height) {
  return width * height // Fokus hanya pada kebutuhan saat ini
}
```

---

# Single Source of Truth (SSOT)

- Pastikan data disimpan dan dipelihara hanya di satu tempat.
- Manfaat: Menghindari inkonsistensi dan kesalahan.

---

# Separation of Concerns (SoC)

- Pisahkan aspek-aspek berbeda dari kode Anda ke dalam modul atau kelas yang berbeda.
- Manfaat: Memudahkan pemahaman, pemeliharaan, dan pengujian kode.

---

# Separation of Concerns (SoC)

```javascript
// Sebelum menerapkan SoC
class User {
  constructor(name, email) {
    this.name = name
    this.email = email
  }

  validateEmail() {
    // Validasi email
  }

  saveUser() {
    // Simpan user ke database
  }
}
```

---

# Separation of Concerns (SoC)

```javascript
// Setelah menerapkan SoC
class User {
  constructor(name, email) {
    this.name = name
    this.email = email
  }
}

class UserValidator {
  static validateEmail(email) {
    // Validasi email
  }
}

class UserDatabase {
  static saveUser(user) {
    // Simpan user ke database
  }
}
```

---

# Readability

Prioritaskan kode yang jelas, mudah dibaca dan dipahami oleh manusia, serta terdokumentasi dengan baik.

```javascript
// sebelum
function area(w, h) {
  return w * h
}
```

---

# Readability

```javascript
// setelah
/**
 * Menghitung luas persegi panjang.
 * @param {number} width - Lebar persegi panjang.
 * @param {number} height - Tinggi persegi panjang.
 * @returns {number} Luas persegi panjang.
 */
function calculateArea(width, height) {
  return width * height
}
```
