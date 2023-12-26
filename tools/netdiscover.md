#network #info-gathering 

Netdiscover is a network address discovering tool, developed mainly for those wireless networks without dhcp server, it also works on hub/switched networks. Its based on arp packets, it will send arp requests and sniff for replies.

```bash
netdiscover -i eth0 -r <ip_address>/24
```