   ### <b>1.4.5. Configure Server</b>

Before attempting any hacking, it is best to secure the server first; one way to do this is by installing a firewall. If you need to install, update, or remove packages, you must use a package manager. In this game's system, you can use 'apt'; if you are unfamiliar with it, you can type <b>'man apt'</b>.
```ruby
   learnnetsec@learnnetsec_server:/# man apt
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
   ```

   1 Install Firewal

   ```ruby
   learnnetsec@learnnetsec_server:/# apt list packages
   ```


   ![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/listpackage.png)

| Packages| Description |
| --- | --- |
| Logd | Receives log messages from applications or services, stores or forwards log messages, assists the system in recording activities or errors, and provides information for debugging and monitoring.|
| maild | A mail daemon is a program that runs in the background to handle email traffic on a system or server. Its primary functions are: 1. Receiving email from applications, users, or other servers. 2. Sending email to a destination server. 3. Relaying email to another server. 4. Storing or managing the email queue if delivery is not immediately possible. 5. Managing the delivery process using protocols such as SMTP. 6. Logging email delivery activities and errors. |
| firewalld | Managing a firewall on Linux to control network traffic entering and leaving a computer or server. The primary functions of firewalld are: 1. Blocking unauthorized connections, 2. Allowing specific connections (e.g., allowing SSH on port 22, HTTP on port 80, and HTTPS on port 443), 3. Managing network ports (e.g., Port 22 → SSH → ALLOW; Port 80 → HTTP → ALLOW; Port 23 → Telnet → BLOCK), 4. Managing network zones; Firewalld utilizes zone concepts such as public, home, work, trusted, drop, and block, 5. Modifying firewall rules without needing to restart the entire firewall. | 
| httpd | A program that runs in the background to provide web/HTTP services. In other words, httpd functions as a web server that receives requests from a browser or client and sends back pages or data in response. |   
| sshd | A program running in the background on Linux that provides secure SSH (Secure Shell) access to a server over a network. The primary functions of sshd are: 1. Accepting SSH connections, 2. Authenticating users, 3. Providing remote terminal access, 4. Securing communication, and 5. Supporting file transfers. |   
| bash | Bash (Bourne Again SHell) is a shell—a program that acts as an intermediary between the user and the Linux operating system. The functions of Bash include: 1. Accepting commands from the user, 2. Executing Linux programs or commands, 3. Running Bash scripts, 4. Managing the environment, and 5. Providing shell features. |   
| modsecurity | ModSecurity is a Web Application Firewall (WAF) used to protect web applications from attacks at the HTTP/HTTPS layer. When httpd operates as a web server, ModSecurity can be deployed as a security layer in front of the web application. The primary functions of ModSecurity are: 1. Detecting web attacks (SQL Injection, Cross-Site Scripting (XSS), Local/Remote File Inclusion, Command Injection, and various other HTTP attack patterns), 2. Blocking malicious requests, 3. Inspecting HTTP requests and responses, and 4. Logging suspicious activity. |   
| wget | wget (Web Get) is a command-line program for retrieving or downloading files from a network, primarily via HTTP, HTTPS, and FTP. The main functions of wget include: 1. downloading files from the internet or a server, 2. downloading web pages, 3. downloading files with specific names, 4. resuming interrupted downloads, 5. downloading multiple files, and 6. retrieving files from a server without a web browser. |   
| sendmail | sendmail is a Mail Transfer Agent (MTA) program that functions to send, receive, and forward email over a network, primarily using the SMTP protocol. The main functions of sendmail are: 1. Sending email, 2. Receiving email, 3. Forwarding (relaying) email, 4. Managing the mail queue, and 5. Communicating using SMTP. |   
| btc-transfer | `btc-transfer` is typically a program or command used to transfer Bitcoin (BTC) from one address or wallet to another. However, unlike `wget`, `sendmail`, or `sshd`, `btc-transfer` **is not a standard Linux command**; its exact function depends on the specific application in which it is used. |   
| systemd |systemd is an init system and service manager found in many modern Linux distributions. Its primary function is to initialize the system during boot and manage services or daemons running in the background. The main functions of systemd include: 1. Running services during Linux boot-up, 2. Starting and stopping services, 3. Checking service status, 4. Enabling services to run automatically at boot, 5. Disabling services from startup, and 6. Managing processes and dependencies. |   
| curl | curl is a command-line tool for communicating with servers over a network. It is frequently used to send or retrieve data via HTTP/HTTPS, though it also supports various other network protocols. Key functions of curl include: 1. Accessing web pages/APIs, 2. Downloading files, 3. Sending data to servers, 4. Testing connections and web services, and 5. Interacting with REST APIs. |   
| peboeka | As for `peboeka` serving as a Linux command or program name, it is not a standard, common Linux command like `curl`, `wget`, `sshd`, or `systemd`; rather, it is a specialized program or command created for the HacktheGame lab environment. |   

 ```ruby
   learnnetsec@learnnetsec_server:/# apt-get install firewalld
   ```
   
   ![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/installfirewalld.png)
   
 
   2 Viewing processes running on the server
   
   To see which processes are running on the server and how much CPU is being used: as you can see, 50% of the CPU is currently in use, specifically by <b>systemd</b> and <b>sshd</b>. However, notice that firewalld is missing from this list; this is because we haven't started the firewall yet. To start the firewall, you can use the <b>`firewall start`</b> command.
    
```ruby
   learnnetsec@learnnetsec_server:/bin/# top 
```

   ![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/topcommand.png)

Run the firewall, then view all CPU processes using the **top** command. As shown in the example below, `firewalld` is now running and currently utilizing **70% of the CPU**, distributed as follows: **`systemd` (35%)**, **`sshd` (15%)**, and **`firewalld` (20%)**.

   ![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/firwallstart.png)


```ruby
   learnnetsec@learnnetsec_server:/bin/# firewall start 
```

   3 Installing more software
   
   Installing more software on your server also means **more potential security vulnerabilities.**
   - Install  **Maild**
```ruby
   learnnetsec@learnnetsec_server:/bin/# apt install maild  
```
  
   ![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/installmaild.png)

- Install **sendmail**
```ruby
   learnnetsec@learnnetsec_server:/bin/# apt install sendmail 
```
  
   ![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/installsendmail.png)

 then run it with the command <b>maild start</b>
 
```ruby
   learnnetsec@learnnetsec_server:/bin/# maild start 
```
    
   ![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/mailstart.png)

After maild is run, it can be seen that maild creates a mail folder inside var, **/var/mail**, and that is where the email will be stored. 

- Install **logd**
```ruby
   learnnetsec@learnnetsec_server:/bin/# apt install logd  
```
  
   ![alt tag](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/hacksim_image/installlogd.png)

 then run it with the command <b>maild start</b>
 
```ruby
   learnnetsec@learnnetsec_server:/bin/# logd start 
```
    

   <b>Back</b>  [[....]](https://github.com/syaifulahdan/Learn-NetSec/blob/main/1_Introduction_NetSec/Hacking_Simulation/Hack_Sim.md)





