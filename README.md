# Tryhackme Web Fundementals (Türkçe Anlatım)
- Bu yolun amacı size web uygulamalarına nasıl saldıracağınızı öğretmektir. Web uygulamalarına başarılı bir şekilde saldırmak ve bunlardan yararlanmak için nasıl çalıştıklarını anlamanız gerekir. İlk bölüm (Web Temelleri) size bununla ilgili tüm ön gerekli bilgileri verecektir.

- İkinci bölüm (Güvenlik Araçları), hedeflerinizle etkileşim kurmak için Endüstri Standardı araçlarının nasıl kullanılacağını öğrenmeye odaklanır.

- Üçüncü bölüm (Güvenlik Açıkları), günümüzde web uygulamalarında bulunan çeşitli güvenlik açıklarını kapsar. Bu bölüm, bu güvenlik açıklarının temel nedenlerini gözden geçirecek ve size bunları kullanma konusunda uygulamalı deneyim sağlayacaktır.

- Son bölüm (Pratik Mükemmelleştirir) önceki bölümlerde öğrendiklerinizi uygulamanıza yardımcı olacaktır.

Bu yolu tamamladıktan sonra şunları yapabilmelisiniz:

1. web uygulamalarının nasıl çalıştığını anlamak
2. web uygulamalarına saldırırken endüstri standardı araçları kullanın
3. yaygın web güvenlik açıklarını açıklayın ve kullanın
4. bu bilgiyi diğer hedeflere uygulayın (bir röportajda veya profesyonel bir web uygulamaları güvenlik değerlendirmesi dahilinde)
## Web Nasıl Çalışır?
Daha iyi bir bilgisayar korsanı olmak için dünya çapında ağın altında yatan işlevleri ve onu neyin çalıştırdığını anlamak çok önemlidir.
### Ayrıntılarıyla DNS
DNS'in nasıl çalıştığını ve internet hizmetlerine erişim sağlarken nasıl yardımcı olduğunu öğrenin.
- [DNS Nedir](What_is_the_DNS.md)
- [Alan Adı Hiyerarşisi](Domain_Hierarchy.md)
- [Kayıt Çeşitleri](Record_Types.md)
- [Bir istek yapma](Making_A_Request.md)
### Ayrıntılarıyla HTTP
HTTP protokolünü kullanarak bir web sunucusundan nasıl içerik talep ettiğinizi öğrenin.
- [HTTPS Nedir](What_is_the_HTTP(S).md)
- [İstekler ve Cevaplar](Request_and_Responses.md)
- [HTTP Metotları](HTTP_Methods.md)
- [HTTP Durum Kodları](HTTP_Status_Codes.md)
- [Başlıklar](Headers.md)
- [Çerezler](Cookies.md)
### Web Siteleri Nasıl Çalışır
Bir web sitesini istismar etmeden önce nasıl çalıştıklarını bilmelisiniz.
- [Web Siteleri Nasıl Çalışır](How_Websites_Work.md)
- [HTML](HTML.md)
- [JavaScript](JavaScript.md)
- [Hassas Veri Açığa Çıkarma](Sensitive_Data_Exposure.md)
- [HTML Injection](HTML_Injection.md)
### Hepsini birleştir
En sevdiğiniz web sitelerine erişmenizi sağlamak için web'in tüm bileşenlerinin birlikte nasıl çalıştığını öğrenin.
- [Hepsini Birleştir](Putting_It_All_Together.md)
- [Diğer Bileşenler](Other_Components.md)
- [Web Sunucuları Nasıl Çalışır](How_Web_Servers_Work.md)

## Web Hacking'e Giriş
Uygulamalı olun, bugün sektörde görülen en popüler web uygulaması güvenlik açıklarından bazılarını öğrenin ve bunlardan yararlanın.
### Bir Uygulamada Gezinmek
Yalnızca tarayıcınızın geliştirici araçlarını kullanarak bir web uygulamasını güvenlik sorunları için manuel olarak inceleyin. Araç veya komut dosyası olmadan yalnızca tarayıcınızla bilgisayar korsanlığı yapın.
- [Bir Uygulamada Gezinmek](Walkin_An_Application.md)
- [Web Sitesini Keşfetmek](Exploring_The_Website.md)
- [Sayfa Kaynağını Görüntülemek](Viewing_The_Page_Source.md)
- [Geliştirici Araçlar - Inspector](Developer_Tools-Inspector.md)
- [Geliştirici Araçlar - Debugger](Developer_Tools-Debugger.md)
- [Geliştirici Araçlar - Network](Developer_Tools-Network.md)
### İçerik Keşfi
Bir web sunucusunda yeni güvenlik açıklarına yol açabilecek gizli veya özel içeriği keşfetmenin çeşitli yollarını öğrenin.
- [İçerik Keşfi Nedir](What_Is_Content_Discovery.md)
- [Manuel Keşif - Robots.txt](Manual_Discovery_Robots.txt.md)
- [Manuel Keşif - Favicon](Manual_Discovery_Favicon.md)
- [Manuel Keşif - HTTP Başlıkları](Manual_Discovery_HTTP_Headers.md)
- [Manuel Keşif - Framework Yığını](Manual_Discovery_Framework_Stack.md)
- [OSINT - Google Korsanlığı](OSINT_Google_Hacking.md)
- [OSINT - Wappalyzer](OSINT_Wappalyzer.md)
- [OSINT - Wayback Machine](OSINT_Wayback_Machine.md)
- [OSINT - Github](OSINT_Github.md)
- [OSINT - S3 Buckets](OSINT_S3_Buckets.md)
- [Otomatik Keşif](Automated_Discovery.md)
### Alt Domain Numaralandırma
Bir hedefin saldırı yüzeyini genişletmek için alt alanları keşfetmenin çeşitli yollarını öğrenin.
- [Bilgilendirme](Subdomain_Enumeration_Brief.md)
- [OSINT - SSL/TLC Sertifikaları](OSINT_SSL_TLS_Certificates.md)
- [DNS Bruteforce](DNS_Bruteforce.md)
- [OSINT - Sublist3r](OSINT_Sublist3r.md)
- [Sanal Hostlar](Virtual_Hosts.md)
### Kimlik Doğrulama Atlatma
- [Bilgilendirme](Authentication_Bypass_Brief.md)
- [Kullanıcı Adı Saydırma](Username_Enumeration.md)
- [Brute Force](Brute_Force.md)
### IDOR
***cooming soon***
### File Inclusion
***cooming soon***
### SSRF
***cooming soon***
### Cross-site Scripting
***cooming soon***
### Command Injection
***cooming soon***
### SQL Injection
- [Bilgilendirme](SQLi_Brief.md)
- [Veritabanı Nedir?](What_is_the_database.md)
