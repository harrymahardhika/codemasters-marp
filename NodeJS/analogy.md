# Analogy of Node.js

Mari kita bayangkan Anda sedang berbisnis warung bakso. Anda ingin menjadi warung bakso yang laris dan efisien, tapi tidak ingin kewalahan sendiri.

**Masalah dengan cara lama (blocking I/O):**

- Anda melayani pelanggan satu per satu. Anda mengambil pesanan, memasak baksonya, baru kemudian melayani pelanggan berikutnya.
- Ini memang memastikan setiap pelanggan diurus dengan baik, tapi antrian jadi panjang dan pelanggan menunggu lama.
- Anda juga tidak bisa melakukan apa-apa sambil menunggu bakso matang, padahal bisa saja ngulek cabai atau ngiris tomat.

**Cara baru yang lebih efisien (non-blocking I/O):**

- Anda mulai menerima pesanan dari banyak pelanggan sekaligus. Anda catat pesanan mereka, lalu langsung menyiapkan bahan-bahan dan panci.
- Sambil menunggu bakso matang, Anda bisa melayani pelanggan lain yang mau pesan es teh atau kerupuk.
- Ketika bakso untuk pelanggan pertama sudah siap, Anda langsung memanggil mereka dan menghitung tagihannya. Ini seperti event yang memicu callback (memanggil fungsi tertentu).
- Pelanggan senang karena tidak perlu menunggu lama, dan Anda juga bisa terus sibuk mengerjakan banyak hal.

**Event-driven programming:**

- Bayangkan ada lonceng kecil di setiap kompor bakso. Ketika bakso matang, loncengnya bunyi. Itulah event!
- Anda tidak perlu terus-terusan mengecek panci, cukup mendengarkan lonceng dan segera beraksi saat bunyi.
- Setiap lonceng punya fungsi sendiri, misalnya memanggil pelanggan yang tepat atau menyiapkan mangkuk. Ini seperti callback function yang spesifik untuk tiap event.

**Kombinasi keduanya:**

- Non-blocking I/O memastikan panci bakso selalu bekerja, dan event-driven programming membuat Anda bisa menangani pelanggan dengan cekatan tanpa menunggu lama.
- Ini seperti punya banyak karyawan terampil yang bekerja sama: satu menerima pesanan, satu menyiapkan bahan, satu merebus bakso, dan satu lagi memanggil pelanggan.

**Keuntungan:**

- Warung Anda bisa melayani lebih banyak pelanggan dengan cepat dan tetap tertib.
- Pelanggan senang karena tidak perlu antri lama.
- Anda dan karyawan tidak perlu bengong menunggu bakso matang, bisa melakukan banyak hal sekaligus.

**Tantangan:**

- Koordinasi antara karyawan dan lonceng harus tepat. Kalau loncengnya rusak atau tidak didengar, bisa kacau.
- Membiasakan diri dengan sistem ini mungkin sedikit lebih sulit daripada cara lama, tapi lama-lama akan terbiasa.

Dengan pendekatan event-driven dan non-blocking I/O, warung bakso Anda bisa jadi yang paling laris dan efisien di sekampung!
