SendEmail is a lightweight, completely command line based, SMTP email agent. It was designed to be used in bash scripts, Perl programs, and web sites, but it is also quite useful in many other contexts.

SendEmail is written in Perl and is unique in that it requires no special modules. It has a straight forward interface, making it very easy to use.

### Usage
```bash
sendemail -f admin@attacker.xyz -t root@openmailbox.xyz -s 192.26.29.3 -u Fakemail -m "Hi root, a fake from admin" -o tls=no
```