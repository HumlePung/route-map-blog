---
title: Javascript Forskjell og Likhet
description: Lær forskjellen mellom =, == og === i JavaScript. Forstå tildeling, løs sammenligning og strict sammenligning.
date: 2025-07-01
tags: [javascript, programmering, webutvikling]
type: coding
toc: false
---

# Forskjellen mellom =, == og === i JavaScript

## 📘 Forklaring

| Symbol | Navn               | Hva det gjør                                  |
|--------|--------------------|-----------------------------------------------|
| `=`    | Tildeling          | Brukes for å tildele en verdi til en variabel |
| `==`   | Løs sammenligning  | Sjekker om verdiene er like, konverterer typer automatisk |
| `===`  | Strict sammenligning | Sjekker om både verdi **og** datatype er like |

---

## 🧪 Eksempler

```javascript
let x = 5;        // Tildeling
console.log(x);   // 5

console.log('5' == 5);   // true (fordi '5' konverteres til tall)
console.log('5' === 5);  // false (forskjellig type)

console.log(null == undefined);  // true
console.log(null === undefined); // false

console.log(true == 1);   // true
console.log(true === 1);  // false
```

---

## ✅ Oppgaver

### Oppgave 1
Hva er resultatet?

```javascript
let a = '10';
let b = 10;

console.log(a == b);   // ?
console.log(a === b);  // ?
```

### Oppgave 2
Forklar forskjellen:

```javascript
console.log(false == 0);   // ?
console.log(false === 0);  // ?
```

### Oppgave 3
Lag et eksempel der `==` gir `true` og `===` gir `false`.

---

*Oppdatert: Juli 2025*
