## JAVA Q
### Java Sanal Makinası (JVM) Nasıl Çalışır?
```
JVM, tüm platformlarda Java kodlarını çalıştırmak üzere geliştirilmiş ve 
hemen her platforma uygun sürümü olan bir bileşendir. 
Java ile geliştirilmiş bir yazılım Java Sanal Makinası sayesinde kullanılabiliyor.
```
```
Programcının yazdığı Java kodları geliştirme ortamı tarafından yazım (syntax) hatalarına karşı kontrol edilir. 
Hatalar giderildiğinde, JDK paketindeki derleyici (compiler) aracılığı ile Java kodları 
bytecode denilen bir ara dilin kodlarına dönüştürülür. 
Üzerinde çalışılan sistemdeki JVM bu bytecode’ u yorumlar ve çalıştırır.
```
### Java’da Final Anahtar Kelimesi
```
- Final sınıf değişkenleri: Final olan bir sınıf değişkenine sadece bir kere değer ataması yapilabilir ve 
bu atama sadece sınıf konstrüktöründe gerçekleşebilir.

- Final metot parametreleri: Final olarak tanımlanmış bir metot parametresine sadece bir kere değer atanabilir. 
Metot parametrelerinin tamamen final olarak tanımlamış olmalarında büyük fayda vardır. 
Bu şekilde parametrenin metot bünyesinde değişikliğe ugrama tehlikesi ortadan kaldırılmış olur.

- Final metotlar: Final olan bir metot ne alt sınıflarca yeniden yüklenebilir 
(method overloading) ne de saklı (hidden) tutulabilir.

- Final sınıflar: Final olan bir sınıf genişletilerek bir alt sınıf oluşturulamaz.

```
### Array ve ArrayList nedir? 
```
İki veri yapısı arasındaki başlıca ve gözle görülür farklılıklardan biri Array'ın statik olmasıdır; 
bu da sabit uzunlukta bir veri türü anlamına gelir; ArrayList doğada dinamiktir, 
yani değişken uzunlukta bir veri yapısı olduğu anlamına gelir. 
Teknik terimlerle, Array nesnesi oluşturulduktan sonra Array uzunluğu değiştirilemez veya değiştirilemez. 
Aynı veri türünün elemanlarının sıralı olarak toplanmasını içerir. Java'daki diziler, C / C ++'da işlev görenden farklı çalışır. 
Öte yandan, ArrayList kendisini yeniden boyutlandırabilir ve diziler ihtiyaç duyuldukça büyüyebilir. 
Dinamik bir veri yapısı olduğu için, elemanlar listeye eklenebilir ve listeden çıkarılabilir.
```
### LinkedList ile ArrayList arasındaki fark
```
ArrayList 
ArrayList öğelerine erişim LinkedList'ten daha hızlıdır.
ArrayList öğelerinin işlenmesi, LinkedList'ten daha yavaştır.
ArrayList, bir Liste olarak çalışır.

LinkedList 
LinkedList öğelerine erişim, ArrayList'ten daha yavaştır.
LinkedList öğelerinin işlenmesi, ArrayList'ten daha hızlıdır.
LinkedList, bir Liste ve Kuyruk olarak çalışır.
```
### Blockİng Queue 
- Java’da Multithreading – Bölüm 7: Producer-Consumer Yapısı
- Producer (Üretici) ve Consumer (Tüketici) yapısı hem günlük hayatta hem de programlama yaparken sıkça karşılaşabileceğimiz bir yapıdır. 
- Producer kuyruğa bir şeyler ekler, Consumer ise bu kuyrukta bir şeyler oldukça sırayla alır ve ne yapması gerekiyorsa yapar. 
```
https://ufukuzun.wordpress.com/2015/05/02/javada-multithreading-bolum-7-producer-consumer-yapisi/

Producer ve Consumer birbirinden bağımsız iki ayrı thread halinde gerçekleştirilebilir. 
Ancak burada yine ortak bir veri kaynağımız olduğunu gözden kaçırmayalım: Kuyruk (Queue). 
Yine yardımımıza yetişen java.util.concurrent.* paketinden “thread-safe” bir yardımcı sınıf olan “BlockingQueue” oluyor. 
BlockingQueue aslında bir arabirim (interface) ve biz onun gerçekleştirimlerinden (implementation) biri olan 
“ArrayBlockingQueue” sınıfını kullanacağız. ArrayBlockingQueue tipinde bir kuyruk oluştururken bir kapasite belirtiriz. 
Bu kapasite dolu ise kuyruğa yeni eleman eklemek isteyen thread bekletilir. Benzer şekilde eğer kuyrukta eleman yoksa 
kuyruktan eleman almak isteyen thread kuyrukta eleman oluncaya kadar bekletilir.
```
```
public class Application {

    private static BlockingQueue queue = new ArrayBlockingQueue<>(10);

    public static void main(String[] args) throws InterruptedException {
        Thread producerThread = new Thread(() -> { produce(); });

        Thread consumerThread = new Thread(() -> { consume(); });

        producerThread.start();     consumerThread.start();
	
        producerThread.join();      consumerThread.join();
    }

    private static void produce() {
        Random random = new Random();
        while (true) {
            try {
                queue.put(random.nextInt(100));
            } catch (InterruptedException e) {
            }
        }
    }

    private static void consume() {
        while (true) {
            try {
                Thread.sleep(100);
                Integer value = queue.take();
                System.out.print("Alınan sayı: " + value + ", Kuyruğun boyutu: " + queue.size());
            } catch (InterruptedException e) {
            }
        }
    }
}

```
### ManyToMany
```

```
### FetchType.EAGER VS FetchType.LAZY
```
FetchType.EAGER
Elimizde yürütülen projeleri (Proje) ve bu projelerde çalışanları(Calisan) tuttuğumuz iki entity olsun. 
Projeler ve çalışanlar arasında bir ilişki bulunduğundan veritabanından Proje entitysini yüklediğimizde ilişkili olduğu 
Calisan tablosununda yüklenmesini istiyorsak FetchType tipini fetch=FetchType.EAGER olarak belirleriz.

FetchType.LAZY 
Bunun aksine Proje entitysini yüklediğimizde Calisan entitysinin yüklenmesini istemiyorsak yani ihtiyaç olması 
halinde Calisan entitysini yüklemek istiyorsak FetchType tipini fetch=FetchType.LAZY olarak belirleriz. 
```
### Statement ve PreparedStatement arasındaki farklar
```
1    PreparedStatement helps us in preventing SQL injection attacks because it automatically escapes the special characters.

2    PreparedStatement allows us to execute dynamic queries with parameter inputs.

3    PreparedStatement provides different types of setter methods to set the input parameters for the query.

4    PreparedStatement is faster than Statement. It becomes more visible when we reuse the PreparedStatement or use it’s 
     batch processing methods for executing multiple queries.
     
5    PreparedStatement helps us in writing object Oriented code with setter methods whereas with Statement we have to use
     String Concatenation to create the query. If there are multiple parameters to set, writing Query using String concatenation 
     looks very ugly and error prone.
```
### URL ve URI nedir. Arasındaki fark nedir.
URI: Uniform Resource Identifier
```
internet üzerinde bir kaynağın tam yerine işaret eden (resim veya belge) standart formata uygun bir 
karakter dizisidir. Kısaca bir URL’nin altında bulunan kaynağın tam yoluna işaret eder.
Örneğin https://www.aramamotoru.com/uniform-resource-identifier-nedir-uri-nedir/ bir URI’dir.
```
URL: Uniform Resource Locator
```
nternet üzerinde kaynağın yerine işaret eden standart bir formata uygun karakter dizisidir. 
Örneğin https://indir.com/ bir URL’dir.
```
URL ile URI arasındaki fark ise 
```
URL’ler ana kaynak, URI’ler ise detayları gösterir.
```
### String ile StringBuilder arasındaki fark nedir.
```
String, değişmez, değerlerini değiştirmeye çalışırsanız, başka bir nesne oluşturulur; 
oysa StringBuffer ve StringBuilder, değiştirilebilir değerlerini değiştirebilirler.

Stringler değişmez (immutable) objelerdir.Öyle ki,tanımladığınız bir string’in içeriğini değiştirdiğinizde, 
o objenin içeriği değişmez.Her ne kadar değişiyor gibi gözükse de,arka planda bellek üzerinde bir kopyası 
daha oluşturulur.Bu da string’e her değer atamanızda yeni bir instance oluşması anlamına gelmektedir

String objesi değişmek için arka planda yeni bir String nesnesi oluşturur. Her değişikilte yeni bir 
String class’ı oluşuyor. Bu da zamanla performansı kötü yönde etkiliyor.
```
### StringBuffer ve StringBuilder arasındaki fark
```
StringBuffer ile StringBuilder arasında ki tek fark ise “senkronizasyon”dur. StringBuffer “synchronized” i
ken StringBuilder “synchronized” değildir.
Thread kullancaksanız; StringBuffer, kullanmayacaksanız StringBuilder kullanmanız daha verimli olcaktır.
```
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
### Java Checked vs Unchecked Exceptions
Checked Exception Example
```
FileNotFoundException is a checked exception in Java.
```

```
    try {
        FileReader file = new FileReader("somefile.txt");
    }  catch (FileNotFoundException e)  {
        e.printStackTrace();
    }
```
Unchecked Exceptions
```
Unchecked Exceptions are subclasses of RuntimeException. 
NullPointerException is unchecked exception in Java.
Example of unchecked exceptions are : ArithmeticException, ArrayStoreException, ClassCastException
```
Exception in thread "main" java.lang.ArithmeticException: / by zero
```
    public static void main(String args[]) { 
       int x = 0; 
       int y = 10; 
       int z = y/x; 
    }
```
### RuntimeException
```
RuntimeException, Java Virtual Machine'nın normal operasyonlar yani çalışma sırasında gerçekleşen exception'lardır.
NullPointerException, Java'da bir RuntimeException'dır. 
```
### Exception Sınıfı:
```
- ClassNotFoundException: Olmayan bir dosyaya erişme istediği durumlarını inceler.
- IOException: Giriş çıkış işlemlerindeki istenmeyen durumları inceler.
- RunTimeException: Çalışma zamanı hatalarını inceler.
- AritmeticException: Aritmetik hataları inceler.
- NullPointerException: Herhangi bir nesneye null referanslı bir değişken ile ulaşılmaya çalışılan durumlarda fırlatılır.
- IllegalArgumentException: Metotlara geçersiz argüman atamalarında fırlatılır.
```
