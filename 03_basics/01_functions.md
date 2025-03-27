
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

## Summary

- **Function Declaration**: Defines a function using `function` keyword.
- **Function Reference vs Execution**: Referencing a function without `()` does not execute it.
- **Returning Values**: Functions can return values instead of just printing them.
- **Handling Undefined Parameters**: Use conditional checks to handle missing arguments.
- **Default Parameters**: Provide default values to avoid `undefined` errors.

