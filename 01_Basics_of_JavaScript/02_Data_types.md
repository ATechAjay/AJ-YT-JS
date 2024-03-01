# Data types in JavaScript?

In JavaScript, data types represent the kind of data that can be used and manipulated in your code. There are two main categories of data types in JavaScript:

- Primitive type
- Object type

### Primitive Types:

Primitive types are immutable data types that directly contain a value. They are passed by value when assigned to a variable. There are seven primitive data types in JavaScript:

1. Number: Represents numeric values. It includes integers, floats, and NaN (Not-a-Number).
2. String: Represents sequences of characters enclosed within single ('') or double ("") quotes.
3. Boolean: Represents a logical value indicating true or false.
4. Undefined: Represents a variable that has been declared but not assigned a value.
5. Null: Represents an intentional absence of any object value.
6. Symbol: Introduced in ECMAScript 2015 (ES6), symbols are unique and immutable primitive values often used as object property keys.
7. BigInt: Introduced in ECMASript 2020 (ES11), It is a primitive data type used to represent integers of arbitrary precision.

> Please, note that BigInt values cannot be mixed with Number values in arithmetic operations without explicit conversion.

### Object Types:

Object types are complex data types that aggregate multiple values and functions, often referred to as properties and methods. Objects are mutable and are stored by reference rather than by value.

### Dynamic Typing:

JavaScript is dynamically typed, meaning that variables are not bound to a particular data type. A variable can hold different types of values at different times during the execution of a program. This provides flexibility but also requires careful handling of types to prevent unexpected behavior.

### Variable has types or values?

In JavaScript, `variables don't have types; rather, values have types`. Variables can hold any type of value, and the type of the value they hold can change over time. This is why JavaScript is often described as having dynamic typing.

> JavaScript is a dynamic typing language.

Here's a quick example to illustrate the dynamic typing in JavaScript:

```javascript
let x; // Variable declaration without initialization, it's type is undefined
console.log(typeof x); // Output: "undefined"

x = 5; // Assigning a numeric value to variable x
console.log(typeof x); // Output: "number"

x = "Hello"; // Assigning a string value to the same variable x
console.log(typeof x); // Output: "string"
```

In the example above:

- The variable `x` initially holds an `undefined` value.
- It then holds a `numeric` value (`5`).
- Later it holds a `string` value (`'Hello'`).

The variable `x` itself doesn't have a fixed type; rather, its value changes dynamically as different types of values are assigned to it.
