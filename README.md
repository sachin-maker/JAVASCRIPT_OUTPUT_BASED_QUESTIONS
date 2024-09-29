# Javascript Output Based Questions
#### This repo contain 100+ javascript Output based questions With detail explaination which we will cover each and every topic and and i will add 5 question every day.
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


