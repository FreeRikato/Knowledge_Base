> Allow JavaScript code to be organized into separate files, known as modules
  - Modularity
  - Export and Import
  - Strict mode
  - Named and Default exports:
    = Named Exports: Allow multiple exports which should be imported with the same name
    = Default Exports: Allow a single export which can be imported with any name

```JavaScript
// Named exports
export const pi = 3.14159;
export function add(a, b) {
  return a + b;
}

// Default export
export default function subtract(a, b) {
  return a - b;
}

// In another file,
import subtract, { pi, add } from './math.js';

console.log(pi); // 3.14159
console.log(add(2, 3)); // 5
console.log(subtract(5, 2)); // 3
```
- [!] Be aware that type should be set as `module` in HTML tag of `script`
```html
<script type="module" src="main.js"></script>
```
