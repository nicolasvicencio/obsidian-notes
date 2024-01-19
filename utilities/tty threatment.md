```
script /dev/null -c bash
ctrl+z

stty raw -echo; fg
reset xterm

export TERM=xterm

stty size
stty rows <number> columns <number
```