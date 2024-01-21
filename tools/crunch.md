#brute-force 

Crunch is a wordlist generator where you can specify a standard character set or any set of characters to be used in generating the wordlists. The wordlists are created through combination and permutation of a set of characters. You can determine the amount of characters and list size.

This program supports numbers and symbols, upper and lower case characters separately and Unicode.

```bash
# crunch <min> <max> <options> 
crunch 10 10 -t ,%curtains -o file.txt
```