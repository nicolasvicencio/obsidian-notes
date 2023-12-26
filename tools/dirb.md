#enumeration #info-gathering #brute-force 

DIRB is a Web Content Scanner. It looks for existing (and/or hidden) Web Objects. It basically works by launching a dictionary based attack against a web server and analyzing the responses.

DIRB comes with a set of preconfigured attack wordlists for easy usage but you can use your custom wordlists. Also DIRB sometimes can be used as a classic CGI scanner, but remember that it is a content scanner not a vulnerability scanner.

# Usage
```bash 
dirb http://192.168.1.224/ /usr/share/wordlists/dirb/common.txt
```
