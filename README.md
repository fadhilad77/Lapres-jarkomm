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

2. Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!
   nc 10.21.78.111 13579
   Solving :
   Masuk ke dalam packet capture dan karena soal menginginkan server maka ikuti protokol http dari file pcap tersebut karena server pasti menempel pada protokol http
   ![Wireshark · Follow HTTP Stream (tcp stream eq 2) · Wi-Fi 9_18_2023 8_02_15 PM](https://github.com/yogs14/Jarkom-jarkoman/assets/121499055/371d18eb-049c-4d0d-9f79-bdcb26c31a95)
