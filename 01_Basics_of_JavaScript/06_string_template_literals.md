In JavaScript, strings are sequences of characters, typically used to represent text. They can be enclosed within single quotes `'...'`, double quotes `"..."`, or backticks ` (``) `.

# String Literals:

String literals are the basic way of representing strings in JavaScript.

Example:

```js
let singleQuoted = "Hello, world!";
let doubleQuoted = "Hello, world!";
let backtickQuoted = `Hello, world!`;
```

All three variables (`singleQuoted`, `doubleQuoted`, and `backtickQuoted`) store the same string, `"Hello, world!"`.

# Template Literals:

Template literals, introduced in ECMAScript 6 (ES6), provide a more flexible way to create strings. They are delimited by backticks ` (``) ` and allow for embedded expressions and multiline strings.

### Template literals support the following features:

1. `String Interpolation`: You can embed expressions directly into template literals using `${}` syntax.

Example:

```js
let name = "John";
let greeting = `Hello, ${name}!`;
console.log(greeting); // Output: "Hello, John!"
```

2. `Multiline Strings`: Template literals allow you to create multiline strings without needing to use escape characters like `\n`.

Example:

```js
let multiline = `This is a
multiline
string.`;
console.log(multiline);
// Output:
// This is a
// multiline
// string.
```

3. `Expression Evaluation`: Any valid JavaScript expression can be used inside `${}` in template literals.

Example:

```js
let a = 5;
let b = 10;
let sum = `The sum of ${a} and ${b} is ${a + b}`;
console.log(sum); // Output: "The sum of 5 and 10 is 15"
```

Template literals provide a cleaner and more readable syntax for creating strings, especially when dealing with `dynamic content` or `multiline text`. They are widely used in modern JavaScript development for their flexibility and convenience.
