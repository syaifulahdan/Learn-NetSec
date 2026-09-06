
   ### <b>1.4.1. Starting HackTheGame</b>
   
1. Please visit  [[hackthegame.com]](https://hackthegame.com/) and Watch [[Video Tutorial]](https://www.youtube.com/watch?v=0-gf05-1uAc)
   ![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/hackthegame.png)

2. Registering an account  [[Registry]](https://wiki.hackthegame.com/registering-an-account-wla5tvk1ul-sgoew5bj3if3)
   - When you first open up the game you are an anonymous user on a public server called starterHub . This is reflected in the prompt of the terminal — anonymous@starterhub.
The first step is to register an account so we can log in. When using a new machine or any server, you can type the command <b>'available'</b> to see which commands are accessible during the current user session. The command we will use is <b>'useradd'</b>. If you want to learn more about a specific command, you can use the manual command—abbreviated as <b>'man'</b>—by running <b>'man useradd'</b>.
   
   ```ruby
      anonymous@starterhub:/$
   ```
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


