## JAVA CODE SORULARI 2

### JAVA_CODE_Q_1 
Kodun çıktısı nedir?
```
	int i = 0, j = 0;
	while (i++ < 3) do
			System.out.print(j);
		while (j++ < 3);
```
OUTPUT
```
012345
```
### JAVA_CODE_Q_2
Kodun çıktısı nedir?
```
public class main {
	public static void main(String [] args) {
		C c = new D(); 
		System.out.println("z : "+c.z);
		c.play();
		c.execute();
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
OUTPUT
```	
z : 0
class d method play 2
class c method execute
```
### JAVA_CODE_Q_3
Kodun çıktısı nedir?
```
public class main {
	public static void main(String [] args) {
		A b1 = new B(); 
		System.out.println("z : "+b1.z);
		b1.play(); 		b1.execute();
		

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
OUTPUT
```		
z : 0
class b method play 2
class a method execute 1
```
### JAVA_CODE_Q_4
Kodun çıktısı nedir?
```
public static void main(String[] args) {
	b b1 = new b(); 
	System.out.println("z : "+b1.z);
	b1.play();
	b1.execute();


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
OUTPUT
```
z : 1
class b method play
class b method execute 
```
### JAVA_CODE_Q_5
Dizide olmayan en küçük pozitif sayıyı bulunuz. Kodunu yazınız...
```
// dizide olmayan en küçük pozitif sayıyı bulunuz....

        int[] arr = {-5,  5, 14 , 1, 3, 12, 2, 11 };
        arr = new int[]{1, 3, 4};
        arr = new int[]{ -3, -1,  3, 6, 4,  2 , 22};
        int cnt = 0;
        int flag = 0;
        int first = 0;
        while (true) {

            if (cnt == arr.length) { break; }
            if (arr[cnt] < 0) {
                cnt++;
                continue;
            }
            first = arr[cnt];
            cnt++;
            if(flag == 0){
               flag = first;
               continue;
            }
            if(first < flag ){ flag = first; }
        }
        System.out.println(" flag " + flag);

```
## JAVA_CODE_Q_6
### REVERSE STRİNG WİTH RECURSİVE FUNCTION
Recursive fonksiyonu ile bir stringi ters çeviren methodu yazınız.
```
	public void reverse() {
		String data = "20022002";
		System.out.println(this.recursive(data, 0, data.length()-1) );
	}
	
	private Boolean recursive( String data, int preIndex, int postIndex) {
		Boolean control = true;
		if(preIndex == postIndex || postIndex < preIndex ) 
			return control;
		if(data.charAt(preIndex) == data.charAt(postIndex) ) {
			control = this.recursive(data, preIndex+1, postIndex-1);
		}else {
			control = false;
		}
		return control;
	}
```

## JAVA_CODE_Q_6
### JDBC CONNECTION EXAMPLE
statik çalışan jdbc connection kodu örneğini yazınız
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
