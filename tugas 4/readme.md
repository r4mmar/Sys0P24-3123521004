1. Buatlah presentasi langkah demi langkah tentang siklus CPU (fetch,decode,execute) utk mengeksekusi sebuah program. Jelaskan juga peran dari Bahasa pemrograman dan compiler, begitu juga dengan peran dari Sistem Operaso. Gunakan referensi : [Video referensi 1](https://www.youtube.com/watch?v=Z5JC9Ve1sfI) dan [Video referensi 2](https://www.youtube.com/watch?v=jFDMZpkUWCw)

 Siklus CPU adalah serangkaian langkah yang dilakukan oleh unit pemrosesan pusat (CPU) saat mengeksekusi instruksi dalam sebuah program. Langkah-langkah utamanya adalah fetch (pengambilan), decode (penyandi), dan execute (eksekusi). Berikut adalah penjelasan langkah demi langkah:

Fetch (Pengambilan):
   - CPU mengambil instruksi berikutnya dari memori utama (RAM) berdasarkan alamat program counter (PC).
   - Alamat program counter kemudian diperbarui untuk menunjuk ke instruksi berikutnya dalam program.

Decode (Penyandi):
   - Instruksi yang diambil dari memori diuraikan atau didekripsi untuk memahami operasi yang perlu dilakukan.
   - Decoder CPU memecah instruksi menjadi bagian-bagian yang dapat dipahami, seperti opcode (kode operasi) dan operand (data yang diperlukan untuk operasi).

Execute (Eksekusi):
   - CPU menjalankan instruksi yang telah dipecah dan diinterpretasikan.
   - Instruksi dieksekusi dengan melakukan operasi yang diperlukan, seperti operasi aritmatika, logika, memindahkan data, atau melompat ke bagian tertentu dari program.

Eksekusi dalam sebuah program

![0](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/dbc142b6-70ba-477d-9443-e43730f938be)

**Siklus Fetch Pertama:**
![1](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/a23d38d3-9cad-4c4b-9232-bed8c1507b2b)
- CPU menunjukkan 29.
- Saat klik pertama, CPU mengambil instruksi (nilai) dari RAM, yaitu LOAD 6, dan memasukkannya ke dalam Instruction Register (IR).

**Siklus Decode Kedua:**
![2](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/8912a6ed-d4a1-4f9c-9233-8361e74686a7)
- CPU menunjukkan 30.
- Pada klik kedua, CPU menerjemahkan instruksi dalam gambar, yaitu LOAD alamat 6, sehingga memuat nilai di alamat 6 ke dalam Akumulator (ACC).

**Siklus Execute Ketiga:**
![3](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/947e0f9b-3156-477f-80cf-9f970d8000f7)
- CPU menunjukkan 4.
- Saat klik ketiga, CPU mengeksekusi instruksi, membutuhkan nilai di alamat 6 (nilai 1) dan memuatnya ke dalam ACC.

**Siklus Fetch Keempat:**
![4](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/3c4bb057-327c-4f16-a743-0b4405ecfe4d)
- CPU menunjukkan 31.
- Pada klik keempat, program counter bertambah, CPU mengambil instruksi berikutnya dari memori, yaitu ADD 7.

**Siklus Decode Kelima:**
![5](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/3da03f6d-3bd1-4c27-b121-2c00dd411670)
- CPU menunjukkan 32.
- Pada klik kelima, CPU menerjemahkan instruksi ADD alamat 7, sehingga menambahkan nilai yang ada di alamat 7 ke nilai yang sudah ada di ACC.

**Siklus Execute Keenam:**
![6](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/78d46c99-93ff-4d53-a3f7-149c449af6cc)
- CPU menunjukkan 7.
- Saat klik keenam, CPU mengeksekusi instruksi dengan alamat 7 (nilai 1). Nilai sebelumnya di ACC adalah 1, sehingga hasilnya adalah 1 + 1 = 2, yang kemudian disimpan kembali di ACC.

**Siklus Fetch Ketujuh:**
![7](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/026fb6f6-b91b-4e72-9d4e-3ae326cd1907)
- CPU menunjukkan 8.
- Pada klik ketujuh, CPU mengambil instruksi berikutnya dari memori, yaitu STORE 6.

**Siklus Decode Kedelapan:**
![8](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/e70769cc-12d7-49ea-bf80-88e39edee90a)
- CPU menunjukkan 9.
- Saat klik kedelapan, CPU menerjemahkan instruksi STORE alamat 6.

**Siklus Execute Kesembilan:**
![9](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/2f259af7-a1d5-4d71-98c3-12a5b189840d)
- CPU menunjukkan 11.
- Pada klik kesembilan, CPU mengeksekusi instruksi dengan menimpa nilai yang ada di alamat 6, yaitu nilai sebelumnya, dengan nilai ACC saat ini, yaitu 2.

**Siklus Fetch Kesepuluh:**
![10](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/081d0049-b9d3-4d40-9d25-e4bc8fb0efff)
- CPU menunjukkan 12.
- Pada klik kesepuluh, CPU mengambil instruksi JUMP 1 dari memori.

**Siklus Decode Kesebelas:**
![11](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/5f11a2b7-7def-4a7d-baee-7984e530f4b0)
- CPU menunjukkan 13.
- Pada klik kesebelas, CPU menerjemahkan instruksi JUMP ke alamat 1, sehingga program melompat ke alamat 1.

**Siklus Execute Keduabelas:**
![12](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/ccc3ffaa-ec4f-4f06-8e47-f6354741ba46)
- CPU menunjukkan 14.
- Saat klik keduabelas, CPU mengeksekusi instruksi, dan program counter kembali ke 1.

**Siklus Fetch Kedua Belas:**
![13](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/816606bf-d29f-4073-820c-adce67ee81f7)
- CPU menunjukkan 15.
- Pada klik keduabelas, CPU mengambil instruksi berikutnya dari memori, yaitu ADD 7.

**Siklus Decode Ketiga Belas:**
![14](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/2f18dfb9-56e6-42a5-b1a5-a09fafd0f954)
- CPU menunjukkan 16.
- Saat klik ketiga belas, CPU menerjemahkan instruksi ADD alamat 7.

**Siklus Execute Keempat Belas:**
![15](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/6eb41ab2-429b-41d9-9d3c-703f80551cfc)
- CPU menunjukkan 17.
- Pada klik keempat belas, CPU menjalankan instruksi dengan menambahkan nilai ACC sebelumnya (3) dengan nilai yang ada di alamat 7 (1), sehingga ACC sekarang bernilai 4.

**Siklus Fetch Kelima Belas:**
![16](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/01fc0c61-309d-40ee-b004-b4a5525fa275)
- CPU menunjukkan 33.
- Saat klik kelima belas, CPU mengambil instruksi berikutnya dari memori, yaitu STORE 6.

**Siklus Decode Enam Belas:**
![17](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/c331a0e9-b364-47ad-b440-ac178e43bb12)
- CPU menunjukkan 19.
- Pada klik enam belas, CPU menerjemahkan instruksi STORE ke alamat 6.

**Siklus Execute Tujuh Belas:**
![18](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/a8282a6a-75c5-45ca-bea9-0048219f2bcf)
- CPU menunjukkan 24.
- Pada klik tujuh belas, CPU mengeksekusi instruksi untuk menyimpan nilai ACC (4) ke lokasi alamat 6, sehingga nilai di alamat 6 sekarang adalah 4.

**Siklus Fetch Delapan Belas:**
![19](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/011d91ac-3d15-4e42-a90c-91076d1f0057)
- CPU menunjukkan 21.
- Saat klik delapan belas, CPU mengambil instruksi berikutnya dari memori, yaitu JUMP 1.

**Siklus Decode Sembilan Belas:**
![20](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/de746482-b3bb-464f-87fb-0e373f626871)
- CPU menunjukkan 22.
- Pada klik sembilan belas, CPU menerjemahkan instruksi JUMP ke alamat 1, sehingga program melompat kembali ke alamat 1.

**Siklus Execute Dua Puluh:**
![21](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/23692bb7-f9e6-4aad-9011-40bdfc0a466b)
- CPU menunjukkan 23.
- Pada klik dua puluh, CPU mengeksekusi instruksi, dan perhitungan program kembali ke langkah 1.


Peran dari bahasa pemrograman dan kompiler:
- Bahasa pemrograman**: Bahasa pemrograman adalah aturan dan sintaks yang digunakan untuk menulis program. Bahasa pemrograman membantu manusia untuk menyusun algoritma dan logika program dengan cara yang mudah dipahami. Contoh bahasa pemrograman termasuk Python, Java, C++, dan lain-lain.
- Compiler: Compiler adalah program yang menerjemahkan kode sumber yang ditulis dalam bahasa pemrograman ke dalam bahasa mesin atau kode objek yang dapat dimengerti oleh CPU. Compiler melakukan proses kompilasi yang mencakup analisis sintaksis, optimasi kode, dan pembuatan kode objek. Setelah kompilasi, program yang dihasilkan dapat dieksekusi oleh CPU.

Peran dari sistem operasi:
- Sistem Operasi (OS): Sistem Operasi adalah perangkat lunak yang mengelola sumber daya perangkat keras komputer dan menyediakan layanan kepada program aplikasi. Peran utama sistem operasi dalam konteks eksekusi program adalah:
  - Mengatur dan mengawasi alokasi sumber daya komputer seperti CPU, memori, dan perangkat input/output.
  - Menyediakan antarmuka bagi program aplikasi untuk berinteraksi dengan perangkat keras.
  - Menyediakan layanan abstraksi yang membantu program-program berjalan dengan lancar dan aman di atas perangkat keras yang mungkin berbeda-beda.
  - 
2. Baca dan pahami rangkuman materi OS: [Materi Intro to OS-01](https://github.com/ferryastika/OS-01)

3. Jalankan VM Debian anda, lalu lakukan clone https://github.com/ferryastika/flops-iops. Compile dan eksekusi sesuai petunjuk. Sesuiakan jumlah thread dengan jumlah CPU yang ada di VM Debianmu. Catat hasilnya dan jelaskan arti dari hasil ekskusi. Lakukan sebanyak 5 kali. Bandingkan hasilnya anatar temanmu. Buat Plot perbandinnga hasil untuk masing-masing PC di tiap kelompokmu. Analisa hasil percobaan tadi dan beri kesimpulan tentang IOPS dan FLOPS.
![make](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/a2b2d03d-6ba9-48fb-b684-9a4987c79550)
$ make
perintah yang digunakan dalam lingkungan pengembangan perangkat lunak untuk mengotomatiskan proses kompilasi dan pembangunan proyek perangkat lunak.
![make clean](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/12f0a79c-2832-49e1-9ef4-d8e6d7077954)
$ make clean
dapat dengan cepat membersihkan proyek mereka dari file-file sementara dan file-file yang dihasilkan selama proses pembangunan
![make install](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/b064b156-dcc6-41e1-98fb-fc2a3739f8a1)
$ sudo make install
perintah yang digunakan dalam lingkungan pengembangan perangkat lunak untuk menginstal perangkat lunak yang telah dikompilasi ke dalam sistem secara sistematis

$ iops32 
(nproc) digunakan untuk mengambil jumlah CPU atau prosesor yang tersedia pada sistem, dan perintah $ iops32 mungkin akan menjalankan serangkaian operasi integer pada setiap prosesor, kemudian mengukur dan melaporkan jumlah operasi per detik yang berhasil dilakukan.
$ iops64 $(nproc): Sama seperti perintah sebelumnya, namun untuk operasi integer 64 bit.
$ flops32 $(nproc): Perintah ini mungkin digunakan untuk mengukur jumlah operasi floating-point per detik (FLOPS) pada sistem dengan panjang bilangan pecahan 32 bit.
$ flops64 $(nproc): Sama seperti perintah sebelumnya, namun untuk operasi floating-point 64 bit.
![Screenshot (672)](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/25ba961c-e5e5-466b-a748-47df71f1d1d5)
percobaan 1
![Screenshot (673)](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/c8429495-142f-4659-b7bd-83c8e4d708d7)
percobaan 2
![Screenshot (674)](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/016427ef-ac67-40a7-87e8-9b8516bcc13b)
percobaan 3
![Screenshot (675)](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/b81c3044-705b-48f9-ae79-e39e5ee5d88f)
percobaan 4
![iops5](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/c4bbc07a-e7d8-4909-8178-a00f22e4ceb1)
![flops5](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/c49dca29-0931-4327-926a-e3f5d6bfd0d3)
percobaan 5

4. Apabila Debian VM mu masih belum terdapat packeage gcc, make dan git, lakukan instalasi dan catat setiap langkahnya!
- $ su -l
- $ apt install make
![isntall make](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/149fbe6f-ce8c-4b51-a3aa-f290c3e279f7)
- $ apt install git
![install git - Copy](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/109c83fd-6255-4d32-93eb-5f05b765d533)
- $ apt install gcc
![gcc1](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/98a0dab3-72aa-4c3f-8b4b-900217c01788)
![gcc2](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/a89b6f4b-e37d-4ee1-a4a3-11c22107e649)
