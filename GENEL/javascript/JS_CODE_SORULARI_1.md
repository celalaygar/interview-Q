## JS CODE SORULARI 1

### JS CODE QUESTION 1
```
console.log(1)
console.log(2)
setInterval(console.log(3), 0)
console.log(4)
```
```
OUTPUT : 
1
2
3
4
``` 
### JS CODE QUESTION 2
what is output?
```
var x = Math.floor(Math.random());
if(x>0.1){
    var x = 1; 
}else{
    var x = 2;
}
console.log(x);  
``` 
output : 
```
 2
``` 
### JS CODE QUESTION 3
what is value of a?
```
const ccc = [45, 4, 9, 16, 25];
let a = ccc.every(val => val> 8);
``` 
output : 
```
false
``` 
### JS CODE QUESTION 4
what is output?
```
console.log("start");
setTimeout(()=>{
console.log("first");
},0);

Promise.resolve(123).then((value) => {
  console.log("value " + value);
});
console.log("end");
``` 
output : 
```
start
ende
value 123
first
```
### JS CODE QUESTION 5
what is output?
```
const realFunction = (callBack1, callBack2) => {
	callBack1();
	setTimeout(callBack2, 1000);
	console.log("three");
};
const callBack1 = () => { console.log("one");};
const callBack2 = () => { console.log("two");};
realFunction(callBack1, callBack2);
```
output : 
```
one
three
two
```
### JS CODE QUESTION 6
what is output?
```
var x = 10;
function ff(){console.log(x); var x = 20;}
ff();
```
output : 
```
undefined
```
### JS CODE QUESTION 7
what is output?
```
const array = [1,2,3,4,5]
const [x,y, , z] = array;
console.log(z)
```
output : 
```
4
```


