---
term: RELAI BLOK KOMPAK

---
Protokol yang diperkenalkan di Bitcoin Core pada tahun 2016 melalui BIP152, yang mengusulkan sebuah metode penghematan bandwidth untuk node jaringan. Compact Block Relay memungkinkan komunikasi informasi blok dengan cara yang ringkas, berdasarkan asumsi bahwa node telah memiliki sebagian besar transaksi dari blok terbaru dalam mempool mereka. Daripada mengirimkan setiap transaksi secara penuh, yang akan mengakibatkan duplikasi, Compact Block Relay mengusulkan untuk mengirimkan hanya pengidentifikasi singkat untuk transaksi yang sudah diketahui oleh rekan-rekannya, disertai dengan beberapa transaksi yang dipilih (terutama transaksi coinbase dan transaksi yang kemungkinan tidak diketahui oleh node). Node kemudian dapat meminta transaksi yang hilang dari rekan-rekannya. Compact Block Relay dengan demikian mengurangi jumlah data yang dipertukarkan selama penyebaran blok, yang pada gilirannya menurunkan lonjakan bandwidth dan meningkatkan efisiensi jaringan secara keseluruhan.