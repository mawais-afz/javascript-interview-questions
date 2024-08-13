# JavaScript Interview Questions And Answers

1. **What is JavaScript? Where is it mostly used?**

   JavaScript is a high-level, interpreted programming language that is primarily used to create interactive and dynamic content on websites. It allows developers to implement complex features on web pages, such as animated graphics, clickable buttons, and real-time updates.

2. **What are client side and server side?**

   - **Client Side**: Refers to operations that are performed on the user's device (the client), typically within a web browser. This includes rendering the user interface, handling user interactions, and making requests to the server. Technologies commonly used for client-side development include HTML, CSS, JavaScript, ReactJS and Angular.

   - **Server Side**: Refers to operations that are performed on the server, which is a remote machine that hosts the application and its data. The server processes requests from the client, performs necessary computations, accesses databases, and sends back the appropriate responses. Server-side technologies include Node.js, Python, Java, Ruby, PHP, and databases like MySQL and MongoDB.

3. **What are variables? What is the difference between `var`, `let`, and `const?`**

   A variable is a container for storing data values. Variables are declared using the `var`, `let`, or `const` keywords.

   | Aspect         | `var`                                             | `let`                                            | `const`                                          |
   | -------------- | ------------------------------------------------- | ------------------------------------------------ | ------------------------------------------------ |
   | Scope          | Function or global scope                          | Block scope                                      | Block scope                                      |
   | Hoisting       | Hoisted and initialized with `undefined`          | Hoisted but not initialized (Temporal Dead Zone) | Hoisted but not initialized (Temporal Dead Zone) |
   | Re-declaration | Allowed in same scope                             | Not allowed in same block                        | Not allowed in same block                        |
   | Re-assignment  | Allowed                                           | Allowed                                          | Not allowed                                      |
   | Initialization | Optional                                          | Optional                                         | Required at declaration                          |
   | Usage          | Older JavaScript, can lead to unexpected behavior | Modern JavaScript, better scoping control        | Constants and immutable references               |
   | Example        | `var x = 1; var x = 2; // Allowed`                | `let y = 1; let y = 2; // SyntaxError`           | `const z = 1; z = 2; // TypeError`               |

4. **What are some important string operations in JS?**

   Some important string operations in JavaScript include:

   - **Length**: The `length` property returns the number of characters in a string.

     ```javascript
     let str = "Hello, World!";
     console.log(str.length); // Output: 13
     ```

   - **Substring**: The `substring()` method extracts characters from a string between two specified indices.

     ```javascript
     let str = "Hello, World!";
     console.log(str.substring(0, 5)); // Output: Hello
     ```

   - **IndexOf**: The `indexOf()` method returns the index of the first occurrence of a specified value in a string, or -1 if not found.

     ```javascript
     let str = "Hello, World!";
     console.log(str.indexOf("World")); // Output: 7
     ```

   - **Slice**: The `slice()` method returns a portion of a string based on specified start and end indices.

     ```javascript
     let str = "Hello, World!";
     console.log(str.slice(7, 12)); // Output: World
     ```

   - **Replace**: The `replace()` method replaces a specified value with another value in a string.

     ```javascript
     let str = "Hello, World!";
     console.log(str.replace("World", "JavaScript")); // Output: Hello, JavaScript!
     ```

   - **ToUpperCase / ToLowerCase**: These methods convert a string to uppercase or lowercase, respectively.

     ```javascript
     let str = "Hello, World!";
     console.log(str.toUpperCase()); // Output: HELLO, WORLD!
     console.log(str.toLowerCase()); // Output: hello, world!
     ```

   - **Trim**: The `trim()` method removes whitespace from both ends of a string.

     ```javascript
     let str = "   Hello, World!   ";
     console.log(str.trim()); // Output: Hello, World!
     ```

   - **Split**: The `split()` method splits a string into an array of substrings based on a specified delimiter.
     ```javascript
     let str = "Hello, World!";
     console.log(str.split(", ")); // Output: ["Hello", "World!"]
     ```

5. **What is DOM?**
   The Document Object Model (DOM) is a programming interface for web documents. It represents the structure of a document as a tree of objects, allowing programs to manipulate the content, structure, and style of a document dynamically. The DOM provides a way for scripts to access and update the content, structure, and style of a document.

   **What is the difference between HTML and DOM?**

   | **Aspect**         | **HTML**                                                     | **DOM**                                                                                   |
   | ------------------ | ------------------------------------------------------------ | ----------------------------------------------------------------------------------------- |
   | **Definition**     | A markup language used to create the structure of web pages. | A programming interface that represents the structure of a document as a tree of objects. |
   | **Nature**         | Static; defines the content and structure of a web page.     | Dynamic; allows for manipulation of the document structure and content.                   |
   | **Representation** | Written in HTML tags (e.g., `<div>`, `<p>`, `<a>`).          | Represented as a tree of nodes (elements, attributes, text).                              |
   | **Interaction**    | Cannot be directly manipulated by scripts.                   | Can be manipulated using JavaScript or other programming languages.                       |
   | **Purpose**        | To define the layout and content of a web page.              | To provide a structured representation of the document for programming.                   |

6. **What are phases of DOM event handling?**

   | **Phase**           | **Description**                                                                               | **Event Triggering**                                                         |
   | ------------------- | --------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
   | **Capturing Phase** | The event starts from the outermost element and propagates inward towards the target element. | The event is captured by the outermost ancestor elements first.              |
   | **Target Phase**    | The event reaches the target element, where the actual event handling occurs.                 | The event is handled by the target element itself.                           |
   | **Bubbling Phase**  | The event bubbles up from the target element back up to the outer elements.                   | The event is processed by ancestor elements from the target element outward. |

7. **What is an execution context in JavaScript?**

   An execution context is an abstract concept that holds information about the environment within which the current code is being executed. It consists of the following components:

   - **Variable Object (VO)**: Contains function arguments, inner variable declarations, and function declarations.
   - **Scope Chain**: A chain of all the variable objects that are accessible to the current execution context, allowing for variable resolution.
   - **this Value**: Refers to the object that is currently executing the code, which can vary depending on how a function is called.

   There are three types of execution contexts:

   1. **Global Execution Context**: Created when the JavaScript engine starts executing the code. It is the default context and has a global object (e.g., `window` in browsers).
   2. **Function Execution Context**: Created whenever a function is invoked. Each function has its own execution context.
   3. **Eval Execution Context**: Created by the `eval()` function, which allows for executing code represented as a string.

   Understanding execution contexts is crucial for grasping how variable scope and the `this` keyword work in JavaScript.

8. **What are the data types in JavaScript?**

   The main data types in JavaScript are: `Number`, `Bigint`, `String`, `Boolean`, `Object`, `Undefined`, `Null`, and `Symbol`

9. **What are the differences between primitives and non-primitives?**

   | Feature           | Primitives                                                             | Non-Primitives                             |
   | ----------------- | ---------------------------------------------------------------------- | ------------------------------------------ |
   | Definition        | Basic data types that are immutable                                    | Complex data types that can be modified    |
   | Examples          | `Number`, `String`, `Boolean`, `Null`, `Undefined`, `Symbol`, `BigInt` | `Object`, `Array`, `Function`              |
   | Memory Allocation | Stored directly in the stack                                           | Stored as references in the heap           |
   | Mutability        | Immutable (cannot be changed)                                          | Mutable (can be changed)                   |
   | Comparison        | Compared by value                                                      | Compared by reference                      |
   | Performance       | Generally faster                                                       | Generally slower due to reference handling |
   | Type Checking     | Type is determined at compile time                                     | Type can change at runtime                 |

10. **What are operators? What are the types of operators in JS?**

    Operators are special symbols in JavaScript that perform operations on variables and values. They are used to manipulate data and variables, allowing for calculations, comparisons, and logical operations.

    ### Types of Operators in JavaScript

    1. **Arithmetic Operators**: Used to perform mathematical operations.

       - `+` (Addition)
       - `-` (Subtraction)
       - `*` (Multiplication)
       - `/` (Division)
       - `%` (Modulus)
       - `**` (Exponentiation)

    2. **Assignment Operators**: Used to assign values to variables.

       - `=` (Assignment)
       - `+=` (Addition assignment)
       - `-=` (Subtraction assignment)
       - `*=` (Multiplication assignment)
       - `/=` (Division assignment)
       - `%=` (Modulus assignment)

    3. **Comparison Operators**: Used to compare two values.

       - `==` (Equal to)
       - `===` (Strict equal to)
       - `!=` (Not equal to)
       - `!==` (Strict not equal to)
       - `>` (Greater than)
       - `<` (Less than)
       - `>=` (Greater than or equal to)
       - `<=` (Less than or equal to)

    4. **Logical Operators**: Used to combine multiple boolean expressions.

       - `&&` (Logical AND)
       - `||` (Logical OR)
       - `!` (Logical NOT)

    5. **Bitwise Operators**: Used to perform operations on binary representations of numbers.

       - `&` (Bitwise AND)
       - `|` (Bitwise OR)
       - `^` (Bitwise XOR)
       - `~` (Bitwise NOT)
       - `<<` (Left shift)
       - `>>` (Right shift)
       - `>>>` (Unsigned right shift)

    6. **Ternary Operator**: A shorthand for the `if-else` statement.

       - `condition ? expr1 : expr2`

    7. **Type Operators**: Used to check the type of a variable.
       - `typeof` (Returns the type of a variable)
       - `instanceof` (Checks if an object is an instance of a specific class)

11. **What are the types of condition statements in JS?**

    In JavaScript, condition statements are used to perform different actions based on different conditions. The main types of condition statements include:

    1. **if statement**: Executes a block of code if a specified condition is true.

       ```javascript
       if (condition) {
         // code to be executed if condition is true
       }
       ```

    2. **if...else statement**: Executes one block of code if the condition is true and another block of code if it is false.

       ```javascript
       if (condition) {
         // code to be executed if condition is true
       } else {
         // code to be executed if condition is false
       }
       ```

    3. **else if statement**: Specifies a new condition to test if the first condition is false.

       ```javascript
       if (condition1) {
         // code to be executed if condition1 is true
       } else if (condition2) {
         // code to be executed if condition2 is true
       } else {
         // code to be executed if both conditions are false
       }
       ```

    4. **switch statement**: Allows a variable to be tested for equality against a list of values, each with its own block of code.

       ```javascript
       switch (expression) {
         case value1:
           // code to be executed if expression === value1
           break;
         case value2:
           // code to be executed if expression === value2
           break;
         default:
         // code to be executed if expression doesn't match any case
       }
       ```

    5. **ternary operator**: A shorthand for the `if...else` statement.
       ```javascript
       condition ? expr1 : expr2;
       ```

12. **What is hoisting?**

    Hoisting is a JavaScript mechanism where variables and function declarations are moved to the top of their containing scope during the compile phase. This means that you can use variables and functions before they are declared in the code.

    #### How Hoisting Works

    1. **Variable Hoisting**:

       Variables declared with `var` are hoisted to the top of their function or global scope, but their initialization remains in place. This means that the variable is accessible before its declaration, but its value will be `undefined` until the line where it is initialized is executed.

       ```javascript
       console.log(myVar); // Output: undefined
       var myVar = 5;
       console.log(myVar); // Output: 5
       ```

       Variables declared with `let` and `const` are also hoisted, but they are not initialized. Accessing them before their declaration results in a `ReferenceError` due to the "temporal dead zone."

       ```javascript
       console.log(myLet); // ReferenceError: Cannot access 'myLet' before initialization
       let myLet = 10;
       ```

    2. **Function Hoisting**:

       Function declarations are fully hoisted, meaning you can call a function before it is defined in the code.

       ```javascript
       myFunction(); // Output: "Hello, World!"

       function myFunction() {
         console.log("Hello, World!");
       }
       ```

       Function expressions, however, are not hoisted in the same way. If you try to call a function expression before it is defined, you will get a `TypeError`.

       ```javascript
       myFunc(); // TypeError: myFunc is not a function
       var myFunc = function () {
         console.log("Hello, World!");
       };
       ```

13. **What is the difference between `null` and `undefined`, or `undeclared`?**

    These three terms represent different states of a variable in JavaScript, and understanding their differences is crucial for effective coding.

    | Aspect                   | `null`                                                     | `undefined`                                                | `Undeclared`                                                  |
    | ------------------------ | ---------------------------------------------------------- | ---------------------------------------------------------- | ------------------------------------------------------------- |
    | Type                     | `object`                                                   | `undefined`                                                | Not defined at all                                            |
    | Meaning                  | Intentional absence of any object value                    | Variable declared but not initialized                      | Variable that has not been declared in any scope              |
    | Assignment               | Explicitly assigned                                        | Default value for uninitialized variables                  | Cannot be assigned a value since it does not exist            |
    | Usage                    | Explicitly signify emptiness or reset a variable           | Indicates lack of initialization                           | Indicates a variable that is not yet defined                  |
    | In comparisons           | `null == undefined` is true, `null === undefined` is false | `undefined == null` is true, `undefined === null` is false | Cannot be compared as it does not exist                       |
    | In arithmetic operations | Converted to 0                                             | Converted to NaN                                           | ReferenceError if accessed                                    |
    | Function return          | Explicitly returned to indicate no object                  | Default return value if no return statement                | Cannot be returned as it does not exist                       |
    | typeof                   | Returns "object"                                           | Returns "undefined"                                        | ReferenceError if accessed                                    |
    | JSON serialization       | Serialized as "null"                                       | Omitted from JSON output                                   | Not applicable                                                |
    | Example                  | `let obj = null;`                                          | `let var;` or `let obj = undefined;`                       | `console.log(myVar); // ReferenceError: myVar is not defined` |

14. **What is a function in JavaScript? How do you define a function in JavaScript?**

    A function is a block of code designed to perform a particular task, and it is executed when something invokes it.

    ```javascript
    function myFunction() {
      // code to be executed
    }
    ```

15. **What is a function expression?**

    A function expression is a function defined inside an expression instead of a declaration.

    ```javascript
    let myFunction = function () {
      // code to be executed
    };
    ```

16. **What are arrow functions? Can we use arguments object in arrow function?**

    Arrow functions are a concise syntax for writing function expressions using the `=>` syntax. Unlike regular functions, arrow functions do not have their own `this`, and they cannot use the `arguments` object. Instead, you can use rest parameters to achieve similar functionality.

    ```javascript
    const myFunction = (...args) => {
      // code to be executed
      console.log(args); // Accessing arguments using rest parameters
    };
    ```

17. **What are the differences between pure and impure functions?**

    | Aspect         | Pure Functions                                                                                      | Impure Functions                                                                                                 |
    | -------------- | --------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
    | Definition     | Functions that always produce the same output for the same input and do not cause any side effects. | Functions that may produce different outputs for the same input or cause side effects.                           |
    | Side Effects   | No side effects; they do not modify any external state.                                             | May have side effects; they can modify external state or interact with the outside world (e.g., I/O operations). |
    | Predictability | Highly predictable; easier to test and debug.                                                       | Less predictable; harder to test and debug due to external dependencies.                                         |
    | Usage          | Ideal for functional programming and scenarios requiring reliability.                               | Common in scenarios where interaction with external systems is necessary.                                        |
    | Example        | `function add(a, b) { return a + b; }`                                                              | `function fetchData() { return fetch('api/data'); }`                                                             |

18. **What is the difference between function declarations and function expressions?**

    | Aspect             | Function Declarations                         | Function Expressions                                   |
    | ------------------ | --------------------------------------------- | ------------------------------------------------------ |
    | Syntax             | `function myFunction() { ... }`               | `const myFunction = function() { ... };`               |
    | Hoisting           | Hoisted; can be called before declaration     | Not hoisted; must be defined before use                |
    | Named/Anonymous    | Always named                                  | Can be named or anonymous                              |
    | Availability       | Available throughout their scope              | Available only after declaration                       |
    | Usage              | Global functions, widely used functions       | Local scopes, callbacks, assignments                   |
    | Example            | `function greet() { console.log("Hello!"); }` | `const greet = function() { console.log("Hello!"); };` |
    | Self-Invocation    | Not typically used for IIFE                   | Can be used for IIFE: `(function() { ... })();`        |
    | Flexibility        | Less flexible, always named                   | More flexible, can be anonymous or named               |
    | Binding            | Bound to function name in its scope           | Bound to variable or property it's assigned to         |
    | In Objects/Classes | Often used directly as methods                | Commonly used as methods, especially in ES6 classes    |

19. **What does the new keyword do?**

    The `new` keyword is used to create an instance of an object that is defined by a constructor function. When `new` is used, it performs the following actions:

    1. It creates a new empty object.
    2. It sets the prototype of the new object to the constructor function's prototype.
    3. It binds `this` to the new object within the constructor function.
    4. It returns the new object unless the constructor function explicitly returns a different object.

    **Example:**

    ```javascript
    function Person(name, age) {
      this.name = name;
      this.age = age;
    }

    const person1 = new Person("John", 30);
    console.log(person1.name); // Output: John
    console.log(person1.age); // Output: 30
    ```

20. **What is a JavaScript object? What are the possible ways to create objects in JavaScript?**

    A JavaScript object is a collection of key-value pairs where the keys are strings (or Symbols) and the values can be of any data type. Objects are used to store and organize data and functions.

    **Methods for Creating JavaScript Objects:**

    1. Using an Object Literal:

       ```javascript
       const person = {
         name: "John",
         age: 30,
         greet: function () {
           console.log("Hello!");
         },
       };
       ```

    2. Using the `new` Keyword with Object Constructor:

       ```javascript
       const person = new Object();
       person.name = "John";
       person.age = 30;
       person.greet = function () {
         console.log("Hello!");
       };
       ```

    3. Using a Constructor Function:

       ```javascript
       function Person(name, age) {
         this.name = name;
         this.age = age;
         this.greet = function () {
           console.log("Hello!");
         };
       }
       const person = new Person("John", 30);
       ```

    4. Using `Object.create()`:

       ```javascript
       const personProto = {
         greet: function () {
           console.log("Hello!");
         },
       };
       const person = Object.create(personProto);
       person.name = "John";
       person.age = 30;
       ```

    5. Using ES6 Class Syntax:
       ```javascript
       class Person {
         constructor(name, age) {
           this.name = name;
           this.age = age;
         }
         greet() {
           console.log("Hello!");
         }
       }
       const person = new Person("John", 30);
       ```

21. **What is the `this` keyword in JavaScript?**

    `this` refers to the object from which it was called. Its value depends on the context in which the function is called.

22. **What is the `this` keyword in traditional and arrow function?**

    | **Aspect**             | **Traditional Functions**                                                                          | **Arrow Functions**                                                                     |
    | ---------------------- | -------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
    | **Definition**         | Function expressions and declarations.                                                             | Functions defined with the arrow syntax (`() => {}`).                                   |
    | **Binding of `this`**  | Dynamically bound based on how the function is called.                                             | Lexically bound to the surrounding context where the arrow function is defined.         |
    | **Method Calls**       | `this` refers to the object that owns the method.                                                  | `this` inherits from the enclosing scope (usually the surrounding function or object).  |
    | **Function Calls**     | `this` is global object (`window` in browsers, `global` in Node.js) or `undefined` in strict mode. | `this` retains the value from the enclosing lexical context.                            |
    | **Constructor Calls**  | `this` refers to the newly created instance when used with `new`.                                  | Cannot be used as constructors. Will throw an error if used with `new`.                 |
    | **Event Handlers**     | `this` typically refers to the element that triggered the event.                                   | `this` refers to the context where the arrow function is defined, not the event target. |
    | **Explicit Binding**   | Can use `.call()`, `.apply()`, or `.bind()` to explicitly set `this`.                              | Cannot be bound to a different `this` value; ignores attempts to change `this`.         |
    | **Usage in Objects**   | Commonly used for object methods when `this` should refer to the object.                           | Useful for callbacks and functions that don't need their own `this` context.            |
    | **`arguments` Object** | Has access to the `arguments` object.                                                              | Does not have its own `arguments` object; inherits from the enclosing scope if needed.  |

There are several types of selectors in JavaScript:

21. **How do you select elements in JavaScript?**

    Selectors in JavaScript are methods used to select and manipulate HTML elements in the Document Object Model (DOM). They allow developers to access elements based on their attributes, such as ID, class, or tag name, and perform actions on them.

    1. **ID Selector**: Selects a single element with a specific ID.

       ```javascript
       const element = document.getElementById("myId");
       ```

    2. **Class Selector**: Selects all elements with a specific class name.

       ```javascript
       const elements = document.getElementsByClassName("myClass");
       ```

    3. **Tag Selector**: Selects all elements of a specific tag name.

       ```javascript
       const elements = document.getElementsByTagName("div");
       ```

    4. **Query Selector**: Selects the first element that matches a CSS selector.

       ```javascript
       const element = document.querySelector(".myClass");
       ```

    5. **Query Selector All**: Selects all elements that match a CSS selector.

       ```javascript
       const elements = document.querySelectorAll("div.myClass");
       ```

22. **What is difference between querySelector and querySelectorAll?**

    | Feature            | `querySelector`                                             | `querySelectorAll`                                                              |
    | ------------------ | ----------------------------------------------------------- | ------------------------------------------------------------------------------- |
    | **Definition**     | Selects the first element that matches a CSS selector.      | Selects all elements that match a CSS selector.                                 |
    | **Return Type**    | Single `Element` object (or `null` if no match).            | `NodeList` of elements (or an empty `NodeList` if no match).                    |
    | **Usage**          | `document.querySelector('selector')`                        | `document.querySelectorAll('selector')`                                         |
    | **Performance**    | Generally faster for single element queries.                | Can be slower if there are many elements because it returns a list.             |
    | **Example**        | `const firstItem = document.querySelector('.item');`        | `const allItems = document.querySelectorAll('.item');`                          |
    | **Modification**   | You can directly modify the single element returned.        | You need to iterate over the `NodeList` to modify multiple elements.            |
    | **Pseudo-Classes** | Supports pseudo-classes like `:first-child`, `:last-child`. | Supports pseudo-classes in a similar way, but applies to all matching elements. |

23. **What is an event in JavaScript? How do you add an event listener in JavaScript?**

    An event is an action or occurrence that can be detected and handled by JavaScript. Here are some common types of JavaScript events:

    - **User Actions**: `click`, `dblclick`, `keydown`, `keyup`, `mousemove`, `scroll`, etc.
    - **Browser Actions**: `load`, `unload`, `resize`, `focus`, `blur`, etc.
    - **Form Events**: `submit`, `change`, `input`, `reset`, etc.
    - **Media Events**: `play`, `pause`, `ended`, `volumechange`, etc.

    To add an event listener in JavaScript, you can use the `addEventListener` method. This method attaches an event handler to an element without overwriting existing event handlers. Here is an example:

    ```javascript
    element.addEventListener("click", function () {
      // code to execute when the event is triggered
    });
    ```

    You can also use an arrow function for the event handler:

    ```javascript
    element.addEventListener("click", () => {
      // code to execute when the event is triggered
    });
    ```

24. **What are custom events? How to create a custom event in JavaScript?**

    Custom events are user-defined events that can be created and dispatched in JavaScript to signal that something has happened. They allow developers to create their own events that can be listened to and handled just like built-in events.

    Here's how to create and dispatch a custom event:

    ```javascript
    // Create a custom event using the Event constructor
    const event1 = new Event("myEvent");

    // Add an event listener for the custom event
    document.addEventListener("myEvent", function (event) {
      console.log("Event triggered using Event constructor");
    });

    // Dispatch the custom event
    document.dispatchEvent(event1);

    // Create a custom event using the CustomEvent constructor
    const event2 = new CustomEvent("myCustomEvent", {
      detail: { key1: "value1", key2: "value2" }, // optional data to pass with the event
    });

    // Add an event listener for the custom event
    document.addEventListener("myCustomEvent", function (event) {
      console.log(
        "Custom event triggered using CustomEvent constructor:",
        event.detail
      );
    });

    // Dispatch the custom event
    document.dispatchEvent(event2);
    ```

25. **What is differance between event bubbling and event capturing?**

    | Feature             | Event Bubbling                                                   | Event Capturing                                                |
    | ------------------- | ---------------------------------------------------------------- | -------------------------------------------------------------- |
    | **Direction**       | Bottom-up: From target element to root                           | Top-down: From root to target element                          |
    | **Order**           | Inner elements first, then outer elements                        | Outer elements first, then inner elements                      |
    | **Default**         | Default behavior in most browsers                                | Must be explicitly enabled                                     |
    | **Usage**           | More commonly used                                               | Less commonly used                                             |
    | **Implementation**  | `addEventListener(event, handler, false)` or omit third argument | `addEventListener(event, handler, true)`                       |
    | **Browser Support** | Supported in all modern browsers                                 | Supported in most modern browsers, but less universally        |
    | **Performance**     | Generally faster, as it's the default                            | Can be slightly slower due to additional processing            |
    | **Use Case**        | Useful for event delegation patterns                             | Useful when you need to handle events before they reach target |

26. **What is a Promise in JavaScript? How do you create a Promise?**

    A Promise is an object representing the eventual completion or failure of an asynchronous operation.

    ```javascript
    // Creating a Promise
    const myPromise = new Promise((resolve, reject) => {
      // Asynchronous operation goes here
      const success = true; // This is just for demonstration
      const result = "Operation successful";
      const error = new Error("Operation failed");

      if (success) {
        resolve(result);
      } else {
        reject(error);
      }
    });

    // Using the Promise
    myPromise
      .then((result) => {
        console.log(result); // Logs: Operation successful
      })
      .catch((error) => {
        console.error(error); // Logs: Error: Operation failed
      });
    ```

27. **What are the states of a Promise?**

    | State     | Description                                                                               | Transition                                         | Handling Method |
    | --------- | ----------------------------------------------------------------------------------------- | -------------------------------------------------- | --------------- |
    | Pending   | Initial state. The asynchronous operation is not yet complete.                            | Can transition to either Fulfilled or Rejected     | N/A             |
    | Fulfilled | The operation completed successfully. The Promise has a resulting value.                  | Final state. Cannot transition to any other state. | .then()         |
    | Rejected  | The operation failed. The Promise has a reason for the failure (usually an error object). | Final state. Cannot transition to any other state. | .catch()        |
    | Settled   | A Promise is settled if it's either Fulfilled or Rejected, but not Pending.               | Represents both Fulfilled and Rejected states      | .finally()      |

28. **What is the difference between `==` and `===`?**

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

29. **What are template literals?**

    Template literals are a feature in JavaScript that allow for more flexible string creation and manipulation. They are enclosed by backticks (`` ` ``) instead of single or double quotes.

    Key features of template literals include:

    1. **String interpolation**: Embed expressions directly in the string using `${}`.
    2. **Multi-line strings**: Create strings that span multiple lines without concatenation.
    3. **Tagged templates**: Use a function to parse the template literal.

    Examples:

    ```javascript
    // String interpolation
    const name = "John";
    console.log(`Hello, ${name}!`); // Output: Hello, John!

    // Multi-line string
    const multiLine = `
      This is a
      multi-line
      string.
    `;

    // Expression evaluation
    console.log(`2 + 2 = ${2 + 2}`); // Output: 2 + 2 = 4

    // Tagged template
    function myTag(strings, ...values) {
      return strings.reduce(
        (result, str, i) => `${result}${str}${values[i] || ""}`,
        ""
      );
    }
    const taggedResult = myTag`Hello, ${"world"}!`;
    console.log(taggedResult); // Output: Hello, world!
    ```

30. **What are default parameters in JavaScript functions?**

    Default parameters in JavaScript functions allow you to specify default values for function parameters. These default values are used when an argument is not provided or is explicitly set to `undefined` when the function is called.

    Key points about default parameters:

    1. They provide a way to ensure that a parameter always has a value, even if not explicitly passed.
    2. They can be any valid expression, including function calls.
    3. They are evaluated at function call time, not at function definition time.

    Example:

    ```javascript
    function greet(name: string = "Guest", greeting: string = "Hello") {
      console.log(`${greeting}, ${name}!`);
    }

    greet(); // Output: Hello, Guest!
    greet("Alice"); // Output: Hello, Alice!
    greet("Bob", "Hi"); // Output: Hi, Bob!
    greet(undefined, "Hey"); // Output: Hey, Guest!
    ```

    In this example, both `name` and `greeting` have default values. If not provided, `name` defaults to "Guest" and `greeting` defaults to "Hello".

    Default parameters can also use more complex expressions:

    ```javascript
    function calculateTotal(
      price: number,
      taxRate: number = 0.1,
      discount: number = price * 0.05
    ) {
      return price + price * taxRate - discount;
    }

    console.log(calculateTotal(100)); // Uses default taxRate and calculated discount
    console.log(calculateTotal(100, 0.15)); // Uses provided taxRate and calculated discount
    console.log(calculateTotal(100, 0.15, 10)); // Uses all provided values
    ```

31. **What is destructuring assignment?**

    Destructuring assignment is a syntax that allows unpacking/extracting values from arrays or objects into distinct variables, making it easier to work with complex data structures.

    Example with arrays:

    ```javascript
    const numbers = [1, 2, 3];
    const [first, second] = numbers;
    console.log(first); // Output: 1
    console.log(second); // Output: 2
    ```

    Example with objects:

    ```javascript
    const point = { x: 10, y: 20 };
    const { x, y } = point;
    console.log(x); // Output: 10
    console.log(y); // Output: 20
    ```

32. **What are rest parameters?**

    Rest parameters allow a function to accept an indefinite number of arguments as an array. They are denoted by three dots (...) followed by a parameter name.

    Key points about rest parameters:

    1. They collect all remaining arguments into an array.
    2. They must be the last parameter in a function definition.
    3. There can only be one rest parameter in a function.
    4. They provide a cleaner alternative to using the `arguments` object.

    ```javascript
    function sum(...numbers: number[]): number {
      return numbers.reduce((total, num) => total + num, 0);
    }

    console.log(sum(1, 2, 3)); // Output: 6
    console.log(sum(4, 5, 6, 7)); // Output: 22
    ```

    Rest parameters can also be used with other parameters:

    ```javascript
    function greet(greeting: string, ...names: string[]): void {
      names.forEach((name) => console.log(`${greeting}, ${name}!`));
    }

    greet("Hello", "Alice", "Bob", "Charlie");
    // Output:
    // Hello, Alice!
    // Hello, Bob!
    // Hello, Charlie!
    ```

33. **What is the `map` method in JavaScript?**

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

34. **What is the `filter` method in JavaScript?**

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

35. **What is the `reduce` method in JavaScript?**

    The `reduce` method in JavaScript is used to apply a function against an accumulator and each element in an array (from left to right) to reduce it to a single value. It’s often used to perform operations like summing numbers, concatenating strings, or accumulating results based on array elements.

    ```javascript
    const numbers = [1, 2, 3, 4, 5];

    const sum = numbers.reduce((accumulator, currentValue) => {
      return accumulator + currentValue;
    }, 0);

    console.log(sum); // Output: 15
    ```

36. **What is a closure in JavaScript?**

    A closure is a function that retains access to its outer scope variables even after the outer function has finished executing. This allows for data encapsulation and private variables.

    ```javascript
    function createCounter() {
      let count = 0; // This variable is private to the closure

      return {
        increment: function () {
          count++;
          return count;
        },
        decrement: function () {
          count--;
          return count;
        },
        getCount: function () {
          return count;
        },
      };
    }

    const counter = createCounter();
    console.log(counter.increment()); // Output: 1
    console.log(counter.increment()); // Output: 2
    console.log(counter.getCount()); // Output: 2
    console.log(counter.decrement()); // Output: 1
    ```

37. **How many ways can a function be invoked?**

    A function in JavaScript can be invoked in several ways:

    1. **Function Invocation**: The simplest way to invoke a function is by calling it directly.

       ```javascript
       function sayHello() {
         console.log("Hello!");
       }
       sayHello(); // Output: Hello!
       ```

    2. **Method Invocation**: When a function is called as a method of an object, the `this` context refers to the object.

       ```javascript
       const obj = {
         greet() {
           console.log("Hello from object!");
         },
       };
       obj.greet(); // Output: Hello from object!
       ```

    3. **Constructor Invocation**: Functions can be invoked as constructors using the `new` keyword, which creates a new instance of an object.

       ```javascript
       function Person(name) {
         this.name = name;
       }
       const person1 = new Person("Alice");
       console.log(person1.name); // Output: Alice
       ```

    4. **Indirect Invocation**: Functions can be invoked using `call`, `apply`, or `bind` to set the `this` context explicitly.

       ```javascript
       function greet() {
         console.log(`Hello, ${this.name}!`);
       }
       const user = { name: "Bob" };
       greet.call(user); // Output: Hello, Bob!
       ```

    5. **Arrow Function Invocation**: Arrow functions can be invoked like regular functions, but they do not have their own `this` context.
       ```javascript
       const greet = () => {
         console.log("Hello from arrow function!");
       };
       greet(); // Output: Hello from arrow function!
       ```

    Each of these invocation methods has its own behavior and context for the `this` keyword.

38. **What is the difference between `call`, `apply`, and `bind`?**

    `call`, `apply`, and `bind` are methods used to manipulate the `this` context of a function in JavaScript. Here's how they differ:

    1. **`call`**: Invokes a function with a specified `this` value and arguments provided individually.
    2. **`apply`**: Similar to `call`, but accepts arguments as an array.
    3. **`bind`**: Returns a new function with a fixed `this` value, without immediately executing it.

    ### Examples

    **Using `call`:**

    ```javascript
    function greet(greeting, punctuation) {
      console.log(`${greeting}, ${this.name}${punctuation}`);
    }

    const person = { name: "Alice" };

    greet.call(person, "Hello", "!"); // Output: Hello, Alice!
    ```

    **Using `apply`:**

    ```javascript
    function greet(greeting, punctuation) {
      console.log(`${greeting}, ${this.name}${punctuation}`);
    }

    const person = { name: "Bob" };

    greet.apply(person, ["Hi", "."]); // Output: Hi, Bob.
    ```

    **Using `bind`:**

    ```javascript
    function greet(greeting, punctuation) {
      console.log(`${greeting}, ${this.name}${punctuation}`);
    }

    const person = { name: "Charlie" };

    const boundGreet = greet.bind(person);
    boundGreet("Hey", "!"); // Output: Hey, Charlie!

    // You can also partially apply arguments
    const greetCharlie = greet.bind(person, "Welcome");
    greetCharlie("!"); // Output: Welcome, Charlie!
    ```

    Key differences:

    - `call` and `apply` execute the function immediately, while `bind` returns a new function.
    - `call` takes arguments separately, `apply` takes them as an array.
    - `bind` allows for partial application of arguments.

39. **What is the `try...catch` statement in JavaScript?**

    The `try...catch` statement allows you to handle exceptions by running code in the `try` block and catching errors in the `catch` block.

    ```javascript
    try {
      // code that may throw an error
    } catch (error) {
      // handle the error
    }
    ```

40. **What is the `finally` block in JavaScript?**

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

41. **How do you throw an error in JavaScript?**

    To throw an error in JavaScript, you use the `throw` statement followed by an `Error` object or any other value. Here are a few examples:

    ```javascript
    // Throwing a basic Error object
    throw new Error("Something went wrong");

    // Throwing a custom error message
    throw "Invalid input";

    // Throwing a specific error type
    throw new TypeError("Expected a number");

    // Throwing an object with additional information
    throw {
      name: "CustomError",
      message: "An error occurred",
      code: 500,
    };
    ```

    It's generally recommended to throw `Error` objects or instances of `Error` subclasses, as they provide a stack trace and are more informative for debugging.

42. **What is a custom error?**

    A custom error is a user-defined error type that extends the built-in Error class or one of its subclasses. It allows developers to create specific error types for different scenarios in their application, providing more detailed and contextual error information.

    Key points about custom errors:

    1. They extend the built-in Error class or its subclasses.
    2. They can include additional properties or methods.
    3. They allow for more specific error handling.
    4. They help in creating a consistent error structure across an application.

    Here's an example of how to create and use a custom error:

    ```typescript
    class CustomError extends Error {
      constructor(public message: string, public errorCode: string) {
        super(message);
        this.name = "CustomError";
        // Set the prototype explicitly.
        Object.setPrototypeOf(this, CustomError.prototype);
      }
    }

    // Usage
    try {
      throw new CustomError("Something went wrong", "ERR001");
    } catch (error) {
      if (error instanceof CustomError) {
        console.log(
          `${error.name}: ${error.message} (Code: ${error.errorCode})`
        );
      } else {
        console.log("An unknown error occurred");
      }
    }
    ```

    Benefits of using custom errors:

    1. Improved error classification and handling
    2. Enhanced debugging capabilities
    3. Better error reporting and logging
    4. Increased code readability and maintainability

43. **What is `typeof` operator in JavaScript?**

    The `typeof` operator in JavaScript is a unary operator that returns a string indicating the type of the unevaluated operand. It's used to determine the type of a value or expression.

    Key points about `typeof`:

    1. It returns a string representing the operand's type.
    2. It can be used with variables, literals, or expressions.
    3. It's particularly useful for type checking in conditional statements.

    Examples:

    ```javascript
    typeof 42; // Returns "number"
    typeof "Hello"; // Returns "string"
    typeof true; // Returns "boolean"
    typeof undefined; // Returns "undefined"
    typeof null; // Returns "object" (this is a known quirk)
    typeof {}; // Returns "object"
    typeof []; // Returns "object"
    typeof function () {}; // Returns "function"
    ```

    Note: While `typeof` is generally reliable, it has some limitations:

    - It returns "object" for arrays and null, which can be misleading.
    - It can't distinguish between different types of objects.

    For more precise type checking, especially with objects, you might need to use other methods like `instanceof` or check for specific properties.

44. **What is `instanceof` operator in JavaScript?**

    The `instanceof` operator tests whether the prototype property of a constructor appears anywhere in the prototype chain of an object.

    Key points about `instanceof`:

    1. It checks the entire prototype chain, not just the immediate constructor.
    2. It's useful for type checking of custom objects.
    3. It can be unreliable with primitive types.

    Example:

    ```javascript
    class Animal {}
    class Dog extends Animal {}

    const myDog = new Dog();

    console.log(myDog instanceof Dog); // true
    console.log(myDog instanceof Animal); // true
    console.log(myDog instanceof Object); // true
    console.log(myDog instanceof Array); // false
    ```

45. **What is a callback function?**

    A callback function is a function passed as an argument to another function, which is then invoked inside that function, often after some operation has been completed. Callbacks are commonly used in asynchronous operations, event handling, and to implement higher-order functions.

    Key points about callback functions:

    1. They allow for asynchronous programming in JavaScript.
    2. They enable the execution of code after a specific task is completed.
    3. They are fundamental to many JavaScript patterns and libraries.

    Example:

    ```javascript
    function fetchData(callback) {
      // Simulating an asynchronous operation
      setTimeout(() => {
        const data = { id: 1, name: "John Doe" };
        callback(data);
      }, 1000);
    }

    function processData(data) {
      console.log("Processed:", data);
    }

    fetchData(processData);
    ```

46. **What is `NaN` in JavaScript?**

    `NaN` stands for "Not-a-Number" aand is a special value that indicates/representing an invalid or unrepresentable number.

    Key points about `NaN`:

    1. `NaN` is of type number, as shown below:

    ```javascript
    typeof NaN; // "number"
    ```

    2. `NaN` is not equal to itself, which can be checked using:

    ```javascript
    console.log(NaN === NaN); // false
    ```

    3. It is commonly produced by operations like dividing zero by zero or attempting to parse a non-numeric string.

    Example:

    ```javascript
    console.log(0 / 0); // NaN
    console.log(parseInt("abc")); // NaN
    ```

47. **What is `use strict`?**

    `"use strict"` is a directive that enables strict mode, which makes error-checking more robust and prevents the use of certain JavaScript features that are considered problematic.

    ```javascript
    "use strict";
    ```

48. **What is the difference between `slice` and `splice`?**

    `slice` creates a new array containing a portion of the original array without modifying it, while `splice` directly alters the original array by removing, replacing, or adding elements.

    **Example of `slice`:**

    ```javascript
    const fruits = ["Apple", "Banana", "Cherry", "Date"];
    const citrus = fruits.slice(1, 3); // ['Banana', 'Cherry']
    console.log(citrus); // Output: ['Banana', 'Cherry']
    ```

    **Example of `splice`:**

    ```javascript
    const vegetables = ["Carrot", "Potato", "Cucumber"];
    vegetables.splice(1, 1, "Tomato"); // Removes 'Potato' and adds 'Tomato'
    console.log(vegetables); // Output: ['Carrot', 'Tomato', 'Cucumber']
    ```

49. **What is `JSON`? How do you convert a JavaScript object to a JSON string?**

    JSON (JavaScript Object Notation) is a lightweight data-interchange format that's easy for humans to read and write and easy for machines to parse and generate.

    ```javascript
    let jsonString = '{"name": "John", "age": 30}';
    let jsonObject = JSON.parse(jsonString);
    ```

    ```javascript
    let jsonString = JSON.stringify({ name: "John", age: 30 });
    ```

50. **What is the `fetch` API?**

    The `fetch` API is a modern interface for making network requests similar to XMLHttpRequest, but with a more powerful and flexible feature set.

    ```javascript
    fetch("https://api.example.com/data")
      .then((response) => response.json())
      .then((data) => console.log(data));
    ```

51. **What are modules in JavaScript?**

    Modules are reusable pieces of code that can be imported and exported, allowing for better organization and separation of concerns.

    ```javascript
    // Exporting a module
    export const myFunction = () => {
      // code
    };

    // Importing a module
    import { myFunction } from "./myModule.js";
    ```

52. **What is the difference between `localStorage` and `sessionStorage`?**

| Feature       | `localStorage`                                                  | `sessionStorage`                                                        |
| ------------- | --------------------------------------------------------------- | ----------------------------------------------------------------------- |
| Lifetime      | Data persists even after the browser is closed                  | Data is cleared when the page session ends (browser/tab is closed)      |
| Scope         | Accessible across all tabs and windows of the same origin       | Accessible only within the same tab or window                           |
| Storage Limit | Typically around 5-10MB per origin                              | Typically around 5-10MB per origin                                      |
| Use Case      | Suitable for storing data that needs to persist across sessions | Suitable for temporary data that is only needed during a single session |

48. **What is a Symbol in JavaScript?**

    A Symbol is a unique and immutable primitive value and may be used as the key of an object property.

49. **What is the `async`/`await` syntax?**

    - **Answer:** `async`/`await` is syntax for writing asynchronous code in a more readable and synchronous-looking manner.
      ```javascript
      async function fetchData() {
        let response = await fetch("https://api.example.com/data");
        let data = await response.json();
        console.log(data);
      }
      ```

50. **What is a generator function?**

    - **Answer:** A generator function is a special type of function that can pause execution and return multiple values using the `yield` keyword.
      ```javascript
      function* generatorFunction() {
        yield 1;
        yield 2;
        yield 3;
      }
      ```

51. **What is a Proxy in JavaScript?**

    - **Answer:** A Proxy object allows you to create a proxy for another object, which can intercept and redefine fundamental operations for that object.
      ```javascript
      let handler = {
        get: function (target, prop) {
          return prop in target ? target[prop] : 42;
        },
      };
      let proxy = new Proxy({}, handler);
      ```

52. **What is a `Set` in JavaScript?**
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

69. **What is a higher-order function? What are the benefits higher order functions?**

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

    The main benefits of higher order functions are:

    - Abstration
    - Reusability
    - Immutability
    - Modularity

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

84. **What are some best practices for writing JavaScript code?**

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
