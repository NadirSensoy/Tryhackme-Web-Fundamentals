# Hepsini Birleştirmek
## Web Sunucuları Nasıl Çalışır
### Web Suncusu Nedir
- Bir web sunucusu, gelen bağlantıları dinleyen ve ardından web içeriğini istemcilerine iletmek için HTTP protokolünü kullanan bir yazılımdır. Karşılaşacağınız en yaygın web sunucusu yazılımı Apache, Nginx, IIS ve NodeJS'dir. Bir Web sunucusu, yazılım ayarlarında tanımlanan kök dizininden dosyaları teslim eder. Örneğin, Nginx ve Apache, Linux işletim sistemlerinde /var/www/html ile aynı varsayılan konumu paylaşır ve IIS, Windows işletim sistemleri için C:\inetpub\wwwroot kullanır. Örneğin, http://www.example.com/picture.jpg dosyasını talep ettiyseniz, /var/www/html/picture.jpg dosyasını yerel sabit sürücüsünden gönderir.
### Sanal Hostlar
- Web sunucuları, farklı alan adlarına sahip birden çok web sitesini barındırabilir; Bunu başarmak için sanal ana bilgisayarlar kullanırlar. Web sunucusu yazılımı, HTTP başlıklarından istenen ana bilgisayar adını kontrol eder ve bunu sanal ana bilgisayarlarıyla eşleştirir (sanal ana bilgisayarlar yalnızca metin tabanlı yapılandırma dosyalarıdır). Bir eşleşme bulursa, doğru web sitesi sağlanacaktır. Eşleşme bulunamazsa, bunun yerine varsayılan web sitesi sağlanacaktır.
- Sanal Ana Bilgisayarlar, kök dizinlerini sabit sürücüdeki farklı konumlara eşleyebilir. Örneğin, bir.com /var/www/website_one ile eşlenir ve iki.com /var/www/website_two ile eşlenir
- Bir web sunucusunda barındırabileceğiniz farklı web sitelerinin sayısında bir sınırlama yoktur.
### Statik ve Dinamik İçerik
- Statik içerik adından da anlaşılacağı gibi hiç değişmeyen içeriktir. Bunun yaygın örnekleri resimler, javascript, CSS vb.'dir, ancak asla değişmeyen HTML'yi de içerebilir. Ayrıca, bunlar üzerinde hiçbir değişiklik yapılmadan doğrudan web sunucusundan sunulan dosyalardır.
- Dinamik içerik ise farklı isteklerle değişebilen içeriktir. Örneğin, bir blog alın. Blogun ana sayfasında, size en son girişleri gösterecektir. Yeni bir giriş oluşturulursa, ana sayfa en son girişle güncellenir veya ikinci bir örnek, bir blogdaki bir arama sayfası olabilir. Hangi kelimeyi aradığınıza bağlı olarak, farklı sonuçlar görüntülenecektir.
- Sonunda gördüğünüz şeydeki bu değişiklikler, programlama ve komut dosyası dillerinin kullanımıyla Backend olarak adlandırılan şeyde yapılır. Backend denir çünkü yapılanların hepsi perde arkasında yapılır. Web sitelerinin HTML kaynağını görüntüleyemez ve Arka Uçta neler olduğunu göremezsiniz, HTML ise Arka Uçtan yapılan işlemin sonucudur. Tarayıcınızda gördüğünüz her şeye Ön Uç denir.
### Komut Dosyası ve Backend Dilleri
- Bir backend dilinin başarabileceklerinin çok fazla bir sınırı yoktur ve bunlar bir web sitesini kullanıcı için etkileşimli yapan şeydir. Bu dillerin bazı örnekleri (belirli bir sırayla :p değil) PHP, Python, Ruby, NodeJS, Perl ve daha pek çok dildir. Bu diller veritabanlarıyla etkileşime girebilir, harici hizmetleri çağırabilir, kullanıcıdan gelen verileri işleyebilir ve çok daha fazlasını yapabilir. Bunun çok basit bir PHP örneği, http://example.com/index.php?name=adam web sitesini istemeniz olabilir.
- index.php şu şekilde oluşturulmuşsa:
- ```
  <html><body>Hello <?php echo $_GET["name"]; ?></body></html>
  ```
- İstemciye aşağıdaki çıktıyı verir:
- ```
  <html><body>Hello adam</body></html>
  ```
- İstemcinin Arka Uçta olduğu için herhangi bir PHP kodu görmediğini fark edeceksiniz. Bu etkileşim, daha sonraki modüllerde öğreneceğiniz gibi, güvenli bir şekilde oluşturulmamış web uygulamaları için çok daha fazla güvenlik sorunu açar.
