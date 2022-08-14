# Ayrıntılarıyla DNS
## Making A Request (Türkçe anlatım)
1. Bir alan adı isteği attığınızda bilgisayarınız ilk olarak adresi yakın zamanda arayıp aramadığınızı görmek için yerel önbelleğini kontrol eder; değilse, Recursive (Özyinelemeli) DNS sunucunuza bir istek yapılacaktır.

2. Recursive DNS sunucusu genellikle ISS'iniz (İnternet Servis Sağlayıcı) tarafından temin edilir. Ama aynı zamanda kendinizinkini de seçebilirsiniz. Bu sunucu aynı zamanda son zamanlarda baktığın alan adlarının yerel önbelleğine sahiptir. Eğer yerelde bir sonuç bulunursa, bu sonuç senin bilgisayarında gönderilir. Ve senin isteğin burada biter. (Bu popüler ve yoğun istek olunan hizmetler içindir. Örneğin Google-Facebook-Twitter). Eğer istek yerel önbellekte bulunamadıysa o zaman doğru cevabı bulmak için yolculuk başlar. İlk olarak internetin root DNS server'inden başlar.

3. Root (kök) server internetin DNS omurgası gibi davranır. Onun işi doğru TLD (Top-Level Domain)'e yönlendirmektir ve isteğine göre değişir. Örneğin sen www.tryhackme.com adresine istek attıysan, root server onun TLD'sini .com olarak tanır, ve sizi .com adresleriyle ilgilenen doğru TLD sunucusuna yönlendirir.

4. TLD sunucusu, DNS isteğini yanıtlayacak yetkili sunucunun nerede bulunacağına ilişkin kayıtları tutar. Yetkili sunucu sıklıkla alan adı içinisim sunucusu olarak da bilinir. Örneğin tryhackme.com için isim sunucusu kip.ns.cloudflare.com ve uma.ns.cloudflare.com 'dur. Sıklıkla bir alan adı için birden çok isim sunucusu bulursunuz. Çünkü birinin düşmesi durumunda diğeri yedek olarak hareket eder.

5. Bir yetkili DNS sunucusu DNS kayıtlarını özel alan adı olarak kaydetmekle ve alan adı DNS kayıtlarınızda herhangibir güncellemenin yapılmasından sorumludur. Kayıt türüne bağlı olarak, DNS kaydı daha sonra, yerel bir kopyanın gelecekteki istekler için önbelleğe alınacağı ve ardından isteği yapan orijinal istemciye geri iletileceği Özyinelemeli DNS Sunucusuna geri gönderilir. Tüm DNS kayıtları bir TTL (Time To Live) değeri ile gelir. Bu saniyelerle temsil edilen değer, tekrar aramanız gerekene kadar yanıtın yerel olarak kaydedilmesi gereken değerdir. Önbelleğe alma, bir sunucuyla her iletişim kurduğunuzda bir DNS isteğinde bulunma zorunluluğundan tasarruf sağlar.





![dns](https://user-images.githubusercontent.com/86947080/184467221-5997f2bb-79a3-4328-8b13-5d3308e6b31c.png)
