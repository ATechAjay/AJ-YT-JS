When we want to compare two values, we have to use the equality operators. In JavaScript, there are two core ways to compare values for equality:

1. Loose Equality (==): Checks if two values are `roughly equivalent` after potential type conversions.
2. Strict Equality (===): Checks if two values are the same without any type conversion.

# Loose Equality (==)

The loose equality operator attempts to convert values of different types before comparing them. This can lead to surprising results.

Examples:

```js
1 == "1"; // true (number 1 is converted to string "1")
0 == false; // true (number 0 is converted to boolean false)
null == undefined; // true (both are considered loosely equal)
```

# Strict Equality (===)

The strict equality operator is more predictable. It only returns `true` if the values being compared have `the same type and the same value`.

Examples:

```js
1 === "1"; // false (number 1 is not the same type as string "1")
0 === false; // false (number 0 is not the same type as boolean false)
null === undefined; // false (null and undefined are distinct types)
```

> Best Practice: It's generally recommended to favor strict equality (`===`) to avoid unexpected type conversion behavior. Use loose equality (`==`) only when you intentionally need type coercion.

> Performance: Strict equality can be marginally faster in some cases since it `doesn't need to perform type conversions`.

### Table Summary

| Operator | Description                           | Example              |
| -------- | ------------------------------------- | -------------------- |
| `==`     | Loose equality (with type coercion)   | `"5"` == 5 // true   |
| `===`    | Strict equality (no type coercion)    | `"5"` === 5 // false |
| `!=`     | Loose inequality (with type coercion) | `0` != null // false |
| `!==`    | Strict Inequality (no type coercion)  | `0` !== null // true |

# Important Note about Objects

When comparing objects (including arrays), both loose and strict equality check for reference equality. This means they only return `true` if both variables point to the exact same object in memory.

```js
let obj1 = { name: "Alice" };
let obj2 = { name: "Alice" };

obj1 == obj2; // false (different object instances)
obj1 === obj2; // false (different object instances)
```
