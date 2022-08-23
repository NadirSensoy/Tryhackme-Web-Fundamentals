# Kimlik Doğrulama Atlatma
## Brute Force (Kaba Kuvvet)
- Önceki görevde oluşturduğumuz valid_usernames.txt dosyasını, şimdi oturum açma sayfasında (http://MACHINE_IP/customers/login) bir kaba kuvvet saldırısı girişiminde bulunmak için kullanabiliriz.
- Kaba kuvvet saldırısı, yaygın olarak kullanılan parolaların bir listesini tek bir kullanıcı adına veya bizim durumumuzda olduğu gibi bir kullanıcı adları listesine karşı deneyen otomatik bir işlemdir.
- Bu komutu çalıştırırken, terminalin valid_usernames.txt dosyasıyla aynı dizinde olduğundan emin olun.
```
user@tryhackme$ ffuf -w valid_usernames.txt:W1,/usr/share/wordlists/SecLists/Passwords/Common-Credentials/10-million-password-list-top-100.txt:W2 -X POST -d "username=W1&password=W2" -H "Content-Type: application/x-www-form-urlencoded" -u http://MACHINE_IP/customers/login -fc 200
```
- Bu ffuf komutu, Görev 2'deki öncekinden biraz farklıdır. Daha önce, kelime listelerinden gelen verilerin istekte nereye ekleneceğini seçmek için FUZZ anahtar sözcüğünü kullanıyorduk, ancak birden fazla kelime listesi kullandığımız için, kendi FUZZ anahtar kelimesini kullanıyoruz. Bu örnekte, geçerli kullanıcı adları listemiz için W1'i ve deneyeceğimiz şifreler listesi için W2'yi seçtik. Birden çok kelime listesi yeniden -w argümanıyla belirtilir, ancak virgülle ayrılır. Olumlu bir eşleşme için, 200'den farklı bir HTTP durum kodunu kontrol etmek için -fc argümanını kullanıyoruz.
