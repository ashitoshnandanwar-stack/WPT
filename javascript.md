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

<hr>

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
<hr>


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

<hr>

## 📌 jQuery
```
🔹 What is jQuery?
jQuery is a fast, lightweight JavaScript library that simplifies:
DOM manipulation
Event handling
AJAX
Animations
📌 Motto: “Write less, do more”

🔹 jQuery Syntax
$(selector).action();

Example:
$("#btn").click(function() {
  alert("Clicked");
});

🔹 jQuery Selectors (VERY IMPORTANT)
Basic Selectors
$("#id")  ----- for id
$(".class")  ----- for class
$("p")  ------for tag

Attribute Selector
$("input[type='text']")
```

### jQuery Event
```
✅ Why jQuery Events?
Cross-browser compatibility
Short and clean syntax
Easy event binding & unbinding
Supports event delegation

🔹 Basic Event Syntax
$(selector).eventName(function(){
    // code to execute
});

Example
$("#btn").click(function(){
    alert("Button clicked!");
});

🖱️ Mouse Events
| Event          | Description                  |
| -------------- | ---------------------------- |
| `click()`      | When mouse button is clicked |
| `dblclick()`   | Double click                 |
| `mouseenter()` | Mouse enters element         |
| `mouseleave()` | Mouse leaves element         |
| `hover()`      | Combination of enter + leave |
| `mousedown()`  | Mouse button pressed         |
| `mouseup()`    | Mouse button released        |

⌨️ Keyboard Events
| Event        | Description                  |
| ------------ | ---------------------------- |
| `keydown()`  | Key pressed                  |
| `keyup()`    | Key released                 |
| `keypress()` | Key pressed (character keys) |

📝 Form Events
| Event      | Description         |
| ---------- | ------------------- |
| `submit()` | Form submission     |
| `change()` | Value changed       |
| `focus()`  | Element gets focus  |
| `blur()`   | Element loses focus |


```
$(document).ready(function(){

    $('p').click(function(){
    alert("clicked")
  })

  $('#btn').dblclick(function(){
    alert("clicked on button")
  })
  $('#btn').click(function(){
      console.log("hover")
  })

  $('#btn').mouseenter(function(){
      console.log("hover")
  })

  $('#btn').hover(function(){
      console.log("hover")
  })
  hover = two ho

  Event in jquery
  mouse - click, dblclick, hover


  $('#para').hide(2000);
  $('#para').show(2000);

  $('#btn').click(function(){
      $('#para').hide(12000);
         $('#para').show(12000);
  })


  $('#para').slideUp(2000);
  $('#para').slideDown(2000);
 $('#para').slideToggle(2000);

 $('#para').animate({opacity:0.3}, 3000)
 
 $('#para').css('background-color','red')

$('#btn').click(function(){
 $('#para').css('background-color','red')
})

$('#inp').val('nandanwar');  
 })


 

 ```
