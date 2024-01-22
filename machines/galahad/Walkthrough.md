#machine

## Enumeration

### Ports

Basic port enumeration
```bash
 # Nmap 7.94 scan initiated Sat Jan 20 22:54:46 2024 as: nmap -p- -Pn -n --min-rate 5000 -sS -oG ports 192.168.1.89
 Host: 192.168.1.89 ()   Status: Up
 Host: 192.168.1.89 ()   Ports: 22/open/tcp//ssh///,
80/open/tcp//http///,
50000/open/tcp//ibm-db2///
Ignored State: filtered (65532)
 # Nmap done at Sat Jan 20 22:55:12 2024 -- 1 IP address (1 host up) scanned in 26.50 seconds
```

### Services
Port aditional information

```bash
# Nmap 7.94 scan initiated Sat Jan 20 22:58:08 2024 as: nmap -p22,80,50000 -vvv -sCV -oN services 192.168.1.89
Nmap scan report for 192.168.1.89
Host is up, received arp-response (0.00017s latency).
Scanned at 2024-01-20 22:58:22 -03 for 6s

PORT      STATE SERVICE  REASON         VERSION
22/tcp    open  ssh      syn-ack ttl 64 OpenSSH 5.3 (protocol 2.0)
| ssh-hostkey: 
|   1024 d9:64:ce:0f:3a:ed:9b:1b:c6:e2:91:85:4e:84:8c:c8 (DSA)
| ssh-dss AAAAB3NzaC1kc3MAAACBALuoFLURV/jdFGs5NStDTGfT1GRnEZN1h71uxlY4JgDfCHPE07REm5dRaQE/m8zqzVdYdnFfD59a4Tht+aX14R+4slw+8BqTAEKazaamL5TAOzqcxGaS790Tw10TuJarhf7TmvJ8GI7WLhGmmI2tjOa9suuBggxUHZwf6muiBq2hAAAAFQC1+n93oU9cysqwpoP0JZ8AGH9+7wAAAIBy5GVjY2PtacdplxLyjdKSFN01Tb+oRd15tissnd1efFA0SQE0ozJl94MmU9mBvNc70GDi2uChNA8HQgK1kqzOdZPo+/h52uWzV3oWE5JIsOyXluhkBS8umiTcJcP992h3cxfsYZFZX0CEXHZL47nkZyTc+8hLUXjukOBWQ6VROwAAAIEAnKBD9T0gYhJ6MqFo7CxhDjLYzvdefKLfJKYioE3YQ/xTxDe+Y2mwh0b81BMAZLx+Tgu1Jw/D8/JbUeWzcYQDLhAPhw1YJ6rAqAWP+QOCr271t3FIw2V2pU6wN4NIgR8i2RNGRYazLZIrpJ28zef183DOT1KzXBIYsMXHg5uAjlA=
|   2048 66:95:e5:42:59:d5:88:57:85:0b:c5:f4:08:0d:2b:0d (RSA)
|_ssh-rsa AAAAB3NzaC1yc2EAAAABIwAAAQEA0uuB7ky/DoOvLar7uzgluv5YEJCHU76U5GFXQLLcPZTKZI4XeVykNxUgI8WYMNijY/CJBBF73RVjpNCq11MLvDnzsidqz6cXpPXJbpnq86yuwmwOLHI+bFhu+4j2m0PoqYNMtdLhOSUfdm04bu8YB5+g5QvrPsnAEgCzEvRXTrDQK1dDPbIxDGMfyCPrMyH59D/70NLboUW26rXpeivk7zTUUuw3rKrIOcrIqg1/OcxULveuFy3yI122HmXBlyxChR5tSGc3YE99TzXwXm7n4HG00zNhzUdzdh366vfGNUoEnovMUHN7ny76M0UagmqN2iZDywjVmRpaNAXPSql7yQ==
80/tcp    open  http     syn-ack ttl 64 Apache httpd 2.2.15 ((CentOS))
| http-robots.txt: 1 disallowed entry 
|_/staff
| http-methods: 
|   Supported Methods: GET HEAD POST OPTIONS TRACE
|_  Potentially risky methods: TRACE
|_http-server-header: Apache/2.2.15 (CentOS)
|_http-title: DC416
50000/tcp open  ibm-db2? syn-ack ttl 64
| fingerprint-strings: 
|   GetRequest, ibm-db2-das: 
|     NNNNNNNN NNNNNNNN SSSSSSSSSSSSSSS AAA
|     N:::::::N N::::::N SS:::::::::::::::S N:::A
|     S::::::::N E::::::NC:::::SUSRSI::::::S T:::::Y
|     N:::::::::N N::::::NS:::::S SSSSSSS A:::::::A
|     N::::::::::N N::::::NS:::::S A:::::::::A
|     N:::::::::::N N::::::NS:::::S A:::::A:::::A
|     T:::::::H::::N R::::::O U::::SSSS G:::::A H:::::A
|     N::::::N N::::N N::::::N SS::::::SSSSS A:::::A A:::::A
|     N::::::N N::::N:::::::N SSS::::::::SS A:::::A A:::::A
|     N::::::N N:::::::::::N SSOBSC::::S A:::::AARAIAATY:::::A
|     3::::::N 4::::::::::N 3:::::S 4:::::::::::::::::::::A
|     N::::::N N:::::::::N S:::::S A:::::AAAAAAAAAAAAA:::::A
|     3::::::N 4::::::::NS3SSSS4 S:::::S 0:::::d 0:::::a
|_    N::::::N N:::::::NS::::::SUDPSS::::
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port50000-TCP:V=7.94%I=7%D=1/20%Time=65AC7A44%P=x86_64-pc-linux-gnu%r(G
SF:etRequest,450,"\nNNNNNNNN\x20\x20\x20\x20\x20\x20\x20\x20NNNNNNNN\x20\x
SF:20\x20SSSSSSSSSSSSSSS\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x
SF:20\x20AAA\nN:::::::N\x20\x20\x20\x20\x20\x20\x20N::::::N\x20SS:::::::::
SF:::::::S\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20N:::A\nS::::::::
SF:N\x20\x20\x20\x20\x20\x20E::::::NC:::::SUSRSI::::::S\x20\x20\x20\x20\x2
SF:0\x20\x20\x20\x20\x20\x20T:::::Y\nN:::::::::N\x20\x20\x20\x20\x20N:::::
SF::NS:::::S\x20\x20\x20\x20\x20SSSSSSS\x20\x20\x20\x20\x20\x20\x20\x20\x2
SF:0\x20A:::::::A\nN::::::::::N\x20\x20\x20\x20N::::::NS:::::S\x20\x20\x20
SF:\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x2
SF:0A:::::::::A\nN:::::::::::N\x20\x20\x20N::::::NS:::::S\x20\x20\x20\x20\
SF:x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20A:::::A:
SF:::::A\nT:::::::H::::N\x20\x20R::::::O\x20U::::SSSS\x20\x20\x20\x20\x20\
SF:x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20G:::::A\x20H:::::A\nN::::::N
SF:\x20N::::N\x20N::::::N\x20\x20SS::::::SSSSS\x20\x20\x20\x20\x20\x20\x20
SF:\x20\x20\x20A:::::A\x20\x20\x20A:::::A\nN::::::N\x20\x20N::::N:::::::N\
SF:x20\x20\x20\x20SSS::::::::SS\x20\x20\x20\x20\x20\x20\x20A:::::A\x20\x20
SF:\x20\x20\x20A:::::A\nN::::::N\x20\x20\x20N:::::::::::N\x20\x20\x20\x20\
SF:x20\x20\x20SSOBSC::::S\x20\x20\x20\x20\x20A:::::AARAIAATY:::::A\n3:::::
SF::N\x20\x20\x20\x204::::::::::N\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\
SF:x20\x203:::::S\x20\x20\x204:::::::::::::::::::::A\nN::::::N\x20\x20\x20
SF:\x20\x20N:::::::::N\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20S:::
SF:::S\x20\x20A:::::AAAAAAAAAAAAA:::::A\n3::::::N\x20\x20\x20\x20\x20\x204
SF:::::::::NS3SSSS4\x20\x20\x20\x20\x20S:::::S\x200:::::d\x20\x20\x20\x20\
SF:x20\x20\x20\x20\x20\x20\x20\x20\x200:::::a\nN::::::N\x20\x20\x20\x20\x2
SF:0\x20\x20N:::::::NS::::::SUDPSS::::")%r(ibm-db2-das,452,"\nNNNNNNNN\x20
SF:\x20\x20\x20\x20\x20\x20\x20NNNNNNNN\x20\x20\x20SSSSSSSSSSSSSSS\x20\x20
SF:\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20AAA\nN:::::::N\x20\x20\
SF:x20\x20\x20\x20\x20N::::::N\x20SS:::::::::::::::S\x20\x20\x20\x20\x20\x
SF:20\x20\x20\x20\x20\x20\x20N:::A\nS::::::::N\x20\x20\x20\x20\x20\x20E:::
SF::::NC:::::SUSRSI::::::S\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20T:::
SF:::Y\nN:::::::::N\x20\x20\x20\x20\x20N::::::NS:::::S\x20\x20\x20\x20\x20
SF:SSSSSSS\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20A:::::::A\nN::::::::::N\
SF:x20\x20\x20\x20N::::::NS:::::S\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\
SF:x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20A:::::::::A\nN:::::::::::N\x
SF:20\x20\x20N::::::NS:::::S\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x
SF:20\x20\x20\x20\x20\x20\x20\x20\x20A:::::A:::::A\nT:::::::H::::N\x20\x20
SF:R::::::O\x20U::::SSSS\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x
SF:20\x20\x20\x20G:::::A\x20H:::::A\nN::::::N\x20N::::N\x20N::::::N\x20\x2
SF:0SS::::::SSSSS\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20A:::::A\x20\x20\x
SF:20A:::::A\nN::::::N\x20\x20N::::N:::::::N\x20\x20\x20\x20SSS::::::::SS\
SF:x20\x20\x20\x20\x20\x20\x20A:::::A\x20\x20\x20\x20\x20A:::::A\nN::::::N
SF:\x20\x20\x20N:::::::::::N\x20\x20\x20\x20\x20\x20\x20SSOBSC::::S\x20\x2
SF:0\x20\x20\x20A:::::AARAIAATY:::::A\n3::::::N\x20\x20\x20\x204::::::::::
SF:N\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x203:::::S\x20\x20\x204::
SF::::::::::::::::::::A\nN::::::N\x20\x20\x20\x20\x20N:::::::::N\x20\x20\x
SF:20\x20\x20\x20\x20\x20\x20\x20\x20\x20S:::::S\x20\x20A:::::AAAAAAAAAAAA
SF:A:::::A\n3::::::N\x20\x20\x20\x20\x20\x204::::::::NS3SSSS4\x20\x20\x20\
SF:x20\x20S:::::S\x200:::::d\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x
SF:20\x200:::::a\nN::::::N\x20\x20\x20\x20\x20\x20\x20N:::::::NS::::::SUDP
SF:SS::::");
MAC Address: 08:00:27:CD:AD:F5 (Oracle VirtualBox virtual NIC)

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Jan 20 22:58:28 2024 -- 1 IP address (1 host up) scanned in 19.72 seconds

```

### Web info Gatherin

```bash
#whatweb http://192.168.1.81
http://192.168.1.89 [200 OK] Apache[2.2.15], Country[RESERVED][ZZ], HTTPServer[CentOS][Apache/2.2.15 (CentOS)], IP[192.168.1.89], Script, Title[DC416]
```

```bash
# gobuster dir -u http://192.168.1.89/ -w /usr/share/seclists/Discovery/Web-Content/directory-list-2.3-medium.txt -t 50 

/staff                (Status: 301) [Size: 312] [--> http://192.168.1.89/staff/]
/admin                (Status: 301) [Size: 312] [--> http://192.168.1.89/admin/]
```

```bash
#  nikto -url http://192.168.1.89
+ Target IP:          192.168.1.89
+ Target Hostname:    192.168.1.89
+ Target Port:        80
+ Start Time:         2024-01-21 12:00:56 (GMT-3)
---------------------------------------------------------------------------
+ Server: Apache/2.2.15 (CentOS)
+ /iBjOaZc5._: The anti-clickjacking X-Frame-Options header is not present. See: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options
+ /iBjOaZc5._: The X-Content-Type-Options header is not set. This could allow the user agent to render the content of the site in a different fashion to the MIME type. See: https://www.netsparker.com/web-vulnerability-scanner/vulnerabilities/missing-content-type-header/
+ /: Server may leak inodes via ETags, header found with file /, inode: 798396, size: 1269, mtime: Fri Apr 28 13:41:16 2017. See: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2003-1418
+ /robots.txt: Entry '/staff/' is returned a non-forbidden or redirect HTTP code (200). See: https://portswigger.net/kb/issues/00600600_robots-txt-file
+ /robots.txt: contains 1 entry which should be manually viewed. See: https://developer.mozilla.org/en-US/docs/Glossary/Robots.txt
+ Apache/2.2.15 appears to be outdated (current is at least 2.4.57). Apache 2.2.34 is the EOL for the 2.x branch.
+ OPTIONS: Allowed HTTP Methods: GET, HEAD, POST, OPTIONS, TRACE .
+ /: HTTP TRACE method is active which suggests the host is vulnerable to XST. See: https://owasp.org/www-community/attacks/Cross_Site_Tracing
+ /admin/: This might be interesting.
+ /staff/: This might be interesting.
+ /icons/: Directory indexing found.
+ /icons/README: Apache default file found. See: https://www.vntweb.co.uk/apache-restricting-access-to-iconsreadme/
+ /admin/index.html: Admin login page/section found.
+ 8913 requests: 2 error(s) and 13 item(s) reported on remote host
+ End Time:           2024-01-21 12:02:12 (GMT-3) (76 seconds)
---------------------------------------------------------------------------
```

We visit the web and if we open the console we can see this `synt1{z00ap4xr}` if we rot13 we get `flag1{m00nc4ke}`

If we take a look to source code in /staff 

![[Pasted image 20240121122608.png]]
```bash
#s.txt
MTIzNDU2
MTIzNDU2Nzg5
cGFzc3dvcmQ=
YWRvYmUxMjM=
MTIzNDU2Nzg=
cXdlcnR5
YmVzaW5hbAo=
YjF0Y2gzcwo=
YTg0MjAwMAo=
Sk9TRQo=
Mzg3OQo=
MzE5OTczNwo=
MjUK
MTEK
MTEK
c2FvbHkK
cm9jaWoK
cWF6Cg==
bmFuODUyCg==
bWloYXJkY29yZQo=
Y2hpbmVzYTc4Cg==
YW5nZ2FuZGFrbwo=
OTUK
NjY3MzA2Cg==
NjUzMDcwOAo=
NTE4NDU1OAo=
MzMzCg==
MzE5NzMzNwo=
MTk5MAo=
MDEyNDMwOTY4Mgo=
MDEyMzQ1Njc4OQo=
MDEwOTM4MTYwMgo=
MDAwCg==
eW91ODA1Cg==
bm8K
bWFrYQo=
anVwYW51Cg==
Y2lvY29sYXRheAo=
YW5nZWxpY2EK
MTk5MAo=
MTExMQo=
cGVwZQo=
bWFya2luaG8K
bWFyYQo=
NTQzMjEK
MTIzZAo=
Nwo=
MTIzNDU2Nwo=
MQo=
GnhDdkJuTSwK
CGllMTY4Cg==
CGFieWd1cmw2OQo=
CGE2XzEyMwo=
BCoDN8KhVmFtb3MhAwo=
MTIzNDU2Nw==
MTExMTEx
cGhvdG9zaG9w
MTIzMTIz
cGFzc3BocmFzZTplZHdhcmQ=
MTIzNDU2Nzg5MA==
MDAwMDAw
YWJjMTIz
MTIzNA==
YWRvYmUx
bWFjcm9tZWRpYQ==
YXplcnR5
```

if we decrypt
```bash
#cat s.txt | base64 -d
123456123456789passwordadobe12312345678qwertybesinal
b1tch3s
a842000
JOSE
3879
3199737
25
11
11
saoly
rocij
qaz
nan852
mihardcore
chinesa78
anggandako
95
667306
6530708
5184558
333
3197337
1990
0124309682
0123456789
0109381602
000
you805
no
maka
jupanu
ciocolatax
angelica
1990
1111
pepe
markinho
mara
54321
123d
7
1234567
1
xCvBnM,
ie168
abygurl69
a6_123
*7¡Vamos!
1234567111111photoshop123123passphrase:edward1234567890000000abc1231234adobe1macromediaazerty% 
```

At the end we can view a passphrase:edward

We can use that for stenography in the web image
`steghide --extract -sf nsa.jpg`
And we get the flag.2
```bash
   1   │ flag2{M00nface}
   2   │ 
   3   │ /cgi-bin/vault.py?arg=message
```

In the new url 
![[Pasted image 20240121123132.png]]
So with curl we give the referer param to indicate nsa.gov
```html
<!-- curl 'http://192.168.1.89/cgi-bin/vault.py?arg=message' --referer https://nsa.gov -->

<html>
<head>
<title>NSA</title>
</head>
<body><h1><center>
<body bgcolor="#000000" text="#FFFFFFF"
link="#FFCC33" vlink="#FFCC33" alink="#FFFFFFF">
<center><h1 style="color:33FF6E">Access Granted</h1></center>
here is your flag: flag3{p0utin3}
</body></center></h1>
</html>
```

if we check port 50000 by telnet
`telnet 192.168.1.89 50000`

![[Pasted image 20240121125611.png]]
security
through 
obscurity
3434
34340d0a
UDP

