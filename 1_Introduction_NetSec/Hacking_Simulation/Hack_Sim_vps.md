
   ### <b>Creating a Virtual Private Server (VPS)</b>

   When entering the game for the first time, you need to create your own server; VPS stands for Virtual Private Server. If you run the <b>'man'</b> command, you will see that 'VPS' accepts various parameters, but the one used most frequently is for creating a new VPS. The <b>'vps create'</b> command is used to create your own server.

   ![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/manvps.png)

1. Create VPS   
 <pre>
    <b>learnnetsec@starterhub:/#</b> vps create
       Creating server...
</pre>

   ![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/vps_create.png)


<pre>

      VPS reboot initiated... [OK]
      sshd config config reset... [OK]
      sshd restarted... [OK]
 
      Server is ready for remote connections.
 
      VPS creation successful.
      IP address: 840d:74cd:dab6:9684:357e:f5b6:2a5b:6925
      Password: nG6R5ZQF
      To connect, use: vps connect

      learnnetsec@starterhub:/#
 </pre>


  perintah vps create membuat server dengan alamat IP dan kata sandi, jadi kita dapat terhubung dengan server VPS.  anda dapat menggunakan perintah <b>'vps'</b> untuk dapat terhubung ke server anda dengan menambahkan perintah <b>'vps connect'</b>.  dan setiap kali anda masuk ke dalam game dengan perintah <b>'su'</b>, anda perlu melakukan koneksi ke server dengan  perintah <b>'vps connect'</b> ke server anda sendiri

  Jadi ketika anda telah terhubung ke server maka akun anda bukan lagi <b>demo@starterHub</b> atau yang saya gunakan saat ini adalah <b>learnnetsec@starterhub</b>. sehingga akan menjadi demo@demo_server.
   
    


   <b>Back</b>  [[....]](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/Hack_Sim.md)




