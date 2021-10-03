# Manage Servers With Terminal

## Apa itu Terminal?
__Terminal__ adalah salah satu aplikasi yang paling sering digunakan untuk update dan upgrade sistem atau software, isntall aplikasi, update kernel, sering juga digunakan untuk menjalankan aplikasi, membuat folder baru atau menghapusnya, dan masih banyak hal-hal lainnya yang bisa dilakukan menggunakan terminal.
## Apa itu BASH?
__BASH__ __*(Bourne-Again Shell)*__ adalah syel unix dan bahasa skrip yang menjadi syel di sebagian besar sistem linux dan macOS atau bahasa yang berjalan di atas kernel (linux/unix), yang berfungsi sebagai penerjemah antara user dan sistem operasi.
## Text Editor
__Text Editor__ adalah perangkat lunak yang bisa digunakan untuk mengedit berkas konfigurasi sistem atau kode sumber bahasa pemrograman dalam bentuk penyunting teks biasa layaknya aplikasi pengolah kata tanpa pengaturan layout, format dokumen dan lain-lain.
#### Text Editor With Nano
jika menggunakan linux, maka secara default nano sudah terinstall pada sistem operasi linux

masukkan perintah berikut pada terminal nano pada linux untuk memeriksa versi nano yang sudah terinstall secara default :
- > __nano --version__
![nano --version](https://user-images.githubusercontent.com/90192123/135763150-de1769c3-20c2-4940-a94a-f54fc6f28b66.png)

untuk membuka file dengan nano, lakukan perintah berikut pada terminal :
- > __nano file.txt__

![nano file txt](https://user-images.githubusercontent.com/90192123/135763337-c2ae3906-a1bc-4d96-9351-fb5a0db86065.png)

atau bisa menggunakan perintah
- > __nano/lokasi/folder/file.txt__

![text editor nano](https://user-images.githubusercontent.com/90192123/135763472-d4daf616-7ad2-4d5b-a771-40cbea265725.png)

dibagian bawah jendela text editor, ada daftar cara pintas perintah paling dasar untuk digunakan dengan editor nano.
semua perintah diawal dengan karakter __(^)__ atau __(M)__. simbol caret __(^)__ mewakili tombol __(ctrl)__. misalnya, perintah __(^J)__ berarti  menekan tombol __(Ctrl+J)__ secara bersamaan. huruf __(M)__ mewakili tombol __(Alt)__. 

![cara pintas perintah](https://user-images.githubusercontent.com/90192123/135763410-4d5453be-1a4d-4c13-9a01-4590ca3e8765.png)

anda juga bisa mendapatkan daftar semua perintah yang tersedia dengan menekan __(Ctrl+g)__ pada keyboard. 
![daftar command](https://user-images.githubusercontent.com/90192123/135763703-eb520ce4-b0bd-47d9-b5e4-13154b7e4840.png)

- > __CTRL+O__ kemudian tekan __Enter__ : untuk menyimpan atau save, tanpa harus menutup aplikasi nano
- > __CTRL+X__ untuk keluar dari editor nano, akan tetapi jika melakukan perubahan maka akan diminta untuk konfirmasi apakah perubahan tersebut akan disimpan atau tidak, maka akan muncul seperti ini

![yes no cancel](https://user-images.githubusercontent.com/90192123/135763986-5e4475af-42e5-4baf-856a-5111b3e6a9a0.png)

*Jika ingin menyimpan ketik __Y__ __(CTRL+X lalu tekan Y kemudian tekan Enter)__*

*Jika tidak ingin menyimpan ketik __N__ __(CTRL+X lalu tekan N kemudian tekan Enter)__*

*Jika ingin meng-cancel ketik __CTRL+C__ __(CTRL+X lalu tekan CTRL+C)__*

- > __CTRL+W__ : untuk mencari text, Masukkan kata/value yang ingin dicari dikolom pencarian kemuadian tekan __Enter__
![ctrl w](https://user-images.githubusercontent.com/90192123/135764325-3e0c30e3-3759-45f4-b415-b2a74295153e.png)

- > __ALT+A__ : untuk menyorot teks, setelah menekan __ALT+A__ cukup arahkan cursor pada teks yang ingin di select 
![alt a](https://user-images.githubusercontent.com/90192123/135764450-ae851472-8281-4f9e-a922-72adf427aad1.png)

lalu untuk Copy Paste bisa lakukan perintah berikut :
- > __ALT+6__ : untuk melakukan copy teks yang telah di select
- > __CTRL+U__ : untuk melakukan paste teks yang sudah dicopy
- > __CTRL+K__ : untuk melakukan cut pada text yang sudah di select
![copy](https://user-images.githubusercontent.com/90192123/135764849-9f0747ca-1d4d-478b-aaab-b1d4a9cc7f92.png)
![cut](https://user-images.githubusercontent.com/90192123/135764855-11d60f21-bc05-45e3-95ca-05396af53e6b.png)
![paste](https://user-images.githubusercontent.com/90192123/135764866-c2ec4920-a6e5-4e1f-afdf-c6e4ef2bc7de.png)

- > __(CTRL+A)__ : untuk memindahkan cursor ke awal baris
![ctrl a](https://user-images.githubusercontent.com/90192123/135764912-49a339ed-de21-4758-a1eb-47cd06789a89.png)

- > __(CTRL+E)__ : untuk memindahkan cursor ke baris akhir
![ctrl e](https://user-images.githubusercontent.com/90192123/135764968-45fc8e50-72d1-4039-b0a7-de9284593b48.png)

## Text Manipulation
pada dasarnya kita bisa melakukan manipulasti pada sebuah file menggunakan terminal, tanpa menggunakan teks editor seperti nano. berikut adalah contoh perintah yanng dapat dilakukan :
- __cat__
- __less__
- __tail__
- __sed__
- __sort__
- __grep__
- __head__
- __diff__

> cat adalah salah satu perintah yang berfungsi untuk membuat daftar konten atau isi file pada standard output (sdout). contoh :
  - > cat file.txt : untuk melihat isi file
  - > cat>file-contoh : untuk membuat file baru dan memasukkan teks
  - > cat file1file2>file3 : untuk menggabungkan dua file dan menyimpannya difile3

![cat](https://user-images.githubusercontent.com/90192123/135765395-3d82a9c8-807e-4e8a-87cc-7e3fec0d6ca6.png)

![cat file cnth](https://user-images.githubusercontent.com/90192123/135765405-1f298f37-a775-4f58-ad2d-8a4591bada89.png)

![cat file baru](https://user-images.githubusercontent.com/90192123/135765415-81c98a97-ac65-4be3-91e5-3bd2445597d6.png)

> __sed__ adalah singkatan dari __*stream editor*__ . gunanya untuk memanipulasi teks dasar pada file. dengan menggunakan perintah sed kita dapat mengganti teks dengan cepat. contoh :
  - > __sed -i 's/pada/di/g'filebaru__
ini akan mengganti semua kata 'pada' menjadi 'di' pada filebaru
![sed](https://user-images.githubusercontent.com/90192123/135765591-30539f03-ee76-4315-a603-e8282c4f6643.png)

> __grep__ merupakan perintah untuk melakukan pencarian sebuah text dalam sebuah file yang telah dibuat. contoh :
  - > grep di filebaru : akan mencari kata "di" pada filebaru
  - > grep -c di file baru : akan menghitung jumlah kata 'di' pada filebaru
  - > grep file* : akan mencari semua file yang berisi kata "file"
![grep](https://user-images.githubusercontent.com/90192123/135765809-7834d757-e9da-4625-897a-a02b2dca0165.png)

> __Sort__ untuk mengurutkan data, baik itu secara ascending atau descending. berikut adalah contoh penggunaan perintahnya :
  - > __sort filebaru__ : untuk mengurutkan berdasarkan ascending
  - > __sort -r filebaru__ : untuk mengurutkan berdasarkan descending
![sort](https://user-images.githubusercontent.com/90192123/135765913-3f468bef-f678-4be6-b8f4-824c83c0ca3d.png)

> __Echo__ digunakan untuk mencetak string/pesan dari hasil perintah lain. berikut adalah contoh penggunaan perintahnya :
  - > __echo "Hello World!"__
  - > __echo "ini bukan data di filebaru"__
  - > __echo "replace semua data"__
![echo](https://user-images.githubusercontent.com/90192123/135766161-796843ca-8f41-428d-9afa-115d8589a186.png)

> __Monitoring__ merupakan aktivitas untuk melihat kinerja sistem secara realtime. berikut ini adalah beberapa perintah yang dapat kita gunakan untuk memonitoring sebuah server.
  - > __htop__
  - > __lsof__
  - > __ps__
__*htop*__ merupakan perintah untuk memonitoring sistem, kita dapat melihat penggunaan memory, cpu, swap. berikut adalah contoh penggunaan perintahnya :
  - > __*htop*__

jika pada sever belum terinstall htop, maka dapat menggunakan perintah berikut :
- __*sudo apt install htop -y*__
- __*htop*__
![htop](https://user-images.githubusercontent.com/90192123/135766341-d9387d0c-cf27-4716-9d5a-ea2a8dfc5353.png)

> __lsof__ merupakan singkatan *list open files*, berfungsi untuk melihat seluruh file yang terbuka berdasarkan proses aktif yang berjalan di sistem. berikut ini adalah contoh penggunaan perintahnya :
  - > __lsof__ : untuk menampilkan seluruh proses
  - > __lsof -u muhammadnurilham__ : menampilkan proses yang dilakukan user "muhammadnurilham"
  - > __lsof -i:80__ : untuk menampilkan proses yang menggunakan port 80
![lsof](https://user-images.githubusercontent.com/90192123/135766531-f1e06092-5253-43f4-983a-e8d96316c129.png)
![lsof -u](https://user-images.githubusercontent.com/90192123/135766714-fa3c96cc-0ec8-41f8-a444-3ceb90a4e9e3.png) 

> __Ps__ merupakan singkatan dari *proses status*, untuk mengetahui daftar proses yang berjalan pada sistem. berikut contoh dari penggunaan perintahnya :
  - > __ps-f-u muhammadnurilham__ : untuk menampilkan proses pada user "muhammadnurilham"
  - > __ps -aux__ : untuk menampilkan seluruh proses secara lengkap
![ps](https://user-images.githubusercontent.com/90192123/135766840-1b251685-4c37-4fe5-ae92-445c49e47fde.png)

### Network Firewall
__Network Firewall__ merupakan perintah yang dapat digunakan untuk mengamankan sebuah server. perintah yang dapat kita gunakan adalah :
  - > __iptables/ufw__

__Iptables__ merupakan sebuah modul di linux yang memberikan dukungan langsung terhadap kernel untuk keamanan sistem serta beberapa keperluan jaringan. Iptables juga dapat digunakan untuk melakukan seleksi terhadap paket-paket yang datang baik itu output, input berdasarkan IP, port dan sebagainya.
__UFW (Uncomplicated firewall)__ salah satu fitur frontend iptables pada linux untuk mengkonfigurasi sistem firewall.

jika sistem tidak memiliki *ufw*, jalankan perintah berikut :
  - > __sudo apt install ufw -y__
  - > __sudo ufw deafult deny incoming__ : memblokir semua akses yang masuk
  - > __sudo ufw default allow outgoing__ : membuka semua akses yang keluar
  - > __sudo ufw app list__ : untuk menampilkan aplikasi yang didukung oleh ufw pada server
  - > __sudo ufw "Nginx Full"__ : untuk mengizinkan akses dari luar ke dalam untuk aplikasi nginx
![nginx](https://user-images.githubusercontent.com/90192123/135767586-8c323815-47c1-4575-b479-ff37cfd6d183.png)

  - > __sudo ufw allow 22__ : membuka akses untuk port 22
  - > __sudo ufw allow 22/tcp__ : membuka akses untuk port 22 dengan koneksi tcp
  - > __sudo ufw allow 22/udp__ : membuka akses untuk port 22 dengan koneksi udp
  - > __sudo ufw deny 80__ : memblokir semua akses ke port 80
  - > __sudo ufw delete deny 80__ : menghapus konfigurasi, haru sama dengan perintah yang ingin dihapus

### System Performance
selain menggunakan tools monitoring yang kita pelajari sebelumnya, kita juga dapat memantau kinerja server menggunakan beberapa tools lain:
  - *vmstat*
  - *iostat*
  - *sar*
  - *nmon*

__Vmstat__ merupakan tool untuk menampilkan penggunaan memory dan swap. tapi juga akan memberikan informasi soal proses, interrupt system, kecepatan I/O dan statistik CPU secara realtime.
sebelum melanjutkan , jalankan perintah berikut : 
  - > __sudo apt install sysstat -y__
untuk menjalankan : __vmstat__
jika hasilnya masih sulit dibaca, maka dapat menjalankan perintah berikut :
  - > __vmstat -sSM__
![vmstat](https://user-images.githubusercontent.com/90192123/135768021-01031b63-f7b2-43cf-8b77-f1ba3e20497b.png)

agar dapat menampilkan data terbaru dapat menggunakan perintah berikut :
- > __vmstat 5 10__ : menampilkan data per 5 detik sebanyak 10 kali

__iostat__ digunakan untuk memantau input dan output sistem, melihat berapa lama perangkat aktif yang kaitannya dengan kecepatan I/O. __*Iostat*__ merupakan bagian dari aplikasi sysstat yang sudah di install pada materi vmstat. cukup jalankan perintah berikut :
  - > __iostat__
![iostat](https://user-images.githubusercontent.com/90192123/135768162-8a77d2c0-7333-4762-b5f4-9f1ae4e5a091.png)

untuk memonitoring dengan data yang lebih lengkap, dapat menggunakan nmon untuk instalasi dapat menjalankan perintah berikut :
  - > __sudo apt install nmon -y__
kemudian jalankan : __nmon__
![nmon](https://user-images.githubusercontent.com/90192123/135768356-60e90fce-9d50-43e6-83c5-8c73f260ffb1.png)

pada halaman awal, 

tekan __c__ : untuk menampilkan CPU

tekan __d__ : untuk menampilkan disks

![cpu](https://user-images.githubusercontent.com/90192123/135768385-6327958d-c143-4a1f-a026-4db7bf0c153d.png)
![disk](https://user-images.githubusercontent.com/90192123/135768392-95b24300-ddbd-43a1-8d79-3cafae3948b0.png)

## CMS Manajer
__CMS Manajer__ memiliki fungsi utama untuk dapat mengelola dan mengembangkan konten secara lebih fleksibel, mudah, dan cepat. sebagai sebuah platform, __CMS__ juga memberikan berbagai kemudahan bagi pengguna untuk dapat mengeksplorasi lebih dalam mengenai konten yang dimuat dalam website.
fungsi __CMS__ selanjutnya adalah mampu untuk menjaga kualitas dari desain dan tampilan website. hal yang sangat diperhatikan agar setiap pengunjung website mendapatkan pengalaman dari sisi tampilan dan penggunaannya. 
fungsi __CMS__ terakhir adalah memiliki fitur untuk hak akses sebagai adminitrator yang mengatur proses pengelolaan dan manajemen konten dalam website.

__Manfaat CMS Manajer__ 
  - > __Membantu proses bisnis__
  - > __Mengoptimalkan fungsi kerja website__
  - > __Memudahkan dalam manajemen konten__

__Kesimpulan__ 
  - > __CMS__ adalah perangkat lunak yang digunakan untuk membantu proses manajemen konten dalam situs web
  - > Macam-macam __CMS__ populer yang sering digunakan adalah WordPress, Joomla, dan Drupal
  - > Manfaat __CMS__ adalah mengembangkan website dalam mengoptimalkan website dari segi konten lebih maksimal dari segi kualitas dan tampilan
