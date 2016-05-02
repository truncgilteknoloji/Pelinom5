- Veritabanı yığın dosyası `(pelinom_bos.sql)` sunucuda oluşturulan veritabanının içerisine `execute` edilir. Daha sonra `bd.php `dosyasındaki veritabanı bağlantı değişkenleri tanımlanır.
```
$sunucu = "localhost";
$veritabani = "pelinom_bos";
$kullanici = "root";
$parola = "";
```
- HTML tasarımı yapılmış çalışma dosyası öncelikle ana dizine html dosyasındaki linklerin sağlıklı çalışacağı şekilde kopyalanır.
- Mevcut HTML dosyası PHP dosyasına dönüştürülür. Örneğin` tema.html` dosyası `tema.php `dosyasına dönüştürülür.  İçerik kodları iki parçaya bölünerek `start() `ve` finish()` fonksiyonları oluşturulur. 
`start();` fonksiyonu `header` 
`finish();` fonksiyonu `footer` 
alanını temsil eder. 
-
```
function start($c=array()) { 
///Döküman Başlangıç HTML Kodları
}
function finish() { 
///Döküman Bitiş HTML Kodları
}
```
- tema.php sayfasının en üst tarafına bilimum değişkenler dosyası (bd.php) include edilir.
`include("bd.php");`
- Ana sayfada gözükecek kodlar` index.php `sayfasına aktarılır.` index.php `sayfası` tema.php `sayfasından türeyen bir sayfadır. Türeyen sayfaların içeriği şu şekilde olmak durumundadır.
```
<?php 
include("tema.php");
start();
//İçerik kodları
finish();
?>
```



