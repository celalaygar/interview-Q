# Genel Mülakat Soruları


## Java Class Loader nedir ?
```

```

## Java Thread ile Virtua Thread arasndaki fark nedir ?
```

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
Spring Framework içinde “scope” bir nesnenin yaşam döngüsünü ve ne kadar süreyle erişilebilir olduğunu tanımlayan bir
kavramdır. Spring, çeşitli nesne scope’ları sağlar ve bu scope’lar nesnelerin oluşturulma, kullanılma ve yok edilme
şeklini belirler.

Bu scope’lar, Spring uygulamalarında nesnelerin nasıl yönetileceğini belirlemek için kullanılır. Scope belirleme,
nesnelerin doğru zamanda oluşturulması, paylaşılması ve yok edilmesi açısından önemlidir ve uygulamanın performansı ve
davranışı üzerinde etkili olabilir.
```

##### singleton Scope 
```
Bir bean default olarak singleton scope’a sahiptir. Bean singleton scope ile tanımlandığı zaman mevcut application
context‘imiz içerisinde o bean’den yalnızca tek bir adet initialize edileceğini garanti ederiz. Bu bean ile yapılacak
olan tüm request’ler cache’lenmiş olan aynı nesne üzerinden yapılır. 
```
##### prototype Scope
```
Prototype ile belirlenmiş bir bean, container içerisinde çağırıldığı her request’te yeniden oluşturulacaktır.
Scope notasyonun iki farklı kullanımını aşağıda görebilirsiniz.

Prototype Scope kullandığınızda, her request geldiğinde yeni bir instance döndürür. Diyelim ki bir setter
methoduna sahip bir sınıfınız var, şimdi bu sınıf için bir bean oluşturduğunuzda, size her zaman sınıfın
yeni bir instance’sını verecek ve nesne niteliklerini değiştirmek için setter’ı özgürce kullanıp çalışacaktır. 
```
##### request Scope
```
Request bean’i HTTP isteği geldiğinde oluşturulur. örneğin, bir “ /products” API’niz var, şimdi controller
bu isteği aldığında ve service methodunu çağırdığında, Request Scope ile bir Bean’iniz olacak ve
bu API isteği yanıtı geri gönderene kadar her zaman nesnenin aynı instance’ını alırsınız, ancak yeni bir
request geldiğinde, yeni bir instance gönderecek.
```
##### session Scope
```
Session Scope Web Uygulamalarında HTTP isteği geldiğinde oluşturulur. Mesela Spring boot uygulamanız
kullanıcı sessionlarını sürdürdüğünde, bu scope yardımcı olabilir. Session Scope kullandığımızda, tüm
Session için (kullanıcı düzeyindeki oturumda) her zaman nesnenin aynı instance’ını return eder. Ancak
kullanıcı oturumu kapandığında, yeni bir kullanıcı oturumu için nesnenin yeni bir instance’ını alacaksınız.
```
##### application Scope
```
Bir application scope, ServletContext’in yaşam döngüsü için bean örneğini oluşturur. Bu singleton scope’a
benzer ancak aralarında farklılıklar mevcuttur. Bir bean application scope değerine sahipken bu bean çoklu
servlet tabanlı uygulamalar ile de paylaşılabilirken, singleton scope değerine sahip bir bean yalnızca
mevcut application context’i içerisinde tanımlıdır.
```

## Circuat Breaker nedir ?
```

```

## spring de interceptorler ?
```

```

## sql de index türleri ?
```

```

## spring IOC Container ?
```

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

## Domain Driven Design Nedir?
```
https://medium.com/@avniozunlu/domain-driven-design-ddd-151c90472914
```
