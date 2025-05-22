# Site Yönetim Otomasyonu


Bu proje, site yöneticilerinin site yönetimlerini; sakinlerin de site ile ilgili işlemlerini kolay bir şekilde yapmasını sağlamak için geliştirilmiş web tabanlı bir  **Site Yönetim Otomasyon** sistemidir.




---


## Proje Özeti


- Yönetici paneli üzerinden yöneticiler duyuru oluşturma, sakin bilgilerini görme ve düzenleme, aidat takibi ve sakinlerin başvurularını görüntüleme işlemlerini yapabilirler.
- Site sakinleri sistem üzerinden duyuruları görüntüleyebilir ve başvuruda bulunabilirler.
- Veritabanı olarak **MySQL**, sunucu taraflı programlama dili olarak **PHP**, arayüz için **HTML & CSS** sunucu platformu olarak da  **XAMPP** kullanılmıştır.


---


## Geliştirme Ortamı


- **PHP** (sürüm 7.4+ önerilir)
- **MySQL** (phpMyAdmin ile yönetim)
- **XAMPP** (Apache ve MySQL sunucuları için)
- **Visual Studio Code** (veya benzeri bir IDE)


---


##  Kurulum ve Çalıştırma


### 1. XAMPP Kurulumu


1. [XAMPP İndirme Sayfası](https://www.apachefriends.org/index.html) üzerinden işletim sisteminize uygun XAMPP sürümünü indirin.
2. Kurulumu yaparken yetki sorunlarını önlemek için **Program Files (C:\Program Files)** gibi klasörler yerine,  `C:\xampp` (önerilen) klasörüne kurmanız tavsiye edilir.
3. Kurulum tamamlandıktan sonra **XAMPP Control Panel**'i açın ve **Apache** ile **MySQL** servislerini **Start** butonu ile başlatın.


### 2. Proje Dosyalarının Yerleştirilmesi


1. Bu GitHub reposunu bilgisayarınıza ZIP olarak indirin veya Git ile klonlayın:
   ```bash
   git clone https://github.com/gulni-hal/SiteYonetimiOtomasyonu.git
   ```
2. Çıkan klasörü `C:\xampp\htdocs` dizinine taşıyın*:
   ```
   Örnek: C:\xampp\htdocs\site_yonetim
   ```


*: `htdocs` klasörü XAMPP'ın web kök dizini olduğundan projeyi bu dizine taşımazsanız `localhost` üzerinden erişemezsiniz.


### 3. Veritabanını Yükleme


1. Tarayıcıda `http://localhost/phpmyadmin` adresine gidin, bu adres MySQL veritabanınızı yönetmenizi sağlar.
2. Yeni bir veritabanı oluşturun (örneğin: `site_yonetim_db`).
3. Bu repoda yer alan `22_sql_betikleri.txt` dosyasını indirin ve phpMyAdmin > site_yonetim > İçe Aktar kısmından içeri aktarın.
4. Tablolarınız oluşmuş olacaktır.


### 4. Veritabanı Bağlantısı


`baglanti.php` dosyasında veritabanı bağlantısı aşağıdaki gibidir:


```php
$servername = "localhost";
$username = "root";
$password = "";
$database = "site_yonetim";


$conn = new mysqli($servername, $username, $password, $database);


```


- Eğer veritabanı adınızı farklı verdiyseniz `site_yonetim` kısmını değiştirin.
- MySQL şifresi belirlediyseniz, `"root"` (kullanıcı adı) ve `""` (şifre) kısmını değiştirin.


### 5. Sistemi Başlatma


Tarayıcınıza aşağıdaki adresi yazarak projeyi başlatabilirsiniz:


```
http://localhost/site_yonetimi/
```


### 6. Test Kullanıcı Bilgileri


**Yöneticiler Girişi:**


A bloğu yöneticisi olarak giriş yapmak için
- Kullanıcı Adı: `nilayycannA`
- Parola: `niloyaniloyaa`


B bloğu yöneticisi olarak giriş yapmak için
- Kullanıcı Adı: `gulni.eruslu`
- Parola: `Parola123.`


C bloğu yöneticisi olarak giriş yapmak için
- Kullanıcı Adı: `egedemirC`
- Parola: `egeegeege`
değerlerini kullanabilirsiniz.


**Sakinler Girişi:**


A bloğu sakini olarak giriş yapmak için
- Kullanıcı Adı: `deryaaozturkkA`
- Parola: `deryamıdevamı05`


B bloğu sakini olarak giriş yapmak için
- Kullanıcı Adı: `SuzanEr`
- Parola: `Ay_Rif60`


C bloğu sakini olarak giriş yapmak için
- Kullanıcı Adı: `ilkersahinC`
- Parola: `ilkerpass`
değerlerini kullanabilirsiniz.




---


## Proje Yapısı


```
 site-yonetimi
 ┣ aidat_takibi.php
 ┣ baglanti.php
 ┣ cikis.php
 ┣ db.php
 ┣ duyuru_ekle.php
 ┣ duyurular.php
 ┣ index.php
 ┣ oneri_sikayet.php
 ┣ sakin_basvuru.php
 ┣ sakin_duzenle.php
 ┣ sakin_ekle.php
 ┣ sakin_giris.php
 ┣ sakin_sil.php
 ┣ sakinleri_listele.php
 ┣ yonetici_giris.php
 ┣ yonetici_panel.php
 ┣ 📄 css/
 ┃  ┗ 📄 style.css
```


---


##  Kullanılan Teknolojiler


| Teknoloji | Açıklama |
|----------|----------|
| PHP | Sunucu taraflı programlama dili |
| MySQL | Veritabanı yönetim sistemi |
| HTML/CSS | Web sayfası yapısı ve stil |
| XAMPP | Apache ve MySQL sunucusu |
| phpMyAdmin | Veritabanı arayüzü |
| Git & GitHub | Sürüm kontrolü ve proje teslimi |


---


## Geliştiriciler


- **Gülnihal ERUSLU** – [gulni-hal]
- **Fatma Nilay Süzer** – [NilaySuzer]
- **Cüneyt Şendur** – [cuneytsendurr]


---
