# Array Methods

`map`, `filter`, `reduce`:

```javascript
const ports = [22, 80, 443, 8080, 3306];

// map — transform each item, same length out
const labeled = ports.map(p => `port ${p}`);

// filter — keep items that pass a test, shorter (or equal) length out
const webPorts = ports.filter(p => p === 80 || p === 443);

// reduce — collapse the array into a single value
const total = ports.reduce((sum, p) => sum + p, 0);
```

`reduce` is the one people find confusing. Think of it as: "start with an initial value, then update it once per item.":

```javascript
// count how many ports are "risky" vs not
const grouped = ports.reduce((acc, p) => {
  const key = p === 22 ? "risky" : "normal";
  acc[key] = (acc[key] || 0) + 1;
  return acc;
}, {}); // {} is the starting value for `acc`
// { risky: 1, normal: 4 }
```

Chaining them is idiomatic:

```javascript
ports.filter(p => p > 1000).map(p => `high port: ${p}`);
```
