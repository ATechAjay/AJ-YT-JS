In JavaScript, `let`, `var`, and `const` are keywords used for variable declaration, but they have different behaviors and scopes.

> let and const introduced in ES6 (2015).

# var keyword

`var` was the original way to declare variables in JavaScript prior to the introduction of `let` and `const`. Variables declared with `var` have `function-level scope` or `global scope` if declared outside of any function. They are also `hoisted` to the top of their scope during the compilation phase.

Example:

```javascript
function example() {
  console.log(x); // Outputs: undefined
  if (true) {
    var x = 10;
  }
  console.log(x); // Outputs: 10
}
example();
```

In this example, the variable `x` is accessible outside of the `if` block due to `hoisting`.

> In this example, even though `var x = 10;` appears later in the if statement, `var x` is hoisted to the top of the function scope during the compilation phase. So, `console.log(x)` doesn't throw an error, but it prints `undefined` because the variable `x` exists but has not been assigned a value at that point.

# let keyword

`let` was introduced in ECMAScript 2015 (ES6) and provides `block-level scoping`. Variables declared with `let` are only accessible within the `block` in which they are defined, whether that's a loop, a conditional statement, or a function.

Example:

```javascript
function example() {
  if (true) {
    let y = 20;
    y = "New type";
  }
  console.log(y); // Throws a ReferenceError: y is not defined
}
example();
```

In this example, `y` is scoped to the `if` block and cannot be accessed outside of it. However one best usecase of the `let` keyword is that we can re-assigned it with a new value in future.

# const:

`const` also came with ES6 (2015) and is used to declare `constants`. The value of a constant `cannot be reassigned once it's initialized`. However, it's important to note that the immutability of `const` applies only to the binding between the `variable identifier` and the value it holds, not to the actual value itself. For `objects` and `arrays`, the properties or elements of a `const` variable can be mutated.

Example:

```javascript
const PI = 3.14;
PI = 3; // Throws a TypeError: Assignment to constant variable.

const myArray = [1, 2, 3];
myArray.push(4); // Allowed
```

- In the first example, trying to reassign a value to `PI` throws an error because it's a `constant`.
- In the second example, while `myArray` itself cannot be reassigned, its elements can be modified.

In modern JavaScript development, it's generally recommended to use `const` by default and only use `let` when variable reassignment is necessary. This helps make your code more predictable and easier to reason about, as it minimizes the risk of accidental reassignments and makes your intent clearer.
