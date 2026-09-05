
   ### <b>Creating a Virtual Private Server (VPS)</b>

   When entering the game for the first time, you need to create your own server; VPS stands for Virtual Private Server. If you run the <b>'man'</b> command, you will see that 'VPS' accepts various parameters, but the one used most frequently is for creating a new VPS. The <b>'vps create'</b> command is used to create your own server..

   ![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/manvps.png)

1. Create VPS   
 <pre>
    <b></b>learnnetsec@starterhub:/#<b> vps create
 </pre>
 The first step is to register an account so we can log in. When using a new machine or any server, you can type the command <b>'available'</b> to see which commands are accessible during the current user session. The command we will use is <b>'useradd'</b>. If you want to learn more about a specific command, you can use the manual command—abbreviated as <b>'man'</b>—by running <b>'man useradd'</b>.
   
   <pre>
      anonymous@starterhub:/$
   </pre>
   - To register an account you must use the command <b>useradd</b> [username] [email address]. You will recieve your password on the provided email address, so make sure you have access to it during setup.
   - anonymous@starterhub:/$  useradd wikidemo wikidemo@hackthegame.com
Account created. Please check your email (*also check the spam-folder) for the password and use the su command to login.
   <pre>
   <b>anonymous@starterhub:/$</b> useradd learnnetsec learnnetsec17@gmail.com

   Account created. Please check your email (*also check the spam-folder) for the password and use the su command to login.
   Message sent!
   anonymous@starterhub:/$
   </pre>

    ![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/learnnetsec-useradd.png)


3. Login Account
   <b>anonymous@starterhub:/$</b> su [username] [password]
   <pre>
   anonymous@starterhub:/$ su learnnetsec ****
      To use your custom theme [green] use the command: refresh
      learnnetsec@starterhub:/#
   </pre>


   <b>Back</b>  [[....]](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/Hack_Sim.md)




