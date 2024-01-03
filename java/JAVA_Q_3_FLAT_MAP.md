## JAVA_Q_3_FLAT_MAP
### flatmap usage 1
```
        List<String> europeanCountries = Arrays.asList("Almanya", "Avusturya", "Belçika", "Bulgaristan");
        List<String> africanCountries = Arrays.asList("Ethiopia", "Tanzania", "Kenya", "Sudan");
        List<String> asianCountries = Arrays.asList("Japonya", "Çin", "Hindistan", "Kore");

        List<List<String>> allCountries = new ArrayList<>();
        allCountries.add(europeanCountries);
        allCountries.add(africanCountries);
        allCountries.add(asianCountries);


        List<String> allCountriesAsFlat = allCountries.stream()
                .flatMap(country -> country.stream()).collect(Collectors.toList());
 
        System.out.println(allCountriesAsFlat);

```
```
output :
        [Almanya, Avusturya, Belçika, Bulgaristan, Ethiopia, Tanzania, Kenya, Sudan, Japonya, Çin, Hindistan, Kore]
```
        
### flatmap usage 2
```
        List<Person> list1 = Arrays.asList(
                new Person(1, "Metin", "Aln"),
                new Person(2, "Kağan", "Aln"),
                new Person(3, "Yusuf", "Aln"),
                new Person(4, "Dilek", "Aln")
        );
        List<Person> list2 = Arrays.asList(
                        new Person(9, "Enver", "Akça"),
                        new Person(10, "Kağan", "Korkmaz"),
                        new Person(11, "Yusuf", "Sönmez"),
                        new Person(12, "Yılmaz", "Aln")
                );
        List<Person> list3 = Arrays.asList(
                new Person(5, "Ahmet", "Davut"),
                new Person(6, "Rıza", "Özkök"),
                new Person(7, "Ali", "Can"),
                new Person(8, "Ayşe", "Nur")
        );
        List<List<Person>> personList = Arrays.asList( list1, list2, list3);
 


        List<Integer> allIds = personList.stream()
                .flatMap(persons -> persons.stream())
                .map(person -> person.id)
                .collect(Collectors.toList());

        System.out.println(allIds);

```
```
output :
        [1, 2, 3, 4, 9, 10, 11, 12, 5, 6, 7, 8]
```
```

        List<Integer> filterIds = personList.stream()
                .flatMap(persons -> persons.stream())
                .map(person -> person.id > 5 ? person.id : null)
                .collect(Collectors.toList());

        System.out.println(filterIds);

```
```
output :
        [null, null, null, null, 9, 10, 11, 12, null, 6, 7, 8]
```
