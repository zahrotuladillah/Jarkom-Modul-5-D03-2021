# Jarkom-Modul-5-D03-2021

- Zahrotul Adillah (05111940000139)
- Muhammad Nur Abdurrauf (05111940000140)
- Aflah Hilmy (05111940000177)

## Daftar Isi

- [A](#a)
- [B](#b)
- [C](#c)
- [D](#d)
- [1](#1)
- [2](#2)
- [3](#3)
- [4](#4)
- [5](#5)
- [6](#6)

Setelah kalian mempelajari semua modul yang telah diberikan, Luffy ingin meminta bantuan untuk terakhir kalinya kepada kalian. Dan kalian dengan senang hati mau membantu Luffy.
## A 
### Soal
Tugas pertama kalian yaitu membuat topologi jaringan sesuai dengan rancangan yang diberikan Luffy dibawah ini:
![image](https://user-images.githubusercontent.com/72771774/145141897-9b37aac8-a71b-4491-9287-9f831f63a50b.png)
```Keterangan : 	
    Doriki adalah DNS Server
		Jipangu adalah DHCP Server
		Maingate dan Jorge adalah Web Server
		Jumlah Host pada Blueno adalah 100 host
		Jumlah Host pada Cipher adalah 700 host
		Jumlah Host pada Elena adalah 300 host
		Jumlah Host pada Fukurou adalah 200 host
```
### Penjelasan Jawaban


## B
### Soal
Karena kalian telah belajar subnetting dan routing, Luffy ingin meminta kalian untuk membuat topologi tersebut menggunakan teknik CIDR atau VLSM. setelah melakukan subnetting,
### Penjelasan Jawaban
Menentukan jumlah ip yang diperlukan di setiap subnet dan netmasknya menggunakan teknik VLSM
|Subnet|Host|Mask|
|------|----|----|
|A1    |3   |/29 |
|A2    |101 |/25 |
|A3    |701 |/22 |
|A4    |2   |/30 |
|A5    |2   |/30 |
|A6    |301 |/23 |
|A7    |201 |/24 |
|A8    |3   |/29 |
|Total |1314|/21 |

Dari tabel di atas, dapat dilihat bahwa total IP adalah 1314, sehingga digunakan netmask /21.
![image](https://user-images.githubusercontent.com/72771774/145614835-bddf88c9-80ed-4732-94ce-e0841864e8aa.png)
<br>
Dari tree tersebut, dapat ditemukan Network ID, Netmask, dan Broadcast ID seperti tabel berikut :
<table>
<tbody>
  <tr>
    <td rowspan="3">A1</td>
    <td>Network ID</td>
    <td>192.193.0.0</td>
  </tr>
  <tr>
    <td>Netmask</td>
    <td>255.255.255.248</td>
  </tr>
  <tr>
    <td>Broadcast Address</td>
    <td>192.193.0.7</td>
  </tr>
  <tr>
    <td rowspan="3">A2</td>
    <td>Network ID</td>
    <td>192.193.0.128</td>
  </tr>
  <tr>
    <td>Netmask</td>
    <td>255.255.255.128</td>
  </tr>
  <tr>
    <td>Broadcast Address</td>
    <td>192.193.0.255</td>
  </tr>
  <tr>
    <td rowspan="3">A3</td>
    <td>Network ID</td>
    <td>192.193.4.0</td>
  </tr>
  <tr>
    <td>Netmask</td>
    <td>255.255.252.0</td>
  </tr>
  <tr>
    <td>Broadcast Address</td>
    <td>192.193.7.255</td>
  </tr>
  <tr>
    <td rowspan="3">A4 </td>
    <td>Network ID</td>
    <td>192.193.0.16</td>
  </tr>
  <tr>
    <td>Netmask</td>
    <td>255.255.255.252</td>
  </tr>
  <tr>
    <td>Broadcast Address</td>
    <td>192.193.0.19</td>
  </tr>
  <tr>
    <td rowspan="3">A5</td>
    <td>Network ID</td>
    <td>192.193.0.20</td>
  </tr>
  <tr>
    <td>Netmask</td>
    <td>255.255.255.252</td>
  </tr>
  <tr>
    <td>Broadcast Address</td>
    <td>192.193.0.23</td>
  </tr>
  <tr>
    <td rowspan="3">A6</td>
    <td>Network ID</td>
    <td>192.193.2.0</td>
  </tr>
  <tr>
    <td>Netmask</td>
    <td>255.255.254.0</td>
  </tr>
  <tr>
    <td>Broadcast Address</td>
    <td>192.193.3.255</td>
  </tr>
  <tr>
    <td rowspan="3">A7</td>
    <td>Network ID</td>
    <td>192.193.1.0</td>
  </tr>
  <tr>
    <td>Netmask</td>
    <td>255.255.255.0</td>
  </tr>
  <tr>
    <td>Broadcast Address</td>
    <td>192.193.1.255</td>
  </tr>
  <tr>
    <td rowspan="3">A8</td>
    <td>Network ID</td>
    <td>192.193.0.8</td>
  </tr>
  <tr>
    <td>Netmask</td>
    <td>255.255.255.248</td>
  </tr>
  <tr>
    <td>Broadcast Address</td>
    <td>192.193.0.15</td>
  </tr>
</tbody>
</table>

## C
### Soal
Kalian juga diharuskan melakukan Routing agar setiap perangkat pada jaringan tersebut dapat terhubung.
### Penjelasan Jawaban
|Router|Subnet|Network ID|Netmask|Next Hop|
|------|------|----------|-------|--------|
|Foosha|A1    |192.193.0.0|255.255.255.248|192.193.0.18|
|Foosha|A2    |192.193.0.128|255.255.255.128|192.193.0.18|
|Foosha|A3    |192.193.4.0|255.255.252.0|192.193.0.18|
|Foosha|A6    |192.193.2.0|255.255.254.0|192.193.0.22|
|Foosha|A7    |192.193.1.0|255.255.255.0|192.193.0.22|
|Foosha|A8    |192.193.0.8|255.255.255.248|192.193.0.22|
|Water7|Default|0.0.0.0|0.0.0.0|192.193.0.17|
|Guanhao|Default|0.0.0.0|0.0.0.0|192.193.0.21|

## D
### Soal
Tugas berikutnya adalah memberikan ip pada subnet Blueno, Cipher, Fukurou, dan Elena secara dinamis menggunakan bantuan DHCP server. Kemudian kalian ingat bahwa kalian harus setting DHCP Relay pada router yang menghubungkannya.
### Penjelasan Jawaban


## 1
### Soal
Agar topologi yang kalian buat dapat mengakses keluar, kalian diminta untuk mengkonfigurasi Foosha menggunakan iptables, tetapi Luffy tidak ingin menggunakan MASQUERADE.
### Penjelasan Jawaban


## 2
### Soal
Kalian diminta untuk mendrop semua akses HTTP dari luar Topologi kalian pada server yang merupakan DHCP Server dan DNS Server demi menjaga keamanan.
### Penjelasan Jawaban


## 3
### Soal
Karena kelompok kalian maksimal terdiri dari 3 orang. Luffy meminta kalian untuk membatasi DHCP dan DNS Server hanya boleh menerima maksimal 3 koneksi ICMP secara bersamaan menggunakan iptables, selebihnya didrop.
### Penjelasan Jawaban
Di Doriki(DNS) dan Jipangu(DHCP), ditambahkan rule seperti berikut
```
iptables -A INPUT -p icmp -m connlimit --connlimit-above 3 --connlimit-mask 0 -j DROP
```
Command tersebut akan memfilter INPUT yang memiliki protokol icmp jika koneksinya lebih dari 3 dari subnet manapun dengan bantuan module connlimit.

Uji coba untuk Doriki:<br/>
**Host 1**<br/>
![image](https://user-images.githubusercontent.com/29938033/145664975-ff239967-38af-4b5d-a712-37288b5d89df.png)

**Host 2**<br/>
![image](https://user-images.githubusercontent.com/29938033/145665003-a726204e-3ff3-4027-b177-6bfee3ff20ff.png)

**Host 3**<br/>
![image](https://user-images.githubusercontent.com/29938033/145665011-fd3f6962-0698-4dba-aa9a-379dc29ca6bd.png)

**Host 4**<br/>
![image](https://user-images.githubusercontent.com/29938033/145665036-1a7474ee-e931-4898-a004-4b38bd2cd7ee.png)

Uji coba untuk Jipangu:<br/>
**Host 1**<br/>
![image](https://user-images.githubusercontent.com/29938033/145665058-c4d2effd-69a8-4c89-a69c-628ff70d592e.png)

**Host 2**<br/>
![image](https://user-images.githubusercontent.com/29938033/145665064-42ce388c-b3f7-4a28-8ebe-df7e24af6cd2.png)

**Host 3**<br/>
![image](https://user-images.githubusercontent.com/29938033/145665083-9cabba7b-0e94-4d68-83b0-8e2cf9a3ec11.png)

**Host 4**<br/>
![image](https://user-images.githubusercontent.com/29938033/145665121-8bd2778c-fdd3-4d82-9ef9-4cb2b1ff324b.png)


## 4
### Soal
**Kemudian kalian diminta untuk membatasi akses ke Doriki yang berasal dari subnet Blueno, Cipher, Elena dan Fukuro dengan beraturan sebagai berikut**
Akses dari subnet Blueno dan Cipher hanya diperbolehkan pada pukul 07.00 - 15.00 pada hari Senin sampai Kamis.
### Penjelasan Jawaban
Di Doriki ditambahkan rule seperti berikut
```
iptables -A INPUT -s 192.193.0.128/25 -m time --timestart 07:00 --timestop 15:00 --weekdays Mon,Tue,Wed,Thu -j ACCEPT
iptables -A INPUT -s 192.193.4.0/22 -m time --timestart 07:00 --timestop 15:00 --weekdays Mon,Tue,Wed,Thu -j ACCEPT
iptables -A INPUT -s 192.193.0.128/25 -j REJECT
iptables -A INPUT -s 192.193.4.0/22 -j REJECT
```
Command tersebut akan memfilter INPUT yang berasal dari subnet 192.193.0.128/25(Blueno) dan 192.193.4.0/22(Cipher) dengan bantuan module time. Untuk koneksi yang memiliki waktu antara 07:00 sampai 15:00 di hari Senin, Selasa, Rabu, dan Kamis akan di-ACCEPT sedangkan koneksi lain yang tidak sesuai rule tadi akan di-REJECT.

Uji coba dari Blueno:<br/>
**Hari Sabtu jam 08:00**<br/>
![image](https://user-images.githubusercontent.com/29938033/145665366-3e503604-f11e-48d4-9c09-6639a1f6a9d4.png)

**Hari Kamis jam 06:00**<br/>
![image](https://user-images.githubusercontent.com/29938033/145665399-913f925b-7e57-4191-8dda-a8ab6740cf9e.png)

**Hari Kamis jam 08:00**<br/>
![image](https://user-images.githubusercontent.com/29938033/145665406-82972c81-dbc6-4f17-bab9-acff2051f7e2.png)

Uji coba dari Cipher:<br/>
**Hari Sabtu jam 08:00**<br/>
![image](https://user-images.githubusercontent.com/29938033/145665446-18f230b3-00eb-47d2-bed6-6d36a87dc8d0.png)

**Hari Kamis jam 06:00**<br/>
![image](https://user-images.githubusercontent.com/29938033/145665451-5114958d-6408-40f3-b203-470e83989517.png)

**Hari Kamis jam 08:00**<br/>
![image](https://user-images.githubusercontent.com/29938033/145665455-ed60be6f-d11b-4b81-ae48-5fd99750835e.png)


## 5
### Soal
Akses dari subnet Elena dan Fukuro hanya diperbolehkan pada pukul 15.01 hingga pukul 06.59 setiap harinya.
### Penjelasan Jawaban

**Selain itu di reject**
## 6
### Soal
Karena kita memiliki 2 Web Server, Luffy ingin Guanhao disetting sehingga setiap request dari client yang mengakses DNS Server akan didistribusikan secara bergantian pada Jorge dan Maingate
### Penjelasan Jawaban


**Luffy berterima kasih pada kalian karena telah membantunya. Luffy juga mengingatkan agar semua aturan iptables harus disimpan pada sistem atau paling tidak kalian menyediakan script sebagai backup.**
