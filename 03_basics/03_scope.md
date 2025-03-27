# JavaScript Functions and Variable Scope

## Block Scope vs Function Scope

```javascript
if(true){
    let a = 20; 
    const b = 30;
    var c = 40;
}

// console.log(a) 
// It cannot be accessed as its scope is limited to the if block.

// console.log(b)
// It cannot be accessed as its scope is also limited to the if block.

// console.log(c)
// It can be accessed because 'var' does not obey block scope.
```

### `let` Keyword
```javascript
/**
 * `let` is used for variables whose values can be modified.
 * It obeys block scope, meaning it is accessible only within the `{}` where it is defined.
 * It is preferred for variables whose values may change.
 */
```

### `const` Keyword
```javascript
/**
 * `const` is used for constants whose values cannot be modified.
 * It also obeys block scope and is accessible only within its `{}` block.
 * It is used when the variable’s value should remain constant.
 */
```

### `var` Keyword
```javascript
/**
 * `var` is similar to `let`, but it does **not** obey block scope.
 * It has function scope, meaning it is accessible outside `{}`.
 * This can cause unintended bugs, which is why `var` is generally avoided.
 */

if(true){
    var num = 100;
}
console.log(num); // Output: 100 (not blocked by scope)
```

### Local vs Global Scope
```javascript
let let_var = 10;

if(true){
    let let_var = 40;
    console.log(let_var); // Local scope variable takes priority
}

console.log(let_var); // Prints global value (10)
```

## Nested Functions
```javascript
function one(){
    let user_name = "Anand";

    function two(){
        // Function inside function
        let platform = "YouTube";
        console.log(user_name); // Accessible due to lexical scope
    }
    
    // console.log(platform); // Not accessible here
    two(); // Calling `two` function
}

one();
```

## Nested If Conditions
```javascript
if(true){
    let name = "Anand";
    if(true){
        let surname = "Maurya";
        console.log(name + surname); // Accessible within nested block
    }
    // console.log(surname); // Not accessible outside the inner block
}

// console.log(name); // Not accessible outside the outer block
```

## Function Declarations vs Expressions

### Function Declaration (Hoisting Allowed)
```javascript
console.log(add_one(5)); 
// We can call the function before its declaration due to hoisting.

function add_one(num){
    return num + 1;
}
```

### Function Expression (No Hoisting)
```javascript
// console.log(add_two(8)); // Error: Cannot access before initialization

const add_two = function(num){
    return num + 2;
};

console.log(add_two(8)); // Works as expected
```




