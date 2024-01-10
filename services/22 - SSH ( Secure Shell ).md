#service #linux 

The Secure Shell (SSH) protocol is a method for securely sending commands to a computer over an unsecured network. SSH uses cryptography to authenticate and encrypt connections between devices. SSH also allows for tunneling, or port forwarding, which is when data packets are able to cross networks that they would not otherwise be able to cross. SSH is often used for controlling servers remotely, for managing infrastructure, and for transferring files.

SSH authentication can be configured in two ways
- Username & password authentication
- Key based authentication

libssh is a multiplatform C library implementing the SSHv2 protocol on client and server side

libssh V0.6.0-0.8.0 in vulnerable to a n authentication bypass vulnerability in the libsssh server code that can be exploited to execute commands on the target server
## Usage
```bash
ssh root@<ip_address> 
```