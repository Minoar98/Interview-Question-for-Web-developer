# JavaScript & React Concepts

## 1. What is Higher Order Component in React JS?
A **Higher Order Component (HOC)** is a function that takes a component and returns a new component with additional capabilities. HOCs are used to reuse component logic.

**Example:**
```jsx
function withLogger(WrappedComponent) {
  return function EnhancedComponent(props) {
    console.log('Props:', props);
    return <WrappedComponent {...props} />;
  }
}
```

## 2. Shadow DOM vs Virtual DOM

| Feature        | Shadow DOM                        | Virtual DOM                     |
|----------------|-----------------------------------|----------------------------------|
| Definition     | A browser technology to encapsulate DOM and styles | A programming concept used by React to optimize DOM rendering |
| Scope          | Encapsulated (isolated from main DOM) | Not encapsulated, simulates full DOM in memory |
| Used by        | Web Components                    | React, Vue (frameworks)         |
| Purpose        | Style and structure encapsulation | Efficient UI updates            |

## 3. How `map()` Function Works in JavaScript?
The `map()` function creates a new array by applying a function to each element of the original array.

**Example:**
```javascript
const numbers = [1, 2, 3];
const squared = numbers.map(num => num * num); // [1, 4, 9]
```

## 4. What is Event Loop in JavaScript?
The **Event Loop** is a mechanism in JavaScript that handles asynchronous operations. It continuously checks the call stack and the task queue, executing tasks in a non-blocking way.

**Main Components:**
- Call Stack
- Web APIs (e.g., setTimeout, fetch)
- Callback Queue / Task Queue
- Event Loop

**Example:**
```javascript
console.log('Start');
setTimeout(() => console.log('Timeout'), 0);
console.log('End');
// Output: Start, End, Timeout
```

## 5. How to Get Elements from HTML Pages?
You can use DOM methods like:
```javascript
document.getElementById("id")
document.getElementsByClassName("class")
document.getElementsByTagName("tag")
document.querySelector("selector")
document.querySelectorAll("selector")
```

## 6. Given Two Strings, Output the Common Characters
```javascript
function commonCharacters(str1, str2) {
  const set1 = new Set(str1);
  const set2 = new Set(str2);
  const common = [...set1].filter(char => set2.has(char));
  return common;
}

console.log(commonCharacters("hello", "world")); // ['l', 'o']
```