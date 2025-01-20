---
term: BIP68

---
Memperkenalkan kemampuan untuk menggunakan waktu penguncian relatif melalui bidang `nSequence`. Hal ini memungkinkan sebuah transaksi untuk menentukan penundaan relatif sebelum transaksi tersebut dapat dimasukkan ke dalam sebuah blok. Penundaan ini dapat ditentukan dalam jumlah blok, atau sebagai kelipatan 512 detik (yaitu, waktu nyata). Perhatikan bahwa interpretasi baru dari bidang `nSequence` ini hanya valid jika bidang `nVersion` lebih besar atau sama dengan `2`. Interpretasi bidang `nSequence` ini terjadi pada tingkat aturan konsensus Bitcoin. Penguncian waktu relatif menetapkan penundaan mulai dari penerimaan transaksi sebelumnya, sedangkan penguncian waktu absolut menentukan waktu yang tepat sebelum transaksi tidak dapat dimasukkan ke dalam blok. BIP68 diperkenalkan melalui soft fork pada tanggal 4 Juli 2016, bersamaan dengan BIP112 dan BIP113, yang diaktifkan pertama kali menggunakan metode BIP9.