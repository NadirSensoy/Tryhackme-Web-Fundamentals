# Detaylarıyla HTTP
## Başlıklar
- Başlıklar, istek yaparken web sunucusuna gönderebileceğiniz ek veri bitleridir.
- Bir HTTP isteğinde bulunurken kesinlikle üstbilgi gerekmese de, bir web sitesini düzgün bir şekilde görüntülemeyi zor bulacaksınız.
### Yaygın İstek Başlıkları 
- Bunlar, istemciden (genellikle tarayıcınız) sunucuya gönderilen başlıklardır.
- **Host** : Bazı web sunucuları birden fazla web sitesi barındırır, bu nedenle ana bilgisayar başlıklarını sağlayarak hangisine ihtiyacınız olduğunu söyleyebilirsiniz, aksi takdirde sunucu için varsayılan web sitesini alırsınız.
- **User-Agent** : Bu, tarayıcı yazılımınız ve sürüm numaranızdır ve web sunucusuna, tarayıcı yazılımınızın web sitesini tarayıcınız için uygun şekilde biçimlendirmesine yardımcı olduğunu ve ayrıca bazı HTML, JavaScript ve CSS öğelerinin yalnızca belirli tarayıcılarda mevcut olduğunu söyler.
- **Content-Lenght : Bir form gibi bir web sunucusuna veri gönderirken, içerik uzunluğu web sunucusuna web isteğinde ne kadar veri bekleyeceğini söyler. Bu şekilde sunucu herhangi bir verinin eksik olmadığından emin olabilir.
- **Accept-Encoding : Web sunucusuna, tarayıcının ne tür sıkıştırma yöntemlerini desteklediğini söyler, böylece veriler internet üzerinden iletilirken daha küçük hale getirilebilir.
- **Cookie** : Bilgilerinizi hatırlamanıza yardımcı olmak için sunucuya gönderilen veriler (daha fazla bilgi için çerez bölümüne bakın).
### Yaygın Yanıt Başlıkları
- Bunlar, bir istekten sonra sunucudan istemciye döndürülen başlıklardır.
- **Set-Cookie** : Her istekte web sunucusuna geri gönderilen saklanacak bilgiler (daha fazla bilgi için çerezler görevine bakın).
- **Cache-Control** : Yanıtın içeriğinin, tekrar istemeden önce tarayıcının önbelleğinde ne kadar süre saklanacağı.
- **Content-Type** : Bu, istemciye ne tür verilerin döndürüldüğünü, yani HTML, CSS, JavaScript, Görüntüler, PDF, Video vb. söyler. Tarayıcı, içerik türü başlığını kullanarak verileri nasıl işleyeceğini bilir.
- **Content-Encoding** : Verileri internet üzerinden gönderirken küçültmek için sıkıştırmak için hangi yöntem kullanılmıştır.
