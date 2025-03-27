# JavaScript Notes

## Understanding `this`

- The `this` keyword is used to refer to the current object.
- It helps in accessing elements within the same object function.

```javascript
const my_obj = {
    name: "Anand",
    price: 1200,

    // Defining function using Type 2 declaration (with a variable)
    fun: function(){
        console.log(`${this.name}, welcome`);
        console.log(this); // Prints the current object
    }
};

my_obj.fun();
// Output:
// Anand, welcome
// { name: 'Anand', price: 1200, fun: [Function: fun] }

// Changing object property
my_obj.name = "Sam";
my_obj.fun();
// Output:
// Sam, welcome
// { name: 'Sam', price: 1200, fun: [Function: fun] }
```

### `this` in Different Environments
```javascript
console.log(this); 
// In Node.js, `this` refers to an empty object: {}
// In the browser, `this` refers to the global `window` object.
```

### `this` in Functions

#### Regular Function
```javascript
function chai(){
    const name = "Anand";
    console.log(this.name); // Undefined, as `this` is not bound to functions
}
```

#### Function Expression
```javascript
const fun1 = function(){
    const name = "Anand";
    console.log(this.name); // Undefined, same issue as regular functions
};
```

## Arrow Functions
```javascript
const arrow_fun = () => {
    const name = "Anand";
    console.log(this.name); // Undefined, arrow functions do not have their own `this`
};
```

### Explicit Return in Arrow Functions
```javascript
const add_three = (num1, num2, num3) => {
    return num1 + num2 + num3;
};

console.log(add_three(10, 20, 30)); // Output: 60
```

### Implicit Return in Arrow Functions
```javascript
const sub_two = (num1, num2) => num1 - num2; 
// OR
const sub_two = (num1, num2) => (num1 - num2);
```

### Returning an Object in Arrow Functions
```javascript
const return_obj = () => ({ name: "Anand", section: "A" });
console.log(return_obj());
// Output: { name: 'Anand', section: 'A' }
```

### Arrow Function Syntax Recap
- **Implicit return**: `()=>()`
- **Explicit return**: `()=>{ return () }`

