# Spread/rest

Same ... syntax, opposite direction depending on context:

```javascript
// spread — expand an array/object out
const base = [1, 2, 3];
const combined = [...base, 4, 5]; // [1,2,3,4,5]

const defaults = { timeout: 5000, retries: 3 };
const config = { ...defaults, retries: 5 }; // override one field, keep rest

// rest — gather multiple things into one
const [head, ...rest] = [1, 2, 3, 4]; // head=1, rest=[2,3,4]
```
