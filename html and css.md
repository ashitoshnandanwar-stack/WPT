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
