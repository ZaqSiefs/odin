# HTML

## Elements and Tags
```<>``` = Opening tag

```</>``` = Closing tag
```html
<p> Paragraph Text </p>
```

## HTML Boilerplate

### Files
```index.html``` = root file for all websites.  Browsers will look for this file first, so it is a **must include**

### Elements

#### External:

```<!DOCTYPE>``` = Tells the browser which version of HTML should be rendered

```<html></html>``` = root element of the document. All else descends from here

```<html lang="en">``` = the "lang" attribute denotes the language that this webpage's content is primarily in.

#### Header:

```<head></head>``` = where important meta-information about webpages live.  **Do Not** use for displaying content

```<meta charset="UTF-8">``` = encodes charset so that special symbols can be displayed

```<title></title>``` = gives the webpage a human-readable title displayed on the browser tab.

#### Body:

```<body></body>``` = Where all the content displayed to useres go. This is where a majority of the HTML elements will be located

## Working with Text

### Elements

```<p></p>``` = Paragraph tag, meant to contain a single paragraph's worth of text.

```<h(1-6)></h(1-6)>``` = Heading tags, displayed Larger and bolder.  1 is largest, and 6 is smallest.

```<strong></strong>``` = Strong tag makes text bold and semantically marks the text as important.

```<em></em>``` = Emphasis tag makes text itallic and semantically places emphasis on the text.

```<!-- (text here) -->``` = Syntax for writing comments in html.  Will not be displayed to the browser.

## Lists

### Elements

```<ul></ul>``` = Unordered list wrapper.

```<ol></ol>``` = Ordered list wrapper.

```<li></li>``` = List item. Child of both list types.

## Links and Images

### Elements

```<a></a>``` = Anchor allows us to link to other files.

>Attributes
>
> ```target``` = Specifies where the linked resource will be opened
> - _self (default)
> - _blank (new tab/window)
> - _parent (parent frame)
> - _top (full body of window)
>
> ```rel``` = Describes relation between the current page and linked document.  Use ="noopener noreferrer" for security purposes when using _blank.

```<img>``` = Self enclosing image element that embeds an image inot the page using a src attribute.

> Attributes
>
> ```src``` = Tells browser where the image file is located. Works much like href, ad can embed an image using absolute and relative paths.
>
> ```alt``` = Text used in place of an image if the image cannot be loaded.
>
> ```height``` = The vertical pixel count
>
> ```width``` = The horizontal pixel count