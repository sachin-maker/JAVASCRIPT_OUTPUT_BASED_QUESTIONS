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
```
<details>
 <summary>View Answer</summary>

 - Output:
    - 1
    - -1
    - 0
    - -0 (or 0)
    - false
  
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








