   ### <b>Configure Server</b>

Before attempting any hacking, it is best to secure the server first; one way to do this is by installing a firewall. If you need to install, update, or remove packages, you must use a package manager. In this game's system, you can use 'apt'; if you are unfamiliar with it, you can type <b>'man apt'</b>.
<pre>
   learnnetsec@learnnetsec_server:/# <b>man apt</b>
   Manage software packages like logd, httpd, maild. For installing packages apt relies on /etc/apt/sources.list

   Listing all available packages
   Syntax: <b>apt list packages</b>

   Installing a package to /bin
   Syntax: <b>apt install [package]</b>
   Example: apt install logd

   Removing a package from /bin
   Syntax: <b>apt remove [package]</b>
   Example: apt remove logd

   Updating a package in /bin
   Syntax: <b>apt update [package]</b>
   Example: apt update httpd

   Update all packages: apt update *
   </pre>

   1 Install Firewal

   <pre>
   learnnetsec@learnnetsec_server:/# <b>apt list packages</b>
   </pre>


   ![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/listpackage.png)
 <pre>
   learnnetsec@learnnetsec_server:/# <b>apt-get install firewalld</b>
   </pre>
   
   ![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/installfirewalld.png)
   
 
   2 Viewing processes running on the server
   
   untuk melihat proses mana yang berjalan di server dan berapa banyak CPU yang digunakan. seperti yang anda lihat, saat ini menggunakan 50% CPU, dan itu digunakan oleh <b>System D</b> dan <b>sshd</b>. tetapi seperti yang anda lihat, firewall D hilang dari daftar ini, dan itu dikarenakan  kita belum menjalankan firewal, untu kmenjalankan firewal, dapat menggunakan  perintah <b>firewall start</b>
    
<pre>
   learnnetsec@learnnetsec_server:/bin/# <b>top </b>
</pre>

   ![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/topcommand.png)

Jalankan Firewall, kemudian lihat seluruh proses di CPU dengan intruksi <b>top</b>, seperti contoh dibawah ini, firwalld sekarang telah berjalan, saat ini menggunakan 70% CPU yang terdiri dari : systemd 35, sshd 15, dan firewalld 20

   ![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/firwallstart.png)


<pre>
   learnnetsec@learnnetsec_server:/bin/# <b>firewall start </b>
</pre>


   <b>Back</b>  [[....]](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/Hack_Sim.md)





