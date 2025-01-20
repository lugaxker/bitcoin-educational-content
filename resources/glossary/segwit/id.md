---
term: SEGWIT

---
SegWit, singkatan dari "Segregated Witness", merupakan sebuah pembaruan protokol Bitcoin yang diperkenalkan pada bulan Agustus 2017. Pembaruan ini bertujuan untuk menyelesaikan beberapa masalah teknis, termasuk masalah kapasitas transaksi jaringan, masalah kelenturan transaksi, dan memfasilitasi modifikasi protokol di masa depan.

Soft fork ini memodifikasi struktur transaksi dengan memindahkan data tanda tangan ke direktori yang terpisah. Secara khusus, dengan SegWit, tanda tangan dihapus dari blok utama dan dimasukkan ke dalam struktur data yang terpisah di akhir blok, yang dikenal sebagai saksi. Pemisahan ini memungkinkan peningkatan kapasitas setiap blok tanpa mengubah ukuran maksimum blok itu sendiri, yaitu 1 MB pada Bitcoin. Perubahan ini juga menyelesaikan masalah kelenturan transaksi. Sebelum SegWit, tanda tangan dapat diubah sebelum transaksi dikonfirmasi, yang mengubah pengenal transaksi. Hal ini menyulitkan pembuatan transaksi yang kompleks, karena transaksi yang belum dikonfirmasi dapat diubah pengenalnya. Dengan memisahkan tanda tangan, SegWit membuat transaksi tidak dapat diubah, karena setiap perubahan pada tanda tangan sekarang hanya mempengaruhi pengenal saksi (WTXID), bukan pengenal transaksi (TXID). Dengan memecahkan masalah kelenturan, SegWit telah membuka jalan untuk pengembangan lebih lanjut di atas sistem Bitcoin, terutama Lightning Network, yang memungkinkan transaksi yang cepat dan murah.