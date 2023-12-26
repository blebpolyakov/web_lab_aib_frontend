# HTTP HTTPS и их параметры 
___________________________________________________
## Лабораторная работа №1

- `-I` - Получать только HTTP заголовок, а все содержимое страницы игнорировать.
- `-s` - указывает на "тихий" (silent) режим выполнения, при котором CURL не выводит на экран информацию о ходе выполнения запроса.
- `-v` - Этот ключ делает подробный вывод информации о запросе.
- `-L` - Принимать и обрабатывать перенаправления.
- `-k` - Отключает проверку SSL-сертификата.
- `--User-agent` -  Указание серверу, какое программное обеспечение или устройство отправляет запрос, в этом случае "Yandex".

## __[🎓 РГУПС](https://www.rgups.ru)__

**GET** запрос
>
> ```shell
> curl -I -k -v https://www.rgups.ru
> ```
HTTP ответ
>```shell
>> Connected to www.rgups.ru (80.72.224.90) port 443 # IP адрес веб сервера, порт к которому вы обращаетесь
>> HEAD / HTTP/1.1 #протокол по которому осуществлялся запрос
>> Host: www.rgups.ru  #истинное значение хоста ресурса
>> User-Agent: curl/8.4.0 #характеристики, по которым сервера и сетевые узлы могут определить тип приложения, операционную систему, производителя и/или версию пользовательского агента.
>> Accept: */* #указывает, какие типы контента, выраженные как MIME типы, клиент может понять (*/* - Любой MIME type)
>
>>
>< HTTP/1.1 200 OK  #код ответа и его значение
>< Server: nginx/1.19.1
>< Date: Tue, 26 Dec 2023 11:29:02 GMT
>< Content-Type: text/html; charset=utf-8  #данные о формате данных которые содержатся в теле ответа
>< Connection: keep-alive #определяет, остаётся ли сетевое соединение активным после завершения текущей транзакции.
>< X-Powered-By: ProcessWire CMS
>< Set-Cookie: wire=bd8ffc1a2b4fa2617512b162317d2a29; path=/; HttpOnly; SameSite=Lax
>< Expires: Thu, 19 Nov 1981 08:52:00 GMT
>< Cache-Control: no-store, no-cache, must-revalidate
>< Pragma: no-cache

- Ip: `80.72.224.90`
- Port: `443`
- Host: `rgups.ru`
- Cache-Control: `?`
- Content-Type: `text/html`
- Response code: `200 OK`
- Protocol: `HTTP/1.1`
___________________________________________________

## __[🐈Github](https://github.com/)__

**GET** запрос
>
> ```shell
> curl -I -k -v https://github.com/
> ```
HTTP ответ
>```shell
>> Connected to github.com (140.82.121.4) port 443
>> HEAD / HTTP/1.1
>> Host: github.com
>> User-Agent: curl/8.4.0
>> Accept: */*
>>
>< HTTP/1.1 200 OK
>< Server: GitHub.com
>< Date: Tue, 26 Dec 2023 11:41:23 GMT
>< Content-Type: text/html; charset=utf-8
>< Vary: X-PJAX, X-PJAX-Container, Turbo-Visit, Turbo-Frame, Accept-Language, Accept-Encoding, Accept, X-Requested-With
>< content-language: en-US
>< ETag: W/"34f7d816ed66fc4105331c8d2072198d"
>< Cache-Control: max-age=0, private, must-revalidate
>< Strict-Transport-Security: max-age=31536000; includeSubdomains; preload
>< X-Frame-Options: deny
>< X-Content-Type-Options: nosniff
>< X-XSS-Protection: 0

- Ip: `140.82.121.4`
- Port: `443`
- Host: `github.com`
- Cache-Control: `?`
- Content-Type: `text/html`
- Response code: `200 OK`
- Protocol: `HTTP/1.1`
___________________________________________________

## __[🚝 РЖД](https://www.rzd.ru/)__

**GET** запрос
>
> ```shell
> curl -I -s -v -L -k --User-agent "Yandex" https://www.rzd.ru/
> ```
HTTP ответ
>```shell
> * Connected to www.rzd.ru (212.164.138.126) port 443
>> HEAD / HTTP/1.1
>> Host: www.rzd.ru
>> User-Agent: Yandex
>> Accept: */*
>>
>< HTTP/1.1 200
>< Content-Type: text/html;charset=utf-8
>< Content-Length: 198392
>< Connection: keep-alive
>< Date: Tue, 26 Dec 2023 12:32:39 GMT
>< Vary: Accept-Encoding
>< X-UCM-Pod-Name: inex-ucm-5574464c4b-w2w8n
>< Strict-Transport-Security: max-age=15724800; includeSubDomains
>< Via: nginx1
>< X-Frame-Options: sameorigin
>< Set-Cookie: session-cookie=17a461adea3b2a93e236755718991a248e590325f77cfeb10742c70bbd98c250af9d8440f6c83801ac10c88851913505; Max-Age=86400; Path=/; secure; HttpOnly
>< X-XSS-Protection: 1; mode=block

- Ip: `212.164.138.126`
- Port: `443`
- Host: `rzd.ru`
- Cache-Control: `?`
- Content-Type: `text/html`
- Response code: `200`
- Protocol: `HTTP/1.1`
___________________________________________________

## __[🕸 Яндекс](https://yandex.ru/)__

**GET** запрос
>
> ```shell
> curl -I -s -v -L -k https://yandex.ru/
> ```
HTTP ответ
>```shell
>* Connected to yandex.ru (5.255.255.70) port 443
>> HEAD / HTTP/1.1
>> Host: yandex.ru
>> User-Agent: curl/8.4.0
>> Accept: */*
>>
>< HTTP/1.1 302 Moved temporarily
>< Accept-CH: Sec-CH-UA-Platform-Version, Sec-CH-UA-Mobile, Sec-CH-UA-Model, Sec-CH-UA, Sec-CH-UA-Full-Version-List, Sec-CH-UA-WoW64, Sec-CH-UA-Arch, Sec-CH-UA-Bitness, Sec-CH-UA-Platform, Sec-CH-UA-Full-Version, Viewport-Width, DPR, Device-Memory, RTT, Downlink, ECT
>< Cache-Control: max-age=1209600,private
>< Date: Tue, 26 Dec 2023 12:39:43 GMT
>< Location: https://dzen.ru/?yredirect=true
>< NEL: {"report_to": "network-errors", "max_age": 100, "success_fraction": 0.001, "failure_fraction": 0.1}
>< P3P: policyref="/w3c/p3p.xml", CP="NON DSP ADM DEV PSD IVDo OUR IND STP PHY PRE NAV UNI"
>< Portal: Home
>< Report-To: { "group": "network-errors", "max_age": 100, "endpoints": [{"url": "https://dr.yandex.net/nel", "priority": 1}, {"url": "https://dr2.yandex.net/nel", "priority": 2}]}
>< X-Content-Type-Options: nosniff
>< X-Robots-Tag: unavailable_after: 12 Sep 2022 00:00:00 PST
>< X-Yandex-Req-Id: 1703594383584860-12405667134167676348-balancer-l7leveler-kubr-yp-vla-131-BAL-8881

- Ip: `5.255.255.70`
- Port: `443`
- Host: `yandex.ru`
- Cache-Control: `max-age=1209600,private`
- Content-Type: `nosniff`
- Response code: `302 Moved temporarily`
- Protocol: `HTTP/1.1`
___________________________________________________

## __[🐍 Python](https://www.python.org/)__

**GET** запрос
>
> ```shell
> curl -I -s -v -L -k http://www.python.org/
> ```
HTTP ответ
>```shell
>  * Connected to www.python.org (151.101.84.223) port 80
>> HEAD / HTTP/1.1
>> Host: www.python.org
>> User-Agent: curl/8.4.0
>> Accept: */*
>>
>< HTTP/1.1 301 Moved Permanently
>< Connection: close
>< Content-Length: 0
>< Server: Varnish
>< Retry-After: 0
>< Location: https://www.python.org/
>< Accept-Ranges: bytes
>< Date: Tue, 26 Dec 2023 11:52:09 GMT
>< Via: 1.1 varnish
>< X-Served-By: cache-bma1645-BMA
>< X-Cache: HIT
>< X-Cache-Hits: 0

- Ip: `151.101.84.223`
- Port: `80`
- Host: `python.org`
- Cache-Control: `?`
- Content-Type: `text/html`
- Response code: `301 Moved Permanently`
- Protocol: `HTTP/1.1`
___________________________________________________


## __[Saint 🌠 GIT](https://git-scm.com/)__

**GET** запрос
>
> ```shell
> curl -I -s -v -L -k https://git-scm.com/
> ```
HTTP ответ
>```shell
>* Connected to git-scm.com (188.114.98.224) port 443
>* schannel: disabled automatic use of client certificate
>* using HTTP/1.x
>> HEAD / HTTP/1.1
>> Host: git-scm.com
>> User-Agent: curl/8.4.0
>> Accept: */*
>>
>< HTTP/1.1 200 OK
>< Date: Tue, 26 Dec 2023 12:50:13 GMT
>< Content-Type: text/html; charset=utf-8
>< Connection: keep-alive
>< X-Frame-Options: SAMEORIGIN
>< X-Xss-Protection: 1; mode=block
>< X-Content-Type-Options: nosniff
>< X-Download-Options: noopen
>< X-Permitted-Cross-Domain-Policies: none
>< Referrer-Policy: strict-origin-when-cross-origin
>< Cache-Control: public, max-age=14400
>< Etag: W/"4555dc199cf8e5ac99f1f0fd9b1e23ed"
>< X-Request-Id: 815ffbd2-6cda-410c-ad9e-83397cce9d7e
>< X-Runtime: 0.009214
>< Via: 1.1 vegur
>< CF-Cache-Status: HIT
>< Age: 1506
>< Server: cloudflare
>< CF-RAY: 83b972c28e915aae-DME

- Ip: `188.114.98.224`
- Port: `443`
- Host: `git-scm.com`
- Cache-Control: `public, max-age=14400`
- Content-Type: `text/html; charset=utf-8`
- Response code: `200 OK`
- Protocol: `HTTP/1.1`
___________________________________________________

## __[🐵 Jetbrains](https://www.jetbrains.com/)__

**GET** запрос
>
> ```shell
> curl -I -s -v -L -k https://www.jetbrains.com/
> ```
HTTP ответ
>```shell
>* Connected to www.jetbrains.com (18.66.97.10) port 443
>> HEAD / HTTP/1.1
>> Host: www.jetbrains.com
>> User-Agent: curl/8.4.0
>> Accept: */*
>>
>< HTTP/1.1 200 OK
>< Content-Type: text/html; charset=utf-8
>< Content-Length: 48898
>< Connection: keep-alive
>< Date: Tue, 26 Dec 2023 12:51:17 GMT
>< Server: nginx
>< X-Content-Type-Options: nosniff
>< Referrer-Policy: same-origin
>< Expires: Tue, 26 Dec 2023 12:51:17 GMT
>< Cache-Control: max-age=0
>< Pragma: no-cache
>< X-Frame-Options: DENY
>< X-Content-Type-Options: nosniff
>< X-Xss-Protection: 1; mode=block
>< Strict-Transport-Security: max-age=31536000;
>< Vary: Accept-Encoding
>< Via: 1.1 367a4718be97a49df7ac0500a986437a.cloudfront.net (CloudFront)
>< Alt-Svc: h3=":443"; ma=86400
>< Age: 280
>< Set-Cookie: cf_country-region=RU-ROS; Domain=jetbrains.com; Path=/; Secure
>< X-Cache: Hit from cloudfront
>< X-Amz-Cf-Pop: FRA56-P2
>< X-Amz-Cf-Id: xMIxAJfZ1HpgGY080HgnBTkqy3_uV45vHsWduOLhAB9fXzJhm92_Vw==


- Ip: `18.66.97.10`
- Port: `443`
- Host: `www.jetbrains.com`
- Cache-Control: `max-age=0`
- Content-Type: `text/html; charset=utf-8`
- Response code: `200 OK`
- Protocol: `HTTP/1.1`
___________________________________________________

## __[💪 VSC - this is best choose](https://code.visualstudio.com/)__

**GET** запрос
>
> ```shell
> curl -I -s -v -L -k https://code.visualstudio.com/
> ```
HTTP ответ
>```shell
>* Connected to code.visualstudio.com (13.107.213.45) port 443
>> HEAD / HTTP/1.1
>> Host: code.visualstudio.com
>> User-Agent: curl/8.4.0
>> Accept: */*
>>
>< HTTP/1.1 200 OK
>< Date: Tue, 26 Dec 2023 12:58:46 GMT
>< Content-Type: text/html; charset=utf-8
>< Content-Length: 49553
>< Connection: keep-alive
>< ETag: W/"c191-gRV3dKwYJtcZGAmSdhs78nRXDfU"
>< Strict-Transport-Security: max-age=31536000; includeSubDomains
>< Content-Security-Policy: frame-ancestors 'self'
>< X-Frame-Options: SAMEORIGIN
>< X-XSS-Protection: 1; mode=block
>< X-Content-Type-Options: nosniff
>< X-Powered-By: ASP.NET
>< x-azure-ref: 20231226T125846Z-yr1udc8t7x4uzb750748fpzndc0000000b20000000000kv1
>< X-Cache: CONFIG_NOCACHE
>< Accept-Ranges: bytes


- Ip: `13.107.213.45`
- Port: `443`
- Host: `code.visualstudio.com`
- Cache-Control: `CONFIG_NOCACHE`
- Content-Type: `text/html; charset=utf-8`
- Response code: `200 OK`
- Protocol: `HTTP/1.1`
___________________________________________________