
   ### <b>Commands that must be learned</b>

   Beberapa perintah perlu benar-benar anda pelajari, salah satunya adalah perintah <b>'ls'</b> yang berfungsi menampilkan file-file di folder saat ini. jika folder saat ini dadalah folder root, atau tanda /. maka perintah ls akan menampilkan file-file  yang ada didalam folder root.

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


The `vps create` command sets up a server with an IP address and password, allowing you to connect to the VPS. You can connect to your server by using the `vps` command followed by `vps connect`. Additionally, every time you enter the game using the `su` command, you must connect to your server using `vps connect`.

So, once you are connected to the server, your account will no longer be <b>demo@starterHub</b>—or, in my current case, <b>learnnetsec@starterhub</b>—but will instead become <b>demo@demo_server</b>.
   
    


   <b>Back</b>  [[....]](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/Hack_Sim.md)





