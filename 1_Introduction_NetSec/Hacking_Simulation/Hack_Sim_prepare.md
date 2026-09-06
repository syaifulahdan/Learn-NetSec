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
rw- LordNikon    2026-09-06 07:39:11 uEHm
</pre>
   


<pre>
   learnnetsec@learnnetsec_server:/etc/apt/# <b>cd vi uEHm</b>
  

</pre>

   <b>Back</b>  [[....]](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/Hack_Sim.md)

