# Lab-2: Blind OS command injection with time delays
## LAB Description - 
This lab contains a blind OS command injection vulnerability in the feedback function. The application executes a shell command containing the user-supplied details. The output from the command is not returned in the response. To solve the lab, exploit the blind OS command injection vulnerability to cause a 10 second delay.

## Solution - 
    * Use Burp Suite to intercept and modify the request that submits feedback.
    * Modify the email parameter, changing it to:

        email=email.com||ping+-c+10+127.0.0.1||

    * Observe that the response takes 10 seconds to return.
    
![Screenshot_2023-05-19_22_51_01](https://github.com/a-fai1ur3/Writeups/assets/119417999/c148e0b8-fef1-422c-a8ee-141880dbd6a4)
