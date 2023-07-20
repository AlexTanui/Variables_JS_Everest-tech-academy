In JavaScript, variables are used to store data values that can be manipulated, accessed, and modified throughout the program's execution. Variables allow developers to give names to values and use those names to refer to the stored data. Here's a detailed explanation of variables in JavaScript:

1. **Variable Declaration:**
   To create a variable in JavaScript, you use the `var`, `let`, or `const` keyword, followed by the variable name. The `var` keyword was traditionally used, but starting from ECMAScript 6 (ES6), `let` and `const` were introduced to provide better scoping and immutability, respectively.

   ```javascript
   // Variable Declaration using var (older approach)
   var age = 30;

   // Variable Declaration using let (recommended for mutable variables)
   let name = "John";

   // Variable Declaration using const (recommended for immutable variables)
   const PI = 3.14;
   ```

2. **Variable Assignment:**
   After declaring a variable, you can assign a value to it using the assignment operator (`=`). The value can be a primitive data type (e.g., number, string, boolean) or a reference to complex data types (e.g., arrays, objects, functions).

   ```javascript
   let age = 30;          // Assigning a number to the variable 'age'
   let name = "John";     // Assigning a string to the variable 'name'
   const PI = 3.14;      // Assigning a number to the constant 'PI'

   let numbers = [1, 2, 3];   // Assigning an array to the variable 'numbers'
   let person = {            // Assigning an object to the variable 'person'
     firstName: "John",
     lastName: "Doe",
     age: 30,
   };
   ```

3. **Variable Naming Rules:**
   When naming variables in JavaScript, you need to follow certain rules:
   - Variable names must start with a letter (a-z, A-Z) or an underscore (_).
   - They can contain letters, numbers, and underscores.
   - Variable names are case-sensitive (e.g., `age`, `Age`, and `AGE` are different variables).
   - Avoid using reserved keywords (e.g., `function`, `let`, `const`, `if`, `else`, etc.) as variable names.

4. **Variable Scopes:**
   Variables in JavaScript have different scopes, which determine where the variable can be accessed. Variables declared with `var` have function scope, while variables declared with `let` and `const` have block scope (limited to the nearest curly braces `{}`). Block-scoped variables are accessible only within the block in which they are defined.

   ```javascript
   function exampleScope() {
     var x = 10;        // 'x' is accessible within the function
     let y = 20;        // 'y' is accessible within the block
     const z = 30;      // 'z' is accessible within the block
   }

   console.log(x);      // Throws an error: 'x' is not defined
   console.log(y);      // Throws an error: 'y' is not defined
   console.log(z);      // Throws an error: 'z' is not defined
   ```

5. **Variable Hoisting:**
   Variables declared with `var` are hoisted to the top of their function scope, which means you can access them before they are declared. However, their value is not hoisted, so it will be `undefined` until the actual assignment is made.

   ```javascript
   console.log(x);   // Outputs 'undefined' (no error), due to hoisting
   var x = 5;
   ```

6. **Constant Variables (`const`):**
   When you declare a variable using `const`, its value cannot be reassigned after it has been assigned once. However, this does not mean the value is immutable. For complex data types like objects and arrays, you can still modify their properties or elements.

   ```javascript
   const PI = 3.14;
   PI = 3.14159;   // Throws an error: Assignment to constant variable

   const person = { name: "John" };
   person.name = "Alice";   // Allowed: Modifying the property of the object
   ```

Variables are fundamental in JavaScript, allowing developers to store and manipulate data throughout their programs. Understanding variable scoping, hoisting, and best practices for naming and usage is essential for writing clean and reliable JavaScript code.