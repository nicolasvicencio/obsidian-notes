#linux 
#escalation 

Kernel exploits on LInux will typically target vulnerabilities in the LInux kernel to execute arbitrary code in order to run privileged system commands or to obtain a system shell.

This process will differ based on the Kernel version and distribution being targeted and the kernel exploit being used

Privilege escalation on Linux systems will typically follow the following methodology:
- Investigating kernel vulnerabilities
- Downloading compiling and transferring kernel exploits onto the target system

### Tools
https://github.com/The-Z-Labs/linux-exploit-suggester

### Cron Jobs

Linux implements task scheduling through a utility call Cron.

Cron is a time-based service that runs applications scripts and other commands repeatedly on a specified schedule

An application or script that has been configured to be run repeatedly with Cron is known as a cron job. Cron can be used to automate or repeat a wide variety of function on a system from daily backups to system upgrades and patches

Then crontab file as a configuration file that is used by the Cron utility to store and track Cron jobs that have been created

Cron jobs can also e run as any user on the system. this is a very important factor to keep an eye on as we will be targeting Cron jobs that has been configured to be run as the 'root' user.

In order to elevate our privileges we will need to find and identify cron jobs scheduled by the root user or the files being processed by the cron job.

You can list the cronjobs with `crontab -l`

### Exploiting SUID Binaries

In addition to the three main file access permissions, Linux also provides users with specialized permissions that can be utilized in specific situations. One of these access permissions is the SUID (Set Owner User ID) permission.

When applied this permission proves users with the ability to execute a script or binary with the permissions of the file owner as opposed to the user that is running the script or binary

The success of our attack will depend on the following factors: 
- Owner of the SUID binary - Given that we are attempting to elevate our privileges, we will only be exploiting SUID binaries that are owned by the 'root' user or other privileged users
- Access permissions - We will require executable permissions in order to execute the SUID binary


### Vulnerable Program
auxiliary/scanner/ssh/ssh_login