#vulnerability 

Keylogging is the process of recording or capturing the keystrokes entered on a target system

This technique is not limited to post exploitation, there are plenty of programs and USB devices that can be used to capture and transmit the keystrokes entered on a system. 

Meterpreter on a Windows system provides us with the ability to capture the keystrokes entered on a target system and download them back to our local system

In meterpreter you have to migrate to "explorer.exe" process
`keyscan_start`
`keyscan_dump`
`keyscan_stop`
