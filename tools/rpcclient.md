[[445 - SMB]] #info-gathering 

Is a utility initially developed to test MS-RPC functionality in Samba itself. It has undergone several stages of development and stability. Many system administrators have now written scripts around it to manage Windows NT clients from their UNIX workstation.

## Usage
```bash
rpcclient -U "" -N <ip_address>
```

When the connections is done
`srvinfo`
`enumdomusers`
`lookupnames <user>` get SID


