#linux 

```bash
find / -perm /4000
```

Search for writebles files
```bash
find / -not -type -perm -o+w
```

```bash
find / -writable -type d 2>/dev/null
```