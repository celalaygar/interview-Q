# Genel Mülakat Soruları

+1 +2 +3 Yıl tecrübeliler için Java mülakat soruları

# JAVA - SPRING Mulakat soruları

## Java Class Loader nedir ?
```
Java’da ClassLoader, Java programlarındaki sınıf dosyalarını yüklemek için kullanılan bir sınıftır.
Java kodu, javac derleyicisi tarafından sınıf dosyasına derlenir ve JVM, sınıf dosyasında yazılmış
byte kodlarını çalıştırarak Java programını yürütür.
```
Java’da üç varsayılan ClassLoader vardır: Bootstrap, Extension ve System (Application) ClassLoader.
```
1. Bootstrap ClassLoader : rt.jar ve diğer temel sınıflar gibi standart JDK sınıf dosyalarını
yükler. Tüm ClassLoader’ların atasıdır ve herhangi bir atası yoktur. Primordial ClassLoader olarak
da adlandırılır.

2. Extension ClassLoader : Bu sınıf yükleyicisi, kullanıcının genişletilmiş sınıf dosyalarını
yüklemesine izin verir. Bu sınıflar, “java.ext.dirs” olarak tanımlanan özel bir klasörde bulunur.

3. System / Application ClassLoader : Bu sınıf yükleyicisi, kullanıcının kendi sınıf dosyalarını
yüklemesine izin verir. (Yazılan Kodlar) Bu sınıflar, “java.class.path” olarak tanımlanan özel
bir klasörde bulunur.
```

## Java'da String ve StringBuilder arasındaki fark ? 
```
String: String sınıfı değiştirilemez (immutable) bir sınıftır. Bir String nesnesi oluşturulduktan
sonra, onun içeriği değiştirilemez. Örneğin, bir String üzerinde herhangi bir değişiklik yapmak
(bir karakter eklemek, çıkarmak veya değiştirmek) yeni bir String nesnesi oluşturur.

StringBuilder: StringBuilder sınıfı değiştirilebilir (mutable) bir sınıftır. Bir StringBuilder
nesnesi oluşturulduktan sonra, onun içeriği değiştirilebilir. Bu, aynı nesne üzerinde değişiklik
yapmanıza olanak tanır ve genellikle daha verimlidir.
```

## Java'da StringBuilder ve StringBuffer arasındaki fark ? 
```
StringBuilder: Thread-safe değildir. Bu, StringBuilder nesnesinin aynı anda birden fazla thread
tarafından güvenli bir şekilde kullanılamayacağı anlamına gelir. Tek thread'li uygulamalarda veya
birden fazla thread'in aynı StringBuilder nesnesine erişmeyeceği durumlarda kullanılması uygundur.

StringBuffer: Thread-safe'dir. Bu sınıfın tüm yöntemleri senkronize edilmiştir, yani aynı anda
birden fazla thread tarafından güvenli bir şekilde kullanılabilir. Bu nedenle, çok thread'li
uygulamalarda veya birden fazla thread'in aynı StringBuffer nesnesine erişmesi gereken durumlarda
kullanılması uygundur.
```

## Javada Access modifiers nelerdir ? 
```
1-Default: Aynı sınıftan, altsınıftan ve aynı package'den erişilebilir. Javada bir access modifier
tanımlanmazsa default olarak kabul edilir ve bu geçerli olur.
2-Private: Sadece aynı sınıftan erişilebilir.
3-Protected: Aynı sınıftan, aynı packageden ve alt sınıflardan erişilebilir.
4-Public: Her yerden erişilebilir.
```

## ArrayList ile Array arasındaki fark nedir ? 
```
1- Boyut: Array'ler, boyutları sabit olan veri yapılarıdır, yani tanımlandıkları boyutta kalırlar.
ArrayList'ler ise boyutları dinamik olarak değiştirilebilen veri yapılarıdır, yani öğe sayısı
arttıkça boyutları da otomatik olarak artar.

2- Tür: Array'ler, tek bir türdeki verileri depolamak için kullanılır. ArrayList'ler ise farklı
türlerdeki verileri depolamak için kullanılabilir.

3- İşlevsellik: Array'ler, basit bir veri yapısıdır ve sınırlı işlevselliğe sahiptirler.
ArrayList'ler ise daha gelişmiş işlevselliklere sahiptir. Örneğin, ArrayList'lerde verileri
ekleme, silme, sıralama gibi işlemler kolayca yapılabilir.

4- İşlem hızı: Array'ler, verileri doğrudan belleklerinde tuttuklarından hızlı işleme imkanı
sağlarlar. ArrayList'ler ise verileri heap bellekte tuttuklarından işlem hızı, Array'lere göre
daha yavaş olabilir.

5- Tip güvenliği: Array'ler, tür güvenliğine sahiptir. Yani, tanımlanan tür haricinde veri
eklenemez. ArrayList'ler ise tür güvenliği sağlamak için cinsiyetli yapılar ile çalışırlar.

6-Null değerler: Array'ler null değerler içerebilirken, ArrayList'ler null değerleri kabul etmezler.
```

## List, Set, Hashmap  acıklayınız ?
```
Set Nesnesi: Kendisine verilen elemanların her birinde sadece bir tanesini tutar. Kopya ya da
tekrarlanan elemanları barındırmaz.

List Nesnesi: Kendisine verilen elemanları sıralı şekilde tutar. Tekrarlana elemanları
barındırabilir.

Map Nesnesi: Her biri birbirinden farklı anahtarlar ile eşleştirilen nesnelerden oluşur.
```

## Javada Statement ve PreparedStatement arasındaki farklar?
```
PreparedStatement ile SQL ifadelerimizi veritabanımızda önceden derlenmek üzere gönderebileceğimiz
ve her defasında derlenmiş hale değer göndererek tekrar tekrar kullanabileceğimiz bir yapıdır.

Statement nesnesinde programımız üzerinde ifade derlenip veritabanımız sadece sorgulama işlemini
gerçekleştirmekte idi.
```
##### Statement
```
- SQL sorgusunun yalnızca bir kez yürütülmesi gerektiğinde kullanılır.
- Çalışma zamanında parametreleri iletemezsiniz.
- Performans çok düşük.
- Normal SQL sorgularını yürütmek için kullanılır.
- Binary verileri okumak  ve yazmak için kullanılmaz.
```
##### PreparedStatement
```
- SQL sorgusunun birden çok kez yürütülmesi gerektiğinde kullanılır
- Çalışma zamanında parametreleri iletebilirsiniz.
- Birden çok kez çalıştırılacak sorgular için kullanılır.
- Performans Statement'ten daha iyidir.
- Dinamik SQL sorgularını çalıştırmak için kullanılır.
- Binary verileri okumak  ve yazmak için Readydstatement'ı kullanabiliriz.
- PreparedStatement, özel karakterlerden otomatik olarak kaçtığı için SQL enjeksiyon
saldırılarını önlememize yardımcı olur.
```

## Java Spring bootda Aspect ile ilgili neler yaptın, ne yapılabilir.
```

```

## Bir final class da içindekı liste final ise değişiklik yapılabilir mi.
```

```

## Set içerisinde bir student nesnesi var nesne id ve name barındırıyor. id leri aynı name leri farklı olan objeleri Set'e yerleştirirsek ne olur acıklayınız ?
```
her yeni new ile oluşturulan class ların hash code ları farklı olduğundan dolayı
Set listesine yeni bir farklı obje olarak eklenir. Örnek kod ve çıktısı aşşağıdadır.
```
```
public static void main(String[] args) {
    Set<Student> set = new HashSet<Student>();
    set.add(new Student(1, "cello"));
    set.add(new Student(2, "mello"));
    set.stream().forEach(System.out::println);
}

class Student{
    private int id;
    private String name;

    public Student(int id, String name) {
        this.id = id;
        this.name = name;
    }
}
```
Output
```
main6.Student@7a81197d
main6.Student@5ca881b5
```
## ArrayList ile LinkedList arasındaki fark nedir ? 
```
1- Dizilerde ulaşmak istediğimiz elemana indisini girerek ulaşırız. Linked List’lerde ise
ulaşmak istediğimiz elemanlara point eden pointerlar vasıtasıyla ulaşırız.

2- Dizilerde eleman ekleme, silme gibi işlemler Linked List’lere göre performans açısından
daha maliyetlidir. Örneğin; 1000 elemanlı bir dizimiz tanımlı olsun. Bu dizinin 500.cü elemanını
silmek istediğimizde, bu elemandan sonra gelen her eleman bir sıra geri kaydırılacak bu da
performans kaybına yol açacaktır. Linked List’te ise bu işlem sadece basit pointer
operasyonlarıyla gerçekleştirilir ve kaydırma işlemlerine gerek kalmaz. Bu sayede
performanstan kazanç sağlanmaktadır.

3- Linked List dinamiktir. Dizi tanımlaması yapılırken en başında veri boyutunu belirtmemiz
gerekirken, Linked List’lerde ihtiyaç duyduğumuzda boyutu artırabilir, silme işlemlerimizden
sonra Linked List boyutumuzu küçültebiliriz.
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
bir sistem çağrısı gerektirmez ve işletim sisteminin bağlam anahtarından (context switch)
muaftırlar. Sonuç olarak, sistemin bağlam anahtarından kurtulduğumuz için daha az maliyetle
birçok virtual thread üretebiliriz.Ayrıca virtual threadler, gerçek çekirdek thread olan taşıyıcı
threadler üzerinde çalışır. Virtual threadler, Java kodu perspektifinden normal threadler gibi
hissedilir, ancak işletim sistemi threadlerine 1:1 eşlenmezler. Taşıyıcı thread havuzundan uygun
olan taşıyıcı threadin üzerine virtual threadler eşlenir.
```

## Java Multi Thread  nedir ?
```
Thread safe, birden çok threadin bir kaynağı aynı anda kullanması durumlarında ortaya çıkan
tutarsızlıkların sonucundaki hatalara karşı; o anki threadin kaynağını güvenceye alan ve bunu
o kaynağı kullanan tüm threadler için uygulayan bir konsepttir.

Asenkron yani multithreading bir yapıda threadlerin aynı veri kaynağına erişip değiştirmeye
çalışması, hatalı davranışların sergilenmesine ve tutarlı bir sonuç elde edilememesine neden
olabilir. Bu ve bunun gibi problemleri önlemek için threadleri güvenli bir şekilde tasarlamak
ve geliştirmek gerekir. Bu metodolojiye thread safe, iş parçacığı güvenliği denir.
```
## Serilization nedir?
```
Bir nesnenin veya bir sınıfın saklanacak forma dönüştürülme işlemidir. Extend edilen Serilization
sınıfı alt sınıf olan kullanacağımız sınıfın byte'lar halinde streamlere yazılabilir böylece bir
java objesi veritabanına kaydedilebilir.

Deserilization ise byte haline çevrilen java objesinin eski haline çevrimine denir.
```

## Java Thread safe ?
```
https://medium.com/@eda.dlkc/thread-safe-nedir-fe52d21238fa
```
```
https://www.gencayyildiz.com/blog/thread-safe-concurrentqueue-concurrentdictionary-concurrentbag-concurrentstack-ve-blockingcollection-koleksiyonlari-ve-kullanim-durumlari/
```

## Spring Boot ve Spring Framework arasındaki fark nedir?
```
- Spring Framework → Konfigürasyon ağırlıklı, XML veya Java Config gerekebilir.
- Spring Boot → Spring üzerine kuruludur, hazır starter bağımlılıkları ve otomatik konfigürasyonu
sayesinde çok daha hızlı geliştirme sağlar.

Özet: Spring Boot = Spring + Auto Configuration + Embedded Server + Production tools
```

## Spring Boot Auto-Configuration nasıl çalışır?
```
Spring Boot uygulama başlarken classpath’teki bağımlılıkları kontrol eder ve uygun
konfigürasyonu otomatik yükler.
- spring-boot-starter-web varsa → DispatcherServlet, Tomcat otomatik başlatılır.
- spring-boot-starter-data-jpa varsa → EntityManagerFactory, DataSource otomatik oluşturulur.

Bunu sağlayan mekanizma: @EnableAutoConfiguration anotasyonu.
```

## Spring Boot Actuator nedir?
```
Spring Boot Actuator, uygulamanın çalışma zamanında sağlık durumu, metrikler, loglar,
env bilgileri gibi üretim seviyesinde izleme (monitoring) ve yönetim özellikleri sağlar.
- /actuator/health → Uygulamanın sağlık durumu
- /actuator/metrics → Bellek, CPU, istek sayısı
- /actuator/env → Ortam değişkenleri
```

## Spring Boot’ta application.properties ve application.yml farkı nedir?
```
- application.properties → Anahtar-değer (key=value) formatındadır.
- application.yml → YAML formatında, daha okunabilir ve hiyerarşik yapı destekler.
```

## Spring Boot’ta Profil (Profile) nedir?
```
Spring Boot, farklı ortamlar için (dev, test, prod) ayrı konfigürasyonlara izin verir.
@Profile anotasyonu ile hangi bean’in hangi ortamda çalışacağını belirleyebiliriz.
```
```
@Profile("dev")
@Bean
public DataSource devDataSource() {
    ...
}
```

## Spring Boot Security ile kimlik doğrulama nasıl yapılır?
```
Spring Security, Spring Boot’ta otomatik entegre gelir.
Varsayılan olarak tüm endpointler korunur, user isimli kullanıcı oluşturulur ve şifre konsolda
gösterilir. Gelişmiş senaryolar için:
```
```
- JWT tabanlı kimlik doğrulama
- OAuth2 / OpenID Connect entegrasyonu
- Role-based access control
```

## Spring’de @Transactional anotasyonu kullanılmasına rağmen neden rollback olmuyor?
#### 1. Exception türü rollback tetiklemiyor olabilir
```
Spring, varsayılan olarak sadece RuntimeException ve Error tiplerinde rollback yapar.
Checked Exception (örn. IOException, SQLException) fırlatılırsa rollback olmaz.
```
```
@Transactional(rollbackFor = Exception.class)
public void myMethod() throws Exception {
    ...
}
```
#### 2. Metodun aynı sınıf içinde çağrılması (self-invocation)
```
Spring @Transactional, AOP proxy üzerinden çalışır.
Eğer bir sınıf içinde transactional metod, yine aynı sınıftaki başka bir metod tarafından
çağrılıyorsa proxy devreye girmez → rollback çalışmaz.

👉 Çözüm:
Transactional metodu başka bir bean’den çağır veya aspectJ ile compile-time weaving kullan.
```
#### 3. Transactional metod public değilse
```
Spring AOP proxy, sadece public metodlara transactional uygular.
Eğer metod private, protected veya default ise rollback çalışmaz.

👉 Çözüm:
Transactional metod public olmalı.
```
#### 4. Exception yakalanıp swallow (yutuluyorsa)
```
Eğer exception try-catch içinde yakalanıp üst kata fırlatılmıyorsa rollback tetiklenmez.
```
```
@Transactional
public void saveData() {
    try {
        // hata fırlatılır
    } catch (Exception e) {
        // log atıp swallow ederse rollback OLMAZ
    }
}
```
```
👉 Çözüm:

- Exception tekrar fırlatılmalı (throw e;)
- Ya da rollback manuel çağrılmalı:

TransactionAspectSupport.currentTransactionStatus().setRollbackOnly();
```
#### 5. Transactional propagation yanlış ayarlanmış olabilir
```
Örneğin REQUIRES_NEW kullanılırken iç transaction rollback olsa bile dış transaction
rollback olmayabilir.

👉 Çözüm:
Doğru propagation stratejisini seçmek (REQUIRED, REQUIRES_NEW, NESTED vs.).
```
#### 6. No proxy / yanlış yapılandırma
```
- @EnableTransactionManagement unutulmuş olabilir.
- Transaction manager (DataSourceTransactionManager, JpaTransactionManager) yanlış veya hiç
tanımlanmamış olabilir.
```
#### 7. Read-only transaction
```
Eğer @Transactional(readOnly = true) kullanıyorsan, bazı veritabanı sürücüleri update/delete
işlemlerini commit etmeyebilir, rollback davranışı da farklı olabilir.
```
✅ Özet:

```
@Transactional var ama rollback olmuyorsa en büyük sebepler:
- Exception tipi (checked/unchecked farkı)
- Self-invocation (aynı sınıf içinden çağrı)
- Metodun public olmaması
- Exception’ın swallow edilmesi
- Yanlış propagation
- Transaction yönetiminin devreye girmemesi
```

## Thread Dump nedir?
```
- Thread Dump, JVM üzerinde o anda çalışan tüm thread’lerin (iş parçacıklarının) durumunu
gösteren bir rapordur.
- İçinde şunlar olur:
  - Hangi thread çalışıyor, hangi kod satırında
  - Thread’in state’i (RUNNABLE, WAITING, BLOCKED, TIMED_WAITING vs.)
  - Lock’lar, deadlock bilgisi
  - Stack trace

👉 Kısaca: Thread Dump = JVM’in “röntgen filmi”
```

## Thread Dump ne zaman kullanılır?
```
- Uygulama donmuşsa (hang, deadlock)
- Yüksek CPU kullanımı varsa
- Thread sayısı artıyorsa (thread leak)
- Performans analizi yapmak gerektiğinde
```

## Spring’te @Component, @Service, @Repository arasındaki farklar?
```
1. @Component
→ En genel stereotype anotasyondur.
→ Spring bean’i tanımlamak için kullanılır.
→ @Component ile işaretlenmiş sınıf, component-scan sırasında Spring IoC Container’a eklenir.

Ne zaman kullanılır?
→ Eğer sınıfın rolü service, repository veya controller gibi belirgin değilse, genel amaçlı
bir Spring bileşeni olduğunu belirtmek için.
```
```
2. @Service
→ @Component’in specialization (özelleştirilmiş) halidir.
→ Semantik olarak bu sınıfın iş mantığını (business logic) içerdiğini belirtir.
→ Ekstra olarak Spring AOP ile iş katmanına yönelik işlemlerde
(örneğin transaction, logging, security) anlam kazanır.

Ne zaman kullanılır?
→ Service/Business katmanı sınıflarında.
```
```
3. @Repository
→ @Component’in başka bir specialization’ıdır.
→ Semantik olarak bu sınıfın data access layer (DAO) olduğunu belirtir.
→ Ekstra özellik: Spring, @Repository ile işaretlenmiş sınıflarda veritabanı
exception’larını Spring’in DataAccessException hiyerarşisine dönüştürür.

Ne zaman kullanılır?
→ Database erişim katmanında (JPA, JDBC, MongoDB, vb.).
```

## Veritabanında 200 bin kayıt update ederken performans problemini nasıl çözersin?

#### 1. Tek sorgu ile toplu update yapmak ✅
```
En hızlı yöntem, 200 bin satırı tek bir SQL UPDATE sorgusu ile güncellemektir.
```
```
UPDATE orders
SET status = 'CLOSED'
WHERE status = 'PENDING';
```
```
👉 Avantajı: Tek transaction, tek IO, çok hızlı.
👉 Not: Eğer güncellemeler farklı değerler içeriyorsa, bu yöntem her zaman uygulanamayabilir.
```

#### 2. Batch Update (Toplu Güncelleme)
```
Eğer her kayıt için farklı değer update edilecekse → tek tek update yerine batch kullanılır.
```
```
jdbcTemplate.batchUpdate(
    "UPDATE employees SET salary = ? WHERE id = ?",
    employees,
    1000, // batch size
    (ps, emp) -> {
        ps.setBigDecimal(1, emp.getSalary());
        ps.setLong(2, emp.getId());
    }
);
```
```
👉 Batch size genelde 1000 – 5000 arasında ayarlanır.
👉 Böylece 200.000 update = 200 query yerine, 200 batch × 1000 update olur → çok daha hızlı.
```
#### 3. Transaction Yönetimi
```
Tek tek update + auto-commit açıksa → her kayıt için commit yapar, çok yavaş olur.
Çözüm: Auto-commit’i kapatıp tek transaction veya batch transaction kullanmak.
```
```
@Transactional
public void bulkUpdate(...) {
   // batch işlemler
}

```
#### 4. Index Optimizasyonu
```
Update sırasında WHERE şartında kullanılan sütunlar indexlenmiş olmalı.
```
```
UPDATE employees SET salary = salary * 1.1 WHERE department_id = 5;
```
```
→ department_id üzerinde index varsa çok daha hızlı çalışır.
```
#### 5. Partitioning veya Chunk Processing
```
200 bin çok büyük değil ama milyonlarca kayıt olduğunda →
- İşlemi chunk’lara bölmek gerekir (örneğin 10k kayıt = 20 işlem).
- Spring Batch veya cursor ile yönetilebilir.
```
#### 6. Lock ve Concurrency Sorunları
```
→ Büyük update işlemi uzun sürerse, tabloyu kilitleyebilir.
→ Çözüm:
  → Update işlemini off-peak saatlerde yapmak
  → Küçük batch’lerle güncellemek
  → Gerekiyorsa row-level lock ile yönetmek
```
#### 7. Veritabanı Özel Çözümleri
```
→ PostgreSQL: COPY ile geçici tabloya yükleyip join-update yapmak çok hızlıdır.
→ Oracle: MERGE INTO kullanılabilir.
→ MySQL: Bulk update için geçici tablo (LOAD DATA INFILE) ve join update yapılabilir.
```

## Sepetteki veriyi nasıl tutarım nasıl hızlı getirirrim nasıl hızlı update ederim..
E-commerce gibi sistemlerde “sepet (shopping cart)” performansı kritik bir konudur.

#### 1. Sepet verisini nerede tutarım?
```
→ Frontend tarafında (client-side):

localStorage veya sessionStorage → küçük sepetler için hızlı çözüm.
Redux / Context API → sayfa yenilendiğinde kaybolmaması için.
Avantaj: Hızlı, server yükünü azaltır.
Dezavantaj: User login olmadan farklı cihazlardan senkronize edemezsin.
```
```
→ Backend tarafında (server-side):

Database (RDBMS/MongoDB) → kalıcı depolama.
Cache (Redis, Memcached) → hızlı erişim için.
Genellikle Redis + DB birlikte kullanılır.
Redis → anlık sepet işlemleri (okuma/yazma çok hızlı).
DB → checkout sırasında kalıcı hale getirme.
```
#### 2. Nasıl hızlı getiririm?
```
→ Cache (Redis) kullan:

Key → cart:userId
Value → JSON formatında sepet içeriği.
Böylece her istek DB’ye gitmez, Redis’ten milisaniyede gelir.
```
```
→ Indexleme yap:

DB’de userId + cartId üzerinde index olmalı.
```
```
→ API optimizasyonu:

GET /cart → tek endpoint, tüm ürünleri + toplam tutarı döner.
Gerekirse ürün bilgilerini batch query ile getir (N+1 probleminden kaçın).
```

#### 3. Nasıl hızlı update ederim?
```
→ Redis Hash veya JSON set kullan:
Örn: HSET cart:123 productId:456 quantity 3
O(1) performans, çok hızlıdır.

→ Optimistic Locking (ETag, Versioning) kullan:
Aynı sepeti iki istek aynı anda güncellerse çakışmayı önler.

→ Partial update yap:
“Sepeti komple sil → tekrar yaz” yerine sadece değişen ürünü update et.

→ Event-driven yaklaşım:
Update geldiğinde bir Kafka/RabbitMQ event yayınla → DB & Redis senkronize olur.
```
#### 4. Örnek Senaryo (Redis + DB birlikte)
```
→ Kullanıcı ürünü sepete ekler → API çağrısı alır.
→ API önce Redis’te günceller (cart:userId).
→ Checkout sırasında Redis’teki sepet alınır, DB’ye yazılır (kalıcı hale gelir).
→ Redis’te TTL (time to live) koy → mesela 7 gün işlem yapılmazsa otomatik silinsin.
```
#### 5. Spring Boot Örneği (Redis ile)
```
@Service
public class CartService {

    private final RedisTemplate<String, Object> redisTemplate;
    private final String CART_KEY_PREFIX = "cart:";

    public CartService(RedisTemplate<String, Object> redisTemplate) {
        this.redisTemplate = redisTemplate;
    }

    public void addToCart(String userId, String productId, int quantity) {
        String key = CART_KEY_PREFIX + userId;
        redisTemplate.opsForHash().put(key, productId, quantity);
        redisTemplate.expire(key, Duration.ofDays(7)); // TTL
    }

    public Map<Object, Object> getCart(String userId) {
        String key = CART_KEY_PREFIX + userId;
        return redisTemplate.opsForHash().entries(key);
    }

    public void removeFromCart(String userId, String productId) {
        String key = CART_KEY_PREFIX + userId;
        redisTemplate.opsForHash().delete(key, productId);
    }
}
```
```
✅ Özet

→ Küçük / basit projeler: localStorage + backend DB yeterli.
→ Orta / büyük ölçek: Redis + DB (hybrid model).
→ Çok büyük ölçek (Amazon, Trendyol, Hepsiburada): Redis Cluster + Kafka event + DB
(CQRS ve Event Sourcing yaklaşımı).
```

## Spring Boot’ta BatchConfig (Spring Batch) ile Cron Job kavramları hem benzer hem de farklı şeylerdir
#### 1. Spring Batch (BatchConfig)
```
→ Ne iş yapar:

Büyük veri setleri üzerinde toplu işlem (read-process-write) yapar.
Örnek: 200.000 kaydı güncellemek, dosyadan veri okumak, ETL işlemleri.

→ Nasıl çalışır:

Job → Step → Reader, Processor, Writer
Chunk’lar ile parçalı işleme (batch update)
Restart, retry, skip, transaction yönetimi hazır gelir

→ Özellikleri:

Veri yoğun işleri yönetmek için optimize edilmiştir.
Database, CSV, Excel, JMS, Kafka gibi kaynaklardan veri okuyabilir.
Spring Batch framework’ü, iş mantığını ve state managementi sağlar.
```
#### 2. Cron Job (@Scheduled)
```
→ Ne iş yapar:

Belirli zamanlarda veya periyodik olarak bir metodu çalıştırır.
Örnek: Her gece 00:00’da rapor oluşturmak, her 5 dakikada bir API çağrısı yapmak.

→ Nasıl çalışır:

Spring Boot’ta @EnableScheduling ve @Scheduled(cron = "...") ile yapılır.
Tek bir metod çağrılır, çoğunlukla küçük işleri yürütmek için uygundur.
```
3. Farklar Tablosu
```
| Özellik              | Spring Batch (BatchConfig)               | Cron Job (@Scheduled)      |
| -------------------- | ---------------------------------------- | -------------------------- |
| Amaç                 | Büyük veri işleme, ETL, toplu güncelleme | Zamanlanmış görevler       |
| Veri kaynağı         | DB, CSV, Excel, JMS, Kafka vs.           | Metod / iş mantığı         |
| Transaction yönetimi | Var (chunk, retry, skip)                 | Yok / manuel               |
| Performans           | Büyük veri setleri için optimize         | Küçük/orta işlerde yeterli |
| Zamanlama            | Spring Batch job launcher veya scheduler | @Scheduled / cron          |
| Durum yönetimi       | Job execution, Step execution, restart   | Yok                        |

```
```
✅ Yani:

Spring Batch = iş mantığı ve veri işleme
Cron Job = zamanlama ve tetikleme
```

## Batch Büyük veri işleme yöntemınde hızlı mı çalışıyor ?
```
Evet, Spring Batch büyük veri işleme yönteminde hızlı çalışabilir, ama bu tamamen kullanım
şekline ve yapılandırmaya bağlıdır.
```

#### 1. Neden hızlı çalışabilir?
```
→  Chunk-based processing:
Büyük veri seti küçük parçalara (chunk) bölünerek işlenir.
Örneğin 200.000 kayıt → chunk size 1000 → 200 batch.
Böylece transaction yönetimi ve memory kullanımı optimize edilir.

→ Batch Update / JDBC Batch:
Update veya insert işlemleri toplu (batch) olarak veritabanına gönderilir.
Tek tek kayıt göndermek yerine, birden fazla kayıt tek seferde işlenir → performans artar.

→ Transaction yönetimi:
Spring Batch, her chunk için tek bir transaction yönetir.
Gereksiz commit ve rollback’leri azaltır.

→ Restart ve Skip mekanizması:
Hata durumunda yalnızca problemli chunk tekrar işlenir, tüm veri baştan işlenmez.
```

#### 2. Performansı etkileyen faktörler
```
→ Chunk boyutu: Çok küçük → sık commit → yavaş. Çok büyük → memory problemi.
Önerilen: 500–5000 arası, veri tipine ve memory’ye göre ayarla.

→ Veritabanı optimizasyonu:
Index’ler, partitioning, batch insert/update destekleyen DB özellikleri.

→ Reader / Writer seçimi:
JDBC, JPA, Hibernate, CSV veya flat file reader hız farkı yaratır.

→ Parallel processing / Multi-threading:
Spring Batch, step’leri paralel çalıştırabilir. Çok büyük verilerde performans artışı sağlar.
```
#### 3. Özet
```
→ Spring Batch tek başına “otomatik hızlı” değildir, doğru yapılandırılırsa büyük veri
setlerinde çok hızlı çalışır.
→ Ana hız faktörleri: chunk size, batch update, transaction yönetimi, paralel processing ve
reader/writer optimizasyonu.
```

## Spring WebFlux ile Spring MVC arasındaki temel fark nedir?
```
→ Spring MVC: Thread-per-request modeli (blocking I/O).
→ Spring WebFlux: Event-loop tabanlı (non-blocking, reactive), çok daha az thread ile
yüksek concurrency sağlar.
→ Kullanım senaryosu: WebFlux → yüksek trafik, streaming API’ler; MVC → klasik CRUD uygulamaları.
```

## Reactive programming’de Mono ve Flux nedir?
```
→ Mono<T>: 0 veya 1 sonuç döner.
→ Flux<T>: 0…N sonuç döner (stream).
👉 Örn: Mono<User> (tek kullanıcı), Flux<User> (çok kullanıcı).
```

## Microservices mimarisinde Service Discovery (Eureka/Consul) neden kullanılır?
```
→ Servisler dinamik olarak scale olunca IP/port sabit kalmaz.
→ Eureka/Consul gibi discovery server’lar, servislerin birbirini bulmasını sağlar.
→ Örn: OrderService → UserService’in IP’sini bilmeden istek atabilir.
```

## Spring Cloud Config Server ne işe yarar?
```
→ Tüm microservice’lerin konfigürasyonlarını merkezi yönetmek için kullanılır.
→ Konfigürasyonlar genellikle Git repo’da tutulur.
→ Dinamik olarak config değişimi (refresh scope) yapılabilir.
```

## Circuit Breaker nedir? Spring Cloud ile nasıl uygulanır?
```
→ Amaç: Bir servis sürekli hata veriyorsa diğer servisleri korumak.
→ Resilience4j / Hystrix ile uygulanır.
→ Örn: @CircuitBreaker(name="inventoryService", fallbackMethod="fallback")
```

## Kafka ile RabbitMQ arasındaki fark nedir?
```
→ Kafka: High throughput, event streaming, partition + offset bazlı,
log mantığında çalışır. Gerçek zamanlı veri işleme (stream processing).

→ RabbitMQ: Message broker, queue tabanlı, daha klasik mesajlaşma.
```

## Spring Boot’ta Kafka consumer grupları nasıl çalışır?
```
→ Cache olarak: @EnableCaching + @Cacheable, @CacheEvict.
→ Data structure store olarak: Hash, List, Set kullanarak (örn: alışveriş sepeti).
→ Message broker olarak: Pub/Sub mekanizması.
```

## Reactive WebFlux + R2DBC nedir?
```
→ R2DBC (Reactive Relational Database Connectivity), klasik JDBC’nin reactive versiyonudur.
→ JDBC blocking çalışır → WebFlux uyumlu değil.
→ R2DBC → Non-blocking DB erişimi (Postgres, MySQL, MSSQL için destek var).
```


## Saga Pattern nedir? Microservices’te neden kullanılır?
```
→ Microservices’te dağıtık transaction problemini çözmek için kullanılan pattern.
→ Her servis kendi DB’sine sahip → klasik transaction yok.
→ Saga → işlemleri adım adım yürütür, hata olursa compensating transaction ile geri alır.
→ Örn: Sipariş → Ödeme → Stok → kargo. Ödeme başarısız olursa sipariş iptal edilir.
```

## WebFlux hangi senaryoda uygun değil?
Spring WebFlux çok güçlü ama her durumda uygun değildir. İşte detaylar:
```
✅ WebFlux’un güçlü olduğu alanlar

→ Çok yüksek concurrency (aynı anda binlerce request → streaming, chat, IoT).
→ Streaming API’ler (Server-Sent Events, WebSocket).
→ I/O bound işler (dosya okuma, başka servis çağırma, DB’den veri çekme).
→ Non-blocking driver’lar ile (R2DBC, Reactive Mongo, WebClient).
```

❌ WebFlux’un uygun olmadığı senaryolar
```
✅CPU-bound işler (ağır işlemci yükü)
→ Örn: görüntü işleme, büyük matematiksel hesaplar, AI model çalıştırma.
→ Çünkü WebFlux event-loop modeli kullanır → CPU’yu meşgul eden işler event-loop’u bloke eder,
performans düşer.
→ Çözüm: Bu tür işleri ayrı thread pool (ör. Schedulers.boundedElastic()) üzerinde çalıştırmak.

✅Blocking API / Driver kullanımı
→ Eğer kullandığın kütüphane blocking ise (örn: klasik JDBC), WebFlux’ın faydasını kaybedersin.
→ Çünkü tek bir blocking işlem event-loop’u durdurur → diğer tüm request’ler etkilenir.
→ Çözüm: R2DBC, Reactive MongoDB, Reactive Redis gibi non-blocking driver’lar kullan.

✅Düşük concurrency, basit CRUD uygulamaları
→ Örn: Küçük bir şirket içi CRUD paneli.
→ MVC daha basittir, debugging kolaydır, community daha büyüktür.
→ WebFlux burada gereksiz karmaşıklık yaratır.

✅Transaction-heavy senaryolar (RDBMS + ACID)
→ WebFlux + R2DBC ile transaction yönetimi sınırlıdır.
→ Eğer çok karmaşık SQL transaction’ların varsa (multi-step join, distributed transaction),
klasik Spring MVC + JDBC daha stabil olur.

✅Ecosystem uyumsuzluğu
→ Bazı 3rd party kütüphaneler (özellikle eski olanlar) reactive desteklemez.
→ Örn: raporlama, PDF, e-mail API’leri blocking çalışır → WebFlux’ı verimsiz hale getirir.
```
🎯 Özet
```
WebFlux = non-blocking, I/O-heavy, high concurrency uygulamalar için süper.
Spring MVC = CPU-heavy, transaction-heavy, basit CRUD için daha uygun.
```

## Reactive WebFlux’ta backpressure nedir, nasıl yönetilir?
```
→ Backpressure: Publisher’ın ürettiği veri hızının, Subscriber’ın tüketme hızını aşması.
→ Yönetim yolları: onBackpressureBuffer(), onBackpressureDrop(), limitRate() gibi
Reactor operatörleriyle kontrol edilir.
```

## Reactive WebFlux’ta thread modeli nasıl çalışır?
```
→ WebFlux Netty event-loop modeli kullanır.
→ Default: N CPU çekirdeği için 2N thread oluşturur.
→ Request processing → event-loop threadlerinde yürür, CPU-bound işler için boundedElastic
veya parallel scheduler kullanılır.
```

## Spring Cloud Gateway ile Zuul arasındaki fark nedir?
```
→ Zuul 1: Servlet (blocking I/O).
→ Spring Cloud Gateway: Netty (non-blocking, reactive).
→ Gateway → route, filter, rate limiting, circuit breaker gibi modern özellikler destekler.
```

## Distributed tracing (Zipkin/Jaeger) nasıl entegre edilir?
```
→ Spring Cloud Sleuth → microservice’ler arasında traceId ve spanId ekler.
→ Log’lar merkezi hale gelir, Zipkin/Jaeger UI’dan request flow izlenebilir.
→ Örn: traceId=123 spanId=456 → hangi servislerde gezdiği görülür.
```

## Kafka’da exactly-once delivery nasıl sağlanır?
```
→ Producer tarafında: enable.idempotence=true.
→ Transactional producer + consumer offset commit birlikte yönetilir (transactional.id).
→ Böylece duplicate veya kayıp mesaj engellenir.
```

## Redis Cluster ve Sentinel arasındaki fark nedir?
```
→ Redis Sentinel: High availability (master-slave failover).
→ Redis Cluster: Sharding + horizontal scaling.
→ Büyük verilerde Redis Cluster, yüksek availability için Sentinel.
```

## CQRS (Command Query Responsibility Segregation) nedir, Microservices’te nasıl uygulanır?
```
→ Command (yazma) ve Query (okuma) işlemleri ayrı servisler/DB’ler ile yapılır.
→ Örn: Write DB (Postgres), Read DB (ElasticSearch/Redis).
→ Microservices’te performans + ölçeklenebilirlik sağlar.
```

## Reactive Kafka (spring-kafka vs reactor-kafka) farkı nedir?
```
→ spring-kafka: Classic (blocking) consumer/producer API’si.
→ reactor-kafka: Kafka client’ını Reactive Streams (Flux/Mono) ile entegre eder.
→ WebFlux tabanlı uygulamalarda reactor-kafka tercih edilir.
```

## Saga Pattern ile Choreography ve Orchestration farkı nedir?
```
→ Choreography: Event-driven, servisler birbirine event gönderir (loosely coupled).
→ Orchestration: Merkezi bir Saga orchestrator servis, tüm adımları yönetir.
→ Trade-off: Choreography → basit ama karmaşıklaşabilir, Orchestration → merkezi kontrol ama single point of failure riski.
```

## Redis’i sadece cache değil, event streaming için nasıl kullanırsın?
```
→ Redis Streams (Kafka benzeri, log-based, consumer group destekli).
→ Event-driven microservices için hafif alternatif.
→ XADD, XREADGROUP komutları ile çalışır.
```

## JPA Nedir ?
```
JPA, Java objeleri ve ilişkisel (relational) database arasında bilgi aktarımı için kullanılan bir
standarttır. JPA bu ikisi arasında bir köprü görevi görür. JPA kullanabilmek için projeye
implemente edilmesi gerekir ve bu yüzden Java dilindeki Hibernate, TopLink gibi çeşitli ORM
araçları bilgiler konusunda bir devamlılık sağlamak için JPA kullanır. JPA aracılığıyla farklı
ORM araçları ufak birkaç ayarlama dışında yazılan kod değiştirilmeden kullanılabilir.
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
Bir bean default olarak singleton scope’a sahiptir. Bean singleton scope ile tanımlandığı zaman
mevcut application context‘imiz içerisinde o bean’den yalnızca tek bir adet initialize
edileceğini garanti ederiz. Bu bean ile yapılacak olan tüm request’ler cache’lenmiş olan aynı
nesne üzerinden yapılır. 
```
##### prototype Scope
```
Prototype ile belirlenmiş bir bean, container içerisinde çağırıldığı her request’te yeniden
oluşturulacaktır. Scope notasyonun iki farklı kullanımını aşağıda görebilirsiniz.

Prototype Scope kullandığınızda, her request geldiğinde yeni bir instance döndürür.
Diyelim ki bir setter methoduna sahip bir sınıfınız var, şimdi bu sınıf için bir bean
oluşturduğunuzda, size her zaman sınıfın yeni bir instance’sını verecek ve nesne
niteliklerini değiştirmek için setter’ı özgürce kullanıp çalışacaktır. 
```
##### request Scope
```
Request bean’i HTTP isteği geldiğinde oluşturulur. örneğin, bir “ /products” API’niz var, şimdi
controller bu isteği aldığında ve service methodunu çağırdığında, Request Scope ile bir Bean’iniz
olacak ve bu API isteği yanıtı geri gönderene kadar her zaman nesnenin aynı instance’ını alırsınız,
ancak yeni bir request geldiğinde, yeni bir instance gönderecek.
```
##### session Scope
```
Session Scope Web Uygulamalarında HTTP isteği geldiğinde oluşturulur. Mesela Spring boot uygulamanız
kullanıcı sessionlarını sürdürdüğünde, bu scope yardımcı olabilir.

Session Scope kullandığımızda, tüm Session için (kullanıcı düzeyindeki oturumda) her zaman nesnenin
aynı instance’ını return eder. Ancak kullanıcı oturumu kapandığında, yeni bir kullanıcı oturumu için
nesnenin yeni bir instance’ını alacaksınız.
```
##### application Scope
```
Bir application scope, ServletContext’in yaşam döngüsü için bean örneğini oluşturur. Bu singleton
scope’a benzer ancak aralarında farklılıklar mevcuttur. Bir bean application scope değerine
sahipken bu bean çoklu servlet tabanlı uygulamalar ile de paylaşılabilirken, singleton scope
değerine sahip bir bean yalnızca mevcut application context’i içerisinde tanımlıdır.
```

## Solid prensipleri nelerdir?
```
1-Single responsibilty: Bir nesne ya da bir sınıfın tek bir sorumluluğu olmalıdır.
2-Open-closed: Bir sınıf değişime kapalı gelişmeye açık olmalıdır.
3-Liskov's Substitution: Nesneler programın çalışmasında sorun yaratmadan kendi alt
  örnekleriyle değiştirilebilmelidir.
4-Interface Segregation: Nesneler ihtiyaç duymadıkları metotların interfacelerinden
  ayrıştırılmalıdır.
5-Dependency Inversion: Yüksek seviyeli sınıflar düşük seviyeli sınıflara bağlı olmamalı,
  her ikisi de soyut kavramlara bağlı olmalıdır.
```

## Single Responsibilty nedir?
```
Single responsibilty bir nesnenin tek bir amaçla yaratılmasını konu alır. Bağlı olduğu sınıfın
içerdiği davranışsal özellikler tek bir amaca uygun olmalı başka bir davranış göstermemelidir.
Örneğin bir çalışan sınıfı içerisinde vergi hesaplama fonskiyonu bulunamaz. Bu single responsibilty
prensibine aykırı bir kod yazım şeklidir.
```

## Dependency Injection nedir?
```
"Dependency Inversion" prensibinin uygulanmasını içeren bir patterndir.Dependency Injection
tekniğinde bağımlılık oluşturacak parçalarının ayrılıp, bunların sisteme dışarıdan verilmesi
(enjekte edilmesi) ile meydana gelir. Temel olarak 3 tür DI vardır. Bunlar;

- Constructor Injection,
- Setter Injection,
- Method Injection 
Tüm yöntemler bağımlı olan sınıfları dışarıdan enjekte etmeye dayanır.
```

## DAO nedir?
```
DAO Data Access Object ifadesini: Bu araç geliştiricilere özellikle Java kaynaklı veri erişim
araçları ile daha kolay çalışma imkanı sunar. Bir yazılım uygulamasında veritabanı veya diğer
veri kaynaklarına erişimi sağlayan bir tasarım desenidir. DAO ile diğer katmanlar etkilenmeden
veritabanı ve bilgi bankası değiştirilebilir. 
```

## @Autowire ve @Qualifier ?
```
Bu kombinasyon türü uygulamada birçok farklı türde tekil bean bulunduğunda kullanılır. Bu
kombinasyon her bir ayrı bean'i farklılaştırır.

@Autowired annotasyonu kullanıldığında Spring, bağımlılığı otomatik olarak enjekte eder.
Ancak birden fazla aday bean olduğunda, hangi bean’in kullanılması gerektiğini belirtmemiz
gerekiyor. İşte @Qualifier annotasyonu bu seçimi yapmamızı kolaylaştırır.
```

## Circuat Breaker nedir ?
```
Circuit Breaker, bir servisin aşırı yük altında olduğunu veya düzgün çalışmadığını tespit
ettiğinde, otomatik olarak o servise gelen istekleri keser. Bu sayede sistem, tek bir
servisin başarısızlığından dolayı tamamen çökme durumuna düşmekten korunmuş olur.
```
##### spring hystrix ?
```
https://medium.com/@SametAkgul/circuit-breaker-pattern-e5311f670c2e
```
```
https://medium.com/trendyol-tech/nedir-bu-circuit-breaker-pattern-2d3d34948767
```

##### spring resilience4j?
```
https://umitsamimi.medium.com/circuit-breaker-resilience4j-7e1082610c52
```


## Spring Boot Interceptor Nedir?
```
Interceptor, Spring MVC paketinde bulunan bir sınıftır. HTTP isteklerinin öncesi, sonrası ve
tamamlandıktan sonra yapılması gereken işlemleri bu sınıf aracılığı ile handle edebilmekteyiz.

Gelen isteklerin endpointe ulaşmadan önce işlenmesini sağlamamıza yarayan bir sınıftır. Bir
servlete benzer ve DispatcherServlet ten sonra bulunmaktadır. HTTP isteklerini kontrol etmek
için kullanılır. İstek başlamadan önce çağrılır ve HTTP isteği ile ilgili bilgileri içeren
HttpServletRequest nesnesini ve HTTP isteği ile ilgili yanıtı döndürecek HttpServletResponse
nesnesini alır.

Ref : 
https://blog.burakkutbay.com/spring-boot-interceptor-nedir-uygulama-ornegi.html/

Spring MVC'de interceptor'lar işlemeden önce, işleme sırasında ve işleme sonrasında bir
istemcinin talebini yerine getirmek için kullanılır. Kodda istenmeyen herhangi bir tekrardan
sakınmak için muhteşem bir araçtır.
```

## Spring IOC Container ?
```
Spring IoC Container, Spring Framework'ün çekirdeğidir. Bu konteyner, nesneleri oluşturur,
nesneleri birbirine bağlar, bağımlılıklarını yapılandırır ve tüm yaşam döngüsünü yönetir.

Inversion of control bir yazılım tasarım prensibidir. Ioc ile Uygulama içerisindeki obje
instance’larının yönetimi sağlanarak, bağımlılıklarını en aza indirgemek amaçlanmaktadır.
Projenizdeki bağımlılıkların oluşturulmasını ve yönetilmesini geliştiricinin yerine,
framework’ün yapması olarak da açıklanır.

Framework‘in üzerinde çalıştığımız da görülüyor ki; frameworkler birçok işi kendisi yapmakta
ve bizim kodumuzu çalıştırmak için framework gerekli kaynakları ve çalışması gereken
metotları oluşturup, yönetmektedir. Yazdığımız kod bloğu çalışacağı zaman, framework bizim
kodumuzu çağırır ve çalıştırır daha sonra kontrol yeniden framework’e geçmesi olayının tümüne
Inversion Of Control adı verilmektedir.
```

## Microservices ler arası iletişim kurma yöntemleri nelerdir?
```
- RestTemplate
- Feign Client
- GRPC
```


# HIBERNATE Mulakat soruları

## Hibernate Nedir ?
```
Hibernate yazılım nesnelerin, ilişkisel veri tabanlarındaki (relational databases) kayıtlara
nasıl karşılık geldiğini yürüten bir teknolojidir.

Java programlama dilinde kullanılan açık kaynaklı bir nesne/ilişkisel eşleme (ORM) aracıdır.
Hibernate, veri tabanı işlemlerini, Java sınıfları arasında doğrudan ilişki kurmak yerine
nesnelerin saklanması ve yönetilmesi yoluyla yönetir.
```

Ref : https://www.turkninja.com/2024/02/hibernate-ileri-seviye-interview.html

## Hibernate FetchType EAGER - LAZY Farkları ?
```
#FetchType : Aralarında ilişki bulunan entitylerden bir tarafı yüklerken diğer tarafın
yüklenme stratejisini belirlememize olanak sağlar.

EAGER kullanırsak nesneyi veritabanından çekerken EAGER olan tüm nesneleri de
beraberinde çekeriz.

LAZY kullanırsak, ihtiyaç duyduğumuzda ilgili veriler çekilecektir.
```

## Hibernate'de Lazy Loading nedir ve nasıl çalışır ?
```
Lazy Loading, bir nesnenin ilişkili nesnelerinin ihtiyaç duyulduğunda, yani erişildiğinde
yüklenmesi yöntemidir. Bu, gereksiz veri yüklemeyi önlemek ve performansı artırmak için
kullanılır. Hibernate, proxy nesneleri veya bytecode enhancement kullanarak lazy loading'i
gerçekleştirir.
```

## Hibernate'de @Entity ve @Table annotasyonlarının farkı nedir?
```
@Entity: bir sınıfın bir veritabanı tablosuna karşılık geldiğini Hibernate'e belirtir.

@Table: sınıfın eşleştirildiği tablonun adını ve isteğe bağlı olarak schema adını belirlemek
için kullanılır.

@Entity zorunludur, ancak @Table kullanımı isteğe bağlıdır; eğer kullanılmazsa, sınıf adı
tablo adı olarak varsayılır.
```

## Hibernate'de Optimistic ve Pessimistic Kilitlenme nedir?
```
Optimistic Kilitlenme, veri çakışmalarını önlemek için sürüm numarası veya zaman damgası
kullanır. Veri güncellenmeden önce, sürüm numarası veya zaman damgasının değişip
değişmediği kontrol edilir.

Pessimistic Kilitlenme ise, bir kaynağa erişim sırasında veritabanı seviyesinde kilit
kullanır, böylece diğer işlemler o kaynağı değiştiremez veya okuyamaz.

Optimistic kilitlenme genellikle okuma yoğun uygulamalarda tercih edilirken, Pessimistic
kilitlenme yazma yoğun işlemlerde veya yüksek çakışma riski olan durumlarda kullanılır.
```

## Hibernate'de cascade türleri nelerdir ve nasıl kullanılır ?
```
Hibernate'de cascade türleri, bir nesne üzerinde yapılan işlemlerin ilişkili nesnelere nasıl
uygulanacağını belirler. Ana cascade türleri: ALL, PERSIST, MERGE, REMOVE, REFRESH, DETACH.

Örneğin,
bir Parent nesnesi Child nesneleri ile bir ilişki içindeyse ve Parent nesnesi kaydedildiğinde
(PERSIST) veya güncellendiğinde (MERGE) Child nesnelerinin de otomatik olarak kaydedilmesi
veya güncellenmesi isteniyorsa, ilgili cascade türü ilişkide belirtilir.
```

## Hibernate Query Plan Cache nedir ve performans üzerindeki etkisi nedir?
```
Hibernate Query Plan Cache, sorgu planlarını önbelleklemek için kullanılır. Bu, aynı sorgunun
tekrar tekrar çalıştırılması durumunda, sorgu derleme süresini azaltarak performansı artırır.
Önbellek, sorgu metni ve bağlamı (örneğin, parametre türleri) bazında sorgu planlarını saklar.
Bu özellik, özellikle karmaşık sorguların ve sık çalıştırılan sorguların olduğu uygulamalarda
önemli performans iyileştirmeleri sağlayabilir.
```

## Hibernate'de N+1 sorgu problemi nedir ve nasıl çözülür?
```
N+1 sorgu problemi, bir entity ve onun ilişkili nesnelerini yüklerken ortaya çıkan bir performans
sorunudur. Örneğin, bir Parent entity'si ile ilişkili çok sayıda Child entity'sini yüklerken,
ilk olarak Parent entity'si için bir sorgu çalıştırılır ve ardından her bir Child için ayrı ayrı
sorgular çalıştırılır. Bu, toplamda 1 (parent için) + N (N child için) sorgu anlamına gelir ve
özellikle N'nin büyük olduğu durumlarda ciddi bir performans düşüklüğüne yol açabilir.
```

# DATABASE Mulakat soruları

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
Hash daha çok eşitlik anında kullanılabilen bir index türüdür. Oluşum hızı index yaratma
süresi açısından Btree’ye göre çok daha fazladır. Ancak kapladığı alan bakımından Btree’ye
göre çok daha az bir yer kaplar. Çünkü Btree ağaç yapısında tutulurken, hash flat bir yapıda
tutulmaktadır.

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
indexlemede, indexler tutulurken bloklar içerisindeki en büyük ve en küçük değerler baz alınır.
B-tree’nin aksine blok içersinde sıralanmış tüm değerler değil, sadece min ve max değerler
tutulur. Eski adıyla min-max indextir.

B-tree yaratıldığında 8Kb’lık veri setlerinin tümünü saklayacak şekilde bir indexleme yapar.
Ancak BRIN ındex 8Kb’lık bloklardan sadece minumum ve maximum değerleri alarak index
halinde saklar.

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
Generalized Inverted Index ile her kelime için bir index ve bu indexin içinde aranan ifadenin
geçtiği yerlerin listesini sıkıştırılmış olarak tutar.

- Bir kolonda array gibi çoklu verinin olması durumlarında kullanılabilir. Yani metin
  içinde aramalarda kullanılması önerilir
- “Full text search” işlerinde kullanılabilir.
- JSONB üzerinde yapılan aramalarda tercih edilebilir.
- Range ve array veri tiplerinde kullanılabilir
- ILIKE ile birlikte ‘%abc%’ şeklindeki aramalarda btree verimli çalışmaz. GIN tercih edilebilir.
```

##### GIST Index
```
Generalized search tree, full text search için güçlü diğer bir adaydır. Btree karşılaştırma yapıları
için kullanılırken, GIST’te ağaç yapısında veri tutmasına karşın daha çok modern veritabanlarındaki
geodata, text documents gibi operatorler için kullanılmaktadır.

- Aynı kolonda değerlerin başka satırlarda çakışması durumlarında kullanılabilir.
- Indexleme yöntemidir ve bu index tipinden birçok index türetilebilir.
- “Full text search” işlerinde kullanılabilir.
- Geometrik veri türlerini indexlemek için kullanılırlar.
```
## Optimistic Lock Nedir ?
```
Optimistic, yani iyimser eş zamanlılık kontrolünde aynı anda bir kaydın update edilmeyeceği
varsayılır ve birden fazla session aynı kaydı update etmek için erişilebilir. Eğer aynı
kayıt birden fazla kişi tarafından update edilirse kayıtlardan biri iptal olur ve kullanıcıya
iptal olduğuna dair bilgilendirme yapılır.
```

## Pessimistic Lock Nedir ?
```
Pessimistic, yani kötümser eş zamanlılık kontrolünde bir kullanıcı bir kaydı değiştirmek istediğinde
o kayda kilit koyar ve o kaydı başkası değiştiremez. İlk değiştirmeye çalışan kişi kaydı
değiştirdikten sonra değiştirilen kayıt üzerindeki kilit açılır ve diğer değiştirmek isteyenler
artık değiştirebilir hale gelir.
```

## Transaction İsolation ? 
```
https://www.buraksenyurt.com/post/Transaction-larda-Izolasyon-Seviyeleri-(Isolation-Level)-1-bsenyurt-com-dan
```
```
https://www.buraksenyurt.com/post/Transaction-larda-Izolasyon-Seviyeleri-2-(IsolationLevel-Numaralandc4b1rc4b1cc4b1sc4b1)-bsenyurt-com-dan
```

## Oracle Explain Plan Kullanımı ? 
```
https://medium.com/yapi-kredi-teknoloji/oracle-explain-plan-kullan%C4%B1m%C4%B1-a0b5b746018e
```

## 3. part bir servise istek attığında hata alırsan yapılan işlemleri nasıl geri alırsın ? 
```
saga pattern ile yapılabilir. Saga pattern ile konuya özel açıklama yapılması iyi olur.
```

## CQRC nedir?
```
https://sefikcankanber.medium.com/cqrs-command-query-responsibility-segregation-nedir-16b196376389
```

## Apache Kafka ve Rabbit MQ arasındaki farklar nelerdir ?
```
https://aws.amazon.com/tr/compare/the-difference-between-rabbitmq-and-kafka/
```

## Saga Pattern nedir ?
```
https://sefikcankanber.medium.com/saga-pattern-nedir-e4a447bef361
```

## Domain Driven Design (DDD) ?
```
https://medium.com/@avniozunlu/domain-driven-design-ddd-151c90472914
```
## Domain Driven Design Nedir?
```
https://medium.com/@avniozunlu/domain-driven-design-ddd-151c90472914
```




# Java ve Spring Mülakat Soruları ve Cevapları

## İçindekiler

1.  [Java Temelleri](#java-temelleri) (8 Soru)
2.  [Spring Framework](#spring-framework) (8 Soru)
3.  [Spring Boot](#spring-boot) (8 Soru)
4.  [Spring Security](#spring-security) (8 Soru)
5.  [Spring Cloud](#spring-cloud) (8 Soru)

## Java Temelleri

1.  **Soru:** Java'da "OOP" (Nesne Yönelimli Programlama) prensipleri nelerdir? Açıklayınız.
    **Cevap:** OOP'nin temel prensipleri şunlardır:
    * **Encapsulation (Kapsülleme):** Verileri ve bu veriler üzerinde işlem yapan metotları bir arada tutmaktır. Erişim belirleyiciler (public, private, protected) ile kontrol sağlanır.
    * **Inheritance (Kalıtım):** Bir sınıfın (alt sınıf/türetilmiş sınıf) başka bir sınıfın (üst sınıf/temel sınıf) özelliklerini ve davranışlarını miras almasıdır. Kodun yeniden kullanılabilirliğini artırır.
    * **Polymorphism (Çok Biçimlilik):** Bir nesnenin farklı biçimlerde davranabilme yeteneğidir. Metot aşırı yüklemesi (method overloading) ve metot geçersiz kılma (method overriding) ile sağlanır.
    * **Abstraction (Soyutlama):** Karmaşık gerçekliği basitleştirerek sadece ilgili detayları göstermektir. Abstract sınıflar ve interface'ler ile sağlanır.

2.  **Soru:** `==` operatörü ile `.equals()` metodu arasındaki fark nedir?
    **Cevap:**
    * `==` operatörü, primitive veri tipleri için değer eşitliğini, referans tipleri için ise nesnelerin bellek adreslerinin eşitliğini kontrol eder.
    * `.equals()` metodu, Object sınıfında tanımlanmış bir metottur ve varsayılan olarak referans eşitliğini kontrol eder. Ancak, String, Integer gibi birçok sınıf bu metodu nesnelerin içeriklerinin eşitliğini kontrol edecek şekilde geçersiz kılmıştır (override). Özel sınıflarınızda da içerik eşitliğini kontrol etmek için `.equals()` metodunu geçersiz kılmanız önerilir.

3.  **Soru:** Java'da Garbage Collection (Çöp Toplama) nasıl çalışır?
    **Cevap:** Java'da otomatik bellek yönetimi sağlayan bir süreçtir. JVM (Java Virtual Machine), artık erişilmeyen (referansı olmayan) nesneleri periyodik olarak tespit eder ve bu nesnelerin kapladığı bellek alanını serbest bırakır. Bu sayede programcının manuel bellek yönetimiyle uğraşmasına gerek kalmaz.

4.  **Soru:** Exception (İstisna) nedir ve Java'da exception handling (istisna yönetimi) nasıl yapılır?
    **Cevap:** Exception, programın normal akışını bozan çalışma zamanı olaylarıdır. Java'da istisna yönetimi `try-catch-finally` blokları ve `throws` anahtar kelimesi ile yapılır.
    * `try`: İstisna oluşabilecek kod bloğu içine alınır.
    * `catch`: Belirli bir türdeki istisna yakalandığında çalışacak kod bloğudur. Birden fazla `catch` bloğu olabilir.
    * `finally`: `try` bloğu başarılı bir şekilde tamamlanmış olsa da, bir istisna oluşmuş olsa da her zaman çalışacak kod bloğudur (genellikle kaynakların serbest bırakılması için kullanılır).
    * `throws`: Bir metodun belirli bir istisna türünü fırlatabileceğini belirtmek için kullanılır.

5.  **Soru:** Interface (Arayüz) ve Abstract Class (Soyut Sınıf) arasındaki temel farklar nelerdir?
    **Cevap:**
    * **Interface:** Tamamen soyuttur. Metot tanımları (imzaları) içerir, ancak varsayılan olarak herhangi bir uygulama içermez (Java 8 ile gelen default metotlar hariç). Bir sınıf birden fazla interface'i implement edebilir.
    * **Abstract Class:** Hem soyut (abstract metotlar) hem de somut (uygulanmış metotlar) metotlar içerebilir. Bir sınıf sadece bir abstract sınıfı extend edebilir. Abstract sınıflar genellikle ortak davranışları alt sınıflara aktarmak için kullanılır.

6.  **Soru:** Java'da multithreading (çoklu iş parçacığı) nedir ve nasıl sağlanır?
    **Cevap:** Multithreading, bir programın aynı anda birden fazla görevi (iş parçacığı) eş zamanlı olarak çalıştırmasıdır. Java'da iki temel şekilde sağlanır:
    * `Runnable` interface'ini implement eden bir sınıf oluşturup, bu sınıfın bir nesnesini bir `Thread` nesnesine geçirerek `start()` metodunu çağırmak.
    * `Thread` sınıfını extend eden bir sınıf oluşturup, bu sınıfın bir nesnesini oluşturarak `start()` metodunu çağırmak.

7.  **Soru:** Java'da Collection Framework nedir ve en sık kullanılan Collection türleri nelerdir?
    **Cevap:** Java Collection Framework, nesne gruplarını (koleksiyonları) temsil etmek ve yönetmek için birleşik bir mimari sağlayan bir dizi interface ve sınıftır. En sık kullanılan Collection türleri şunlardır:
    * **List:** Sıralı ve tekrar eden elemanlara izin verir (ArrayList, LinkedList).
    * **Set:** Sırasız ve tekrar etmeyen elemanlara izin verir (HashSet, TreeSet).
    * **Map:** Anahtar-değer çiftlerini saklar (HashMap, TreeMap, LinkedHashMap).

8.  **Soru:** Final anahtar kelimesinin Java'daki farklı kullanım alanlarını açıklayınız.
    **Cevap:**
    * **Sınıflarda (`final class`):** Bir sınıfın alt sınıf oluşturulmasını engeller.
    * **Metotlarda (`final method`):** Bir metodun alt sınıflar tarafından geçersiz kılınmasını (override) engeller.
    * **Değişkenlerde (`final variable`):** Bir değişkene sadece bir kez değer atanabileceği anlamına gelir. İlklendirildikten sonra değeri değiştirilemez (sabit gibi davranır).

## Spring Framework

1.  **Soru:** Spring Framework'ün temel prensipleri nelerdir?
    **Cevap:** Spring Framework'ün temel prensipleri şunlardır:
    * **Dependency Injection (DI - Bağımlılık Enjeksiyonu):** Nesnelerin bağımlılıklarının (diğer nesneler) dışarıdan sağlanmasıdır. Bu, gevşek bağlı (loosely coupled) ve daha test edilebilir kod oluşturmayı sağlar.
    * **Inversion of Control (IoC - Kontrolün Tersine Çevrilmesi):** Nesnelerin oluşturulması ve yönetilmesi sorumluluğunun framework'e devredilmesidir.
    * **Aspect-Oriented Programming (AOP - Yönlendirilmiş Programlama):** Uygulamanın farklı bölümlerinde tekrar eden kesen ilgileri (logging, transaction management gibi) merkezi bir şekilde yönetmeyi sağlar.
    * **Data Access Abstraction:** Farklı veri erişim teknolojileri için tutarlı bir arayüz sunar.
    * **Model-View-Controller (MVC):** Web uygulamaları geliştirmek için kullanılan bir tasarım desenidir.

2.  **Soru:** Dependency Injection (DI) Spring'de nasıl uygulanır? Farklı DI türleri nelerdir?
    **Cevap:** Spring'de DI temel olarak iki şekilde uygulanır:
    * **Constructor Injection (Kurucu Enjeksiyonu):** Bağımlılıklar sınıfın kurucu metodu aracılığıyla enjekte edilir. Genellikle zorunlu bağımlılıklar için tercih edilir.
    * **Setter Injection (Setter Metot Enjeksiyonu):** Bağımlılıklar sınıfın setter metotları aracılığıyla enjekte edilir. İsteğe bağlı bağımlılıklar için kullanılabilir.
    * **Field Injection (Alan Enjeksiyonu):** `@Autowired` anotasyonu doğrudan alan üzerine uygulanarak bağımlılıklar enjekte edilir. Genellikle önerilmez çünkü birim testini zorlaştırabilir.

3.  **Soru:** Spring Bean nedir ve Bean yaşam döngüsü nasıldır?
    **Cevap:** Spring Bean, Spring IoC konteyneri tarafından yönetilen bir nesnedir. Bean yaşam döngüsü şu aşamaları içerir:
    1.  **Bean Definition (Bean Tanımı):** Spring konfigürasyon dosyalarında (XML veya anotasyonlar aracılığıyla) bean'in nasıl oluşturulacağı tanımlanır.
    2.  **Bean Instantiation (Bean Oluşturma):** Spring konteyneri, bean tanımına göre bean'in bir örneğini oluşturur.
    3.  **Dependency Injection (Bağımlılık Enjeksiyonu):** Bean'in bağımlılıkları enjekte edilir.
    4.  **Initialization (Başlatma):** Bean özelliklerinin ayarlanması ve özel başlatma metotlarının (örneğin `@PostConstruct` anotasyonlu metotlar veya `InitializingBean` interface'indeki `afterPropertiesSet()` metodu) çalıştırılması.
    5.  **Usage (Kullanım):** Bean uygulama içinde kullanılır.
    6.  **Destruction (Yok Etme):** Uygulama kapandığında veya bean kapsamı sona erdiğinde, özel yok etme metotları (örneğin `@PreDestroy` anotasyonlu metotlar veya `DisposableBean` interface'indeki `destroy()` metodu) çalıştırılır ve bean yok edilir.

4.  **Soru:** Spring'de `@Component`, `@Service`, `@Repository`, `@Controller` anotasyonlarının rolleri nelerdir?
    **Cevap:** Bu anotasyonlar, sınıfları Spring tarafından yönetilen bean'ler olarak işaretlemek için kullanılır ve aynı zamanda anlamsal bir rol de taşırlar:
    * `@Component`: Genel amaçlı bir Spring bean'ini işaretler. Diğer özel anotasyonların temelidir.
    * `@Service`: İş mantığı katmanındaki (service layer) bean'leri işaretler.
    * `@Repository`: Veri erişim katmanındaki (data access layer) bean'leri işaretler. Genellikle veritabanı etkileşimlerini yöneten sınıflar için kullanılır. Ayrıca platforma özgü istisnaları Spring'in `DataAccessException` hiyerarşisine çevirme konusunda yardımcı olur.
    * `@Controller`: Web katmanındaki (presentation layer) bean'leri işaretler ve gelen web isteklerini işlemek için kullanılır.

5.  **Soru:** Spring AOP (Aspect-Oriented Programming) nedir ve temel kavramları nelerdir?
    **Cevap:** Spring AOP, uygulamanın farklı bölümlerinde tekrar eden kesen ilgileri (cross-cutting concerns) merkezi bir şekilde yönetmeyi sağlayan bir programlama paradigmasıdır. Temel kavramları şunlardır:
    * **Aspect:** Kesen bir ilgiyi (örneğin logging, güvenlik) uygulayan modüldür. Java'da genellikle bir sınıf ve anotasyonlar (örneğin `@Aspect`) ile tanımlanır.
    * **Join Point:** Uygulamada bir aspect'in uygulanabileceği bir noktadır (örneğin bir metot çağrısı, bir exception fırlatılması).
    * **Advice:** Bir join point'te gerçekleştirilecek eylemdir (örneğin bir metot çağrısı öncesinde loglama yapmak). Farklı advice türleri vardır: `@Before`, `@After`, `@AfterReturning`, `@AfterThrowing`, `@Around`.
    * **Pointcut:** Hangi join point'lere advice'ın uygulanacağını belirleyen bir ifadedir. Genellikle AspectJ pointcut ifadesi dili kullanılır.
    * **Weaving:** Aspect'in join point'lere uygulanması sürecidir. Compile-time, load-time veya runtime'da gerçekleşebilir.

6.  **Soru:** Spring MVC mimarisini açıklayınız.
    **Cevap:** Spring MVC (Model-View-Controller), web uygulamaları geliştirmek için kullanılan bir tasarım deseninin Spring Framework tarafından implementasyonudur. Temel bileşenleri şunlardır:
    * **Model:** Uygulamanın verilerini ve iş mantığını temsil eder.
    * **View:** Kullanıcıya gösterilecek olan arayüzü (genellikle HTML, JSP, Thymeleaf gibi şablon motorları ile oluşturulur) temsil eder.
    * **Controller:** Kullanıcıdan gelen istekleri işler, modeli günceller ve hangi view'in gösterileceğine karar verir.
    İstek akışı genellikle şu şekildedir: Kullanıcı bir istek gönderir -> DispatcherServlet bu isteği alır -> HandlerMapping uygun Controller'ı bulur -> Controller isteği işler, modeli günceller -> ViewResolver uygun View'i bulur -> View modeldeki verilerle birlikte render edilir -> Kullanıcıya cevap gönderilir.

7.  **Soru:** Spring Bean scope'ları nelerdir? En sık kullanılanları açıklayınız.
    **Cevap:** Spring Bean scope'ları, Spring konteynerinin bean örneklerini nasıl oluşturacağını ve yöneteceğini belirler. En sık kullanılan scope'lar şunlardır:
    * **singleton:** Uygulama boyunca sadece bir tane bean örneği oluşturulur ve tüm istekler için aynı örnek kullanılır (varsayılan scope).
    * **prototype:** Her istek için yeni bir bean örneği oluşturulur.
    * **request:** Her HTTP isteği için yeni bir bean örneği oluşturulur. Sadece web uygulamalarında geçerlidir.
    * **session:** Her HTTP oturumu için yeni bir bean örneği oluşturulur. Sadece web uygulamalarında geçerlidir.
    * **global-session:** Portlet tabanlı web uygulamalarında global HTTP oturumu için yeni bir bean örneği oluşturulur.
    * **application:** Web uygulamasının ServletContext yaşam döngüsü boyunca bir tane bean örneği oluşturulur. Sadece web uygulamalarında geçerlidir.
    * **websocket:** Bir WebSocket oturumunun yaşam döngüsü boyunca bir tane bean örneği oluşturulur. Sadece WebSocket uygulamalarında geçerlidir.

8.  **Soru:** Spring'de `@Autowired` ve `@Qualifier` anotasyonları ne için kullanılır?
    **Cevap:**
    * `@Autowired`: Spring IoC konteynerine, işaretlendiği alan, kurucu veya setter metodu aracılığıyla bağımlılığı otomatik olarak enjekte etmesini söyler. Spring, uyumlu tipteki bir bean'i konteynerden bulup enjekte eder.
    * `@Qualifier`: Birden fazla uyumlu tipte bean olduğunda, hangi bean'in enjekte edileceğini belirtmek için `@Autowired` ile birlikte kullanılır. `@Qualifier` anotasyonuna, enjekte edilecek bean'in adını veya özel bir niteleyici değerini belirtebilirsiniz.

## Spring Boot

1.  **Soru:** Spring Boot nedir ve Spring Framework'e göre avantajları nelerdir?
    **Cevap:** Spring Boot, Spring tabanlı uygulamaları hızlı ve kolay bir şekilde geliştirmek, yapılandırmak ve çalıştırmak için tasarlanmış bir framework'tür. Spring Framework'ün üzerine inşa edilmiştir ve aşağıdaki avantajları sunar:
    * **Hızlı Başlangıç:** Minimum yapılandırma ile bağımsız, üretim düzeyinde Spring uygulamaları oluşturmayı kolaylaştırır.
    * **Otomatik Yapılandırma (Auto-Configuration):** Bağımlılıklarınıza göre yaygın uygulama yapılandırmalarını otomatik olarak yapar.
    * **Gömülü Sunucular:** Tomcat, Jetty veya Undertow gibi gömülü sunucularla birlikte gelir, bu da uygulamaların kolayca çalıştırılmasını sağlar.
    * **Opinionated Defaults:** Çoğu kullanım senaryosu için mantıklı varsayılan yapılandırmalar sunar, ancak gerektiğinde özelleştirmeye izin verir.
    * **CLI (Command Line Interface):** Komut satırından Spring Boot uygulamalarını geliştirmek ve yönetmek için araçlar sunar.
    * **Geliştirilmiş Geliştirici Deneyimi:** Daha az boilerplate kod ve daha hızlı geliştirme döngüsü sağlar.

2.  **Soru:** Spring Boot'ta "Starters" nedir? Ne işe yararlar?
    **Cevap:** Spring Boot Starters, belirli bir işlevsellik için gereken tüm bağımlılıkları içeren bağımlılık gruplarıdır. Örneğin, `spring-boot-starter-web` web uygulaması geliştirmek için gereken tüm temel bağımlılıkları (Spring MVC, Tomcat, Jackson vb.) içerir. Starters, proje bağımlılıklarını yönetmeyi kolaylaştırır ve uyumlu bağımlılık sürümlerini bir arada tutar.

3.  **Soru:** Spring Boot uygulamasının temel yapılandırma dosyası hangisidir ve nasıl yapılandırılır?
    **Cevap:** Spring Boot uygulamasının temel yapılandırma dosyaları `application.properties` veya `application.yml` dosyalarıdır. Bu dosyalarda uygulama ayarları (sunucu portu, veritabanı bağlantı bilgileri, logging seviyeleri vb.) tanımlanır. Yapılandırma, ana kaynaklar (src/main/resources) dizinine yerleştirilerek veya komut satırı argümanları veya ortam değişkenleri aracılığıyla yapılabilir. YAML daha yapılandırılmış ve okunabilir bir format sunarken, Properties daha basit bir anahtar-değer çifti formatındadır.

4.  **Soru:** Spring Boot Actuator nedir ve hangi amaçlarla kullanılır?
    **Cevap:** Spring Boot Actuator, çalışan bir Spring Boot uygulamasının iç işleyişini izlemek ve yönetmek için kullanılan bir modü


# Spring Boot, Spring Cloud ve Mikroservis Mülakat Soruları ve Cevapları

## Spring Boot

1.  **Soru:** Spring Boot'un temel özellikleri nelerdir?
    **Cevap:** Spring Boot'un temel özellikleri şunlardır:
    * Bağımsız (stand-alone) Spring uygulamaları oluşturma yeteneği.
    * Gömülü Tomcat, Jetty veya Undertow gibi servlet konteynerleri sunması.
    * Basitleştirilmiş yapılandırma (auto-configuration) sayesinde hızlı geliştirme.
    * "Opinionated" varsayılan yapılandırmalar sunarak geliştirici kararlarını azaltması.
    * Geliştirme araçları ve Actuator gibi özellikler sunarak uygulama izleme ve yönetimi kolaylaştırması.

2.  **Soru:** Spring Boot'ta Auto-Configuration nasıl çalışır?
    **Cevap:** Spring Boot Auto-Configuration, projenize eklediğiniz bağımlılıkları analiz ederek, uygulamanız için gerekli olan bean'leri otomatik olarak yapılandırır. Bu işlem `@EnableAutoConfiguration` anotasyonu (genellikle `@SpringBootApplication` içinde bulunur) ile tetiklenir. Spring Boot, `spring.factories` dosyalarında tanımlanan `AutoConfiguration` sınıflarını yükler ve belirli koşullar sağlandığında bu sınıflardaki bean tanımlarını IoC konteynerine ekler.

3.  **Soru:** Spring Boot Actuator'ın temel kullanım alanları nelerdir? Hangi önemli endpoint'leri sunar?
    **Cevap:** Spring Boot Actuator, çalışan bir Spring Boot uygulamasının sağlık durumu, metrikleri, yapılandırması ve diğer operasyonel bilgilerini izlemek ve yönetmek için kullanılır. Önemli endpoint'leri şunlardır:
    * `/health`: Uygulamanın sağlık durumunu gösterir.
    * `/info`: Uygulama hakkında özel bilgileri (örneğin sürüm, build bilgileri) gösterir.
    * `/metrics`: Uygulama metriklerini (bellek kullanımı, CPU kullanımı, HTTP istek sayıları vb.) gösterir.
    * `/env`: Uygulama ortam özelliklerini gösterir.
    * `/beans`: Spring IoC konteynerindeki tüm bean'leri listeler.
    * `/configprops`: `@ConfigurationProperties` ile tanımlanmış yapılandırma özelliklerini gösterir.
    * `/mappings`: Uygulamadaki tüm request mapping'lerini (endpoint'leri) listeler.
    * `/loggers`: Uygulamanın logger yapılandırmasını yönetmeye olanak tanır.

4.  **Soru:** Spring Boot CLI (Command Line Interface) ne işe yarar?
    **Cevap:** Spring Boot CLI, Spring Boot uygulamalarını hızlı bir şekilde prototiplemek ve çalıştırmak için komut satırı araçları sunar. Özellikle basit uygulamalar veya hızlı denemeler için faydalıdır. Java kodunu derleme ve çalıştırma süreçlerini basitleştirir.

5.  **Soru:** Spring Boot'ta farklı profiller nasıl yönetilir? Ne zaman kullanılırlar?
    **Cevap:** Spring Boot'ta farklı ortamlar (development, test, production vb.) için farklı yapılandırmalar tanımlamak için profiller kullanılır. `application-{profilAdı}.properties` veya `application-{profilAdı}.yml` şeklinde isimlendirilmiş yapılandırma dosyaları oluşturularak profiller tanımlanır. Uygulama başlatılırken `--spring.profiles.active={profilAdı}` argümanı ile veya `spring.profiles.active` ortam değişkeni ile aktif profil belirtilebilir.

6.  **Soru:** Spring Boot'ta gömülü sunucu (embedded server) kullanmanın avantajları nelerdir?
    **Cevap:** Gömülü sunucu kullanmanın avantajları şunlardır:
    * Uygulamanın bağımsız bir şekilde çalıştırılabilmesi (JAR olarak paketlenebilir).
    * Dağıtımın kolaylaşması (harici bir sunucu kurulumuna gerek kalmaz).
    * Geliştirme sürecinin hızlanması (dahili sunucu ile hızlı test ve yineleme).
    * Test ortamlarının kolayca kurulabilmesi.

7.  **Soru:** Spring Boot uygulamasını production ortamına nasıl deploy edersiniz? Farklı yöntemler nelerdir?
    **Cevap:** Spring Boot uygulamalarını production ortamına deploy etmek için farklı yöntemler vardır:
    * **JAR olarak çalıştırma:** Gömülü sunucu ile paketlenmiş JAR dosyasını `java -jar` komutuyla çalıştırmak.
    * **WAR olarak deploy etme:** Uygulamayı geleneksel bir Java EE uygulama sunucusuna (Tomcat, JBoss vb.) WAR dosyası olarak deploy etmek (bu durumda `spring-boot-starter-tomcat` gibi bağımlılıkların `provided` olarak işaretlenmesi gerekebilir).
    * **Docker konteyneri:** Uygulamayı bir Docker imajı içine alıp, konteyner orkestrasyon araçları (Kubernetes, Docker Swarm vb.) ile yönetmek.
    * **Cloud platformlarına deploy etme:** AWS, Azure, Google Cloud gibi bulut platformlarının sunduğu özel servisler (örneğin AWS Elastic Beanstalk, Azure App Service, Google Cloud Run) aracılığıyla deploy etmek.

## Spring Cloud

1.  **Soru:** Spring Cloud nedir ve mikroservis mimarisindeki rolü nedir?
    **Cevap:** Spring Cloud, mikroservis mimarisi oluşturmayı kolaylaştıran bir dizi araç ve kütüphane sağlayan bir şemsiye projedir. Mikroservisler arasındaki iletişimi, yapılandırma yönetimini, servis keşfini, devre kesici (circuit breaker) mekanizmalarını, API ağ geçidini ve daha birçok dağıtık sistem sorununu çözmek için çözümler sunar.

2.  **Soru:** Spring Cloud Config Server ne işe yarar? Avantajları nelerdir?
    **Cevap:** Spring Cloud Config Server, mikroservis uygulamalarının merkezi bir yerden yapılandırılmasını sağlayan bir servistir. Git, SVN veya HashiCorp Vault gibi farklı backend'lerden yapılandırma bilgilerini okuyabilir ve istemci mikroservislere HTTP üzerinden sunar. Avantajları şunlardır:
    * Yapılandırma yönetimini merkezileştirir.
    * Yapılandırma değişikliklerinin tüm servislere kolayca yayılmasını sağlar.
    * Sürüm kontrolü ve yapılandırma geçmişi tutulabilir.
    * Güvenli yapılandırma yönetimi imkanı sunar.

3.  **Soru:** Spring Cloud Netflix Eureka nedir ve mikroservislerde servis keşfi (service discovery) için nasıl kullanılır?
    **Cevap:** Spring Cloud Netflix Eureka, mikroservislerin birbirlerini bulmasını sağlayan bir servis keşfi sunucusudur. Her mikroservis, başlatıldığında Eureka Server'a kendi adres ve port bilgilerini kaydeder. Diğer mikroservisler de Eureka Server'a danışarak ihtiyaç duydukları servisin konumunu öğrenir ve iletişim kurarlar. Bu sayede servislerin dinamik olarak ölçeklenmesi ve yer değiştirmesi kolaylaşır.

4.  **Soru:** Spring Cloud Gateway nedir ve mikroservis mimarisinde ne gibi roller üstlenir?
    **Cevap:** Spring Cloud Gateway, mikroservisler için bir API ağ geçidi (API Gateway) görevi gören bir projedir. Temel rolleri şunlardır:
    * Tek bir giriş noktası sağlayarak istemcilerin mikroservislere erişimini kolaylaştırır.
    * Yönlendirme (routing) kurallarını yönetir.
    * Güvenlik (authentication, authorization) gibi kesen ilgileri merkezi olarak yönetebilir.
    * Hız sınırlaması (rate limiting), devre kesici (circuit breaking) gibi özellikleri uygulayabilir.
    * İstek ve cevapları dönüştürebilir.

5.  **Soru:** Spring Cloud Circuit Breaker (örneğin Resilience4j) ne işe yarar? Hangi sorunları çözmeye yardımcı olur?
    **Cevap:** Spring Cloud Circuit Breaker (Resilience4j gibi kütüphaneler aracılığıyla), dağıtık sistemlerde servisler arasındaki iletişimde olası hatalara karşı dayanıklılığı artırmak için kullanılır. Bir servis çağrısı belirli bir eşiği aşan sayıda başarısız olursa, devre kesici açılır ve bir süre boyunca hatalı servise yapılan çağrıları engeller. Bu sayede sistemin tamamının çökmesi önlenir ve hatalı servisin iyileşmesi için zaman tanınır.

6.  **Soru:** Spring Cloud Load Balancer mikroservisler arasındaki yük dengelemesini nasıl sağlar?
    **Cevap:** Spring Cloud Load Balancer, Eureka gibi bir servis keşfi mekanizmasıyla entegre olarak çalışır. Bir istemci bir servise istek gönderdiğinde, Load Balancer mevcut olan servis örnekleri arasından birini seçerek isteği yönlendirir. Bu, yükün birden fazla servis örneğine eşit olarak dağıtılmasını sağlar ve tek bir servis örneğinin aşırı yüklenmesini önler. Farklı yük dengeleme algoritmaları (round-robin, random, weighted response time vb.) desteklenebilir.

7.  **Soru:** Spring Cloud Stream nedir ve mikroservisler arasında asenkron iletişimi nasıl kolaylaştırır?
    **Cevap:** Spring Cloud Stream, mikroservisler arasında olay güdümlü (event-driven) ve asenkron iletişimi basitleştiren bir framework'tür. Kafka, RabbitMQ gibi farklı mesajlaşma aracıları (message broker) için soyut bir katman sağlar. Mikroservisler, Spring Cloud Stream'in sağladığı binder'lar aracılığıyla mesaj kuyruklarına kolayca mesaj gönderebilir ve mesajları dinleyebilirler. Bu, servisler arasındaki bağımlılığı azaltır ve daha ölçeklenebilir ve esnek sistemler oluşturmaya olanak tanır.

## Mikroservis Mimarisi

1.  **Soru:** Monolitik mimari ile mikroservis mimarisinin temel farkları nelerdir? Mikroservislerin avantaj ve dezavantajları nelerdir?
    **Cevap:**
    * **Monolitik Mimari:** Tüm uygulama tek bir büyük kod tabanı ve tek bir dağıtım birimi olarak geliştirilir.
    * **Mikroservis Mimarisi:** Uygulama, bağımsız olarak dağıtılabilen küçük, özel amaçlı servislerden oluşur. Her servis kendi veritabanına ve teknoloji yığınına sahip olabilir.

    **Mikroservislerin Avantajları:**
    * **Teknolojik Çeşitlilik:** Farklı servisler farklı teknolojilerle geliştirilebilir.
    * **Ölçeklenebilirlik:** Her servis bağımsız olarak ölçeklenebilir.
    * **Hızlı Geliştirme ve Dağıtım:** Küçük ve bağımsız servisler daha hızlı geliştirilip deploy edilebilir.
    * **Hata İzolasyonu:** Bir servisteki hata diğer servisleri etkilemez.
    * **Daha İyi Organizasyon:** Küçük, odaklanmış ekipler tarafından geliştirilebilir.

    **Mikroservislerin Dezavantajları:**
    * **Dağıtık Sistem Karmaşıklığı:** Servisler arası iletişim, ağ sorunları, dağıtık veri yönetimi gibi zorluklar ortaya çıkar.
    * **Operasyonel Yük:** Daha fazla sayıda servis yönetmek gerekir.
    * **İzleme ve Hata Ayıklama Zorluğu:** Dağıtık sistemlerde izleme ve hata ayıklama daha karmaşıktır.
    * **Servisler Arası İletişim Yönetimi:** Etkili ve performanslı servisler arası iletişim mekanizmaları (REST, gRPC, mesajlaşma) gereklidir.

2.  **Soru:** Mikroservisler arası iletişimde kullanılan yaygın yöntemler nelerdir? Avantaj ve dezavantajlarını karşılaştırınız.
    **Cevap:** Yaygın iletişim yöntemleri şunlardır:
    * **REST (Synchronous):** HTTP protokolü üzerinden yapılan senkron iletişimdir. Basit ve yaygın olarak kullanılır. Dezavantajı, servisler arasındaki sıkı bağlılık ve olası performans sorunlarıdır.
    * **Mesajlaşma (Asynchronous):** Kafka, RabbitMQ gibi mesaj kuyrukları aracılığıyla yapılan asenkron iletişimdir. Daha gevşek bağlılık, daha iyi ölçeklenebilirlik ve güvenilirlik sağlar. Dezavantajı, karmaşıklık ve eventual consistency (sonunda tutarlılık) sorunlarıdır.
    * **gRPC (Synchronous/Asynchronous):** Google tarafından geliştirilen yüksek performanslı, dil bağımsız bir RPC framework'üdür. Protobuf ile veri serileştirme kullanır. Yüksek performans ve güçlü tip güvenliği sunar. Dezavantajı, bazı platformlarda ve dillerde daha az yaygın olmasıdır.

3.  **Soru:** Mikroservislerde veri yönetimi nasıl ele alınır? Her servis kendi veritabanına sahip olmanın avantajları nelerdir?
    **Cevap:** Mikroservislerde genellikle her servis kendi bağımsız veritabanına sahiptir (database per service pattern). Bunun avantajları şunlardır:
    * **Teknolojik Özgürlük:** Her servis kendi ihtiyaçlarına en uygun veritabanı teknolojisini seçebilir.
    * **İzolasyon:** Bir servisteki veri modeli veya şemasındaki değişiklikler diğer servisleri etkilemez.
    * **Ölçeklenebilirlik:** Her veritabanı servisin ihtiyaçlarına göre bağımsız olarak ölçeklenebilir.
    * **Daha İyi Performans:** Her servis kendi veri erişimini optimize edebilir.

    Ancak bu yaklaşım, dağıtık işlemler (distributed transactions) gibi veri tutarlılığı sorunlarını da beraberinde getirebilir. Bu sorunları çözmek için Saga pattern gibi yaklaşımlar kullanılabilir.

4.  **Soru:** Mikroservislerde distributed tracing (dağıtık izleme) neden önemlidir? Hangi araçlar kullanılabilir?
    **Cevap:** Mikroservislerde distributed tracing, bir isteğin birden fazla servis üzerinden geçerkenki yolunu ve her bir serviste harcadığı süreyi izlemek için kritik öneme sahiptir. Bu, performans sorunlarını tespit etmek, hataları ayıklamak ve sistemin genel davranışını anlamak için gereklidir. Kullanılabilecek araçlar arasında Zipkin, Jaeger ve Spring Cloud Sleuth (çeşitli tracing backend'lerini destekler) bulunur.

5.  **Soru:** API Gateway mikroservis mimarisinde neden gereklidir? Temel sorumlulukları nelerdir?
    **Cevap:** API Gateway, mikroservis mimarisinde istemciler için tek bir giriş noktası sağlayarak karmaşıklığı azaltır. Temel sorumlulukları şunlardır:
    * **Yönlendirme (Routing):** Gelen istekleri uygun mikroservislere yönlendirmek.
    * **Güvenlik (Authentication ve Authorization):** Kimlik doğrulama ve yetkilendirme işlemlerini merkezi olarak yönetmek.
    * **Hız Sınırlaması (Rate Limiting):** Servislerin aşırı yüklenmesini önlemek için istek hızını kontrol etmek.
    * **İstek ve Cevap Dönüşümü:** İstemci ve servisler arasındaki veri formatlarını dönüştürmek.
    * **Önbellekleme (Caching):** Sık erişilen verilere daha hızlı erişim sağlamak.
    * **İzleme ve Günlükleme:** İstekleri ve cevapları izlemek ve loglamak.

6.  **Soru:** Mikroservis mimarisinde "Contract Testing" ve "End-to-End Testing" arasındaki fark nedir? Neden önemlidirler?
    **Cevap:**
    * **Contract Testing (Kontrat Testi):** Bir servis sağlayıcısının (provider) sunduğu API kontratının (istek ve cevap formatları) tüketicisi (consumer) tarafından beklendiği gibi olduğunu doğrular. Amaç, servisler arasındaki entegrasyon sorunlarını erken aşamada tespit etmektir.
    * **End-to-End Testing (Uçtan Uca Test):** Tüm sistemin veya belirli bir iş akışının baştan sona doğru çalıştığını doğrular. Birden fazla servisin etkileşimini ve genel sistem davranışını test eder.


