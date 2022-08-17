# Web Siteleri Nasıl Çalışır
## JavaScript
- JavaScript dünyadaki en yaygın kodlama dillerinden biridir ve sayfaları etkileşimli hale getirmeye izin verir. HTML içerik ve yapıyı oluşturmak için kullanılır, Javascript ise web sitenin işlevselliğini kontrol etmek için kullanılır. Javascript'siz, bir sayfa etkileşim içeren bir elemet içermez ve her zaman statik olarak kalır. JS sayfayı gerçek zamanlı ve dinamik bir şekilde günceller, sayfada belirli bir olay meydana geldiğinde (örneğin, bir kullanıcı bir düğmeyi tıklattığında) bir düğmenin stilini değiştirme veya hareketli animasyonları görüntüleme işlevi sağlar.
- JavaScript sayfanın kaynak koduna eklenir ve <script> etiketleri içine yüklenebilir veya src özelliği ile uzaktan dahil edilebilir:
- ```
  <script src="/location/of/javascript_file.js"></script>
  ```
- Aşağıdaki JavaScript kodu, sayfada "demo" kimliğine sahip bir HTML öğesi bulur ve öğenin içeriğini "Hack the Planet" olarak değiştirir:
- ```
  document.getElementById("demo").innerHTML = "Hack the Planet";
  ```
-HTML öğeleri, olay gerçekleştiğinde JavaScript'i çalıştıran "onclick" veya "onhover" gibi olaylara da sahip olabilir. Aşağıdaki kod, demo kimliğine sahip öğenin metnini Button Clicked olarak değiştirir:
- ```
  <button onclick='document.getElementById("demo").innerHTML = "Button Clicked";'>Click Me!</button>
  ```
- onclick olayları, doğrudan öğeler üzerinde değil, JavaScript komut dosyası etiketlerinin içinde de tanımlanabilir.
