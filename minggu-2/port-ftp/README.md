## Apa Itu FTP?

FTP (File Transfer Protocol) adalah layanan internet yang dirancang untuk membuat sambungan ke server internet tertentu atau komputer, sehingga user dapat mengirimkan file ke komputer (download) atau mengirimkan file ke server (upload). FTP server adalah hal yang saat ini banyak digunakan untuk melakukan pertukaran data, karena lebih mudah daripada menggunakan perangkat kabel atau fisik.

## Mengapa dalam Satu Port FTP Terdapat 2 Protokol TCP dan UDP?

Pertanyaan yang mungkin muncul adalah mengapa dalam satu port FTP bisa terdapat dua protokol, yakni TCP (Transmission Control Protocol) dan UDP (User Datagram Protocol)? Untuk menjawabnya, kita perlu memahami struktur kerja FTP dan kegunaan masing-masing protokol tersebut.

FTP, atau <i>File Transfer Protocol</i>, adalah protokol yang digunakan untuk mentransfer file antara client dan server di dalam jaringan komputer. Dalam kebanyakan kasus, FTP menggunakan protokol TCP sebagai protokol transport utama. TCP adalah protokol yang handal, dimana ia menjamin pengiriman data dengan akurasi dan urutan yang tepat. Hal ini dicapai dengan memastikan bahwa data yang dikirimkan mencapai tujuan dengan benar dan dalam urutan yang sesuai.

Namun, terdapat situasi khusus dalam implementasi FTP, terutama dalam mode aktif, dimana protokol UDP juga dapat digunakan bersamaan dengan TCP. Mode aktif FTP melibatkan dua koneksi terpisah antara client dan server: koneksi kontrol dan koneksi data. Koneksi kontrol menggunakan protokol TCP untuk mengatur perintah dan respons antara client dan server, sementara koneksi data digunakan untuk mengirimkan file sebenarnya.

Pada tahap ini, penggunaan protokol UDP dalam koneksi data bisa dipertimbangkan. Hal ini terkait dengan pertimbangan performa dan kecepatan transfer. Dalam situasi di mana kecepatan transfer lebih diutamakan daripada ketepatan mutlak, misalnya dalam streaming video atau audio, protokol UDP dapat diimplementasikan. UDP memiliki sedikit overhead dibandingkan dengan TCP karena tidak melibatkan mekanisme pengiriman ulang untuk memastikan akurasi data. Dengan demikian, UDP bisa memungkinkan transfer data lebih cepat.

Namun, harus ditegaskan bahwa penggunaan UDP dalam mode aktif FTP bukanlah praktik umum atau standar. TCP tetap menjadi pilihan utama dalam banyak situasi karena keandalan dan jaminan pengiriman yang diberikannya. TCP memastikan data dikirimkan dengan benar dan dalam urutan yang tepat, namun dengan sedikit tambahan latensi akibat mekanisme pengiriman ulang.

Kesimpulannya, pemilihan antara penggunaan protokol TCP atau UDP dalam mode aktif FTP sebaiknya didasarkan pada kebutuhan spesifik. Jika kecepatan transfer lebih penting daripada ketepatan mutlak, maka penggunaan UDP bisa dipertimbangkan, namun dengan kesadaran akan risiko kehilangan data atau ketidakurutan. Dalam sebagian besar kasus, FTP masih mengandalkan protokol TCP untuk kedua jenis koneksi, karena keandalan dan akurasi data tetap menjadi prioritas utama dalam transfer file.
