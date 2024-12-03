# C Socket Programming: Simple Server and Client

`server.c` - multithreaded server 

`server_single.c` - singlethreaded server

`client.c` - client

### UDP Socket
![The connect process of UDP Socket]("images/UDP_Socket.png")

### TCP Socket
![The connect process of TCP Socket]("images/TCP_Socket.png")

### Apa Itu Socket Programming?
Socket programming adalah teknik pemrograman untuk memungkinkan komunikasi antar perangkat di jaringan melalui koneksi soket. Soket bertindak sebagai titik akhir (endpoint) untuk pengiriman atau penerimaan data.

Konsep Utama dalam Socket Programming

1. Socket: Representasi abstrak dari titik koneksi jaringan.
- Server Socket: Mendengarkan koneksi dari klien.
- Client Socket: Membuat koneksi ke server.
2. Protokol Transport:
- TCP (Transmission Control Protocol): Koneksi stabil dan andal.
- UDP (User Datagram Protocol): Koneksi ringan, tanpa jaminan reliabilitas.
3. Alamat dan Port:
- Setiap koneksi ditentukan oleh kombinasi alamat IP dan port.
- Dalam kasus ini, port 5002 adalah port yang digunakan untuk komunikasi.

### Alur Dasar Socket Programming (Server dan Client)
Server:
1. Buat Socket: Gunakan fungsi socket() untuk membuat soket.
2. Bind: Ikat soket ke alamat IP dan port tertentu dengan bind().
3. Listen: Tunggu koneksi klien dengan listen().
4. Accept: Terima koneksi klien dengan accept().
5. Komunikasi: Kirim dan terima data dengan send() dan recv().
6. Tutup Koneksi: Gunakan close() untuk menutup soket.

Client:
1. Buat Socket: Sama seperti server, gunakan socket().
2. Connect: Sambungkan ke server dengan connect().
3. Komunikasi: Kirim dan terima data dengan send() dan recv().
4. Tutup Koneksi: Gunakan close() untuk menutup soket.
    
Poin Penting:
1. Pastikan port 5002 tidak digunakan oleh aplikasi lain.
2. Jika ingin berkomunikasi antar perangkat, pastikan firewall atau izin jaringan tidak memblokir koneksi.
3. Untuk komunikasi lebih kompleks, gunakan multithreading atau asynchronous I/O.
