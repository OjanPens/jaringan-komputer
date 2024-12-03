### HTTP/1.1
1. Koneksi Persisten:
Dalam HTTP/1.1, koneksi TCP tetap terbuka setelah server mengirimkan respons. Hal ini memungkinkan permintaan dan respons berikutnya antara klien dan server menggunakan koneksi yang sama.
Satu halaman web (seperti file HTML dasar dan 10 gambar di dalamnya) dapat dikirim melalui satu koneksi TCP persisten.
Beberapa halaman web di server yang sama juga dapat dikirimkan ke klien melalui koneksi TCP persisten yang sama.
2. Pipelining: Klien dapat mengirim permintaan secara berurutan tanpa harus menunggu respons dari permintaan sebelumnya, dan server dapat mengirimkan respons secara berurutan.
Server biasanya menutup koneksi jika tidak ada aktivitas dalam jangka waktu tertentu (dapat dikonfigurasi).
3. Metode HTTP:
HTTP/1.1 mendukung metode seperti GET, POST, PUT, dan DELETE.

### HTTP/2
1. Multiple Response:
HTTP/2 memungkinkan server mengirimkan banyak respons untuk satu permintaan klien.
Sebagai contoh, jika klien meminta halaman HTML dasar, server dapat menganalisis halaman tersebut untuk mengidentifikasi objek-objek yang diperlukan (seperti gambar, CSS, dan JavaScript).
Server kemudian dapat langsung mengirimkan objek-objek tersebut ke klien tanpa menunggu permintaan eksplisit dari klien (server push).
2. Efisiensi:
Fitur ini membantu mengurangi waktu loading halaman karena objek yang diperlukan sudah dikirimkan sebelumnya.

### HTTP/3
1. Dibangun di Atas QUIC:
HTTP/3 dirancang untuk berjalan di atas protokol QUIC, yang merupakan protokol "transport" baru yang diimplementasikan pada lapisan aplikasi di atas protokol UDP.
QUIC menawarkan fitur seperti:
- Multiplexing pesan: Memungkinkan pesan dari berbagai aliran data diinterleaving tanpa saling mengganggu.
- Kontrol aliran per aliran: Membatasi data yang bisa dikirim di tiap aliran untuk mencegah kelebihan beban.
- Establish koneksi dengan latensi rendah: Mengurangi waktu yang diperlukan untuk membangun koneksi.
- Sederhana dan Efisien:
Banyak fitur HTTP/2, seperti interleaving pesan, sudah didukung langsung oleh QUIC. Hal ini memungkinkan desain HTTP/3 menjadi lebih sederhana dan efisien.
2. Status Standar:
Per tahun 2020, HTTP/3 masih dalam bentuk draft Internet dan belum sepenuhnya distandarisasi.

