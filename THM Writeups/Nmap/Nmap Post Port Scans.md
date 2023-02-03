# Nmap Post Port Scans
## Task 2 (Service Detection) - 
* Start the target machine for this task and launch the AttackBox. Run nmap -sV --version-light MACHINE_IPvia the AttackBox. What is the detected version for port 143?
 = Dovecot imapd
* Which service did not have a version detected with --version-light? 
 = rpcbind
## Task 3 (OS Detection and Traceroute) - 
* Run nmap with -O option against MACHINE_IP. What OS did Nmap detect?
 = Linux
## Task 4 (Nmap Scripting Engine (NSE)) - 
* Knowing that Nmap scripts are saved in /usr/share/nmap/scripts on the AttackBox. What does the script http-robots.txt check for?
 = disallowed entries
* Can you figure out the name for the script that checks for the remote code execution vulnerability MS15-034 (CVE2015-2015-1635)?
 = http-vuln-cve2015-1635
* Launch the AttackBox if you haven't already. After you ensure you have terminated the VM from Task 2, start the target machine for this task. On the AttackBox, run Nmap with the default scripts -sC against MACHINE_IP. You will notice that there is a service listening on port 53. What is its full version value?
 = 9.9.5-9+deb8u19-Debian
* Based on its description, the script ssh2-enum-algos “reports the number of algorithms (for encryption, compression, etc.) that the target SSH2 server offers.” What is the name of the key exchange algorithms (kex_algorithms) that relies upon “sha1” and is supported by MACHINE_IP?
 = diffie-hellman-group14-sha1
## Task 5 (Saving the Output) - 
Terminate the target machine of the previous task and start the target machine for this task. On the AttackBox terminal, issue the command scp pentester@MACHINE_IP:/home/pentester/* . to download the Nmap reports in normal and grepable formats from the target virtual machine.

* Note that the username pentester has the password THM17577
Check the attached Nmap logs. How many systems are listening on the HTTPS port?
 = 3
* What is the IP address of the system listening on port 8089?
 = 172.17.20.147

Video Walkthrough - https://youtu.be/agKV_yqal_U