##Dokumentasi Perancangan Keamanan Sistem dan Jaringan

>###Penulis
>* M. Syaiful Jihad A.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5113100022
>* Yoga Bayu Aji P.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5113100023
>* Bagas Andita S.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5113100029

###Percobaan serangan Brute-Force pada SSH Server

#####Simulasi dan skema serangan
&nbsp;&nbsp;&nbsp;&nbsp;Percobaan yang akan dibuat adalah melakukan _brute-force attack_ pada sebuah sever yang dipasang ssh server.

&nbsp;&nbsp;&nbsp;&nbsp;1. Persiapan environment yang akan digunakan untuk simulasi.
Disini kita menggunakan sebuah host dengan sistem operasi Ubuntu Server 14.04 yang telah terinstall openSSH-server. Sistem operasi ini akan digunakan sebagai target serangan. Kemudian digunakan sistem operasi Kali Linux yang akan digunakan sebagai komputer penyerang.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;a. Instalasi host dengan menggunakan Virtualbox.
Sebelum melakukan serangan kita harus menyiapkan kedua buah sistem operasi yang akan digunakan untuk simulasi. Pertama kita menginstall dulu ubuntu server 14.04. Setelah itu install openSSH-server pada sistem operasi tersebut. 
```
$ sudo apt-get install openssh-server
```
Setelah server yang akan menjadi korban serangan siap, kita melakukan instalasi sistem operasi untuk penyerang. Pada komputer penyerang kita akan menggunakan beberapa tools yaitu: _Hydra, Ncrack,_ dan _Medusa._
Langkah selanjutnya pastikan antara sever korban dan penyerang sudah terhunung.
Dari sisi penyerang, kita akan melakukan test dahulu apakah port SSH dari server terbuka dengan menggunakan nmap.
```
# nmap -sV [_IP address korban_]
```
Jika port 22 sudah terbuka, maka selanjutnya kita mempersiapkan _dictionary password_ yang digunakan untuk mencoba masuk ke server korban. Pada 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;b. Setting alamat IP untuk masing-masing host sehingga dapat saling terhubung satu sama lain.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;c. Melakukan simulasi serangan brute-force SSH dengan menggunakan aplikasi Hydra dan Ncrack.