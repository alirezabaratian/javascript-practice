# Truthy-Falsy

Only 8 falsy values in JS: false, 0, -0, 0n, "", null, undefined, NaN. Everything else — including "0", [], {} — is truthy. This trips people up constantly:

```javascript
if ([]) console.log("runs");   // yes, empty array is truthy
if ("0") console.log("runs");  // yes, non-empty string is truthy
if (0) console.log("runs");    // no
```
