## GENERAL Q

### Stack and Queue arasındaki fark
``` 

``` 
### Garbage Collector nedir
``` 
Garbage Collection, otomatik bellek yönetimi mekanizmasıdır. Bu işlem heap belleğe bakıp, kullanılan objelerin tespit edilmesi ve 
referans edilmeyenlerin silinmesi üzerine kuruludur. Kullanılmayan/referans edilmeyen nesnelerin kapladığı alan bellekte boşa 
çıkarılır ve bellekte boş yer açılmış olur. Bu işlemi yapan mekanizmaya da Garbage Collector denir.
```
Garbage Collector : 
- https://medium.com/@tugrulbayrak/jvm-garbage-collector-nedir-96e76b6f6239
- https://medium.com/@gokhansengun/garbage-collector-nas%C4%B1l-%C3%A7al%C4%B1%C5%9F%C4%B1r-3bdf2fb20282

### binary search
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
### Genel Sorular (Spring, Java) turkcell soruları
Annatasyonlar sorulabilir.
- depencey ınjectıon ve ozellıkle solidi acıkla 
- 2 class var 1 ınterfaceden ımplement edılmıs. bunun bır annatasyonu varmıs. nedır bu ?
- Spring @Qualifier @Primary
- Spring interceptor AOP
- Spring Hystrix
- mikroservis projesi var servislerdeen biri 2 tane instance oluşmuş biri full dolu isteklerle ugrasıyor diğeri yarım dolu. API GATEWAY ISTEK GELDI bu 2 instance hangısıne gıdecegını nasıl anlıcak ve exceptıon olursa nasıl kontrol edıcem ve bunun loglamasını nasıl yapıcaz. API GATEWAY onun ınstancesı olmadıgını bılıyorsa annatasyon sayesınde o zaman 500 atar. bi kere gider baktı ayakta degıl bir daha gıdıp kontrol etmez.
-


- @LAZY kullanımı ile ilgilş bir soru: a classı var ıcınde b classı new lenmiş. b classı var ıcınde a new lenmiş. circuler oluşuyor ne yaparsın.

2 ayrı soru var
- a  b ve c classı var   a için b den bir instance var ve ayrıca arraylist var ve c classı tutuyor bu arraylist a classı ıcınde.
- a class lı bır arraylist var  stream kullanarak dön her a classı ıcındekı b lerı bır lısteye at.
- a listesini stream ile dön her a içindeki c listesini bir listeye at (flatmap)


1 methoda 1 cümle ve 2 kelime gönderecem. bu kelimeler cümlede kac defa geçti kontrol et eşitse true gönder değilse false gönder.



