#enumeration #info-gathering #network 

Nmap ("Network Mapper") is a [free and open source](https://nmap.org/npsl/) utility for network discovery and security auditing. Many systems and network administrators also find it useful for tasks such as network inventory, managing service upgrade schedules, and monitoring host or service up time. Nmap uses raw IP packets in novel ways to determine what hosts are available on the network, what services (application name and version) those hosts are offering, what operating systems (and OS versions) they are running, what type of packet filters/firewalls are in use, and dozens of other characteristics. It was designed to rapidly scan large networks, but works fine against single hosts.

Types of port scanning https://nmap.org/book/man-port-scanning-basics.html

# Usage 

```bash
nmap -sS -T5 -p- --open -n -Pn <ip_adress> -oG scanPorts
```

```bash
nmae -sS --min-rate 5000 -p- --open -n -Pn <ip_adress> -oG scanPorst
```

You can extract the port numbers with this script

``` bash
cat scanPorst | grep -oP '\d{1,5}/open' | awk "{print $1}" FS='/' | xargs | tr ' ' ','
```

Then you can scan the services and do a basic script numeration
```bash
nmap -p<ports> -sCV -vvv <ip_adress> -oN scanServices
```

You can control the intensity of version scanning with
```bash
rest of the command.. -sV --version-intensity 8 ...
```

If the port 80 is open you can send this basic script
```bash
nmap --script=http.enum <ip_adress> <port>
```

The nmap script have the `.nse` prefix
#### Host scan
with `-sn` is no port scan
- host discovery and sends ICMP Echo Request packets

```bash
sudo nmap -sn -Pn <ip_address>
```
#### UDP scan
```bash
sudo nmap -Pn -sU <ip_address>
```
#### Subnet Scan
```bash
#ip 10.30.9.4
sudo nmap -sn 10.30.9.0/24 
```
#### File scan
```bash
sudo nmap -iL file.txt
```
#### TCP SYN ping
```bash
sudo nmap -PS<port> <ip_address>
```
#### TCP ACK ping
```bash
sudo nmap -PA<port> <ip_address>
```
#### Host discovery ICMP echo
```bash
sudo nmap -PE<port> <ip_address>
```
#### TCP connect Scan
This type of connection complete the 3way-handshake, is more noisier but more precise
```bash
sudo nmap -Pn -sT <ip_address>
```
#### OS Detection
```bash
sudo nmap -O <ip_address>
```

If you want to be more aggressive
```bash
sudo nmap -O --osscan-guess <ip_address>
```

`-D` Decoy IP
`-f` packet fragmentation
`--host-timeout`
`--scan-delay`
`--top-ports <number>` most popular ports
