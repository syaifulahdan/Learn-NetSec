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
   
   To see which processes are running on the server and how much CPU is being used: as you can see, 50% of the CPU is currently in use, specifically by <b>systemd</b> and <b>sshd</b>. However, notice that firewalld is missing from this list; this is because we haven't started the firewall yet. To start the firewall, you can use the <b>`firewall start`</b> command.
    
<pre>
   learnnetsec@learnnetsec_server:/bin/# <b>top </b>
</pre>

   ![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/topcommand.png)

Run the firewall, then view all CPU processes using the **top** command. As shown in the example below, `firewalld` is now running and currently utilizing **70% of the CPU**, distributed as follows: **`systemd` (35%)**, **`sshd` (15%)**, and **`firewalld` (20%)**.

   ![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/firwallstart.png)


<pre>
   learnnetsec@learnnetsec_server:/bin/# <b>firewall start </b>
</pre>

   3 Installing more software
   
   installing more sorftware on your server juga means **more potentials security holes**
   - Apakah Maild diperlukan agar dapat mengirim email ?
<pre>
   learnnetsec@learnnetsec_server:/bin/# <b>apt install maild </b> 
</pre>
  
   ![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/installmaild.png)

 lalu jalankan dengan perintah <b>maild start</b>
 
<pre>
   learnnetsec@learnnetsec_server:/bin/# <b>maild start </b>
</pre>
    
   ![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/mailstart.png)

   <b>Back</b>  [[....]](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/Hack_Sim.md)





