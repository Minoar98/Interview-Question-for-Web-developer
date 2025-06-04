
## JavaScript Core Concepts

### 1. Difference between Method & Function
- **Function**: A block of code that performs a task and can be called independently.
- **Method**: A function that is a property of an object.

### 2. What is a Higher Order Function?
- A function that either takes another function as an argument or returns a function.

### 3. Difference between `??` and `||`
- `??` (Nullish Coalescing): Returns the right-hand operand only if the left-hand operand is `null` or `undefined`.
- `||` (Logical OR): Returns the right-hand operand if the left-hand operand is **falsy** (e.g. `0`, `''`, `null`, `undefined`, `false`, `NaN`).

### 4. Code Output:
```js
const ar = ['apple', 'orange', 'kiwi'];
console.log(ar.shift());
// Output: 'apple'
```

### 5. Use of `...` (Spread Syntax)
Used to copy arrays, combine arrays, or spread iterable values:
```js
const arr1 = [1, 2];
const arr2 = [...arr1, 3, 4];
console.log(arr2); // [1, 2, 3, 4]
```

### 6. Fetch First & Fifth Element using ES6
```js
const arr = [1, 2, 3, 4, 5];
const [first, , , , fifth] = arr;
console.log(first, fifth); // 1 5
```

### 7. Falsy Values in JavaScript
- `undefined`
- `NaN`
- `""`
- `null`
- `0`
- `false`
Total: **6 falsy values**

### 8. `14 + 2 + 'JS' + 4`
- Evaluates as: `16 + 'JS'` = `'16JS' + 4` = `'16JS4'`
- Output: `'16JS4'`

### 9. Difference between `undefined` vs `null`
- `undefined`: Variable is declared but not assigned.
- `null`: Value is explicitly set to indicate "no value".

### 10. When to Use `==` vs `===`
- `==` checks for value equality with type coercion.
- `===` checks for both value and type equality.
```js
console.log(null == undefined);  // true
console.log(null === undefined); // false
```

### 11. Output of `"Hello" - "World"`
- Output: `NaN`

### 12. Describe `const x = x => x`
- This is an arrow function that returns whatever is passed to it.
- Identity function.

### 13. If You Want to Use `var` Instead of `let` & `const`
- It's **not recommended** due to `var`'s function scoping.
- If needed, use `var`, but understand the scoping limitations.

### 14. Fix the Bug in Code:
```js
const person = {
    name: 'Ronaldo',
    jerseyNo: 7
}
const { name, jerseyNo: jerseyNumber } = person;
console.log(jerseyNumber); // 7
```

### 15. Destructuring a String:
```js
let name = "W3Schools";
let [a1, a2, a3, a4, a5] = name;
console.log(a2); // '3'
```

### 16. Output with Rest Syntax:
```js
let name = "W3Schools";
let [a1, a2, a3, a4, ...a5] = name;
console.log(a5); // ['c', 'h', 'o', 'o', 'l', 's']
```

### 17. Describe `{ x }`
- Destructuring object syntax. Extracts variable `x` from object `{ x: value }`

### 18. What is an Operator?
- Operators perform operations on variables/values (e.g., `+`, `-`, `==`, `===`).

### 19. What is an Array?
- A collection of ordered elements.
- Used to store multiple values in a single variable.

### 20. `x++` vs `++x`
- `x++`: Post-increment, returns the value before increment.
- `++x`: Pre-increment, returns the value after increment.

### 21. Scope Example:
```js
function varAndLetScoping() {
  var x = 1;
  if (true) {
    let x = 2;
    console.log(x); // 2
  }
  console.log(x); // 1
}
```

### 22. What is Coercion in JavaScript?
- Automatic or implicit conversion of values from one data type to another (e.g., number to string).

### 23. Summary of Key Points
- Understand scope (`var`, `let`, `const`)
- Know falsy values
- Use destructuring and spread syntax efficiently
- Be careful with type coercion and equality operators
