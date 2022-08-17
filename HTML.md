# How Websites Work
## HTML
- HTML, web siteleri oluşturmak ve yapılarını tanımlamak içindir.
- CSS, Stil seçenekleri ekleyerek web sitelerinin güzel görünmesini sağlamak içindir.
- JavaScript, etkileşimi kullanarak karmaşık özellikleri sayfalara uygulayın.
- **H**yper**T**ext**M**arkup**L**anguage (HTML) websitelerinin yazıldığı dildir. Elementler (Aynı zamanda tag olarak da bilinirler) HTML bloklarını oluştururlar ve içeriklerin nasıl görüneceğini tarayıcıya söylerler. Aşağıda gösterilen kırpılmış kod parçası basit bir HTML dökümanıdır. Bu yapı her websitesinde aynıdır.
- ![example_html](https://user-images.githubusercontent.com/86947080/184975657-4e46725c-427a-4472-afca-76d26a7dd62f.png)
- HTML yapısı (SS'de görüldüğü gibi) aşağıdaki bileşenlere sahiptir.
- `<!DOCTYPE html>` sayfanın HTML5 sayfası olduğunu tanımlar. Bu farklı tarayıcılar arasında standartlaşmaya yardım eder ve yorumlaması için tarayıcıya HTML5 kullanmasını söyler.
- `<html>` elementi HTML sayfasının kök elementidir. Diğer tüm elementler bundan sonra gelir.
- `<head>` sayfa ile ilgili bilgileri içerir.(sayfa başlığı gibi)
- <body> HTML sayfasının gövde kısmını tanımlar. Sadece body elementinin içerisinde olanlar taryıcıda gözükür.
- `<h1>` büyük başlık olarak tanımlar.
- `<p>` paragraf olarak tanımlar.
- Farklı amaçlar için birçok element vardır. Öeneğin butonlar için elementler vardır. (`<button>`),görüntüler için (`<img>`) listeler ve daha fazlası..
- Tag'ler özellikler içerebilir, örneğin class özelliği bir öğeye stil vermek için kullanılabilir. ( örneğin tag'e farklı bir renk vermek) `<p class="bold-text">` veya src özelliği görüntüler üzerinde görüntünün konumunu belirtmek için kullanılır. `<img src="img/cat.jpg">`. Bir element birden fazla her biri birbirinden benzersiz özelliklere sahip olabilir.Örneğin `<p attribute1="value1" attribute2="value2">`.
- Elementler ayrıca id özelliğine de sahip olabilir. `(p id="example">)`, bu element benzersiz bir özelliğe sahiptir. class özelliğine benzemez, birçok element aynı class'a sahip olabilir. Ama benzersiz bir şekilde tanımlamak için bir öğenin farklı kimliklere (id) sahip olması gerekir. Element kimlikleri (id), stil oluşturmak ve onu JavaScript ile tanımlamak için kullanılır.
