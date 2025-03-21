

# JavaScript Variables - Explained Simply

## What are Variables?
A **variable** is a named storage that holds a value. In JavaScript, we can declare variables using:
- `const` (constant, cannot be changed)
- `let` (block-scoped, can be changed)
- `var` (function-scoped, avoid using)

---
## **1. `const` - The Immutable Variable**
- A `const` variable **cannot** be reassigned a new value after declaration.
- It **must** be initialized when declared.
- However, if the value is an **object or array**, its **properties/elements can be modified**.

### Example:
```javascript
const accountId = 1283;
// accountId = 24;  ❌ Error! Cannot reassign a const variable.

const user = { name: "John" };
user.name = "Doe"; // ✅ Allowed (modifying property)
console.log(user); // { name: "Doe" }
```

---
## **2. `let` - The Block-Scoped Variable**
- Can be reassigned a new value.
- **Block-scoped**, meaning it's only accessible inside `{}` where it's declared.
- Prevents issues caused by `var` (explained next).

### Example:
```javascript
let emailId = "anand123@gmail.com";
emailId = "abc@gmail.com"; // ✅ Allowed
console.log(emailId); // abc@gmail.com
```

---
## **3. `var` - The Function-Scoped Variable (Avoid Using)**
- `var` is **function-scoped**, meaning it’s accessible anywhere inside a function.
- It **ignores block scope**, which can lead to unexpected behavior.
- It **can be redeclared**, causing bugs.

### Example:
```javascript
if (true) {
    var city = "Varanasi";
}
console.log(city); // ✅ Accessible outside the block (Not safe)
```
**Why is this a problem?**
- If you use `let` instead, the variable would not be accessible outside the block, which is safer.

---
## **4. Declaring Variables Without `const`, `let`, or `var` (Not Recommended)**
- If you assign a value **without declaring it using `let`, `const`, or `var`**, JavaScript treats it as a **global variable**.
- This is dangerous because it can unintentionally affect other parts of the program.

### Example:
```javascript
accountState = "Uttar Pradesh"; // ❌ Bad practice (Implicit Global Variable)
console.log(accountState); // ✅ Works, but should be avoided.
```

---
## **5. Difference Between `const`, `let`, `var`, and Implicit Declaration**
| Variable Type | Can Change Value? | Scope | Can Be Redeclared? |
|--------------|-----------------|-------|-----------------|
| `const` | ❌ No | Block Scope | ❌ No |
| `let` | ✅ Yes | Block Scope | ❌ No |
| `var` | ✅ Yes | Function Scope | ✅ Yes (Bad practice) |
| Implicit (`x = 10;`) | ✅ Yes | Global Scope | ✅ Yes (Worst practice) |

---
## **6. Best Practices**
✅ **Use `const`** when the value should never change.
✅ **Use `let`** when you need to update a variable.
❌ **Avoid `var`** due to its function-scoping issues.
❌ **Never declare variables without `let`, `const`, or `var`** to prevent accidental global pollution.

---
### **Final Example Code**
```javascript
const accountId = 1283; // Cannot be changed
let emailId = "abc@gmail.com"; // Can be updated
var city = "xyz"; // Not recommended
accountState = "Uttar Pradesh"; // Bad practice (Implicit Global Variable)

console.table([accountId, emailId, city, accountState]);

emailId = "abc@gmail.com";
city = "abc";
accountState = "Gorakhpur";

console.table([accountId, emailId, city, accountState]);
```

