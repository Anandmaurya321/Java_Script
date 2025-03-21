# Number and Math Functions in JavaScript

## Number Object in JavaScript
JavaScript provides a `Number` object with various methods to perform numerical operations.

### Creating Numbers
```javascript
const num = 400;
const num1 = new Number(400);
console.log(num);  // Output: 400
console.log(num1); // Output: [Number: 400]
```
`num` is a primitive number, while `num1` is a `Number` object.

## Number Methods

### 1. Convert Number to String
```javascript
console.log(num1.toString());       // Output: "400"
console.log(num1.toString().length); // Output: 3
```
Converts a number to a string.

### 2. `toFixed()` Function
- Rounds a number to a fixed number of decimal places and returns a string.
```javascript
const decnum1 = 456.94943;
console.log(decnum1.toFixed(2)); // Output: "456.95"

const decinum2 = 45;
console.log(decinum2.toFixed(3)); // Output: "45.000"
```

### 3. `toPrecision()` Function
- Formats a number to a specified precision, returning a string.
```javascript
console.log(decinum2.toPrecision(9)); // Output: "45.0000000"
console.log(decnum1.toPrecision(7));  // Output: "456.9494"
console.log(decnum1.toPrecision(1));  // Output: "5e+2"
```

### 4. `toLocaleString()` Function
- Converts a number into a string formatted according to a locale.
```javascript
const largeValue = BigInt(784930238);
console.log(largeValue.toLocaleString());      // Output: "784,930,238"
console.log(largeValue.toLocaleString('en-IN'));// Output: "78,49,30,238"
```

## Number Constants
```javascript
console.log(Number.MAX_SAFE_INTEGER); // Output: 9007199254740991
console.log(Number.MIN_SAFE_INTEGER); // Output: -9007199254740991
console.log(Number.MAX_VALUE);        // Output: 1.7976931348623157e+308
```

---

# Math Functions in JavaScript

## 1. `Math.abs()` - Absolute Value
```javascript
console.log(Math.abs(-38)); // Output: 38
```
Returns the absolute (positive) value.

## 2. `Math.round()` - Round to Nearest Integer
```javascript
console.log(Math.round(47.98)); // Output: 48
```
Rounds the number to the nearest integer.

## 3. `Math.ceil()` - Round Up
```javascript
console.log(Math.ceil(4.1)); // Output: 5
```
Always rounds up to the nearest integer.

## 4. `Math.floor()` - Round Down
```javascript
console.log(Math.floor(4.9)); // Output: 4
```
Always rounds down to the nearest integer.

## 5. `Math.pow(a, b)` - Exponentiation
```javascript
console.log(Math.pow(2, 5)); // Output: 32 (2^5)
```
Computes `a` raised to the power of `b`.

## 6. `Math.min()` - Minimum Value
```javascript
console.log(Math.min(2, -5, 7, 98, -3, 2, 6, 1, -43, 56)); // Output: -43
```
Finds the smallest number in the list.

## 7. `Math.max()` - Maximum Value
```javascript
console.log(Math.max(47, 67, 24, 21, 13, 87, 74)); // Output: 87
```
Finds the largest number in the list.

## 8. `Math.random()` - Generate Random Numbers

### Generate a Random Number Between 0 and 1
```javascript
console.log(Math.random()); // Output: (Random decimal between 0 and 1)
```

### Generate a Random Number Between 0 and 100
```javascript
console.log(Math.floor(Math.random() * 100)); // Output: (Random integer from 0 to 99)
console.log(Math.ceil(Math.random() * 100)); // Output: (Random integer from 1 to 100)
```

### Generate a Random Number in a Given Range
- Formula: `Math.floor(Math.random() * (max - min + 1)) + min`
- Ensures values are within the given range `[min, max]`.

#### Example: Generate a number between 10 and 20
```javascript
const min = 10;
const max = 20;
console.log(Math.floor(Math.random() * (max - min + 1)) + min);
// Output: (Random integer between 10 and 20, inclusive)
```

---

