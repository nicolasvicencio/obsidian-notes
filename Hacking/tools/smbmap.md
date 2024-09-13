[[445 - SMB-SAMBA]] #enumeration #info-gathering 

SMBMap allows users to enumerate samba share drives across an entire domain. List share drives, drive permissions, share contents, upload/download functionality, file name auto-download pattern matching, and even execute remote commands. This tool was designed with pen testing in mind, and is intended to simplify searching for potentially sensitive data across large networks.

## Usage
```bash 
#smbmap -u <user> -p <pass> -d <domain> -H <ip_address> 
smbmap -u guest -p '' -d . -H 10.10.10.2 
```

`-r 'C$'` Read file
`-x 'ipconfig'` Execute
`--upload`
`--download`
