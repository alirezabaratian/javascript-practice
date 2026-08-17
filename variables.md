# Variables

## Variable Types

```javascript
var x = 1;      // function-scoped, hoisted weirdly - avoid
let y = 2;      // block-scoped, reassignable
const z = 3;    // block-scoped, can't be reassigned
```

## Why Var Is Dangerous

```javascript
if (true) {
  var a = 1;
  let b = 2;
}
console.log(a); // 1 — leaked out of the block
console.log(b); // ReferenceError — stayed inside the block
```

**Rule of thumb:** use const by default, let when you need to reassign, never var.

**Note:** const doesn't mean immutable — it means the binding can't be reassigned:

```javascript
const arr = [1, 2, 3];
arr.push(4);      // fine — mutating contents
arr = [5, 6];      // TypeError — reassigning the variable itself
```
