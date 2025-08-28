# LAB-46-Firewall-Mangle
Kamis 28 Agustus 2025  
  
# Mangle
  Mangle adalah salah satu firewall di MikroTik untuk menandai (marking) paket atau koneksi. Tanda ini hanya ada di dalam router, tidak ikut terbawa ke jaringan luar.  

# Chain
![](IMAGES/)  
  1. Prerouting, sebelum paket routing. COcok untuk mark routing.  
  2. Forward, Paket yang lewat router (bukan tujuan router.  
  3. Postrouting, Setelah routing, sebelym keluar interface.  
  4. Input, Paket menuju router.  
  5. Output, Paket yang keluar dari router.  
  
# Action
![](IMAGES/)  
1. accept  
   Menghentikan pemeriksaan rule selanjutnya dalam chain. 
