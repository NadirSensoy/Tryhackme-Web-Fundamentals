# Alt Alan Adı Numaralandırma
## Sanal Host'lar
- Bazı alt alanlar, bir web uygulamasının veya yönetim portallarının geliştirme sürümleri gibi, genel olarak erişilebilir DNS sonuçlarında her zaman barındırılmaz. Bunun yerine, DNS kaydı özel bir DNS sunucusunda tutulabilir veya geliştiricinin makinelerinde alan adlarını eşleyen /etc/hosts dosyasına (veya Windows kullanıcıları için c:\windows\system32\drivers\etc\hosts dosyasına) kaydedilebilir. IP adresleri.
- Web sunucuları, bir istemciden bir web sitesi istendiğinde, bir sunucudan birden çok web sitesini barındırabildiğinden, sunucu, istemcinin Host başlığından hangi web sitesini istediğini bilir. Bu ana bilgisayar başlığında değişiklik yaparak ve yeni bir web sitesi keşfedip keşfetmediğimizi görmek için yanıtı izleyerek kullanabiliriz.
- DNS Bruteforce'da olduğu gibi, bu işlemi yaygın olarak kullanılan alt alan adlarının bir kelime listesini kullanarak otomatikleştirebiliriz.
- Aşağıda örnek komutlar gösteriliyor:
```
user@machine$ ffuf -w /usr/share/wordlists/SecLists/Discovery/DNS/namelist.txt -H "Host: FUZZ.acmeitsupport.thm" -u http://MACHINE_IP
```
- Yukarıdaki komut, kullanacağımız kelime listesini belirtmek için -w anahtarını kullanır. -H anahtarı bir başlık ekler/düzenler (bu örnekte, Host başlığı), bir alt alanın normalde gideceği alanda FUZZ anahtar kelimesine sahibiz ve burası, kelime listesindeki tüm seçenekleri deneyeceğimiz yer.
- Yukarıdaki komut her zaman geçerli bir sonuç üreteceği için çıktıyı filtrelememiz gerekiyor. Bunu -fs anahtarı ile sayfa boyutu sonucunu kullanarak yapabiliriz. {size} öğesini önceki sonuçtan en çok ortaya çıkan boyut değeriyle değiştirerek aşağıdaki komutu düzenleyin ve AttackBox'ta deneyin.
```
user@machine$ ffuf -w /usr/share/wordlists/SecLists/Discovery/DNS/namelist.txt -H "Host: FUZZ.acmeitsupport.thm" -u http://MACHINE_IP -fs {size}
```
- Bu komut, ffuf'a belirtilen boyuttaki sonuçları yoksaymasını söyleyen -fs anahtarı dışında, birincisine benzer bir sözdizimine sahiptir.
- Yukarıdaki komut, daha önce karşılaşmadığımız iki olumlu sonucu ortaya çıkarmalı.
