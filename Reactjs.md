# React 

| Feature          | Props          | State          | Context       |
| ---------------- | -------------- | -------------- | ------------- |
| Mutability       | Read-only      |  Mutable       |  Mutable      |
| Scope            | Parent → Child | Local          | Global        |
| Used for         | Data passing   | Component data | App-wide data |
| Causes re-render | Yes            | Yes            | Yes           |

## Key difference between js and react
| JavaScript (HTML)         | React                         |
| ------------------------- | ----------------------------- |
| `onclick="handleClick()"` | `onClick={handleClick}`       |
| Event names are lowercase | Event names are **camelCase** |
| String event handlers     | Function references           |

## Event handling

1.🔹 Basic Event Handling Example
```
✅ Button Click
function ClickExample() {
  function handleClick() {
    alert("Button clicked!");
  }

  return (
    <button onClick={handleClick}>
      Click Me
    </button>
  );
}
export default ClickExample;

🔑 Important
❌ onClick={handleClick()} → wrong (executes immediately)
✅ onClick={handleClick} → correct (passes function reference)
```

2.🔹 Using Arrow Functions
```
<button onClick={() => alert("Hello React!")}>
  Click Here
</button>

✔ Useful when passing arguments
❌ Avoid heavy logic inside JSX
```

3. 🔹 Passing Arguments to Event Handlers
```
function Greeting() {
  function sayHello(name) {
    alert(`Hello, ${name}`);
  }

  return (
    <button onClick={() => sayHello("Ashitosh")}>
      Say Hello
    </button>
  );
}
```

4.🔹 Handling Events with State
```
import { useState } from "react";

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>
        Increment
      </button>
    </>
  );
}

📌 Events often update state, which causes re-rendering.
```

5. 🔹 Handling Form Events
```
✅ Input Change Event
function FormExample() {
  const [name, setName] = useState("");
  return (
    <input
      type="text"
      value={name}
      onChange={(e) => setName(e.target.value)}
    />
  );
}


✅ Form Submit Event
function SubmitForm() {
  function handleSubmit(e) {
    e.preventDefault(); // stops page reload
    alert("Form submitted");
  }

  return (
    <form onSubmit={handleSubmit}>
      <button type="submit">Submit</button>
    </form>
  );
}
```

6.🔹 Synthetic Events (Important for Exams)
```
React uses Synthetic Events, which:
Are cross-browser compatible
Wrap native browser events
Have the same interface as DOM events

Example:
function showEvent(e) {
  console.log(e.type); // click
}
```

| Event         | Use             |
| ------------- | --------------- |
| `onClick`     | Mouse click     |
| `onChange`    | Input change    |
| `onSubmit`    | Form submission |
| `onMouseOver` | Mouse hover     |
| `onKeyDown`   | Keyboard input  |
