## JAVA Q
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
### Examp -1 
Java examp 1
```
	int i = 0, j = 0;
	while (i++ < 3) do
			System.out.print(j);
		while (j++ < 3);

//	output
//	012345
```
Java examp 2
```
public class main {
	public static void main(String [] args) {
		C c = new D(); 
		System.out.println("z : "+c.z);
		c.play();
		c.execute();
			
//		output
//		z : 0
//		class d method play 2
//		class c method execute
	}
}
class C{
	static int z= 0;
	void play() { System.out.println("class c method play "+(++z)); } 
	static void execute() { System.out.println("class c method execute"); }
}
class D extends C { 
	static int z= 1; 
	void play() { System.out.println("class d method play "+(++z)); } 
	static void execute() { System.out.println("class d method execute"); }
}
```
Java examp 3
```
public class main {
	public static void main(String [] args) {
		A b1 = new B(); 
		System.out.println("z : "+b1.z);
		b1.play(); 		b1.execute();
		
//		OUTPUT :		
//		z : 0
//		class b method play 2
//		class a method execute 1
	}
}
class A{
	static int z= 0;
	void play() { System.out.println("class a method play "+(++z)); } 
	static void execute() { System.out.println("class a method execute "+(++z)); }
}
class B extends A { 
	static int z= 1; 
	void play() { System.out.println("class b method play "+(++z)); } 
	static void execute() { System.out.println("class b method execute "+(++z)); }
}
```
Java examp 4
```
public static void main(String[] args) {
	b b1 = new b(); 
	System.out.println("z : "+b1.z);
	b1.play();
	b1.execute();

	// output
//	z : 1
//	class b method play
//	class b method execute 
}
class a{
	static int z= 0;
	void play() { System.out.println("class a method play"); } 
	static void execute() { System.out.println("class a method execute"); }
}
class b extends a { 
	static int z= 1; 
	void play() { System.out.println("class b method play"); } 
	static void execute() { System.out.println("class b method execute"); }
}
```
### JDBC CONNECTION EXAMPLE
```
   public class ORACLEConnection {
	private static Connection connection;

	public static Connection getConnection() throws SQLException {
		if (connection != null) { return connection; }
		String İpAdress="";     String port="";     String dbName="";       String username="";     String password="";

		connection = DriverManager.getConnection( "jdbc:oracle:thin:@İpAdress:port:dbName", "username", "password");

		if (connection != null)   System.out.println("Connected to the database!");
		else                      System.out.println("Failed to make connection!");

		return connection;
	}

	public static void closeConnection() throws SQLException {
		connection.close();
	} 
   }

public class DbHelper {
	private ArrayList<Patient> patients;
	private Connection connection;
	private PreparedStatement stmt;
	
	public DbHelper() throws SQLException {
		connection = ORACLEConnection.getConnection();
	}

	public Patient addPatient(Patient patient) throws SQLException {
		if (patient != null) {
			String sql = "INSERT INTO AAPATIENT VALUES (?,?,?,?,?,?)";
			stmt = connection.prepareStatement(sql);
			int id = databaseId();
			stmt.setInt(1, id);
			stmt.setString(2, patient.getName());
			stmt.setString(3, patient.getSurname());
			stmt.setString(5, patient.getGender());
			patient.setId(id);
			int i = stmt.executeUpdate();
			System.out.println(i + " records inserted");
			return patient;
		} else {
			System.out.println("Patient is null");
			return null;
		}
	}
}
```
