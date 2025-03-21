

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
