# HTTP HTTPS и их параметры 
___________________________________________________
## Лабораторная работа №1

`-I` - Получать только HTTP заголовок, а все содержимое страницы игнорировать.
`-v` - Этот ключ делает подробный вывод информации о запросе.
`-k` - Отключает проверку SSL-сертификата.

**GET** запрос
>
> ```shell
> curl -I -k -v https://www.rgups.ru
> ```
HTTP ответ
>```shell
>   Connected to www.rgups.ru (80.72.224.90) port 443
*   schannel: disabled automatic use of client certificate
*   using HTTP/1.x
>    HEAD / HTTP/1.1
>   Host: www.rgups.ru
>   User-Agent: curl/8.4.0
>   Accept: */*
>
<   HTTP/1.1 200 OK
<   Server: nginx/1.19.1
<   Date: Tue, 26 Dec 2023 11:29:02 GMT
<    Content-Type: text/html; charset=utf-8
<    Connection: keep-alive
<   X-Powered-By: ProcessWire CMS
<   Set-Cookie: wire=bd8ffc1a2b4fa2617512b162317d2a29; path=/; HttpOnly; SameSite=Lax
<   Expires: Thu, 19 Nov 1981 08:52:00 GMT
<   Cache-Control: no-store, no-cache, must-revalidate
<    Pragma: no-cache
>```
>___________________________________________________
**GET** запрос
>
> ```shell
> curl -v https://github.com/
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
