## JS QUESTION 2

### JS_CODE_Q_1
```
const person1 = {name:"celal"};
const person2 = {name:"aygar"};

const person = Object.assign(person1, person2);
console.log(person.name);
console.log(person1.name);

//output : aygar aygar
```

### JS_CODE_Q_2
```
const calc = (a) => {
	return (b) => {
		if(b) return calc(a+b);
		return a;
	};
};

console.log(calc(1)(2)(3)(4)());

// output : 10
```

### JS_CODE_Q_3
```
const calc = (a) => {
	return (b) => {
		if(b) return calc(a+b);
		return a;
	};
};

console.log(calc(1)(2)());

// output : 3
```

### JS_CODE_Q_4
```
const fetcData = ()=>{
    return new Promise((res) => res("one"))
};
let isLoading = true;

fetcData().then((result) => {
    console.log(result);
}).finally(()=>{
    console.log("two");
    isLoading = false;
})
console.log(isLoading); 

// output : true   one   two
```
### JS_CODE_Q_5
```
const fetcData = ()=>{
    return new Promise((res) => res("one"))
};
let isLoading = true;

await fetcData().then((result) => {
    console.log(result);
}).finally(()=>{

    console.log("two");
    isLoading = false;
})
console.log(isLoading);

// output :  one   two   false
```
### JS_CODE_Q_6
```
const person ={
  name:"celal",
  displayName(){
    console.log(this.name)
  }
}
const copyPerson = Object.create(person);
person.displayName();
copyPerson.displayName();

// output :  celal   celal
```
### JS_CODE_Q_7
```

```
### JS_CODE_Q_8
```

```
