## GENEL SORULAR 2

### Stack and Queue arasındaki fark nedir ?
``` 
Stack koleksiyon sınıfı, LIFO adı verilen, Last In First Out( Son giren ilk çıkar) prensibine gore çalışırken, 
Queue koleksiyon sınıfı ise FIFO yani First In First Out(ilk giren ilk çıkar) prensibine gore çalışır.
``` 
### Garbage Collector nedir ?
``` 
Garbage Collection, otomatik bellek yönetimi mekanizmasıdır. Bu işlem heap belleğe bakıp, kullanılan objelerin 
tespit edilmesi ve referans edilmeyenlerin silinmesi üzerine kuruludur. Kullanılmayan/referans edilmeyen 
nesnelerin kapladığı alan bellekte boşa çıkarılır ve bellekte boş yer açılmış olur. Bu işlemi yapan mekanizmaya da 
Garbage Collector denir.
```
Garbage Collector : 
- https://medium.com/@tugrulbayrak/jvm-garbage-collector-nedir-96e76b6f6239
- https://medium.com/@gokhansengun/garbage-collector-nas%C4%B1l-%C3%A7al%C4%B1%C5%9F%C4%B1r-3bdf2fb20282

### binary search açıklayınız
Binary Search algoritmasında dizi her adımda ikiye bölünür. Mantığı şu şekildedir.
```
- Dizinin ortasındaki elemanı bul eğer aradığın elemana eşitse index’i döndür
- Eğer aradığın eleman ortadaki elemandan küçükse sol tarafa bak ve ortadaki sayıyla karşılaştır
- Eğer aradığın eleman ortadaki elemandan büyükse sağ tarafa bak ve sayıyla karşılaştır
Yukarıdaki mantık aranan eleman bulununcaya kadar devam eder.
```
### Liquibase ve Flyway nedir, farkları nelerdir?
Alıntıdır : [Liquibase ve Flyway farkları nelerdir?](https://medium.com/sahibinden-technology/liquibase-ve-flyway-nedir-farklar%C4%B1-nelerdir-1b8d95fe1537)

Temel olarak veri tabanı taşıma (migration) işlemlerimizi gerçekleştirebildiğimiz ve bunun yanında farklı yardımcı mekanizmaları da destekleyen araçlar olduklarından bahsedebiliriz.
``` 
- Liquibase, veritabanı şema değişikliklerini izlemek, yönetmek ve uygulamak için açık kaynaklı, 
veri tabanından bağımsız bir kütüphanedir.

- Flyway, açık kaynaklı bir veritabanı taşıma (migration) aracıdır. Sadeliği ve 
konfigürasyondan bağımsız konvensiyonel bir mekanizmayı ön plana çıkarmayı amaçlar.
``` 

