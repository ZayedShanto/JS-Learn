# JS-Learn

[abcd](#js-statements)

## Output
JS can display output in many ways.Some of them are:
- ## innerHTML
  document.getElementById(id) method of JS can access HTML element.
  id attribute will the HTML element. The innerHTML property defines the HTML content:
  
  #### Example
  
  ```js
  <p id="demo"></p>
    <script>
      document.getElementById("demo").innerHTML = 11;
    </script>
  
  ```
  
  **Answer:** `output will be 11`
  
   #### Example
  
  ```js
  <p id="demo">abcd</p>
   <script>
    document.getElementById("demo").innerHTML = 6 + 6;
   </script>
  
  ```
   **Answer:** `output will be 12`
  
  - ## document.write()

   ```js
      <p> new doc</p>
     <script>
       document.write(11);
    </script>


   ```
  
  **Answer:**   
  
  ```
     new doc 
     11
     
  ```   
   - ## JS Values
      JS has two type of values
     
      - fixed values
      - variable values
               
     -  Fixed values are called **Literals** .
      - Variable values are called **Variables** .
               
               
## JS Expressions
 An expression is a combination of values, variables, and operators, which computes to a value.
 JS expressions can not contain keywords like var,let,const
   #### Example
  
  ```js
 <p id="demo"></p>
 <script>
 document.getElementById("demo").innerHTML = 5 * 10;
 </script>


  
  ```
  
  
  ## JS Statements
   JavaScript statements are contains:
   Values, Operators, Expressions, Keywords, and Comments.
   Statements can contain  expressions
   
  #### Example
  
  ```js
  <p id="demo"></p>
  <script>
  document.getElementById("demo").innerHTML = "Hello Dolly.";
  </script>

  ```
  
  ## JS Variables
   - ## let variable
   - Variables defined with let cannot be redeclared.
  
     #### Example
  
  ```js
   let x = "Iron Man";

   let x = 0;

   // SyntaxError: 'x' has already been declared

  ```
  
   - ## var variable
   - Variables defined with var can be redeclared.
  
     #### Example
  
  ```js
   var x = "Iron Man";

   var x = 0; //allowed

   

  ```
  
  ## JS Block Scope
  Variables declared inside a { } block cannot be accessed from outside the block:
  
   #### Example
  
  ```js
    let x = 4;
    if (true){
    let x = 6;
    console.log(x);
    }

    console.log(x);

  ```
   **Answer:**   
  
  ```
     6
     4
     
  ``` 
  Variables declared inside a { } block can be accessed from outside the block.
  #### Example
  
  ```js
   { 
    var x = 2; 
   }
    // x CAN be used here

  ```
  ## Redeclearing Variables
  Redeclaring a variable using the var keyword can create problems.
  Redeclaring a variable inside a block will also redeclare the variable outside the block
  
   #### Example
  
  ```js
  var  x = 10;
  console.log(x);

  {  
   var x = 2;

  }
   console.log(x);

  ```
  **Answer:**   
  
  ```
     10
     2
     
  ``` 
  Redeclaring a variable using the let keyword will fix this problem.
   #### Example
  
  ```js
    let  x = 10;
    console.log(x);

    {  
      let x = 2;
      console.log(x);
    }
    console.log(x);

  ```
  **Answer:**   
  
  ```
     10
     2
     10
     
  ```
  ## Redeclearing 
   var can be redeclearedis  anywhere in a program
  
  
  #### Example
    
    
    ```js
     var x = 2;
     // Now x is 2

      var x = 3;
      // Now x is 3

     ```
   redeclaring let in the same block is NOT allowed
   
   #### Example
   
   
     ```js
      var x = 2;    // Allowed
      let x = 3;    // Not allowed

      {
       let x = 2;    // Allowed
       let x = 3     // Not allowed
       }

       {
        let x = 2;    // Allowed
        var x = 3     // Not allowed
        }

     ```
   
   ## let hoisting
   Variables defined with var,const and let are hoisted to the top.But var can only be initialized at any time.
   Meaning: the variable can be used  before it is declared.
   
   #### Example
    ```js
      carName = "volvo";
      var carName;
      console.log(carName);
    ```
     
   **Answer:**   
  
  ```
     volvo
     
  ```
  this is possible because var is hoisted to the top and initialize a default value **undefined**
  **undefined** is a is a property of the global object.That is, it is a variable in global scope.
  The initial value of **undefined** is the **primitive** value undefined.
  But let and const are not initialized like var.
  
   #### Example
     ```js
      carName = "volvo";
      let carName;
      console.log(carName);

     ```
   **Answer:**   
  
  ```
     ReferenceError
     
  ```
  
   #### Example
     ```js
      carName = "volvo";
      let carName;
      console.log(carName);

     ```
   **Answer:**   
  
  ```
     synta error
     
  ```
  
  ## const variable
  const is similar to let variable.but it must be assigned at time of declaration.const can not be reassigned .
  
  #### Example
  
  ```js
  const x = 2;
  const y = 3;
  const z = x+y;
  z = 10
  console.log(z);
  
  ```
  
  ```
   Uncaught TypeError: Assignment to constant variable
  
  ```


  ## Function
  function is a block of code.It can perform particular task. It has to be called to perform.
  
  #### Example
  
  ```js
  function sleep(){
    console.log("xyz");
  }
  sleep();
 
 ```
 
 ```
  outout: xyz
  
 ``` 
 
 variables inside function parentheses () are called **parameters**. And values received by function when it is invoked is **arguments**
 
 #### Example
 
 ```js
 function sleep(x, y){
    console.log(x);
 }

 sleep(5);
 
 ```
 ```
  here x and y are parameters 
  and 5 is the argement
 
 ```
 
 ## Function return
 inside function when JS reaches **return** statement it stops executing.
 
 #### Example
 
 ````js
  function sleep(x, y){
    return x*y;
    console.log("hello");
  }

 let x = sleep(5,5);
 console.log(x);

```

```
  output: 25
  
```  
