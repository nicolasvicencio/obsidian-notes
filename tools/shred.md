
The shred command helps to overwrite the data in place several times. This makes it harder for third party software and hardware probing to recover the data. That is why it's commonly used to securely remove data.

```bash
shred -zuv <file> -n 10
```