
## JavaScript Notes

### Immediately Invoked Function Expressions (IIFE)

IIFE is used to execute a function immediately after its declaration and helps in avoiding global scope pollution.

#### Example of a Regular Function
```js
function chai() {
    console.log("Database Connected!");
}
chai(); // Calling the function manually
```

#### Named IIFE
```js
(function chai() { // Named IIFE
    console.log("Database Connected!");
})();
```

- The first `()` contains the function.
- The second `()` executes the function immediately.
- A semicolon `;` is required at the end to prevent issues when writing multiple IIFEs.

#### Anonymous IIFE
```js
(() => {
    console.log("Database Two connected");
})();
```

#### Passing Parameters in IIFE
```js
((name) => {
    console.log(`Hello ${name}`);
})("Anand");
