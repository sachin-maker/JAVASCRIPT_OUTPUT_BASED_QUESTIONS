# 🚀 Javascript Output Based Questions
#### 😍This repo contain 100+ javascript Output based questions With detail explaination which we will cover each and every topic and and i will add 5 question every day.
___

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


[Scroll_To_Top](README.md)

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
 


  






