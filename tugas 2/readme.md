## BOOTING PROSESS
![Nama Alternatif](https://github.com/r4mmar/Sys0P24-3123521004/blob/main/tugas%202/assets/Operating%20System.jpg)

proses booting komputer adalah proses perjalanan penyalaan komputer awal sampai pengambilalihan sistem operasi secara penuh terhadap perangkat. Bisa juga diartikan sebagai proses pemasukan arus listrik kedalam peralatan komputer sehingga komputer dapat berkomunikasi dengan pengguna.

- Power On: Tahap awal saat komputer dihidupkan atau "dinyalakan". Pada titik ini, listrik mulai mengalir ke komponen-komponen komputer dan proses booting dimulai.
- BIOS/UEFI: Biasanya merupakan perangkat lunak firmware yang memulai proses booting komputer. BIOS (Basic Input/Output System) atau UEFI (Unified Extensible Firmware Interface) bertanggung jawab untuk melakukan tes awal terhadap perangkat keras dan memuat sistem operasi yang akan digunakan.
- Boot Device: Perangkat tempat sistem operasi dimuat saat proses booting. Ini bisa berupa hard drive, solid-state drive (SSD), USB flash drive, atau jaringan (dalam beberapa kasus).
- Operating System: Perangkat lunak yang mengelola sumber daya perangkat keras dan memberikan antarmuka antara perangkat keras dan perangkat lunak aplikasi. Contohnya termasuk Windows, macOS, dan Linux.
- Kernel: Bagian inti dari sistem operasi yang mengatur akses ke sumber daya perangkat keras, mengelola memori, dan menjalankan proses-proses utama sistem.
- System Process dan User Space: System processes adalah program-program yang berjalan di latar belakang untuk mengelola sistem operasi, seperti penjadwalan tugas dan manajemen memori. User space adalah lingkungan di mana aplikasi pengguna berjalan, seperti aplikasi pengolah kata atau peramban web.
- Komputer Siap Digunakan: Setelah proses booting selesai dan sistem operasi berhasil dimuat, komputer siap untuk digunakan oleh pengguna. Antarmuka pengguna akan muncul, dan pengguna dapat mulai menjalankan program-program dan tugas-tugas yang diinginkan. 

## IDENTIFIKASI KOMPUTER ANDA

### CPU
Pada tab CPU terdapat informasi seputar Prosessor, Clocks, Cache dan beberapa informasi lain.
#### Prosessor
- Name : adalah informasi tentang nama lengkap dari prosessor yaitu “Intel Celeron N4000”,
- Code Name : adalah informasi tentang kode prosessor yaitu “Gemini Lake”,
- Package : adalah informasi paket yang digunakan prosessor yaitu “Socket 1090 FCBGA”,
- Tecnology : adalah informasi tentang teknologi manufaktur yang digunakan untuk membuat prosessor yaitu “10 nm”,
- Specification : adalah informasi tentang nama nama lengkap dan no model prosessor,
- Family : adalah informasi keluarga prosessor yaitu “6”,
- Model : adalah informasi tentang model prosessor,
- Instructions : adalah daftar instruksi yang support oleh prosessor,
#### Clocks
- Core Speed : adalah informasi kecepatan clock dari inti prosessor yaitu “1108.74 MHz”,
- Multiplier : adalah informasi penganda yang digunakan untuk menentukan kecepatan clock inti,
- Bus Speed : adalah informasi kecepatan bus yang menghubungkan prosessor ke memori dan perangkat lain,
#### Cache
- L1 Data : adalah informasi ukuran cache L1 data yaitu “2 x 24 KBytes”,
- L1 Inst. : adalah infromasi ukuran cache L1 Iinstruksi yaitu“2 x 32 KBytes”,
- Level 2 : adalah informasi ukuran cache L2 yaitu “4 MBytes”,

### Mainboard
Pada tab Mainboard terdapat informasi seputar Motherboard, BIOS, dan Graphic Interface.
#### Mainboard
- Manufacturer : adalah informasi produsen dari motherboard yaitu “HP”,
- Model : adalah informasi tentang model motherboard yaitu “84B6”,
•   Bus Specs : adalah informasi spesifikasi bus yaitu “PCI-Express 2.0 (5.0 GT/s)”,
- Chipset : adalah informasi chipset yang digunakan motherboard yaitu “Intel Gemini Lake Host Bridge”,
#### BIOS
- Brand : adalah informasi merek BIOS yaitu “Insyde”,
- Version : adalah informasi versi BIOS Yaitu “F .58”,
- Date : adalah informasi tanggal produksi BIOS yaitu “06/12/2020”,

### MEMORY
Pada tab Memory terdapat informasi general memori dan timings.
#### General
- Type : adalah informasi jenis memori yang digunakan yaitu “DDR4”,
- Size : adalah informasi jumlah memori kapasitas memori yaitu “4 GBytes”,
#### Timings
- DRAM Frequency : adalah informasi clock speed memori yaitu “1188.9 MHz”,
- FBS:DRAM : adalah informasi rasio antara FBS dan DRAM clock speed yaitu “1:12”,

### SPD

Pada tab SPD terdapat informasi memory slot selection timings table.
#### Memory Slot Selection
- Memory Slot : adalah informasi yang menunjukan memori yang terpasang pada komputer, hanya ada satu memori yang terpasang,
- Module Size : adalah informasi yang menunjukan ukuran modul memori terpasang pada slot memori, modul memori yang terpasang adalah “4 GBytes”,
- Max Bandwidth : adalah informasi yang menunjukan bandwidth maksimal memori yaitu “DDR4-3200 (1600 MHz)”,
- Module Manuf : adalah informasi tentang nama manufaktur modul memori yaitu “Micron Technology”,
- Week/Year : adalah informasi yang menunjukan minggu dan tahun pembuatan modul memori yaitu “ 29/20 atau minggu ke-29 tahun 2020”,
- DRAM Manuf : adalah informasi temtang nama manufaktur DRAM (Dynamic Random Access
Memory) yang digunakan pada modul memori yaitu “Micron Technology”
- Ranks : adalah informasi tentang jumlah rank pada modul memori, rank adalah sekumpulan chip memori yang bekerja sama sebagai satu kesatuan, jumlah pada komputer yaitu “satu/single”,
- Part Number : adalah informasi nomor bagian modul memori, nomor bagian modul memori adalah “4ATF51264HZ-3G2J1”,
#### TIMINGS TABLE
- Frequency : adalah informasi yang menginformasikan frekuensi memori yaitu “1533 MHz”,
- CAS# Latency : adalah inforrmasi tentang latensi CAS (Column Address Strobe), latensi CAS
adalah waktu yang diperlukan untuk membuka sebuah kolom memori tertentu,
- RAS# to CAS# : adalah informasi yang menunjukan waktu yang diperlukan berpindah dari baris memori ke kolom memori,
- RAS# Precharge : adalah informasi tentang waktu yang dibutuhkan untuk menutup baris memori,
- tRAS : adalah informasi waktu yang diperlukan untuk membaca data dari baris memori,
- tRC : adalah informasi waktu yang diperlukan untuk membaca data dari kolom memori

### Grapics
Pada tab Grapics terdapat informasi GPU, Clocks, dan Memory.
- Display Device Selection : adalah informasi opsi yang memungkinkan memilih perangkat tampilan yang ingin dilihat informasinya,
#### GPU
- Name : adalah informasi tentang nama dari GPU yaitu “Intel UHD Graphics 600”,
- Board Manuf : adalah informasi tentang nama pabrikan motherboard,
- Revision : adalah informasi revisi CPU,
#### Clocks
- GFX Core : adalah informasi kecepatan clock dasar atau kecepatan maksimum di mana inti grafis dapat beroperasi.
