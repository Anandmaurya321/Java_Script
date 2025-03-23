

# JavaScript Array Manipulation 🚀  

JavaScript provides several methods to manipulate arrays efficiently. Here, we will explore **push, concat, spread operator, flat, and various array conversion methods**.  

---

## 1️⃣ **Adding an Array as an Element using `push()`**  
When we use `push()` to add an array inside another array, it stores the entire array as a **single element**, creating a nested structure.  

```js
const marvel_heroes = ["Thor", "Spiderman", "Ironman"];
const dc_heroes = ["Superman", "Batman", "Flash"];

marvel_heroes.push(dc_heroes); // Adds dc_heroes as a single element
console.log(marvel_heroes);

// Output: [ 'Thor', 'Spiderman', 'Ironman', [ 'Superman', 'Batman', 'Flash' ] ]
console.log(marvel_heroes[3][1]); // Accessing Batman
```

---

## 2️⃣ **Concatenation using `concat()`**
The `concat()` method merges two arrays and **returns a new array** without modifying the original ones.  

```js
const all_heroes = marvel_heroes.concat(dc_heroes);
console.log(all_heroes);

// Output: [ 'Thor', 'Spiderman', 'Ironman', 'Superman', 'Batman', 'Flash' ]
```

---

## 3️⃣ **Concatenation using Spread Operator `...`**
Using the **spread operator (`...`)**, we can achieve the same result as `concat()`, but in a cleaner way.  

```js
const new_all_heroes = [...dc_heroes, ...marvel_heroes];
console.log(new_all_heroes);

// Output: [ 'Superman', 'Batman', 'Flash', 'Thor', 'Spiderman', 'Ironman' ]
```

---

## 4️⃣ **Flattening Nested Arrays using `flat()`**
The `flat()` method **flattens** nested arrays into a single array. We can specify the depth to which we want to flatten.  

```js
const nested_array = ["Anand", ["Ankush", "Aman"], ["Ankush", ["Aman", "Kumar"]]];
const simplified_array = nested_array.flat(2); // Flattens up to depth 2

console.log(simplified_array);

// Output: [ 'Anand', 'Ankush', 'Aman', 'Ankush', 'Aman', 'Kumar' ]
```

---

## 5️⃣ **Checking and Converting Data into Arrays**
### 🔹 **Checking if a value is an array using `Array.isArray()`**
```js
console.log(Array.isArray("Anand")); // Output: false
```

### 🔹 **Converting a String into an Array using `Array.from()`**
```js
const converted_arr = Array.from("Anand Maurya");
console.log(converted_arr);

/* Output:
 [
    'A', 'n', 'a', 'n',      
    'd', ' ', 'M', 'a',      
    'u', 'r', 'y', 'a'       
  ]
*/
```

### 🔹 **Attempting to Convert an Object into an Array**
If `Array.from()` is used on an object without iterable properties, it returns an **empty array**.  

```js
const converted_arr = Array.from({name: "Anand"});
console.log(converted_arr); // Output: []
```

---

## 6️⃣ **Creating Arrays using `Array.of()`**
The `Array.of()` method creates an array from a set of values.  

```js
const score1 = 100;
const score2 = 200;
const score3 = 300;

console.log(Array.of(score1, score2, score3)); 
// Output: [ 100, 200, 300 ]
```

---
