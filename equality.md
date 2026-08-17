# Equality

== does type coercion before comparing. === doesn't. Always use === unless you have a specific reason not to:

```javascript
0 == false        // true  — coerced
0 === false       // false — different types
"5" == 5          // true  — coerced
"5" === 5         // false
null == undefined // true  — special case
null === undefined // false
```
