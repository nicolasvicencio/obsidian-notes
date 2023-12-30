#windows 

The Windows OS stores hashed user account passwords locally in the SAM (Security Accounts Manager) database

Authentication and verification of user credentials is facilitated by the local security authority (LSA)

Windows Server 2003 utilize two different types of hashes:
- LM
- NTLM
Windows disables LM hashing and utilizes NTLM hashing from Windows Vista onwards.

NTLM utilized MD4 encryption
### SAM Database

SAM(Security Account Manager) is a database file that is responsible for managing user accounts and passwords on Windows. All user account passwords stores in the SAM database are hashed

The SAM database cannot be copied while the operating system is running

The windows NT kernel keeps the SAM database file locked and as a result attackers typically utilize in-memory techniques and tools to dump SAM hashes from the LSAAS process

In modern versions of Windows, the SAM database is encrypted with a syskey

***NOTE: Elevated/Administrative privileges are required in order to access and interact with the LSASS process***

