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
```

```

### JAVA_CODE_Q_3 
```

```
