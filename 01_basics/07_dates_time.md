# JavaScript Number and Math Functions

## Number Object in JavaScript

```js
const num = 400;
const num1 = new Number(400);
console.log(num); // Output: 400
console.log(num1); // Output: [Number: 400]
```

### Converting Number to String

```js
console.log(num1.toString()); // Output: "400"
console.log(num1.toString().length); // Output: 3
```

### `toFixed()` Function

- Defines the number of decimal places (rounds off if necessary).
- Returns a string.

```js
const decnum1 = 456.94943;
console.log(decnum1.toFixed(2)); // Output: "456.95"

const decinum2 = 45;
console.log(decinum2.toFixed(3)); // Output: "45.000"
```

### `toPrecision()` Function

- Prints the number with required precision.
- Returns a string and rounds off values if needed.

```js
console.log(decinum2.toPrecision(9)); // Output: "45.0000000"
console.log(decnum1.toPrecision(7)); // Output: "456.9494"
console.log(decnum1.toPrecision(1)); // Output: "5e+2"
```

### `toLocaleString()` Function

- Formats numbers with commas for readability.

```js
const largeValue = BigInt(784930238);
console.log(largeValue.toLocaleString()); // Output: "784,930,238"
console.log(largeValue.toLocaleString('en-IN')); // Output: "78,49,30,238"
```

### Number Constants

```js
console.log(Number.MAX_SAFE_INTEGER); // Maximum safe integer
console.log(Number.MIN_SAFE_INTEGER); // Minimum safe integer
console.log(Number.MAX_VALUE); // Maximum possible value
```

---

# Math Functions in JavaScript

## Math Object

```js
console.log(Math); // Output: [Math Object]
```

### `abs()` Function

- Returns the absolute value.

```js
console.log(Math.abs(-38)); // Output: 38
```

### `round()` Function

- Rounds off to the nearest integer.

```js
console.log(Math.round(47.98)); // Output: 48
```

### `ceil()` Function

- Rounds up to the next integer.

```js
console.log(Math.ceil(4.1)); // Output: 5
```

### `floor()` Function

- Rounds down to the nearest integer.

```js
console.log(Math.floor(4.9)); // Output: 4
```

### `pow()` Function

- Calculates power (a^b).

```js
console.log(Math.pow(2,5)); // Output: 32
```

### `min()` Function

- Finds the minimum value.

```js
console.log(Math.min(2,-5,7,98,-3,2,6,1,-43,56)); // Output: -43
```

### `max()` Function

- Finds the maximum value.

```js
console.log(Math.max(47,67,24,21,13,87,74)); // Output: 87
```

### `random()` Function

- Returns a random number between 0 and 1.

```js
console.log(Math.random()); // Example Output: 0.74893
```

- Generating a random number within a range:

```js
const min = 10;
const max = 20;
console.log(Math.floor((Math.random() * (max - min)) + min)); // Random value between 10 and 20
```

---

# JavaScript Date Functions

## Creating a Date Object

```js
let MyDates = new Date(); // Defaults to the current date and time
console.log(typeof(MyDates)); // Output: "object"
console.log(MyDates.toString());
```

### Converting Date to String

```js
console.log(MyDates.toDateString());
console.log(MyDates.toISOString());
console.log(MyDates.toLocaleDateString());
console.log(MyDates.toJSON());
console.log(MyDates.toLocaleTimeString());
```

### Setting a Specific Date

```js
const myNewDate = new Date(2024, 0, 23);
console.log(myNewDate.toDateString()); // Output: "Tue Jan 23 2024"
```

### Setting Date and Time

```js
const myNewDateTime = new Date(2024, 0, 23, 5, 30, 10);
console.log(myNewDateTime.toLocaleString()); // Output: "23/1/2024, 5:30:10 AM"
```

### Different Date Formats

```js
const dateISO = new Date("2024-01-23");
console.log(dateISO.toLocaleString()); // Output: "23/1/2024"

const dateUS = new Date("01-23-2024");
console.log(dateUS.toDateString()); // Output: "Tue Jan 23 2024"
```

---

# Timestamp in JavaScript

- Measures time in milliseconds since **January 1, 1970** (UNIX Epoch).

```js
let myTimeStamp = Date.now();
console.log(myTimeStamp); // Example Output: 1722571261164
```

- Convert milliseconds to seconds:

```js
console.log(Math.floor(myTimeStamp / 1000));
```

### Extracting Date Components

```js
let NewDate = new Date();  // 02-08-2024
console.log(NewDate.getMonth() + 1); // Output: 8 (August) [Zero-based index]
console.log(NewDate.getDate()); // Output: 2 (Day of the month)
console.log(NewDate.getHours()); // Output: 10 (Hour)
console.log(NewDate.getDay()); // Output: 5 (Friday, as Sunday=0)
```

### Custom Date Formatting

```js
console.log(`Today's date is ${NewDate.getDate()} and time in milliseconds is ${NewDate.getTime()}`);
```

- Formatting with locale options:

```js
console.log(NewDate.toLocaleString('default', { weekday: "long" })); // Output: "Friday"
```
