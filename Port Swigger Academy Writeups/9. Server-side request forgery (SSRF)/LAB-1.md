# Lab-1: Basic SSRF against the local server
## LAB Description -
This lab has a stock check feature which fetches data from an internal system. To solve the lab, change the stock check URL to access the admin interface at http://localhost/admin and delete the user carlos.

## Solution - 
    * Browse to /admin and observe that you can't directly access the admin page.
    * Visit a product, click "Check stock", intercept the request in Burp Suite, and send it to Burp Repeater.
    * Change the URL in the stockApi parameter to http://localhost/admin. This should display the administration interface.
    * Read the HTML to identify the URL to delete the target user, which is:

    http://localhost/admin/delete?username=carlos

    * Submit this URL in the stockApi parameter, to deliver the SSRF attack.