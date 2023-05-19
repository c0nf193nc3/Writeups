
# Lab-1: OS command injection, simple case

## Lab Description - 
This lab contains an OS command injection vulnerability in the product stock checker. The application executes a shell command containing user-supplied product and store IDs, and returns the raw output from the command in its response. To solve the lab, execute the whoami command to determine the name of the current user.

## Solution - 
    * Use Burp Suite to intercept and modify a request that checks the stock level.
    * Modify the storeID parameter, giving it the value 1|whoami.
    * Observe that the response contains the name of the current user.