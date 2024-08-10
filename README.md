# Here are 100 basic JavaScript interview questions along with their answers

1. **What is JavaScript?**<br>

   JavaScript is a high-level, interpreted programming language used to create interactive effects within web browsers.

2. **What are the data types in JavaScript?**<br>

   The main data types in JavaScript are: `Number`, `Bigint`, `String`, `Boolean`, `Object`, `Undefined`, `Null`, and `Symbol`

3. **What is a variable in JavaScript?**

   A variable is a container for storing data values. Variables are declared using the `var`, `let`, or `const` keywords.

4. **What is the difference between `var`, `let`, and `const`?**

   | **Aspect**         | **`var`**                                                                                   | **`let`**                                                                             | **`const`**                                                                     |
   | ------------------ | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
   | **Scope**          | Function scope or global scope if declared outside a function.                              | Block scope (within curly braces `{}`).                                               | Block scope (within curly braces `{}`).                                         |
   | **Hoisting**       | Variables are hoisted to the top of their scope and initialized with `undefined`.           | Variables are hoisted to the top of their block but not initialized.                  | Variables are hoisted to the top of their block but not initialized.            |
   | **Re-declaration** | Can be re-declared within the same scope.                                                   | Cannot be re-declared within the same block.                                          | Cannot be re-declared within the same block.                                    |
   | **Re-assignment**  | Can be re-assigned new values.                                                              | Can be re-assigned new values.                                                        | Cannot be re-assigned after initial assignment.                                 |
   | **Initialization** | Can be declared without initialization.                                                     | Must be initialized at the time of declaration or later.                              | Must be initialized at the time of declaration.                                 |
   | **Usage**          | Can lead to unexpected results due to function scope and hoisting.                          | Provides better control with block scope and avoids some issues with `var`.           | Ensures values remain constant, useful for constants and immutable references.  |
   | **Examples**       | <code>var x = 10;<br>function test() {<br> var x = 20;<br>}<br>console.log(x); // 10</code> | <code>let y = 10;<br>if (true) {<br> let y = 20;<br>}<br>console.log(y); // 10</code> | <code>const z = 10;<br>z = 20; // Error: Assignment to constant variable</code> |

5. **What is the difference between `null` and `undefined`?**

   | **Aspect**                             | **`null`**                                                                                                           | **`undefined`**                                                                                                                                                  |
   | -------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   | **Type**                               | `object`                                                                                                             | `undefined`                                                                                                                                                      |
   | **Meaning**                            | Represents the intentional absence of any object value. Used to explicitly indicate that a variable should be empty. | Indicates that a variable has been declared but not yet initialized with a value. Also used as the default return value of functions without a return statement. |
   | **Default Value**                      | Must be explicitly assigned.                                                                                         | Automatically assigned to variables that are declared but not initialized.                                                                                       |
   | **Usage**                              | Used to explicitly signify emptiness or to reset a variable.                                                         | Indicates lack of initialization or absence of value implicitly.                                                                                                 |
   | **Assignment**                         | It is an assignment value. Can be assigned to a variable to indicate that it does not point to any object.           | It is not an assignment value. It means a variable has been declared but has not yet been assigned a value.                                                      |
   | **Primitive Value Representation**     | Represents the null, empty, or non-existent reference.                                                               | Used when a variable has not been assigned a value.                                                                                                              |
   | **Indicates Absence Of**               | Indicates the absence of a value for a variable.                                                                     | Indicates the absence of the variable itself.                                                                                                                    |
   | **Conversion in Primitive Operations** | Null is converted to zero (0) while performing primitive operations.                                                 | Undefined is converted to NaN while performing primitive operations.                                                                                             |
   | **Example**                            | `javascript<br>let y = null;<br>console.log(y); // null<br>`                                                         | `javascript<br>let x;<br>console.log(x); // undefined<br>`                                                                                                       |

6. **What is a function in JavaScript? How do you define a function in JavaScript?**

   A function is a block of code designed to perform a particular task, and it is executed when something invokes it.

   ```javascript
   function myFunction() {
     // code to be executed
   }
   ```

7. **What is a function expression?**

   A function expression is a function defined inside an expression instead of a declaration.

   ```javascript
   let myFunction = function () {
     // code to be executed
   };
   ```

8. **What are arrow functions?**

   Arrow functions are a concise syntax for writing function expressions using the `=>` syntax.

   ```javascript
   const myFunction = () => {
     // code to be executed
   };
   ```

9. **What is the difference between function declarations and function expressions?**

   Function declarations are hoisted and can be called before they are defined, while function expressions are not hoisted.
   | **Aspect** | **Function Declarations** | **Function Expressions** |
   |-----------------------------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
   | **Syntax** | <code>function myFunction() {<br> // code<br>}<code> | <code>const myFunction = function() {<br> // code<br>};<code> |
   | **Hoisting** | Function declarations are hoisted. The function can be called before its declaration in the code. | Function expressions are not hoisted. They must be defined before they are used. |
   | **Named or Anonymous** | Can be named. | Can be named or anonymous. |
   | **Execution Context** | Available throughout the scope in which they are defined, even before the declaration. | Available only after the execution context where they are defined. |
   | **Usage** | Typically used for defining functions that will be used across multiple places or globally. | Often used for creating functions that are used as arguments or to assign to variables or properties. |
   | **Example** | <code>function greet() {<br> console.log("Hello!");<br>}<code> | <code>const greet = function() {<br> console.log("Hello!");<br>};<code> |
   | **Self-Invocation** | Not typically used for self-invocation (immediately-invoked function expressions). | Can be used for self-invocation. Example: <code>(function() {<br> console.log("Immediately Invoked");<br>})();<code>
   | **Parameters** | Can be defined with parameters, and the function will be available throughout its scope. | Can also be defined with parameters, but must be assigned to a variable before it can be invoked. |
   | **Binding Behavior** | Bound to the function name within its scope. | Bound to the variable or property it is assigned to. |
   | **Usage in Object Methods** | Often used directly within objects or as methods in classes. | Often used as methods within objects or classes, especially in ES6 classes. |

10. **What is a JavaScript object? How do you create an object in JavaScript?**

    A JavaScript object is a collection of key-value pairs where the keys are strings (or Symbols) and the values can be of any data type. Objects are used to store and organize data and functions.

    **Methods for Defining JavaScript Objects:**

    - Using an Object Literal
    - Using the new Keyword
    - Using an Object Constructor
    - Using Object.assign()
    - Using Object.create()
    - Using Object.fromEntries()

11. **What is the `this` keyword in JavaScript?**

    `this` refers to the object from which it was called. Its value depends on the context in which the function is called.

12. **What is the `this` keyword in traditional and arrow function?**

    | **Aspect**               | **Traditional Functions**                                                                                       | **Arrow Functions**                                                                       |
    | ------------------------ | --------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
    | **Definition**           | Function expressions and declarations.                                                                          | Functions defined with the arrow syntax (`() => {}`).                                     |
    | **Binding of `this`**    | Dynamically bound based on the call site.                                                                       | Lexically bound based on the surrounding context where the arrow function is defined.     |
    | **Method Calls**         | `this` refers to the object that owns the method.                                                               | `this` refers to the object that owns the method (inherits from the surrounding context). |
    | **Function Calls**       | `this` refers to the global object (`window` in browsers or `global` in Node.js) or `undefined` in strict mode. | `this` refers to the surrounding lexical context (not the global object).                 |
    | **Constructor Calls**    | `this` refers to the newly created object.                                                                      | Not applicable, as arrow functions cannot be used as constructors.                        |
    | **Usage with Callbacks** | Can lead to issues with `this` binding inside callbacks or nested functions.                                    | Preserves the `this` value of the enclosing context, making it useful for callbacks.      |

13. **What is the DOM?**

    The DOM (Document Object Model) is a programming interface for HTML and XML documents, representing the page so that programs can change the document structure, style, and content.

14. **What are phases of DOM event handling?**

    | **Phase**           | **Description**                                                                               | **Event Triggering**                                                         |
    | ------------------- | --------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
    | **Capturing Phase** | The event starts from the outermost element and propagates inward towards the target element. | The event is captured by the outermost ancestor elements first.              |
    | **Target Phase**    | The event reaches the target element, where the actual event handling occurs.                 | The event is handled by the target element itself.                           |
    | **Bubbling Phase**  | The event bubbles up from the target element back up to the outer elements.                   | The event is processed by ancestor elements from the target element outward. |

15. **How do you select elements in JavaScript?**

- **By ID:**

  ```javascript
  document.getElementById("myElement");
  ```

- **By Class Name:**

  ```javascript
  document.getElementsByClassName("myClass");
  ```

- **By Tag Name:**
  ```javascript
  document.getElementsByTagName("div");
  ```

18. **What is difference between querySelector and querySelectorAll?**

    | Feature            | `querySelector`                                             | `querySelectorAll`                                                              |
    | ------------------ | ----------------------------------------------------------- | ------------------------------------------------------------------------------- |
    | **Definition**     | Selects the first element that matches a CSS selector.      | Selects all elements that match a CSS selector.                                 |
    | **Return Type**    | Single `Element` object (or `null` if no match).            | `NodeList` of elements (or an empty `NodeList` if no match).                    |
    | **Usage**          | `document.querySelector('selector')`                        | `document.querySelectorAll('selector')`                                         |
    | **Performance**    | Generally faster for single element queries.                | Can be slower if there are many elements because it returns a list.             |
    | **Example**        | `const firstItem = document.querySelector('.item');`        | `const allItems = document.querySelectorAll('.item');`                          |
    | **Modification**   | You can directly modify the single element returned.        | You need to iterate over the `NodeList` to modify multiple elements.            |
    | **Pseudo-Classes** | Supports pseudo-classes like `:first-child`, `:last-child`. | Supports pseudo-classes in a similar way, but applies to all matching elements. |

19. **What is an event in JavaScript? How do you add an event listener in JavaScript?**

    An event is an action or occurrence detected by JavaScript. Here's some common JavaScript events:

    - **User Actions**: `click`, `dblclick`, `keydown`, `keyup`, `mousemove`, `scroll`, etc.
    - **Browser Actions**: `load`, `unload`, `resize`, `focus`, `blur`, etc.
    - **Form Events**: `submit`, `change`, `input`, `reset`, etc.
    - **Media Events**: `play`, `pause`, `ended`, `volumechange`, etc.

      ```javascript
      element.addEventListener("click", function () {
        // code to execute
      });
      ```

20. **What is event bubbling?**

    Event bubbling is the process by which an event starts at the target element and then bubbles up to its parent elements.

21. **What is event capturing?**
    Event capturing is the opposite of event bubbling, where the event starts from the root and propagates down to the target element.

22. **What is a Promise in JavaScript? How do you create a Promise?**

    A Promise is an object representing the eventual completion or failure of an asynchronous operation.

    ```javascript
    let myPromise = new Promise((resolve, reject) => {
      // asynchronous operation
      if (success) {
        resolve(result);
      } else {
        reject(error);
      }
    });
    ```

23. **What are the states of a Promise?**

    | State         | Description                                                                                    | Actions                                                |
    | ------------- | ---------------------------------------------------------------------------------------------- | ------------------------------------------------------ |
    | **Pending**   | The initial state of a Promise. The operation represented by the Promise is not yet completed. | The Promise is waiting for the operation to complete.  |
    | **Fulfilled** | The operation completed successfully. The Promise has resolved with a result value.            | The `.then()` method can be used to handle the result. |
    | **Rejected**  | The operation failed. The Promise has been rejected with a reason or error.                    | The `.catch()` method can be used to handle the error. |

24. **What is the difference between `==` and `===`?**

    | Feature             | `==` (Equality)                                                                   | `===` (Strict Equality)                                                             |
    | ------------------- | --------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
    | **Definition**      | Compares two values for equality, performing type conversion if necessary.        | Compares two values for equality without type conversion.                           |
    | **Type Conversion** | Yes, performs type conversion (coercion) before comparison.                       | No, does not perform type conversion; values must be of the same type.              |
    | **Usage**           | Often used when you are okay with type coercion and want to check value equality. | Preferred when you need strict type and value equality to avoid unexpected results. |

    #### Examples in Code:

    ```javascript
    // Equality (==) Example
    console.log(5 == "5"); // true, because '5' is converted to number 5
    console.log(0 == false); // true, because false is converted to number 0
    console.log(null == undefined); // true, because null and undefined are considered equal

    // Strict Equality (===) Example
    console.log(5 === "5"); // false, different types (number and string)
    console.log(0 === false); // false, different types (number and boolean)
    console.log(null === undefined); // false, different types (null and undefined)
    ```

25. **What are template literals?**

    Template literals are string literals allowing embedded expressions, enclosed by backticks (`` ` ``).

    ```javascript
    let name = `John`;
    let message = `Hello, ${name}!`;
    ```

26. **What are default parameters in JavaScript functions?**

    Default parameters allow named parameters to be initialized with default values if no value or `undefined` is passed.

    ```javascript
    function myFunction(x = 10) {
      // x is 10 if not provided
    }
    ```

27. **What is destructuring assignment?**

    Destructuring assignment is a syntax that allows extracting values from arrays or objects into distinct variables.

    ```javascript
    let [a, b] = [1, 2];
    let { x, y } = { x: 10, y: 20 };
    ```

28. **What are rest parameters?**

    Rest parameters allow a function to accept an indefinite number of arguments as an array.

    ```javascript
    function myFunction(...args) {
      // args is an array of all arguments
    }
    ```

29. **What is the `map` method in JavaScript?**

    The `map` method in JavaScript is used to create a new array by applying a function to each element of an existing array. It doesn't modify the original array but instead returns a new array with the results of the function applied to each element.

    ```javascript
    let newArr = arr.map((element) => element * 2);
    ```

    #### Common Use Cases

    - **Transforming Data**: Converting data from one format to another.
    - **Extracting Properties**: Creating an array of specific properties from objects.
    - **Applying Functions**: Applying a function to each element in an array.

    Here’s another example where we extract names from an array of objects:

    ```javascript
    const users = [
      { id: 1, name: "Alice" },
      { id: 2, name: "Bob" },
      { id: 3, name: "Charlie" },
    ];

    // Create a new array containing only the names
    const names = users.map((user) => user.name);

    console.log(names); // ['Alice', 'Bob', 'Charlie']
    ```

30. **What is the `filter` method in JavaScript?**

    The `filter` method in JavaScript is used to create a new array containing all elements that pass a test implemented by a provided function. It allows you to filter out elements from an array based on certain criteria without modifying the original array.

    ```javascript
    const numbers = [5, 12, 8, 130, 44];

    // Create a new array with numbers greater than 10
    const bigNumbers = numbers.filter((number) => number > 10);

    console.log(bigNumbers); // [12, 130, 44]
    ```

    ### Common Use Cases

    - **Filtering Data**: Extracting elements that meet specific criteria.
    - **Removing Items**: Creating a new array that excludes certain elements.
    - **Selecting Subsets**: Finding elements that match certain conditions from a larger set.

    Here’s another example where we filter an array of objects to find users older than 18:

    ```javascript
    const users = [
      { name: "Alice", age: 17 },
      { name: "Bob", age: 25 },
      { name: "Charlie", age: 30 },
      { name: "Dave", age: 15 },
    ];

    // Create a new array with users older than 18
    const adults = users.filter((user) => user.age > 18);

    console.log(adults);
    // [{ name: 'Bob', age: 25 }, { name: 'Charlie', age: 30 }]
    ```

31. **What is the `reduce` method in JavaScript?**

    The `reduce` method in JavaScript is used to apply a function against an accumulator and each element in an array (from left to right) to reduce it to a single value. It’s often used to perform operations like summing numbers, concatenating strings, or accumulating results based on array elements.

    ```javascript
    const numbers = [1, 2, 3, 4, 5];

    const sum = numbers.reduce((accumulator, currentValue) => {
      return accumulator + currentValue;
    }, 0);

    console.log(sum); // Output: 15
    ```

32. **What is a closure in JavaScript?**

    A closure is a function that retains access to its outer scope variables even after the outer function has finished executing.

    ```javascript
    function outerFunction(outerVariable) {
      return function innerFunction(innerVariable) {
        console.log(`Outer variable: ${outerVariable}`);
        console.log(`Inner variable: ${innerVariable}`);
      };
    }

    const myClosure = outerFunction("outerValue");
    myClosure("innerValue");
    ```

33. **What is the difference between `call` and `apply`?**

    Both `call` and `apply` are used to invoke functions with a specified `this` value, but `call` takes arguments separately, while `apply` takes arguments as an array.

    ### Examples

    **Using `call`:**

    ```javascript
    function greet(greeting, punctuation) {
      console.log(greeting + ", " + this.name + punctuation);
    }

    const person = { name: "Alice" };

    greet.call(person, "Hello", "!"); // Output: Hello, Alice!
    ```

    **Using `apply`:**

    ```javascript
    function greet(greeting, punctuation) {
      console.log(greeting + ", " + this.name + punctuation);
    }

    const person = { name: "Bob" };

    greet.apply(person, ["Hi", "."]); // Output: Hi, Bob.
    ```

34. **What is the `try...catch` statement in JavaScript?**

    The `try...catch` statement allows you to handle exceptions by running code in the `try` block and catching errors in the `catch` block.

    ```javascript
    try {
        // code that may throw an error
    } catch (error) {
        // handle the error
    ```

35. **What is the `finally` block in JavaScript?**

    The `finally` block contains code that will run regardless of whether an error was thrown or not.

    ```javascript
    try {
      // code that may throw an error
    } catch (error) {
      // handle the error
    } finally {
      // code to run regardless of error
    }
    ```

36. **How do you throw an error in JavaScript?**

    - **Answer:**
      ```javascript
      throw new Error("Something went wrong");
      ```

37. **What is a custom error?**
    - **Answer:** A custom error is an error object that you create to provide specific error messages or codes for different error conditions.
      ```javascript
      class CustomError extends Error {
        constructor(message) {
          super(message);
          this.name = "CustomError";
        }
      }
      ```

### Miscellaneous

45. **What is `typeof` operator in JavaScript?**

    - **Answer:** The `typeof` operator returns a string indicating the type of the operand.
      ```javascript
      typeof 123; // "number"
      typeof "Hello"; // "string"
      ```

46. **What is `instanceof` operator in JavaScript?**

    - **Answer:** The `instanceof` operator tests whether the prototype property of a constructor appears anywhere in the prototype chain of an object.
      ```javascript
      obj instanceof MyClass;
      ```

47. **What is a callback function?**

    - **Answer:** A callback function is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.
      ```javascript
      function myFunction(callback) {
        // code to execute
        callback();
      }
      ```

48. **What is `NaN` in JavaScript?**

    - **Answer:** `NaN` stands for "Not-a-Number" and is a value representing an invalid number.
      ```javascript
      typeof NaN; // "number"
      ```

49. **What is `use strict`?**

    - **Answer:** `"use strict"` is a directive that enables strict mode, which makes error-checking more robust and prevents the use of certain JavaScript features that are considered problematic.
      ```javascript
      "use strict";
      ```

50. **What is the difference between `slice` and `splice`?**
    - **Answer:** `slice` returns a shallow copy of a portion of an array into a new array, while `splice` changes the contents of an array by removing or replacing existing elements and/or adding new elements.

### More Advanced Questions

51. **What is `JSON`?**

    - **Answer:** JSON (JavaScript Object Notation) is a lightweight data-interchange format that's easy for humans to read and write and easy for machines to parse and generate.
      ```javascript
      let jsonString = '{"name": "John", "age": 30}';
      let jsonObject = JSON.parse(jsonString);
      ```

52. **How do you convert a JavaScript object to a JSON string?**

    - **Answer:**
      ```javascript
      let jsonString = JSON.stringify({ name: "John", age: 30 });
      ```

53. **What is the `fetch` API?**

    - **Answer:** The `fetch` API is a modern interface for making network requests similar to XMLHttpRequest, but with a more powerful and flexible feature set.
      ```javascript
      fetch("https://api.example.com/data")
        .then((response) => response.json())
        .then((data) => console.log(data));
      ```

54. **What are modules in JavaScript?**

    - **Answer:** Modules are reusable pieces of code that can be imported and exported, allowing for better organization and separation of concerns.

      ```javascript
      // Exporting a module
      export const myFunction = () => {
        // code
      };

      // Importing a module
      import { myFunction } from "./myModule.js";
      ```

55. **What is the difference between `localStorage` and `sessionStorage`?**

    - **Answer:** `localStorage` stores data with no expiration date, while `sessionStorage` stores data for the duration of the page session (data is lost when the page is closed).

56. **What is a Symbol in JavaScript?**

    - **Answer:** A Symbol is a unique and immutable primitive value and may be used as the key of an object property.

57. **What is the `async`/`await` syntax?**

    - **Answer:** `async`/`await` is syntax for writing asynchronous code in a more readable and synchronous-looking manner.
      ```javascript
      async function fetchData() {
        let response = await fetch("https://api.example.com/data");
        let data = await response.json();
        console.log(data);
      }
      ```

58. **What is a generator function?**

    - **Answer:** A generator function is a special type of function that can pause execution and return multiple values using the `yield` keyword.
      ```javascript
      function* generatorFunction() {
        yield 1;
        yield 2;
        yield 3;
      }
      ```

59. **What is a Proxy in JavaScript?**

    - **Answer:** A Proxy object allows you to create a proxy for another object, which can intercept and redefine fundamental operations for that object.
      ```javascript
      let handler = {
        get: function (target, prop) {
          return prop in target ? target[prop] : 42;
        },
      };
      let proxy = new Proxy({}, handler);
      ```

60. **What is a `Set` in JavaScript?**
    - **Answer:** A `Set` is a collection of unique values, meaning a value in a `Set` can only occur once.
      ```javascript
      let mySet = new Set([1, 2, 3, 4, 4]);
      ```

### Event Loop and Concurrency

61. **What is the event loop in JavaScript?**

    - **Answer:** The event loop is a mechanism that handles asynchronous callbacks by placing them in a queue, and executing them in order once the main thread is free.

62. **What is a microtask in JavaScript?**

    - **Answer:** Microtasks are tasks that are executed after the currently executing script and before the next rendering. They include tasks such as `Promise` callbacks.

63. **What is the difference between synchronous and asynchronous code?**

    - **Answer:** Synchronous code is executed line by line, with each line blocking the execution until it's done. Asynchronous code allows other tasks to be performed while waiting for a process to complete.

64. **What is the purpose of `setTimeout`?**

    - **Answer:** `setTimeout` is used to execute a function after a specified number of milliseconds.
      ```javascript
      setTimeout(() => {
        console.log("Hello after 2 seconds");
      }, 2000);
      ```

65. **What is the purpose of `setInterval`?**
    - **Answer:** `setInterval` is used to repeatedly execute a function every specified number of milliseconds.
      ```javascript
      setInterval(() => {
        console.log("Hello every 2 seconds");
      }, 2000);
      ```

### Closures and Scope

66. **What is lexical scoping in JavaScript?**

    - **Answer:** Lexical scoping means that the accessibility of variables is determined by the physical placement of those variables within the nested function scopes.

67. **What is a module pattern in JavaScript?**

    - **Answer:** The module pattern is used to emulate private and public scope by creating a closure around a function that returns an object.
      ```javascript
      let module = (function () {
        let privateVar = "I am private";
        return {
          publicMethod: function () {
            console.log(privateVar);
          },
        };
      })();
      ```

68. **What is an IIFE (Immediately Invoked Function Expression)?**

    - **Answer:** An IIFE is a function that is executed immediately after it is defined.
      ```javascript
      (function () {
        console.log("IIFE executed");
      })();
      ```

69. **What is a higher-order function?**

    A higher-order function is a function that either takes one or more functions as arguments, returns a function, or both.

    ```javascript
    function greet(message) {
      return function (name) {
        return `${message}, ${name}!`;
      };
    }

    const sayHello = greet("Hello");
    console.log(sayHello("Alice")); // Hello, Alice!
    ```

70. **What is function currying?**

    Function currying is the process of transforming a function with multiple arguments into a series of functions that each take a single argument.

    ```javascript
    function curryAdd(a) {
      return function (b) {
        return function (c) {
          return a + b + c;
        };
      };
    }

    You can use the curried function like this:

    const add5 = curryAdd(5);       // Returns a function that takes `b` and `c`
    const add5And3 = add5(3);       // Returns a function that takes `c`
    const result = add5And3(10);

    Alternatively, you can also call the curried function in one line:
    const result = curryAdd(5)(3)(10); // Returns 18
    ```

71. **What is prototypal inheritance?**

    Prototypal inheritance is a feature in JavaScript where objects can inherit properties and methods from other objects.

    ```javascript
    const parent = {
      greet() {
        console.log("Hello from parent");
      },
    };

    const child = Object.create(parent);
    child.greet(); // Output: "Hello from parent"
    ```

72. **What is the difference between `Object.create` and `class inheritance`?**

    `Object.create()` offers a more direct, flexible, and prototype-oriented way to create objects with specific prototypes.

    `Class inheritance` provides a more structured, OOP-like approach to object creation and inheritance, using the class and extends syntax, making it more familiar and readable in many contexts.

73. **What are getter and setter methods?**

    Getter and setter methods are special methods that provide a way to get and set the values of object properties.

    ```javascript
    let obj = {
      _value: 0,
      get value() {
        return this._value;
      },
      set value(newValue) {
        this._value = newValue;
      },
    };
    ```

74. **What is the difference between `Object.keys` and `Object.values`?**

    `Object.keys` returns an array of the keys (property names) of an object.

    `Object.values` returns an array of the values corresponding to those keys in an object.

75. **What is the difference between `Object.freeze` and `Object.seal`?**

    `Object.freeze():`Completely freezes the object, making it fully immutable. You cannot add, delete, or modify properties or their attributes.

    `Object.seal():` Seals the object, allowing modification of existing properties but preventing the addition or deletion of properties. The object's structure is locked, but values of existing properties can still be changed.

76. **What is the `forEach` method in JavaScript?**

    The `forEach` executes the provided callback function once for each array element in order, starting from index 0 to the last index. The `forEach` method does not return a new array or any value; its purpose is purely to perform side effects (e.g., logging, modifying external variables) for each element.

    ```javascript
    const numbers = [1, 2, 3, 4, 5];

    numbers.forEach(function (number) {
      console.log(number);
    });
    ```

77. **What is the `find` method in JavaScript?**

    The `find` method is an array method that returns the first element in the array that satisfies a provided testing function. If no elements satisfy the testing function, `undefined` is returned. The `find` method stops executing once it finds an element that passes the test.

    ```javascript
    const users = [
      { id: 1, name: "Alice" },
      { id: 2, name: "Bob" },
      { id: 3, name: "Charlie" },
    ];

    const user = users.find((user) => user.id === 2);

    console.log(user); // Output: { id: 2, name: 'Bob' }
    ```

78. **What is the `findIndex` method in JavaScript?**

    The `findIndex` method is an array method that returns the index of the first element in the array that satisfies a provided testing function. If no elements satisfy the testing function, it returns -1. This method is similar to the `find` method, but instead of returning the element itself, it returns its index.

    ```javascript
    const numbers = [5, 8, 12, 3, 15, 7];
    const index = numbers.findIndex((element) => element > 10);
    console.log(index); // Output: 2 (index of the first element greater than 10, which is 12)
    ```

79. **What is the `some` method in JavaScript?**

    The `some` method tests whether at least one element in the array passes passes a given test (provided as a callback function). It returns `true` if the callback function returns `true` for at least one element in the array, otherwise it returns `false`.

    ```javascript
    const numbers = [1, 2, 3, 4, 5];

    // Check if any number is greater than 3
    const hasNumberGreaterThanThree = numbers.some((num) => num > 3);
    console.log(hasNumberGreaterThanThree); // Output: true

    // Check if any number is negative
    const hasNegativeNumber = numbers.some((num) => num < 0);
    console.log(hasNegativeNumber); // Output: false
    ```

80. **What is the `every` method in JavaScript?**

    The `every` method is an array method that tests whether all elements in the array pass a specified test (provided as a callback function). It returns a Boolean value - `true` if the callback function returns `true` for every array element; otherwise, it returns `false`.

    ```javascript
    const numbers = [2, 4, 6, 8, 10];

    const allEven = numbers.every((num) => num % 2 === 0);
    console.log(allEven); // Output: true

    const allGreaterThanFive = numbers.every((num) => num > 5);
    console.log(allGreaterThanFive); // Output: false
    ```

81. **How do you create a regular expression in JavaScript?**

    In JavaScript, you can create a regular expression using two methods:

    1. Using literal notation:

       ```javascript
       let regex = /pattern/;
       let regexWithFlags = /pattern/gi;
       ```

    2. Using the RegExp constructor:
       ```javascript
       let regex = new RegExp("pattern");
       let regexWithFlags = new RegExp("pattern", "gi");
       ```

    The literal notation is more concise and generally preferred when the pattern is known at compile time. The RegExp constructor is useful when you need to create a regex dynamically at runtime.

82. **What are regular expression flags? How do you test a string against a regular expression?**

    Regular expression flags are optional parameters that modify the behavior of a regular expression. They are appended to the end of a regex literal or passed as a second argument to the RegExp constructor. Common flags include:

    - `g` (global): Matches all occurrences of the pattern in a string, not just the first one.
    - `i` (case-insensitive): Makes the regex match case-insensitive.
    - `m` (multiline): Changes the behavior of `^` and `$` to match the start/end of each line instead of the whole string.
    - `s` (dotAll): Allows `.` to match newline characters.
    - `u` (unicode): Treats the pattern as a Unicode sequence.
    - `y` (sticky): Matches only from the index indicated by the `lastIndex` property.

    Example usage:

    ```javascript
    // Using 'g' and 'i' flags
    let regex = /pattern/gi;
    console.log("PATTERN".match(regex)); // Output: ["PATTERN"]
    console.log("pattern pattern".match(regex)); // Output: ["pattern", "pattern"]

    // Using 'g', 'i', and 'm' flags
    let regexObj = new RegExp("pattern", "gim");
    let multilineText = `PATTERN
    pattern
    PaTtErN`;
    console.log(multilineText.match(regexObj)); // Output: ["PATTERN", "pattern", "PaTtErN"]

    // Using 's' flag (dotAll)
    let dotAllRegex = /pattern.all/s;
    console.log("pattern\nall".match(dotAllRegex)); // Output: ["pattern\nall"]

    // Using 'y' flag (sticky)
    let stickyRegex = /\d+/y;
    let text = "123abc456";
    stickyRegex.lastIndex = 3;
    console.log(stickyRegex.exec(text)); // Output: ["456"]

    // Using 'u' flag (unicode)
    let unicodeRegex = /\u{1F600}/u;
    console.log(unicodeRegex.test("😀")); // Output: true
    ```

83. **How do you replace parts of a string using a regular expression?**

    You can use the `replace()` method with a regular expression to replace parts of a string. Here are a few examples:

    1. Basic replacement:

       ```javascript
       let newString = "hello world".replace(/world/, "JavaScript");
       console.log(newString); // Output: "hello JavaScript"
       ```

    2. Global replacement (replace all occurrences):

       ```javascript
       let newString = "hello hello hello".replace(/hello/g, "hi");
       console.log(newString); // Output: "hi hi hi"
       ```

    3. Case-insensitive replacement:

       ```javascript
       let newString = "Hello World".replace(/world/i, "JavaScript");
       console.log(newString); // Output: "Hello JavaScript"
       ```

    4. Using capture groups:

       ```javascript
       let newString = "John Doe".replace(/(\w+) (\w+)/, "$2, $1");
       console.log(newString); // Output: "Doe, John"
       ```

    5. Using a function for dynamic replacement:
       ```javascript
       let newString = "apple banana cherry".replace(
         /\b\w+\b/g,
         function (match) {
           return match.charAt(0).toUpperCase() + match.slice(1);
         }
       );
       console.log(newString); // Output: "Apple Banana Cherry"
       ```

### Best Practices

86. **What are some best practices for writing JavaScript code?**

- **Answer:** Use `let` and `const` instead of `var`, write descriptive variable names, keep functions small and focused, use comments judiciously, and follow consistent coding conventions.

87. **Why should you avoid using global variables?**

- **Answer:** Global variables can be accessed from anywhere in the code, which can lead to unexpected behaviors and make the code harder to maintain and debug.

88. **What is the importance of code readability?**

- **Answer:** Code readability makes it easier for others (and yourself) to understand, maintain, and debug the code.

89. **What is a polyfill?**

- **Answer:** A polyfill is a piece of code used to provide modern functionality on older browsers that do not natively support it.

90. **Why should you avoid modifying built-in objects?**

- **Answer:** Modifying built-in objects can lead to unpredictable results and compatibility issues, as it changes the expected behavior for all code that uses those objects.

### Tools and Environment

91. **What are JavaScript frameworks and libraries?**

- **Answer:** Frameworks and libraries are pre-written JavaScript code that help developers build applications more efficiently. Popular ones include React, Angular, and Vue.js.

92. **What is npm?**

- **Answer:** npm (Node Package Manager) is a package manager for JavaScript that helps manage dependencies and allows you to share code with other developers.

93. **What is a transpiler?**

- **Answer:** A transpiler is a tool that converts source code written in one language to another language, such as Babel, which converts ES6+ JavaScript to ES5 for browser compatibility.

94. **What is a linter?**

- **Answer:** A linter is a tool that analyzes your code for potential errors and coding standard violations. Examples include ESLint and JSHint.

95. **What is Webpack?**

- **Answer:** Webpack is a module bundler for JavaScript applications, which compiles multiple modules into a single file or a few files.

### Testing

96. **What is unit testing?**

- **Answer:** Unit testing is a software testing method where individual units of code are tested in isolation from the rest of the application.

97. **What are some JavaScript testing frameworks?**

- **Answer:** Popular JavaScript testing frameworks include Jest, Mocha, and Jasmine.

98. **What is Test-Driven Development (TDD)?**

- **Answer:** TDD is a development process where tests are written before the code itself, ensuring that the code is always tested and meets the required functionality.

99. **What is continuous integration (CI)?**

- **Answer:** CI is a development practice where code changes are automatically tested and integrated into a shared repository multiple times a day.

100.  **What is a mock object in testing?**

- **Answer:** A mock object simulates the behavior of real objects in controlled ways to test parts of the application without relying on real data or external systems.

These questions cover a wide range of fundamental JavaScript concepts and should help prepare you for basic JavaScript interviews.

```

```
