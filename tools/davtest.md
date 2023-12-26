#enumeration #info-gathering 
[[{80;443} - WebDav]]

DAVTest tests WebDAV enabled servers by uploading test executable files, and then (optionally) uploading files which allow for command execution or other actions directly on the target. It is meant for penetration testers to quickly and easily determine if enabled DAV services are exploitable.

### Usage
```bash
davtest -auth bobo:password_123321 -url <web_url>
```