### Pengertian SMTP
SMTP (Simple Mail Transfer Protocol) adalah protokol standar yang digunakan untuk mengirimkan email melalui internet. SMTP bertanggung jawab untuk mengirimkan pesan dari email client (misalnya, aplikasi seperti Outlook atau Thunderbird) ke server email penerima, atau dari satu server email ke server email lainnya.

### Alur Kerja SMTP

Proses SMTP:
1. Pengiriman Pesan oleh Alice: Alice membuka aplikasi email (user agent), memasukkan alamat email Bob (misalnya, bob@someschool.edu), menulis pesan, dan mengirimkannya.

2. Pesan Dikirim ke Mail Server Alice: Aplikasi email Alice mengirimkan pesan tersebut ke mail server miliknya, yang kemudian menempatkan pesan dalam antrean pengiriman.

3. SMTP Client Membuka Koneksi: Bagian client dari SMTP di mail server Alice mendeteksi pesan di antrean, lalu membuka koneksi TCP ke server SMTP di mail server Bob.

4. Pengiriman Pesan melalui Koneksi TCP: Setelah melakukan proses SMTP handshaking, SMTP client mengirimkan pesan Alice melalui koneksi TCP.

5. Pesan Diterima oleh Mail Server Bob: Bagian server dari SMTP di mail server Bob menerima pesan tersebut dan menempatkannya di kotak masuk Bob.

6. Bob Membaca Pesan: Bob membuka aplikasi emailnya (user agent) untuk membaca pesan yang telah diterima, sesuai waktunya

### Protokol Pendukung
SMTP hanya mengurus pengiriman email. Protokol seperti IMAP (Internet Message Access Protocol) atau POP3 (Post Office Protocol) digunakan untuk menerima atau mengambil email dari server tujuan.
