# Lab-3: Blind OS command injection with output redirection
## LAB Description - 
This lab contains a blind OS command injection vulnerability in the feedback function. The application executes a shell command containing the user-supplied details. The output from the command is not returned in the response. However, you can use output redirection to capture the output from the command. There is a writable folder at:

`/var/www/images/`

The application serves the images for the product catalog from this location. You can redirect the output from the injected command to a file in this folder, and then use the image loading URL to retrieve the contents of the file. To solve the lab, execute the whoami command and retrieve the output.

## Solution - 
    * Use Burp Suite to intercept and modify the request that submits feedback.
    * Modify the email parameter, changing it to:

        email=||whoami>/var/www/images/output.txt||

    * Now use Burp Suite to intercept and modify the request that loads an image of a product.
    * Modify the filename parameter, changing the value to the name of the file you specified for the output of the injected command:

        filename=output.txt

    * Observe that the response contains the output from the injected command.