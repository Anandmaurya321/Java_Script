# **JavaScript Type Conversion & Coercion**

## **1. Understanding `typeof` Operator**
The `typeof` operator helps check the data type of a variable.

```javascript
let score = "45";
console.log(typeof score); // "string"
console.log(typeof (score)); // "string"
```

- Since `score` is enclosed in double quotes, it is treated as a **string**.

---

## **2. Converting Values to Number**
The `Number()` function converts different data types into numbers.

```javascript
let numval = Number(score); // Converts "45" to 45 (number)
let var1 = "abc"; 
let var11 = Number(var1); // NaN (Cannot convert "abc" to a number)
let var2 = null; 
let var22 = Number(var2); // 0 (null converts to 0)
let var3 = undefined; 
let var33 = Number(var3); // NaN (undefined converts to NaN)
```

### **Outputs:**
```javascript
console.log(typeof (score)); // "string"
console.log(typeof (numval)); // "number"
console.log(typeof (var1)); // "string"
console.log(typeof (var22)); // "number"
console.log(typeof (var33)); // "number"

console.log(score);  // "45" (string)
console.log(numval); // 45 (number)
console.log(var1);   // "abc" (string)
console.log(var22);  // 0 (number)
console.log(var33);  // NaN (Not a Number)
```

### **Conversions Summary:**
| Value | Conversion to Number |
|-------|----------------------|
| "33"  | `33` (number) |
| "33abc" | `NaN` (invalid number) |
| `true` | `1` |
| `false` | `0` |
| `null` | `0` |
| `undefined` | `NaN` |

---

## **3. Converting Values to Boolean**
JavaScript automatically converts values to `true` or `false` in conditions.
You can explicitly convert values using `Boolean()`.

```javascript
let b = 1;
let boolvalue = Boolean(b);
console.log(boolvalue); // true (1 is treated as true)
```

```javascript
let b1 = "anand";
let b2 = Boolean(b1);
console.log(b2); // true (Non-empty strings are true)
```

### **Boolean Conversion Rules:**
| Value | Conversion to Boolean |
|-------|----------------------|
| `1` | `true` |
| `0` | `false` |
| `""` (empty string) | `false` |
| `"anand"` (non-empty string) | `true` |

---

## **4. Converting Values to String**
Use the `String()` function to convert numbers to strings.

```javascript
let v = 123;
let stringv = String(v);
console.log(stringv); // "123"
console.log(typeof stringv); // "string"
```

### **Conversion Summary:**
| Value | Conversion to String |
|-------|----------------------|
| `123` | "123" |
| `true` | "true" |
| `false` | "false" |
| `null` | "null" |
| `undefined` | "undefined" |

---

## **Key Takeaways**
✅ `Number()`, `String()`, and `Boolean()` help in **explicit type conversion**.
✅ **Falsy values**: `0`, `false`, `null`, `undefined`, `""` → Convert to `false`.
✅ **Truthy values**: Any non-zero number, non-empty string → Convert to `true`.
✅ **NaN (Not a Number)** results from invalid numerical conversions.
✅ **Use `typeof` to check variable types** before conversion.

---

