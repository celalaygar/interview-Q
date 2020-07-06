## JAVA Q
### Thread.yield()
```
Current da çalışan thread ın geçici olarak durmasına sebeb olur. Diğer thread lerin çalışmasına izin verir.
```
### Thread.join() method waits for this thread to die.
```
JOİN() methodu çalışan thread ölmesini bekler. çalışan thread işini bitirene kadar çalışır.
bir thread işlemini bitirmeden diğer bir thread çalışması engellenir.
```
### synchronized
```
Basitçe, aynı anda çalışan birden fazla (thread) veya işlemin (process) sıralı olmasını ve birbiri ile iletişim halinde 
çalışmasını sağlar. Bir methodda tanımladığımız zaman o method içerisine bir anda sadece bir thread in girmesi ve 
kullanmasına izin verir. 2 thread in aynı anda synchronized edilmiş bir methodu kullanmasına izin verilmez.
```
### SET
```
Set Interface'ini kullanan sınıfların aynı objeden sadece bir tane saklama imkanı olur. 
Aynı objeden 2 tanesi SET içerisinde tutulmaz. 
Kendisine verilen elemanların her birinde sadece bir tanesini tutar. Kopya ya da
tekrarlanan elemanları barındırmaz.
```
### RuntimeException
```
RuntimeException, Java Virtual Machine'nın normal operasyonlar yani çalışma sırasında gerçekleşen exception'lardır.
NullPointerException, Java'da bir RuntimeException'dır. 
```
### Exception Sınıfı:
```
ClassNotFoundException: Olmayan bir dosyaya erişme istediği durumlarını inceler.
IOException: Giriş çıkış işlemlerindeki istenmeyen durumları inceler.
RunTimeException: Çalışma zamanı hatalarını inceler.
AritmeticException: Aritmetik hataları inceler.
NullPointerException: Herhangi bir nesneye null referanslı bir değişken ile ulaşılmaya çalışılan durumlarda fırlatılır.
IllegalArgumentException: Metotlara geçersiz argüman atamalarında fırlatılır.
```
### binary search
Binary Search algoritmasında dizi her adımda ikiye bölünür. Mantığı şu şekildedir.
```

- Dizinin ortasındaki elemanı bul eğer aradığın elemana eşitse index’i döndür
- Eğer aradığın eleman ortadaki elemandan küçükse sol tarafa bak ve ortadaki sayıyla karşılaştır
- Eğer aradığın eleman ortadaki elemandan büyükse sağ tarafa bak ve sayıyla karşılaştır
Yukarıdaki mantık aranan eleman bulununcaya kadar devam eder.
```


```

```
