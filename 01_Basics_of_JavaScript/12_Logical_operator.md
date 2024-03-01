Logical operators are used to combine conditions and control program flow based on multiple boolean expressions. JavaScript provides four main logical operators:

# 1. AND (&&)

The AND operator (`&&`) checks if `both operands are truthy` and returns:

- true if both operands are truthy.
- false if any operand is

> `Short-circuit evaluation`: The evaluation stops after encountering the first falsy operand and returns that value. This behavior can improve efficiency.

Examples:

```js
let isLoggedIn = true;
let hasPermission = true;

if (isLoggedIn && hasPermission) {
  console.log("Access granted!");
} else {
  console.log("Access denied.");
}

// Output: Access granted!
```

# 2. OR (||)

The OR operator (`||`) checks if `at least one operand is truthy` and returns:

- true if any operand is truthy.
- false if both operands are falsy.

> `Short-circuit evaluation`: The evaluation stops after encountering the first truthy operand and returns that value.

Examples:

```js
let isStudent = false;
let isTeacher = true;

if (isStudent || isTeacher) {
  console.log("Eligible for scholarship.");
} else {
  console.log("Not eligible.");
}

// Output: Eligible for scholarship.
```

# 3. NOT (!)

The NOT operator (`!`) inverts the truth value of the operand.

- It returns true if the operand is falsy.
- It returns false if the operand is truthy.

Examples:

```js
let isValid = false;

console.log(!isValid); // true (inverts the value)
```

# 4. Nullish Coalescing (??) -- Introduced in ES2020

The nullish coalescing operator (`??`) provides a safe way to handle `null` and `undefined` values.

- It returns the left operand if it is not null or undefined.
- Otherwise, it returns the right operand.

Examples:

```js
let user = undefined;
let defaultName = "Guest";

let greeting = user ?? defaultName; // greeting will be "Guest"

console.log(undefined ?? "Ajay"); // Ajay
console.log("Success" ?? "Ajay"); // Success
console.log(null ?? undefined); // undefined
```

Summary:

- Logical operators are used to combine boolean expressions.
- They follow short-circuit evaluation, improving performance.
- Use `&&` for conditions requiring both operands to be true.
- Use `||` for situations where at least one operand needs to be true.
- Use `!` to invert the truth value of an operand.
- Use `??` to provide a default value for `null` or `undefined` variables.
