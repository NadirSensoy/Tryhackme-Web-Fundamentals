# İçerik Keşfi
## OSINT - S3 Buckets
### S3 Buckets
- S3 Buckets, Amazon AWS tarafından sağlanan ve insanların HTTP ve HTTPS üzerinden erişilebilen bulutta dosyaları ve hatta statik web sitesi içeriğini kaydetmesine olanak tanıyan bir depolama hizmetidir. Dosyaların sahibi, dosyaları herkese açık, özel ve hatta yazılabilir hale getirmek için erişim izinleri ayarlayabilir. Bazen bu erişim izinleri yanlış ayarlanır ve yanlışlıkla halka açık olmaması gereken dosyalara erişime izin verir. 
- S3 klasörlerinin biçimi http(s)://{name}.s3.amazonaws.com şeklindedir; burada {name} sahibi tarafından belirlenir, örneğin tryhackme-assets.s3.amazonaws.com. S3 klasörleri, web sitesinin sayfa kaynağındaki, GitHub depolarındaki URL'leri bulmak ve hatta süreci otomatikleştirmek gibi birçok yolla keşfedilebilir. Yaygın bir otomasyon yöntemi, şirket adının ardından {name}-assets, {name}-www, {name}-public, {name}-private, vb. gibi ortak terimlerin kullanılmasıdır.
