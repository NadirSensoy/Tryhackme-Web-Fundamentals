# İçerik Keşfi 
## Otomatik Keşif
### Otomatik Keşif Nedir
- Otomatik keşif, içeriği manuel olarak yapmak yerine keşfetmek için araçları kullanma sürecidir. Bu süreç, genellikle bir web sunucusuna yüzlerce, binlerce ve hatta milyonlarca istek içerdiğinden otomatikleştirilmiştir. Bu istekler, bir web sitesinde bir dosya veya dizinin bulunup bulunmadığını kontrol ederek daha önce varlığından haberdar olmadığımız kaynaklara erişmemizi sağlar. Bu işlem, kelime listeleri adı verilen bir kaynak kullanılarak mümkün kılınmıştır.
### Wordlist Nedir
- Kelime listeleri, yalnızca yaygın olarak kullanılan kelimelerin uzun bir listesini içeren metin dosyalarıdır; birçok farklı kullanım durumunu kapsayabilirler. Örneğin, bir parola sözcük listesi en sık kullanılan parolaları içerirken, bizim durumumuzda içerik arıyoruz, bu nedenle en sık kullanılan dizin ve dosya adlarını içeren bir listeye ihtiyacımız var. THM AttackBox'a önceden yüklenmiş kelime listeleri için mükemmel bir kaynak, Daniel Miessler'in küratörlüğünü yaptığı https://github.com/danielmiessler/SecLists'dir.
### Otomasyon Araçları
- Tüm özellikleri ve kusurları ile mevcut birçok farklı içerik keşif aracı olmasına rağmen, saldırı kutumuza önceden yüklenmiş üç tanesini ele alacağız, ffuf, dirb ve gobuster.
- AttackBox'ta Acme BT Desteği web sitesini hedefleyen aşağıdaki üç komutu yürütün ve hangi sonuçları aldığınızı görün.
- ffuf kullanırken:
```
user@machine$ ffuf -w /usr/share/wordlists/SecLists/Discovery/Web-Content/common.txt -u http://MACHINE_IP/FUZZ
```
- dirb kullanırken:
```
user@machine$ dirb http://MACHINE_IP/ /usr/share/wordlists/SecLists/Discovery/Web-Content/common.txt

```
- Gobuster kullanırken:
```
user@machine$ gobuster dir --url http://MACHINE_IP/ -w /usr/share/wordlists/SecLists/Discovery/Web-Content/common.txt

```
