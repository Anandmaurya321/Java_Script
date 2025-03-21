## Summary and Memory Info in JavaScript

### **Primitive Data Types**
Primitive data types store values directly in memory. JavaScript has **7 primitive data types**:

1. **Number**
2. **Boolean**
3. **Null**
4. **String**
5. **Symbol**
6. **BigInt**
7. **Undefined**

### **Reference (Non-Primitive) Data Types**
These data types store references (memory addresses) rather than actual values.

1. **Array**
2. **Object**
3. **Function (Special object type)**

---
### **Data Type Conversion**
JavaScript provides built-in functions to convert data types:

- **`Number()`** → Converts value into a number
- **`Boolean()`** → Converts value into a boolean (`true` or `false`)
- **`String()`** → Converts value into a string

---
### **Symbol Data Type**
- `Symbol` returns a unique value for each variable.

```javascript
const id = Symbol("123");
const another_id = Symbol("123");

console.log(id); // Output: Symbol(123)
console.log(another_id); // Output: Symbol(123)
console.log(id == another_id); // Output: false (Symbols are unique)
```

---
### **BigInt Data Type**
- BigInt is used for very large numbers that cannot be represented using `Number` type.

```javascript
const a = 123n;
console.log(typeof a); // Output: bigint
```

---
### **Array Data Type**
Arrays store multiple values in a single variable.

```javascript
let arr = ["Anand", "Anand Kumar"];
console.log(arr); // Output: [ 'Anand', 'Anand Kumar' ]
```

---
### **Object Data Type**
Objects store key-value pairs.

```javascript
let obj = {
    name: "Anand",
    class: 14
};
console.log(obj); // Output: { name: 'Anand', class: 14 }
```

---
### **Function Data Type**
Functions are objects in JavaScript.

```javascript
let fun = function() {
    console.log("Hello World");
};
fun(); // Output: Hello World
```

---
## **Memory Allocation in JavaScript**
JavaScript uses two types of memory:

1. **Stack Memory** → Used for **primitive data types** (stores actual values)
2. **Heap Memory** → Used for **non-primitive data types** (stores reference addresses)

### **Example: Stack Memory (Primitive Data Types)**
- Stack memory **copies values** rather than referencing them.

```javascript
let s1 = "Anand";
let s2 = s1; // Value is copied
console.log(s2); // Output: Anand

s1 = "Addamy";
console.log(s1); // Output: Addamy
console.log(s2); // Output: Anand (original value remains unchanged)
```

---
### **Example: Heap Memory (Non-Primitive Data Types)**
- Heap memory stores **references**, so modifying one variable affects all references.

```javascript
let obj1 = {
    name: "Anand Maurya",
    email: "abc@gmail.com"
};

let objcpy = obj1; // Reference is passed, not value
objcpy.name = "Adamay"; // Changes the original object

console.log(obj1.name); // Output: Adamay
console.log(objcpy.name); // Output: Adamay
```

📌 **Note:** Unlike primitive types, changing a non-primitive variable affects all references pointing to it.
