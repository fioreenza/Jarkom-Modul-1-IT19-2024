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
2. Buka nc 10.15.42.60 53000 di terminal dan rahasia.pcap pada wireshark
3. Disini kita menemukan data_pns.csv
   ![image](https://github.com/user-attachments/assets/ff329d26-d2ba-474f-88ad-04afa84a8b7b)
4. Jawab soal sesuai yang ada di data tersebut
   ![image](https://github.com/user-attachments/assets/24bf2c5b-309e-47a9-8331-bd521beae2e3)
5. Flag ditemukan
   ![image](https://github.com/user-attachments/assets/5f1018f6-44e1-4e94-aaa2-6e4b0245dae7)

 ## Write Up Corporate Breach
1. Terdapat breach.pcap dan nc 10.15.42.60 51000 pada soal.
2. Buka nc nc 10.15.42.60 51000 di terminal dan breach.pcap pada wireshark
3. Filter packet yang memiliki protocol http
   ![image](https://github.com/user-attachments/assets/b66b586f-cd98-482b-94e8-7249b4028b1c)
4. Dari situ bisa didapatkan nama attacker yang ditanyakan
   ![image](https://github.com/user-attachments/assets/68327636-6496-4826-ac77-be9f316a1f44)
5. Didapatkan email dan password yang digunakan untuk login
   ![image](https://github.com/user-attachments/assets/53f79d85-aa55-47e0-ab1e-39d985ddc764)
6. Lalu ditemukan flagnya
   ![image](https://github.com/user-attachments/assets/0c78b378-6380-4c88-9ed2-6dbbf711c981)



