#info-gathering #enumeration #web 

Sublist3r is a python tool designed to enumerate subdomains of websites using OSINT. It helps penetration testers and bug hunters collect and gather subdomains for the domain they are targeting. Sublist3r enumerates subdomains using many search engines such as Google, Yahoo, Bing, Baidu and Ask. Sublist3r also enumerates subdomains using Netcraft, Virustotal, ThreatCrowd, DNSdumpster and ReverseDNS.

# Usage

- To enumerate subdomains of specific domain:
`python sublist3r.py -d example.com`

- To enumerate subdomains of specific domain and show only subdomains which have open ports 80 and 443 :
`python sublist3r.py -d example.com -p 80,443`

- To enumerate subdomains of specific domain and show the results in realtime:
`python sublist3r.py -v -d example.com`

- To enumerate subdomains and enable the bruteforce module:
`python sublist3r.py -b -d example.com`

- To enumerate subdomains and use specific engines such Google, Yahoo and Virustotal engines
`python sublist3r.py -e google,yahoo,virustotal -d example.com`