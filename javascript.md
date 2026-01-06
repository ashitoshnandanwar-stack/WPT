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

## how to access ?
- using id, class, tagname
- using getElementById, getElementByClassName, getElementByTagName
- using  querySelectory, querySelectoryAll = in that #-for id, .-for class
## how to update 
- using getElementById and innerHTML
```
  let p = document.getElementById('fpara');
undefined
p.inert
false
p.innerHTML
'First paragraph'
p.innerHTML = "update paragraph";
'update paragraph'
p.innerHTML
'update paragraph'
```

- using quryselector and innerhtml
```
let a = document.querySelector('#fheading');
undefined
a.innerHTML = "update heading";
'update heading
```

| Feature              | **innerHTML**   | **innerText**     | **textContent**             |
| -------------------- | --------------- | ----------------- | --------------------------- |
| Returns              | HTML + text     | Visible text only | All text (including hidden) |
| Reads HTML tags      |  Yes            |  No               |  No                         |
| Interprets tags      |  Yes            |  No               |  No                         |
| Includes hidden text |  No             |  No               |  Yes                        |
| Affected by CSS      |  No             |  Yes              |  No                         |
| Performance          | Slower          | Slowest           | Fastest                     |
| Security risk        |  XSS possible   | Safe              | Safe                        |

### how to append child
```
let bodyTag = document.querySelector('body');
undefined
bodyTag
<body>​…​</body>​
let head = document.createElement('h1');
undefined
head
<h1>​</h1>​
head.textContent = "my name is ashitosh";
'my name is ashitosh'
head
<h1>​my name is ashitosh​</h1>​
bodyTag.appendChild('head');
```
