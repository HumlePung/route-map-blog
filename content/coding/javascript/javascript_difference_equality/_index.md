---
title: Javascript - Difference and equality
description: Learn the difference between =, ==, and === in JavaScript. Understand assignment, loose comparison, and strict comparison.
date: 2025-07-01
tags: [javascript, programmering, webutvikling]
type: coding
toc: false
---

# The Difference Between =, == and === in JavaScript

## 📘 Explanation

| Symbol | Name                 | What it does                                      |
|--------|----------------------|---------------------------------------------------|
| `=`    | Assignment           | Assigns a value to a variable                     |
| `==`   | Loose equality       | Compares values after converting types if needed |
| `===`  | Strict equality      | Compares both value **and** type exactly         |

---

## 🧪 Examples

```js
let x = 5;        // Assignment
console.log(x);   // 5

console.log('5' == 5);   // true (string converted to number)
console.log('5' === 5);  // false (different types)

console.log(null == undefined);  // true
console.log(null === undefined); // false

console.log(true == 1);   // true
console.log(true === 1);  // false
```

---

## ✅ Exercises

### Exercise 1
What is the result?

```js
let a = '10';
let b = 10;

console.log(a == b);   // ?
console.log(a === b);  // ?
```

### Exercise 2
Explain the difference:

```js
console.log(false == 0);   // ?
console.log(false === 0);  // ?
```

### Exercise 3
Create an example where `==` returns `true` and `===` returns `false`.

---

*Updated: July 2025*
