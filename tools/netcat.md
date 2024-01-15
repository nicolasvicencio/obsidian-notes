#network

Ncat is a feature-packed networking utility which reads and writes data across networks from the command line. Ncat was written for the Nmap Project as a much-improved reimplementation of the venerable [Netcat](https://sectools.org/tool/netcat/). It uses both TCP and UDP for communication and is designed to be a reliable back-end tool to instantly provide network connectivity to other applications and users. Ncat will not only work with IPv4 and IPv6 but provides the user with a virtually limitless number of potential uses.

Netcat utilizes a client-server communication architecture with two modes:
- Client mode - Netcat be used in client mode to connect to any TCP/UDP port as well as a Netcat listener (server)
- Server mode - Netcat can be used to listen for connections from clients on a specific port

Netcat can be used by penetration testers to perform the following functionality.
- Banner Grabbing
- Port Scanning
- Transferring Files
- BindReverse Shells
# usage

```bash
nc -nlvp <ip_adress> -p <port>
```

```bash
echo "this is my message" > nc localhost <port>
```

```bash
nc -nlvp <ip_adress> < file.txt
```


