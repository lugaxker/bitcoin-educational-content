---
jangka waktu CPFP (ANAK MEMBAYAR UNTUK ORANG TUA)

---
Sebuah mekanisme transaksi yang bertujuan untuk mempercepat konfirmasi transaksi Bitcoin, mirip dengan apa yang dilakukan oleh Replace-by-Fee (RBF), tetapi dari sisi penerima. Ketika sebuah transaksi dengan biaya yang terlalu rendah dibandingkan dengan pasar tetap terjebak dalam kumpulan node dan tidak terkonfirmasi dengan cukup cepat, penerima dapat melakukan transaksi baru, menggunakan bitcoin yang diterima dalam transaksi yang diblokir, meskipun belum terkonfirmasi. Transaksi kedua ini membutuhkan transaksi pertama yang akan ditambang untuk dikonfirmasi. Dengan demikian, penambang dipaksa untuk menyertakan kedua transaksi tersebut secara bersamaan. Transaksi kedua akan mengalokasikan lebih banyak biaya transaksi dibandingkan transaksi pertama, sedemikian rupa sehingga biaya rata-rata mendorong para penambang untuk menyertakan kedua transaksi tersebut. Transaksi anak (yang kedua) membayar transaksi induk yang macet (yang pertama). Inilah mengapa hal ini disebut sebagai "CPFP"

Dengan demikian, CPFP memungkinkan penerima untuk mendapatkan dana mereka lebih cepat meskipun biaya awal yang dikeluarkan oleh pengirim rendah, tidak seperti RBF (*Replace-By-Fee*), yang memungkinkan pengirim untuk mengambil inisiatif untuk mempercepat transaksi mereka sendiri dengan meningkatkan biaya.