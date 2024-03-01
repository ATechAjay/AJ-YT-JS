# What are Conditional Statements?

Conditional statements are the traffic lights of your code. They allow you to execute different blocks of code based on whether certain conditions are true or false. JavaScript offers several constructs for conditional logic:

### 1. if Statements

The most basic form of conditional execution. Checks if a specific condition is true. If so, it executes the code block within the `if` statement's curly braces.

```js
let age = 25;
if (age >= 18) {
  console.log("You are eligible to vote");
}
```

### 2. else Statements

The `"backup"` plan for an `if` statement. If the `if` condition is false, the code block within the `else` statement is executed.

```js
let isWeekend = false;
if (isWeekend) {
  console.log("Time to relax!");
} else {
  console.log("Back to work.");
}
```

### 3. else if Statements

Used to chain multiple conditions together. Provide additional checks if the initial `if` condition is false.

```js
let grade = 85;
if (grade >= 90) {
  console.log("Excellent! You got an A");
} else if (grade >= 80) {
  console.log("Good job! You got a B");
} else {
  console.log("Keep studying harder.");
}
```

### 4. Switch Statements

Good for comparing a single variable against multiple possible values. Each `case` acts as a comparison, and if there's a match, the associated code block runs. The `default` case is like an `else` for the entire `switch`.

```js
let dayOfWeek = "Monday";
switch (dayOfWeek) {
  case "Saturday":
  case "Sunday":
    console.log("It's the weekend!");
    break;
  default:
    console.log("Weekday blues...");
}
```

# Note on Truthy and Falsy

- Conditions in JavaScript are evaluated as either `"truthy"` or `"falsy."`
- Truthy values: Values that translate to `true` in a boolean context (numbers except 0, non-empty strings, objects, arrays, etc.)
- Falsy values: Values that translate to `false` (0, empty strings "", `null`, `undefined`, `NaN`)
