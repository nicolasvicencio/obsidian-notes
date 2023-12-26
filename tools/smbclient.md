[[445 - SMB]] #info-gathering #enumeration 

Is a client that can 'talk' to an SMB/CIFS server. It offers an interface similar to that of the ftp program (see [ftp(1)](https://www.samba.org/samba/docs/current/man-html/ftp.1.html)). Operations include things like getting files from the server to the local machine, putting files from the local machine to the server, retrieving directory information from the server and so on.

## Usage
```bash
smbclient -L <ip_address> -N
```

`-N` NULL session
`-U` user

```bash
smbclient //192.190.242.3/Public -N
```
With "get" we can pass the shared files to our system