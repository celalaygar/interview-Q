## JAVASCRIPT_SORULARI_2
### == ve === arasındaki fark nedir?
```
İki eşittir ve üç eşittir arasındaki en temel fark, tip ve değer karşılaştırmasıdır.
Üç eşittir ile, iki değerin hem tipini hem de değerini karşılaştırırken
iki eşittir ile değerlerin tiplerini eşitleyerek sadece değer karşılaştırması yapılır.
```
### null ve undefined anahtar kelimeler arasında fark nedir?
```
undefined, bir değişkenin bildirildiği ancak henüz bir değer atanmamış olduğu anlamına gelir.
null ise bir atama değeridir, değişkene değersiz bir gösterim olarak atanabilir. typeof null bize nesne döndürür.
```
### JavaScript ve ECMA Script arasındaki fark nedir?
```
ECMAScript, betik dilleri için bir standarttır.
JavaScript gibi diller ECMAScript standardını temel alır.
ECMA Standardı, en bilinen JavaScript (Netscape) ve JScript (Microsoft) olmak üzere
çeşitli kaynak teknolojilerine dayanmaktadır.ECMA, Avrupa Bilgisayar Üreticileri Birliği anlamına gelir.
```
### call (), bind () ve apply () arasındaki fark nedir?
```
Call() fonksiyonu, verilen this anahtar değeriyle(obje) ve bağımsız olarak sağlanan
bağımsız argümanlarla bir fonksiyonu çağırır. Argümanlar fonksiyona tek tek gönderilir.
(Örnek: test(obj,arg1,arg2,arg3))
```
```
Apply() fonksiyonu, verilen this anahtar değeriyle(obje) ve bağımsız olarak sağlanan değişkenlerle
bir fonksiyonu çağırır. Argümanlar fonksiyona argüman listesi şeklinde gönderilir.
(Örnek: test(obj,[arg1,arg2,arg3]))
```
```
Bind() fonksiyonu, içine verilen objeye göre yeni bir fonksiyon kopyası yaratır.
Oluşan bu kopya fonksiyonu daha sonradan argüman listesi ile beraber gönderilen objeye kullanabiliriz.

```
