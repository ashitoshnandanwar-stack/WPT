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
### Difference between InnerHTML, InnerText, TextContent
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

## 📌 JSON (JavaScript Object Notation)
```
🔹 What is JSON?
JSON is a lightweight, text-based data interchange format used to exchange data between client and server.
Language independent
Easy to read and write
Easy to parse and generate

👉 Mostly used in AJAX, REST APIs, web services

🔹 JSON Structure
1️⃣ JSON Object
{
  "id": 101,
  "name": "Amit",
  "active": true
}

2️⃣ JSON Array
[
  { "id": 1, "name": "A" },
  { "id": 2, "name": "B" }
]

🔹 JSON Data Types (EXAM FAVORITE)
JSON Type	Example
String	"CDAC"
Number	100, 45.6
Boolean	true, false
Object	{}
Array	[]
null	null

❌ No functions
❌ No comments
❌ No undefined

🔹 JSON Rules (VERY IMPORTANT)
Keys must be in double quotes
Trailing commas not allowed
Case sensitive
Pure data format (no logic)

🔹 JSON vs JavaScript Object (MCQ TRAP)
| Feature       | JSON               | JS Object       |
| ------------- | ------------------ | --------------- |
| Keys          | Double quotes only | Quotes optional |
| Functions     | Not allowed        | Allowed         |
| Comments      | No                 | Yes             |
| Data exchange | Yes                | No              |

🔹 JSON in JavaScript
Convert JSON → JS Object
let obj = JSON.parse(jsonString);

Convert JS Object → JSON
let json = JSON.stringify(obj);


📌 MCQ Line
JSON.parse() converts JSON string to object
JSON.stringify() converts object to JSON string

🔹 JSON with AJAX (WPT Context)
$.get("data.json", function(data) {
  console.log(data.name);
});
```
