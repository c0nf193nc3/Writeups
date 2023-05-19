# Lab-4: Blind OS command injection with out-of-band interaction
## LAB Description - 
This lab contains a blind OS command injection vulnerability in the feedback function. The application executes a shell command containing the user-supplied details. The command is executed asynchronously and has no effect on the application's response. It is not possible to redirect output into a location that you can access. However, you can trigger out-of-band interactions with an external domain.

To solve the lab, exploit the blind OS command injection vulnerability to issue a DNS lookup to Burp Collaborator.

`Note - 
To prevent the Academy platform being used to attack third parties, our firewall blocks interactions between the labs and arbitrary external systems. To solve the lab, you must use Burp Collaborator's default public server.`

## Solution - 
    * Use Burp Suite to intercept and modify the request that submits feedback.
    * Modify the email parameter, changing it to:

    email=x||nslookup+x.BURP-COLLABORATOR-SUBDOMAIN||

    * Right-click and select "Insert Collaborator payload" to insert a Burp Collaborator subdomain where indicated in the modified email parameter.


![Screenshot_2023-05-19_23_26_00](https://github.com/a-fai1ur3/Writeups/assets/119417999/888a1fb6-ffc1-46c7-86b9-c3ed0b6eef7f)
