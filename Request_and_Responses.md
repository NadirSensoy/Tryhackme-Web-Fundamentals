# Detaylarıyla HTTP
## İstekler ve Cevaplar
- Biz bir web siteye eriştiğimizde, tarayıcınız HTML, görüntüler gibi varlıklar için bir web sunucusuna istekte bulunması ve yanıtları indirmesi gerekir. Ondan önce, senin tarayıcına özellikle nerede ve nasıl o kaynaklara erişim sağlayacağını söylemen gerekir, işte burada URL'ler bize yardım ediyor.
## URL nedir?
- Eğer daha önce internet kullandıysanız daha önce URL'de kullandınız demektir. Bir URL ağırlıklı olarak internetteki kaynağa nasıl erişileceğinin talimatını verir. Aşağıdaki görüntüde URL'in nasıl göründüğünü tüm özellikleriyle gösteriyor.(Her istekte tüm özellikler kullanılmaz)
- 
![newurl](https://user-images.githubusercontent.com/86947080/184703328-aaa9f3da-f817-4405-acdf-6a0f19c5484e.png)
### Scheme (Şema)
- Bu HTTP, HTTPS, FTP (File Transfer Protokol) gibi kaynaklara erişim için hangi protokolün kullanılacağını bildirir.
### User (Kullanıcı)
- Bazı hizmetler giriş onayı gerektirir, giriş yapmak için kullanıcı adı ve şifre URL içinde yer alır.
### Host
- Erişim sağlamak istediğiniz alan adı veya ip adresidir.
### Port
- Bağlanmak istediğiniz port, genellikle HTTP için 80, HTTPS için 443'tür. Ama 1-65535 arasında olabilir.
### Path(yol)
- Erişmek istediğiniz kaynağın konu veya adı.
### Query String (Sorgu dizisi)
- İstenen yola gönderilebilecek extra bilgi parçaları. Örneğin /blog?id=1 blog sayfasının yolunu söyler,  istediğiniz blog makalesi id numarası 1'dir.
### Fragment (Parça)
- Bu, istenen asıl sayfa içeriğinde referans konumdur. Bu yaygın olarak uzun içerikli sayfalarda kullanılır ve sayfanın belirli bir bölümünün doğrudan kendisine bağlı olabilir, bu nedenle kullanıcı sayfaya girer girmez görüntülenebilr.
## Bir İstek Yapmak
- Sadece bir satırda web sitesine istek yapmak mümkündür.
- "GET / HTTP/1.1"
- ![line](https://user-images.githubusercontent.com/86947080/184836241-71952d33-e528-4c3d-9e82-ab1c8a1bd7e3.png)
- Ama çok daha zengin web deneyimi için diğer verileride göndermeniz gerekir. Bu diğer veriler, başlıkların iletişim kurduğunuz web sunucusuna vermek için ek bilgiler içerdiği başlıklar olarak adlandırılır, ancak bu konuya başlık görevinde daha fazla gireceğiz.
- Example Request:
```
GET / HTTP/1.1
Host: tryhackme.com
User-Agent: Mozilla/5.0 Firefox/87.0
Referer: https://tryhackme.com/
```
- Bu isteği her satırını parçalayalım.
### Line 1
Bu istek GET isteği gönderiyor. (daha fazlası HTTP metotları başlığı altında), istek anasayfaya / ve web sunucusunun HTTP versiyon 1.1 kullandığını söylüyor.
### Line 2
Web sunucusuna tryhackme.com adresini istediğimiz söylüyoruz.
### Line 3
Web sunucusuna Firefox 87 versiyonun kullandığımız söylüyoruz.
### Line 4 
Web sunucusuna bize referans olan web sayfasının https://tryhackme.com olduğunu söylüyoruz.
### Line 5
HTTP istekleri her zaman boş satırla biter, bu web sunucusuna isteğin bittiği hakkında bilgi verir.
- Örnek Cevap
```
HTTP/1.1 200 OK
Server: nginx/1.15.8
Date: Fri, 09 Apr 2021 13:34:03 GMT
Content-Type: text/html
Content-Length: 98

<html>
<head>
    <title>TryHackMe</title>
</head>
<body>
    Welcome To TryHackMe.com
</body>
</html>
```
- Şimdi bu cevabın her satırını parçalayalım.
### Line 1 
HTTP 1.1, sunucunun kullandığı HTTP protokolünün sürümüdür ve ardından bu durumd isteğin başarıyla tamamlandığını bildiren "200 OK" HTTP Durum Kosu gelir.
### Line 2
Bu bize web sunucu yazılımını ve versiyonunu söyler.
### Line 3
Web sunucusunun son tarih zaman ve saat dilimi.
### Line 4
İçerik tipi başlığı, ziyaretçiye hangi tip bilgi göndereceğini söyler. HTML, görüntüler, videolar, pdf, XML gibi.
### Line 5
İçerik uzunluğu ziyaretçiye cevabın ne kadar uzun olduğunu söyler, böylelikle veri kaçırmadığımızı onaylarız.
### Line 6 
HTTP cevabı, cevabın sonunda boş satır içerir.
### Line 7-14
İstenen bilgiler, bu durumda ana sayfa.







