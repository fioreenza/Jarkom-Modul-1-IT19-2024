# Jarkom-Modul-1-IT19-2024

| Nama | NRP | 
|----------|----------|
| Fiorenza A.N. | 5027231053 |
| Nicholas E.F. | 5027231070 |


## Write Up Advance Sanity Check
1. Terdapat sanity.pcapng dan nc 10.15.42.60 44000 pada soal.
2. Buka ncat 10.15.42.60 44000 di terminal dan sanity.pcapng pada wireshark
3. Filter packet yang memiliki protocol http
   ![image](https://github.com/user-attachments/assets/f78eac1f-be31-44fd-b373-4d561ce73c59)
4. Dari situ bisa ditemukan jawaban yang ditanyakan seperti username, nama file, dan petunjuk yang berada di rules soal shift
   ![image](https://github.com/user-attachments/assets/b34ba632-3fda-41ff-800e-996b30dae228)
   ![image](https://github.com/user-attachments/assets/1a088fe9-48df-4cfa-83d4-afeb8efa99f1)
5. Di rules soal shift terdapat clue yang harus di decrypt menggunakan base64 terlebih dahulu
6. Lalu dapat ditemukan flagnya
   ![image](https://github.com/user-attachments/assets/1356d299-9483-4ff5-a2a5-0f1fe5268657)


## Write Up Pegawai Negeri Sebelah
1. Terdapat rahasia.pcap dan nc 10.15.42.60 53000 pada soal.
2. Buka ncat 10.15.42.60 53000 di terminal dan rahasia.pcap pada wireshark
3. Disini kita menemukan data_pns.csv
   ![image](https://github.com/user-attachments/assets/ff329d26-d2ba-474f-88ad-04afa84a8b7b)
4. Jawab soal sesuai yang ada di data tersebut
   ![image](https://github.com/user-attachments/assets/24bf2c5b-309e-47a9-8331-bd521beae2e3)
5. Flag ditemukan
   ![image](https://github.com/user-attachments/assets/5f1018f6-44e1-4e94-aaa2-6e4b0245dae7)


 ## Write Up Corporate Breach
1. Terdapat breach.pcap dan nc 10.15.42.60 51000 pada soal.
2. Buka ncat 10.15.42.60 51000 di terminal dan breach.pcap pada wireshark
3. Filter packet yang memiliki protocol http
   ![image](https://github.com/user-attachments/assets/b66b586f-cd98-482b-94e8-7249b4028b1c)
4. Dari situ bisa didapatkan nama attacker yang ditanyakan
   ![image](https://github.com/user-attachments/assets/68327636-6496-4826-ac77-be9f316a1f44)
5. Didapatkan email dan password yang digunakan untuk login
   ![image](https://github.com/user-attachments/assets/53f79d85-aa55-47e0-ab1e-39d985ddc764)
6. Lalu ditemukan flagnya
   ![image](https://github.com/user-attachments/assets/0c78b378-6380-4c88-9ed2-6dbbf711c981)


## Write Up Malicious Code
1. Terdapat breach.pcap dan nc 10.15.42.60 52000 pada soal.
2. Buka ncat 10.15.42.60 52000 di terminal dan breach.pcap pada wireshark
3. Disini kita filter http yang method nya get untuk mendapatkan jumlah attacker melakukan dir listing
   ![image](https://github.com/user-attachments/assets/7bd6ed0b-9f2d-4fce-9ab6-93c518f14b95)
4. Disini bisa diketahui attacker menemukan endpoint login berupa index.php
   ![image](https://github.com/user-attachments/assets/dddb3a44-2e98-4adb-89a2-8a2775511674)
5. Lalu filter http.request.method == "POST" untuk mengetahui attempt ke berapa (169 dari display dikurangi 16)
   ![image](https://github.com/user-attachments/assets/81b3e09b-2c74-42be-9559-b8f731130f0b)
6. Disini hacker menjawab pertanyaan yang merupakan decimal, kita ubah dari decimal to text
   ![image](https://github.com/user-attachments/assets/f95a3a12-2003-451e-98f3-861fc8135b72)
   ![image](https://github.com/user-attachments/assets/7138a622-1e5d-4039-9fd8-627266fd73b9)
7. Disini saya mencoba coba warna untuk mendapatkan flag dan jawabannya adalah merah
   ![image](https://github.com/user-attachments/assets/59a2085f-d716-4320-9d13-b4e98a7be4c0)


## Write Up FTP Login
1. Terdapat ftplogin.pcapng dan nc 10.15.42.60 49000 pada soal.
2. Buka ncat 10.15.42.60 49000 di terminal dan ftplogin.pcapng pada wireshark
3. Disini kita filter ftp lalu sebelum login sucessfull terdapat user dan password yang berhasil digunakan untuk login
   ![image](https://github.com/user-attachments/assets/8f4ada23-4e1f-4d2d-945a-a208c4b1e996)
4. Follow TCP Stream untuk melihat lebih jelas
   ![image](https://github.com/user-attachments/assets/66ca4877-5908-456e-b994-04382e3d7405)
6. Lalu dapat ditemukan flagnya
   ![image](https://github.com/user-attachments/assets/d64d1c0f-7c14-47a3-96c8-0c3927d6adae)


## Write Up Surprise
1. Terdapat ftplogin.pcapng dan nc 10.15.42.60 48500 pada soal.
2. Buka ncat 10.15.42.60 48500 di terminal dan ftplogin.pcapng pada wireshark
3. Ditemukan service yang digunakan
   ![image](https://github.com/user-attachments/assets/df45d86f-91ab-49c7-a2bf-2790511b73a2)
4. File yang dikirim adalah g0tcha.cpp
   ![image](https://github.com/user-attachments/assets/0945a126-e4d3-4715-8869-25835a036246)
5. String yang ditinggalkan dapat dilihat dari follow TCP Stream dari FTP Data
   ![image](https://github.com/user-attachments/assets/ebe9b920-6644-4432-bdb8-f799e64cbedd)
6. Didapatkan code ini lalu run
   ![image](https://github.com/user-attachments/assets/91f92b73-3452-48d1-ae69-f84d86e6e3a4)
   ![image](https://github.com/user-attachments/assets/1b1238a9-fc60-47c1-8ee0-bd731a224cdf)
7. Flagnya bisa didapatkan
   ![image](https://github.com/user-attachments/assets/62674f02-9c93-4313-adf3-2ac7e4d8428c)


## Write Up Gajah Terbang (Server Recon)
1. Terdapat gajahterbang.pcapng dan nc 10.15.42.60 61000 pada soal.
2. Buka ncat 10.15.42.60 61000 di terminal dan gajahterbang.pcapng pada wireshark
3. Dari sini bisa dilihat DBMS nya menggunakan PostgreSQL
   ![image](https://github.com/user-attachments/assets/7049c772-e0ee-408d-98af-fd6e640dfe57)
4. DBMS berjalan di port 6969
   ![image](https://github.com/user-attachments/assets/5571de82-9df9-4173-8e00-830a0031e399)
5. Follow TCP Stream
   ![image](https://github.com/user-attachments/assets/e2779acd-b89e-4a55-b4f6-d434851ac3f1)
6. Dari sini didapatkan server dijalankan di OS Debian, username s1gm4, dan databasenya sigmaskibidigyatrizzzz
   ![image](https://github.com/user-attachments/assets/8d9bc6eb-3c6e-434d-be2b-bbd87991a58a)
7. Disini juga terlihat terdapat 4 user di database
   ![image](https://github.com/user-attachments/assets/1b9860b7-a00d-44bf-98ed-fdbfe451c609)
8. Email yang digunakan admin adalah jojohermawan@gmail.com dan passwordnya c93ccd78b2076528346216b3b2f701e6 yang akan di decrypt menggunakan md5 
   ![image](https://github.com/user-attachments/assets/24c148ee-2948-4c66-b2c4-80ef0206b0af)
   ![image](https://github.com/user-attachments/assets/7859cad7-3b92-47cb-9fa2-18b1c482c0a6)
9. Flag bisa didapatkan
   ![image](https://github.com/user-attachments/assets/e1522f8e-a80e-47e6-a1d8-131c2d7db65a)


## Write Up Gajah Terbang (Server Recon)
1. Terdapat gajahterbang.pcapng dan nc 10.15.42.60 62000 pada soal.
2. Buka ncat 10.15.42.60 62000 di terminal dan gajahterbang.pcapng pada wireshark
3. Follow TCP Stream
   ![image](https://github.com/user-attachments/assets/e2779acd-b89e-4a55-b4f6-d434851ac3f1)
4. Disini kita bisa mengetahui attackernya dengan cara mencoba coba data user email dari database ini, dan yang benar adalah kuntoajiisrillll@gmail.com serta dengan password aa1cbddbb1667f7227bcfdb25772 yang akan di decrypt menggunakan md5
   ![image](https://github.com/user-attachments/assets/55c43a03-5718-4e3a-894e-d5464d6acb82)
   ![image](https://github.com/user-attachments/assets/6368be31-11f8-40c9-a11b-507437f1010c)
5. Penyerang di ban tanggal 2024-06-09
   ![image](https://github.com/user-attachments/assets/0e8b7d80-12b1-4a6a-a7c9-1bedde391837)
6. Tabel yang diserang adalah users dan banned users
   ![image](https://github.com/user-attachments/assets/9e280c09-0406-46ba-99d7-1f6e60ef5cc0)
7. Barang yang dibeli adalah rokok dan es krim, serta total transaksi yaitu dengan menjumlahkan harga dari rokok dan eskrim yang jumlahnya 24500
   ![image](https://github.com/user-attachments/assets/855384f7-566e-4a34-abd5-4d303c079fb8)
8. Lalu flag ditemukan
   ![image](https://github.com/user-attachments/assets/a2dd76dd-9efd-4e6c-b752-26f08d39598e)


## Write Up EZ
1. Terdapat nc.pcapng dan nc 10.15.42.60 54000 pada soal.
2. Buka ncat 10.15.42.60 54000 di terminal dan gajahterbang.pcapng pada wireshark
3. Follow TCP Stream ke salah satu packet
   ![image](https://github.com/user-attachments/assets/deca2e51-5e3c-4169-bf33-d558079b2d69)
4. Hasilnya ditemukan string ini yang berisi jawaban
   ![image](https://github.com/user-attachments/assets/73a88a83-6a68-47e5-881b-ff642865b92c)
5. Temukan portnya di dst port yaitu 1234
   ![image](https://github.com/user-attachments/assets/11aa7d0f-d6c0-4841-a131-e35f0de8d113)
6. Flag dapat ditemukan
   ![image](https://github.com/user-attachments/assets/81b987ab-aa2b-40c9-b5b0-e673bd176917)


## Write Up Rizzset
1. Terdapat riset.pcapng dan nc 10.15.42.60 59500 pada soal.
2. Buka ncat 10.15.42.60 59500 di terminal dan gajahterbang.pcapng pada wireshark
3. Disini dapat dilihat domain dari dns query adalah www.its.ac.id
   ![image](https://github.com/user-attachments/assets/13568186-9daa-4e2b-9594-e5b8ca6cc9d9)
4. IP dari domain saya coba coba dan yang benar adalah 103.94.189.5
   ![image](https://github.com/user-attachments/assets/ecdb768f-1ed8-467c-8185-8ac611bc06d5)
5. JARM fingerprint yang dihasilkan bisa dilihat di jarm online atau menggunakan script py
   ![image](https://github.com/user-attachments/assets/9373a534-a442-4459-b7ff-527722fbd9a2)
6. Dapat ditemukan flagnya
   ![image](https://github.com/user-attachments/assets/87843df9-23d2-4084-b126-cc56edc9e8e3)


## Write Up Illegal Breakthrough
1. Terdapat break.pcapng dan nc 10.15.42.60 46000 pada soal.
2. Buka ncat 10.15.42.60 46000 di terminal dan break.pcapng pada wireshark
3. Filter packet yang memiliki protocol http
   ![image](https://github.com/user-attachments/assets/bb13594c-19f6-4702-86f3-3bba962f398a)
4. Disini terdapat IP Address dari korban yaitu 172.21.88.207 dan port yang digunakan webserver yaitu 1917
   ![image](https://github.com/user-attachments/assets/e2cb4238-963e-4a44-b8e6-0a8f346d89ed)
5. Disini dapat dilihat bahwa endpoint untuk login yaitu /ww1.php
   ![image](https://github.com/user-attachments/assets/022fe3fc-00a4-43c3-909e-f441d3cdd9e7)
6. Follow TCP HTTP pada web yang found
   ![image](https://github.com/user-attachments/assets/94c2027c-dd66-4cd6-a98f-edabeb7e0255)
7. Disini dapat dilihat tools yang digunakan ffuf-v2.1.0-dev
   ![image](https://github.com/user-attachments/assets/a92cf25a-52fd-4ffb-a48c-155ace6dda60)
8. Kredensial untuk login yaitu Redbaron:fly1ng4c3
   ![image](https://github.com/user-attachments/assets/0194e046-9524-4775-bcbf-6220fb640e6c)
9. Lalu dapat ditemukan flagnya
   ![image](https://github.com/user-attachments/assets/15987c88-141e-4ee2-8e70-ccda947b94b4)

   

## Write Up Packets Barrage
1. Terdapat break.pcapng dan nc 10.15.42.60 47000 pada soal.
2. Buka ncat 10.15.42.60 47000 di terminal dan break.pcapng pada wireshark
3. Disini kita bisa menemukan IP Address attackernya yaitu 172.21.80.1
   ![image](https://github.com/user-attachments/assets/7f564234-436e-48ca-97f8-2580078b1b9b)
4. Lalu filter menggunakan http.request.method == "POST" untuk total attempt dari bruteforce attacker
   ![image](https://github.com/user-attachments/assets/2370971e-b662-44cf-94ce-e9bf8b2997f9)
5. Disini terlihat displayed packet dengan method post adalah 1918, namun ketika diinput ternyata salah. Jadi saya mencoba input 1917 atau menguranginya dengan 1 dan hasilnya benar
   ![image](https://github.com/user-attachments/assets/acf5fb09-5e24-4b69-ae25-c9b4c975edfa)
6. Untuk melihat file yang didownload yaitu dengan melakukan follow packet dibawah ini
   ![image](https://github.com/user-attachments/assets/f1a9291e-bd33-42f4-b301-5ea7211fde50)
7. Disini terdapat dua file, ketika dicoba Regev.zip salah, maka saya input lagi yaitu Albatros.txt
   ![image](https://github.com/user-attachments/assets/03db6ef1-54c3-4397-b53a-0728995edcbb)
8. Terdapat string berupa Der Rote Kampfflieger
   ![image](https://github.com/user-attachments/assets/f157b89f-8a95-40aa-aa6e-6158afbcf978)
9. Dapat ditemukan flagnya
    ![image](https://github.com/user-attachments/assets/a6ebf65e-67e3-49bf-b293-8ef9029715c2)



## Write Up 22 Nightmare
1. Terdapat oimazrim.pcap dan nc 10.15.42.60 45000 pada soal.
2. Buka ncat 10.15.42.60 45000 di terminal dan break.pcapng pada wireshark
3. Filter ftp, disini bisa kita lihat file yang dikirim penyerang adalah Sh1k4.jpg
   ![image](https://github.com/user-attachments/assets/a1b73b78-31d0-4095-8c79-718001531601)
4. Export file yang dikirim, dan setelah diexport bisa kita lihat ada tulisan NUN
   ![image](https://github.com/user-attachments/assets/4b87e4a5-0ca8-47fe-b260-f0fa3597d9e4)
5. Follow TCP stream file kedua, lalu didapatkam bahwa file kedua dikirim di stream ke 141
   ![image](https://github.com/user-attachments/assets/766e1eb7-a5a8-40af-b6ff-bfd8c4c47a3a)
6. Nama pengirim terdapat pada petunjuk yang ada di file kedua, noko.py
   ![image](https://github.com/user-attachments/assets/0181149b-5f46-449a-826a-bd836fd669af)
7. Kita perlu decrypt xor binary dengan key jpg (atau tulisan yang ada di Sh1k4.jpg = nun), hasilnya adalah Torako Koshi
   ![image](https://github.com/user-attachments/assets/1959b414-b8ad-4ce6-81d0-ab6122974a8f)
8. Sehingga bisa didapatkan flagnya
   ![image](https://github.com/user-attachments/assets/33a7c735-6174-48c7-a619-baf226c7e0dd)
   ![image](https://github.com/user-attachments/assets/0c8a2fa6-5924-435f-8078-09a9d22b85f4)
   ![image](https://github.com/user-attachments/assets/f4258aa0-8bac-4983-8cea-0b0da07dc79a)









