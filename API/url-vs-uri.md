---
marp: true
theme: one
---

## Perbedaan URL dan URI

- URL (Uniform Resource Locator) dan URI (Uniform Resource Identifier) adalah dua istilah yang sering digunakan dalam pengembangan web.
- Keduanya digunakan untuk mengidentifikasi sumber daya, tetapi ada beberapa perbedaan penting di antara keduanya.

---

## URI

- URI mengidentifikasi sumber daya tanpa harus menyediakan informasi tentang cara mengaksesnya.
- URI dapat menggunakan berbagai skema, termasuk skema yang tidak biasanya terkait dengan akses jaringan.
- URI adalah istilah yang lebih luas yang mencakup URL dan cara lain untuk mengidentifikasi sumber daya.

---

## Contoh URI

```
urn:isbn:0-471-11709-9

tel:+1-816-555-1212

mailto:john@example.com
```

---

## URL

URL adalah jenis URI yang digunakan untuk mengidentifikasi sumber daya di internet. URL terdiri dari beberapa bagian, yaitu:

- **Protokol:** Mekanisme yang digunakan untuk mengakses sumber daya, seperti HTTP, HTTPS, atau FTP.
- **Host:** Nama domain atau alamat IP server yang hosting sumber daya.
- **Path:** Lokasi sumber daya di dalam sistem file server.
- **Query string:** Parameter opsional yang dapat diteruskan ke sumber daya.
- **Fragment identifier:** Identitas opsional untuk bagian tertentu dari sumber daya.

---

## Contoh URL:

```
https://www.example.com/path/to/resource?query=value#fragment
```

---

## Perbedaan Utama

| Fitur      | URL                                          | URI                                               |
| ---------- | -------------------------------------------- | ------------------------------------------------- |
| Fokus      | Lokasi sumber daya                           | Identifikasi sumber daya                          |
| Skema      | Selalu protokol jaringan (HTTP, HTTPS, dll.) | Dapat berupa protokol atau skema lain (urn, data) |
| Penggunaan | Utamanya untuk mengakses sumber daya web     | Dapat digunakan dalam berbagai konteks            |
