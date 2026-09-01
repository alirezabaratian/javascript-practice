# Destructuring

Pulling values out of arrays/objects into named variables.

```javascript
// object destructuring
const widget = { id: "github", title: "GitHub Activity", tag: "api" };
const { id, title } = widget;
// id = "github", title = "GitHub Activity"

// rename while destructuring
const { id: widgetId } = widget;

// with a default value
const { retries = 3 } = config;

// array destructuring
const [first, second] = ["nmap", "burp"];

// skip elements
const [, , third] = ["a", "b", "c"]; // third = "c"

// function parameters — extremely common in real code
function renderWidget({ id, title }) {
  return `<div id="${id}">${title}</div>`;
}
```
