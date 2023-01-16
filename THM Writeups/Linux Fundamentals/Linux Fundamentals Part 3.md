# Linux Fundamentals Part 3
## Task 3 ( Terminal Text Editors) - 
* Edit "task3" located in "tryhackme"'s home directory using Nano. What is the flag?
 = THM{TEXT_*******}
## Task 4 (General/Useful Utilities) - 
* Download the file http://MACHINE_IP:8000/.flag.txt onto the TryHackMe AttackBox.
What are the contents?
 = THM{WGET_*********}
## Task 5 (Processes 101) - 
* If we were to launch a process where the previous ID was "300", what would the ID of this new process be?
 = 301
* If we wanted to cleanly kill a process, what signal would we send it?
 = SIGTERM
* Locate the process that is running on the deployed instance (MACHINE_IP). What flag is given?
 = THM{*********}
* What command would we use to stop the service "myservice"?
 = systemctl stop myservice
* What command would we use to start the same service on the boot-up of the system?
 = systemctl enable myservice
* What command would we use to bring a previously backgrounded process back to the foreground?
 = fg
## Task 6 (Maintaining Your System: Automation) - 
* When will the crontab on the deployed instance (MACHINE_IP) run?
 = @reboot
## Task 8 (Maintaining Your System: Logs) - 
* What is the IP address of the user who visited the site?
 = 10.9.232.111
*  What file did they access?
 = catsanddogs.jpg

Video Walkthrough - https://youtu.be/NNjZAFzxcAg