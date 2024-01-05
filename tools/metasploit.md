

The Metasploit Project is a computer security project that provides data about security vulnerabilities and assists penetration testing. It is owned by Rapid7, a US-based cyber security firm. A notable sub project of Metasploit is the open-source Metasploit Framework—a tool used to develop and run exploit code on remote target systems.

The Metasploit project includes anti-forensics and remediation tools, some of which are built into the Metasploit Framework. Metasploit comes pre-installed on the Kali Linux operating system.

 ### Modules
 - Exploit - A module that is used to take advantage of vulnerability and is typically paired with a payload.
 - Payload - Code that is delivered by MSF and remotely executed on the target after successful exploitation. An example of a payload is a revers shell that initiates a connection from the target system back to the attacker.
 - Encoder - Used to encode payloads in order to avoid AV detection. fro example, shikata_ga_nai is used to encode Windows payloads.
 - NOPS - Used to ensure that payloads sizes are consistent and ensure the stability of a payload when executed
 - Auxiliary - Module that is used to perform additional functionality like port scanning and enumeration.

When working with exploits. MSF provides you with two types of payloads than can be paired with an exploit
1. Non-Stages Payload - Payload that is sent to the target system as is along with the exploit.
2. Stages Payload - A staged payload is sent to the target in two parts whereby:
	- The first part( stager) contains a payload that is used to establish a reverse connection back tot the attacker, download the second part of the payload ( stage and execute it)

MSF stores module under the following directory on Linux systems
`/usr/share/metasploit-framework/modules`

User specified modules are stored under the following directory on LInux systems:

`~/.ms4/modules`

### Penetration Testing With MSF
| Penetration Testing Phase | Metasploit Framework Implementation |
| ---- | ---- |
| Information Gathering & enumeration | Auxiliary Modules |
| Vulnerabilty Scanning | Auxiliary Modules Nessus |
| Exploitation | Exploit Modules & Payloads |
| Post Escalation | Meterpreter |
| Privilege Escalation | Post Exploitation Modules Meterpreter |
| Maintaining Persistent Access | Post Exploitation Modules Persistence |

#### A very useful plugin is autopwn but you have to download it from git hub
You have to drop in `/usr/share/metasploit-framework/plugins`
`load db_autopwn`
`db_autopwn -h`
`analizew`
### Usage

Start the database
```bash
msfdb init
```

```bash
service postgresql start && metasploit
```

`search cve:2017 type:exploit platform:-linux`

### Create workspace
`workspace`
`hosts`
`workspace -a Test_workspace`
`workspace -d Test_workspace`

### Import nmap scan
You can import a .xml file [[nmap]] scan with `db_import <path_to_file.`
`hosts`
`vulns`
`services`
run 
### TCP Scan with msfconsole
`use auxiliary/scanner/portscan/tcp`

When you are doing pivoting and have a meterpreter session you can add the new IP with
`run autoroute -s <subnet_ip>`
Remember to add 1 to the last number

### Automating metasploit with resource scripts
They operate similarly to batch scripts, whereby, you can specify a  set of msfconsole commands that you want to execute sequentially.

You can load the script with msfconsole and automate the execution of the commands yous specified din the resource script.

We can use resource scripts to automate various tasks like setting up multi handlers as well as loading and executing payloads.

The resources are located in `/usr/share/metasploit-framewokr/scripts/resource`

You can write your own script like this

```bash
#handler.rc
use multi/handler
set payload windows/meterpreter/reverse_tcp
set lhosts 10.10.10.1
set lport 1234
run
```

You can load it in msfconsole `msfconsole -r handler.rc`


### WEB modules
- auxiliary/scanner/http/apache_userdir_enum
- auxiliary/scanner/http/brute_dirs
- auxiliary/scanner/http/dir_scanner
- auxiliary/scanner/http/dir_listing
- auxiliary/scanner/http/http_put
- auxiliary/scanner/http/files_dir
- auxiliary/scanner/http/http_login
- auxiliary/scanner/http/http_header
- auxiliary/scanner/http/http_version
- auxiliary/scanner/http/robots_txt
### MYSQL Modules
- auxiliary/admin/mysql/mysql_enum
- auxiliary/admin/mysql/mysql_sql
- auxiliary/scanner/mysql/mysql_file_enum
- auxiliary/scanner/mysql/mysql_hashdump
- auxiliary/scanner/mysql/mysql_login
- auxiliary/scanner/mysql/mysql_schemadump
- auxiliary/scanner/mysql/mysql_version
- auxiliary/scanner/mysql/mysql_writable_dirs

### SSH Modules
- auxiliary/scanner/ssh/ssh_version
- auxiliary/scanner/ssh/ssh_login