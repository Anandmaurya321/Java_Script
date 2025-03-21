# **JavaScript Operations**

## **1. Arithmetic Operations**
JavaScript supports basic arithmetic operations like addition, subtraction, multiplication, etc.

```javascript
console.log(2 + 2); // 4 (Addition)
console.log(2 * 2); // 4 (Multiplication)
console.log(2 ** 3); // 8 (Exponentiation: 2^3)
console.log(3 % 2); // 1 (Remainder when 3 is divided by 2)
console.log(3 / 2); // 1.5 (Division)
```

### **Explanation:**
- `+` adds numbers.
- `*` multiplies numbers.
- `**` represents exponentiation.
- `%` returns the remainder after division.
- `/` performs division.

---

## **2. Unary Operators**
Unary operators operate on a single operand.

```javascript
let con = 4;
let con1 = -con;
console.log(con1); // -4 (Negation)
```

- **Negation (`-`)**: Converts a number into its negative form.
- **Unary `+`**: Converts a value into a number.

```javascript
console.log(+true); // 1 (`true` is converted to 1)
console.log(+'');   // 0 (An empty string is converted to 0)
```

---

## **3. String Concatenation with `+` Operator**

```javascript
let str1 = "hello";
let str2 = " Anand maurya";
let str3 = str1 + str2;
console.log(str3); // "hello Anand maurya"
```

- When `+` is used with strings, it **concatenates** (joins) them instead of performing addition.

```javascript
console.log("2" + 3); // "23" (String + Number → Converts number to string)
console.log(2 + "3"); // "23" (Number + String → Converts number to string)
console.log("2" + 3 + 3); // "233" (Leftmost "2" is a string, so everything becomes a string)
console.log(3 + 3 + "2"); // "62" (3+3=6 first, then "6" + "2" = "62")
```

### **Why does this happen?**
- JavaScript follows **type coercion**, which means it converts numbers to strings when the `+` operator is used between a number and a string.
- If a number appears **first**, normal arithmetic happens before conversion.
- If a **string appears first**, everything gets converted to a string.

---

## **4. Assignment with Multiple Variables**

```javascript
let num1, num2, num3;
num1 = num2 = num3 = 3 + 3; // num1 = num2 = num3 = 6
```

- JavaScript allows **chaining assignments**, meaning all variables receive the same value.

---

## **5. Increment and Decrement Operators**
These operators increase or decrease a value by 1.

### **Post-increment (`var++`) and Pre-increment (`++var`)**

```javascript
num1++; 
console.log(num1); // 7 (Post-increment: num1 was 6, then increased to 7)

++num1; 
console.log(num1); // 8 (Pre-increment: num1 increased to 8 before logging)

console.log(++num1); // 9 (num1 is now 9 after pre-increment)
console.log(num1++); // 9 (Prints 9, then increases num1 to 10)
```

### **Difference:**
- **`num++` (Post-increment)** → First returns the current value, then increases it.
- **`++num` (Pre-increment)** → First increases the value, then returns it.

---

## **Key Takeaways**
✅ **Use `+` carefully with numbers and strings** to avoid unwanted string concatenation.
✅ **Understand the difference between `++num` and `num++`** to avoid logical errors.
✅ **Unary `+` can convert non-number values** into numbers.
✅ **Use `%` for remainder calculations.**

---

This guide simplifies JavaScript operations with explanations and examples! 🚀 Feel free to share or modify it as needed! 💡
