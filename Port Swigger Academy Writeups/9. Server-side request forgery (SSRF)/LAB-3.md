# Lab-3: SSRF with blacklist-based input filter
## LAB Description - 
This lab has a stock check feature which fetches data from an internal system. To solve the lab, change the stock check URL to access the admin interface at http://localhost/admin and delete the user carlos. The developer has deployed two weak anti-SSRF defenses that you will need to bypass.

## Solution - 
    * Visit a product, click "Check stock", intercept the request in Burp Suite, and send it to Burp Repeater.
    * Change the URL in the stockApi parameter to http://127.0.0.1/ and observe that the request is blocked.
    * Bypass the block by changing the URL to: http://127.1/
    * Change the URL to http://127.1/admin and observe that the URL is blocked again.
    * Obfuscate the "a" by double-URL encoding it to %2561 to access the admin interface and delete the target user.


![Screenshot_2023-05-20_12_02_18](https://github.com/a-fai1ur3/Writeups/assets/119417999/65d2e7f3-bc30-4279-b0db-192cb6e47c40)
![Screenshot_2023-05-20_12_02_50](https://github.com/a-fai1ur3/Writeups/assets/119417999/d2429cfb-b208-408e-a328-f3761c1b8d1b)
![Screenshot_2023-05-20_12_03_10](https://github.com/a-fai1ur3/Writeups/assets/119417999/ab1f99d6-b6f4-45b5-846f-de1acab70ee2)
![Screenshot_2023-05-20_12_04_22](https://github.com/a-fai1ur3/Writeups/assets/119417999/b5bafe46-78d2-474f-9e92-1cb707e76507)
![Screenshot_2023-05-20_12_05_03](https://github.com/a-fai1ur3/Writeups/assets/119417999/eed16984-4444-40b4-9727-a30ffd5227a0)
