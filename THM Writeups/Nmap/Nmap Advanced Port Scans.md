# Nmap Advanced Port Scans
## Task 2 (TCP Null Scan, FIN Scan, and Xmas Scan) - 
* In a null scan, how many flags are set to 1?
 = 0
* In a FIN scan, how many flags are set to 1?
 = 1
* In a Xmas scan, how many flags are set to 1?
 = 3
* Start the VM and load the AttackBox. Once both are ready, open the terminal on the AttackBox and use nmap to launch a FIN scan against the target VM. How many ports appear as open|filtered?
 = 7
* Repeat your scan launching a null scan against the target VM. How many ports appear as open|filtered?
 = 7
## Task 3 (TCP Maimon Scan) - 
* In the Maimon scan, how many flags are set?
 = 2
## Task 4(TCP ACK, Window, and Custom Scan) - 
* In TCP Window scan, how many flags are set?
 = 1
* You decided to experiment with a custom TCP scan that has the reset flag set. What would you add after --scanflags? 
 = RST
* The VM received an update to its firewall ruleset. A new port is now allowed by the firewall. After you make sure that you have terminated the VM from Task 2, start the VM for this task. Launch the AttackBox if you haven't done that already. Once both are ready, open the terminal on the AttackBox and use Nmap to launch an ACK scan against the target VM. How many ports appear unfiltered?
 = 4
* What is the new port number that appeared?
 = 443
* Is there any service behind the newly discovered port number? (Y/N)
 = N
## Task 5 (Spoofing and Decoys) - 
* What do you need to add to the command sudo nmap MACHINE_IP to make the scan appear as if coming from the source IP address 10.10.10.11 instead of your IP address?
 = -S 10.10.10.11
* What do you need to add to the command sudo nmap MACHINE_IP to make the scan appear as if coming from the source IP addresses 10.10.20.21 and 10.10.20.28 in addition to your IP address?
 = -D 10.10.20.21,10.10.20.28,ME
## Task 6 ( Fragmented Packets) - 
* If the TCP segment has a size of 64, and -ff option is being used, how many IP fragments will you get?
 = 4
## Task 7 (Idle/Zombie Scan) - 
* You discovered a rarely-used network printer with the IP address 10.10.5.5, and you decide to use it as a zombie in your idle scan. What argument should you add to your Nmap command?
 = -sI 10.10.5.5
## Task 8 (Getting More Details) - 
* Launch the AttackBox if you haven't done so already. After you make sure that you have terminated the VM from Task 4, start the VM for this task. Wait for it to load completely, then open the terminal on the AttackBox and use Nmap with nmap -sS -F --reason MACHINE_IP to scan the VM. What is the reason provided for the stated port(s) being open?
 = syn-ack

Video Walkthrough - https://youtu.be/DoKeC7fqbo8