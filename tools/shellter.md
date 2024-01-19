#AV

Shellter is a dynamic shellcode injection tool, and the first truly dynamic PE infector ever created.

It can be used in order to inject shellcode into native Windows applications.

The shellcode can be something yours or something generated through a framework, such as Metasploit.

Shellter takes advantage of the original structure of the PE file and doesn’t apply any modification such as changing memory access permissions in sections (unless the user wants), adding an extra section with RWE access, and whatever would look dodgy under an AV scan.

Shellter uses a unique dynamic approach which is based on the execution flow of the target application, and this is just the tip of the iceberg.

  
Shellter is not just an EPO infector that tries to find a location to insert an instruction to redirect execution to the payload.

Unlike any other infector, Shellter’s advanced infection engine never transfers the execution flow to a code cave or to an added section in the infected PE file.
