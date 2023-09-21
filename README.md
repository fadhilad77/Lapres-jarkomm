Lapres Praktikum Modul 1 
Wireshark

1. User melakukan berbagai aktivitas dengan menggunakan protokol FTP.
   nc 10.21.78.111 12345
   Solving :
   Masuk ke dalam netcat dan perhatikan soal yang diinginkan! Berikutnya analisis lewat file packet capture yang diberikan.
![Windows PowerShell 9_21_2023 9_55_19 AM](https://github.com/fadhilad77/Lapres-jarkomm/blob/main/Screen%20Shot%202023-09-21%20at%2013.55.20.png)

Pada wireshark lakukan filter dengan keyword "FTP" karena clue yang diberikan oleh soal adalah aktivitas yang terjadi pada protokol FTP.
Lalu, pusatkan perhatian pada "STOR" yang terdapat pada info paket yang terekam karena diduga kuat itu merupakan aktivitas yang dimaksud.
![soal 1 FTP](https://github.com/fadhilad77/Lapres-jarkomm/blob/main/Screen%20Shot%202023-09-21%20at%2013.55.13.png)
![soal 1 FTP](https://github.com/fadhilad77/Lapres-jarkomm/blob/main/Screen%20Shot%202023-09-21%20at%2013.53.44.png)

2. Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!
   nc 10.21.78.111 13579

   Solving :
   Masuk ke dalam packet capture dan karena soal menginginkan server maka ikuti protokol http dari file pcap tersebut karena server pasti menempel pada protokol http

![Wireshark · Follow HTTP Stream (tcp stream eq 2) · Wi-Fi 9_18_2023 8_02_15 PM](https://github.com/fadhilad77/Lapres-jarkomm/blob/main/Screen%20Shot%202023-09-20%20at%2021.30.30.png)

   sehingga ditemukan jawaban dan flag sebagai berikut
![jawaban soal 2](https://github.com/fadhilad77/Lapres-jarkomm/blob/main/Screen%20Shot%202023-09-20%20at%2021.31.12.png)

3. Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut:
   nc 10.21.78.111 13590

   Solving:
   Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?
   pada wireshark lakukan filter dengan keyword (ip.src == 239.255.255.250 || ip.dst == 239.255.255.250) && (udp.port == 3702 || tcp.port      == 3702) sehingga ditemukan ini

   ![soal 3](https://github.com/fadhilad77/Lapres-jarkomm/blob/main/Screen%20Shot%202023-09-20%20at%2022.03.52.png)

   sehingga dapat ditemukan jawaban dari pertanyaan tersebut dan ditemukan flag nya sebagai berikut

   ![jawaban soal 3](https://github.com/fadhilad77/Lapres-jarkomm/blob/main/Screen%20Shot%202023-09-20%20at%2022.04.06.png)


4. Berapa nilai checksum yang didapat dari header pada paket nomor 130?
   nc 10.21.78.111 13591

   Solving:
   Untuk mendapat nilai checksum dari paket nomor 130 dengan cara mencari paket 130 dan melihat pada bagian checksum seperti paket berikut

   ![soal4](https://github.com/fadhilad77/Lapres-jarkomm/blob/main/Screen%20Shot%202023-09-21%20at%2015.44.43.png)

   sehingga dapat ditemukan jawaban dari pertanyaan tersebut dan ditemukan flag nya sebagai berikut

   ![jawaban soal 4](https://github.com/fadhilad77/Lapres-jarkomm/blob/main/Screen%20Shot%202023-09-21%20at%2015.44.48.png)
