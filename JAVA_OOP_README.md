## JAVA OOP Q
###  Polymorphism in Java
Java’da farklı şekilde çalışan nesnelere aynı şekilde erişmek şeklinde tanımlayabiliriz.
```
class Parent { 
    void Print()  {  System.out.println("parent class");  } 
} 
  
class subclass1 extends Parent { 
   void Print()  {   System.out.println("subclass1");  } 
} 
  
class subclass2 extends Parent {  
    void Print()  {   System.out.println("subclass2");  } 
} 
  
class TestPolymorphism3 { 
    public static void main(String[] args) 
    { 
        Parent a; 
        a = new subclass1(); 
        a.Print(); 
        a = new subclass2(); 
        a.Print(); 
    } 
}
```
Output:
```
subclass1
subclass2
```
###  Inheritance in Java  Kalıtım(Inheritance)
Kalıtım(Inheritance), bir sınıfın kendisine ait özellikleri ve işlevleri bir başka sınıfa aynen 
aktarması ya da bazı özellik ve işlevlerini diğer sınıfların kullanmasına izin vermesi şeklinde oluşmaktadır.
```
class one  { 
    public void print_geek()  { 
        System.out.println("Geeks"); 
    } 
} 
  
class two extends one  { 
    public void print_for()  { 
        System.out.println("for"); 
    } 
} 
  
class three extends two  { 
    public void print_geek()  { 
        System.out.println("Geeks"); 
    } 
} 
  
// Drived class 
public class Main  { 
    public static void main(String[] args)   { 
        three g = new three(); 
        g.print_geek(); 
        g.print_for(); 
        g.print_geek(); 
    } 
} 
```
Output:
```
Geeks
for
Geeks
```
### Encapsulation in Java

Private: Sınıfa özel değişkenlerdir.
Public: Herkese açık olan değişkenlerdir.
Protected: Extends edenlere, türetenlere ve aynı pakette olanlara açık olan değişkenlerdir.
Default: Hiçbir şey yazılmazsa aynı pakettekilerin erişebildiği değişkenlerdir.
```
public class Encapsulate 
{  
    private String geekName; 
    private int geekRoll; 
    private int geekAge; 
   
    public int getAge()   { 
      return geekAge; 
    }  
    public String getName()   { 
      return geekName; 
    }  
    public int getRoll()   { 
       return geekRoll; 
    }
    
    public void setAge( int newAge)  { 
      geekAge = newAge; 
    }  
    public void setName(String newName)   { 
      geekName = newName; 
    }  
    public void setRoll( int newRoll)    { 
      geekRoll = newRoll; 
    } 
} 


public class TestEncapsulation 
{     
    public static void main (String[] args)  
    { 
        Encapsulate obj = new Encapsulate();  
        obj.setName("Harsh"); 
        obj.setAge(19); 
        obj.setRoll(51); 
           
        System.out.println("Geek's name: " + obj.getName()); 
        System.out.println("Geek's age: " + obj.getAge()); 
        System.out.println("Geek's roll: " + obj.getRoll());  
    } 
} 

```
Output:
```
Geek's name: Harsh
Geek's age: 19
Geek's roll: 51
```
