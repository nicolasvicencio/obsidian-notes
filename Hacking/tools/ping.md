#enumeration #info-gathering 

Linux
```bash
ping -c 5 <ip_address>
```

Windows
```bash 
ping -n 5 <ip_address>
```

If you want to tell to utility to scan subnet you change your 

```bash
#ip 10.1.0.2

ping -b -c 5 10.1.0.0
```