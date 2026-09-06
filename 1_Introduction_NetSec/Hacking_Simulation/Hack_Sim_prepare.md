### <b>1.4.7. Preparation for the First Hack</b>

Jika sekarang kita memeriksa email, maka anda akan melihat bahwa anda memiliki satu pesan yang belum dibaca, dan seperti yang anda ingat, email disimpan didalam folder **mail** pada folder **var** : **/var/mail** jadi kita dapat melihat email pada direktori mail dengan menggunakan perintah

<pre>
   learnnetsec@learnnetsec_server:/etc/apt/# <b>ls /var/mail</b>
</pre>

atau masuk ke direktori /var/mail dengan perintah :
<pre>
   learnnetsec@learnnetsec_server:/etc/apt/# <b>cd /var/mail</b>
   learnnetsec@learnnetsec_server:/var/mail/# <b>ls</b>

</pre>
 
![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/cekmail.png)

Ada 7 email baru yang belum terbaca, untuk membaca file teks dapat menggunakan perintah V atau view, jadi **ketik V kemudian [nama file]**

<pre>
RWX OWNER        LAST MODIFIED       NAME                           
rw- LordNikon    2026-09-06 09:28:26 eXt3
rw- LordNikon    2026-09-06 09:27:20 J2AR
rw- LordNikon    2026-09-06 09:26:53 LDZd
rw- LordNikon    2026-09-06 09:26:45 hPJW
rw- LordNikon    2026-09-06 09:26:08 fJEx
rw- LordNikon    2026-09-06 07:48:57 VheR
rw- LordNikon    2026-09-06 07:39:11 <b>uEHm</b>
</pre>
   

<pre>
learnnetsec@learnnetsec_server:/etc/apt/# <b>vi uEHm</b>
FROM: lordnikon
DATE: 2026-09-06 07:39:11
BODY:
You are missing a vital tool on your server called nmap. This tool, and a lot of other hacking tools are available on a secret APT-server.

Add the following IP address to a new line in your /etc/apt/sources.list: a976:62cf:8029:ed4b:1d85:c8ed:a746:790f

After adding that IP you can install nmap by typing: apt-get install nmap


Before you can do jobs for me, you need a bitcoin wallet. Create one on your server by typing: btc create   

</pre>

![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/viewemail.png)

**isi email**

- Isi email dengan nama **uEHm** adalah email yang dikirim Lord Nikon kepada kita dan isinya mengatakan anda kehilangan alat penting di server anda, yaitu **nmap** dan ada banyak alat peretasan lainnya yang tersedia di  
server aplikasi rahasia. 
- Tambahkan alamat  IP berikut ke baris baru di file ini, jadi mari kita salin alamat IP ini ke dalam file **/etc/apt/sources.list** dengan memilihnya. setelah menambahkan ip tersebut, anda dapat menginstal nmap dengan mengetikan  **get install nmap** atau **apt-install nmap**
- Email ini juga mengatakan bahwa, sebelum anda dapat melakukan pekerjaan untuk saya, anda memerlukan Dompet Bitcoin. Buat satu di server anda menggunakan perintah **btc create** , mari kita lakukan dua hal  ini dan kemudia hubungi Lord Nikon.
- 
   <b>Back</b>  [[....]](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/Hack_Sim.md)

<pre>
  learnnetsec@learnnetsec_server:/var/mail/# <b>cd /etc/apt</b>
</pre>
