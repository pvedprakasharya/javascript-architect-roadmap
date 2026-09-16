# Variables, Scope, and Bindings in JavaScript

A comprehensive reference for understanding **variable declarations, scope rules, bindings, and hoisting** in JavaScript.  
Includes **code snippets, interview-style Q&A, and best practices**.

---

## 📌 Variable Declarations

### Difference between `var`, `let`, and `const`

**Answer**  
- `var` → Function-scoped, hoisted, allows redeclaration, can be reassigned.  
- `let` → Block-scoped, hoisted but in TDZ, cannot be redeclared in same scope, can be reassigned.  
- `const` → Block-scoped, hoisted but in TDZ, must be initialized, cannot be reassigned.

**Example**
```js
var a = 1;
let b = 2;
const c = 3;

a = 10;   // ✅ allowed
b = 20;   // ✅ allowed
c = 30;   // ❌ TypeError: Assignment to constant variable
