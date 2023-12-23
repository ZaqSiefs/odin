# CSS

## Intro

### Basic Syntax

- ```Selector```
    - Refers to the HTML elements to which CSS rules apply. These are what are being selected for each rule.
- Declarations
    - ```propery```
    - ```value```

Example:
```css
div.bold-text {
    front-weight: 700;
}
```
div.bold-text = ```selector```

front-weight = ```property```

700 = ```value```

### Selectors

```*``` = Universal Selector. Selects html elements of any type.

```css
* {
    color: purple;
}
```

```div```, ```p```, ```h1```, etc = Type selectors. Selects all html elements of a given type.

```css
p {
    color: white;
}

div {
    color: red;
}
```

```.<class>``` = Class selectors. Only affects html elements with the appropriate class attribute. HTML elements may have multiple classes.

```css
.alert-text {
    color: red;
}
```

```#``` = ID selectors.  HTML elements can only have one ID attribute, and only one instance of an ID can exist per page. **Use sparingly**

```css
#title {
    background-color: red;
}
```

### DRY

If two elements share some style declarations, we can combine them

not DRY:

```css
.read {
    color: white;
    background-color: black;
    /* several unique declarations */
}

.unread {
    color: white;
    background-color: black;
    /* several unique declarations */
}
```

DRY:

```css
.read,
.unread {
    color: white;
    background-color: black;
}

.read {
    /* several unique declarations */
}

.unread {
    /* several unique declarations */
}
```

### Chaining Selectors

Consider the following:

```html
<!-- HTML -->
<div>
    <div class="subsection header">Latest Posts</div>
    <p class="subsection" id="preview">Preview</p>
</div>
```
We have two elements with the class 'subsection', but we only want to access one of them.  This is where chaining can help.  **Cannot chain types**

```css
.subsection.header {
    color: red;
}

.subsection#preview {
    color: blue;
}
```

### Descendant combinator

Combinators can combine selectors differently than either grouping or chaining.  This combinator will only select a specific element if its selector matches all listed parent selectors

```html
<!-- HTML -->
<div class="ancestor">
    <!-- A -->
    <div class="contents">
        <!-- B -->
        <div class="contents">
            <!-- C -->
        </div>
    </div>
</div>

<div class="contents">
    <!-- D -->
</div>
```

Only affect B and C:

```css
/* CSS */
.ancestor .contents{
    /* some declarations */
}
```

### Properties

#### Color

```color``` = sets an element's text color

```background-color``` = sets an element's background color

> Both properties can accept these values:
>
> ```keyword``` eg. ```red``` or ```transparent```
>
> ```HEX``` eg. ```#1100ff```
>
> ```RGB``` eg. ```rgb(100,0,127)```
>
> ```HSL``` eg. ```hsl(15,82%,56%)```

#### Typography Basics and text-align

```font-family``` = single value or comma-separated list that determines a font.

> Each font falls into two categories: "font family name" or "generic family name"
>
> ```"Times New Roman"``` = font family name
>
> ```serif``` = generic family name

It is best to use a font family that you want, then use a generic font as a fallback.

```css
/* CSS */
p {
    font-family: "Times New Roman", serif;
}
```

```font-size``` = sets size of font in pixels

```css
/* CSS */
p {
    font-size: 22px;
}
```

```font-weight``` = affects the boldness of text. Can be **keyword** or a number from **1 to 1000**

```css
/* CSS */
p {
    font-weight: bold;
}

div {
    font-weight: 700;
}
```

```text-align``` = aligns text horizontally within an element using keywords.

```css
 /* CSS */
 p {
    text-align: center;
 }
```

#### Image height and width

By default, the height and width of an image is the height and width of the image file in pixels.  Use ```auto``` if you wish to save proportions while resizing.  Always include these values so that the web page allocates space for the image.

```height``` = height in pixels.

```width``` = width in pixels.

```css
/* CSS */
img {
    height: auto;
    width: 500px;
}
```

### Connecting to HTML

#### External CSS

links to an external CSS file within the ```<head>``` element.

```html
<!-- HTML -->
<head>
    <link rel="stylesheet" href="styles.css">
</head>
```

#### Internal CSS

Adding CSS within the HTML file's ```<style>``` element, inside the ```<head>``` element.

```html
<!-- HTML -->
<head>
    <style>
        div {
            color: white;
        }
        p {
            color: red;
        }
    </style>
</head>
```

#### Inline CSS

Adding styles directly to HTML elements. **Not recommended**

```html
<!-- HTML -->
<body>
    <div style="color: white; background-color: black;">
    </div>
</body>
```

## Cascade

This is what determines which rules get applied to HTML.

### Specificity

More specific declarations will take precedence over less specific ones.

1. ID selectors
2. Class selectors
3. Type selectors

Precedence of selectors of the same type are determined by the amount of instances of that selector.
```html
<!-- HTML -->
<div class="main">
    <div class="list subsection">Red text</div>
</div>
```
```css
/* CSS */
/* rule 1 */
.subsection {
    color: blue;
}
/* rule 2 */
.main .list {
    color: red;
}
```

above, rule 2 is more specific and would take precedence over rule 1.

```html
<!-- HTML -->
<div class="main">
    <div class="list" id="subsection">Red text</div>
</div>
```
```css
/* CSS */
/* rule 1 */
#subsection {
    color: blue;
}
/* rule 2 */
.main .list {
    color: red;
}
```

above, rule 1 uses an ID, which is more specific than even multiple classes, and would take precedence over rule 2.

```html
<!-- HTML -->
<div class="main">
    <div class="list" id="subsection">Red text</div>
</div>
```
```css
/* CSS */
/* rule 1 */
#subsection {
    color: blue;
}
/* rule 2 */
.main #subsection {
    color: red;
}
```

above, since both have the same number of IDs, the cascade sees that rule 2 has a class selector and rule 1 does not.  Rule 2 would then get precedence

```*``` has no specificity, meaning even type selectors will take precedence

### Inheritance

CSS properties that when applied to an element, are ingerited by that element's descendants.

```typography-based``` properties are usually inherited (```color```, ```font-size```, etc.)

Directly targeting an element will always beat inheritance.

### Rule Order

The final tiebreaker will go to the rule that is defined last.

## The Box Model

Most important thing to master with CSS is *positioning* and *layout*

Every sing thing on a webpage is a rectangular box. They may have additional boxes inside, and can sit alongside eachother.

```padding``` = the space between the border of a box and the content of the box, in pixels from **each side**. Holds the background color.

```border``` = the space between the margin and the padding, in pixels from **each side**.  Given own color.

```margin``` = the space between the borders of a box and the borders of adjacent boxes, in pixels from **each side**. Collapses with other virtical margins, giving the larger margin the priority.  4 arguments: **Top, Left, Bottom, Right** can be defined.  Can use negative values.

> ![boxmodel](img/boxmodel.png "Title")

the ```box-sizing``` attribute will calculate the entire size of an object from the ```height``` attribute.  Applying the border and padding sizes will subtract from the height value, leaving the remainder as the element size. Best practice is to add this to ```*``` (all) elements.

### Outer Display Type

#### Block

If a box is of outer display type ```block```, then:

- Box will break onto new line
- width and height properties are respected
- padding, margin, and border will cause other elements to be pushed away from box
- if width is not specified, box will extend in the inline direction to fill the space available in it's container.
- ```<h1>``` and ```<p>``` use ```block``` as outer display type by default.

#### Inline

If box has an outer display type of ```inline```, then:

- Box will not break into new line
- width and height properties will not apply
- top and bottom padding, margins, and borders will apply but will not cause other inline boxes to move away from the box
- left and right padding, margins, and borders will apply and will cause other inline boxes to move away from the box.
- ```<a>```, ```<span>```, ```<em>```, and ```strong``` use ```inline``` outer display by default

### Inner Display Type

Dictates how elements inside the box are laid out.

elements inside of a box are laid out in **normal flow** by default.

Can change the inner display type by setting ```display: flex;``` where the outer display will still be ```block```, but the inner display will become ```flex```.  Any children of this box will maintain ```flex```





