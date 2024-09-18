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
 

