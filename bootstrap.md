# BootStrap


## 🅱️ Overview of Bootstrap

*🔧 Why We Need to Use Bootstrap?*
```

📱 Responsive Design
Automatically adjusts layout for:
Desktop
Tablet
Mobile

⚡ Fast Development
No need to design from scratch
Use pre-built components

🎨 Consistent UI
Same look across all browsers
Professional appearance

🧩 Built-in Components
Navbar
Forms
Buttons
Cards
Alerts
Modals

🌍 Cross-Browser Support
Works well on:
Chrome
Firefox
Edge
Safari
```
<hr>

*🧱 Bootstrap Grid System*
```
The Bootstrap Grid System is used to create responsive page layouts.
It is based on a 12-column structure and works with rows and columns.

It helps your page automatically adjust for:
Desktop
Tablet
Mobile
```
📊 Grid Classes
- Bootstrap provides different column classes for different screen sizes:
  
| Class Prefix | Device                |
| ------------ | --------------------- |
| `col-`       | Extra small (default) |
| `col-sm-`    | Small (≥576px)        |
| `col-md-`    | Medium (≥768px)       |
| `col-lg-`    | Large (≥992px)        |
| `col-xl-`    | Extra large (≥1200px) |

Example
```
<div class="row">
  <div class="col-12 col-md-6 col-lg-4">Box 1</div>
  <div class="col-12 col-md-6 col-lg-4">Box 2</div>
  <div class="col-12 col-md-6 col-lg-4">Box 3</div>
</div>


Behavior:
Mobile: each box full width (col-12 = extra small one box)
Tablet: 2 boxes per row (col-md-6 = medium two box)
Desktop: 3 boxes per row (col-lg-4 = large three box)
```
<hr>

## ✍️ Typography (in Web / Bootstrap)

- Typography refers to the style and appearance of text on a webpage—such as font size, weight, alignment, spacing, and headings.
Good typography improves readability and user experience.

- In Bootstrap, typography is already styled for you with clean and professional defaults.

🔹 Headings
```
Bootstrap styles all HTML headings:
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>

You can also use heading classes:
<p class="h1">Heading Style</p>
<p class="h2">Heading Style</p>
```
🔹 Text Utilities
```
<p class="text-muted">Muted text</p>  //fant text
<p class="fw-bold">Bold text</p>
<p class="fst-italic">Italic text</p>
<p class="text-center">Center aligned</p>
<p class="text-end">Right aligned</p>
```

🔹 Display Headings
```
Used for large titles:
<h1 class="display-1">Display 1</h1>
<h1 class="display-4">Display 4</h1>
```
🔹 Lists & Blockquotes
```
<ul class="list-unstyled">
  <li>Item 1</li>
  <li>Item 2</li>
</ul>

<blockquote class="blockquote">
  <p>Learning never stops.</p>
</blockquote>

* <blockquote> is used to indicate that the enclosed text is an extended quotation
```
*Purpose of Typography*
```
Makes content readable
Improves visual hierarchy
Gives professional look
Enhances user experience
In Bootstrap, typography helps you create clean and consistent text styles with simple classes.
```
<hr>


```
For Text
<p class="text-muted">Muted text (gray)</p>
<p class="text-primary">Primary text (blue)</p>
<p class="text-success">Success text (green)</p>
<p class="text-info">Info text (light blue)</p>
<p class="text-warning">Warning text (orange/yellow)</p>
<p class="text-danger">Danger text (red)</p>

For Background
<p class="bg-primary">Primary background(blue)</p> 
<p class="bg-success">Success background(green)</p>
<p class="bg-info">Info background(skyblue)</p>
<p class="bg-warning">Warning background(yellow)</p>
<p class="bg-danger">Danger background(danger)</p>
```
<hr>



📘 Bootstrap Text Utility Classes
| **Class**         | **Purpose**                                      |
| ----------------- | ------------------------------------------------ |
| `lead`            | Makes paragraph stand out (larger, lighter text) |
| `text-left`       | Left-aligns text                                 |
| `text-center`     | Center-aligns text                               |
| `text-right`      | Right-aligns text                                |
| `text-justify`    | Justifies text (equal spacing)                   |
| `text-nowrap`     | Prevents text wrapping                           |
| `text-lowercase`  | Converts text to lowercase                       |
| `text-uppercase`  | Converts text to uppercase                       |
| `text-capitalize` | Capitalizes first letter of each word            |
| `text-muted`      | Displays gray / muted text                       |
| `text-primary`    | Displays blue text                               |
| `text-success`    | Displays green text                              |
| `text-info`       | Displays light blue text                         |
| `text-warning`    | Displays orange text                             |
| `text-danger`     | Displays red text                                |

## Heading in bootstrap
| **Heading** | **Size (rem)** | **Size (px)** |
| ----------- | -------------- | ------------- |
| **h1**      | 2.5rem         | **40px**      |
| **h2**      | 2rem           | **32px**      |
| **h3**      | 1.75rem        | **28px**      |
| **h4**      | 1.5rem         | **24px**      |
| **h5**      | 1.25rem        | **20px**      |
| **h6**      | 1rem           | **16px**      |

## Tables
| **Class**        | **Purpose**           |
| ---------------- | --------------------- |
| `table`          | Basic Bootstrap table |
| `table-striped`  | Zebra-striped rows    |
| `table-bordered` | Adds borders          |
| `table-hover`    | Hover effect          |
| `table-dark`     | Dark theme table      |

## 🖼️ 2. Images
| **Class**        | **Purpose**       |
| ---------------- | ----------------- |
| `img-fluid`      | Responsive image  |
| `img-thumbnail`  | Image with border |
| `rounded`        | Rounded corners   |
| `rounded-circle` | Circular image    |

## 3. Alerts
| **Class**       | **Meaning** |
| --------------- | ----------- |
| `alert-success` | Success     |
| `alert-danger`  | Error       |
| `alert-warning` | Warning     |
| `alert-info`    | Information |

## 🔘 4. Buttons

| **Class**      | **Purpose** | **Colour**  |
| ---------------| ----------- | ----------- |
| `btn`          | Base button | no color    |
| `btn-primary`  | Main action | blue        |
| `btn-success`  | Success     | green       |
| `btn-danger`   | Danger      | red         |
| `btn-warning`  | Warning     | yellow      |
| `btn-secondary`| Neutral     | gray        |

<hr>

## 📝 Bootstrap Forms & Inputs
- Bootstrap makes forms look clean and responsive with ready-made classes.
```
<form class="container mt-3">
  <div class="mb-3">
    <label class="form-label">Name</label>
    <input type="text" class="form-control" placeholder="Enter name">
  </div>

  <div class="mb-3">
    <label class="form-label">Email</label>
    <input type="email" class="form-control" placeholder="Enter email">
  </div>

  <div class="mb-3">
    <label class="form-label">City</label>
    <select class="form-select">
      <option>Pune</option>
      <option>Mumbai</option>
    </select>
  </div>

  <div class="form-check mb-3">
    <input class="form-check-input" type="checkbox">
    <label class="form-check-label">Accept Terms</label>
  </div>

  <button class="btn btn-primary">Submit</button>
</form>

Common form classes:
form-control – textboxes, textarea
form-select – dropdown
form-check – checkbox/radio
form-label – labels
btn – buttons
```

```
🎯 Final CCEE Tips (Last Revision)

✔ d-none → hide elements
✔ fixed-top → navbar fixed
✔ container-fluid → full width
✔ Panels/Wells → replaced by Cards
✔ Bootstrap 5 → no jQuery
```
