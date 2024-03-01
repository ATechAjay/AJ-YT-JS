In JavaScript, type conversion refers to the `process of converting a value from one data type to another`. There are` two main types of type conversion`:

1. Explicit type conversion
2. Implicit type conversion - Coercion

# 1. Explicit Type Conversion:

Explicit type conversion, also known as type casting, occurs when you manually convert a value from one data type to another using built-in functions or methods provided by JavaScript.

Examples of Explicit Type Conversion:

- String Conversion: Using `String()` function or `.toString()` method to convert values to strings.

  ```js
  let num = 123;
  let str = String(num); // Explicitly convert num to a string
  console.log(typeof str); // Output: "string"
  ```

- Number Conversion: Using `Number()` function, `parseInt()`, or `parseFloat()` functions to convert values to numbers.

  ```js
  let str = "123";
  let num = Number(str); // Explicitly convert str to a number
  console.log(typeof num); // Output: "number"
  ```

- Boolean Conversion: Using `Boolean()` function to convert values to booleans.

  ```js
  let value = "Hello";
  let boolValue = Boolean(value); // Explicitly convert value to a boolean
  console.log(boolValue); // Output: true
  ```

# 2. Implicit Type Conversion (Coercion):

Implicit type conversion, also known as `type coercion`, occurs automatically in JavaScript when values are compared or operated on in ways that require different data types.

Examples of Implicit Type Conversion:

- String Concatenation: When using the `+` operator with strings and other data types, JavaScript implicitly converts non-string values to strings and performs concatenation.

  ```js
  let num = 123;
  let str = "The number is " + num; // Implicitly convert num to a string
  console.log(str); // Output: "The number is 123"
  ```

- Arithmetic Operations: During arithmetic operations, JavaScript may implicitly convert operands to a common data type before performing the operation.

  ```js
  let num = "10";
  let result = num * 2; // Implicitly convert num to a number
  console.log(result); // Output: 20
  ```

- Comparison Operations: When using comparison operators like `==` or `===`, JavaScript may implicitly convert operands to the same data type before comparing.

  ```js
  let num = "10";
  console.log(num == 10); // Output: true (implicit conversion of num to number before comparison)
  ```

Understanding both explicit and implicit type conversion is important in JavaScript to handle data types effectively and prevent unexpected behavior in your code.
