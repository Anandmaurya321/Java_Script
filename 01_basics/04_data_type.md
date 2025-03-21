
# JavaScript Data Types

## Introduction
JavaScript provides different types of data to store and manipulate values. Understanding these data types is fundamental to programming in JavaScript.


## JavaScript Data Types

### 1. Primitive Data Types
- **Number** → Can store values up to `2^53`.
- **BigInt** → Used for very large numbers.
- **String** → Text values enclosed in quotes.
- **Boolean** → Represents `true` or `false`.
- **Null** → A standalone value representing "nothing".
- **Undefined** → A declared variable without an assigned value.
- **Symbol** → A unique and immutable identifier.

### 2. Non-Primitive (Reference) Data Type
- **Object** → Collection of key-value pairs.

## Examples of Data Types in JavaScript
```javascript
let name = "Anand maurya";  // String data type
let age = 19;   // Number data type
let isLogin = true;  // Boolean data type

console.log(typeof "Anand maurya"); // Outputs: string
console.log(typeof 34); // Outputs: number
console.log(typeof null); // Outputs: object (special case in JavaScript)
console.log(typeof undefined); // Outputs: undefined
```

## Explanation of Outputs
- `typeof "Anand maurya"` → Returns "string" because it is a sequence of characters.
- `typeof 34` → Returns "number" because it is a numeric value.
- `typeof null` → Returns "object" due to a JavaScript quirk (historically classified as an object).
- `typeof undefined` → Returns "undefined" since no value is assigned.

## Summary
JavaScript has different types of data, categorized into primitive and non-primitive types. Understanding how they work helps in writing efficient and bug-free code.