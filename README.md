# Raspberry-pi-Dark-Web-Server-

* Merhaba tor üzerinden bir dark web sunucusu kurmayı göstericem. Bu sunucu için sabit ip veya modem üzerine 80 port u açmamıza gerek yok ve normal bir sunucu için lazım olan şeylerin çoğuna ihtiyacınız olmuyor. Bu sunucu sadece tor da kullana bilirsiniz. Neden dark web de bir sunucu açmak istedim çünki sabit ip için ücretlendirme yapılıyor ve normal bir sunucuya ihtiyacım yoktu. Bu sunucu da olan trafiği "prensipte" kimse dinliyemiyor çünki bütün trafik encrypted lanmış olduğu için biraz daha güvenili ve gizli oluyor. Hadi kuruluma başlayalım.

* Öncelikle terminali açıyoruz.

* Sonra tor u kuruyoruz. Kurmak içinde "sudo apt install tor" yazıp enter a basıyoruz. Şifre sorarsa şifremizi giriyoruz.

![Ekran Alıntısı11](https://user-images.githubusercontent.com/95309199/145665690-a6645de1-a1d6-4a16-8a99-d56c79334990.PNG)



![Ekran Alıntısı22](https://user-images.githubusercontent.com/95309199/145665823-87bb3708-f01b-40b5-9a54-021fa5974639.PNG)

* Tor umuz çalışıyormu kontrol deiyoruz. Onun içinde "sudo tor status" yazıyoruz. Yeşil yazı ile "active" yazıyorsa çalışıyor demektir.


![Ekran Alıntısı33](https://user-images.githubusercontent.com/95309199/145665914-a82146e2-7e07-40ce-a50c-e11b9985bac7.PNG)

* Ayarlarımızı yapmak için sudo nano /etc/tor/torrc yazıp enter a basıyoruz.


![Ekran Alıntısı44](https://user-images.githubusercontent.com/95309199/145665957-5b6ff544-0584-4b71-b1c5-851f57169e8a.PNG)

* Ayar sayfamız açılıyor sayfamızdan "HiddenServiceDir ve HiddenServicePort" un yanlarındaki "Hashtag" leri kaldırıyoruz. Ve "ctrl x" yapıyoruz kayıt edilsinmi diye soruyor "y" ye basıyoruz saonrada enter a basınca kayıt edip kontrol paneline atıyor.


![Ekran Alıntısı55](https://user-images.githubusercontent.com/95309199/145666116-4c024740-a8a1-413e-acfc-d2f18ef5d028.PNG)

* Tor umuzu kapatıp açmamız gerekiyor onun içinde "sudo service tor stop" yazıp kapatıyoruz. Sonra "sudo service tor start" yazıp yeniden çalıştırıyoruz. sonra tor umuz çalışıyormu kontrol deiyoruz. Onun içinde "sudo tor status" yazıyoruz. Yeşil yazı ile "active" yazıyorsa çalışıyor demektir.


![Ekran Alıntısı66](https://user-images.githubusercontent.com/95309199/145666219-a0f8cc6b-3ae1-417d-8582-4faccaea771b.PNG)

* 80 port una uygun bir web sunucusu kurmamız gerekiyor. En çok tercih edilen "nginx" i kuruyorum. Kurulum içinde "sudo apt install nginx" yazıp enter a basıyoruz. Şifre sorarsa şifremizi giriyoruz.


* Şuan vpn en den dinleyen vpn en den broadcast eden bir sunucu kurmuş olduk. Şimdi ise bu sunucuya tor üzerinden bağlanmak için adresimizi ögrenmemiz gerekiyor.



* Adresimizi öğrenmek için "sudo cat /var/lib/tor/hidden_service/hostname" yazıyoruz ve enter a basıyoruz ve alt satıra düşüyor sonu ".onion" ile bitiyor. Adresimizin bukadar uzun olmasının sebebi 56 bit lik olduğu için daha güvenilir.

![Ekran Alıntısı88](https://user-images.githubusercontent.com/95309199/145666717-2f81ae3f-f816-4123-bbcc-568447d729f3.PNG)

* Şimdi ise adresimizi istediğimiz bir bigisayar veya başka bir yerden erişe biliyoruz. Erişmek için tor browser veya tor a bağlanan başka bir browser a adresimizi yapıştırıyoruz ve ekrana "Welcome to nginx"  yazıyorsa başarmışız demektir. Şimdi "Dark web" te bir sunucun var demektir istediğin gibi kullana bilirsin.
