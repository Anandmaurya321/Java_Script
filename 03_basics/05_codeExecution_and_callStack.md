
# JavaScript Execution Context

## 1. JavaScript Execution Context

### Three Types of Execution Context:
1. **Global Execution Context**
2. **Function Execution Context**
3. **Eval Execution Context**

### JavaScript Code Runs in Two Phases:
1. **Memory Creation Phase**: Allocates memory for variables.
2. **Execution Phase**: Executes the code.

### Example Code:
```js
let val1 = 10;
let val2 = 20;

function add(num1, num2) {
    let total = num1 + num2;
    return total;
}

let result1 = add(val1, val2);
let result2 = add(5, 7);
```

### Execution Breakdown:
#### 1. Global Execution Context
- Every JavaScript code starts in the global execution context.
- Accessed via `this` in browsers (refers to `window` object).

#### 2. Memory Allocation Phase
Memory is allocated as:
```plaintext
val1 = undefined
val2 = undefined
add = function definition
result1 = undefined
result2 = undefined
```

#### 3. Execution Phase
```plaintext
val1 = 10
val2 = 20
Skip 'add' (nothing to execute directly)
result1 = add(val1, val2) → Creates a new execution context
```

When `add(val1, val2)` is called:
- A **new execution context** is created with:
  - **Memory Allocation:**
    ```plaintext
    num1 = undefined
    num2 = undefined
    total = undefined
    ```
  - **Execution:**
    ```plaintext
    num1 = val1 (10)
    num2 = val2 (20)
    total = num1 + num2 (30)
    ```
  - Returns `total` to the global execution context and frees memory.

Same process happens for `result2 = add(5, 7)`.

---

## Call Stack in JavaScript

### Example Code:
```js
function one() {
    console.log("one");
    two();
}
function two() {
    console.log("two");
    three();
}
function three() {
    console.log("three");
}

one();
two();
three();
```

### Execution Flow:
1. `one()` is pushed to the **Call Stack** → Executes `console.log("one")`
2. `two()` is called inside `one()` → Pushed to **Call Stack** → Executes `console.log("two")`
3. `three()` is called inside `two()` → Pushed to **Call Stack** → Executes `console.log("three")`
4. `three()` completes and pops from the stack.
5. `two()` completes and pops from the stack.
6. `one()` completes and pops from the stack.

Final output:
```plaintext
one
two
three
two
three
```

---

## Summary:
- **Execution Context** is created whenever a function is called.
- **Memory is allocated first**, then the **code is executed**.
- **Call Stack** maintains function execution order (LIFO - Last In, First Out).


