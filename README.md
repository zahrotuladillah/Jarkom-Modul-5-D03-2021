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
```
Keterangan : 	
	Doriki adalah DNS Server
	Jipangu adalah DHCP Server
	Maingate dan Jorge adalah Web Server
	Jumlah Host pada Blueno adalah 100 host
	Jumlah Host pada Cipher adalah 700 host
	Jumlah Host pada Elena adalah 300 host
	Jumlah Host pada Fukurou adalah 200 host
```
### Penjelasan Jawaban
![image](https://user-images.githubusercontent.com/74708771/145672341-10fe2b42-58eb-424f-9ddd-8993bdaf6212.png)

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
Install `apt-get install isc-dhcp-relay -y` pada Water7, Foosha, dan Guanhao lalu install `apt-get install isc-dhcp-server` pada Jipangu

Lalu, tambahkan pengaturan pada file `/etc/default/isc-dhcp-relay` dan edit server dengan mengarahkan dchp-relay menuju Jipangu `192.193.0.3`
```
SERVERS="192.193.0.3"
```

Pada Jipangu edit file `/etc/default/isc-dhcp-server` dengan menambahkan
```
INTERFACES="eth0"
```

Selanjutnya, isikan pengaturan pada `/etc/dhcp/dhcpd.conf` menjadi seperti berikut
```
subnet 192.186.1.0 netmask 255.255.255.0 {
    range 192.186.1.2 192.186.1.254;
    option routers 192.186.1.1;
    option broadcast-address 192.186.1.255;
    option domain-name-servers 192.186.0.18;
    default-lease-time 600;
    max-lease-time 7200;
}
subnet 192.186.0.128 netmask 255.255.255.128 {
    range 192.186.0.130 192.186.0.254;
    option routers 192.186.0.129;
    option broadcast-address 192.186.0.255;
    option domain-name-servers 192.186.0.18;
    default-lease-time 600;
    max-lease-time 7200;
}
subnet 192.186.4.0 netmask 255.255.252.0 {
    range 192.186.4.2 192.186.4.254;
    option routers 192.186.4.1;
    option broadcast-address 192.186.4.255;
    option domain-name-servers 192.186.0.18;
    default-lease-time 600;
    max-lease-time 7200;
}
subnet 192.186.2.0 netmask 255.255.254.0 {
    range 192.186.2.2 192.186.2.254;
    option routers 192.186.2.1;
    option broadcast-address 192.186.2.255;
    option domain-name-servers 192.186.0.18;
    default-lease-time 600;
    max-lease-time 7200;
}
subnet 192.186.0.16 netmask 255.255.255.248{
}
```

Lalu, ubah file `/etc/network/interfaces` pada Blueno, Cipher, Fukurou, dan Elena menjadi
```
auto eth0
iface eth0 inet dhcp
```

## 1
### Soal
Agar topologi yang kalian buat dapat mengakses keluar, kalian diminta untuk mengkonfigurasi Foosha menggunakan iptables, tetapi Luffy tidak ingin menggunakan MASQUERADE.
### Penjelasan Jawaban
Jalankan command pada Foosha dengan command berikut:
```
ipEth0=`hostname -I | awk '{print $1}'`

iptables -t nat -A POSTROUTING -o eth0 -j SNAT --to-source $ipEth0
```

Hasil ping dari Water7:
![image](https://user-images.githubusercontent.com/74708771/145672712-4f47993a-3016-4ca7-ad3b-2163015b998f.png)


## 2
### Soal
Kalian diminta untuk mendrop semua akses HTTP dari luar Topologi kalian pada server yang merupakan DHCP Server dan DNS Server demi menjaga keamanan.
### Penjelasan Jawaban
Jalankan command pada Jipangu dan Doriki dengan command:
```
iptables -A FORWARD -p tcp --dport 80 -d 192.193.0.0/29 -i eth0 -j DROP
```
Testing:
Pada Jipangu dan Doriki install netcat 	`apt-get install netcat` lalu jalankan `nc -l -p 80`
Lalu, pada Foosha jalankan `nmap -p 80 192.193.0.2` mengarah ke Doriki dan `nmap -p 80 192.193.0.3` mengarah ke Jipangu.
Ke Doriki:
![image](https://user-images.githubusercontent.com/74708771/145672883-bfc0dfe5-90a0-4cf3-bcee-e5bb640c6061.png)
Ke Jipangu:
![image](https://user-images.githubusercontent.com/74708771/145672917-5796cc8b-ffa1-4cbd-84d8-5065a740fefb.png)


## 3
### Soal
Karena kelompok kalian maksimal terdiri dari 3 orang. Luffy meminta kalian untuk membatasi DHCP dan DNS Server hanya boleh menerima maksimal 3 koneksi ICMP secara bersamaan menggunakan iptables, selebihnya didrop.
### Penjelasan Jawaban
Di Doriki(DNS) dan Jipangu(DHCP), ditambahkan rule seperti berikut
```
iptables -A INPUT -p icmp -m connlimit --connlimit-above 3 --connlimit-mask 0 -j DROP
```
Command tersebut akan memfilter INPUT yang memiliki protokol icmp jika koneksinya lebih dari 3 dari subnet manapun dengan bantuan module `connlimit`.

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
Command tersebut akan memfilter INPUT yang berasal dari subnet 192.193.0.128/25(Blueno) dan 192.193.4.0/22(Cipher) dengan bantuan module `time`. Untuk koneksi yang memiliki waktu antara 07:00 sampai 15:00 di hari Senin, Selasa, Rabu, dan Kamis akan di-ACCEPT sedangkan koneksi lain yang tidak sesuai rule tadi akan di-REJECT.

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
**Selain itu di reject**
### Penjelasan Jawaban
Di Doriki kembali ditambahkan rule seperti berikut
```
iptables -A INPUT -s 192.193.2.0/23 -m time --timestart 07:00 --timestop 15:00 -j REJECT
iptables -A INPUT -s 192.193.1.0/24 -m time --timestart 07:00 --timestop 15:00 -j REJECT
```
Command tersebut akan memfilter INPUT yang berasal dari subnet 192.193.2.0/23(Elena) dan 192.193.1.0/24(Fukurou) dengan bantuan module `time`. Untuk koneksi yang memiliki waktu antara 07:00 sampai 15:00 akan di-REJECT sedangkan sisanya akan dilanjutkan akan di-ACCEPT.

Uji coba dari Elena:<br/>
**Hari Sabtu jam 08:00**<br/>
![image](https://user-images.githubusercontent.com/29938033/145665735-ec2ac004-d2f1-4662-a006-7c90e2447618.png)

**Hari Sabtu jam 06:00**<br/>
![image](https://user-images.githubusercontent.com/29938033/145665746-30e17bb9-9d14-426a-8953-5ce627f3521b.png)

Uji coba dari Fukurou:<br/>
**Hari Sabtu jam 08:00**<br/>
![image](https://user-images.githubusercontent.com/29938033/145665762-9f5cb17e-4525-4a34-926b-e930bd644435.png)

**Hari Sabtu jam 06:00**<br/>
![image](https://user-images.githubusercontent.com/29938033/145665775-a79038b3-2dc2-42cf-8147-c08e0501194a.png)

## 6
### Soal
Karena kita memiliki 2 Web Server, Luffy ingin Guanhao disetting sehingga setiap request dari client yang mengakses DNS Server akan didistribusikan secara bergantian pada Jorge dan Maingate
### Penjelasan Jawaban
Di Jorge dan Maingate, install webserver dengan command `apt-get update && apt-get install apache2 -y` dan kemudian ubah isi `/var/www/html/index.html` di Jorge:
```html
<!DOCTYPE html>
<head>
    <title>Jorge</title>
</head>
<body>
    <h1>Mengakses Jorge</h1>
</body>
</html>
```
sedangkan di Maingate, isi `/var/www/html/index.html` diubah menjadi:
```html
<!DOCTYPE html>
<head>
    <title>Maingate</title>
</head>
<body>
    <h1>Mengakses Maingate</h1>
</body>
</html>
```
file `index.html` diubah agar mudah membedakan server yang diakses ketika testing nanti. Server lalu diaktifkan dengan menjalankan `service apache2 start`

Kemudian di Guanhao, tambahkan rule iptables berikut:
```
iptables -A PREROUTING -t nat -p tcp -d 192.193.0.2 --dport 80 -m statistic --mode nth --every 2 --packet 0 -j DNAT --to-destination 192.193.0.10:80
iptables -A PREROUTING -t nat -p tcp -d 192.193.0.2 --dport 80 -j DNAT --to-destination 192.193.0.11:80
```
Rule tersebut akan merubah destination paket dengan protokol tcp, tujuan 192.193.0.2 (IP Doriki), di port 80 ke IP Maingate atau Jorge dengan bantuan modul `statistic`. Mode nth berarti akan menggunakan algorith round robin. Parameter every 2 dan packet 0 akan berarti untuk setiap 2 paket dari paket 0 akan diarahkan ke `192.193.0.10:80`. Sedangkan sisanya akan diarahkan ke `192.193.0.11:80`.

Untuk testing, install wget di Elena atau Fukurou dengan command `apt-get install wget -y` kemudian jalankan `wget -qO- 192.193.0.2` beberapa kali<br/>
![image](https://user-images.githubusercontent.com/29938033/145666285-1c662d98-20f2-4305-823e-c32972bccef3.png)


**Luffy berterima kasih pada kalian karena telah membantunya. Luffy juga mengingatkan agar semua aturan iptables harus disimpan pada sistem atau paling tidak kalian menyediakan script sebagai backup.**
