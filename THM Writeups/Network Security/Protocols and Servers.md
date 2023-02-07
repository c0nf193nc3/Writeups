# Protocols and Servers
## Task 2 (Telnet) - 
* To which port will the telnet command with the default parameters try to connect?
 = 23
## Task 3 (Hypertext Transfer Protocol (HTTP)) - 
* Launch the attached VM. From the AttackBox terminal, connect using Telnet to MACHINE_IP 80 and retrieve the file flag.thm. What does it contain?
 = THM{e3eb0a1df437f3f97a64aca5952c8ea0}
## Task 4 (File Transfer Protocol (FTP)) - 
* Using an FTP client, connect to the VM and try to recover the flag file. What is the flag?
Username: frank
Password: D2xc9CgD
 = THM{364db6ad0e3ddfe7bf0b1870fb06fbdf}
## Task 5 (Simple Mail Transfer Protocol (SMTP)) - 
* Using the AttackBox terminal, connect to the SMTP port of the target VM. What is the flag that you can get?
 = THM{5b31ddfc0c11d81eba776e983c35e9b5}
## Task 6 (Post Office Protocol 3 (POP3)) - 
* Connect to the VM (MACHINE_IP) at the POP3 port. Authenticate using the username frank and password D2xc9CgD. What is the response you get to STAT?
 = +OK 0 0
* How many email messages are available to download via POP3 on MACHINE_IP?
 = 0
## Task 7 (Internet Message Access Protocol (IMAP)) -
 * What is the default port used by IMAP?
 = 143

Video Walkthrough - https://youtu.be/dPSDe3znDYA