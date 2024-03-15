# Genel Mülakat Soruları

+1 +2 +3 Yıl tecrübeliler için Java mülakat soruları

## Java Class Loader nedir ?
```
Java’da ClassLoader, Java programlarındaki sınıf dosyalarını yüklemek için kullanılan bir sınıftır.
Java kodu, javac derleyicisi tarafından sınıf dosyasına derlenir ve JVM, sınıf dosyasında yazılmış
byte kodlarını çalıştırarak Java programını yürütür.
```
Java’da üç varsayılan ClassLoader vardır: Bootstrap, Extension ve System (Application) ClassLoader.
```
1. Bootstrap ClassLoader : rt.jar ve diğer temel sınıflar gibi standart JDK sınıf dosyalarını yükler.
Tüm ClassLoader’ların atasıdır ve herhangi bir atası yoktur. Primordial ClassLoader olarak da
adlandırılır.

2. Extension ClassLoader : Bu sınıf yükleyicisi, kullanıcının genişletilmiş sınıf dosyalarını
yüklemesine izin verir. Bu sınıflar, “java.ext.dirs” olarak tanımlanan özel bir klasörde bulunur.

3. System / Application ClassLoader : Bu sınıf yükleyicisi, kullanıcının kendi sınıf dosyalarını
yüklemesine izin verir. (Yazılan Kodlar) Bu sınıflar, “java.class.path” olarak tanımlanan özel
bir klasörde bulunur.
```

## Javada Access modifiers nelerdir? 
```
1-Default: Aynı sınıftan, altsınıftan ve aynı package'den erişilebilir. Javada bir access modifier
tanımlanmazsa default olarak kabul edilir ve bu geçerli olur.
2-Private: Sadece aynı sınıftan erişilebilir.
3-Protected: Aynı sınıftan, aynı packageden ve alt sınıflardan erişilebilir.
4-Public: Her yerden erişilebilir.
```

## Final anahtar kelimesi ne işe yarar?
```
Final değişkenler:Değiştirilemez. Static ile beraber Constant olarak kullanılabilir.
Final class:Extend edilemez
Final methods: Override edilemez.
```

## Error ve Exception arasındaki farklar ?
```
Error, jvm tarafından runtime'da handle edilmesi mümkün olmayan türden hatalardır.
Exception ise try catch ile handle edilebilir. Java'da exceptionları 5 farklı keyword ile
handle edilebilir. -- Try -- Catch -- Finally -- Throw -- Throws
```

## Checked Exception ve Unchecked Exception arasındaki farklar ?
```
RuntimeException ve Error dışında Throwable sınıfını extend eden sınıflar Checked Exceptions
olarak tanımlanabilir. Checked Exceptionlar compile edilirken alınan hatalardır.
(IOException, SQLException)

RuntimeException sınıfını extend eden exceptionlar Unchecked Exceptionlar olarak adlandırılır.
Compile edilirken kontrol edilip gözükmez,
(ArithmeticException, NullPointerException)
```

## Java Thread ile VirtuaL Thread arasndaki fark nedir ?
```
https://medium.com/@onurokkyay/java-virtual-thread-nedir-6049151ac2b8
```
```
Java’da kullandığımız geleneksel threadler (bundan sonra Platform Thread olarak da bahsedeceğiz)
işletim sistemi tarafından yönetilir ve planlanır. Yeni bir platform thread oluşturmak için bir
sistem çağrısı yapılmalıdır ve bu maliyetli bir işlemdir.

Geleneksel threadlerin aksine virtual threadler JVM tarafından yönetilir. Bu nedenle, tahsisleri
bir sistem çağrısı gerektirmez ve işletim sisteminin bağlam anahtarından (context switch) muaftırlar.
Sonuç olarak, sistemin bağlam anahtarından kurtulduğumuz için daha az maliyetle birçok virtual
thread üretebiliriz.Ayrıca virtual threadler, gerçek çekirdek thread olan taşıyıcı threadler
üzerinde çalışır. Virtual threadler, Java kodu perspektifinden normal threadler gibi hissedilir,
ancak işletim sistemi threadlerine 1:1 eşlenmezler. Taşıyıcı thread havuzundan uygun olan taşıyıcı
threadin üzerine virtual threadler eşlenir.
```

## Java Multi Thread  nedir ?
```
Thread safe, birden çok threadin bir kaynağı aynı anda kullanması durumlarında ortaya çıkan
tutarsızlıkların sonucundaki hatalara karşı; o anki threadin kaynağını güvenceye alan ve
bunu o kaynağı kullanan tüm threadler için uygulayan bir konsepttir.

Asenkron yani multithreading bir yapıda threadlerin aynı veri kaynağına erişip değiştirmeye
çalışması, hatalı davranışların sergilenmesine ve tutarlı bir sonuç elde edilememesine
neden olabilir. Bu ve bunun gibi problemleri önlemek için threadleri güvenli bir şekilde
tasarlamak ve geliştirmek gerekir. Bu metodolojiye thread safe, iş parçacığı güvenliği denir.
```
## Serilization nedir?
```
Bir nesnenin veya bir sınıfın saklanacak forma dönüştürülme işlemidir. Extend edilen
Serilization sınıfı alt sınıf olan kullanacağımız sınıfın byte'lar halinde streamlere
yazılabilir böylece bir java objesi veritabanına kaydedilebilir.

Deserilization ise byte haline çevrilen java objesinin eski haline çevrimine denir.
```

## Java Thread safe ?
```

```

## Java ConcurrentHashMap ?
```
https://medium.com/@mmuratakbiyik/concurrenthashmap-detaylar%C4%B1-ve-temel-kullan%C4%B1m%C4%B1-5bb415d3bcf2
```

## Spring Scope Türleri nelerdir ?
```
Spring Framework içinde “scope” bir nesnenin yaşam döngüsünü ve ne kadar süreyle erişilebilir
olduğunu tanımlayan bir kavramdır. Spring, çeşitli nesne scope’ları sağlar ve bu scope’lar
nesnelerin oluşturulma, kullanılma ve yok edilme şeklini belirler.

Bu scope’lar, Spring uygulamalarında nesnelerin nasıl yönetileceğini belirlemek için kullanılır.
Scope belirleme, nesnelerin doğru zamanda oluşturulması, paylaşılması ve yok edilmesi açısından
önemlidir ve uygulamanın performansı ve davranışı üzerinde etkili olabilir.
```

##### singleton Scope 
```
Bir bean default olarak singleton scope’a sahiptir. Bean singleton scope ile tanımlandığı
zaman mevcut application context‘imiz içerisinde o bean’den yalnızca tek bir adet initialize
edileceğini garanti ederiz. Bu bean ile yapılacak olan tüm request’ler cache’lenmiş olan aynı
nesne üzerinden yapılır. 
```
##### prototype Scope
```
Prototype ile belirlenmiş bir bean, container içerisinde çağırıldığı her request’te yeniden
oluşturulacaktır. Scope notasyonun iki farklı kullanımını aşağıda görebilirsiniz.

Prototype Scope kullandığınızda, her request geldiğinde yeni bir instance döndürür. Diyelim ki
bir setter methoduna sahip bir sınıfınız var, şimdi bu sınıf için bir bean oluşturduğunuzda,
size her zaman sınıfın yeni bir instance’sını verecek ve nesne niteliklerini değiştirmek için
setter’ı özgürce kullanıp çalışacaktır. 
```
##### request Scope
```
Request bean’i HTTP isteği geldiğinde oluşturulur. örneğin, bir “ /products” API’niz var, şimdi
controller bu isteği aldığında ve service methodunu çağırdığında, Request Scope ile bir
Bean’iniz olacak ve bu API isteği yanıtı geri gönderene kadar her zaman nesnenin aynı
instance’ını alırsınız, ancak yeni bir request geldiğinde, yeni bir instance gönderecek.
```
##### session Scope
```
Session Scope Web Uygulamalarında HTTP isteği geldiğinde oluşturulur. Mesela Spring boot
uygulamanız kullanıcı sessionlarını sürdürdüğünde, bu scope yardımcı olabilir.
Session Scope kullandığımızda, tüm Session için (kullanıcı düzeyindeki oturumda) her zaman
nesnenin aynı instance’ını return eder. Ancak kullanıcı oturumu kapandığında, yeni bir
kullanıcı oturumu için nesnenin yeni bir instance’ını alacaksınız.
```
##### application Scope
```
Bir application scope, ServletContext’in yaşam döngüsü için bean örneğini oluşturur.
Bu singleton scope’a benzer ancak aralarında farklılıklar mevcuttur. Bir bean application
scope değerine sahipken bu bean çoklu servlet tabanlı uygulamalar ile de paylaşılabilirken,
singleton scope değerine sahip bir bean yalnızca mevcut application context’i içerisinde
tanımlıdır.
```

## Solid prensipleri nelerdir?
```
1-Single responsibilty: Bir nesne ya da bir sınıfın tek bir sorumluluğu olmalıdır.

2-Open-closed: Bir sınıf değişime kapalı gelişmeye açık olmalıdır.

3-Liskov's Substitution: Nesneler programın çalışmasında sorun yaratmadan kendi alt örnekleriyle
  değiştirilebilmelidir.

4-Interface Segregation: Nesneler ihtiyaç duymadıkları metotların interfacelerinden ayrıştırılmalıdır.

5-Dependency Inversion: Yüksek seviyeli sınıflar düşük seviyeli sınıflara bağlı olmamalı,
  her ikisi de soyut kavramlara bağlı olmalıdır.
```

## Single Responsibilty nedir?
```
Single responsibilty bir nesnenin tek bir amaçla yaratılmasını konu alır. Bağlı olduğu sınıfın
içerdiği davranışsal özellikler tek bir amaca uygun olmalı başka bir davranış göstermemelidir.
Örneğin bir çalışan sınıfı içerisinde vergi hesaplama fonskiyonu bulunamaz. Bu single
responsibilty prensibine aykırı bir kod yazım şeklidir.
```

## Circuat Breaker nedir ?
```

```

## Spring Boot Interceptor Nedir?
```
Interceptor, Spring MVC paketinde bulunan bir sınıftır. HTTP isteklerinin öncesi, sonrası
ve tamamlandıktan sonra yapılması gereken işlemleri bu sınıf aracılığı ile handle edebilmekteyiz.

Gelen isteklerin endpointe ulaşmadan önce işlenmesini sağlamamıza yarayan bir sınıftır.
Bir servlete benzer ve DispatcherServlet ten sonra bulunmaktadır. HTTP isteklerini kontrol
etmek için kullanılır. İstek başlamadan önce çağrılır ve HTTP isteği ile ilgili bilgileri
içeren HttpServletRequest nesnesini ve HTTP isteği ile ilgili yanıtı döndürecek
HttpServletResponse nesnesini alır.

Ref : 
https://blog.burakkutbay.com/spring-boot-interceptor-nedir-uygulama-ornegi.html/
```

## PostgreSQL de index türleri ?
https://gokhana.dev/postgresql-index-tipleri-ve-index-secimi/
##### BTREE Index
```
Bir index yaratıldığında tipi verilmez ise default olarak btree oluşturulmaktadır. Özellikle
“büyüktür”, “büyük eşittir”, “küçüktür”, “küçük eşittir”, “eşittir”, “between”, “is null”,
“is not null” gibi sorguların hepsinde kullanılabilir. Like’lı ifadeler ise “sabit değer%”
şeklinde ise kullanılabilir. Balance tree algoritmasını kullanmaktadır.

- Çoğu sorgu türü için en performanslı seçenektir.”>, >=, <, <=, =, IN, BETWEEN” gibi gibi..
- Varsayılan/Default sorgu tipidir.
- Çoklu kolon indexlemesini yapılabilir. 
```
##### Hash Index
```
Hash daha çok eşitlik anında kullanılabilen bir index türüdür. Oluşum hızı index yaratma süresi
açısından Btree’ye göre çok daha fazladır. Ancak kapladığı alan bakımından Btree’ye göre çok 
daha az bir yer kaplar. Çünkü Btree ağaç yapısında tutulurken, hash flat bir yapıda tutulmaktadır.

Hash index, kullanım şekli açısından genellikle B-tree ile karşılaştırılmaktadır.

- Eşitlik operatörü ile yapılan sorgular için iyi bir seçenektir. 
- Hash index, B-Tree indexinden daha az yer kaplar.
- Tabloya satırlar eklendikçe linear olarak büyüyen B-Tree indexinin aksine, Hash indexi ani
  artışlarla büyür.
- Hash indexler ile “unique” constraint kullanılamaz.
- Hash indexler birden fazla kolon için oluşturulamazlar. 
- Hash indexleme yapılırken sıralama ifadelerine yer verilemez.
- Hash indexleme yaptığınız bir tablo için Cluster kullanamazsınız.
```
##### BRIN: Block range index
```
Postgresql verileri varsayılan olarak 8 Kb’lık bloklar halinde saklamaktadır. Brin
indexlemede, indexler tutulurken bloklar içerisindeki en büyük ve en küçük değerler
baz alınır. B-tree’nin aksine blok içersinde sıralanmış tüm değerler değil, sadece
min ve max değerler tutulur. Eski adıyla min-max indextir.

B-tree yaratıldığında 8Kb’lık veri setlerinin tümünü saklayacak şekilde bir
indexleme yapar. Ancak BRIN ındex 8Kb’lık bloklardan sadece minumum ve maximum
değerleri alarak index halinde saklar.

- Btree ile karşılaştırıldığında tutalan veri boyutuna bakarsak çok çok daha az
  olduğunu görebiliriz.
- Doğrudan bir veri yerine bir aralık üzerinde işlem yapılıyorsa çok performanslı
  çalışabilir.
- Sadece belirli veriler index için tutulduğundan ötürü en az yer kaplayan index
  türüdür.
- Özellikle big data ve veri analizi alanlarında range işlemlerinin çokluğundan
  dolayı tercih edilmektedir.
```
##### GIN Index
```
Generalized Inverted Index ile her kelime için bir index ve bu indexin içinde aranan
ifadenin geçtiği yerlerin listesini sıkıştırılmış olarak tutar.

- Bir kolonda array gibi çoklu verinin olması durumlarında kullanılabilir. Yani metin
  içinde aramalarda kullanılması önerilir
- “Full text search” işlerinde kullanılabilir.
- JSONB üzerinde yapılan aramalarda tercih edilebilir.
- Range ve array veri tiplerinde kullanılabilir
- ILIKE ile birlikte ‘%abc%’ şeklindeki aramalarda btree verimli çalışmaz. GIN tercih edilebilir.
```

##### GIST Index
```
Generalized search tree, full text search için güçlü diğer bir adaydır. Btree karşılaştırma
yapıları için kullanılırken, GIST’te ağaç yapısında veri tutmasına karşın daha çok modern
veritabanlarındaki geodata, text documents gibi operatorler için kullanılmaktadır.

- Aynı kolonda değerlerin başka satırlarda çakışması durumlarında kullanılabilir.
- Indexleme yöntemidir ve bu index tipinden birçok index türetilebilir.
- “Full text search” işlerinde kullanılabilir.
- Geometrik veri türlerini indexlemek için kullanılırlar.
```
## Optimistic Lock Nedir ?
```
Optimistic, yani iyimser eş zamanlılık kontrolünde aynı anda bir kaydın update edilmeyeceği
varsayılır ve birden fazla session aynı kaydı update etmek için erişilebilir. Eğer aynı kayıt
birden fazla kişi tarafından update edilirse kayıtlardan biri iptal olur ve kullanıcıya
iptal olduğuna dair bilgilendirme yapılır.
```

## Pessimistic Lock Nedir ?
```
Pessimistic, yani kötümser eş zamanlılık kontrolünde bir kullanıcı bir kaydı değiştirmek
istediğinde o kayda kilit koyar ve o kaydı başkası değiştiremez. İlk değiştirmeye çalışan
kişi kaydı değiştirdikten sonra değiştirilen kayıt üzerindeki kilit açılır ve diğer
değiştirmek isteyenler artık değiştirebilir hale gelir.
```

## Spring IOC Container ?
```
Spring IoC Container, Spring Framework'ün çekirdeğidir. Bu konteyner, nesneleri oluşturur,
nesneleri birbirine bağlar, bağımlılıklarını yapılandırır ve tüm yaşam döngüsünü yönetir.

Inversion of control bir yazılım tasarım prensibidir. Ioc ile Uygulama içerisindeki obje
instance’larının yönetimi sağlanarak, bağımlılıklarını en aza indirgemek amaçlanmaktadır.
Projeniz deki bağımlılıkların oluşturulmasını ve yönetilmesini geliştiricinin yerine,
framework’ün yapması olarak da açıklanabilir.

Framework‘in üzerinde çalıştığımız da görülüyor ki; frameworkler birçok işi kendisi yapmakta
ve bizim kodumuzu çalıştırmak için framework gerekli kaynakları ve çalışması gereken metotları
oluşturup, yönetmektedir. Yazdığımız kod bloğu çalışacağı zaman, framework bizim kodumuzu
çağırır ve çalıştırır daha sonra kontrol yeniden framework’e geçmesi olayının tümüne
Inversion Of Control adı verilmektedir.
```

## CQRC nedir?
```

```

## Apache Kafka ve Rabbit MQ arasındaki farklar nelerdir ?
```

```

## Saga Pattern nedir ?
```

```

## Domain Driven Design (DDD) ?
```
https://medium.com/@avniozunlu/domain-driven-design-ddd-151c90472914
```
## Domain Driven Design Nedir?
```
https://medium.com/@avniozunlu/domain-driven-design-ddd-151c90472914
```
