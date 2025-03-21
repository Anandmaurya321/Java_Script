# Comparison Operators in JavaScript

## Basic Comparisons
```javascript
console.log(2 > 1); // true
console.log(1 == 2); // false
console.log(5 < 2); // false
```

## Comparisons with null
```javascript
console.log(null > 0);  // false, because null is treated as 0 in comparisons but not in equality
console.log(null >= 0); // true, because null is converted to 0 and 0 >= 0 is true
console.log(null == 0); // false, because == does not convert null to a number
```

## Comparisons with undefined
```javascript
console.log(undefined == 0);  // false, undefined is not equal to any value except itself
console.log(undefined > 0);   // false, undefined cannot be compared meaningfully
console.log(undefined <= 0);  // false, undefined remains undefined in comparisons
```

## Strict Equality Check
```javascript
console.log("2" === 2); // false, because '===' checks both value and data type
```
