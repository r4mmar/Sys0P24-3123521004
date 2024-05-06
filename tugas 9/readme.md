# Forking, Orphan & Zombie
Akses dan clonning repo : https://github.com/ferryastika/operatingsystem.git
Deskripsikan dan visualisasikan pohon proses hasil eksekusi dari kode program fork01.c, fork02.c, fork03.c,
![image](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/20d5b212-f8ae-444b-90f7-8777e6ab5118)
![image](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/0919e931-3398-43df-9799-1b7bb37fe2e7)
 
Sebelum menjalankan fork , lakukan instalasi compiler dengan menggunakan program apt install gcc g++. perintah tersebut digunakan untuk menginstall compiler bahasa C dan bahasa C++

gcc adalah compiler untuk bahasa C
g++ adalah compiler untuk bahasa C++
![image](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/b6b36396-0258-4740-993f-e1d72b53b25d)

Untuk menjalankan fork01.cpp , menggunakan perintah g++ fork01.cpp -o fork01.exe
![image](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/5a5f38e9-551e-455e-b49e-8580ac7578a4)
![image](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/9198a818-b196-4833-a173-3c88e851e4f5)
 
Perintah di atas digunakan untuk mengkompilasi program C++ yang disebut dengan fork01.cpp menggunakan compiler g++ kemudian akan menghasilkan output berupa fork01.exe
Untuk menampilkan program menggunakan perintah nano fork01.cpp
![image](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/7c897226-a928-478c-a59f-35d66bb91c40)

Untuk menjalankan program menggunakan perintah ./fork01.exe
![image](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/94f80e00-5d6f-4fc9-acad-d5d373a1b5a4)

Output program ini menampilkan ID proses (PID), ID proses parent (PPID), dan ID pengguna (UID). Setiap kali program mencetak informasi tersebut, program akan berhenti selama tiga detik sebelum mencetak informasi lagi. Program ini akan diulang sebanyak tiga kali.
Kemudian untuk menjalankan fork02.cpp dan juga fork03.cpp caranya sama seperti menjalankan fork01.cpp
fork02.cpp
![image](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/18996ac7-f0b8-454c-b089-a8810820d9d0)
 
Output dari program tersebut adalah melakukan proses forking secara berulang sebanyak 5 kali, yang menghasilakn proses baru dengan pesan yang mencatat PID masing-masing.
fork03.cpp
![image](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/bf13da28-c4d5-493e-8076-834f85eb252a)
![image](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/1545477e-f53e-4559-a60b-c4a5c8735041)

Output dari program tersebut adalah menampilkan PID mereka sendiri dan nilai variabel x dalam loop tak terbatas. Program menggunakan system call fork() untuk membuat proses saat ini, dan menciptakan child process.
Cara penginstalan orphan sama seperti menginstall fork
Sebelum menjalankan orphan , lakukan instalasi compiler dengan cara mengetikkan apt install gcc g++.
perintah tersebut untuk menginstall compiler bahasa C dan bahasa C++
![image](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/cc5c8feb-0f03-49e4-bf0e-45c83866006a)
![image](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/e08ca045-2ccd-49bf-ab1d-344d1712c76f)
![image](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/6fb245e5-53c8-4592-86a3-fd776fbf1e9c)

Output dari program tersebut adalah menampilkan PID mereka sendiri
Sebelum menjalankan zombie , lakukan instalasi compiler dengan cara mengetikkan apt install gcc g++.
perintah tersebut untuk menginstall compiler bahasa C dan bahasa C++
![image](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/1ded9a21-c290-4605-b137-712fb1e1351b)
![image](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/a1d0e52e-7c49-44c8-9d41-1df236ab5dc5)
![image](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/bb4b1821-f3f1-4c2f-bd71-9d859b361714)

Output dari program tersebut adalah tidak menampilkan PID.
