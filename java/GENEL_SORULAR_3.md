## JAVA GENEL SORULAR 3

###  Java’da HashMap ve ConcurrentHashMap arasındaki fark nedir?
```
1. ConcurrentHashMap iş parçacığı açısından güvenlidir; Bir seferde yalnızca bir iş parçacığı koda erişebilir,
oysa HashMap iş parçacığı için güvenli değildir.

2. ConcurrentHashMap anahtarların boş değerler içermesine izin vermezken, HashMap bir boş anahtar içerebilir.
```

###  ThreadLocal nedir?
```
Java ThreadLocal, iş parçacığı yerel değişkenleri oluşturmak için kullanılır.
Bir Object’in tüm evrelerinin değişkenlerini paylaştığını biliyoruz,
bu nedenle değişken evre güvenli değilse senkronizasyonu kullanabiliriz …
ancak senkronizasyondan kaçınmak istiyorsak, ThreadLocal değişkenleri kullanabiliriz.

Her iş parçacığının kendi ThreadLocal değişkeni vardır ve varsayılan değeri almak veya
yerel değerini Thread olarak değiştirmek için onun gets () ve set ()
yöntemlerini kullanabilirler. ThreadLocal örnekleri, durumu bir evre ile
ilişkilendirmek isteyen sınıflarda tipik olarak özel statik alanlardır.
```

###   Java’da java.lang.OutOfMemoryError gibi bir hatayı nasıl çözersiniz?
```
Java’da OutOfMemoryError’ı çözmenin ilk ve kolay yolu, OutOfMemoryError’ınızı
hemen çözecek olan JVM seçeneklerini “-Xmx512M” kullanarak maksimum yığın boyutunu artırmaktır.

JVM’nin maksimum yığın boyutunu artırmanın bir örneği, java uygulama dışa aktarmanızda yığın boyutunu ayarlıyorsanız
-Xmx – Xms oranını 1: 1 veya 1: 1.5 korumanın daha iyi olduğuna dikkat edin JVM_ARGS = “- Xms1024m -Xmx1024m. “

Java’da OutOfMemoryError’ı çözmenin ikinci yolu oldukça zordur ve çok fazla belleğiniz olmadığında ve
maksimum yığın boyutunun artmasından sonra bile java.lang.OutOfMemoryError’ı alıyorsunuz.
Bu durumda, muhtemelen uygulamanızın profilini çıkaracak ve bir bellek sızıntısı arayacaksınız.
```

###  HashSet ile TreeSet arasındaki fark nedir?
```
Küme, yinelenen öğeler içermeyen genel bir değerler kümesidir. Bir TreeSet, öğelerin sıralandığı bir kümedir.
Bir HashSet, öğelerin sıralanmadığı veya sıralanmadığı ve bir TreeSet’ten daha hızlı olduğu bir settir.
```

###  Comparator ve Comparable arayüzlerini ne zaman kullanmalısınız?
```
Bir nesne, sınıfı sınıflandırmanın açık ve doğal bir yoluysa ve herkes sınıfı bu şekilde sıralayabilirse,
Comparable’ı uygulamalıdır. Bununla birlikte, sıralama sınıfın alışılmadık bir kullanımıysa veya
sıralama yalnızca belirli bir kullanım durumu için mantıklıysa, Karşılaştırıcı daha iyi bir seçenektir.
```
 
###  Java Virtual Threads — Easy introduction
Java 21'de Gelen Yenilikler - Virtual Threads
```
https://yteblog.bilgem.tubitak.gov.tr/jdk21-virtual-threads-springte-kullanimi
https://medium.com/@onurokkyay/java-virtual-thread-nedir-6049151ac2b8
https://medium.com/@RamLakshmanan/java-virtual-threads-easy-introduction-44d96b8270f8
```
 
###  Difference Between Thread and Virtual Thread in Java
```
https://www.baeldung.com/java-virtual-thread-vs-thread
```
 
