

# JavaScript Arrays 🚀  

Arrays in JavaScript allow us to store multiple elements in a single variable. Unlike some other languages, JavaScript arrays are **dynamic**, meaning they can grow or shrink in size.  

## Features of JavaScript Arrays:  
- Can store multiple **data types** (Numbers, Strings, Booleans, Objects, even other Arrays).  
- **Zero-based indexing** (First element at index `0`).  
- **Resizable** (Can expand or shrink dynamically).  
- **Shallow Copy Behavior**: Modifications to referenced objects affect all shared variables.  

---

## 📌 Basic Array Declaration  
```js
let myArray = [1, 2, 3, 4, 5, 6, 7, 8, 9];

console.log(myArray[0]); // Output: 1
```

Arrays can store **mixed data types**:  
```js
const myArray2 = ["Anand", "Ankush", "Kumar", 4, 3, 5, [2, 3, 4, 5], true];
```

---

## 🔥 Array Methods  

### 📌 Adding and Removing Elements  

#### **push()** – Adds element at the end  
```js
myArray.push(10); 
console.log(myArray); // [1,2,3,4,5,6,7,8,9,10]
```

#### **pop()** – Removes last element  
```js
myArray.pop();
console.log(myArray); // [1,2,3,4,5,6,7,8,9]
```

#### **unshift()** – Adds element at the beginning  
```js
myArray.unshift(100); 
console.log(myArray); // [100,1,2,3,4,5,6,7,8,9]
```

#### **shift()** – Removes first element  
```js
myArray.shift();
console.log(myArray); // [1,2,3,4,5,6,7,8,9]
```

---

## 🔍 Searching in Arrays  

#### **includes()** – Checks if element exists  
```js
console.log(myArray.includes(20)); // false
```

#### **indexOf()** – Finds index of an element  
```js
console.log(myArray.indexOf(7)); // 6
```

---

## 🎯 Alternative Array Declaration  

Using `new Array()` constructor:  
```js
const singleElementArray = new Array(5); // [undefined, undefined, undefined, undefined, undefined]
const multipleElementArray = new Array(1, 2, 3); // [1, 2, 3]
```

---

## 📌 Converting Array to String  

#### **join()** – Converts array to a comma-separated string  
```js
const joinArray = myArray.join();
console.log(joinArray); // "1,2,3,4,5,6,7,8,9"
```

---

## 🔪 Slice vs Splice  

### **slice()** – Extracts a portion **without modifying** the original array  
```js
console.log("A:", myArray); // Original array

const sliceArray = myArray.slice(1, 3);
console.log(sliceArray); // [2, 3]

console.log("B:", myArray); // Original array remains unchanged
```

### **splice()** – Removes elements **and modifies** the original array  
```js
const mySpliceArray = myArray.splice(1, 3);
console.log(mySpliceArray); // [2, 3, 4]

console.log("C:", myArray); // Original array modified
```

---

## ⚡ Summary of Array Methods  

| Method        | Description |
|--------------|-------------|
| `push()`     | Adds element at the end |
| `pop()`      | Removes last element |
| `unshift()`  | Adds element at the beginning |
| `shift()`    | Removes first element |
| `includes()` | Checks if element exists |
| `indexOf()`  | Finds index of an element |
| `join()`     | Converts array to string |
| `slice()`    | Extracts part of array (no modification) |
| `splice()`   | Removes elements (modifies array) |

---


