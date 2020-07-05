## SOLID-Q

### S — Single-Responsibility Principle(Tek Sorumluluk Prensibi)

```
Bir Sınıfın ya da fonksiyonun,metodun tek bir görevi, sorumluluğu olmalıdır. Başka sınıfların 
görevlerini gerçekleştirmemelidir.

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

```
Applicationun veya objelerin ya da entitylerin geliştirilmeye açık ancak değiştirmeye kapalı olduğunu belirtir. 
İnterface ve abstract sınıflar kullanılarak istenen eklemeler yapılabilir.

```
### L — Liskov Substitution Principle ( Liskov’un Yerine geçme Prensibi)

```
Bir ana sınıftan ya da sınıflardan türetilen sınıfların bir üst hiyerarşideki sınıfların yerine geçmesini 
esas alan bir prensiptir.

```
### I — Interface Segregation Principle ( Arayüz Ayrımı Prensibi)

```
Bir arayüze gerekli olmayan eklentilerin eklenmemesini belirten bir prensiptir.

```
### D — Dependency Inversion Principle ( Bağımlılıkların Terslenmesi Prensibi)

```
Varlıklar(Alt sınıflar ve Üst sınıflar) somut olmayan soyutlamalara bağlı olmalıdır. Üst seviye modülün 
düşük seviye modülüne bağlı olmamasını, ancak soyutlamalara bağlı olması gerektiğini belirtir. 
Alt sınıflarda yapılan değişiklikler üst sınıfları etkilememelidir.

```
