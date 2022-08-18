# İçerik Keşfi 
## Manuel Keşif - HTTP Başlıkları
### HTTP Başlıkları
- Web sunucusuna istek yaptığımızda, sunucu çeşitli HTTP başlıklarını döndürür. Bu başlıklar bazen web sunucusu yazılımı ve muhtemelen kullanılan programlama/komut dosyası dili gibi faydalı bilgiler içerebilir. Aşağıdaki örnekte, web sunucusunun NGINX sürüm 1.18.0 olduğunu ve PHP 7.4.3 sürümünü çalıştırdığını görebiliriz. Bu bilgileri kullanarak, kullanılan yazılımların savunmasız sürümlerini bulabiliriz. Aşağıdaki curl komutunu web sunucusuna karşı çalıştırmayı deneyin; burada -v anahtarı, başlıkların çıktısını alacak olan ayrıntılı modu etkinleştirir (ilginç bir şey olabilir!).
```
user@machine$ curl http://MACHINE_IP -v
*   Trying MACHINE_IP:80...
* TCP_NODELAY set
* Connected to MACHINE_IP (MACHINE_IP) port 80 (#0)
> GET / HTTP/1.1
> Host: MACHINE_IP
> User-Agent: curl/7.68.0
> Accept: */*
> 
* Mark bundle as not supporting multiuse
< HTTP/1.1 200 OK
< Server: nginx/1.18.0 (Ubuntu)
< X-Powered-By: PHP/7.4.3
< Date: Mon, 19 Jul 2021 14:39:09 GMT
< Content-Type: text/html; charset=UTF-8
< Transfer-Encoding: chunked
< Connection: keep-alive
```
