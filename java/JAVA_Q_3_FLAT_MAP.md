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

        System.out.println("allCountries as list ------------------------------------  ");
        System.out.println(allCountries);


        /*   output :
        [[Almanya, Avusturya, Belçika, Bulgaristan], [Ethiopia, Tanzania, Kenya, Sudan], [Japonya, Çin, Hindistan, Kore]]
        */


        System.out.println("allCountries as list foreach ------------------------------------  ");
        allCountries.forEach(System.out::println);



        /*   output :
        [Almanya, Avusturya, Belçika, Bulgaristan]
        [Ethiopia, Tanzania, Kenya, Sudan]
        [Japonya, Çin, Hindistan, Kore]
        */

        List<String> allCountriesAsFlat = allCountries.stream()
                .flatMap(country -> country.stream()).collect(Collectors.toList());

        System.out.println("allCountries as String list ------------------------------------  ");
        System.out.println(allCountriesAsFlat);



        /*   output :
        [Almanya, Avusturya, Belçika, Bulgaristan, Ethiopia, Tanzania, Kenya, Sudan, Japonya, Çin, Hindistan, Kore]
        */
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

        System.out.println(" ----------------------------- personList");
        System.out.println(personList);
        /*   output :
        [[Person{id=1, name='Metin', surname='Aln'}, Person{id=2, name='Kağan', surname='Aln'}, Person{id=3, name='Yusuf', surname='Aln'}, Person{id=4, name='Dilek', surname='Aln'}], [Person{id=9, name='Enver', surname='Akça'}, Person{id=10, name='Kağan', surname='Korkmaz'}, Person{id=11, name='Yusuf', surname='Sönmez'}, Person{id=12, name='Yılmaz', surname='Aln'}], [Person{id=5, name='Ahmet', surname='Davut'}, Person{id=6, name='Rıza', surname='Özkök'}, Person{id=7, name='Ali', surname='Can'}, Person{id=8, name='Ayşe', surname='Nur'}]]
        */


        List<Integer> allIds = personList.stream()
                .flatMap(persons -> persons.stream())
                .map(person -> person.id)
                .collect(Collectors.toList());

        System.out.println(" ----------------------------- allIds");
        System.out.println(allIds);



        /*   output :
        [1, 2, 3, 4, 9, 10, 11, 12, 5, 6, 7, 8]
        */



        List<Integer> filterIds = personList.stream()
                .flatMap(persons -> persons.stream())
                .map(person -> person.id > 5 ? person.id : null)
                .collect(Collectors.toList());

        System.out.println(" ----------------------------- filterIds");
        System.out.println(filterIds);



        /*   output :
        [null, null, null, null, 9, 10, 11, 12, null, 6, 7, 8]
        */



```
