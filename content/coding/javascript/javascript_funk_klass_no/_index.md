---
title: Javascript Klasser og Funksjoner
toc: false
---

# JavaScript Grunnleggende – Oppsummering med Eksempler og Oppgaver

Dette dokumentet oppsummerer grunnleggende konsepter i JavaScript relatert til bruk av klasser, funksjoner, frontend (React) og backend (Node.js), inkludert praktiske eksempler og oppgaver.

---

## 🔁 1. Forskjellen på Node.js og React

| Teknologi   | Hva det er                      | Bruksområde                            |
|-------------|----------------------------------|----------------------------------------|
| **Node.js** | JavaScript-runtime (backend)     | Kjører kode på serveren, lager API-er  |
| **React**   | JavaScript-bibliotek (frontend)  | Lager brukergrensesnitt i nettleseren  |

### 🧪 Eksempel
Node.js server:
```js
app.get('/api/hello', (req, res) => {
  res.json({ message: 'Hei fra backend!' });
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

### ✅ Oppgave
1. Lag et enkelt Express-API med én rute som returnerer `"Velkommen"`.
2. Lag en React-app som henter denne meldingen og viser den på skjermen.

---

## 🧱 2. Hvordan frontend og backend snakker sammen

- React bruker `fetch()` eller `axios` for å hente data.
- Node.js må aktivere CORS for å tillate det:

```js
const cors = require('cors');
app.use(cors());
```

### ✅ Oppgave
1. Legg til CORS i Express.
2. Lag en knapp i React som, når du klikker, henter data fra en `/api/data`-rute.

---

## 🧱 3. Klasser (`class`) i JavaScript

```js
class Bruker {
  constructor(navn, alder) {
    this.navn = navn;
    this.alder = alder;
  }

  siHei() {
    console.log(`Hei, jeg heter ${this.navn}`);
  }
}
```

### ✅ Oppgave
1. Lag en `Bil`-klasse med `merke`, `modell` og `år`.
2. Legg til en metode `beskriv()` som skriver ut informasjon om bilen.
3. Lag to biler og kall metoden på dem.

---

## 🔧 4. Funksjoner (`function`)

```js
function erVoksen(alder) {
  return alder >= 18;
}
```

### ✅ Oppgave
1. Lag en funksjon `regnUtPris(pris, moms)` som returnerer pris med moms.
2. Lag en funksjon `siVelkommen(navn)` som returnerer en tekst: `Velkommen, <navn>`.

---

## 🤝 5. Klasser og funksjoner sammen

```js
class Produkt {
  constructor(navn, pris) {
    this.navn = navn;
    this.pris = pris;
  }
}

function totalPris(produkter) {
  return produkter.reduce((sum, p) => sum + p.pris, 0);
}
```

### ✅ Oppgave
1. Lag en `Kunde`-klasse med `navn` og `handlekurv` (en liste av produkter).
2. Lag en funksjon `beregnTotal(kunde)` som summerer handlekurven.

---

## 🧭 6. Eksport og import

### Eksport av klasse:
```js
export class Person {
  constructor(navn) {
    this.navn = navn;
  }
}
```

### Import:
```js
import { Person } from './Person.js';
```

### ✅ Oppgave
1. Lag en fil `Person.js` med en `Person`-klasse.
2. Eksporter den og importer den i `main.js`.
3. Lag et objekt og kall en metode på det.

---

## ⚡ 7. Arrow Functions

```js
const pluss = (a, b) => a + b;
const hei = navn => `Hei, ${navn}`;
```

### ✅ Oppgave
1. Lag en arrow-funksjon `erLike(a, b)` som returnerer `true` hvis tallene er like.
2. Lag en array med navn, og bruk `map()` med en arrow-funksjon til å skrive ut: `Hei, <navn>`.

---

## 📌 Nøkkelbegreper

| Begrep           | Forklaring                                           |
|------------------|------------------------------------------------------|
| `this`           | Peker på objektet som funksjonen/metoden tilhører   |
| `constructor()`  | Kjøres når du bruker `new` på en klasse              |
| `new`            | Lager et nytt objekt fra en klasse                   |
| `export/import`  | Gjør det mulig å dele kode mellom filer              |

---

*Oppdatert: Juli 2025*
