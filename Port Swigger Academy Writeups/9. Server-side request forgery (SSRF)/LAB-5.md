# Lab-5: SSRF with filter bypass via open redirection vulnerability
## LAB Description - 
This lab has a stock check feature which fetches data from an internal system. To solve the lab, change the stock check URL to access the admin interface at http://192.168.0.12:8080/admin and delete the user carlos. The stock checker has been restricted to only access the local application, so you will need to find an open redirect affecting the application first.

## Solution - 
    * Visit a product, click "Check stock", intercept the request in Burp Suite, and send it to Burp Repeater.
    * Try tampering with the stockApi parameter and observe that it isn't possible to make the server issue the request directly to a different host.
    * Click "next product" and observe that the path parameter is placed into the Location header of a redirection response, resulting in an open redirection.
    * Create a URL that exploits the open redirection vulnerability, and redirects to the admin interface, and feed this into the stockApi parameter on the stock checker:

    /product/nextProduct?path=http://192.168.0.12:8080/admin
    * Observe that the stock checker follows the redirection and shows you the admin page.
    Amend the path to delete the target user:

    /product/nextProduct?path=http://192.168.0.12:8080/admin/delete?username=carlos