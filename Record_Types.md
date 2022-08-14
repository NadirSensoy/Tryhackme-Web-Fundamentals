# Ayrıntılarıyla DNS
## DNS Record Types (Türkçe anlatım)
- DNS sadece web siteleri için değildir. Birden çok DNS kaydetme çeşidi vardır. Şimdi kaşılaşabileceiğiniz en yaygın türlerin üzerinden geçicez.

### A Record
- Bu kayıtlar IPv4 için çözümlenir. Örneğin 104.26.10.229

### AAAA Record
- Bu kayıtlar IPv6 için çözümlenir. Örneğin 2606:4700:20::681a:be5

### CNAME Record
- Bu kayıtlar diğer domain adları için çözümlenir. Örneğin TryHackMe'nin online satış mağazası, store.tryhackme.com CNAME kaydı döndüren bir shops.shopify.com adlı bir subdomain adı vardır.

### MX Record
-Bu kayıtlar sorguladığınız domain için e-postayı işleyen sunucuların adresine çözümlenir.

-Örneğin tryhackme.com için MX record yanıtı **alt1.aspmx.l.google.com** gibidir.

### TXT Record
- TXT kayıtları herhangibir metin tabanlı verinin kaydedilebileceği serbest metin alanlarıdır.

- TXT kayıtların birçok kullanımı vardır, ama en yaygın olanlar domaine e-posta gönderme yetkisine sahip sunucuları listelemek olabilir. Bu istenmeyen ve sahte e-postalara karşı mücadelede yardımcı olabiliyor.

- Aynı zamanda üçüncü taraf hizmetlerine kayıt yaparken domain adı sahibini doğrulamakda kullanılabilirler.
