#service 

SMTP ( Simple Mail Transfer Protocol) is a communication protocol that is used for the transmission of email.

SMTP uses TCP port 25 by default. It is can also be configured to run on TCP port 465 and 587

Haraka is an open source high performance SMTP server developd in Node js.

The Haraka SMTP server comes with a plugin for porcessing attachments. Haraka versions prior to V2.8.9 are vulnerable to command injection

You can get the admin email with [[netcat]] 
```bash
nc <ip_address> 25
```