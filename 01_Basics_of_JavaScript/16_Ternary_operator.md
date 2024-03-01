# What is the Ternary Operator?

The ternary operator provides a compact way to write a conditional expression that works much like a concise `if...else` statement. It's the only JavaScript operator that takes `three operands`.

Syntax:

```js
`condition` ? `expression_if_true` : `expression_if_false`;
```

Explanation:

- `condition`: An expression that is evaluated to a boolean value (`true` or `false`).
- `expression_if_true`: The expression executed if the `condition` evaluates to `true`.
- `expression_if_false`: The expression executed if the `condition` evaluates to `false`.

Example

```js
let age = 25;
let eligibility = age >= 18 ? "Eligible to vote" : "Not eligible to vote";
console.log(eligibility); // Output: "Eligible to vote"
```

# How it Works

- The condition (`age >= 18`) is evaluated.
- Since it's `true`, the expression `"Eligible to vote"` is returned and assigned to the `eligibility` variable.
- If the condition was `false`, the expression `"Not eligible to vote"` would be assigned.

# Benefits of ternary operator

- Conciseness: It provides a shorter way to write simple conditional statements.
- Readable (if used appropriately): Can make simple conditions more readable within a single line.

# Cautions

Overuse hurts readability: Nesting multiple ternary operators can quickly make code confusing. Prioritize readability, and use traditional `if...else` when complexity increases.
