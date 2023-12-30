#windows #vulnerability 

Windows can automate a variety of repetitive tasks. such as the mass roll out or installation of Windows on many systems.

This is typically done through the use of the Unattended Setup utility which is used to automate the mass installation/deployment of Window on systems

this tool utilizes configuration files that contain specific configurations and user account credentials, specifically the Administrator account's password

If the Unattended Windows Setup configuration file are left on the target system after installation, they can reveal user account credential that can be used by attackers to authenticate with Windows target legitimately

The Unattended Windows Setup utility will typically utilize on of the following configuration files that contain user account and system configurations information:
- C:\\Windows\Panther\Unattend.xml
- C:\\Windows\Panther\Autounattend.xml

As a security precaution, the passwords stored in the Unattended Windows Setup configuration file may be encoded in base64 