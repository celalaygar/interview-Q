## JAVA CODE SORULARI 1
### Writing Code (Usage of Recursive Function)
### Recursive fonksiyon kullanarak printData methodunun içini doldurunuz..
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
void printData(int ustId,String bosluk) {
    for (int i = 0; i < array.size(); i++) { 
        if(ustId==array.get(i).ustId){ 
            System.out.println(bosluk + array.get(i).menu);
            printData(array.get(i).id, bosluk+"  "); 
        }
    }
}
```
## JAVA_CODE_Q_2
### Show Character count on String
### bir metindeki karakter miktarını gösteriniz.
```
		String sentence = "bu bir denemedir";
		Map<Character, Integer> letterMap = new HashMap<Character, Integer>();

		for (Character letter : sentence.replace(" ", "").toCharArray()) {

			Integer integer = letterMap.get(letter);
			if (integer == null)
				letterMap.put(letter, 1);
			else
				letterMap.put(letter, integer + 1);

		}

		System.out.println(letterMap);

		// output :
		// {b=2, r=2, d=2, u=1, e=3, i=2, m=1, n=1}

//		for (Map.Entry<Character, Integer> entry : letterMap.entrySet()) {
//			System.out.print(entry.getKey() + ":" + entry.getValue() + ", ");
//		}
```
## JAVA_CODE_Q_3
### Find Repeating Character String
### Tekrar eden karakterleri bulunuz.
```
		String sentence = "hih everybody".toLowerCase();
		Map<Character, Integer> letterMap = new HashMap<Character, Integer>();

		for (Character letter : sentence.replace(" ", "").toCharArray()) {

			Integer integer = letterMap.get(letter);
			if (integer == null) 	letterMap.put(letter, 1);
			else 					letterMap.put(letter, integer + 1);
		}

		for (Map.Entry<Character, Integer> entry : letterMap.entrySet())
			if (entry.getValue() > 1)	System.out.print(entry.getKey() + ":" + entry.getValue() + " ");
	
		// output :
		// e:2 h:2 y:2 
```
## JAVA_CODE_Q_4
### Find First Non Repeating Character
### ilk Tekrar etmeyen karakteri bulunuz.

```
		String str1 = "gibblegabbler";
		for (int i = 0; i < str1.length(); i++) {
			boolean unique = true;
			for (int j = 0; j < str1.length(); j++) {
				if (i != j && str1.charAt(i) == str1.charAt(j)) {
					unique = false;
					break;
				}
			}
			if (unique) {
				System.out.println("The first non repeated character in String is: " + str1.charAt(i));
				break;
			}
		}
```
## JAVA_CODE_Q_5
### Find First Repeating Character
### ilk Tekrar eden karakteri bulunuz.
```
	Character[] charArray = {'a', 'b', 'c', 'd', 'e' , 'c','e'};
	
	System.out.println(getMultipleFirstCharacter(charArray));
	
	public Character getMultipleFirstCharacter(Character[] charArray) {
		
		Set<Character> charHashSet = new HashSet<Character>();
		Character result = null;
		for(int i = 0;i<charArray.length; i++) {
			if(charHashSet.contains(charArray[i])) {
				result = charArray[i];
				break;
			}
			charHashSet.add( charArray[i]);
		}
        
        	return result;
	}
```
