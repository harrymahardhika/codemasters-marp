---
marp: true
theme: one
---

# JavaScript Function Scope

---

## Scope Levels

Scope levels dalam JavaScript terdiri terdiri dari 3 level, yaitu:

- Global scope
- Local scope
- Function arguments

---

## Scope Levels: Global scope

Variabel yang dinyatakan di luar fungsi mana pun dapat diakses secara global.

```javascript
const globalVar = "I'm global!";

function hasAccess() {
  console.log(globalVar); // This works!
}

hasAccess(); // Output: I'm global!
```

---

## Scope Levels: Local scope

Variabel yang dinyatakan di dalam fungsi hanya dapat diakses di dalam fungsi tersebut.

```javascript
function localFunction() {
  const localVar = "I'm local!";
  console.log(localVar); // This works!
}

// Cannot access localVar outside the function
console.log(localVar); // This will error!
```

---

## Scope Levels: Argumen fungsi

Argumen yang diteruskan ke fungsi bertindak seperti variabel lokal dalam cakupannya.

```javascript
function addNumbers(a, b) {
  const sum = a + b;
  console.log(`The sum of ${a} and ${b} is: ${sum}`);
}

addNumbers(5, 10); // Output: The sum of 5 and 10 is: 15
console.log(a); // This will error!
console.log(sum); // This will error!
```

---

## Function Relationships:

```javascript
function outerFunction() {
  const outerVar = "I'm outer!";

  function innerFunction() {
    console.log(outerVar); // This works!
  }

  innerFunction();
}

outerFunction(); // Output: I'm outer!
innerFunction(); // This will error!
```

---

## Function Relationships: Nested Functions

```javascript
function outerFunction() {
  const outerVar = "I'm outer!";

  function innerFunction() {
    const innerVar = "I'm inner!";
    console.log(outerVar); // This works!
    console.log(innerVar); // This works!
  }

  innerFunction();
  console.log(outerVar); // This works!
  console.log(innerVar); // This will error!
}
```
