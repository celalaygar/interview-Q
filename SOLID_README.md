## SOLID-Q

### S — Single-Responsibility Principle(Tek Sorumluluk Prensibi)
Bir Sınıfın ya da fonksiyonun,metodun tek bir görevi, sorumluluğu olmalıdır. Başka sınıfların 
görevlerini gerçekleştirmemelidir.
```
public class JsonValidator {
    public bool IsValid(string input) {
        // Kural denetimini yap
        return true;
    }
}

public class JsonFormatter {
    private JsonValidator _validator = new JsonValidator();

    public string Format(string input) {
        
        if (!_validator.IsValid(input))
            throw new ValidationException();

        // Formatlama işlemini yap
        return "formatlanmış metin!";
    }
}

```
### · O — Open-Closed Principle(Açık Kapalı Prensibi)
- Open Sınıf için yeni davranışlar eklenebilmesini sağlar. Gereksinimler değiştiğinde, yeni gereksinimlerin karşılanabilmesi için bir sınıfa yeni veya farklı davranışlar eklenebilir olmasıdır.
- Closed Bir sınıf temel özelliklerinin değişimi ise mümkün olmamalıdır.
```
Applicationun veya objelerin ya da entitylerin geliştirilmeye açık ancak değiştirmeye kapalı olduğunu belirtir. 
İnterface ve abstract sınıflar kullanılarak istenen eklemeler yapılabilir.

public interface Shape { 
   double getArea(); 
}

public class Rectangle implements Shape {
    private double length;
    private double height;
    // getters/setters … 
    @Override
    public double getArea() { return (length * height); }
}

public class Circle implements Shape {
    private double radius;
    // getters/setters … 
    @Override
    public double getArea() {  return (radius * radius * Math.PI); }
}

public class AreaManager {
    public double calculateArea(List<Shape> shapes) {
        double area = 0;
        for (Shape shape : shapes) {
            area += shape.getArea();
        }
        return area;
    }
}
```
### L — Liskov Substitution Principle ( Liskov’un Yerine geçme Prensibi)
- Alt sınıflardan oluşturulan nesneler üst sınıfların nesneleriyle yer değiştirdiklerinde aynı davranışı göstermek zorundadırlar.
- Bir ana sınıftan ya da sınıflardan türetilen sınıfların bir üst hiyerarşideki sınıfların yerine geçmesini 
esas alan bir prensiptir.
```
interface IUcakKesif{
    bool KesifYap();
}
 
interface IHedefiVur{
    bool HedefiVur();
}
 
class UcakA : IUcakKesif, IHedefiVur {
    public bool HedefiVur(){
        Console.WriteLine("UcakA Hedefi vurdu.");
        return true;
    }
    public bool KesifYap() {
        Console.WriteLine("UcakA keşfi tamamladı.");
        return true;
    }
}
class UcakB : IUcakKesif, IHedefiVur{
    public bool HedefiVur(){
        Console.WriteLine("UcakB Hedefi vurdu.");
        return true;
    }
    public bool KesifYap(){
        Console.WriteLine("UcakB keşfi tamamladı.");
        return true;
    }
}
class UcakC : IUcakKesif {
    public bool KesifYap() {
        Console.WriteLine("UcakC keşfi tamamladı.");
        return true;
    }
}
class Savas {
    List<IHedefiVur> HedefVurucular;
    List<IUcakKesif> KesifYapicilar;
    public Savas(List<IUcakKesif> KesifYapicilar, List<IHedefiVur> HedefVurucular) {
        this.KesifYapicilar = KesifYapicilar;
        this.HedefVurucular = HedefVurucular;
    }
 
    public void KesifYap() {
        KesifYapicilar.ForEach(u => { u.KesifYap(); });
    }
 
    public void HedefiVur()  {
        HedefVurucular.ForEach(u => { u.HedefiVur(); });
    }
}
```
```
public interface IFly {  void Fly(); }

public interface ISwim { void Swim(); }

public interface IQuack { void Quack(); }

public class MallardDuck : IFly, ISwim, IQuack
{
    public void Quack() { System.Console.WriteLine("Quack!"); }

    public void Swim() {  System.Console.WriteLine("Swimming!"); }

    public void Fly()  {  System.Console.WriteLine("Flying!"); }
}

public class MarbledDuck : IFly, ISwim, IQuack
{
    public void Quack() { System.Console.WriteLine("Quack!"); }

    public void Swim() {  System.Console.WriteLine("Swimming!"); }

    public void Fly()  {  System.Console.WriteLine("Flying!");  }
}

public class RubberDuck : ISwim, IQuack
{
    public void Quack() {  System.Console.WriteLine("Squeak!"); }

    public void Swim() { System.Console.WriteLine("Floating!"); }
}

```
### I — Interface Segregation Principle ( Arayüz Ayrımı Prensibi)
- Sınıflar, ihtiyaç duymadıkları metotların bulunduğu Interface’lere bağlı olmaya zorlanmamalıdır.
- Tek bir interface kullanmak yerine ihtiyaçlara göre bölünmüş birden fazla interface ile işlemleri gerçekleştirmeliyiz.
- Bir arayüze gerekli olmayan eklentilerin eklenmemesini belirten bir prensiptir.

```
interface HavaAraclari {
  void Yuksel();
  void Alcal();
}
interface SavasabilirHavaAraclari : HavaAraclari {
  void AtesEt();
}

public class F16 : SavasabilirHavaAraclari {
  public void Yuksel() {
    Console.Write("F16 yükseliyor..")
  }
  public void Alcal() {
    Console.Write("F16 alçalıyor..")
  }
  public void AtesEt() {
    Console.Write("F16 ateş ediyor !!")
  }
}

// Artık F16 SavasabilirHavaAraclari'ni implemente edecek.
// Yolcu Uçağı ise HavaAraclari' ni implemente edecek.

public class YolcuUcagi: HavaAraclari {
  public void Yuksel() {
    Console.Write("Yolcu Uçağı yükseliyor..")
  }
  public void Alcal() {
    Console.Write("Yolcu Uçağı alçalıyor..")
  }
}
```
### D — Dependency Inversion Principle ( Bağımlılıkların Terslenmesi Prensibi)
- Katmanlı mimarilerde üst seviye modüller alt seviyedeki modüllere doğruda bağımlı olmamalıdır.
- Varlıklar(Alt sınıflar ve Üst sınıflar) somut olmayan soyutlamalara bağlı olmalıdır. Üst seviye modülün 
düşük seviye modülüne bağlı olmamasını, ancak soyutlamalara bağlı olması gerektiğini belirtir. 
- Alt sınıflarda yapılan değişiklikler üst sınıfları etkilememelidir.
```
public interface Message {
    void sendMessage();
}
public class Email implements Message {

    @Override
    public void sendMessage() { sendEmail();     }

    private void sendEmail() { ...... }
}

public class SMS implements Message {

    @Override
    public void sendMessage() {sendSMS(); }

    private void sendSMS() { ... }
}

public class Notification {
    private List<Message> messages;

    public Notification(List<Message> messages) { this.messages = messages; }

    public void sender() {
        for (Message message : messages)  message.sendMessage();
    }
}
```
