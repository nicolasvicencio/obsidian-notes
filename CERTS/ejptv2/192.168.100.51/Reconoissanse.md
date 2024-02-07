WIN-02
tcp ports
```
[+] 192.168.100.51:       - 192.168.100.51:21 - TCP OPEN
[+] 192.168.100.51:       - 192.168.100.51:80 - TCP OPEN
[+] 192.168.100.51:       - 192.168.100.51:139 - TCP OPEN
[+] 192.168.100.51:       - 192.168.100.51:135 - TCP OPEN
[+] 192.168.100.51:       - 192.168.100.51:445 - TCP OPEN
[+] 192.168.100.51:       - 192.168.100.51:3389 - TCP OPEN
[+] 192.168.100.51:       - 192.168.100.51:5985 - TCP OPEN
[+] 192.168.100.51:       - 192.168.100.51:47001 - TCP OPEN
[+] 192.168.100.51:       - 192.168.100.51:49155 - TCP OPEN
[+] 192.168.100.51:       - 192.168.100.51:49152 - TCP OPEN
[+] 192.168.100.51:       - 192.168.100.51:49153 - TCP OPEN
[+] 192.168.100.51:       - 192.168.100.51:49154 - TCP OPEN
[+] 192.168.100.51:       - 192.168.100.51:49156 - TCP OPEN
[+] 192.168.100.51:       - 192.168.100.51:49170 - TCP OPEN

```

tcp services
```
5121/tcp  open  ftp          Microsoft ftpd
| ftp-syst: 
|_  SYST: Windows_NT
5180/tcp  open  http         Microsoft IIS httpd 8.5
|_http-title: IIS Windows Server
|_http-server-header: Microsoft-IIS/8.5
51445/tcp open  microsoft-ds Microsoft Windows Server 2008 R2 - 2012 microsoft-ds
51446/tcp open  ssl/unknown
| ssl-cert: Subject: commonName=WINSERVER-02
| Not valid before: 2024-02-05T13:36:44
|_Not valid after:  2024-08-06T13:36:44
51447/tcp open  http         Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-title: Not Found
|_http-server-header: Microsoft-HTTPAPI/2.0
Service Info: OSs: Windows, Windows Server 2008 R2 - 2012; CPE: cpe:/o:microsoft:windows

```