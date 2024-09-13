#enumeration #brute-force #web 

Gobuster is a tool used to brute-force:

- URIs (directories and files) in web sites.
- DNS subdomains (with wildcard support).
- Virtual Host names on target web servers.
- Open Amazon S3 buckets
- Open Google Cloud buckets
- TFTP servers

# Usage

dir mode:
```bash
gobuster dir -u https://mysite.com/path/to/folder -c 'session=123456' -t 50 -w common-files.txt -x .php,.html
```

dns mode:
```bash
gobuster dns -d mysite.com -t 50 -w common-names.txt
```
