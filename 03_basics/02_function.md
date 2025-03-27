

# JavaScript Functions - Notes

## Function Declaration

```javascript
// This function, myName, prints the name "Anand Mauraya" when executed.
function myName() {
    console.log("Anand Mauraya");
}
```

## Function Reference vs Execution

```javascript
myName;  // This is just a reference to the function. It does not execute it.
myName(); // Adding parentheses () executes the function, printing "Anand Mauraya".
```

## Function to Add Two Numbers

```javascript
// This function takes two parameters, num1 and num2, and returns their sum.
function addTwoNumbers(num1, num2) {
    return num1 + num2;
}

// Calling the function and storing the result
let result = addTwoNumbers(5, 5); // 5 and 5 are arguments passed to the function
console.log(result); // Output: 10
```

## Function to Log a User's Status

```javascript
// This function takes a name as a parameter and returns a message.
function isLogged(name) {
    return `${name} has just logged in.`;
}

console.log(isLogged("Anand Maurya")); // Output: Anand Maurya has just logged in.
```

## Handling Undefined Parameter

```javascript
// If no name is provided, return an appropriate message.
function isLogged(name) {
    if (name === undefined) {  
        /**
         * In JavaScript, undefined is considered a falsy value,
         * so we can also use: if (!name) instead of if (name === undefined).
         */
        return "Please enter a valid name.";
    }
    return `${name} has just logged in.`;
}

console.log(isLogged()); // Output: Please enter a valid name.
```

## Using Default Parameters

```javascript
// If no argument is provided, the function uses a default value.
function isLogged(name = "Anand") {
    // If a value is provided, it overwrites the default.
    return `${name} has just logged in.`;
}

console.log(isLogged()); // Output: Anand has just logged in.
console.log(isLogged("Rahul")); // Output: Rahul has just logged in.
```

## Passing an Unknown Number of Elements

```javascript
// Function to add elements to a cart
function addElementInCart(items1, items2, ...items) {
    /*
     * '...' is known as the rest operator when used in function parameters.
     * It allows multiple arguments to be passed and stores them as an array.
     */
    return items;
}

console.log(addElementInCart(200, 400, 800, 300, 1500));
// Output: [800, 300, 1500] - rest of the elements are stored in 'items'.
```

## Passing an Object to a Function

```javascript
const obj = {
    item: "Book",
    price: 300
};

function handleObject(anyObject) {
    console.log(`Your item is ${anyObject.item} and its price is ${anyObject.price}`);
}

handleObject(obj);
handleObject({ item: "Pen", price: 10 });
```

## Passing an Array to a Function

```javascript
const myArray = [12, 24, 36, 48];

function handleArray(anyArray) {
    return anyArray[1]; // Returns the second element of the array
}

console.log(handleArray(myArray)); // Output: 24
console.log(handleArray([200, 400, 800, 1200])); // Output: 400
```

## Function Declarations

### Type 1: Standard Function Declaration

```javascript
function typeOneFunction() {
    return 1;
}
```

### Type 2: Function Expression

```javascript
const typeTwoFunction = function() {
    return 2;
};
```

### Type 3: Arrow Function

```javascript
// Explicit return in an arrow function
const explicitArrowFun = (num1, num2) => {
    return num1 + num2; // Returns the sum of two numbers
};

// Implicit return in an arrow function
const implicitArrowFun = () => 2; // Returns 2
```

## Summary

- **Function Declaration**: Defines a function using the `function` keyword.
- **Function Reference vs Execution**: Referencing a function without `()` does not execute it.
- **Returning Values**: Functions can return values instead of just printing them.
- **Handling Undefined Parameters**: Use conditional checks to handle missing arguments.
- **Default Parameters**: Provide default values to avoid `undefined` errors.
- **Rest Operator**: Allows functions to accept an unknown number of arguments.
- **Passing Objects and Arrays**: Objects and arrays can be passed to functions for flexibility.
- **Different Function Types**: JavaScript supports function declarations, function expressions, and arrow functions.

