WIN-03
tcp ports
```
[+] 192.168.100.55:       - 192.168.100.55:80 - TCP OPEN
[+] 192.168.100.55:       - 192.168.100.55:135 - TCP OPEN
[+] 192.168.100.55:       - 192.168.100.55:139 - TCP OPEN
[+] 192.168.100.55:       - 192.168.100.55:445 - TCP OPEN
[+] 192.168.100.55:       - 192.168.100.55:3389 - TCP OPEN
[+] 192.168.100.55:       - 192.168.100.55:5985 - TCP OPEN
[+] 192.168.100.55:       - 192.168.100.55:47001 - TCP OPEN
[+] 192.168.100.55:       - 192.168.100.55:49667 - TCP OPEN
[+] 192.168.100.55:       - 192.168.100.55:49664 - TCP OPEN
[+] 192.168.100.55:       - 192.168.100.55:49665 - TCP OPEN
[+] 192.168.100.55:       - 192.168.100.55:49670 - TCP OPEN
[+] 192.168.100.55:       - 192.168.100.55:49666 - TCP OPEN
[+] 192.168.100.55:       - 192.168.100.55:49669 - TCP OPEN
[+] 192.168.100.55:       - 192.168.100.55:49672 - TCP OPEN
[+] 192.168.100.55:       - 192.168.100.55:49671 - TCP OPEN


```

services
```
PORT      STATE SERVICE       VERSION
5580/tcp  open  http          Microsoft IIS httpd 10.0
|_http-server-header: Microsoft-IIS/10.0
55445/tcp open  microsoft-ds  Microsoft Windows Server 2008 R2 - 2012 microsoft-ds
55446/tcp open  ms-wbt-server Microsoft Terminal Services
|_ssl-date: 2024-02-06T21:37:18+00:00; 0s from scanner time.
| ssl-cert: Subject: commonName=WINSERVER-03
| Not valid before: 2024-02-05T13:36:26
|_Not valid after:  2024-08-06T13:36:26
55447/tcp open  http          Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-server-header: Microsoft-HTTPAPI/2.0
Service Info: OSs: Windows, Windows Server 2008 R2 - 2012; CPE: cpe:/o:microsoft:windows

```


user administrator:swordfish

windows/smb/psexec