---
term: BIP119

---
Memperkenalkan sebuah opcode baru bernama `OP_CHECKTEMPLATEVERIFY` (CTV). CTV akan memungkinkan pembuatan perjanjian non-rekursif dalam transaksi, untuk memaksakan kondisi spesifik tentang bagaimana koin tertentu dapat digunakan, termasuk dalam transaksi di masa depan. Lebih konkretnya, ini akan memungkinkan definisi kondisi pada `scriptPubKey` dari output transaksi berdasarkan `scriptPubKey` dari UTXO yang dibelanjakan sebagai input. CheckTemplateVerify didesain untuk menjadi sederhana dan tanpa status dinamis. Implementasinya bertujuan untuk memperluas kemampuan skrip Bitcoin untuk memfasilitasi berbagai aplikasi seperti kontrol kemacetan transaksi, pembuatan saluran pembayaran non-interaktif, DLC, kumpulan pembayaran ... Opcode baru ini akan diperkenalkan sebagai pengganti `OP_NOP4`. Perubahan ini akan mengimplikasikan sebuah soft fork.