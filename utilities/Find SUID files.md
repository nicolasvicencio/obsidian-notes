#linux 

```bash
find / -perm /4000
```

Search for writebles files
```bash
find / -not -type | -perm -o+w
```