---
title: Javascript Classes and Functions
toc: false
---
# JavaScript Fundamentals – Summary with Examples and Exercises

This document summarizes essential JavaScript concepts related to classes, functions, frontend (React), and backend (Node.js), including practical examples and exercises.

---

## 🔁 1. Difference Between Node.js and React

| Technology | What it is                     | Purpose                                  |
|------------|-------------------------------|------------------------------------------|
| **Node.js** | JavaScript runtime (backend)   | Runs server-side code, builds APIs       |
| **React**   | JavaScript library (frontend)  | Builds user interfaces in the browser    |

### 🧪 Example
Node.js server:
```js
app.get('/api/hello', (req, res) => {
  res.json({ message: 'Hello from backend!' });
});
```

React frontend:
```js
useEffect(() => {
  fetch('http://localhost:5000/api/hello')
    .then(res => res.json())
    .then(data => setMessage(data.message));
}, []);
```

### ✅ Exercise
1. Create a simple Express API with one route that returns `"Welcome"`.
2. Create a React app that fetches this message and displays it.

---

## 🧱 2. How Frontend Talks to Backend

- React uses `fetch()` or `axios` to request data.
- Node.js must enable CORS to allow cross-origin access:

```js
const cors = require('cors');
app.use(cors());
```

### ✅ Exercise
1. Add CORS support in Express.
2. Create a button in React that fetches data from a `/api/data` route on click.

---

## 🧱 3. Classes (`class`) in JavaScript

```js
class User {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log(`Hi, my name is ${this.name}`);
  }
}
```

### ✅ Exercise
1. Create a `Car` class with `brand`, `model`, and `year`.
2. Add a `describe()` method that prints the car info.
3. Instantiate two cars and call their method.

---

## 🔧 4. Functions (`function`)

```js
function isAdult(age) {
  return age >= 18;
}
```

### ✅ Exercise
1. Create a function `calculatePrice(price, tax)` that returns total with tax.
2. Create a function `welcome(name)` that returns `Welcome, <name>`.

---

## 🤝 5. Classes and Functions Together

```js
class Product {
  constructor(name, price) {
    this.name = name;
    this.price = price;
  }
}

function totalPrice(products) {
  return products.reduce((sum, p) => sum + p.price, 0);
}
```

### ✅ Exercise
1. Create a `Customer` class with `name` and a `cart` (list of products).
2. Create a function `calculateTotal(customer)` that sums the cart items.

---

## 🧭 6. Export and Import

### Export a class:
```js
export class Person {
  constructor(name) {
    this.name = name;
  }
}
```

### Import:
```js
import { Person } from './Person.js';
```

### ✅ Exercise
1. Create a file `Person.js` with a `Person` class.
2. Export it and import it in `main.js`.
3. Instantiate the class and call a method.

---

## ⚡ 7. Arrow Functions

```js
const add = (a, b) => a + b;
const greet = name => `Hi, ${name}`;
```

### ✅ Exercise
1. Create an arrow function `areEqual(a, b)` that returns `true` if the numbers match.
2. Create an array of names, and use `map()` with an arrow function to print `Hi, <name>`.

---

## 📌 Key Concepts

| Concept         | Explanation                                          |
|------------------|-----------------------------------------------------|
| `this`           | Refers to the object the method/function belongs to |
| `constructor()`  | Runs when using `new` on a class                    |
| `new`            | Creates a new object from a class                   |
| `export/import`  | Allows sharing code across files                    |

---

*Updated: July 2025*
