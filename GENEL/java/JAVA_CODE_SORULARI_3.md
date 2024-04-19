## JAVA CODE SORULARI 3

### JAVA_CODE_Q_1 
Palindrome String in Java v1
```
    public static void main(String[] args) {
        String str = "1cceecc1";
        String rev = "";
        
        boolean ans = false;
        
        for (int i = str.length() - 1; i >= 0; i--) { rev = rev + str.charAt(i); }
        
        if (str.equals(rev)) { ans = true; }
        
        System.out.println(ans);
    }
```
Palindrome String in Java v2
```
    public static void main(String[] args) {

        String str = "1cceecc1xx";
        String control = "Yes";

        for (int i = str.length() - 1; i >= 0; i--) {
            if(str.charAt(i) != str.charAt(str.length() -1 - i )){
                control = "No";
                break;
            }
        }

        System.out.println(control);
    }
```

### JAVA_CODE_Q_2 

Remove the biggset number from integer list on java
```
        int[] intList= new int[]{1,4,3,22,33,12,13};
        List<Integer> list = new ArrayList<>();

        int currentInt = intList[0];
        int index = 0;

        for (int i = 0; i <= intList.length - 1; i ++) {

            list.add(intList[i]);
            if( intList[i] > currentInt  ){
                currentInt = intList[i];
                index = i;
            }
        }
        list.remove(index);
        int[] newList = new int[list.size()];
        for (int i = 0; i <= list.size() - 1; i ++) {
            newList[i] = list.get(i);
        }
        System.out.println(Arrays.toString(newList));
```

### JAVA_CODE_Q_3 
```

```
