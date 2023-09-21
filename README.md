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

5. Elshe menemukan suatu file packet capture yang menarik. Bantulah elshe untuk menganalisis file packet capture tersebut.

   Solving:
   pada soal ini diberikan sebuah zipfile yang terkunci cara membukanya adalah temukan password pada wireshark kemudia didecode menggunakan base 64 seperti berikut

   ![soal5](https://github.com/fadhilad77/Lapres-jarkomm/blob/main/Screen%20Shot%202023-09-20%20at%2022.16.42.png)
   ![soal5](https://github.com/fadhilad77/Lapres-jarkomm/blob/main/Screen%20Shot%202023-09-20%20at%2022.17.25.png)
   ![soal5](https://github.com/fadhilad77/Lapres-jarkomm/blob/main/Screen%20Shot%202023-09-20%20at%2022.17.09.png)

   setelah itu didapatkan nc 10.21.78.111 11111 kemudian didapatkan pertanyaan yang akan dijawab menggunakan wireshark yaitu berapa banyak port, port smtp, dan alamat ip nya dapat dilihat berikut

   ![jawaban soal 5](https://github.com/fadhilad77/Lapres-jarkomm/blob/main/Screen%20Shot%202023-09-20%20at%2022.18.06.png)
   ![jawaban soal 5](https://github.com/fadhilad77/Lapres-jarkomm/blob/main/Screen%20Shot%202023-09-20%20at%2022.18.25.png)

   sehingga didapatkan flag sebagai berikut
   
   ![jawaban soal 5](https://github.com/fadhilad77/Lapres-jarkomm/blob/main/Screen%20Shot%202023-09-20%20at%2022.18.54.png)

6. Seorang anak bernama Udin Berteman dengan SlameT yang merupakan seorang penggemar film detektif. sebagai teman yang baik, Ia selalu mengajak slamet untuk bermain valoranT bersama. suatu malam, terjadi sebuah hal yang tak terdUga. ketika udin mereka membuka game tersebut, laptop udin menunjukkan sebuah field text dan Sebuah kode Invalid bertuliskan "server SOURCE ADDRESS 7812 is invalid". ketika ditelusuri di google, hasil pencarian hanya menampilkan a1 e5 u21. jiwa detektif slamet pun bergejolak. bantulah udin dan slamet untuk menemukan solusi kode error tersebut.

   Solving:  Seorang anak bernama Udin Berteman dengan Slamet yang merupakan seorang penggemar
   film detektif. sebagai Teman yang baik, Ia selalu mengajak slamet untuk bermain valorant
   bersama. suatu malam, Terjadi sebuah hal yang tak terduga. ketika Udin mereka membuka
   game tersebut, laptop udin menunjukkan sebuah field text dan aSebuah kode Invalid
   bertuliskan "server SOURCE ADDRESS 7812 is invalid".
   ketika ditelusuri di google, hasil pencarian hanya menampilkan a1 e5 u21. jiwa detektif
   slamet pun bergejolak.
   bantulah udin dan slamet untuk menemukan solusi kode error tersebut.
   ➔ 104.18.14.101 → 0-18 → 10 4 18 14 10 1 → J D R N J A

    seperti pada gambar berikut:

   ![soal6](https://github.com/fadhilad77/Lapres-jarkomm/blob/main/Screen%20Shot%202023-09-21%20at%2014.01.59.png)

   sehingga dapat menjawab pertanyaan dan mendapat flag sebagai berikut

   ![jawaban soal 6](https://github.com/fadhilad77/Lapres-jarkomm/blob/main/Screen%20Shot%202023-09-21%20at%2014.02.05.png)

   
