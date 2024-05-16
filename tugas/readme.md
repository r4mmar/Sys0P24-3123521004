# Reader-Writer Problem

## Pengantar
Masalah Reader-Writer adalah masalah klasik dalam pengendalian konkuren yang berhubungan dengan sinkronisasi akses ke sumber daya bersama. Masalah ini sering muncul dalam database atau struktur data yang dibaca dan ditulis oleh banyak thread atau proses.

## Deskripsi Masalah
- **Readers**: Proses yang hanya membaca data.
- **Writers**: Proses yang dapat membaca dan menulis data.

Tujuannya adalah untuk mengelola akses ke sumber daya sehingga:
- Beberapa pembaca bisa membaca data secara bersamaan tanpa saling mengganggu.
- Penulis harus memiliki akses eksklusif ke data, yang berarti tidak boleh ada pembaca atau penulis lain yang mengakses data saat seorang penulis sedang menulis.

## Tantangan
- **Race Condition**: Keadaan di mana hasil dari operasi tergantung pada urutan eksekusi yang tidak diinginkan.
- **Deadlock**: Ketika dua atau lebih proses menunggu satu sama lain untuk melepaskan sumber daya yang diinginkan.
- **Starvation**: Ketika satu atau lebih proses tidak pernah mendapatkan akses ke sumber daya yang dibutuhkan.

## Solusi Potensial
### Reader Preference Solution
- Memberikan prioritas kepada pembaca.
- Pembaca bisa terus membaca selama tidak ada penulis yang menunggu. Namun, ini bisa menyebabkan penulis mengalami starvation.

### Writer Preference Solution
- Memberikan prioritas kepada penulis.
- Jika seorang penulis ingin menulis, pembaca baru tidak diizinkan untuk memulai membaca sampai penulis selesai. Ini bisa menyebabkan pembaca mengalami starvation.

### Fair Reader-Writer Solution
- Menggunakan algoritma yang adil untuk memastikan tidak ada proses yang mengalami starvation.
- Semaphore atau mekanisme sinkronisasi lain dapat digunakan untuk menjaga keseimbangan antara pembaca dan penulis, memastikan bahwa semua proses mendapatkan giliran yang adil untuk mengakses sumber daya.
