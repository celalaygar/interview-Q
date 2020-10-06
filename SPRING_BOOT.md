# SPRING BOOT  

### Difference between @SpringBootApplication vs @EnableAutoConfiguration annotations
@SpringBootApplication = Alttaki 3 anotasyonunun işlerini yapar.
```
@Configuration  is used in Java-based configuration on Spring framework
@ComponentScan to enable component scanning of components you write like @Controller classes
@EnableAutoConfgiuration itself, which is used to allow for auto-configuration in Spring Boot application
```

### @ConfigurationProperties
pom.xml e bu dependency eklendiğinde bu alttaki anotasyon kullanılır.
```
	<dependency>
		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-configuration-processor</artifactId>
		<optional>true</optional>
	</dependency>
```
```
@ConfigurationProperties  // application.properties deki değerleri bu class a assign eder.
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
### ---
---
```
------
```
