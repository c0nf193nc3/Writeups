# Lab-2: Basic SSRF against another back-end system
## LAB Description - 
This lab has a stock check feature which fetches data from an internal system. To solve the lab, use the stock check functionality to scan the internal 192.168.0.X range for an admin interface on port 8080, then use it to delete the user carlos.

# Solution - 
    * Visit a product, click "Check stock", intercept the request in Burp Suite, and send it to Burp Intruder.
    * Click "Clear §", change the stockApi parameter to http://192.168.0.1:8080/admin then highlight the final octet of the IP address (the number 1), click "Add §".
    * Switch to the Payloads tab, change the payload type to Numbers, and enter 1, 255, and 1 in the "From" and "To" and "Step" boxes respectively.
    * Click "Start attack".
    * Click on the "Status" column to sort it by status code ascending. You should see a single entry with a status of 200, showing an admin interface.
    * Click on this request, send it to Burp Repeater, and change the path in the stockApi to: /admin/delete?username=carlos
    

![Screenshot_2023-05-20_11_29_13](https://github.com/a-fai1ur3/Writeups/assets/119417999/bcdd3f16-7cea-4e56-a6a6-38bda52022ba)
![Screenshot_2023-05-20_11_30_04](https://github.com/a-fai1ur3/Writeups/assets/119417999/7fd6ad8e-e838-4447-8cf9-e27450369dfb)
![Screenshot_2023-05-20_11_37_45](https://github.com/a-fai1ur3/Writeups/assets/119417999/6de8b33a-91a1-4380-941c-f8475e93cc33)
![Screenshot_2023-05-20_11_38_29](https://github.com/a-fai1ur3/Writeups/assets/119417999/a77ddaa3-b479-487c-8d90-a44a957b3429)
![Screenshot_2023-05-20_11_39_07](https://github.com/a-fai1ur3/Writeups/assets/119417999/7c1fa693-0c0f-442b-be9e-3ee262b6dc4d)
