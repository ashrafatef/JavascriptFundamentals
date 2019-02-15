
- Today we will talk about one of the most fundamental topic in javascript , it is "Hoisting" , hoisting one of concepts that is make 
  javascript behaviour different from other programming language. what I mean here about hoisting changing code behaviour in 
  javascript is you may write code you expect an output but when execute it another output appera one of reasons of this problem is you 
  don't know how your code comipled how javascript engin see your code , so let's know what is hoisting. 
  
- Hoisting is that your variables and function are hoisted up within your scope , there are two types of hoisting : variable hoisting and function hoisting , let's see what I mean through code 
```javascript
  sayHi(); // output "Hello world" !!!
  function sayHi(){
    console.log("Hello world");
  }
```
Whaaaaaat !!! .. how even function called and output value before it defined ! . That is what I mean with function hoisting , which is move function up in file , so what is reaaly happened .
```javascript
  function sayHi(){ // <------------ moved up  
    console.log("Hello world");
  }
  sayHi(); // output "Hello world" !!!
```
- that is happend for all functions but wait a minute there are two types for writing function : function declaration and function           experision , is that happened to both ? No , and that take us to second hoisting type which is variable hoisting

- The same happened in variable hoisting which is variable declaration hoisted up in your scope , more clearer in below example 
```javascript
  console.log(a); // output : undefined 
  var a = 3 ;
```
- here what is happend while comipling this javascript code , in compilation phase variable (a) decalared and initilized to undefined       value and in execution phase when it execute console.log fucntion it finds variable (a) has value undefined so it output this value and   works fine 
- the same in function expersion , it finds variable that holds function is undefiend and thrown error 
```javascript
  sayHi(); // output : Uncaught TypeError: sayHi is not a function 
  var sayHi = function(){
    console.log("Hello World");
  }
```
