# SPRING BOOT  

### Difference between @SpringBootApplication vs @EnableAutoConfiguration annotations
@SpringBootApplication = Alttaki 3 anotasyonunun işlerini yapar.
```
@Configuration  is used in Java-based configuration on Spring framework
@ComponentScan to enable component scanning of components you write like @Controller classes
@EnableAutoConfgiuration itself, which is used to allow for auto-configuration in Spring Boot application
```

### @ConfigurationProperties ne iş yapar?
@ConfigurationProperties ne iş yapar?
```
application.properties deki değerleri bu class a assign eder.
```
pom.xml e bu dependency eklendiğinde bu üstteki anotasyon kullanılır.
```
	<dependency>
		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-configuration-processor</artifactId>
		<optional>true</optional>
	</dependency>
```

### @Profile
applicaton.yml dosyasında öncelikli olarak alttaki gibi bir örnek kullanmalısınız.
```
spring:  
  profiles: 
    active: prod
---
spring:  
  profiles: prod
app:  
  upload-path: storage-production
---
spring:  
  profiles: dev
app:  
  upload-path: storage-dev
```
Daha sonra bu anotasyon ile methodlara çalışacakları durumları belirtebilirsiniz
```
@Profile("dev")
spring.profiles.active = dev ise bu anotasyonun oldugu method çalışır.
@Profile("!dev") veya @Profile("prod") 
spring.profiles.active = prod ise bu anotasyonun oldugu method çalışır.
```

### AOP nedir?
```
AOP ifadesi Aspect-Oriented Programming ifadesinin kısaltması. OOP'den (Object-Oriented Programming) farkı 
OOP'nin class'lara odaklanırken AOP'nin ana modülarite biriminin aspect olması. AOP'de aspect'ler 
cross-cuting concern'leri uygular ve belirtir.
```

### "Dependency injection" nedir?
```
Dependency injection nesneler için belli bağlımlılıklar sağlamak için kullanılıyor. 
Projenizi sorunsuz ve test gibi eylemlere daha uygun hale getiren bir tasarım modelidir.
```
```
Dependency injection kaba tabir ile bir sınıfın/nesnenin bağımlılıklardan kurtulmasını amaçlayan ve o nesneyi 
olabildiğince bağımsızlaştıran bir programlama tekniği/prensibidir.
```

### @Autowire ve @Qualifier birlikte kullanılırsa ne olur?
```
Bu kombinasyon türü uygulamada birçok farklı türde tekil bean bulunduğunda kullanılır. 
Bu kombinasyon her bir ayrı bean'i farklılaştırır.
```

### Spring Bean Scopes nelerdir.
```
https://medium.com/@ismailbozdag0/spring-bean-scopes-aae18c1ef877
```

### Spring Cloud — Netflix Hystrix ile Circuit Breaker
```
https://acokgungordu.medium.com/spring-cloud-netflix-hystrix-ile-circuit-breaker-a055e5e7b910
```

### Nedir bu Circuit Breaker Pattern ?
```
https://medium.com/trendyol-tech/nedir-bu-circuit-breaker-pattern-2d3d34948767
```

### spring ioc container nedir
```
Spring IoC Container, Spring Framework'ün çekirdeğidir. Bu konteyner, nesneleri oluşturur,
nesneleri birbirine bağlar, bağımlılıklarını yapılandırır ve tüm yaşam döngüsünü yönetir.
Spring konteyneri, bir uygulamayı oluşturan bileşenleri yönetmek için Dependency Injection'ı kullanır.
```
