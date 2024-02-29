---
marp: true
theme: one
class:
  - lead
  - invert
---

# **Desain Database: Gambaran Umum**

---

## Model Konseptual, Logis, & Fisik

- Bagian kunci dari desain database
- Masing-masing memiliki tujuan unik
- Langkah yang berbeda untuk setiap model

---

## 1. Model Konseptual

### **Tujuan**

- Menetapkan entitas, atribut, dan hubungan tingkat tinggi

### **Langkah-langkah**

1. **Identifikasi Entitas**
   - Objek/konsep utama dalam domain
2. **Definisikan Hubungan**
   - Cara entitas saling berhubungan
3. **Identifikasi Atribut Kunci**
   - Karakteristik kunci setiap entitas
4. **Buat Diagram**
   - ERD dengan entitas, hubungan, atribut

---

## 2. Model Logis

### **Tujuan**

- Memperhalus entitas/hubungan dari Model Konseptual
- Lebih detail, masih independen sistem

### **Langkah-langkah**

1. **Rincikan Entitas/Atribut**
   - Sertakan semua bidang relevan
2. **Definisikan Kunci Utama**
   - Tetapkan kunci utama untuk setiap entitas
3. **Tetapkan Kunci Asing**
   - Untuk hubungan antar entitas
4. **Normalisasi Data**
   - Terapkan aturan normalisasi
5. **Perhalus Hubungan**
   - Spesifikasikan kardinalitas, opsi
6. **Buat Diagram Detail**
   - ERD terbaru dengan semua atribut, kunci

---

## 3. Model Fisik

### **Tujuan**

- Model untuk implementasi dalam sistem database
- Termasuk detail penyimpanan fisik

### **Langkah-langkah**

1. **Spesifikasi Tabel/Kolom**
   - Terjemahkan entitas ke tabel, atribut ke kolom
2. **Definisikan Tipe Data**
   - Tetapkan tipe data untuk setiap kolom
3. **Tentukan Indeks**
   - Strategi pengindeksan untuk kinerja
4. **Terapkan Batasan**
   - NOT NULL, UNIQUE, CHECK, dll.
5. **Desain Penyimpanan Fisik**
   - Partisi, pengelompokan, organisasi file
6. **Buat Skrip Database**
   - Skrip SQL atau alat desain untuk implementasi

---

## Kolaborasi & Alat

- Bekerjasama erat dengan pemangku kepentingan
- Pastikan model memenuhi kebutuhan bisnis
- Gunakan alat: perangkat lunak ERD, alat UML, alat desain database
