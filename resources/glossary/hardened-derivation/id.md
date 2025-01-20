---
term: TURUNAN YANG DIKERASKAN

---
Proses pembuatan kunci anak di dompet HD. Derivasi yang diperkeras menggunakan kunci pribadi induk sebagai input untuk fungsi `HMAC-SHA512`, sehingga tidak memungkinkan untuk membuat kunci publik anak dari kunci publik induk dan kode rantai induk. Proses ini melibatkan penggabungan kunci privat induk dan indeks yang lebih besar dari atau sama dengan $2^{31}$, diikuti dengan penerapan `HMAC-SHA512` dengan kode rantai induk. Hasilnya dibagi menjadi dua bagian: 256 bit pertama ditambahkan ke kunci privat induk untuk mendapatkan kunci privat anak, sedangkan 256 bit sisanya membentuk kode rantai anak. Metode ini memastikan bahwa walaupun kunci publik yang diperluas dikompromikan, kunci tersebut tidak dapat digunakan untuk mendapatkan kunci publik anak. Pada derivasi standar, derivasi yang diperkeras digunakan pada semua tingkat derivasi hingga kedalaman akun. Dalam notasi jalur derivasi, derivasi yang diperkeras diidentifikasi dengan tanda kutip `` atau lebih jarang dengan `h`.