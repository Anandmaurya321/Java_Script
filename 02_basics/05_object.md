# JavaScript Objects 📌

JavaScript objects are fundamental data structures that store key-value pairs. Objects can be created using constructors or object literals.

---

## 1️⃣ Creating Objects

### Using Constructor (`new Object()`) - Singleton Object
```js
const tinderUser = new Object(); // Constructor method
console.log(tinderUser); // Output: {}
```

### Using Object Literals (Preferred)
```js
const tinderUser1 = {}; // Object literal
console.log(tinderUser1); // Output: {}
```

### Defining Object Properties
```js
const tinderUser = {};
tinderUser.id = "123abc";
tinderUser.name = "Anand";
tinderUser.isLoggedin = false;
console.log(tinderUser);
```

---

## 2️⃣ Nested Objects 🏗️
```js
const regularUser = {
    emailId: "anand@gmail.com",
    fullName: {
        userFullName: {
            firstName: "Anand",
            lastName: "Maurya"
        }
    }
};
console.log(regularUser.fullName.userFullName.firstName); // Output: Anand
```

🔹 Use `.` notation to access object properties.
🔹 To check if a property exists, use `hasOwnProperty()`.

---

## 3️⃣ Combining Multiple Objects 🛠️

### Using `Object.assign()`
```js
const obj1 = { 1: "a", 2: "b" };
const obj2 = { 3: "c", 4: "d" };
const obj3 = { 5: "e", 6: "f" };
const obj4 = Object.assign({}, obj1, obj2, obj3);
console.log(obj4);
```

### Using Spread Operator (Preferred)
```js
const obj4 = { ...obj1, ...obj2, ...obj3 };
console.log(obj4);
```

---

## 4️⃣ Array of Objects 📋
```js
const objArr = [
    { id: 1, email: "a@gmail.com" },
    { id: 2, email: "b@gmail.com" },
    { id: 3, email: "c@gmail.com" }
];
console.log(objArr[1].email); // Output: b@gmail.com
```

---

## 5️⃣ Object Methods 🔍

### Finding Keys, Values & Entries
```js
console.log(Object.keys(tinderUser));   // Returns an array of keys
console.log(Object.values(tinderUser)); // Returns an array of values
console.log(Object.entries(tinderUser)); // Returns an array of key-value pairs
```

### Checking Property Existence
```js
console.log(tinderUser.hasOwnProperty('isLoggedin')); // Output: true
```

---

## 6️⃣ Object Prototype Methods
Every JavaScript object inherits methods from `Object.prototype`.

Some useful ones:
- `hasOwnProperty(property)`: Checks if a property exists.
- `toString()`: Converts an object to a string.
- `valueOf()`: Returns the primitive value of an object.
- `isPrototypeOf()`: Checks if an object is in another's prototype chain.

Example:
```js
const obj = { 1: "Anand", 2: "Maurya", 3: "Kumar" };
console.log(obj.hasOwnProperty(2)); // Output: true
console.log(obj.toString()); // Output: [object Object]
```

---

## 7️⃣ Object Destructuring 🎯
Destructuring allows extracting object properties into variables.

### Basic Destructuring
```js
const course = {
    name: "Js_hindi",
    price: 999,
    instructor: "Anand"
};

const { instructor } = course; // Extracts instructor property
console.log(instructor); // Output: Anand
```

### Destructuring with Alias
```js
const { name: nm } = course;
console.log(nm); // Output: Js_hindi
```

---

## 🔥 Summary Table

| Feature                | Method / Example |
|------------------------|-----------------|
| **Create Object**      | `new Object()`, `{}` |
| **Access Property**    | `obj.key`, `obj["key"]` |
| **Check Property**     | `obj.hasOwnProperty('key')` |
| **Find Keys**          | `Object.keys(obj)` |
| **Find Values**        | `Object.values(obj)` |
| **Find Entries**       | `Object.entries(obj)` |
| **Combine Objects**    | `Object.assign({}, obj1, obj2)`, `{...obj1, ...obj2}` |
| **Array of Objects**   | `[ { id:1, email:"a@gmail.com" }, ... ]` |
| **Destructuring**      | `const { key } = obj` |

---

