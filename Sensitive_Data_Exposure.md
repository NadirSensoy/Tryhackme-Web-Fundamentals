# Web Nasıl Çalışır
## Hassas Verileri Açığa Çıkarma
- Bir web sitesi hassas verileri düzgün bir şekilde korumadığı veya silmediğinde hassas açık metin bilgileri son kullanıcıya ulaşır; genellikle sitenin frontend kısmında bulunur.
- Biz biliyoruz ki web siteleri birçok HTML öğesinden meydana geliyor, biz hepsini"viewing the page source" (sayfa kaynağını görüntüle) kısmından basit bir şekilde görüntüleyebiliriz. Bir web site geliştircisi kimlik bilgilerini, web sitesindeki gizli linkleri veya HTML ya da JavaScript içerisindeki diğer hassas bilgileri silmeyi unutmuş olabilir.
- ![html_source](https://user-images.githubusercontent.com/86947080/185056268-fa2fea36-5bac-4271-91e9-7f890cf0c163.png)
- Bir saldırganın bir web uygulamasının farklı bölümlerine erişimini ilerletmek için hassas bilgiler potansiyel olarak kullanılabilir. Örneğin, geçici oturum açma kimlik bilgilerine sahip HTML yorumları olabilir ve sayfanın kaynak kodunu görüntülediyseniz ve bunu bulduysanız, bu kimlik bilgilerini uygulamada başka bir yerde oturum açmak için kullanabilirsiniz (veya daha kötüsü, sitenin diğer arka uç bileşenlerine erişmek için kullanılır).
- Bir web uygulamasını güvenlik sorunları açısından değerlendirirken yapmanız gereken ilk şeylerden biri, açıkta kalan oturum açma kimlik bilgilerini veya gizli bağlantıları bulup bulamayacağınızı görmek için sayfa kaynak kodunu incelemektir. 
