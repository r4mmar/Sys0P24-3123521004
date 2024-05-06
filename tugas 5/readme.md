## TUGAS PENDAHULUAN:

## Jawablah pertanyaan-pertanyaan di bawah ini :

1. Apa yang dimaksud redirection?<br>
Pembelokan/redirection adalah mengalihkan file descriptor dari 0, 1, dan 2 yang dilakukan untuk standard 
input, output dan error. ada redirection output (>) untuk menyimpan hasil atau output kedalam sebuah file 
dan input redirection (<) untuk mengambil sebuah ke dalam file lain.
2. Apa yang dimaksud pipeline?<br>
Pipeline (|) adalah mekanisme untuk alat komunikasi atau menghubungkan, misal ada proses1 lalu agar 
output dari proses1 menjadi inputan dari proses2 maka digunakannya pipeline (|) untuk menghubungkan 
proses1 dan proses2.
3. Apa yang dimaksud perintah di bawah ini :<br>
    echo, cat, more, sort, grep, wc, cut, uniq<br>
* Echo: Perintah yang digunakan untuk menampilkan string atau variabel ke terminal. Anda dapat menggunakan perintah ini dengan menyertakan string yang ingin ditampilkan sebagai argumennya.
* cat: perintah yang digunakan untuk menampilkan isi file di terminal atau menggabungkan beberapa file menjadi satu. Anda dapat menggunakan perintah ini dengan menyertakan nama file yang ingin ditampilkan sebagai argumennya.
* more: digunakan untuk menampilkan isi dari sebuah file teks secara bertahap, halaman per halaman. Utilitas ini berguna ketika Anda memiliki file teks yang panjang dan ingin melihatnya secara bertahap tanpa memuat seluruh konten sekaligus.
* sort: Digunakan untuk mengurutkan masukannya berdasarkan urutan nomor ASCII dari karakter.
* grep: Digunakan untuk menyaring masukan dan menampilkan baris-baris yang hanya mengandung pola yang ditentukan.
* wc: digunakan untuk menghitung jumlah baris, kata dan karakter dari baris-baris masukan yang diberikan kepadanya.
* cut: Digunakan untuk mengambil kolom tertentu dari baris-baris masukannya, yang ditentukan pada option -c.
* uniq: Digunakan untuk menghilangkan baris-baris berurutan uyang mengalami duplikasi, biasanya digabungkan dalam pipeline dengan sort.

## PERCOBAAN:

1. Login sebagai user.
2. Bukalah Console Terminal dan lakukan percobaan-percobaan di bawah ini. Perhatikan hasil setiap percobaan.
3. Selesaikan soal-soal latihan.


## Percobaan 1 : File descriptor

1. Output ke layar (standar output), input dari system (kernel)
    ```
    $ ps
    ```
    ![p11](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/e52b6806-8410-4712-9593-9320b408ce2c)
<br> Keterangan : Perintah $ ps digunakan untuk untuk menampilkan informasi tentang proses yang sedang aktif di dalam sistem.

3. Output ke layar (standar output), input dari keyboard (standard input)
   ```
    $ cat
    hallo, apa khabar
    hallo, apa khabar
    exit dengan ^d
    exit dengan ^d
    [Ctrl-d]
   ```
    ![p12](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/f2568506-67b7-41ed-b212-c4886d05d1ac)
   <br> Keterangan : Perintah cat digunakan untuk untuk menampilkan informasi tentang proses yang sedang aktif di dalam sistem.

5. Input nama direktori, output tidak ada (membuat direktori baru), bila terjadi error maka tampilan error pada layar (standard error)
   ```
   $ mkdir mydir
   $ mkdir mydir **(Terdapat pesan error)**
   ```
    ![p13](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/37dd3a4f-7b44-4464-bde8-b81e57ef335d)
<br> Keterangan : Perintah mkdir perintah yang digunakan untuk membuat direktori baru di dalam filesystem.

## Percobaan 2 : Pembelokan (redirection)
1. Pembelokan standar output
   ```
    $ cat 1> myfile.txt
    Ini adalah teks yang saya simpan ke file myfile.txt
   ```
   ![Screenshot (472)](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/8c7da49e-f07a-48e5-9508-bcd3d12751b2)
<br> Keterangan : Perintah “cat 1> myfile.txt” digunakan untuk meng-input‐kan dengan keyboard dan tanda "1>" merupakan pengganti dari standard output.

3. Pembelokan standar input, yaitu input dibelokkan dari keyboard menjadi dari file
   ```
    $ cat 0< myfile.txt
    $ cat myfile.txt
   ```
   ![Screenshot (473)](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/8806e7a6-93d8-4871-b669-ccece05a8885)
<br> Keterangan : Perintah “cat 0< myfile.txt” ini digunakan untuk file input dibelokkan dari keyboard dari file sehingga antara “cat 0< myfile.txt” dan “cat myfile.txt” memiliki keterkaitan.

5. Pembelokan standar error untuk disimpan di file
   ```
    $ mkdir mydir (Terdapat pesan error)
    $ mkdir mydir 2> myerror.txt
    $ cat myerror.txt
   ```
   ![Screenshot (474)](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/d01f6083-878d-4eea-9756-f0cdf66e97f4)
<br> Perintah “mkdir mydir” digunakan untuk membuat folder dengan nama mydir tetapi muncul pesan error, karena sudah dibuat sebelumnya. Selanjutnya, pada perintah “mkdir mydir 2> myerror.txt” digunakan untuk membelokkan (memindahkan) pesan error sebelumnya ke dalam file myerror.txt. Tanda "2>" menandakan bahwa output standard error. Selanjutnya, pada perintah “cat myerror.txt” digunakan untuk memunculkan teks yang terdapat dalam file myerror.txt berupa pesan error yang telah dibelokkan sebelumnya.

7. Notasi 2>&1 : pembelokan standar error (2>) adalah identik dengan file descriptor 1.
   ```
    $ ls filebaru (Terdapat pesan error)
    $ ls filebaru 2> out.txt
    $ cat out.txt
    $ ls filebaru 2> out.txt 2>&
    $ cat out.txt
   ```
   ![Screenshot (475)](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/cc705676-33e1-4638-bbe6-076d2ca35a7e)
<br> Pembelokan standard error (2>) adalah identik dengan file descriptor 1. Perintah “ls filebaru” digunakan untuk menampilkan isi dari folder atau direktori dari filebaru. Tetapi, muncul pesan error karena direktori filebaru tidak ada. Kemudian, perintah “ls filebaru 2> out.txt” digunakan untuk memindahkan pesan error tersebut ke dalam file out.txt melalui standard error yang ditandai dengan "2>". Kemudian, perintah “ls filebaru 2 > out.txt 2>&1” mempunyai fungsi yang sama dengan perintah “cat out.txt.”.

9. Notasi 1>&2 (atau >&2) : pembelokan standar output adalah sama dengan file descriptor 2 yaitu standar error
   ```
   $ echo “mencoba menulis file” 1> baru
   $ cat filebaru 2> baru 1>&
   $ cat baru
   ```
   ![Screenshot (476)](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/be338c90-9e8c-4bf0-a708-8e99688d8810)
   <br> Perintah echo "mencoba menulis file" >1 baru digunakan untuk menulis kata "mencoba menulis file" yang kemudian dibelokkan ke filebaru yang ditandai dengan tanda "1>". Selanjutnya, pada perintah “cat filebaru 2> baru 1>&2” digunakan untuk membelokkan tampilan filebaru ke standard output yang ditandai dengan tanda "1>&2" yang berarti sama dengan descriptor 2 yaitu standard error.

10. Notasi >> (append)
   ```
   $ echo “kata pertama” > surat
   $ echo “kata kedua” >> surat
   $ echo “kata ketiga” >> surat
   $ cat surat
   $ echo “kata keempat” > surat
   $ cat surat
   ```
   ![Screenshot (477)](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/017cd74b-4f6c-4301-865f-852937a5a856)
   <br> Perintah echo "kata pertama" > surat digunakan untuk menulis kalimat "kata pertama" ke dalam file surat. Selanjutnya, pada perintah echo "kata kedua" >> surat digunakan untuk menulis "kata kedua" ke dalam file surat tanpa menghapus teks sebelumnya yang ditandai dengan ">>". Selanjutnya, pada perintah echo "kata ketiga" >> surat digunakan untuk menulis kalimat "kata ketiga" ke dalam file surat tanpa menghapus teks sebelumnya. Kemudian, teks tersebut ditampilkan dengan perintah cat surat. Selanjutnya, perintah echo "kata keempat" > surat digunakan untuk menulis "kata keempat" dengan menghapus teks sebelumnya yang ditandai dengan tanda ">". Kemudian perintah cat surat digunakan untuk menampilkan isi file surat.

11. Notasi here document (<<++ .... ++) digunakan sebagai pembatas input dari keyboard. Perhatikan bahwa tanda pembatas dapat digantikan dengan tanda apa saja, namun harus sama dan tanda penutup harus diberikan pada awal baris
   ```
   $ cat <<++
   Hallo, apa kabar?
   Baik-baik saja?
   Ok!
   ++
   $ cat <<%%%
   Hallo, apa kabar?
   Baik-baik saja?
   Ok!
   %%%
   ```
   ![Screenshot (478)](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/965e467a-8cce-42c7-83b3-401ce49bb6c0)
<br> Tanda ++ ... ++ digunakan sebagai pembatas input dari keyboard. Tanda tersebut bisa diganti oleh tanda apa saja asalkan pada awal dan akhirnya sama. Pada saat mengetikkan perintah “cat << ++” kemudian mengetikkan kalimat, setelah enter ternyata bisa memasukkan beberapa kalimat lagi. Tetapi, saat menuliskan kalimat ++, sistem menghentikan proses kemudian menampilkannya.

11. Notasi – (input keyboard) adalah representan input dari keyboard. Artinya menampilkan file 1, kemudian menampilkan input dari keyboard dan menampilkan file 2. Perhatikan bahwa notasi “-“ berarti menyelipkan input dari keyboard
  ```
  $ cat myfile.txt – surat
  ```
  ![Screenshot (479)](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/09f7b3bb-7dde-4769-a5eb-60e4b082fbc2)
<br> Tanda "‐" (input dari keyboard) adalah representan input dari keyboard. Artinya, menampilkan file 1, kemudian menampilkan input dari keyboard dan menampilkan file 2. Tanda "‐" menyatakan bahwa menyelipkan input dari keyboard. Pada terminal ini, akan menampilkan isi file dari "myfile.txt" sekaligus menampilkan file "surat".

## Percobaan 3 : Pipa (pipeline)

1. Operator pipa (|) digunakan untuk membuat eksekusi proses dengan melewati data langsung ke data lainnya.
   ```
   $ who
   $ who | sort
   $ who | sort –r
   $ who > tmp
   $ sort tmp
   $ rm tmp
   $ ls –l /etc | more
   $ ls –l /etc | sort | more
   ```
   ![Screenshot (481)](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/8153f443-7032-46b1-88ea-8b3c916ca06e)
   ![Screenshot (483)](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/d243435f-49c9-4316-a57f-3fa7486e9cea)
   <br> Pipeline memungkinkan user untuk menggabungkan beberapa perintah secara efisien, dengan output dari satu perintah menjadi input untuk perintah berikutnya. Hal ini sangat berguna untuk memproses dan menganalisis data secara langsung tanpa perlu menyimpannya dalam file sementara.

2. Untuk membelokkan standart output ke file, digunakan operator ">"
   ```
   $ echo hello
   $ echo hello > output
   $ cat output
   ```
   ![Screenshot (484)](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/91e270bf-bc54-4e5d-9593-b512d9e68cf8)
   <br> Perintah “echo hello” digunakan untuk menampilkan teks "hello" seketika itu juga. Selanjutnya, perintah “echo hello > output” digunakan untuk membelokkan kata "hello" ke file output. Selanjutnya, perintah “cat output” digunakan untuk menampilkan isi dari file output.

3. Untuk menambahkan output ke file digunakan operator ">>"
   ```
   $ echo bye >> output
   $ cat output
   ```
    ![Screenshot (485)](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/2a522f3d-c5c0-4442-9cfe-2166efd80ac4)
      <br> Perintah “echo bye >> output” digunakan untuk menambahkan teks "bye" ke dalam file output yang ditandai dengan ">>". Setelah itu, perimtah “cat output” digunakan untuk menampilkan isi dari file output.

5. Untuk membelokkan standart input digunakan operator "<"
   ```
   $ cat < output
   ```
   ![Screenshot (486)](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/56292239-6dbc-408e-b537-243dbd1852cb)
   <br> Perintah “cat < output > out” dan “cat out” merupakan perintah yang dikombinasikan untuk membelokkan standard output dari file output menjadi standard input untuk file out sehingga hasil standard output‐nya sama. Selanjutnya, perintah “cat < output >> out” digunakan untuk membelokkan standard output dari file output menjadi penambahan output ke file yang bernama out. Sehingga, output dari file out akan ditambahkan dengan output dari file output. Selanjutnya, perintah “cat output >> out”, “cat out”, “cat < output > output”, “cat output”, “cat < out >> out” tidak diperkenankan karena menggunakan nama file yang sama. Maka, akan muncul tulisan terus menerus hingga menekan tombol CTRL+c

6. Pembelokan standart input dan standart output dapat dikombinasikan tetapi tidak boleh menggunakan nama file yang sama sebagai standart input dan output.
   ```
   $ cat < output > out
   $ cat out
   $ cat < output >> out
   $ cat out
   $ cat < output > output
   $ cat output
   $ cat < out >> out (Proses tidak berhenti)
   [Ctrl-c]
   $ cat out
   ```
   ![Screenshot (487)](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/548e3daf-0213-4a2b-8cc9-907e8c6d33b1)

## Percobaan 4 : Filter
1. Pipa juga digunakan untuk mengkombinasikan utilitas sistem untuk membentuk fungsi yang lebih kompleks
   ```
    $ w –h | grep <user>
    $ grep <user> /etc/passwd
    $ ls /etc | wc
    $ ls /etc | wc –l
    $ cat > kelas1.txt
    Badu
    Zulkifli
    Yulizir
    Yudi
    Ade
    [Ctrl-d]
    $ cat > kelas2.txt
    Budi
    Gama
    Asep
    Muchlis
    [Ctrl-d]
    $ cat kelas1.txt kelas2.txt | sort
    $ cat kelas1.txt kelas2.txt > kelas.txt
    $ cat kelas.txt | sort | uniq
   ```
   ![p41](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/e2599eb1-e4df-4b35-86f1-9ae65627d439)
   ![p42](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/f2ef1fdb-e277-49f8-a1df-8caae7e4953c)
   <br> $ cat > kelas1.txt: Perintah ini membuka editor untuk membuat atau mengedit file bernama kelas1.txt

## LATIHAN:

1. Lihat daftar secara lengkap pada direktori aktif, belokkan tampilan standard output   ke file baru.
![Screenshot (678)](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/fdca7762-9b47-4ac2-93a8-7b5f6503b097)
2. Lihat daftar secara lengkap pada direktori /etc/passwd, belokkan tampilan standard output ke file baru tanpa menghapus file baru sebelumnya.
![Screenshot (679)](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/41e527eb-8319-4a6c-9ccc-a5a0dea41b2f)
3. Urutkan file baru dengan cara membelokkan standard input.
![Screenshot (680)](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/d4e2e47b-5587-4ab0-9cc1-e79198059784)
4. Urutkan file baru dengan cara membelokkan standard input dan standard output ke file baru.urut.
![Screenshot (681)](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/1bd60e9e-feeb-4fd7-89b3-8446e7f2c579)
5. Buatlah direktori latihan 2 sebanyak 2 kali dan belokkan standard error ke file rmdirerror.txt.
![Screenshot (682)](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/06ddd1ad-3989-4e7d-a856-2c35c7115689)
6. Urutkan kalimat berikut :
   ```
   Jakarta
   Bandung
   Surabaya
   Padang
   Palembang
   Lampung
   ```
  Dengan menggunakan notasi **here document (<@@@ ...@@@)** . [HINT](https://www.geeksforgeeks.org/how-to-use-here-document-in-bash-programming/)
  ![Screenshot (684)](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/52882310-c8ef-4e8b-9cde-702ff70038f4)
7. Hitung jumlah baris, kata dan karakter dari file baru.urut dengan menggunakan filter dan tambahkan data tersebut ke file baru.
8. Gunakan perintah di bawah ini dan perhatikan hasilnya.
   ```
    $ cat > hello.txt
    dog cat
    cat duck
    dog chicken
    chicken duck
    chicken cat
    dog duck
    [Ctrl-d]
    $ cat hello.txt | sort | uniq
    $ cat hello.txt | grep “dog” | grep –v “cat”
   ```
![Screenshot (683)](https://github.com/r4mmar/Sys0P24-3123521004/assets/160557580/b7b6a51e-dca3-436f-b37e-4719a3b91a4b)


## LAPORAN RESMI:

1. Analisa hasil percobaan 1 sampai dengan 4, untuk setiap perintah jelaskan    tampilannya.
2. Kerjakan latihan diatas dan analisa hasilnya
3. Berikan kesimpulan dari praktikum ini.

## KESIMPULAN
Proses I/O, file descriptor, redirection, dan pipeline adalah konsep-konsep fundamental dalam sistem operasi dan pengelolaan aliran data di dalamnya.
Proses I/O (Input/Output) :
Sebuah proses memerlukan Input dan Output. Instruksi (command) yang diberikan pada Linux melalui Shell disebut sebagai eksekusi program yang selanjutnya disebut proses. Setiap kali instruksi diberikan, maka Linux kernel akan menciptakan sebuah proses dengan memberikan nomor PID (Process Identity). Proses dalam Linux selalu membutuhkan Input dan menghasilkan suatu Output.
File Descriptor :
- File descriptor adalah angka yang digunakan oleh sistem operasi untuk mengidentifikasi dan merujuk ke file atau aliran data yang terbuka oleh proses.
- File descriptor ini sering kali diasosiasikan dengan tiga deskriptor standar: 0 = keyboard (standar input), 1 = layar(standar output), dan 2 = layar (standar error).
Redirection :
- Redirection adalah proses mengubah aliran data standar masukan (stdin), keluaran (stdout), dan keluaran kesalahan (stderr) dari dan ke file lain.
- Dalam sistem UNIX/Linux, operator seperti '<', '>', dan '>>' digunakan untuk mengalihkan aliran data dari dan ke file.
Pipeline :
- Pipa adalah mekanisme di sistem operasi UNIX/Linux yang memungkinkan keluaran dari satu program digunakan sebagai masukan untuk program lainnya secara berurutan.
- Pipa menggunakan operator '|' untuk menghubungkan beberapa perintah bersama-sama, sehingga keluaran dari perintah pertama menjadi masukan bagi perintah kedua, dan seterusnya.
