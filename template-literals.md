# Template Literals

It is recommended to use backticks instead of string concatenation:

```javascript
const name = "Alireza";
const role = "pentester";

// old way
"Hello " + name + ", you work as a " + role;

// template literal
`Hello ${name}, you work as a ${role}`;
```
