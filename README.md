# Here are 100 basic JavaScript interview questions along with their answers

1. **What is JavaScript?**<br>

   JavaScript is a high-level, interpreted programming language used to create interactive effects within web browsers.

2. **What are the data types in JavaScript?**<br>

   The main data types in JavaScript are: `Number`, `Bigint`, `String`, `Boolean`, `Object`, `Undefined`, `Null`, and `Symbol`

3. **What is a variable in JavaScript?**

   A variable is a container for storing data values. Variables are declared using the `var`, `let`, or `const` keywords.

4. **What is the difference between `var`, `let`, and `const`?**

   - `var`: Declares a variable that is function-scoped or globally-scoped, can be re-assigned, and is hoisted.
   - `let`: Declares a block-scoped variable that can be re-assigned and is not hoisted.
   - `const`: Declares a block-scoped variable that cannot be re-assigned after its initial assignment.

5. **What is `undefined` in JavaScript?**

   `undefined` is a variable that has been declared but has not yet been assigned a value.

6. **What is `null` in JavaScript?**

   `null` is an assignment value that represents no value or no object.

7. **What is the difference between `null` and `undefined`?**

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

8. **What is a function in JavaScript? How do you define a function in JavaScript?**

   A function is a block of code designed to perform a particular task, and it is executed when something invokes it.

   ```javascript
   function myFunction() {
     // code to be executed
   }
   ```

9. **What is a function expression?**

   A function expression is a function defined inside an expression instead of a declaration.

   ```javascript
   let myFunction = function () {
     // code to be executed
   };
   ```

10. **What are arrow functions?**

    Arrow functions are a concise syntax for writing function expressions using the `=>` syntax.

    ```javascript
    const myFunction = () => {
      // code to be executed
    };
    ```

11. **What is the difference between function declarations and function expressions?**

    - **Answer:** Function declarations are hoisted and can be called before they are defined, while function expressions are not hoisted.
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

12. **What is a JavaScript object? How do you create an object in JavaScript?**

    A JavaScript object is a collection of key-value pairs where the keys are strings (or Symbols) and the values can be of any data type. Objects are used to store and organize data and functions.

    **Object Example:**

    ```javascript
    const person = {
      name: "Alice",
      age: 30,
      greet: function () {
        console.log("Hello!");
      },
    };
    ```

    **Object Creation:**

    ```javascript
    let obj = {
      property1: "value1",
      property2: "value2",
    };
    ```

13. **How do you create an array in JavaScript?**

    - **Answer:**
      ```javascript
      let arr = [1, 2, 3, 4, 5];
      ```

14. **How do you access object properties?**

    - **Answer:**
      ```javascript
      obj.property1;
      obj["property2"];
      ```

15. **How do you access array elements?**

    - **Answer:**
      ```javascript
      arr[0]; // accesses the first element
      ```

16. **What is the `this` keyword in JavaScript?**
    - **Answer:** `this` refers to the object from which it was called. Its value depends on the context in which the function is called.

### DOM Manipulation

16. **What is the DOM?**

    - **Answer:** The DOM (Document Object Model) is a programming interface for HTML and XML documents, representing the page so that programs can change the document structure, style, and content.

17. **How do you select an element by ID?**

    - **Answer:**
      ```javascript
      document.getElementById("myElement");
      ```

18. **How do you select elements by class name?**

    - **Answer:**
      ```javascript
      document.getElementsByClassName("myClass");
      ```

19. **How do you select elements by tag name?**

    - **Answer:**
      ```javascript
      document.getElementsByTagName("div");
      ```

20. **How do you use querySelector to select an element?**
    - **Answer:**
      ```javascript
      document.querySelector(".myClass");
      ```

### Event Handling

21. **What is an event in JavaScript?**

    - **Answer:** An event is an action or occurrence detected by JavaScript (e.g., clicks, form submissions).

22. **How do you add an event listener in JavaScript?**

    - **Answer:**
      ```javascript
      element.addEventListener("click", function () {
        // code to execute
      });
      ```

23. **What are some common JavaScript events?**

    - **Answer:** Common events include `click`, `mouseover`, `mouseout`, `keydown`, `keyup`, `load`, and `submit`.

24. **What is event bubbling?**

    - **Answer:** Event bubbling is the process by which an event starts at the target element and then bubbles up to its parent elements.

25. **What is event capturing?**
    - **Answer:** Event capturing is the opposite of event bubbling, where the event starts from the root and propagates down to the target element.

### Promises and Asynchronous Programming

26. **What is a Promise in JavaScript?**

    - **Answer:** A Promise is an object representing the eventual completion or failure of an asynchronous operation.

27. **How do you create a Promise?**

    - **Answer:**
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

28. **What are the states of a Promise?**

    - **Answer:** Pending, Fulfilled, and Rejected.

29. **How do you handle a fulfilled Promise?**

    - **Answer:**
      ```javascript
      myPromise.then((result) => {
        // handle the result
      });
      ```

30. **How do you handle a rejected Promise?**
    - **Answer:**
      ```javascript
      myPromise.catch((error) => {
        // handle the error
      });
      ```

### ES6 Features

31. **What is the difference between `==` and `===`?**

    - **Answer:** `==` checks for equality with type conversion, while `===` checks for strict equality without type conversion.

32. **What are template literals?**

    - **Answer:** Template literals are string literals allowing embedded expressions, enclosed by backticks (`` ` ``).
      ```javascript
      let name = `John`;
      let message = `Hello, ${name}!`;
      ```

33. **What are default parameters in JavaScript functions?**

    - **Answer:** Default parameters allow named parameters to be initialized with default values if no value or `undefined` is passed.
      ```javascript
      function myFunction(x = 10) {
        // x is 10 if not provided
      }
      ```

34. **What is destructuring assignment?**

    - **Answer:** Destructuring assignment is a syntax that allows extracting values from arrays or objects into distinct variables.
      ```javascript
      let [a, b] = [1, 2];
      let { x, y } = { x: 10, y: 20 };
      ```

35. **What are rest parameters?**
    - **Answer:** Rest parameters allow a function to accept an indefinite number of arguments as an array.
      ```javascript
      function myFunction(...args) {
        // args is an array of all arguments
      }
      ```

### Advanced Topics

36. **What is the `map` method in JavaScript?**

    - **Answer:** The `map` method creates a new array populated with the results of calling a provided function on every element in the calling array.
      ```javascript
      let newArr = arr.map((element) => element * 2);
      ```

37. **What is the `filter` method in JavaScript?**

    - **Answer:** The `filter` method creates a new array with all elements that pass the test implemented by the provided function.
      ```javascript
      let filteredArr = arr.filter((element) => element > 2);
      ```

38. **What is the `reduce` method in JavaScript?**

    - **Answer:** The `reduce` method executes a reducer function on each element of the array, resulting in a single output value.
      ```javascript
      let sum = arr.reduce((total, element) => total + element, 0);
      ```

39. **What is a closure in JavaScript?**

    - **Answer:** A closure is a function that retains access to its outer scope variables even after the outer function has finished executing.
      ```javascript
      function outerFunction() {
        let outerVariable = "I'm outside!";
        function innerFunction() {
          console.log(outerVariable);
        }
        return innerFunction;
      }
      ```

40. **What is the difference between `call` and `apply`?**
    - **Answer:** Both `call` and `apply` are used to invoke functions with a specified `this` value, but `call` takes arguments separately, while `apply` takes arguments as an array.

### Error Handling

41. **What is the `try...catch` statement in JavaScript?**
    - **Answer:** The `try...catch` statement allows you to handle exceptions by running code in the `try` block and catching errors in the `catch` block.
      ```javascript
      try {
          // code that may throw an error
      } catch (error) {
          // handle the error
      ```

## ASSISTANT

      }
      ```

42. **What is the `finally` block in JavaScript?**

    - **Answer:** The `finally` block contains code that will run regardless of whether an error was thrown or not.
      ```javascript
      try {
        // code that may throw an error
      } catch (error) {
        // handle the error
      } finally {
        // code to run regardless of error
      }
      ```

43. **How do you throw an error in JavaScript?**

    - **Answer:**
      ```javascript
      throw new Error("Something went wrong");
      ```

44. **What is a custom error?**
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

    - **Answer:** A higher-order function is a function that can take other functions as arguments and/or return a function as its result.
      ```javascript
      function higherOrderFunction(callback) {
        callback();
      }
      ```

70. **What is function currying?**
    - **Answer:** Function currying is the process of transforming a function with multiple arguments into a series of functions that each take a single argument.
      ```javascript
      function curryFunction(a) {
        return function (b) {
          return a + b;
        };
      }
      ```

### More on Objects

71. **What is prototypal inheritance?**

    - **Answer:** Prototypal inheritance is a feature in JavaScript where objects can inherit properties and methods from other objects.
      ```javascript
      let parentObj = {
        greet: function () {
          console.log("Hello");
        },
      };
      let childObj = Object.create(parentObj);
      ```

72. **What is the difference between `Object.create` and class inheritance?**

    - **Answer:** `Object.create` sets up prototype inheritance directly, while class inheritance uses the `class` syntax to create a blueprint for objects and their inheritance.

73. **What are getter and setter methods?**
    - **Answer:** Getter and setter methods

## ASSISTANT

are special methods that provide a way to get and set the values of object properties.
`javascript
      let obj = {
          _value: 0,
          get value() {
              return this._value;
          },
          set value(newValue) {
              this._value = newValue;
          }
      };
      `

74. **What is the difference between `Object.keys` and `Object.values`?**

    - **Answer:** `Object.keys` returns an array of a given object's own enumerable property names, while `Object.values` returns an array of the object's own enumerable property values.

75. **What is the difference between `Object.freeze` and `Object.seal`?**
    - **Answer:** `Object.freeze` makes an object immutable, while `Object.seal` allows modification of existing properties but prevents adding or removing properties.

### Arrays and Iteration

76. **What is the `forEach` method in JavaScript?**

    - **Answer:** The `forEach` method executes a provided function once for each array element.
      ```javascript
      arr.forEach((element) => {
        console.log(element);
      });
      ```

77. **What is the `find` method in JavaScript?**

    - **Answer:** The `find` method returns the value of the first element in the array that satisfies the provided testing function.
      ```javascript
      let found = arr.find((element) => element > 10);
      ```

78. **What is the `findIndex` method in JavaScript?**

    - **Answer:** The `findIndex` method returns the index of the first element in the array that satisfies the provided testing function.
      ```javascript
      let index = arr.findIndex((element) => element > 10);
      ```

79. **What is the `some` method in JavaScript?**

    - **Answer:** The `some` method tests whether at least one element in the array passes the provided function.
      ```javascript
      let hasPositiveNumbers = arr.some((element) => element > 0);
      ```

80. **What is the `every` method in JavaScript?**
    - **Answer:** The `every` method tests whether all elements in the array pass the provided function.
      ```javascript
      let allPositiveNumbers = arr.every((element) => element > 0);
      ```

### Strings and Regular Expressions

81. **What is a template literal?**

    - **Answer:** Template literals allow for embedded expressions and multi-line strings using backticks (`` ` ``).
      ```javascript
      let name = "John";
      let message = `Hello, ${name}!`;
      ```

82. **How do you create a regular expression in JavaScript?**

    - **Answer:**
      ```javascript
      let regex = /pattern/;
      let regexWithFlags = /pattern/g;
      ```

83. **What are regular expression flags?**

    - **Answer:** Flags are used to modify the behavior of a regular expression. Common flags include `g` (global), `i` (case-insensitive), and `m` (multiline).

84. **How do you test a string against a regular expression?**

    - **Answer:**
      ```javascript
      let regex = /pattern/;
      regex.test("string to test"); // returns true or false
      ```

85. **How do you replace parts of a string using a regular expression?**
    - **Answer:**
      ```javascript
      let newString = "hello world".replace(/world/, "JavaScript");
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
