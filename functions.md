# Functions

Declerations vs arrow functions:

```javascript
// declaration — hoisted, has its own `this`
function greet(name) {
  return `hi ${name}`;
}

// arrow function — not hoisted, inherits `this` from surrounding scope
const greet2 = (name) => `hi ${name}`;
```

Default parameters and rest parameters:

```javascript
function scan(target, timeout = 5000) { ... }  // default value

function logAll(...args) {  // rest — gathers extra args into an array
  console.log(args);
}
logAll(1, 2, 3); // [1, 2, 3]
```
