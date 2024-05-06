OPERATING SYSTEM
![Mind mapping](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/37726223-6d17-4ce2-851e-d3e67604ed88)

>>Introduction to Operating System

>Introduction
Sistem Operasi (OS) adalah kumpulan program yang bertindak sebagai antarmuka antara pengguna komputer dan perangkat keras komputer. Tujuan dari sistem operasi adalah untuk menyediakan lingkungan di mana pengguna dapat menjalankan program. Sistem Operasi dipandang sebagai manajer sumber daya.

>1.1 Operating System: Meaning
Sistem operasi (kadang-kadang disingkat "OS") adalah program yang, setelah awalnya dimuat ke dalam komputer oleh program booting, mengelola semua program lain dalam komputer. Program lain disebut aplikasi atau program aplikasi.

>1.2 History of Computer Operating Systems
Komputer awal tidak memiliki sistem operasi apa pun. Pengguna hanya menggunakan mesin dan akan datang dengan membawa program dan data, sering kali di atas kertas berlubang dan pita. Program akan dimuat ke dalam mesin, dan mesin akan diatur untuk bekerja sampai program selesai atau macet.

>1.3 Supervisor and User Mode
Mode pengguna tunggal adalah mode di mana sistem operasi komputer multiuser melakukan booting menjadi satu pengguna super. Mode ini terutama digunakan untuk pemeliharaan lingkungan multi-pengguna seperti jaringan server.

>1.4 Goals of an Operating System
Tujuan utama komputer adalah untuk menjalankan instruksi dengan cara yang ef cient dan untuk meningkatkan produktivitas sumber daya pemrosesan yang melekat pada sistem komputer seperti sumber daya perangkat keras, sumber daya perangkat lunak, dan pengguna.
o	Tujuan utama sistem operasi adalah membuat komputer nyaman digunakan.
o	Tujuan sekundernya adalah menggunakan perangkat keras dengan cara yang ef cient.

>1.5 Generations of Operating Systems
Sistem operasi telah berkembang selama bertahun-tahun. Anda akan brie y melihat perkembangan ini sistem operasi sehubungan dengan evolusi perangkat keras/arsitektur sistem komputer di bagian ini.
o	1.5.1 0th Generation
Istilah generasi ke-0 digunakan untuk merujuk pada periode perkembangan komputasi, yang mendahului produksi dan penjualan komersial peralatan komputer.
o	1.5.2 First Generation (1951-1956)
Generasi pertama  menandai dimulainya komputasi komersial, termasuk diperkenalkannya UNIVAC I dari Eckert dan Mauchy pada awal tahun 1951, dan beberapa saat kemudian, IBM 701 yang juga dikenal sebagai Kalkulator Pertahanan. Generasi pertama  ditandai lagi oleh tabung hampa udara sebagai teknologi komponen aktif. tabung vakum sebagai teknologi komponen aktif.
o	1.5.3 Second Generation (1956-1964)
Generasi kedua perangkat keras komputer terutama ditandai oleh transistor 
yang menggantikan tabung vakum sebagai teknologi komponen perangkat keras.
o	1.5.4 Third Generation (1964-1979)
Generasi ketiga resmi dimulai pada bulan April 1964 dengan pengumuman IBM tentang System/360 keluarga komputer System/360. Teknologi perangkat keras mulai menggunakan Sirkuit Terpadu (IC) yang menghasilkan signi keuntungan dalam hal kecepatan dan ekonomi.
o	1.5.5 Fourth Generation (1979-Present)
Generasi keempat ditandai dengan kemunculan komputer pribadi dan 
workstation. Miniaturisasi sirkuit dan komponen elektronik terus berlanjut dan Large Scale 
Integrasi Skala Besar (LSI), teknologi komponen dari generasi ketiga, digantikan oleh Integrasi Skala Scale Integration (VLSI), yang menjadi ciri generasi keempat.

>>Operation and Function of Operating System

>Introduction
Tujuan utama sistem operasi adalah untuk meningkatkan produktivitas sumber daya pemrosesan, seperti perangkat keras komputer atau pengguna sistem komputer. Kenyamanan dan produktivitas pengguna adalah pertimbangan sekunder.

>2.1 Operations and Functions of OS
o	Process Management
CPU mengeksekusi sejumlah besar program. Meskipun perhatian utamanya adalah eksekusi pengguna pengguna, CPU juga diperlukan untuk aktivitas sistem lainnya.
o	Memory Management
Memori adalah bagian yang paling mahal dalam sistem komputer. Memori adalah susunan besar kata-kata atau 
byte, masing-masing dengan alamatnya sendiri. Interaksi dicapai melalui urutan pembacaan atau penulisan alamat memori tertentu. CPU mengambil dari dan menyimpan dalam memori.
o	Secondary Storage Management
Tujuan utama sistem komputer adalah untuk menjalankan program. Program-program ini, bersama dengan 
data yang mereka akses, harus berada di memori utama selama eksekusi. Karena memori utama terlalu 
kecil untuk menampung semua data dan program secara permanen, sistem komputer harus menyediakan 
penyimpanan sekunder untuk mencadangkan memori utama.
o	I/O Management
Salah satu tujuan dari sistem operasi adalah untuk menyembunyikan keunikan atau spesifikasi perangkat keras 
perangkat keras dari pengguna. Sebagai contoh, pada UNIX, keistimewaan perangkat I/O disembunyikan dari 
sebagian besar sistem operasi itu sendiri oleh sistem I/O.
o	File Management
Manajemen file adalah salah satu layanan yang paling terlihat dari sistem operasi. Komputer dapat menyimpan 
informasi dalam beberapa bentuk fisik yang berbeda: pita magnetik, disk, dan drum adalah yang paling bentuk yang paling umum.
o	Protection
Berbagai proses dalam sistem operasi harus dilindungi dari aktivitas satu sama lain. Untuk 
Untuk itu, berbagai mekanisme yang dapat digunakan untuk memastikan bahwa À les, segmen memori, 
CPU dan sumber daya lainnya hanya dapat dioperasikan oleh proses-proses yang telah mendapatkan 
otorisasi dari sistem operasi.
o	Networking
Sistem terdistribusi adalah kumpulan prosesor yang tidak berbagi memori atau clock. Sebaliknya, masing-masing 
prosesor memiliki memori lokalnya sendiri, dan prosesor berkomunikasi satu sama lain melalui berbagai jalur komunikasi, seperti bus berkecepatan tinggi atau saluran telepon.
o	Command Interpretation
Salah satu komponen terpenting dari sistem operasi adalah penerjemah perintahnya. Penerjemah perintah 
adalah antarmuka utama antara pengguna dan seluruh sistem.

>2.2 Types of Operating System
Sistem operasi komputer modern dapat diklasifikasikan ke dalam tiga kelompok, yang dibedakan berdasarkan sifat interaksi yang terjadi antara pengguna komputer dan programnya selama pemrosesan. Ketiga kelompok tersebut disebut sistem operasi batch, pembagian waktu, dan waktu nyata Sistem.
o	Batch Processing Operating System
Dalam lingkungan sistem operasi pemrosesan batch, pengguna mengirimkan pekerjaan ke tempat pusat di mana 
pekerjaan ini dikumpulkan ke dalam batch, dan kemudian ditempatkan pada antrian input di komputer di mana mereka akan dijalankan.
o	Time Sharing
Mode lain untuk memberikan layanan komputasi disediakan oleh sistem operasi berbagi waktu 
sistem. Dalam lingkungan ini, komputer menyediakan layanan komputasi untuk beberapa atau banyak pengguna 
secara bersamaan secara online.
o	Real-time Operating System (RTOS)
Kelas ketiga adalah sistem operasi waktu nyata, yang dirancang untuk melayani aplikasi-aplikasi 
di mana waktu respons sangat penting untuk mencegah kesalahan, kesalahan penyajian, atau bahkan bencana.
o	Multiprogramming Operating System
Sistem operasi multipemrograman adalah sistem yang memungkinkan lebih dari satu program pengguna aktif 
(atau bagian dari program pengguna) untuk disimpan dalam memori utama secara bersamaan.
o	Multiprocessing System
Sistem multiprosesor adalah konfigurasi perangkat keras komputer yang mencakup lebih dari satu 
unit pemrosesan independen.
o	Networking Operating System
Sistem komputasi jaringan adalah kumpulan komputer fisik yang saling terhubung. Sistem operasi Sistem operasi dari masing-masing komputer yang saling terhubung harus berisi, selain fungsinya sendiri fungsionalitas yang berdiri sendiri, ketentuan untuk menyerahkan komunikasi tambahan ini tidak berubah struktur esensial dari sistem operasi.
o	Distributed Operating System
Sistem komputasi terdistribusi terdiri dari sejumlah komputer yang terhubung dan dikelola sehingga mereka secara otomatis berbagi beban pemrosesan pekerjaan di antara komputer, atau memisahkan beban pekerjaan yang sesuai dengan prosesor tertentu.
o	Operating Systems for Embedded Devices
Karena sistem tertanam (PDA, ponsel, perangkat tempat penjualan, VCR, kontrol robot industri, 
atau bahkan pemanggang roti Anda) menjadi lebih kompleks dari segi perangkat keras di setiap generasi, dan lebih banyak lagi fitur dimasukkan ke dalamnya dari hari ke hari, aplikasi yang mereka jalankan membutuhkan lebih banyak dan lebih banyak lagi untuk dijalankan kode sistem operasi yang sebenarnya untuk menjaga agar waktu pengembangan tetap masuk akal.
o	Single Processor System
Secara teori, setiap sistem komputer dapat diprogram dalam bahasa mesinnya, tanpa dukungan perangkat lunak. Pemrograman "mesin telanjang" adalah kebiasaan untuk komputer awal sistem.
o	Parallel Processing System
Sistem operasi paralel terutama berkaitan dengan pengelolaan sumber daya mesin paralel. Tugas ini menghadapi banyak tantangan: pemrogram aplikasi menuntut semua kinerja mungkin, banyak konvensi perangkat keras yang ada dan berubah dengan sangat cepat, namun sistem operasi harus semakin kompatibel dengan versi mainstream yang digunakan di komputer pribadi dan workstation karena tekanan pengguna dan sumber daya terbatas yang tersedia untuk pengembangan versi baru dari sistem ini.
o	Multitasking
Dalam komputasi, multitasking adalah metode di mana beberapa tugas, juga dikenal sebagai proses, berbagi sumber daya pemrosesan umum seperti CPU. Dalam kasus komputer dengan CPU tunggal, hanya satu tugas dikatakan berjalan pada titik waktu tertentu, yang berarti bahwa CPU secara aktif mengeksekusi instruksi untuk tugas itu.

>2.3 Operating System: Examples
o	2.3.1 Disk Operating System (DOS
DOS (Disk Operating System) adalah sistem operasi pertama yang diinstal secara luas untuk komputer. Ini adalah program kontrol utama yang secara otomatis dijalankan ketika Anda memulai komputer (PC). DOS tetap berada di dalam komputer sepanjang waktu sehingga Anda dapat menjalankan program dan mengelola À les.
o	2.3.2 UNIX
Sistem operasi UNIX digunakan pada produk workstation yang banyak dijual dari Sun Microsystems, Silicon Graphics, IBM, dan sejumlah perusahaan lainnya. Lingkungan UNIX dan model program model program klien/server merupakan elemen penting dalam pengembangan Internet dan membentuk kembali komputasi yang berpusat pada jaringan dan bukan pada komputer individual.
o	2.3.3 Windows
Windows adalah sistem operasi komputer pribadi dari Microsoft yang, bersama dengan beberapa aplikasi bisnis yang umum digunakan seperti Microsoft Word dan Excel, telah menjadi de facto "standar" untuk pengguna individu di sebagian besar perusahaan dan juga di sebagian besar rumah.
o	2.3.4 Macintosh
Macintosh (sering disebut "Mac"), yang diperkenalkan pada tahun 1984 oleh Apple Computer, adalah komputer 
komputer pribadi pertama yang dijual secara luas dengan Antarmuka Pengguna Grafis (GUI).
