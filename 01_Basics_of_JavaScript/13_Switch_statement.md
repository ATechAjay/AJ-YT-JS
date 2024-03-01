# What is a switch statement?

The switch statement lets you execute different code blocks based on the value of an expression. It's like a more structured alternative to multiple `if...else if...else` statements, often making your code more readable when you have many conditions.

Syntax:

```js
switch (expression) {
  case value1:
    // Code to execute if expression matches value1
    break;

  case value2:
    // Code to execute if expression matches value2
    break;

  // ... more cases if needed

  default:
  // Code to execute if no cases match
}
```

# How Switch case works?

1. Evaluation: The `expression` within the `switch` parentheses is evaluated once.
2. Comparison: The value of the `expression` is compared with the values following each `case` keyword.
3. Match: If a `case` value matches the expression's value, the code in that `case` block is executed.
4. Break: The `break` keyword is crucial, It prevents "fall-through". Without `break`, the code will continue executing into subsequent `case` blocks until it hits a `break` or the end of the `switch`.
5. Default: The optional `default` block is executed if no `case` values match.

Example:

```js
let day = new Date().getDay(); // getDay() returns day of week (0-6)

switch (day) {
  case 0:
    console.log("It's Sunday!");
    break;
  case 6:
    console.log("It's Saturday!");
    break;
  default:
    console.log("Just another weekday.");
}
```

# Things to keep in mind

- `Strict Comparison`: The `switch` statement uses strict equality comparison (`===`). Ensure your expression and case values have the same data type.
- `The Power of break`: Don't forget those `break` statements to avoid unintentional fall-through.
- `Default for "Otherwise"`: The `default` block acts as your catch-all scenario.
- `Flexibility`: You can test for multiple values within a single case if needed:

  ```js
  case 1:
  case 2:
  case 3:
     // Code to execute if day is 1, 2, or 3
     break;
  ```
