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
rw- LordNikon    2026-09-06 09:28:26 <b>eXt3</b>
rw- LordNikon    2026-09-06 09:27:20 <b>J2AR</b>
rw- LordNikon    2026-09-06 09:26:53 <b>LDZd</b>
rw- LordNikon    2026-09-06 09:26:45 <b>hPJW</b>
rw- LordNikon    2026-09-06 09:26:08 <b>fJEx</b>
rw- LordNikon    2026-09-06 07:48:57 <b>VheR</b>
rw- LordNikon    2026-09-06 07:39:11 <b>uEHm</b>
</pre>
   


<pre>
   learnnetsec@learnnetsec_server:/etc/apt/# <b>cd vi uEHm</b>
  

</pre>

   <b>Back</b>  [[....]](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/Hack_Sim.md)

