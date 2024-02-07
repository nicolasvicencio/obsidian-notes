UBUNTU
tcp ports
```
[+] 192.168.100.52:       - 192.168.100.52:22 - TCP OPEN
[+] 192.168.100.52:       - 192.168.100.52:21 - TCP OPEN
[+] 192.168.100.52:       - 192.168.100.52:80 - TCP OPEN
[+] 192.168.100.52:       - 192.168.100.52:139 - TCP OPEN
[+] 192.168.100.52:       - 192.168.100.52:445 - TCP OPEN
[+] 192.168.100.52:       - 192.168.100.52:3306 - TCP OPEN
[+] 192.168.100.52:       - 192.168.100.52:3389 - TCP OPEN

```

services
```
PORT     STATE SERVICE REASON         VERSION
5221/tcp open  ftp     syn-ack ttl 64 vsftpd 3.0.3
| ftp-syst: 
|   STAT: 
| FTP server status:
|      Connected to ::ffff:192.168.100.50
|      Logged in as ftp
|      TYPE: ASCII
|      No session bandwidth limit
|      Session timeout in seconds is 300
|      Control connection is plain text
|      Data connections will be plain text
|      At session startup, client count was 2
|      vsFTPd 3.0.3 - secure, fast, stable
|_End of status
| ftp-anon: Anonymous FTP login allowed (FTP code 230)
|_Can't get directory listing: PASV IP 192.168.100.52 is not the same as 127.0.0.1
5222/tcp open  ssh     syn-ack ttl 64 OpenSSH 8.2p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   3072 a3:3f:2d:73:09:35:09:05:00:ac:84:54:be:bf:cc:91 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDOs1i/bb5qgy2ar7gQMxvcnz3z6fas5JSEON5MIrDmUK1Ov3Rski4CFwqXU2Zmcb0FHG27+sq59fEks4onn2Bwdpi+e+yAL4eHf7J6G2vWAZ9pFyhMZX5NMX44sgGvON1msYb9PPoKSAQLiDuVTv6A7OYF5p3xy/zZ+y6YNKBOQM7PT+G0TTe0Nyc/A9GwO4z2WdfGueb+aDUTsjO53GSiLIYmG0GfYCoZMK3+1rzKDnQ2AVK/19W5piksGXM10254N93nzo+MBSznNEftjYyeybm9ObYLTOogOQvGGfUfKlWBVvFvSasSg9ei/CFpNZ3gjw5jwSkLYGhtuQcDFu39GYHJeaOapNPJw0IevERPCkfwKbCwQJUg6cU+NCqd7oiv9UyXpGb3hL1NtHsI7V2tQdQfxsjRvjqg760+9R60ScYkxaD/wOFWCCacCFbPk9U+qzX6gqqI+1VqEQXO23GoLXhjAzoTrO2tdV4m5O7bUgPSU64Cb40hCbvBfsWGMBc=
|   256 23:69:91:d4:dd:ce:43:21:2b:20:23:6f:f8:98:99:f4 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBFFAQm2C5CL62uUqQmOTl5kPH/PYF78638OSGNAIZ+/NM87YtB9RFsfSHZphbRErM0t70BAEk2ZFEm0AfAkADRQ=
|   256 74:3e:d2:24:c9:7d:f6:05:89:55:79:b2:a2:5e:87:e2 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIIOEiW03l+SMny+E3FkE8bzX8UvjT/YiYIm0/REiP3dy
| xmpp-info: 
|   STARTTLS Failed
|   info: 
|     unknown: 
|     errors: 
|       (timeout)
|     capabilities: 
|     xmpp: 
|     features: 
|     auth_mechanisms: 
|_    compression_methods: 
5280/tcp open  http    syn-ack ttl 64 Apache httpd 2.4.41
|_http-title: Index of /
| http-ls: Volume /
| SIZE  TIME              FILENAME
| -     2018-02-21 17:28  drupal/
|_
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-server-header: Apache/2.4.41 (Ubuntu)
Service Info: Host: ip-192-168-100-52.ec2.internal; OSs: Unix, Linux; CPE: cpe:/o:linux:linux_kernel

```

we gain acces with drupalgeddon

auditor:qwertyuiop