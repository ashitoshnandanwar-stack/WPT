# JavaScript

| Topic          | Correct Fact    |
| -------------- | --------------- |
| JS comment     | `//`            |
| Character type |  Not in JS      |
| Message box    | `alert()`       |
| JS execution   | Browser         |
| Root object    | `Object`        |
| JSON → object  | `JSON.parse()`  |
| Property check | `in`            |
| Array → string | `join()`        |
| Inheritance    | Prototype-based |
| `let` scope    | Block           |
| Async handling | Promise         |
| NaN            | Not a Number    |

## DOM (Document Object Model)
### What is DOM?
- DOM is a tree-like representation of a web page that allows JavaScript to manipulate HTML and CSS.

```
🧱 DOM Structure (Tree Model)
  Document → root
  Elements → tags (<html>, <body>, <p>)  
  Attributes → id, class
  Text nodes → text inside tags

🎯 Why DOM is Important?
  Change content without reloading page
  Handle user events (click, input)
  Build interactive web apps (SPA)
```
| Method                     | Use                        |
| -------------------------- | -------------------------- |
| `getElementById()`         | Select by id               |
| `getElementsByClassName()` | Select by class            |
| `getElementsByTagName()`   | Select by tag              |
| `querySelector()`          | First match (CSS selector) |
| `querySelectorAll()`       | All matches                |

| Property      | Meaning           |
| ------------- | ----------------- |
| `innerHTML`   | HTML + text       |
| `textContent` | Text only (safer) |

🖱️ DOM Events
| Event       | Trigger     |
| ----------- | ----------- |
| `click`     | Mouse click |
| `mouseover` | Hover       |
| `keydown`   | Key press   |
| `submit`    | Form submit |
| `load`      | Page load   |
