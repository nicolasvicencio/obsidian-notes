#info-gathering 

Included in our [Exploit Database repository on GitLab](https://gitlab.com/exploit-database/exploitdb) is _searchsploit_, a command line search tool for Exploit-DB that also allows you to take a copy of Exploit Database with you, everywhere you go. SearchSploit gives you the power to perform detailed off-line searches through your locally checked-out copy of the repository. This capability is particularly useful for security assessments on segregated or air-gapped networks without Internet access.

Many exploits contain links to binary files that are not included in the standard repository but can be found in our [Exploit Database Binary Exploits repository](https://gitlab.com/exploit-database/exploitdb-bin-sploits) instead. If you anticipate you will be without Internet access on an assessment, ensure you check out both repositories for the most complete set of data.

The files of searchesploit are in `/usr/share/exploitdb`

If you want view the exploit on web
`searchsploit -w <exploit_name>`

If you want to copy the exploit in your local folder
`searchsploit -m <exploit_id>`