# LAB-46-Firewall-Mangle
Kamis 28 Agustus 2025  
  
# Mangle
  FIrewall mangle digunakan untuk menandai sebuah koneksi atau paket dengan tanda khusus untuk pemrosesan selanjutnya, yang mana biasanya mark ini digunakan pada fitur lainnya seperti routing, mark ini hanya bekerja di dalam router untuk di proses dan juga dengan mangle admin dapat mengubah IP header pada paket yang ditentukan.  

# Chain
![](IMAGES/)  
  1. Prerouting, untuk traffic yang masuk dan melewati router, tidak bisa memilih out interface.  
  2. Forward, untuk traffic yang melewati router.  
  3. Postrouting, untuk traffic yang keluar dan melewati router, tidak bisa memilih in interface.  
  4. Input, Untuk traffic yang menuju router, tidak bisa memilih out interface.  
  5. Output, Untuk traffic yang keluar dari router, tidak bisa memilih in interface.  
  
# Action
![](IMAGES/)  
1. accept  
   Menerima paket, tidak akan diproses pada rule berikutnya.  
2. add dst to address list  
   Untuk menambah informasi dst address dari paket ke address list yang ditentukan.  
3. add src to address list  
   Menambahkan informasi src address dari paket ke address list yang ditentukan.  
4. change DSCP (TOS)  
   Mengubah parameter Type of Service of Diffserv (TOS) oada keader sebuah paker.  
5. change MSS  
   Mengubah parameter MSS (Maximum Segmen Size) pada header sebuah paket, biasanya diterapkan pada koneksi VPN.  
6. change TTL  
   mengubah parameter TTL (Time To Live) pada header sebuah paket  
7. Clear DF
   Menghapus flag DF agar paket bisa di fragmentasi.  
9. Fasttrack connection  
   Untuk mempercepat pemrosesan paket, bypass paket di rule selanjutnya.  
10. jump  
   Paket akan dilempat ke chain yang ditentukan  
11. log  
    Menampilkan informasi di log system.  
12. mark connection  
    Membuat mark baru pada sebuah connection traffic.  
13. mark packet  
    Menandai semua paket yang sesuai dengan klasifikasi yang ditentukan.  
14. mark routing  
    Menandai paket untuk digunakan pada policy routing.  
15. passthrought  
    meneruskan ke rule dibawahnya  
16. return  
    Mengembalikam ke chain sebelumnya yang menerapkan jump  
17. route  
    memaksa paket ke IP gateway tertentu, tidak akan di proses pada routing decision, hanya pada chain prerouting.  
18. set priority  
    Untuk mengatur prioritas paket.  
19. sniff PC  
    Untuk mengirim paket ke CALEA server  
20. sniff TZSP  
    Kirim paket ke Wireshark/TZSP server  
21. strip ipv4 options  
    Menghapus opsi IPv4  
