# 1. Core JavaScript Concepts

## 1.1 Closures

**Questions**

- What is a closure in JavaScript?
- Explain closure with an example.
- What does lexical scope mean?

Example:

```javascript
function outer() {
  let count = 0;

  return function inner() {
    count++;
    console.log(count);
  };
}

const counter = outer();
counter(); // 1
counter(); // 2
```

Topics covered:

- Scope chain
- Lexical environment
- Data encapsulation

---

# 2. Array Manipulation

## Flatten an Array with Depth

Implement a function to flatten an array where the **user can define the depth level**.

Example:

```javascript
flatten([1, [2, [3, 4]]], 1);
// [1,2,[3,4]]

flatten([1, [2, [3, 4]]], 2);
// [1,2,3,4]
```

Concepts tested:

- Recursion
- Depth control
- Array traversal

---

## Array Set Operations

Questions based on:

- Union
- Intersection
- Symmetric Difference
- Remove duplicates
- First occurrence
- Find index

Example:

```javascript
const arr1 = [1, 2, 3];
const arr2 = [2, 3, 4];

intersection(arr1, arr2);
// [2,3]
```

---

# 3. Object Manipulation

## Flatten an Object

Convert nested objects into a flattened structure.

Example:

```javascript
const obj = {
  a: {
    b: {
      c: 1,
    },
  },
};
```

Output:

```javascript
{
  "a.b.c": 1
}
```

---

## Object Behaviour Questions

Topics included:

- Shallow Copy
- Deep Copy
- `Object.assign()`
- `Object.create()`
- `Object.freeze()`
- `Object.seal()`
- Copy by Reference
- Copy by Value

Example:

```javascript
const obj1 = { a: 1 };
const obj2 = obj1;

obj2.a = 10;

console.log(obj1.a);
```

Expected understanding:

- Memory references
- Object mutation

---

# 4. JavaScript Execution Model

Deep conceptual questions about **how JavaScript executes code internally**.

Topics included:

- Execution Context
- Memory Phase
- Execution Phase
- Call Stack
- Event Loop
- Browser APIs
- Macro Task Queue
- Microtask Queue

Example:

```javascript
console.log("Start");

setTimeout(() => {
  console.log("Timeout");
}, 0);

Promise.resolve().then(() => {
  console.log("Promise");
});

console.log("End");
```

---

# 5. Asynchronous Output Questions

Example:

```javascript
console.log(1);

setTimeout(() => console.log(2));

Promise.resolve().then(() => console.log(3));

console.log(4);
```

Expected Output:

```
1
4
3
2
```

---

# 6. Performance Optimization

## Debouncing

Explain **debouncing with example**.

Use cases:

- Search input API calls
- Resize events

---

## Throttling

Explain **throttling with example**.

Common use cases:

- Scroll events
- Button clicks

---

## Memoization

Implement a **memoized function**.

Example:

```javascript
function memoize(fn) {
  const cache = {};

  return function (n) {
    if (cache[n]) return cache[n];

    const result = fn(n);
    cache[n] = result;
    return result;
  };
}
```

---

# 7. Higher Order Functions

A **Higher Order Function** is a function that:

- Takes another function as an argument
- Returns another function

---

# 8. JavaScript Polyfills

Implement custom polyfills for common JavaScript methods.

## Array Polyfills

- `Array.map`
- `Array.reduce`
- `Array.filter`

## Function Polyfills

- `call`
- `apply`
- `bind`

## Promise Polyfills

- `Promise.all`
- `Promise.any`
- `Promise.allSettled`
- `Promise.race`
- `Promise.finally`

These implementations should be done **without using built-in implementations**.

---

# 9. Lazy Man Problem

Implement the **Lazy Man pattern**.

Example:

```javascript
LazyMan("Amit").eat("Dinner").sleep(5).eat("Dessert");
```

Concepts tested:

- Async task scheduling
- Promise chaining
- Queue based execution

---

# 10. Custom Utility Functions

## Custom Object.assign

Write your own implementation of:

```javascript
Object.assign(target, source);
```

---

## Deep Clone Function

Implement a **deep clone utility** without using libraries.

Requirements:

- Support nested objects
- Support arrays

---

# 11. DOM Event System

Questions based on the **DOM Event Flow**.

Topics covered:

- Event Propagation
- Event Delegation
- Event Capturing
- Event Bubbling

Example:

```javascript
event.stopPropagation();
```

Possible interview questions:

- What is event delegation?
- How does event propagation work?
- How can we prevent event bubbling?

---

# 12. Arrow Functions and `this`

Example:

```javascript
const obj = {
  name: "JS",
  say() {
    console.log(this.name);
  },
};
```

Topics included:

- Arrow vs normal functions
- `this` binding behavior
- Output-based questions

---

# 13. ES6+ Features

Topics related to modern JavaScript:

- `let` / `const`
- Spread operator
- Rest operator
- Destructuring
- Template literals
- Modules

---

# 14. Generators

Explain **generator functions**.

Example:

```javascript
function* generator() {
  yield 1;
  yield 2;
  yield 3;
}
```

Concepts covered:

- `yield`
- Iterators
- Controlled execution

---

# 15. Factory Functions

Explain **factory functions** and how they differ from constructor functions.

Example:

```javascript
function createUser(name) {
  return {
    name,
    greet() {
      console.log("Hello " + name);
    },
  };
}
```

---

# 16. Data Transformation Coding Questions

## Question 1 – Aggregate Object Values

Input:

```javascript
const fruitsArray = [
  { apple: 1, orange: 1, banana: 3, grapes: 5 },
  { apple: 4, orange: 3, grapes: 1 },
  { apple: 2, orange: 6, banana: 7 },
];
```

Output:

```javascript
{
 apple:7,
 orange:10,
 banana:10,
 grapes:6
}
```

Concepts tested:

- Object iteration
- Aggregation
- Data transformation

---

## Question 2 – Group By Property

Input:

```javascript
const arr = [
  { type: "fruit", name: "apple" },
  { type: "fruit", name: "banana" },
  { type: "veg", name: "carrot" },
];
```

Output:

```javascript
{
 fruit:["apple","banana"],
 veg:["carrot"]
}
```

Concepts tested:

- Object grouping
- Reduce based transformation

---

# Summary

The interview mainly evaluated the following areas:

## JavaScript Core Depth

- Closures
- Execution context
- Event loop
- Async behavior

## Coding Skills

- Array manipulation
- Object manipulation
- Utility functions

## DOM Knowledge

- Event propagation
- Event delegation

## Advanced Topics

- Memoization
- LazyMan pattern
- Generator functions

## 5. JavaScript Function Design – Function Chaining

Write a JavaScript function `Add` such that every function call returns the **sum of all numbers passed across chained calls**.

### Example Calls

```javascript
Add(1, 2)(3, 4, 5, 6)(1)(6, 8, 3, 4, 5, 6);
Add(1, 2, 5, 6, 7)(5, 6)(1, 7, 8)(6, 8, 5, 6);
Add(1)(3, 4, 5, 6, 9, 11, 23)(1, 11, 111)(66);
Add(1, 2, 5, 6, 7, 8)(3)(1)(6);
```

### Problem Requirement

- Each function call can receive **multiple numbers**.
- Calls are **chained**.
- The function should **accumulate all numbers across all calls**.
- The final result should be the **sum of all numbers passed**.

### Example

```javascript
Add(1, 2)(3, 4)(5);
```

### Expected Output

```
15
```

---

## 6. Follow-Up Question – Dynamic Function Calls

Modify the previous problem with the following changes:

### Requirements

- The number of chained function calls should be **dynamic**.
- The chain should **terminate when an empty call `()` is made**.
- The function should return the **sum of all numbers passed before the empty call**.

### Example Calls

```javascript
Add(1, 2)(3, 4)(5, 6)();
Add(10)(20)(30)(40)(50)();
```

### Expected Output

```
Add(1,2)(3,4)(5,6)() -> 21
Add(10)(20)(30)(40)(50)() -> 150
```

---

## 7. Custom Array Method – Implement `myFlat()`

Implement a custom method `myFlat()` that **flattens a nested array**.

### Example Input

```javascript
[1, [3, 4, [5, 6, 7], 11], 102].myFlat();
```

### Expected Output

```javascript
[1, 3, 4, 5, 6, 7, 11, 102];
```

### Requirements

- The function should **flatten nested arrays recursively**.
- It should work for **arrays of any depth**.

---

## 8. Design Pattern – Singleton Pattern

- Design a **Singleton class** in JavaScript.

### Requirements

- Only **one instance** of the class should ever be created.
- Multiple calls to create an instance should **return the same instance**.
- Prevent **direct instantiation from outside** if possible.

### Example Usage

```javascript
const instance1 = Singleton.getInstance();
const instance2 = Singleton.getInstance();

console.log(instance1 === instance2);
```

### Expected Output

```
true
```

- Both variables should reference the **same instance of the class**.

## 10. JavaScript Function Chaining – Calculator Executor

Write a JavaScript utility that supports **method chaining** like the following:

```javascript
exec().add(1, 2).multiply(45, 5).divide(12, 3);
```

### Requirements

- The function should support **method chaining**.
- Each method should **perform its operation and accumulate the result**.
- The final result should be returned when `.value()` (or similar) is called.
- Supported operations:
  - `add`
  - `multiply`
  - `divide`

---

### Example Usage

```javascript
exec().add(1, 2).multiply(45, 5).divide(12, 3).value();
```

### Expected Output

```
114.75
```
