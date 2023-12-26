# HTTP HTTPS и их параметры 
___________________________________________________
## Лабораторная работа №1

`-I` - Получать только HTTP заголовок, а все содержимое страницы игнорировать.  
`-s` - указывает на "тихий" (silent) режим выполнения, при котором CURL не выводит на экран информацию о ходе выполнения запроса.  
`-v` - Этот ключ делает подробный вывод информации о запросе.  
`-L` - Принимать и обрабатывать перенаправления.
`-k` - Отключает проверку SSL-сертификата.

**GET** запрос
>
> ```shell
> curl -I -k -v https://www.rgups.ru
> ```
HTTP ответ
>```shell
>>Connected to www.rgups.ru (80.72.224.90) port 443
>>HEAD / HTTP/1.1
>>Host: www.rgups.ru
>>User-Agent: curl/8.4.0
>>Accept: */*
>>
>< HTTP/1.1 200 OK
>< Server: nginx/1.19.1
>< Date: Tue, 26 Dec 2023 11:29:02 GMT
>< Content-Type: text/html; charset=utf-8
>< Connection: keep-alive
>< X-Powered-By: ProcessWire CMS
>< Set-Cookie: wire=bd8ffc1a2b4fa2617512b162317d2a29; path=/; HttpOnly; SameSite=Lax
>< Expires: Thu, 19 Nov 1981 08:52:00 GMT
>< Cache-Control: no-store, no-cache, must-revalidate
>< Pragma: no-cache

>```
>___________________________________________________
**GET** запрос
>
> ```shell
> curl -I -k -v https://github.com/
> ```
HTTP ответ
>```shell
>>Connected to github.com (140.82.121.4) port 443
>>HEAD / HTTP/1.1
>>Host: github.com
>>User-Agent: curl/8.4.0
>>Accept: */*
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

>```
>___________________________________________________
**GET** запрос
>
> ```shell
> curl -I -s -v -L -k http://www.python.org/
> ```
HTTP ответ
>```shell
>  * Connected to www.python.org (151.101.84.223) port 80
>>HEAD / HTTP/1.1
>>Host: www.python.org
>>User-Agent: curl/8.4.0
>>Accept: */*
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

>```
>___________________________________________________
**GET** запрос
>
> ```shell
> curl -v http://www.python.org/
> ```
HTTP ответ
>```shell
>  
>```
>___________________________________________________
**GET** запрос
>
> ```shell
> curl -v http://www.python.org/
> ```
HTTP ответ
>```shell
>  
>```
