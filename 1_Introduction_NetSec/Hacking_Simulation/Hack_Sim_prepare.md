### <b>1.4.7. Preparation for the First Hack</b>

**1. Periksa email**

Jika sekarang kita memeriksa email, maka anda akan melihat bahwa anda memiliki satu pesan yang belum dibaca, dan seperti yang anda ingat, email disimpan didalam folder **mail** pada folder **var** : **/var/mail** jadi kita dapat melihat email pada direktori mail dengan menggunakan perintah

```ruby
   learnnetsec@learnnetsec_server:/etc/apt/# ls /var/mail
```

atau masuk ke direktori /var/mail dengan perintah :
```ruby
   learnnetsec@learnnetsec_server:/etc/apt/# <b>cd /var/mail</b>
   learnnetsec@learnnetsec_server:/var/mail/# <b>ls</b>

```
 
![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/cekmail.png)

Jika pada percobaan ini terdapat 7 email baru yang belum terbaca, karena saya melakukan pengiriman email kepada LordNikon sebanyak 7x, untuk membaca file teks dapat menggunakan perintah V atau view, jadi **ketik V kemudian [nama file]**

```python
RWX OWNER        LAST MODIFIED       NAME                           
rw- LordNikon    2026-09-06 09:28:26 eXt3
rw- LordNikon    2026-09-06 09:27:20 J2AR
rw- LordNikon    2026-09-06 09:26:53 LDZd
rw- LordNikon    2026-09-06 09:26:45 hPJW
rw- LordNikon    2026-09-06 09:26:08 fJEx
rw- LordNikon    2026-09-06 07:48:57 VheR
rw- LordNikon    2026-09-06 07:39:11 uEHm
```
   

```python
learnnetsec@learnnetsec_server:/etc/apt/# vi uEHm
FROM: lordnikon
DATE: 2026-09-06 07:39:11
BODY:
You are missing a vital tool on your server called nmap. This tool, and a lot of other hacking tools are available on a secret APT-server.

Add the following IP address to a new line in your /etc/apt/sources.list: a976:62cf:8029:ed4b:1d85:c8ed:a746:790f

After adding that IP you can install nmap by typing: apt-get install nmap


Before you can do jobs for me, you need a bitcoin wallet. Create one on your server by typing: btc create   

```

![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/viewemail.png)

**2. Buka email**

- Isi email dengan nama **uEHm** adalah email yang dikirim Lord Nikon kepada kita dan isinya mengatakan anda kehilangan alat penting di server anda, yaitu **nmap** dan ada banyak alat peretasan lainnya yang tersedia di  
server aplikasi rahasia. 
- Tambahkan alamat  IP berikut ke baris baru di file ini, jadi mari kita salin alamat IP ini ke dalam file **/etc/apt/sources.list** dengan memilihnya. setelah menambahkan ip tersebut, anda dapat menginstal nmap dengan mengetikan  **get install nmap** atau **apt-install nmap**
- Email ini juga mengatakan bahwa, sebelum anda dapat melakukan pekerjaan untuk saya, anda memerlukan Dompet Bitcoin. Buat satu di server anda menggunakan perintah **btc create** , mari kita lakukan dua hal  ini dan kemudia hubungi Lord Nikon.
  

```ruby
learnnetsec@learnnetsec_server:/var/mail/# cd /etc/apt
learnnetsec@learnnetsec_server:/etc/apt/# ls
   
RWX OWNER        LAST MODIFIED       NAME                           
rw- systemd      2026-09-05 09:27:14 sources.list

learnnetsec@learnnetsec_server:/etc/apt/#
```

![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/lssourclist.png)

**3. Lihat file Sources.list**

- melihat file **sources.list** yang ada di direktori /etc/apt dengan menggunakan perintah **vi** dan file sources list berisikan alamat ip **afe2:9673:7fc4:05d6:7162:5813:ea53:83ec**

```ruby
learnnetsec@learnnetsec_server:/etc/apt/# vi sources.list

afe2:9673:7fc4:05d6:7162:5813:ea53:83ec

learnnetsec@learnnetsec_server:/etc/apt/#
```



![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/viewsourclist.png)

**4. Merubah file Sources.list**

Kemudian kita akan mengedit file sources.list menggunakan **vim**

```python
learnnetsec@learnnetsec_server:/etc/apt/# vim sources.list
```

![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/vimsourcelist.png)


**afe2:9673:7fc4:05d6:7162:5813:ea53:83ec** adalah alamat IP yang ada pada file sources.list, jika anda menekan **Enter** lalu **Ctrl+V**, **a976:62cf:8029:ed4b:1d85:c8ed:a746:790f** adalah alamat IP yang kita salin dari email ini. Kemudian tekan **Save dan Exit** untuk memperbarui file  ini.

<pre>
afe2:9673:7fc4:05d6:7162:5813:ea53:83ec
</pre>

![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/copyip.png)

**5. Lihat perubahan file Sources.list**

Periksa apakah isi file **sources list** telah diperbaruhi, menggunakan perintah **vi**
  
```ruby
learnnetsec@learnnetsec_server:/etc/apt/# vi sources.list
```

![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/cekupdatesourcelis.png)

**6 Lihat Perubahan Paket**

periksa apakah paket sudah diperbarui dengan menggunakan perintah **apt list packages** atau **apt-get list packages**
<pre>
learnnetsec@learnnetsec_server:/etc/apt/# <b>apt list packages</b>

APT-server afe2:9673:7fc4:05d6:7162:5813:ea53:83ec <b>(Daftar paket lama)</b>
    logd
    maild
    firewalld
    httpd
    sshd
    bash
    modsecurity
    wget
    sendmail
    btc-transfer
    systemd
    curl
    peboeka
 
APT-server a976:62cf:8029:ed4b:1d85:c8ed:a746:790f <b>(Daftar paket yang baru ditambahkan)</b>
    nmap
    mailxpl01t
    httpwnd
    btcr4ck
    xpresshion
    btcsrvd
    btcminerd
    hacktheplanet
 
learnnetsec@learnnetsec_server:/etc/apt/#
</pre>

![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/updatepackages.png)

**7 Install nmap**
```ruby
learnnetsec@learnnetsec_server:/etc/apt/# apt install nmap
```
![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/installnmap.png)

**8 Membuat dompet Bitcoin**

seperti yang dikatakan oleh Lord Nikon, kita harus membuat dompet Bitcoin dengan perinah **btc create** jika kita mengetikan perintah **man btc**, kita bisa melihat bahwa kia dapat membuat dompet dengan perintah **create**, menghapus dengan perintah **remove**, mendapatkan informasi tentang dompet kita, dengan perintah **info**. selanjutnya mari kita ketik **btc create**

```ruby
learnnetsec@learnnetsec_server:/etc/apt/# man btc 
```

![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/manbtc.png)

```ruby
learnnetsec@learnnetsec_server:/etc/apt/# btc create
```

![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/btccreate.png)

pada **folder btc** kita dapat melihat terdapat dua file **private key** kita hanya membutuhkan private key saat mengirim Bitcoin, tetapi kita akan melakukan peretasan, jadi kita mungkin akan mencuri beberapa Bitcoin, jadi kita membutuhkan key public. ini adalah key publik Bitcoin kita.

```ruby
learnnetsec@learnnetsec_server:/etc/apt/# cd ../btc  
learnnetsec@learnnetsec_server:/etc/btc/# ls 
```

![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/btcls.png)

Lihat Public key dengan perintah **vi**.

```ruby
learnnetsec@learnnetsec_server:/etc/apt/# vi public.key

<b>CmRdrUXvSkncHxu8zJygfhPB</b>

```

![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/vipublickey.png)

selanjunya, mari kita salin public key, 

![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/copypublickey.png)

   <b>Back</b>  [[....]](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/Hack_Sim.md)

