# Detaylarıyla HTTP
## HTTP Durum Kodları
- Son bölümde bir HTTP sunucusu cevaplarını öğrendiniz. İlk satır her zaman istemciyi isteklerinin sonucu ve ayrıca potansiyel olarak nasıl ele alınacağı konusunda bilgilendiren bir durum kodu içerir. Bu durum kodları 5 farklı aralığa ayrılabilir:
### 100-199 Bilgilendirme Cevabı
Bunlar, ziyaretçiye talebinin ilk bölümünün kabul edildiğini ve talebinin geri kalanını göndermeye devam etmesi gerektiğini bildirmek için gönderilir. Bu kodlar artık çok yaygın değil.
### 200-299 Başarılı
Bu durum kodları aralığı, ziyaretçiye talebinin başarılı olduğunu söylemek için kullanılır.
### 300-399 Yeniden Yönlendirme
Bunlar, ziyaretçinin isteğini başka bir kaynağa yönlendirmek için kullanılır. Bu, farklı bir web sayfasına veya tamamen farklı bir web sitesine olabilir.
### 400-499 Ziyaretçi Hataları
İstemciye isteğiyle ilgili bir hata olduğunu bildirmek için kullanılır.
### 500-599 Sunucu Hataları
Bu, sunucu tarafından meydana gelen hatalar için ayrılmıştır ve genellikle sunucunun isteği yerine getirmesiyle ilgili oldukça büyük bir soorun olduğunu gösterir.
## Yaygın HTTP Durum Kodları
- Pek çok farklı HTTP durum kodu vardır ve bu, uygulamaların kendilerinin tanımlayabileceği gerçeğini içermiyor, muhtemel olarak karşılaşabileceğiniz en yaygın HTTP yanıtlarını gözden geçireceğiz.
- **200 - OK** : İstek başarıyla tamamlandı.
- **201 - Created** : Bir kaynak oluşturuldu (öreğin bir blog  ya da yeni kullanıcı)
- **301 - Permanent Redirect** : Bu, ziyaretçinin tarayıcısını yeni bir web sayfasına yönlendiri vya aram motorlarına sayfanın başka bir yere taşındığını ve bunun yerine oraya bakmalarını söyler.
- **302 - Temporary Redirect** : Yukarıdaki kalıcı yönlendirmeye benzer, ancak adından da anlaşılacağı gibi, bu yalnızca geçici bir değişikliktir ve yakın gelecekte tekrar değişebilir.
- **400 - Bad Request** : Bu, tarayıcıya isteklerinde bir şeylerin yanlış veya eksik olduğunu söyler. Bu, bazen, istenen web sunucusu kaynağı, istemcinin göndermediği belirli bir parametreyi bekliyorsa kullanılabilir.
- **401 - Not Authorised** : Web uygulamasıyla, çoğunlukla bir kullanıcı adı ve  parolayla yetkilendirmeden, şu anda bu kaynağı görüntülemenize izin verilmemektedir.
- **403 - Forbidden** : Giriş yapmış olsanız da olmasanız da bu kaynağı görüntüleme izniniz yok.
- **405 - Method Not Allowed** : Kaynak bu yöntem isteğine izin vermiyor; örneğin, bunun yerine bir POST isteği beklerken kaynağa /create-account'a bir GET isteği gönderirsiniz.
- **404 - Page Not Found** : İstediğiniz sayfa/kaynak mevcut değil.
- **500 - Internal Service Error** : Sunucu, isteğinizle ilgili olarak nasıl düzgün bir şekilde ele alınacağını bilmediği bir tür hatayla karşılaştı.
- **503 - Service Unavailable** : Bu sunucu, aşırı yüklendiğinden veya bakım nedeniyle kapalı olduğundan isteğinizi yerine getiremez.
