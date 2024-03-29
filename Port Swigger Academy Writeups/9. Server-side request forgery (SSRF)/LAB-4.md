# Lab-4: SSRF with whitelist-based input filter
## LAB Description - 
This lab has a stock check feature which fetches data from an internal system. To solve the lab, change the stock check URL to access the admin interface at http://localhost/admin and delete the user carlos. The developer has deployed an anti-SSRF defense you will need to bypass.

## Solution - 
    * Visit a product, click "Check stock", intercept the request in Burp Suite, and send it to Burp Repeater.
    * Change the URL in the stockApi parameter to http://127.0.0.1/ and observe that the application is parsing the URL, extracting the hostname, and validating it against a whitelist.
    * Change the URL to http://username@stock.weliketoshop.net/ and observe that this is accepted, indicating that the URL parser supports embedded credentials.
    * Append a # to the username and observe that the URL is now rejected.
    * Double-URL encode the # to %2523 and observe the extremely suspicious "Internal Server Error" response, indicating that the server may have attempted to connect to "username".
    * To access the admin interface and delete the target user, change the URL to:
    http://127.0.0.1:80%2523@stock.weliketoshop.net/admin/delete?username=carlos
    
![Screenshot_2023-05-20_15_15_42](https://github.com/a-fai1ur3/Writeups/assets/119417999/292317d9-5ab6-4ecc-a219-035b2da02eae)
![Screenshot_2023-05-20_15_14_58](https://github.com/a-fai1ur3/Writeups/assets/119417999/45f4ed7d-b410-42a7-8b14-fc8d7c07f3bb)
