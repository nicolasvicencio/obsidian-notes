[[ARP Poisoning]]

A program to perform an ARP spoofing attack against someone else on your local unencrypted network.

The arpspoof.c file sends 2 ARP requests, one to the default gateway and one to the victim, to get their MAC addresses. I then use these addresses to construct a phony ARP response to the victim that tells them that I am their default gateway (or any other IP address if you don't want it to be the default gateway). Some operating systems (e.g. Linux) are very suspicious of spurious ARP responses like this and will quickly figure out the ruse, but Windows will happily chug along in blissful ignorance until you annoy it by taking too long to respond to requests. To prevent even this weak defense mechanism from deploying, the program has an option to keep resending the phony packet every X number of seconds. Note: if it takes more than about 1 second for something to happen your response probably got lost, so try again.