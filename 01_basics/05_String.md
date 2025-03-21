# JavaScript Data Types

## String Operations and Methods

### String Concatenation (Outdated Method)
```javascript
let s1 = "Hello ";
let s2 = " Anand";
let num = 1;
console.log(s1 + num + s2); // Hello 1 Anand
```

### String Interpolation (Modern Way)
```javascript
console.log(`My name is ${s2}. My serial no. is ${num}.`);
console.log(`My surname is ${s1}. My serial number is ${num}.`);
```

### Creating a String Object
```javascript
const newstring = new String('Anand Maurya');
console.log(newstring);
```
#### Output in Console:
```
String {'Anand Maurya'}
0: "A"
1: "n"
2: "a"
3: "n"
4: "d"
5: " "
6: "M"
7: "a"
8: "u"
9: "r"
10: "y"
11: "a"
length: 12
[[Prototype]]: String
[[PrimitiveValue]]: "Anand Maurya"
```

### Accessing Characters in a String
```javascript
console.log(newstring[0]); // A
console.log(newstring[4]); // d
```

## String Functions

### Convert to Uppercase
```javascript
console.log(newstring.toUpperCase()); // ANAND MAURYA
```

### Finding Character at an Index
```javascript
console.log(newstring.charAt(2)); // a
```

### Finding Index of a Character
```javascript
console.log(newstring.indexOf('t')); // -1 (not present)
console.log(newstring.indexOf('n')); // 1 (first occurrence)
```

### Extracting Substrings
```javascript
const substring1 = newstring.substring(0, 6); // Does not include index 6
console.log(substring1); // Anand
```

### Slicing a String (Supports Negative Indexing)
```javascript
const substring2 = newstring.slice(-1, 7);
console.log(substring2); // (Empty string, as -1 is before 7)
```
#### Explanation of Slicing:
- `slice(start, end)` extracts part of a string from `start` to `end-1`.
- If `start` is negative, it is counted from the end of the string.
- If `end` is omitted, slicing goes to the end of the string.
- If `start` is greater than `end`, it returns an empty string.
```javascript
const str = "Hello World";
console.log(str.slice(0, 5)); // "Hello"
console.log(str.slice(-5));  // "World"
console.log(str.slice(-1, 7)); // "" (empty string, -1 is before 7)
```

### Trimming Whitespace
```javascript
const name1 = "      Anand      ";
console.log(name1);       // "      Anand      "
console.log(name1.trim()); // "Anand"
```

### Replacing Parts of a String
```javascript
const url = "https://anand20%maurya.com";
console.log(url.replace('20%', '_')); // "https://anand_maurya.com"
```

### Checking for Substring
```javascript
console.log(url.includes('anand')); // true
console.log(url.includes('sundaram')); // false
```

### Splitting a String
```javascript
const para = "My name is Anand maurya. I am pursuing B-tech. It is my second Year";  
const words = para.split(' '); // Splitting on spaces
console.log(words[3]); // Anand
console.log(words[2]); // is
console.log(words[12]); // Year
console.log(words);

const sentences = para.split('.'); // Splitting on full stops
console.log(sentences[0]); // "My name is Anand maurya"
console.log(sentences[1]); // " I am pursuing B-tech"
console.log(sentences[2]); // " It is my second Year"
console.log(sentences);
```
