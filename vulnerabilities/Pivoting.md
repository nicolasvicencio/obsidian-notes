#windows #linux 

Pivoting is a post exploitation technique that involves utilizing a compromised host to attack other systems on the compromised host's private internal network.

After gaining access to one host, we can use the compromised host to exploit other hosts on the same internal network to which we could not access previously

Meterpreter provides us with the ability to add a network route to the internal network's subnet and consequently scan and exploit other systems on the network

Add network route to the target subnet
`run autoroute -s <ip_subnet>`

```bash
portfwd add -l <local_port> -p <victim_port> -r <victim_ip>
```

then
```bash
nmap -sS -sCV -p <local_port> localhost
```

then you can config the payload
`set payload windows/meterpreter/bind_tcp`
