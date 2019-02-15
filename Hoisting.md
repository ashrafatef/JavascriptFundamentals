- Today we will talk about one of the most fundamental topic in javascript , it is "Hoisting" , hoisting one of concepts that is make 
  javascript behaviour different from other programming language. what I mean here about hoisting changing code behaviour in 
  javascript is you may write code you expect an output but when execute it another output appera one of reasons of this problem is you 
  don't know how your code comipled how javascript engin see your code , so let's know what is hoisting. 
  
- Hoisting is that your variables and function are hoisted up within your scope , let's see what I mean through code 
```javascript
  //index.js file
  sayHi(); // output "Hello world" !!!
  function sayHi(){
    console.log("Hello world");
  }
```
