#info-gathering 

Banner grabbing is an information gathering technique used by penetrations testers to enumerate information regrading the target operating system as well as the services that are running on its open ports.

The primary objective of banner grabvbing is to identify the service running on a specific port as well as the service version

Banner grabbing can be performed through various techniques:
- Performing a service version detection scan with Nmap
- connecting to the open port with Netcat
- Authenticating with the service (if the service supports authentication) for example SSH FTP Telnet etc

With [[nmap]] we can use banner --script
or with [[netcat]] we cat ` nc <ip_address> <port>` to get banner