honestly I'm cheap and bad at enum so I ran a vuln scan like a noob

┌──(kali㉿kali)-[~]
└─$ nmap -sV -p- -oN simple.nmap 10.10.110.33
Starting Nmap 7.95 ( https://nmap.org ) at 2025-06-17 20:34 EDT
Nmap scan report for 10.10.110.33
Host is up (0.096s latency).
Not shown: 65527 closed tcp ports (reset)
PORT      STATE SERVICE  VERSION
22/tcp    open  ssh      OpenSSH 8.2p1 Ubuntu 4ubuntu0.11 (Ubuntu Linux; protocol 2.0)
25/tcp    open  smtp     Postfix smtpd
110/tcp   open  pop3     Dovecot pop3d
143/tcp   open  imap     Dovecot imapd (Ubuntu)
993/tcp   open  ssl/imap Dovecot imapd (Ubuntu)
995/tcp   open  ssl/pop3 Dovecot pop3d
4000/tcp  open  http     Node.js (Express middleware)
50000/tcp open  http     Apache httpd 2.4.41 ((Ubuntu))
Service Info: Host:  mail.filepath.lab; OS: Linux; CPE: cpe:/o:linux:linux_kernel


┌──(kali㉿kali)-[~]
└─$ telnet 10.10.110.33 25
Trying 10.10.110.33...
Connected to 10.10.110.33.
Escape character is '^]'.
220 mail.filepath.lab ESMTP Postfix (Ubuntu)
?
502 5.5.2 Error: command not recognized
help
502 5.5.2 Error: command not recognized
EHLO mail.filepath.lab
250-mail.filepath.lab
250-PIPELINING
250-SIZE 10240000
250-VRFY
250-ETRN
250-STARTTLS
250-ENHANCEDSTATUSCODES
250-8BITMIME
250-DSN
250-SMTPUTF8
250 CHUNKING
VRFY root
252 2.0.0 root
VRFY admin
550 5.1.1 <admin>: Recipient address rejected: User unknown in local recipient table
VRFY user
550 5.1.1 <user>: Recipient address rejected: User unknown in local recipient table
421 4.4.2 mail.filepath.lab Error: timeout exceeded
Connection closed by foreign host.

we know a root user exists on the SMTP server so we can potentially yolo the PW creds with hydra 

hydra failed

┌──(kali㉿kali)-[~]
└─$ nmap -p 25 --script smtp-enum-users 10.10.94.1 -oN smpt-enum.nmap
Starting Nmap 7.95 ( https://nmap.org ) at 2025-06-19 22:05 EDT
Nmap scan report for 10.10.94.1
Host is up (0.089s latency).

PORT   STATE SERVICE
25/tcp open  smtp
| smtp-enum-users: 
|   root
|   admin
|   administrator
|   webadmin
|   sysadmin
|   netadmin
|   guest
|   user
|   web
|_  test

Nmap done: 1 IP address (1 host up) scanned in 1.79 seconds

┌──(kali㉿kali)-[~]
└─$ gobuster dir -u http://10.10.94.1:4000/ -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt  
===============================================================
Gobuster v3.6
by OJ Reeves (@TheColonial) & Christian Mehlmauer (@firefart)
===============================================================
[+] Url:                     http://10.10.94.1:4000/
[+] Method:                  GET
[+] Threads:                 10
[+] Wordlist:                /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt
[+] Negative Status codes:   404
[+] User Agent:              gobuster/3.6
[+] Timeout:                 10s
===============================================================
Starting gobuster in directory enumeration mode
===============================================================
/index                (Status: 302) [Size: 29] [--> /signin]
/images               (Status: 301) [Size: 179] [--> /images/]
/signup               (Status: 500) [Size: 1246]
/Index                (Status: 302) [Size: 29] [--> /signin]
/signin               (Status: 200) [Size: 1295]
/fonts                (Status: 301) [Size: 177] [--> /fonts/]
/INDEX                (Status: 302) [Size: 29] [--> /signin]
/Signup               (Status: 500) [Size: 1246]
/SignUp               (Status: 500) [Size: 1246]
/signUp               (Status: 500) [Size: 1246]
/SignIn               (Status: 200) [Size: 1295]
Progress: 34187 / 220561 (15.50%)^C
[!] Keyboard interrupt detected, terminating.
Progress: 34204 / 220561 (15.51%)
===============================================================
Finished
===============================================================
                                                                                                                
┌──(kali㉿kali)-[~]
└─$ gobuster dir -u http://10.10.94.1:50000/ -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt 
===============================================================
Gobuster v3.6
by OJ Reeves (@TheColonial) & Christian Mehlmauer (@firefart)
===============================================================
[+] Url:                     http://10.10.94.1:50000/
[+] Method:                  GET
[+] Threads:                 10
[+] Wordlist:                /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt
[+] Negative Status codes:   404
[+] User Agent:              gobuster/3.6
[+] Timeout:                 10s
===============================================================
Starting gobuster in directory enumeration mode
===============================================================
/templates            (Status: 301) [Size: 321] [--> http://10.10.94.1:50000/templates/]
/uploads              (Status: 301) [Size: 319] [--> http://10.10.94.1:50000/uploads/]
/javascript           (Status: 301) [Size: 322] [--> http://10.10.94.1:50000/javascript/]
/phpmyadmin           (Status: 403) [Size: 278]
/server-status        (Status: 403) [Size: 278]

This client side JS code snippet clues us that the recommend an activity upload form MIGHT affect the profile details, obviously we are after "isAdmin" field

form class="mb-4"> <h2 class="mb-3">Friend Details</h2> <ul class="list-group"> <li class="list-group-item"> id: 1 </li> <li class="list-group-item"> name: &#34;guest&#34; </li> <li class="list-group-item"> age: 25 </li> <li class="list-group-item"> country: &#34;UK&#34; </li> <li class="list-group-item"> albums: [{&#34;name&#34;:&#34;USA Trip&#34;,&#34;photos&#34;:&#34;www.thm.me&#34;}] </li> <li class="list-group-item"> isAdmin: false </li> <li class="list-group-item"> profileImage: &#34;/images/prof1.avif&#34; </li> </ul> </form> <!-- Recommend Activity Form --> <form action="/recommend-activity/1" method="post" class="mb-4"> <h2 class="mb-3">Recommend an Activity to guest </h2> <div class="form-group"> <input type="text" class="form-control" name="activityType" placeholder="Activity Type (e.g., Favorite Book)"> </div> <div class="form-group"> <input type="text" class="form-control" name="activityName" placeholder="Activity Name (e.g., 1984)"> </div> <button type="submit" class="btn btn-primary">Recommend Activity</button> </form>

surely enough the CTF CTF's

when feeding admin API GET HTTP command to the image upload secution of INCLUDE_IP:4000 you get the following response (in base 64 but that is easy to convert) from the picture upload form

{"ReviewAppUsername":"admin","ReviewAppPassword":"admin@!!!","SysMonAppUsername":"administrator","SysMonAppPassword":"S$9$qk6d#**LQU"}

which when you login to the sysmon portal with the sysmon creds dumped here 

┌──(kali㉿kali)-[~]
└─$ python3 -m http.server 8080
Serving HTTP on 0.0.0.0 port 8080 (http://0.0.0.0:8080/) ...
10.10.91.131 - - [14/Jul/2025 21:11:52] "GET /confirmed.txt HTTP/1.1" 200 -
@
http://10.10.91.131:4000/admin/settings

view-source:http://10.10.91.131:50000/profile.php?img=profile.png