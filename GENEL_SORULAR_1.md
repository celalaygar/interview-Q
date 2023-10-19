## GENEL SORULAR 1


##### Genel Sorular 
```
- gRPC graphQL rest soap  Bu 4 ü arasındaki farklar nelerdir
- New lemeden classı nasıl kullanırsın Bu soru turkcell den geldi
- İnterface içerinde hiç birşey yazmazsam ne olur
```

##### Yapıkredi mülakat sorulaır 
```
Java
- hibernate nin kullandığı design pattern nedir (Proxy)
- hibernate nasıl connection oluşturur. (ipucu : Session Factory)

- Redux? Context Api?
- A component ile B componenti aynı dizinde. arasında veri nasıl taşırım.
```
##### Bilge adam Garanti Mülakat soruları
```
- Domain Driven Design (DDD) Açıklayınız?
https://medium.com/@avniozunlu/domain-driven-design-ddd-151c90472914

- rabbitmq, kafka , active mq nedir message brokerlerı acıklayınız

Java ****************
- Grpc nedir?
- Saga patternn nedir açıklayınız.
- Domain Driven Design (DDD) nedir?
- Scope ler nelerdır? singletion dısında request ve sessıon scope yı acıklayınız
- aspect ıle ılgılı sorular sorulabılır? Loglama yöntemleri nelerdir? Nasıl bir loglama yöntemi izlersiniz?

React js ****************
- componentler arası data nasıl taşınır?
Redux toolkit, Redux, Context Api, Mobx
- Useeffect ne yapar?
- UseRef açıklayınız.
```
##### İnnova mülakat sorusu 
``` 
- DATABASE de tarihleri formatlayarak karşılaştırma yapmak durumunda kalabiliyoruz. Sebebi Nedir?
- many to many ilişkiyi açıklayınız? one to many den farkı nedir? 

- 11 sayısı ile ilgili soru : [1,2,3,5,9,8,6] array içindeki herhangi 2 sayının toplamı 11 ediyorsa 
   o 2 sayının indexlerini yazarmısın. Ama o(N) İle çözülmesi gerekiyor.
``` 

##### Turkcell soruları
```
Annatasyonlar sorulabilir.
- depencey ınjectıon ve ozellıkle solidi acıkla 
- 2 class var 1 ınterfaceden ımplement edılmıs. bunun bır annatasyonu varmıs. nedır bu ?
- Spring @Qualifier @Primary
- Spring interceptor AOP
- Spring Hystrix nedir? 
- Mikroservisler arası iletişimi yapmanın yolları nelerdir? 
  Örnek: Feign client ve resttemplate


- mikroservis projesi var servislerdeen biri 2 tane instance oluşmuş biri full dolu isteklerle ugrasıyor diğeri yarım dolu. 
    API GATEWAY ISTEK GELDI bu 2 instance hangısıne gıdecegını nasıl anlayacak ve 
    exceptıon olursa nasıl kontrol edıcem ve bunun loglamasını nasıl yapıcaz. 
    API GATEWAY onun ınstancesı olmadıgını bılıyorsa annatasyon sayesınde o zaman 500 atar. 
    Bi kere gider baktı ayakta degıl bir daha gıdıp kontrol etmez.


Kod yazma sorusu
- 1 methoda 1 cümle ve 2 kelime gönderecem. bu kelimeler cümlede kac defa geçti kontrol et 
   eşitse true gönder değilse false gönder.


- @LAZY kullanımı ile ilgilş bir soru: 
   a classı var ıcınde b classı new lenmiş. b classı var ıcınde a new lenmiş. circuler oluşuyor ne yaparsın.

2 ayrı soru var
- a  b ve c classı var. a için b den bir instance var ve ayrıca arraylist var ve c classı tutuyor.
   bu arraylist a classı ıcınde. a class lı bır arraylist var  stream kullanarak dön her a classı ıcındekı b lerı 
   bır lısteye at. 
   a listesini stream ile dön her a içindeki c listesini bir listeye at (flatmap)
```

### Genel Mülakat soruları  v1 - Real Time İnterview Questions
``` 
- array ile arraylist arasındakı fark
- component ile element farkı varmıdır nedir
- final class ile method kullanımı ? 
- virtual dom ile real dom arasındakı fark ? 
- Component life cycle.
- functıonal ınterface

- final class extend edılemez
- final method override edilemez
``` 
### Obss Turkcell soruları

``` 
- bir react projesini farklı ip ve portta nasıl çalıştırırız ? 
.env.local dosyası  kullanarak yapılır.
- useeffect, useMemo nedir? 
- bir div için margin:auto yaparsak sonuç ne olur?

- login sıfresını unutursa ne yaparsın 
- logın guvrenlıgı nasıl saglanır 
- şifresini unutursa ne yaparsın...

thrad agırlıklı soru soruldu
- thread nasıl olusturulur. nasıl calısır.
- thread ile procces arasındakı fark nedir
- thread ve runnable ne zaman kullanılmalı. hangı durumlarda kullanılmalı
- run ve call methodları arasındakı fark nedır
- %99 thread sorarlar
- thread safety nedir
- thread nasıl durdurulur.
- javada 2 thread arasında veri paylaşımı ve aktarımı nasıl yapılır
- thread yield, join isAlive interrrupt 
- notify ve notifyAll arasındakı fark ne ,
- interrupted ile isInterrupted arasındakı fark nedir.

- stack ve heap arasındakı fark nedir.
- garbage collector acıkla
- deadlock ve livelock arasındakı fark
- thread concurrency
- HttpClient nedir ?
- 2 farklı tablo var bunlardakı verı tekrarı onlemek ıcın ne yaparsn..
- reverse string nedir kesin bil   polingrom kelime   2002   ada   
- stack de çözümü (tersten çekme), recursive functıon ile çözümüde var..
- string de her karakter arasında (bir cümlede) 1 kez tekrar eden karakteri bul.. 
- reverse string nedir kesin bil   polingrom kelime   2002   ada   
``` 
### Etiya 
``` 
- Union all sorusu sorulur  
- join 
- group by havıng sorulur
- Hash  map de nesne tekrarını önlemek ıcın ne kullanılır..
- String, Stringbuilder, StringBuffer (thread sencronıze oldugu ıcın daha guvenlı ve 2. birinin kullanılmasını engelliyor..) .

- bir arrayde en buyuk sayıyı bulan kodu nasıl yazarsın
- sort algorıtmaları nasıl calısır.
- facede , observer desıgn pattern neden kullanırız. kodunu yazabılır mısın
``` 
#### Genel Mülakat soruları v2
``` 
- array ile arraylist arasındakı fark
- component ile element farkı varmıdır nedir
- virtual dom ile real dom arasındakı fark ? 
- Component life cycle.
- functıonal ınterface

Final class larla ilgili soru gelebilir?
- final class ile method kullanımı ? 
- final class extend edılemez
- final method override edilemez
``` 

### Scrum nedir
``` 

``` 

### Kanvas nedir
``` 

``` 
### round robin 
``` 

``` 
