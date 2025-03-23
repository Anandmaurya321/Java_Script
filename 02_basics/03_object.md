

# JavaScript Objects & Singleton Pattern 🚀

## Introduction ✨
Objects in JavaScript are key-value pairs used to store structured data and behavior. JavaScript provides multiple ways to create objects, including **object literals**, **constructor functions**, and **Object.create()**.

---

## 📌 Singleton Pattern in JavaScript
A **Singleton** ensures that only **one instance** of an object exists at a time. This is useful for maintaining global configurations or managing shared resources.

### 🔹 Creating a Singleton using a Constructor
```js
// Singleton: When we create an object using a constructor
const Singleton = new function () {
    this.name = "Singleton Instance";
}();

console.log(Singleton.name); // Output: Singleton Instance
```

### 🔹 Using `Object.create()` - Constructor Pattern
```js
const prototypeObj = {
    greet: function() {
        return "Hello from prototype!";
    }
};

const newObj = Object.create(prototypeObj);
console.log(newObj.greet()); // Output: Hello from prototype!
```

---

## 📌 Object Literals in JavaScript
Object literals provide a **simple way** to define objects. They use **key-value pairs**, where keys are strings or symbols.

```js
const my_sym = Symbol("Key1");
const js_user = {
    name: "Anand Maurya",
    [my_sym]: "key value", // Using Symbol as a key
    "Surname": "Maurya",
    age: 20,
    location: "Varanasi",
    isLogin: false,
    last_login: ["Monday", "Tuesday", "Wednesday"]
};
```

### 🔹 Accessing Object Properties 🧐
We can access object properties in two ways:

```js
console.log(js_user.location);   // Output: Varanasi
console.log(js_user["location"]); // Alternative syntax
console.log(js_user["Surname"]);  // Output: Maurya
```

### 🔹 Accessing Symbol Keys 🏷️
```js
console.log(js_user[my_sym]); // Output: key value
```

---

## 📌 Modifying and Freezing Objects ❄️
### 🔹 Changing Object Properties
```js
js_user.age = 19; // Age is updated to 19
```

### 🔹 Freezing an Object (Prevents Modification)
```js
Object.freeze(js_user); // Now the object is frozen

js_user.age = 18; // This won't work, as the object is frozen
console.log(js_user.age); // Output: 19 (unchanged)
```

---

## 📌 Adding Functions to an Object
Objects in JavaScript can store functions as properties.

```js
js_user.greeting = function() {
    console.log("Hello JS user");
};

js_user.greeting_two = function() {
    console.log(`Hello JS user. My name is ${this.name}.`);
};
```

### 🔹 Calling Object Functions
```js
console.log(js_user.greeting()); // Output: Hello JS user
console.log(js_user.greeting);   // Output: [Function (anonymous)]

console.log(js_user.greeting_two()); // Output: Hello JS user. My name is Anand Maurya.
console.log(js_user.greeting_two);   // Output: [Function (anonymous)]
```

---

## 📌 Summary Table 📜
| Feature | Description |
|---------|-------------|
| **Singleton** | Ensures only one instance of an object exists. |
| **Object.create()** | Creates objects with a prototype. |
| **Object Literal** | Simplest way to create objects. |
| **Symbol Keys** | Used for unique property keys. |
| **Object.freeze()** | Prevents object modifications. |
| **Object Functions** | Objects can contain functions as properties. |

---

