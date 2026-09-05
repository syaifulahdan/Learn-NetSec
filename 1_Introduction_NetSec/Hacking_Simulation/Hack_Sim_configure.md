   ### <b>Configure Server</b>

   Sebelum melakukan peretasan, sebaiknya server diamankan terlebih dahulu, salah satu tindakan untuk pengamanan server adalah menginsal firewall. Jika anda ingin menginstall paket, memperbarui paket, atau menghapus paket, anda perlu menggunakan  pengelola paket. pada sistem dalam game  ini anda dapat menggunakan <b>'apt'</b>, jika anda tidak mengetahui apa itu, anda dapat mengetikan <b>'man apt'.</b>
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
Jalankan Firewall

<pre>
   learnnetsec@learnnetsec_server:/bin/# <b>firewall start </b>
</pre>

   <b>Back</b>  [[....]](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/Hack_Sim.md)





