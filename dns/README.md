# DNS

### Pengertian DNS
DNS (Domain Name System) adalah sistem yang menerjemahkan nama domain (seperti www.google.com) menjadi alamat IP (seperti 142.250.190.78) yang dapat digunakan oleh komputer untuk saling berkomunikasi. DNS bertindak seperti buku telepon internet, memudahkan pengguna untuk mengakses layanan tanpa harus mengingat alamat IP.

### Jenis Query
- Recursive Query
Dalam recursive query, sebuah DNS resolver meminta informasi kepada server DNS dengan tanggung jawab penuh untuk menemukan jawaban yang diminta. Jika server DNS yang pertama kali diminta tidak memiliki jawaban, ia akan mengirimkan permintaan ke server DNS lain atas nama resolver hingga jawaban ditemukan atau kesalahan dikembalikan.
- Iterative Query
Dalam iterative query, resolver meminta informasi ke server DNS, tetapi server DNS hanya memberikan informasi terbaik yang dimilikinya, seperti alamat server DNS berikutnya yang lebih relevan. Resolver kemudian mengulangi permintaan ini ke server DNS lain hingga menemukan jawaban akhir.

### Alur Kerja DNS 
Proses DNS:
1. Pengiriman DNS Query: Host cse.nyu.edu mengirimkan pesan query DNS ke server DNS lokal dns.nyu.edu untuk mencari alamat IP dari hostname gaia.cs.umass.edu.
2. Pengiriman ke Root DNS Server: Server DNS lokal meneruskan query tersebut ke root DNS server.
3. Pencatatan Suffix "edu": Root DNS server memeriksa sufiks "edu" pada hostname dan mengirimkan daftar alamat IP untuk TLD server yang bertanggung jawab atas domain "edu".
4. Pengiriman ke TLD DNS Server: Server DNS lokal kemudian mengirimkan query ke salah satu TLD server yang bertanggung jawab atas domain "edu".
5. Pencatatan Suffix "umass.edu": TLD server memeriksa sufiks "umass.edu" dan merespons dengan alamat IP dari authoritative DNS server untuk University of Massachusetts, yaitu dns.umass.edu.
6. Pengiriman ke Authority DNS Server: Server DNS lokal mengirimkan query ke dns.umass.edu untuk mencari alamat IP dari gaia.cs.umass.edu.
7. Respon dari Authority DNS Server: dns.umass.edu merespons dengan alamat IP dari gaia.cs.umass.edu.
8. Proses Query Lengkap: Dalam proses ini, ada 8 pesan DNS yang dikirim, yaitu 4 pesan query dan 4 pesan reply.



