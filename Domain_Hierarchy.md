# Ayrıntılarıyla DNS
## Domain Hiyerarşisi

![domain_levels](https://user-images.githubusercontent.com/86947080/184388236-80bbe963-2ab0-4475-9559-32cfa4407c65.png)

### TLD(Top-Level Domain)
- TLD domain isminin en sağındaki kısımdır. Örneğin **tryhackme.com** daki **.com** TLD'dir.

- TLD iki çeşittir; gTLD (Generic Top Level Domain) ve ccTLD (Country Code Top Level Domain).

- gTLD kullanıcıya domain'in amacını ifade ediyor. Örneğin .com ticari amaçlı, .org organizasyon amaçlı, .edu eğitim amaçlı, .gov devlet amaçlı.

- ccTLD ise coğrafi amaç olarak kullanılmıştır. Örneğin .ca Kanada için, .co.uk Birleşik Krallık içindir.

- Böyle bir ihtiyaç olduğu için .online, .club, .website gibi pekçok gTLD ortaya çıkmıştır.

- Toplamda 2000'i aşkın TLD listesi için [buraya tıklayınız](https://data.iana.org/TLD/tlds-alpha-by-domain.txt) .

### Second-Level Domain
- tryhackme.com'u örnek alalım; **.com** kısmı TLD kısmıdır, **tryhackme** kısmı ise Second-Level Domain kısmıdır.

- Bir domain adı girerken Second-Level Domain kısmı 63 karaktere kadar sınırlıdır ve sadece a-z 0-9 arası ve kısa çizgi kullanılabilir.(kısa çizgi ardışık, başta ve sonda kullanılamaz.) 

### Subdomain
- Subdomain Second-Level Domain'in nokta ile ayrılmış olarak sol tarafında yer alır.

- Örneğin admin.tryhackme.com'da **admin** subdomain'in bir parçasıdır.

- Subdomain Secon-Level Domain ile aynı oluşturma kısıtlamasına sahip. 63 karaktere kadar sınırlıdır ve sadece a-z 0-9 arası ve kısa çizgi kullanılabilir.(kısa çizgi ardışık, başta ve sonda kullanılamaz.)

- Nokta ile ayırarak birden fazla subdomain kullanabilirsiniz. Örneğin jupiter.servers.tryhackme.com gibi.

- Ama uzunluk 253 karaktere kadar sınırlı.

- Domain adı için sınırsız sayıda subdomain oluşturabilirsiniz.
