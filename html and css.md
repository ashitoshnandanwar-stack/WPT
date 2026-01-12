# Html and css

## Priority in css

```
In css: Inline > Internal > External
*but it can be change using '!important'*

Specificity of selectors:  IDs > Clasess > Elements 
Specificity of selectors matter more than the style location when cmparing internal and extrenal styles.
```

## CSS Box Model

In CSS, every HTML element is treated as a rectangular box.
```
+-----------------------+
|        Margin         |
|  +-----------------+  |
|  |     Border      |  |
|  |  +-----------+  |  |
|  |  |  Padding  |  |  |
|  |  | +-------+ |  |  |
|  |  | |Content| |  |  |
|  |  | +-------+ |  |  |
|  |  +-----------+  |  |
|  +-----------------+  |
+-----------------------+


🔹 Parts of the Box Model
Content – Actual text/image inside the element
Padding – Space between content and border
Border – Line around padding and content
Margin – Space outside the border (distance from other elements)
```

## 🎨 HTML Style Tags
- HTML provides some built-in style (formatting) tags to change the appearance of text. These were widely used before CSS became popular.

| Tag        | Purpose             | Example                      |
| ---------- | ------------------- | ---------------------------- |
| `<b>`      | Bold text           | `<b>Bold</b>`                |
| `<i>`      | Italic text         | `<i>Italic</i>`              |
| `<u>`      | Underline           | `<u>Underline</u>`           |
| `<strong>` | Important (bold)    | `<strong>Important</strong>` |
| `<em>`     | Emphasized (italic) | `<em>Emphasis</em>`          |
| `<mark>`   | Highlight text      | `<mark>Mark</mark>`          |
| `<small>`  | Small text          | `<small>Small</small>`       |
| `<sup>`    | Superscript         | `x<sup>2</sup>`              |
| `<sub>`    | Subscript           | `H<sub>2</sub>O`             |
| `<del>`    | Deleted text        | `<del>Old</del>`             |
| `<ins>`    | Inserted text       | `<ins>New</ins>`             |

```
In Array:
push() – adds elements to the same array (modifies original)
pop() – removes last element from the same array
shift() – removes first element from the same array
map() – creates and returns a new array without changing the original
```
