#windows #dump 

Mimikatz is an open-source tool that hackers use to steal credentials and other sensitive data from compromised Windows computers. It breaks Windows functionality and allows malicious users to access a system’s memory and security tokens, such as Kerberos tickets, which later can be used to gain unauthorized access to restricted information. Mimikatz extracted credentials usually come in the shape of a hash or plaintext password.

***mimkatz require elevated privileges in order to run correctly.***
**[[metasploit]]  have a extension called kiwi**

Kali linux already have the mimikatz executable located at `/usr/share/windows-resources/mimikatz/x64/mimikatz.exe`

When we have the hash we can a [[Pass-The-Hash]]
attack
