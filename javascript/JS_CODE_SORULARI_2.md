## JS_CODE_SORULARI_2

### JS CODE QUESTION 1
```
const person1 = {name:"celal"};
const person2 = {name:"aygar"};

const person = Object.assign(person1, person2);
console.log(person.name);
console.log(person1.name);
``` 
output : 
```
aygar aygar
```
### JS CODE QUESTION 2
```
const calc = (a) => {
	return (b) => {
		if(b) return calc(a+b);
		return a;
	};
};

console.log(calc(1)(2)(3)(4)());
``` 
output : 
```
10
```
### JS CODE QUESTION 3
```
const calc = (a) => {
	return (b) => {
		if(b) return calc(a+b);
		return a;
	};
};

console.log(calc(1)(2)());
``` 
output : 
```
3
```
### JS CODE QUESTION 4
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
``` 
output : 
```
true   one   two
```
### JS CODE QUESTION 5
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
``` 
output : 
```
one   two   false
``` 
### JS CODE QUESTION 6
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
### JS CODE QUESTION 7
```
function execc (){
    let a = (b = 0);
  a++;
    return a;
}
execc();
console.log(typeof a);
console.log(typeof b); 
``` 
output : 
```
 undefined   number
```
### JS CODE QUESTION 8
```
var str = true;
console.log(str + 0);
console.log(str + "abc");
console.log(str + true);
console.log(str + false);

``` 
output : 
``` 
1 
trueabc
2 
1
```
### JS CODE QUESTION 9
```
const resp = () => {
    return (()=> 0 )();
}
console.log("typeof : "+ typeof resp())
```
output : 
``` 
typeof : number
```
### JS CODE QUESTION 10
```
const setList = new Set(); 
setList.add(1);
setList.add(2);
setList.add(3);
setList.add(4);
setList.delete(2);

console.log(setList.has(2) +" " + setList.size);
``` 
output : 
``` 
false 3
```
