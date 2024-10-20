# 🚀 Javascript Output Based Questions
#### 😍This repo contain 100+ javascript Output based questions With detail explaination which we will cover each and every topic and and i will add 5 question every day.
___

<a name="my-custom-anchor-point"></a>

## Day 1
 ####  1. What will be the output ?
 ``` js
let data=100;
 console.log(data +"100");
 console.log(++data);
  ```
<details>
 <summary>View Answer</summary>
 
 - Output:-  
   100100  
   101
 - Reason:-If we add **+** Operater then it will do string concatenation
</details>
           

 ####  2. What will be the output ?
 ``` js
console.log(parseInt('108'))
console.log(parseInt('108*hello'))
console.log(parseInt('108*111'))
```
 <details>
  <summary>View Answer</summary>

  - Output:-  
  108  
  108  
  108
  - Reason:- because parseInt convert into integer till it find non-numeric value,then it stop
</details>

 ####  3. What will be the output ?
```js
const name='sachin';
age=24;

console.log(delete name);
console.log(delete age);
```
<details>
 <summary>View Answer</summary>

 - Output:-  
   false  
   true
 - Reason:-
   - because we want to delete variable but delete keyword is used to delete the key inside the object thats why its false
   - because the undeclared variable add into window object so that it can be delete from window object thats why its true(window.age)
</details>
 
 ####  4. What will be the output ?
 ```js
for(var i=0;i<10;i++){
    setTimeout(()=>{
        console.log(i);
    },0)
}
 ```
<details>
 <summary>View Answer</summary>

 - Output:-10 10 10 10 10 10 10 10 10 10
 - Reason:-
     - because var  variable in this condition is a global scope and setTimeout is run after closing for loop so that's why the value of i is reached to 10 then setTimeOut is executed.then value of var variable is 10.
     - we can fix this using let variable so that it can create setTimeout for every iteration for every let variable
 
</details>

 ####  5. What will be the output ?
 ```js
let user ={name:"sachin"};
let userName=[user];
user=null;
console.log(user);
console.log(userName);
```
<details>
 <summary>View Answer</summary>

 - Output:-
     - null
     - [ { name: 'sachin' } ]
 - Reason:-Setting user to null does not remove the object from userName, because the array holds a separate reference to the object.
</details>

___  


 
[Scroll To Top](#my-custom-anchor-point)


## Day 2  

 ####  6. What will be the output ?
 ```js
(function(){
    var a=b=3;
})();


console.log(typeof a !=='undefined');
console.log(typeof b !=='undefined');
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - false  
    - true  
 - Reason:-
    - var a = b = 3;: This is interpreted as b = 3 followed by var a = b. The variable a is declared with var, which makes it function-scoped, so it is not accessible outside the function.Inside the function, typeof a would be 'number'Outside the function, a is not defined, so typeof a will be 'undefined'.  
    - On the other hand, b = 3 is not declared with var, let, or const. This makes b implicitly global (attached to the global object), so it is accessible outside the function.So type of b is number
</details>

 ####  7. What will be the output ?
```js
var a={},b={key:'b'},c={key:'c'};


a[b]=123;
a[c]=456;


console.log(a[b]);
```
<details>
 <summary>View Answer</summary>

 - Output:-456
 - Reason:-
 - In JavaScript, object keys are internally converted to strings. When you use objects as keys in another object, they are converted to strings using their toString() method.
 - In this case, b and c are both objects, but when used as keys in object a, they are converted to strings.
 - Both b and c will have the same string representation, which is "[object Object]". This is because their default toString() method returns [object Object].
 - So, a[b] and a[c] essentially refer to the same property in object a.
 - Therefore, when you set a[b] = 123 and then a[c] = 456, you are essentially overwriting the value of the property "[object Object]" in object a.
 - Hence, console.log(a[b]) will output 456, as it accesses the property with the key "[object Object]" in object a, which has been overwritten with the value 456.

</details>

 ####  8. What will be the output ?
 ```js
function showData(){
    console.log(name);
    console.log(age);
    var name="heleo";
    let age=23;
}
showData();
```
<details>
 <summary>View Answer</summary>

 - Output:-
     - undefined
     - error, let variable are in temporal dead zone so we cannot access before initilization 
  
</details>

 ####  9. What will be the output ?
```js
const income={
    skills:108,
    monthly(){
      return this.skills * 108  
    },
    yearly:()=>888 * this.skills
}


console.log(income.monthly());
console.log(income.yearly());
```
<details>
 <summary>View Answer</summary>

 - Output:-
      - 102110
      - NaN
 - Reason:- because arrow function is refers to parent object and parent of income object is window and inside window object it does not find yearly() method so that's why this.skills is evaluated is undefined and any number multiply by undefined then answer is NAN

</details>

 ####  10. What will be the output ?
 ```js
console.log(+true)
console.log(-true)
console.log(+false)
console.log(-false)
console.log(!"javascript")
console.log(true + false)
console.log("2"+true );
console.log(-'34'+10 );
console.log(+'dude');
```
<details>
 <summary>View Answer</summary>

 - Output:
    - 1
    - -1
    - 0
    - -0 (or 0)
    - false
    - 1
    - 2true
    - -24
    - NaN

  
 - Reason: 
    - The unary `+` operator converts the boolean `true` to a number. `true` is converted to `1`.  
    - The unary `-` operator converts the boolean `true` to a number and then negates it. `true` is converted to `1`, and negating it gives `-1`.  
    - The unary `+` operator converts the boolean `false` to a number. `false` is converted to `0`.  
    - The unary `-` operator converts the boolean `false` to a number and then negates it. `false` is converted to `0`, and negating it gives `0`.  
    - The logical NOT operator `!` checks the truthiness of the string `"javascript"`. Since non-empty strings are truthy, `!"javascript"` evaluates to `false`.
</details>

___  

[Scroll To Top](#my-custom-anchor-point)

## Day 3

 ####  11. What will be the output ?
```js
let message='heelo';
mesage={data:[24]}


console.log(mesage)
```
<details>
 <summary>View Answer</summary>

 - Output:-{ data: [ 24 ] }
 - Reason:-because js internally declared the undeclared variable
</details>

 ####  12. What will be the output ?
 ```js
function showModel(){
    console.log(showModel.timeout);
}
showModel();
showModel.timeout=200;


showModel.timeout=100;
showModel();
```
<details>
 <summary>View Answer</summary>

- Output:
    - undefined
    - 100
         
- Reason:
    - Initial Call (showModel()): When the function showModel() is first called, the property timeout has not yet been assigned, so console.log(showModel.timeout) will output undefined.
    
</details>

 ####  13. What will be the output ?
 ```js
function Human(fName,lName){
    this.firstName=fName;
    this.lastName=lName;
}

const Name1=Human("sachin","Deshpande");
console.log(Name1)

const Name2=new Human("sachin","Deshpande");
console.log(Name2)
```
<details>
 <summary>View Answer</summary>

  - Output:-  
    - undefined  
    - { firstName: 'sachin', lastName: 'Deshpande' }  
 - Reason:-
    - Here, you're calling Human without the `new` keyword. `This` means:`this` inside Human will refer to the global object (in non-strict mode) or be undefined (in strict mode).
    - As a result, `Name1` will be `undefined`, and the firstName and lastName properties won't be set on any object.
    - Using `new` creates an instance of the object, while calling the constructor without `new` results in `undefined` since it doesn't create a new object.  

</details>


 ####  14. What will be the output ?
 ```js
function getSummary(one,two,three){
    console.log(one)
    console.log(two)
    console.log(three)
}


const name="Sachin";
const age=24;
getSummary`${name} age is ${age}`

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - [ ' ', ' age is ', ' ' ]  
    - Sachin  
    - 24
 - Reason:-
    - The template literal `${name} age is ${age}` is passed to the `getSummary` function as its first argument. In a tagged template literal, the first argument is an array of strings where interpolated values are injected as separate arguments.
    - In this case, the array passed to `getSummary` would be `["", " age is ", ""]`.
    - The subsequent arguments are the evaluated values of the expressions inside the template literal. So, `name` evaluates to `"Sachin"` and `age` evaluates to `24`.
    - Hence, when `getSummary` is called, `one` receives the array `["", " age is ", ""]`, `two` receives the value of `name` (which is `"Sachin"`), and `three` receives the value of `age` (which is `24`).
    - The `console.log` statements inside `getSummary` print these values accordingly.
  
</details>


 ####  15. What will be the output ?
 ```js
function checkAge(data){
    if(data==={age:18}){
        console.log("1")
    }
    else if(data == {age:18}){
        console.log("2")
    }
    else{
        console.log("3")
    }
}
checkAge({age:18})

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - 3 
 - Reason:-
    -  When comparing objects in JavaScript using `==` or `===`, it checks for reference equality, meaning it checks if both objects reference the same location in memory, not if they have the same properties and values.   
    - In the `checkAge` function:The first `if` statement compares the `data` object to `{age: 18}` using `===`. Even though both objects have the same properties and values, they are different objects in memory, so the condition evaluates to `false`.
    - The second `else if` statement similarly compares the `data` object to `{age: 18}` using `==`, and again, it evaluates to `false` due to reference inequality.
    - As both the `if` and `else if` conditions evaluate to `false`, the `else` block is executed, and `"3"` is logged to the console.

</details>

____

[Scroll To Top](#my-custom-anchor-point)

## Day 4

 ####  16. What will be the output ?
 ```js
function hello(...args){
    console.log(typeof args)
}
hello(108)

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - Object  
 - Reason:-
    - The `hello` function is defined with the rest parameter syntax `...args`, which allows it to accept an arbitrary number of arguments as an array.   
    - When you log `typeof args`, it outputs `"object"`, because in JavaScript, arrays are considered objects. Therefore, `args` is of type `"object"`.
</details>


 ####  17. What will be the output ?
 ```js
const obj = { 1: "a", 2: "b", 3: "c" };
const sett = new Set([1, 2, 3, 4, 5]);


console.log(obj.hasOwnProperty("1"));
console.log(obj.hasOwnProperty(1));


console.log(sett.has("1"));
console.log(sett.has(1));

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - true  
    - true
    - false
    - true  
 - Reason:-
    - The key 1 in the object is implicitly converted to a string, while the Set uses strict equality (===) without type conversion.
    - obj.hasOwnProperty("1") returns true because object keys are stored as strings.
    - obj.hasOwnProperty(1) returns true because 1 is implicitly converted to "1".
    - sett.has("1") returns false because Set compares values with strict equality (no type coercion).
    - sett.has(1) returns true because 1 is found in the Set.  

</details>

 ####  18. What will be the output ?
 ```js
function sayHi(){
    return (()=>0)()
}
console.log(typeof sayHi())

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - Number    
 - Reason:-
    - The sayHi function returns the result of an immediately invoked arrow function (() => 0)(), which returns 0. The typeof operator applied to 0 returns "number".
</details>


 ####  19. What will be the output ?
 ```js
console.log(typeof typeof 1)
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - String  
 - Reason:-
    - console.log(typeof "number")    
    - String
</details>

  
 ####  20. What will be the output ?
 ```js
(()=>{
    let x,y;
    try{
        throw new Error
    }
    catch(x){
        (x=1),(y=2);
        console.log(x);
    }
        console.log(x);
        console.log(y);


   
})()

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - 1  
    - undefined
    - 2  
 - Reason:-
    - console.log(x); inside the catch block logs the value of the local x, which is 1.  
      Outside the catch block:  
    - The first console.log(x); statement logs the value of the outer x variable, which is undefined. This is because the local x variable inside the catch block does not affect the outer x variable due to scope.
    - The second console.log(y); statement logs the value of y, which is 2. This value was assigned inside the catch block, and it remains accessible outside the block because y is declared in a wider scope.

      
</details>

___  

[Scroll To Top](#my-custom-anchor-point)

## Day 5



 ###  21. What will be the output ?
 ```js
const arr = [..."sachin"];
console.log(arr);

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - [ 's', 'a', 'c', 'h', 'i', 'n' ] 
</details>


 ####  22. What will be the output ?
 ```js
 function getMessage(){
    throw "Hello World"
}


function sayHello(){
    try{
        const data=getMessage();
        console.log("worked",data);
    }
    catch(e){
        console.log("an Error",e)
    }
}
sayHello();

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - an Error Hello World
 
 - Reason:-
    - In getMessage(), the throw statement is executed with the string "Hello World". This means an exception is thrown immediately, and no value is returned from the function.  
    - The try block in sayHello() attempts to call getMessage(), but since an exception is thrown, control is passed directly to the catch block.
</details>

 ####  23. What will be the output ?
 ```js
 console.log(
    [1,2,3].map(num=>{
    if(num  > 0)return;
    return num * 2
})
)

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - [ undefined, undefined, undefined ]  
 - Reason:-
    - When num > 0, the function returns undefined  
</details>

 ####  24. What will be the output ?
 ```js
 (function(){
    var a=b=3;
})();


console.log(typeof a );
console.log(typeof b );

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - undefined  
    - number  
 - Reason:-
    - a is undefined outside the function because it's a local variable and is not accessible in the global scope. 
    - b, however, was implicitly declared as a global variable and is available globally with the value 3.
</details>

 ####  25. What will be the output ?
 ```js
 const obj={a:"sachin",b:"deshpande"};
const data={c:24,...obj};
console.log(data);

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - { c: 24, a: "sachin", b: "deshpande" }  
 - Reason:-
    - When creating data, the spread operator adds all the properties of obj to the data object, along with the existing property c: 24.
</details>

___  

[Scroll To Top](#my-custom-anchor-point)

## Day 6



 ####  26. What will be the output ?
 ```js
 function* generatorfn(i){
    console.log("A");
    yield i;
    console.log("B");
    yield i * 2
}


const gen=generatorfn(10);


console.log(gen.next().value);
console.log(gen.next().value);

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - A  
    - 10
    - B
    - 20  
 - Reason:-
    - The first gen.next() logs "A" and yields i (10). 
    - The second gen.next() logs "B" and yields i * 2 (20).
</details>

 ####  27. What will be the output ?
 ```js
 var superHero = "SilverSurfer";
let realName = "Noren Red";
console.log(window.superHero);
console.log(window.realName);

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - SilverSurfer  
    - Undefined  
 - Reason:-
    - Because in js having a Global Environment record and this environment having two type ie.Object Environment record and Declarative Environment record
    - if we declared variable using var it will add into Object Environment record and this object merge with window object  
    - if we declared variable using let,const it will add into Declarative Environment record and this object does not merge into the window object.

</details>

 ####  28. What will be the output ?
 ```js
 let obj ={lang:'react'}
const lib={};
lib.name=obj;
obj=null;
console.log(lib.name);

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - { lang: 'react' }
 - Reason:-
    - lib.name = obj; assigns a reference to the object { lang: 'react'} to lib.name.
    - When obj = null; is executed, it only changes the obj variable to null, but this doesn't affect the reference that lib.name is holding. The object { lang: 'react'} still exists in memory, and lib.name still points to it.  
    - Therefore, console.log(lib.name) will output the original object { lang: 'react' }.
</details>

 ####  29. What will be the output ?
 ```js
 function show(){
this.lang='react';
this.showLang=()=>{
console.log(this.lang)
}
}
const data=new show();
const fn=data.showLang;
fn();

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - react  
 - Reason:-
    -  showLang is defined as an arrow function. Arrow functions do not have their own this; they inherit the this from the context in which they are defined.
</details>

 ####  30. What will be the output ?
 ```js
 var x=[typeof x, typeof y][1];
console.log(typeof typeof x)

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - string  
 - Reason:-
    -  var x=["undefined","undefined"][1] 
    - typeof x: Since x is now "undefined" (a string), typeof x returns "string".
    - typeof typeof x: Since typeof x itself is a string ("string"), typeof typeof x evaluates to "string".
</details>


___  


[Scroll To Top](#my-custom-anchor-point)

## Day 7



 ####  31. What will be the output ?
 ```js
console.log([]=="")
console.log([]==[])

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - true  
    - false  
 - Reason:-
    - When comparing [] (an empty array) with "" (an empty string) using ==, JavaScript performs type coercion.
    - The empty array ([]) is converted to an empty string (""), so the comparison becomes "" == "", which evaluates to true
    - In JavaScript, arrays are reference types, meaning each array is a distinct object in memory
    - Even though both arrays are empty, they are separate objects in memory. Hence, [] == [] compares the references, not the values, and since they are different objects, the result is false.
</details>


 ####  32. What will be the output ?
 ```js
 function switch1(num){
console.log(~~num);
}
switch1(1.2);

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - 1  
 - Reason:-
    - The ~~ (double tilde) is a bitwise operator trick that is commonly used to truncate a floating-point number and convert it into an integer.  
    - The first ~ (bitwise NOT) flips all the bits of the number.
    - The second ~ flips them back but results in a truncated (integer) value.
    - ~~1.2 becomes 1 because the fractional part is discarded.
    -  ~~ this symbol convert decimal number into floating number
</details>


 ####  33. What will be the output ?
 ```js
 async function getData(){
return await Promise.resolve("Promise Resolved")
}
const data=getData();
console.log(data);
data.then(res=>console.log(res));
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - Promise { <pending> }  
    - Promise Resolved  
 - Reason:-
    - Since getData() is an async function, it always returns a Promise, regardless of whether await is used inside the function. 
    - So, when getData() is called, data becomes a Promise. Initially, the Promise is in the pending state.
    - console.log(data) shows that data is a pending Promise.
    - data.then(...) logs the resolved value of the Promise: "Promise Resolved".

</details>


 ####  34. What will be the output ?
 ```js
 const {fName:feDev}={fName:"Sachin"};
console.log(fName)
console.log(feDev)
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - Error  
    - sachin  
 - Reason:-
    - In the code, const {fName: feDev} = {fName: "Sachin"};, you are using object destructuring to extract the fName property from the object and assign it to a new variable feDev. 
    - This means feDev will hold the value of "Sachin".
    - console.log(fName), This throws a ReferenceError because there is no variable named fName in the current scope. The object destructuring assigns the fName value to feDev, not to fName.
    - console.log(feDev), This will print "Sachin" since the value of fName from the object is correctly assigned to feDev.

</details>

 ####  35. What will be the output ?
 ```js
 let list=[1,2].push(3);
console.log(list.push(4))
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - error  
 - Reason:-
    - push is not a function 
    - because push method return length of an array so value list variable is 3 and now list variable is integer and we are try to push value to interger variable thats not correct so throw an error.

</details>

___  


[Scroll To Top](#my-custom-anchor-point)

## Day 8


 ####  36. What will be the output ?
 ```js
 function num(a,b){
if(a > b) console.log(" a is large")
else console.log("b is large")
return
a+b;
}
console.log(num(4,2))
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - a is large  
    - undefined  
 - Reason:-
    - undefined because after semicoln return statement if there is any value is exist then it is undefined
    - but there no semicoln after return satment then js engine automatically added semicolon internally

</details>


 ####  37. What will be the output ?
 ```js
 const one =false || {} || null ;
const two =null || false || ' ' ;
const three=[] || 0 || true;
console.log(one,two,three);
```

<details>
  <summary>View Answer</summary>

### Output:
- `{}` 
- `" "` 
- `[]`

### Reason:
- **JavaScript's logical OR (`||`) operator** evaluates expressions from left to right and returns the first truthy value. If all values are falsy, it returns the last value.

#### Example 1:
```javascript
const one = false || {} || null;
```
- `false` is falsy, so evaluation continues.  
- `{}` (an empty object) is truthy, so the result is `{}`.  
- The evaluation stops here, and `one` is `{}`.

#### Example 2:
```javascript
const two = null || false || ' ';
```
- `null` is falsy, so evaluation continues.  
- `false` is also falsy, so evaluation continues.  
- `' '` (a non-empty string with a space) is truthy, so the result is `' '` (a space).  
- The evaluation stops here, and `two` is `' '`.

#### Example 3:
```javascript
const three = [] || 0 || true;
```
- `[]` (an empty array) is truthy, so the result is `[]`.  
- The evaluation stops here, and `three` is `[]`.
</details>


 ####  38. What will be the output ?
 ```js
 console.log(`${(x=>x)("I Love")} JS`)
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - I Love JS
</details>

 ####  39. What will be the output ?
 ```js
 let randomValue={name:"Sachin"};
randomValue=10;
if(! typeof randomValue ==="string"){
console.log("not a string");
}
else{
console.log("its string")
}

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - its string  
 - Reason:-
    -  typeof randomValue="Number"  
    -  !  "Number"==="string"

</details>

 ####  40. What will be the output ?
 ```js
 const arr = [10,20,30];
arr.slice(0,1);
arr.splice(0,1);
arr.unshift(40);
console.log(arr)

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - [40, 20, 30]
 - Reason :-  

`arr.slice(0, 1);`
- The `slice()` method returns a shallow copy of a portion of an array without modifying the original array.
- `arr.slice(0, 1)` extracts the element at index `0` (which is `10`) and returns `[10]`.
- However, since this returned value is not stored or used, the original array `arr` remains unchanged: `[10, 20, 30]`.

`arr.splice(0, 1);`
- The `splice()` method modifies the original array by removing or replacing elements.
- `arr.splice(0, 1)` removes one element starting at index `0`, which is `10`.
- After this operation, the array becomes: `[20, 30]`.

`arr.unshift(40);`
- The `unshift()` method adds elements to the beginning of the array and modifies the array in place.
- `arr.unshift(40)` adds `40` to the start of the array.
- After this operation, the array becomes: `[40, 20, 30]`.

</details>


___  


[Scroll To Top](#my-custom-anchor-point)

## Day 9

 ####  41. What will be the output ?
 ```js
 let count=0;
const nums =[0,1,2,3];
nums.forEach(num =>{
if(num){
count +=1;
}
})
console.log(count);
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - 3  
 - Reason:-
    - why not 4 because 0 in array is a falsy value then it cant true for falsy value
</details>

 ####  42. Information   
 
  - `Object . Freeze()` method does not allow to update ,delete and addition the object upto level 1

 - `Object.seal ()`  doesn’t allow deletion and addition but it allow updation

 ####  43. What will be the output ?
 ```js
 const arr=[10,20];
({item:arr[2]}={item:30})
console.log(arr)

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - [ 10, 20, 30 ]  
</details>

 ####  43. What will be the output ?
 ```js
 const foo='Sachin';
console.log(! typeof foo =='object');
console.log(! typeof foo =='string');

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - false  
    - false  
 - Reason:-  
     `! typeof foo == 'object':`

- The `typeof foo` is `'string'` because `foo` is assigned the string `'Sachin'`.
- The expression `! typeof foo` is evaluated first because the `!` operator has higher precedence than `==`.
- So, `! typeof foo` becomes `! 'string'`, and in JavaScript, the logical negation of any non-empty string (like `'string'`) is `false`.
- Then, the comparison `false == 'object'` is made, which results in `false` because `false` is not equal to `'object'`.

 `! typeof foo == 'string':`
   

- Similar to the first case, `! typeof foo` becomes `false` since `typeof foo` is `'string'` and negating it results in `false`.
- Then, the comparison `false == 'string'` is made, which again results in `false` because `false` is not equal to `'string'`.

</details>

 ####  44. What will be the output ?
 ```js
 const myFunc =({x,y,z})=>{
console.log(x,y,z);
}
myFunc(1,2,3);
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - undefined undefined undefined  
 - Reason:-
    - because myFunc expecting argument as a object but we are passing numeric value thats why its undefined  

- Correct version
```js   
const myFunc = ({x, y, z}) => {
    console.log(x, y, z);
}

myFunc({x: 1, y: 2, z: 3});

```

 
</details>


 ####  45. What will be the output ?
 ```js
 const add =(x)=>(y)=>(z)=>{
console.log(x+y+z)
}
add(10)(20)(30);

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - 60  
 - Reason:-
    - currying with arrow function
</details>


___  


[Scroll To Top](#my-custom-anchor-point)

## Day 10

 ####  46. What will be the output ?
 ```js
 const arr=[10,20];
if(arr.indexOf(10)){
console.log("hello");
}
else{
console.log("hi");
}

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - hi  
 - Reason:-
    - The indexOf() method returns the index of the first occurrence of the specified element in the array. In this case, arr.indexOf(10) returns 0 because 10 is at index 0 in the array [10, 20]  
    - In JavaScript, if(0) evaluates to false, since 0 is a falsy value.
</details>


 ####  47. What will be the output ?
 ```js
 const obj={name:"sachin"};
obj.ref=obj;
const str=JSON.stringify(obj);
console.log(str)
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - TypeError  
 - Reason:-
    - `Circular Reference`:  
The object obj contains a property ref that refers back to itself: obj.ref = obj;. This creates a circular reference because the object contains itself as one of its properties.

    - `JSON.stringify(obj)`:  
The JSON.stringify() method tries to convert an object into a JSON string. However, JSON does not support circular references. When JSON.stringify() encounters the circular structure, it throws a TypeError because it can't represent the object in JSON format.
    
</details>

 ####  48. What will be the output ?
 ```js
 var hi=900;
function hi(){
console.log("hi")
}

console.log(hi)
console.log(hi())

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - 900  
    - error, hi is not a function  
 - Reason:-
    - When hoisting occurs, variable declarations (var) take precedence over function declarations. So, when the code is interpreted, the variable hi defined as var hi = 900 will overwrite the function hi().  
    - First, the function hi() is hoisted to the top, followed by the variable hi being hoisted and set to undefined.
    - Then, the variable hi is assigned the value 900, which overwrites the function hi.
    - As a result, when you call hi(), it tries to execute hi, which is now 900 (a number), not a function. This leads to the TypeError because 900 is not callable.
</details>

 ####  49. What will be the output ?
 ```js
 const arr=[{key:"S"},'10','20'];
delete arr[0];
console.log(arr.length)
console.log(arr)

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - 3  
    - [ <1 empty item>, '10', '20' ] 
</details>

 ####  50. What will be the output ?
 ```js
 let z=a={};
a.name="Sachin";
console.log(z.name)
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - Sachin  
 - Reason:-
    - let z = a = {}; means both z and a are references to the same empty object {}. This is because in JavaScript, objects are assigned by reference, not by value.
</details>

___  


[Scroll To Top](#my-custom-anchor-point)

## Day 11

 ####  51. What will be the output ?
 ```js
 const dataMap=new WeakMap();
let person={name:"Sachin"};
dataMap.set(person,"TVA");
console.log(dataMap.get(person))
person=null;
console.log(dataMap.get(person));
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - TVA  
    - Undefined  
 - Reason:-
    -  `WeakMap` is a collection of key-value pairs where the keys are objects. It allows for garbage collection of keys when there are no other references to the object, making it useful for cases where you don't want the map to prevent objects from being garbage collected.  
    - `let person = { name: "Sachin" }:` You create an object person and assign it to the variable person.
    - `dataMap.set(person, "TVA"):` This adds the person object as a key in the WeakMap, with the value "TVA".
    - `console.log(dataMap.get(person)):-` At this point, person is still referencing the object { name: "Sachin" }, so dataMap.get(person) will return "TVA".
    - `person = null;:` This line removes the reference to the object { name: "Sachin" }. Since WeakMap holds a weak reference to the key object, it will no longer have access to it because no other variables are referencing that object.
    - After setting person to null, the object is eligible for garbage collection. The key no longer exists in the WeakMap, so dataMap.get(person) will return undefined.
    
</details>

 ####  52. What will be the output ?
 ```js
 let x=10;
let y=20;
[x,y]=[y,x];
console.log(x,y)
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - 20  10  
 - Reason:-
    - swap the value between two variable
</details>

 ####  53. What will be the output ?
 ```js
 let str=new String("JS");
console.log(str==="JS");
console.log(str =="JS");
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - false  
    - true  
 - Reason:-
    - `===` it check type, content,reference store in memory
    -  `==` it check only content and refernce store in memory

</details>

 ####  54. What will be the output ?
 ```js
 const obj={};
obj[obj["A"]="B"]="c"
console.log(obj);
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - { A: "B", B: "c" }  
 - Reason:-
    - `obj["A"] = "B":` This sets the property "A" on obj with the value "B". `{ A: "B" }`
    - `obj[obj["A"]] = "c":` obj["A"] is now "B", so this becomes obj["B"] = "c".  
    This adds a new property "B" to the object with the value "c". `{ A: "B", B: "c" }
    - So the final result of console.log(obj) will output:
       `{ A: "B", B: "c" }
`
`
</details>

 ####  55. What will be the output ?
 ```js
 function init(x,y,z){
}
function end(a,b=0,c){
}
console.log(init.length);
console.log(end.length);

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - 3  
    - 1  
 - Reason:-
    - when we used length property for function then it will count number of parameters thats why answer is 3 
    - `end` function has three parameters: a, b, and c. b has a default value (b = 0), so end.length only counts the parameters before b. Therefore, end.length is 1 (because only a is counted).
</details>


___  


[Scroll To Top](#my-custom-anchor-point)
## Day 12

 ####  56. What will be the output ?
 ```js
 const arr=[1,3,2];
console.log(arr[5]);
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - undefined  
 - Reason:-
    - When you try to access an out-of-bounds index in a JavaScript array, the result is undefined
</details>


 ####  57. create a variable whose name is inside a variable ?
 ```js
 var varName ='lang';


//first way
window[varName]="js is love"
console.log(lang)

```

 ####  58. Make sure the sum function works with n number of arguments ?
 ```js
 function sum(...nums){
  return nums.reduce(function(a,n){
      return a + n
  },0)
}
console.log(sum(2,3))
console.log(sum(2,3,4))
console.log(sum(2,3,4,5))

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - 5  
    - 9 
    - 14 

</details>


 ####  59. What will be the output ?
 ```js
 let bool1= false;
let bool2=new Boolean(false)


if(bool1){
    console.log("first boolean")
}
if(bool2){
    console.log("second boolean")
}

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - second boolean  
    - true  
 - Reason:-
    - first boolean false thats why its not executed  
    - second boolean is created using boolean constructor .when we declard variable using constructor then that variable is object and object is truthy value that's whys second block is executed.
</details>



 ####  60. Make sure expected output is 1 2 3 ?
 ```js
 let obj ={
  val:1,
  get a(){
      return this.val++
  }
}


console.log(obj.a)
console.log(obj.a)
console.log(obj.a)
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - 1  
    - 2
    - 3  

</details>

___  


[Scroll To Top](#my-custom-anchor-point)
## Day 13


 ####  61. What will be the output ?
 ```js
 let arr=[9,8,7,6][1,2,3]
console.log(arr)
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - 6  
 - Reason:-
    - `The comma operator` in JavaScript evaluates each of its operands (from left to right) and returns the value of the last operand. 
    - In your expression [9, 8, 7, 6][1, 2, 3], the comma operator evaluates 1, 2, and 3 in sequence, and then the entire expression returns the value of the last operand, which is 3.
    - Now, this becomes arr[3], where arr = [9, 8, 7, 6].
    - The element at index 3 in the array is 6.
</details>


 ####  62. What will be the output ?
 ```js
 const {
  a='default',
  b='defdault',
  c='default',
  d='default',
  e='default'
}={a:null,b:undefined,c:false,d:0}


console.log(a,b,c,d,e)

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - null  
    - defdault
    - false
    - 0
    - default  
</details>

 ####  63. What will be the output ?
 ```js
 console.log(null > 0)
console.log(null == 0)
console.log(null >= 0)
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - false  
    - false
    - true  
 - Reason:-
    - because > is used to convert null into number ie.0
</details>

 ####  64. What will be the output ?
 ```js
 console.log(typeof [] );
console.log(typeof arguments );
console.log(typeof null );
console.log(typeof NaN );

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - Object  
    - Object
    - Object
    - Number
</details>

 ####  65. What will be the output ?
 ```js
 let num = 0;
console.log(num++); 
console.log(++num); 
console.log(num);
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - 0  
    - 2
    - 2  
</details>

___  


[Scroll To Top](#my-custom-anchor-point)
## Day 14

 ####  66. What will be the output ?
 ```js
 function MCQ1() {
  const person = {
    name: "Jayesh",
    displayName1: function () {
      console.log("name1", this.name);
    },
    displayName2: () => {
      console.log("name2", this.name);
    },
  };

  person.displayName1();
  person.displayName2();
}
MCQ1()
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - name1 Jayesh
    - name2 undefined  
 - Reason:-
    - `displayName1` is a regular function, and in JavaScript, when a regular function is called as a method of an object, the value of this inside the function refers to the object on which it was called (in this case, the person object).  
    - `displayName2` is an arrow function. Arrow functions do not have their own this context. Instead, they inherit this from the lexical scope in which they were defined (the scope in which the arrow function was created).
    - In this case, `displayName2` was defined inside the MCQ1 function, but it does not have its own this. Instead, this in the arrow function refers to the this value of the MCQ1 function, which is global context (in non-strict mode, this is the window object in a browser).
    - Since the window object does not have a name property, `this.name` is `undefined`. Therefore, the output is:
</details>


 ####  67. What will be the output ?
 ```js
 function MCQ2() {
  let name = "Jayesh";
  function printName() {
    if (name === "Jayesh") {
      let name = "JC";
      console.log(name);
    }
    console.log(name);
  }
  printName();
}

MCQ2()
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - JC  
    - Jayesh  
 - Reason:-
    - because let variables are block scope, name inside if condition will shadow outer name 
</details>


 ####  68. What will be the output ?
 ```js
 function MCQ3() {
  var player = "Virat";
  function displayPlayer() {
    if (player === "Virat") {
      var player = "VK";
      console.log(player);
    }
    console.log(player);
  }
  displayPlayer()
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - undefined  
 - Reason:-
    - `undefined` because var variables are functional scope, When `displayPlayer` fn starts executing, Execution context of
   displayPlayer will be created in callstack and at the memory creation phase var variable player is initialized as undefined.
    - hence if condition will become false and It will print only undefined.

</details>

 ####  69. What will be the output ?
 ```js
 function MCQ4() {
  const person = {
    name: "Jayesh",
    age: 24,
  };


  const getAge = person.age;
  delete person.age;


  console.log(person);
  console.log(getAge);
}

MCQ4()
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - { name: 'Jayesh' }  
    - 24  
 - Reason:-
    - because delete keyword deletes property of an object and we are setting getAge as pass by value.  
</details>

 ####  70. What will be the output ?
 ```js
 function MCQ5() {
  // No Strict Mode
  name = "Jayesh"; // window.name ( property of window object )
  console.log(delete name);


  const displayName = (function (name) {
    console.log(delete name); // Local variable of function
    return name;
  })("JC");


  console.log(displayName);
}
MCQ5()
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - true  
    - false
    - JC  
 - Reason:-
    - because delete keyword deletes only property of an object.
    -  delete keyword can not delete local variables ( declared with var, let, and const ) and functions.
    - delete keyword can delete global variables as they are property of window object.
</details>

___  


[Scroll To Top](#my-custom-anchor-point)
## Day 15

 ####  71. What will be the output ?
 ```js
 function MCQ6() {
  const arr = [];


  for (var i = 0; i < 5; i++) {
    arr[i] = function () {
      return i;
    };
  }


  console.log(arr[0]());
  console.log(arr[4]());

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - 5  
    - 5  
 - Reason:-
    - because variables declared with var keyword are function-scoped or globally-scoped but not blocked scoped.  
    -   Inner function will form the closure and points to the updated value of i that is 5.
    - In the case of Let variable, as they are blocked scoped so inner function will hold different values of i from 0 to 4.

</details>

 ####  72. What will be the output ?
 ```js
 function MCQ7() {
  let person = { name: "Jayesh" };
  const personArray = [person];
  person = null;
  console.log(personArray);


  personArray = [];
  console.log(personArray);
}
MCQ7()
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - { name: "Jayesh" };  
    - Type Error, assignment to const variable is not allowd  
</details>

 ####  73. What will be the output ?
 ```js
 function MCQ8() {
  const value = { number: 10 };


  const addition = (x = { ...value }) => {
    console.log((x.number += 5));
  };


  addition();
  addition();
  addition(value);
  addition(value);
}
MCQ8()
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - 15  
    - 15
    - 15
    - 20  
 - Reason:-
    - `First Call: addition():`   
        - The function addition() is called without any arguments, so it uses the default parameter x = { ...value }. This creates a shallow copy of the value object.
        - The shallow copy means that the number property of the new object is 10 (from value), but it is a separate object from value.
        - Then, the function adds 5 to x.number, resulting in x.number = 15.
        - console.log(x.number) logs 15.
    - `Second Call: addition():`
        -  Again, addition() is called without arguments, so a new shallow copy of value is created (separate from the first one).
        - The function adds 5, resulting in x.number = 15 again.  
       
    - `Third Call: addition(value):`
        - This time, value is passed as the argument x, so no copy is made.
        - The function directly modifies the value object.
        - Initially, value.number = 10, and the function adds 5, making value.number = 15.
        - console.log(x.number) logs 15.
    - `Fourth Call: addition(value):`
        - Now, value has already been modified by the previous call and its number property is 15.
        - The function adds 5 again, resulting in value.number = 20.
</details>

 ####  74. What will be the output ?
 ```js
 function MCQ9() {
  function makePerson() {
    return {
      userName: "Jayesh",
      ref: this,
    };
  }


  const person = makePerson();
  console.log(person.ref.userName);
}
MCQ9()
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - undefined  
 - Reason:-
    - because "this" keyword in makePerson function will refer to the window object,
    - person.ref.userName is same as Window.userName and no property named with userName is present in window object, Hence It will console undefined.

- Corrected version
```js
function makePerson2() {
    return {
      userName: "Jayesh",
      // 👇 Here, We have assigned a function to ref property of an object, and function's "this" will point to the returned object.
      ref: function () {
        return this;
      },
    };
  }


  const person2 = makePerson2();
  console.log(person2.ref().userName); // Jayesh
}
MCQ9();

```
</details> 

####  75. What will be the output ?
 ```js
 function MCQ10() {
  const user = {
    userName: "Jayesh",
    displayName: function () {
      console.log(this.userName);
    },
  };


  setTimeout(user.displayName, 1000);
}
MCQ10()
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - undefiend  
 - Reason:-
    - because setTimeout is using user.displayName as a callback function rather than object method.
  
    -  callback function's "this" will refer to the window object and It will console undefined as there is no property such as userName in the window object.  
- Corrected Version

```js
setTimeout(function () {
    user.displayName(); // Here, displayName is called by user object ( object method ). Hence, "this" will refer to user object.
  }, 1000);
}

```
</details>

___  


[Scroll To Top](#my-custom-anchor-point)
## Day 16

 ####  76. What will be the output ?
 ```js
 function MCQ11() {
  const series = { name: "JavaScript-with-JC" };


  function getSatus(postNumber) {
    return `${this.name} 🌟 ${postNumber}`;
  }


  console.log(getSatus.call(series, 50));
  console.log(getSatus.bind(series, 50));
}
MCQ11()
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - JavaScript-with-JC 🌟 50  
    - ƒ bound getSatus() { [native code] }  
 - Reason:-
    - `getSatus.call(series, 50):`  
         - The call() method in JavaScript allows you to invoke a function immediately with a specified this value and arguments.
         - In this case, getSatus.call(series, 50) invokes getSatus with this bound to the series object and passes 50 as the argument (postNumber).

    - `getSatus.bind(series, 50):`
         - The bind() method in JavaScript does not invoke the function immediately. Instead, it returns a new function with a bound this value and preset arguments.
         - When you call getSatus.bind(series, 50), it returns a new function, where this is bound to series, and the first argument is preset to 50. The returned function can then be called later.
         - The result of getSatus.bind(series, 50) is a function, not the actual result of invoking the function.

- Corrected Version:-
```js
 // 👇 We can get 'JavaScript-with-JC 🌟 50, JavaScript-with-JC 🌟 50' as an output by calling borrowed function of bind method :-


  console.log(getSatus.call(series, 50)); // JavaScript-with-JC 🌟 50
  console.log(getSatus.bind(series, 50)()); // JavaScript-with-JC 🌟 50
```
</details>

####  77. What will be the output ?
 ```js
 function MCQ12() {
  var name = "Jayesh";


  function displayName() {
    console.log(this.name);
  }


  const person = {
    name: "JC",
    method(fn) {
      fn();
    },
  };


  person.method(displayName);
}
MCQ12()

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - `Jayesh` in case of browser environment or `Undefined` in case of node js environment  
 - Reason:-
    - `In the browser:`  
       - When you declare a global variable using var at the top level (outside any function), it gets added as a property of the global object (window). So, var name = "Jayesh"; makes window.name = "Jayesh"
       - When displayName is called as a regular function, this inside the function refers to window. So, this.name would resolve to "Jayesh" because window.name exists.

    - `In Node.js:`  
       - Global variables declared with var are not automatically attached to the global object. So, even though var name = "Jayesh"; declares a global variable, it doesn't become global.name.
       - When displayName is invoked as a regular function, this will refer to global, and global.name doesn't exist, resulting in undefined.
</details>


####  78. What will be the output ?
 ```js
 function MCQ13() {
  var length = 4;


  function callback() {
    console.log(this.length);
  }


  const object = {
    length: 5,
    method: function () {
      arguments[0]();
    },
  };


  object.method(callback, 2, 3);
}
MCQ13()
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - 3  
 - Reason:
    - The method object.method(callback, 2, 3) is called, passing the callback function and two other arguments 2 and 3.   
    - Inside the method, the arguments object contains [callback, 2, 3].
    - `arguments[0]()` means the callback function is invoked, but the context (this) of callback is now arguments.
    - When callback() is called as arguments[0](), the this value inside callback refers to the arguments object.
    - The arguments object has a length property, which is equal to the number of arguments passed to method, which is 3 (callback, 2, 3).
    - So, this.length inside the callback function refers to arguments.length, which is 3.

</details>


####  79. What will be the output ?
 ```js
 function MCQ14() {
  var name = "Jayesh";


  function displayName() {
    console.log(this.name);
  }


  const person = {
    name: "JC",
    method: displayName.bind(this),
  };


  person.method();
}
MCQ14()
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - `Jayesh` in browser level or `undefined` in node js level  
 - Reason:-
    - `In a Browser`
       -  In a browser environment, this at the top level refers to the window object.
       - When you declare var name = "Jayesh", it becomes window.name = "Jayesh".
       - When displayName.bind(this) is used, this refers to the global window object.
       - So, when person.method() is called, it will log "Jayesh" because this.name refers to window.name.
    - `In Node.js`
       - In Node.js, this at the top level does not refer to the global object (global). Instead, this is undefined in a top-level script.
       - As a result, when displayName.bind(this) is called, this will refer to undefined. Since this.name does not exist, the output will be undefined.

- Corrected Version:-
```js
function MCQ14() {
  var name = "Jayesh";


  function displayName() {
    console.log(this.name);
  }


  const person2 = {
    name: "JC",
    method: function () {
      return displayName.bind(this); // Here, "this" refers to the person2 object
    },
  };


  person2.method()(); // JC
}

MCQ14()
```
</details>


####  80. What will be the output ?
 ```js
 function MCQ15() {
  function show() {
    console.log(this.name);
  }


  const person1 = { name: "Jc" };
  const person2 = { name: "Jayesh" };


  show = show.bind(person1).bind(person2);
  show();
}
MCQ15()
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - JC  
 - Reason:-
    - because a function which is bound with bind keyword can not be re-bound with other new context, bind chaining does not exist. 
    -  once the function is bound to a particular object, It will always be bound to that object no matter how many times it's further bounded.

</details>


___  


[Scroll To Top](#my-custom-anchor-point)
## Day 17



 ####  81. What will be the output ?
 ```js
 function MCQ16() {
  let person1 = {
    name: { firstName: "Jayesh" },
    age: 24,
  };
  let person2 = { ...person1 };


  person2.name.firstName = "Virat";
  person2.age = 33;


  console.log(person1.name.firstName);
  console.log(person1.age);
}
MCQ16()
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - Virat  
    - 24  
 - Reason:-
    - person2 is created as a shallow copy of person1 using the spread operator: 
    - This means that while person2 has its own copy of the age property, the name property points to the same object reference as person1.name. So both person1.name and person2.name refer to the same object.
    - When you change the firstName in person2:This changes the firstName property in the shared object that both person1.name and person2.name point to. Therefore, person1.name.firstName is also updated to "Virat".
    - Changing person2.age does not affect person1.age because age is a primitive value. person2 has its own copy of the age property:person1.age remains 24 because age is a primitive type and was copied, not referenced.
</details>

 ####  82. What will be the output ?
 ```js
 function MCQ17() {
  for (var i = 0; i < 5; i++) {
    setTimeout((i) => {
        console.log(i);
      },1000,i);
  }
}
MCQ17()
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - 0 1 2 3 4  
 - Reason:-
    - because as we are passing i ( 0 to 4 ) value as an argument to setTimeout callback function
  therefore this will console different values of i from 0 to 4.
    - if there was no argument passed to setTimeout callback function then the output would be 5 5 5 5 5 because variables declared
    -  with var keyword are function-scoped or globally-scoped but not blocked scoped. Inner function i would point to the updated value of i that is 5.
</details>

 ####  83. What will be the output ?
 ```js
 function MCQ18() {
  console.log(1);


  async function fetchData() {
    console.log(2);
    let result = await Promise.resolve(3);
    console.log(result);
  }


  fetchData();
  console.log(4);
}
MCQ18()
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - 1  
    - 2
    - 4
    - 3  
 - Reason:-
    -  beacause promise is used to handle the asynchronous result of an operation and
  callback functions attached to the promises are stored into microtask queue.
    - So, first synchronous code will be executed i.e 1,2,4 and once callstack is empty, event loop pushes the microtask queue's task into callstack
  callstack will start executing the task and It will console 3 at last.

</details>


 ####  84. What will be the output ?
 ```js
 function MCQ19() {
  console.log("start");


  const promise = new Promise((resolve) => {
    console.log(1);
    resolve(2);
    console.log(3);
  });


  promise.then((result) => {
    console.log(result);
  });


  console.log("end");
}
MCQ19()
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - start  
    - 1
    - 3
    - end 
    - 2  
 - Reason:-
    -  beacause The function we pass into the Promise constructor runs synchronously,
  but anything that depends on its resolution ( resolve or reject ) will be called asynchronously.
    -  Even if the promise resolves immediately, any handlers ( callback attached to promise then and catch ) will execute asynchronously.
</details>

 ####  85. What will be the output ?
 ```js
 function MCQ20() {
  console.log("First");


  const promise = new Promise((resolve) => {
    console.log("Second");
  });


  promise.then((result) => {
    console.log(result);
  });


  console.log("Third");
}
MCQ20()
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - first  
    - Second
    - third  
 - Reason:-
    - First Second Third because as there is no resolve in Promise constructor, So it will not go inside of .then block. 
</details>

___  


[Scroll To Top](#my-custom-anchor-point)
## Day 18

 ####  86. What will be the output ?
 ```js
 function MCQ21() {
  const fetchData = function () {
    return new Promise((resolve, reject) => {
      reject();
    });
  };


  fetchData()
    .then(() => {
      console.log("Success 1");
    })
    .catch(() => {
      console.log("Error 1");
    })
    .then(() => {
      console.log("Success 2");
    });
}
MCQ21()
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - Error 1  
    - Suceess 2  
 - Reason:-
    - because in promise chaining .then method below .catch method will be called if in .catch method we are not
  returning rejected promise ( by default implicitly returns a promise that is handled by it's below .then method )
</details>


 ####  87. What will be the output ?
 ```js
 function MCQ24() {
  const person1 = {
    name: "Jayesh",
    age: 24,
  };


  const person2 = person1;
  person2.name = "Virat";


  console.log(person1.name);
  console.log(person2.name);
}
MCQ24()
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - Virat  
    - Virat  
 - Reason:-
    -  because objects are passed as a reference, person1 and person2 will hold the same memory address
  and altering any property of person2 will modify property of person1 as well. 
</details>


 ####  88. What will be the output ?
 ```js
 const fetchData = function(){
  return new Promise((res, reject)=>{
    reject("Error!!")
  })
}


fetchData()
.then(null, (err)=>{
  console.log("First");
  console.log(err);
})
.catch(()=>{
  console.log("Second");
  console.log(err)
})

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - First  
    - Error !!  
 - Reason:-
    - After the then(), there is a catch() method. However, since the rejection was already handled by the error callback in the previous then(), the catch() will not execute. In addition, there is a potential error here:
</details>

####  89. What will be the output ?
 ```js
 displayName();
var displayName = function(){
  console.log("Priya")
}
function displayName(){
  console.log("dolly")
}
displayName();

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - Dolly  
    - Priya  
 - Reason:-
    - Normal function will get execute before, because of function Hoisting concept, then function expression wil get execute. 
</details>


 ####  90. What will be the output ?
 ```js
 const inc = async(x) => {
  x = x + await 1; 
  return x;
}


const increment = async(x) =>{
  x = x+1; 
  return x; 
}

inc(1)
.then((x)=>{ 
  increment(x) 
  .then((x)=>console.log(x)) 
})

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - 3  

</details>

___  


[Scroll To Top](#my-custom-anchor-point)
## Day 19

 ####  91. What will be the output ?
 ```js
 

const promise = () => Promise.resolve("Success");

function first(){
  promise().then((res)=> console.log(res)); //async
  console.log("First"); //sync
}

async function second(){
  const res = await promise();
  console.log(res); //async
  console.log("Second"); //sync
}
first();
second();

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - First  
    - success  
    - success
    - second
</details>

 ####  92. What will be the output ?
 ```js
 const person1 = {
  name : "Priya"
}
const person2 = {
  name : "Dolly"
}
const person = Object.assign(person1, person2);


console.log(person); 
console.log(person.name); 
console.log(person1.name); 
console.log(person2.name); 

```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - { name: 'Dolly' }  
    - Dolly
    - Dolly
    - Dolly
     
 - Reason:-
    - The Object.assign() method is used to copy the properties of person2 into person1:
</details>

 ####  93. What will be the output ?
 ```js
 const array = [8, 18, 28, 38];
const result = array.map(element => element + 2)
               .filter((element) => element > 25);
console.log(result);
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - [30,40]  
</details>

 ####  94. What will be the output ?
 ```js
 const userDetails = {
  firstName: "Surbhi",
  lastName: "Dighe",
  age: 20,
  address: {
    city: "Hyderabad",
    country: "India",
  },
};

let cloneUserDetails = { ...userDetails };
//Updating original object
userDetails.age = 22;
userDetails.address.city = "Banglore";

console.log(cloneUserDetails.age); 
console.log(cloneUserDetails.address.city);
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - 20  
    - Banglore  
 - Reason:-
    - The age property in cloneUserDetails remains 20 because the change was made to the original object. 
    - The city property in cloneUserDetails.address shows Banglore because it is a reference to the same address object that was modified in userDetails.

</details>

 ####  95. What will be the output ?
 ```js
 function checkAge(data) {
  if (data === { age: 18 }) {
    console.log('You are an adult!');
  } else if (data == { age: 18 }) {
    console.log('You are still an adult.');
  } else {
    console.log(`Hmm.. You don't have an age I guess`);
  }
}

checkAge({ age: 18 });
```
<details>
 <summary>View Answer</summary>

 - Output:-  
    - Hmm.. You don't have an age I guess
   - Reason:-
    - When testing equality, primitives are compared by their value, while objects are compared by their reference. JavaScript checks if the objects have a reference to the same location in memory.
    - The two objects that we are comparing don't have that: the object we passed as a parameter refers to a different location in memory than the object we used in order to check equality.
    - This is why both `{ age: 18 } === { age: 18 }` and `{ age: 18 } == { age: 18 }` return false.
</details>





