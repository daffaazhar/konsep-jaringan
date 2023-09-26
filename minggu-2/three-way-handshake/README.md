# Three-Way Handshake

Dalam dunia jaringan komputer, koneksi antara dua perangkat, seperti komputer atau server, dibangun dengan menggunakan apa yang dikenal sebagai "tiga tahap perkenalan" atau dalam bahasa Inggris dikenal sebagai "three-way handshaking". Konsep ini adalah dasar dari protokol Transmission Control Protocol (TCP) yang banyak digunakan dalam komunikasi jaringan.

<img src="assets/illustration.jpg">

Tiga tahap perkenalan merujuk pada proses tiga langkah yang harus dilalui untuk memastikan bahwa kedua perangkat siap untuk memulai pertukaran data. Proses ini memastikan bahwa komunikasi dapat berlangsung dengan benar dan andal. Berikut adalah penjelasan rinci tentang masing-masing tahap dalam pembentukan koneksi menggunakan tiga tahap perkenalan:

### Tahap 1: Permintaan Sinkronisasi (SYN)

1. Perangkat A (biasanya disebut pengirim) ingin memulai koneksi dengan Perangkat B (penerima).
2. Perangkat A mengirimkan pesan khusus yang disebut "Permintaan Sinkronisasi" atau "SYN" ke Perangkat B.
3. Pesan SYN ini berisi nomor urutan yang digunakan untuk mengidentifikasi data dalam koneksi dan nomor acak yang disebut "nomor acak awal".

### Tahap 2: Balasan Sinkronisasi dan Permintaan Sinkronisasi (SYN-ACK)

1. Perangkat B menerima pesan SYN dari Perangkat A dan merespons dengan mengirimkan pesan khusus yang disebut "Balasan Sinkronisasi dan Permintaan Sinkronisasi" atau "SYN-ACK".
2. Pesan SYN-ACK ini berisi nomor urutan yang digunakan oleh Perangkat B, nomor urutan dari pesan SYN yang diterima, dan juga nomor acak yang berbeda.
3. Dengan mengirimkan SYN-ACK, Perangkat B juga menunjukkan bahwa ia bersedia untuk menerima data dari Perangkat A.

### Tahap 3: Balasan Sinkronisasi (ACK)

1. Setelah menerima pesan SYN-ACK dari Perangkat B, Perangkat A mengirimkan balasan kembali yang disebut "Balasan Sinkronisasi" atau "ACK".
2. Pesan ACK ini berisi nomor urutan yang disesuaikan, menandakan bahwa Perangkat A telah menerima pesan SYN-ACK dan koneksi telah berhasil dibuat.
3. Pada tahap ini, koneksi telah dibentuk dan pertukaran data antara kedua perangkat dapat dimulai.

Tiga tahap perkenalan ini memastikan bahwa kedua perangkat memiliki informasi yang diperlukan untuk mengatur aliran data dengan benar. Jika salah satu pesan tidak berhasil mencapai tujuan atau terjadi masalah lain, proses tiga tahap perkenalan akan diulang hingga koneksi berhasil dibentuk. Dengan cara ini, protokol TCP memastikan bahwa koneksi yang stabil dan handal dapat terjaga dalam lingkungan jaringan yang berubah-ubah.
