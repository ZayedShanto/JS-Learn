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
 
 ```js
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
If return statement is not added inside function by default it returns **undefined** and exits from function

#### Example

```js
function sleep(x, y){
    console.log("hello");
}

let x = sleep(5,5);
console.log(x);

```

```
 output: undefined
 
``` 


## Object

#### Example

```js
  const bike = {

     name: "Yamaha",
     model: "R15",
     color: "grey",
     start: function(){
         console.log("bike has started");     
     }
  };

  console.log(bike.model);
  console.log(bike["model"]);
  bike.start();

```

```
output:
R15
R15
bike has started

```
here bike is the object
properties:name,model,color

## Events

## Strings 
In JS strings are written inside quotes
#### Example

```js
 let x = "Among the supercars 'Ferrari' is the best"; /allowed
 let x = 'Among the supercars "Ferrari" is the best'; /allowed
 let x = "Among the supercars "Ferrari" is the best"; / not allowed
 
 ```
 
 ```
   same quotes not allowed
 
 ```
 
 The soluion of the above problem is the backslash(\) **escape character**
 
 ```js
  let x = "Among the supercars \"Ferrari\" is the best";
  let y = "It\'s the best";
  let z = "Among the supercars \\Ferrari\\ is the best";
  console.log(x);
  console.log(y);
  console.log(z);
  
 ```
 
 ```
  Among the supercars "Ferrari" is the best
  It's the best
  Among the supercars \Ferrari\ is the best

 ```
 
 We can create strings as object using **new** keyword
 
 #### Example
 
 ```js
  let x = "batman";
  let y = new String("batman");

  console.log(x == y);
  console.log(x === y);
 
 ```
 
 ```
  true
  false
 
 ```
 
== only compares value thats why first output is true
=== compares value+type so the secodnd output is false
but comparing two objects will always return false

```js
 let x = new String("batman");
 let y = new String("batman");

 console.log(x == y);
 console.log(x === y);

```

```
  false
  false
```  

## String methods
  - ## String slice()
  - slice() method cuts a part of a string and returns ii a new string
  
  ```js
  let x = "Apple, Banana, Kiwi";
  let y = x.slice(-13 , -7);
  let z = x.slice(7 , 13);
  let a = x.slice(7);

  console.log(y);
  console.log(z);
  console.log(a);
  
  ```
  
  ```
  outout:
   Banan
   Banana
   Banana, Kiwi
 
  ```
    
    
   - ## substring()
   - substring() is similar to slice() but it does not take negative indexes
   
   ```js
    let x = "Apple, Banana, Kiwi";
    let y = x.substring(7 , 13);
    console.log(y);
    
   ```
   
   ```
    output: banana
    
   ``` 
    
   - ## substr()
   - It's also similar to slice() but it's second parameter is the length of the extracted string
   
   #### Example 
   
   ```js
    let x = "Apple, Banana, Kiwi";
    let y = x.substr(7 , 6);
    console.log(y);
    
   ```
   
   ```
     output: banana
     
   ```  

   - ## replace()
   - with this method we can replace a value with another from a string
   - this method has two parameters
   - first parameter takes the value which will be changed
   - the second parameter takes the new value
   
   ```js
    let x = "I love coke";
    let y = x.replace("love" , "like");
    console.log(y);
    console.log(x);
   
   ```
   
   ```
    output:
     I like coke
     I love coke
     
   ```
    
    
  here the replace() doesn't change the string in x variable
  it returns a new string
     
   - ## replace() method only replace the first match
     
   #### Example
   
   ```js
    let x = "I like coke and coke";
    let y = x.replace("coke" , "pepsi");
    console.log(y);
    
   ```
   
   ```
   output:
     I like pepsi and coke
   ```
    
    
   - ## toUpperCase()
   - converts strings to upper case
   
   #### Example
   
   ```js 
    let x = "I like coke ";
    let y = x.toUpperCase();
    console.log(y);
   
   ```
   
   ```
    output:I LIKE COKE 
   
   ``` 
