

# JavaScript Objects

## What is an Object in JavaScript?
An object is a collection of key-value pairs where the keys are strings (or Symbols) and the values can be of any data type.

---

## Object Creation Methods

### 1. Object Literals
An object literal is the simplest way to create an object.
```javascript
const person = {
  name: "John",
  age: 30
};
```

### 2. Object Constructor
Objects can be created using the `new Object()` constructor.
```javascript
const person = new Object();
person.name = "John";
person.age = 30;
```

### 3. Constructor Function
```javascript
function Person(name, age) {
  this.name = name;
  this.age = age;
}
const person1 = new Person("Alice", 25);
```

### 4. Class Syntax
```javascript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
}
const person2 = new Person("Bob", 28);
```

---

## Important Object Methods
### `hasOwnProperty()`
Checks if an object has a specific property.
```javascript
const obj = { name: "John" };
console.log(obj.hasOwnProperty("name")); // true
```

### `isPrototypeOf()`
Checks if an object exists in the prototype chain of another object.
```javascript
function Person() {}
const person = new Person();
console.log(Person.prototype.isPrototypeOf(person)); // true
```

### `propertyIsEnumerable()`
Checks if a property is enumerable.
```javascript
const obj = { name: "Alice" };
console.log(obj.propertyIsEnumerable("name")); // true
```

### `toLocaleString()`
Returns a locale-sensitive string representation of an object.
```javascript
const date = new Date();
console.log(date.toLocaleString());
```

### `toString()`
Returns a string representation of an object.
```javascript
const num = 42;
console.log(num.toString()); // "42"
```

### `valueOf()`
Returns the primitive value of an object.
```javascript
const numObj = new Number(10);
console.log(numObj.valueOf()); // 10
```

---

## Object vs Constructor Example
### Object Literal:
```javascript
const car1 = {
  brand: "Toyota",
  model: "Camry"
};
```
### Constructor Function:
```javascript
function Car(brand, model) {
  this.brand = brand;
  this.model = model;
}
const car2 = new Car("Honda", "Civic");
```

---

## Summary
- Objects can be created using literals, constructors, functions, and classes.
- `hasOwnProperty()`, `isPrototypeOf()`, and `propertyIsEnumerable()` help check properties.

- `toLocaleString()`, `toString()`, and `valueOf()` convert objects to strings or primitive values.




