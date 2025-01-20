---
term: GABUNG BAYAR

---
Sebuah struktur transaksi Bitcoin khusus yang meningkatkan privasi pengguna selama melakukan pembelanjaan dengan berkolaborasi dengan penerima pembayaran. Keunikan Payjoin terletak pada kemampuannya untuk menghasilkan sebuah transaksi yang sekilas terlihat biasa namun sebenarnya merupakan sebuah coinjoin mini antara dua pihak. Untuk itu, struktur transaksi melibatkan penerima pembayaran dalam input di samping pengirim yang sebenarnya. Dengan demikian, penerima menyertakan pembayaran untuk diri mereka sendiri di tengah-tengah transaksi yang memungkinkan mereka untuk dibayar. Misalnya, jika Anda membeli baguette seharga `6.000 sats` menggunakan UTXO sebesar `10.000 sats`, dan Anda memilih Payjoin, pembuat roti Anda akan menambahkan UTXO sebesar `15.000 sats` milik mereka sebagai input, yang akan mereka terima secara penuh sebagai output, selain `6.000 sats` Anda.

Transaksi Payjoin memenuhi dua tujuan. Pertama, bertujuan untuk menyesatkan pengamat eksternal dengan menciptakan umpan dalam analisis rantai pada Common Input Ownership Heuristic (CIOH). Biasanya, ketika sebuah transaksi pada blockchain memiliki beberapa input, diasumsikan bahwa semua input tersebut kemungkinan besar adalah milik entitas yang sama. Dengan demikian, ketika seorang analis memeriksa transaksi Payjoin, mereka akan percaya bahwa semua input berasal dari orang yang sama. Akan tetapi, persepsi ini tidak benar karena penerima pembayaran juga berkontribusi pada input bersama dengan pembayar yang sebenarnya. Kedua, Payjoin juga menipu pengamat eksternal tentang jumlah pembayaran yang sebenarnya dilakukan. Dengan memeriksa struktur transaksi, analis mungkin percaya bahwa pembayaran tersebut setara dengan jumlah salah satu output. Pada kenyataannya, jumlah pembayaran tidak sesuai dengan salah satu output. Ini sebenarnya adalah perbedaan antara UTXO penerima dalam output dan UTXO penerima dalam input. Dalam hal ini, transaksi Payjoin masuk ke dalam ranah steganografi. Hal ini memungkinkan untuk menyembunyikan jumlah transaksi yang sebenarnya di dalam sebuah transaksi palsu yang bertindak sebagai umpan.

![](../../dictionnaire/assets/14.webp)

> ► *Payjoin juga terkadang disebut "P2EP (Pay-to-End-Point)", "Penumpang gelap", atau "transaksi steganografi".*