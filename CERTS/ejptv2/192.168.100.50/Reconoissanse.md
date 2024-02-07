WIN-01
nmap open ports
```
PORT      STATE SERVICE
80/tcp    open  http
135/tcp   open  msrpc
139/tcp   open  netbios-ssn
445/tcp   open  microsoft-ds
3307/tcp  open  opsession-prxy
3389/tcp  open  ms-wbt-server
5985/tcp  open  wsman
47001/tcp open  winrm
49152/tcp open  unknown
49153/tcp open  unknown
49154/tcp open  unknown
49155/tcp open  unknown
49156/tcp open  unknown
49174/tcp open  unknown
```

nmap port services
```
PORT      STATE SERVICE            REASON          VERSION
80/tcp    open  http               syn-ack ttl 128 Apache httpd 2.4.51 ((Win64) PHP/7.4.26)
|_http-server-header: Apache/2.4.51 (Win64) PHP/7.4.26
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-title: WAMPSERVER Homepage
|_http-favicon: Unknown favicon MD5: 79E32EEA338FA735AD22D36104C4337A
135/tcp   open  msrpc              syn-ack ttl 128 Microsoft Windows RPC
139/tcp   open  netbios-ssn        syn-ack ttl 128 Microsoft Windows netbios-ssn
445/tcp   open  microsoft-ds       syn-ack ttl 128 Windows Server 2012 R2 Standard 9600 microsoft-ds
3307/tcp  open  opsession-prxy?    syn-ack ttl 128
| fingerprint-strings: 
|   NULL: 
|_    Host 'ip-192-168-100-5.ec2.internal' is not allowed to connect to this MariaDB server
3389/tcp  open  ssl/ms-wbt-server? syn-ack ttl 128
|_ssl-date: 2024-02-06T13:55:51+00:00; -1s from scanner time.
| rdp-ntlm-info: 
|   Target_Name: WINSERVER-01
|   NetBIOS_Domain_Name: WINSERVER-01
|   NetBIOS_Computer_Name: WINSERVER-01
|   DNS_Domain_Name: WINSERVER-01
|   DNS_Computer_Name: WINSERVER-01
|   Product_Version: 6.3.9600
|_  System_Time: 2024-02-06T13:55:37+00:00
| ssl-cert: Subject: commonName=WINSERVER-01
| Issuer: commonName=WINSERVER-01
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2024-02-05T13:36:48
| Not valid after:  2024-08-06T13:36:48
| MD5:   bd42 6bbf 38ee 9ebb dcb8 5028 91d7 06fe
| SHA-1: 5e22 a053 c461 8b6c aca5 9ed0 128c f48e c0fe eb77
| -----BEGIN CERTIFICATE-----
| MIIC3DCCAcSgAwIBAgIQFGQGl/gdlYhPGN1JLdCIZTANBgkqhkiG9w0BAQsFADAX
| MRUwEwYDVQQDEwxXSU5TRVJWRVItMDEwHhcNMjQwMjA1MTMzNjQ4WhcNMjQwODA2
| MTMzNjQ4WjAXMRUwEwYDVQQDEwxXSU5TRVJWRVItMDEwggEiMA0GCSqGSIb3DQEB
| AQUAA4IBDwAwggEKAoIBAQC3lhE7LE2BSX10YRldgJKz6GK3Otxwm2p46hh6Vtbq
| SqbOfg4LUVZGSYMl8I3mERhY2YP0jH4vkFCl83ImTsx7kEvJIBPdvOeALoNy57p3
| b5dP0hFyjBtpRrUhCTwD05NLOaGsniBtkMxx+t9FskT+mJlTMnAA/DCC+6pjL70G
| xZ7BOmJYqIqqHRozcH1FGd+X0ickhEiEST83TiV/SG1tn+9nyETbhbM+jpeVpSdh
| VHEyZ/IBVR/UTW66wXQeaP+7HJvqF4kth4br4bfEM3WPdmUHIrTxC6Hwa6Rc/A3V
| B1wvl4E2xXwUz+F4IEu1dJwI3TCDxt9dnxbppbqQCjuNAgMBAAGjJDAiMBMGA1Ud
| JQQMMAoGCCsGAQUFBwMBMAsGA1UdDwQEAwIEMDANBgkqhkiG9w0BAQsFAAOCAQEA
| sXOzJpNfrsm9nz2qt7/NUSmYSu9nV+ItP+DmdgpuHXqqa/Flva+GP3rft2gR9c0Q
| k6VoA6rXY5xWyNOgDGihTMQSxHwIUeKXBPzdT7lmCnz9iNFikF+erNtHdl1GUrc0
| ICLCOKDdCg4nZ00LDe4GXxCYG1gWrm1B8fgts3UlA25MpQ0jIMZ3haRk47LrrV2m
| X+NQW6Qmx9a+erliFb51tgilfJ+eZOJJ2DGvK+9ISNCYohouS9khoh394x3m66ml
| ebDqYhjQYARl91kHkU6WbpXAks3kcVSit/lyfl5NeYeuX7jQAwA7mDLrwlq78P7r
| Q9MLdoaESukc0OizHOCYvw==
|_-----END CERTIFICATE-----
5985/tcp  open  http               syn-ack ttl 128 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-server-header: Microsoft-HTTPAPI/2.0
|_http-title: Not Found
47001/tcp open  http               syn-ack ttl 128 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-server-header: Microsoft-HTTPAPI/2.0
|_http-title: Not Found
49152/tcp open  msrpc              syn-ack ttl 128 Microsoft Windows RPC
49153/tcp open  msrpc              syn-ack ttl 128 Microsoft Windows RPC
49154/tcp open  msrpc              syn-ack ttl 128 Microsoft Windows RPC
49155/tcp open  msrpc              syn-ack ttl 128 Microsoft Windows RPC
49156/tcp open  msrpc              syn-ack ttl 128 Microsoft Windows RPC
49174/tcp open  msrpc              syn-ack ttl 128 Microsoft Windows RPC
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port3307-TCP:V=7.92%I=7%D=2/6%Time=65C23A19%P=x86_64-pc-linux-gnu%r(NUL
SF:L,5C,"X\0\0\x01\xffj\x04Host\x20'ip-192-168-100-5\.ec2\.internal'\x20is
SF:\x20not\x20allowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server"
SF:);
MAC Address: 0E:40:2C:13:FD:B3 (Unknown)
Service Info: OSs: Windows, Windows Server 2008 R2 - 2012; CPE: cpe:/o:microsoft:windows

Host script results:
| smb-os-discovery: 
|   OS: (Windows Server 2012 R2 Standard 6.3)
|   OS CPE: cpe:/o:microsoft:windows_server_2012::-
|   Computer name: WINSERVER-01
|   NetBIOS computer name: WINSERVER-01\x00
|   Workgroup: WORKGROUP\x00
|_  System time: 2024-02-06T13:55:37+00:00
| smb2-security-mode: 
|   3.0.2: 
|_    Message signing enabled but not required
| smb2-time: 
|   date: 2024-02-06T13:55:37
|_  start_date: 2024-02-06T13:36:37
| smb-security-mode: 
|   account_used: guest
|   authentication_level: user
|   challenge_response: supported
|_  message_signing: disabled (dangerous, but default)
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 28474/tcp): CLEAN (Couldn't connect)
|   Check 2 (port 23001/tcp): CLEAN (Couldn't connect)
|   Check 3 (port 65370/udp): CLEAN (Failed to receive data)
|   Check 4 (port 25669/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
| nbstat: NetBIOS name: WINSERVER-01, NetBIOS user: <unknown>, NetBIOS MAC: 0e:40:2c:13:fd:b3 (unknown)
| Names:
|   WINSERVER-01<00>     Flags: <unique><active>
|   WORKGROUP<00>        Flags: <group><active>
|   WINSERVER-01<20>     Flags: <unique><active>
| Statistics:
|   0e 40 2c 13 fd b3 00 00 00 00 00 00 00 00 00 00 00
|   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
|_  00 00 00 00 00 00 00 00 00 00 00 00 00 00
|_clock-skew: mean: 0s, deviation: 0s, median: -1s

```


This machines is running wordpress

```bash
#/wp-login.php
[80][http-post-form] host: wordpress.local   login: admin   password: estrella
```

Host discovery
```
# ping sweep module
[+]     192.168.100.5 host found
[+]     192.168.100.1 host found
[+]     192.168.100.50 host found
[+]     192.168.100.51 host found
[+]     192.168.100.52 host found
[+]     192.168.100.55 host found
[+]     192.168.100.67 host found

```