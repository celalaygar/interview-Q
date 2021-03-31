## JAVA Q
### Writing Code 
what is print functıon --->  printData(0, ""); 
```
class Menu {
    int id;
    int ustId;
    String menu;

    public Menu(int id, int ustId, String menu) {
        super();
        this.id = id;
        this.ustId = ustId;
        this.menu = menu;
    }
}


public class MyClass {

    static List<Menu> array;
    public static void main(String[] args) {

        array=Arrays.asList(
                new Menu(11,0,"Class 1"),
                new Menu(12,11,"Class 11"),
                new Menu(13,11,"Class 12"),
                new Menu(14,11,"Class 13"),
                new Menu(15,14,"Class 131"),
                new Menu(16,14,"Class 132"),
                new Menu(17,11,"Class 14"),
                new Menu(18,0,"Class 2"),
                new Menu(19,0,"Class 3"),
                new Menu(20,19,"Class 31"),
                new Menu(21,19,"Class 32"),
                new Menu(22,0,"Class 4"),
                new Menu(23,22,"Class 41"),
                new Menu(24,22,"Class 42"),
                new Menu(25,24,"Class 421"),
                new Menu(26,24,"Class 422")
                );
        printData(0, "");
    }
    
}    
```
