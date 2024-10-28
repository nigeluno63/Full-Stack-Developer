
# Table of Contents

1. [HTML Element Types](#1)
   1. [Headings](#1a)
   2. [Paragraphs](#1b)
   3. [Links](#1c)
   4. [Images](#1d)
   5. [Picture](#1e)
   6. [Color](#1f)
   7. [Table](#1g)
   8. [Lists](#1h) 
   9. [HTML Block and Inline Elements](#1i)
   10. [iframe](#1j)     
   11. [Layout](#1k)
   12. [Computer Code ](#1l)
   13. [semantics ](#1m)
    
2. [HTML Attribute Types](#2)
   1.  [style](#2a)
   2.  [lang](#2b)
   3.  [title](#2c)
   4.  [dir](#2d)
   5.  [class](#2e)
   6.  [id](#2f)

3. [HTML Empty Tags](#3)
4. [HTML TAGS](#4)
5. [CSS](#5)
6. [JavaScript](#6)
7. [HTML Entities](#7)
8. [XHTML](#8)
9. [HTML FORMS](#9)

[-----------------------------------------------------------------------------------------------------------------------------]: #

# What is an HTML Element? 

An HTML element is defined by a start tag, some content, and an end tag:

`<tagname> Content goes here... </tagname>`

<u>The HTML element is everything from the start tag to the end tag:</u>

```html
<h1>My First Heading</h1>
<p>My first paragraph.</p>
```

***

### Tag Examples
- The `<!DOCTYPE html>` declaration defines that this document is an HTML5 document
- The `<html>` element is the root element of an HTML page
- The `<head>` element contains meta information about the HTML page
- The `<title>` element specifies a title for the HTML page (which is shown in the browser's title bar or in the page's tab)
- The `<body>` element defines the document's body, and is a container for all the visible contents, such as headings, paragraphs, images, hyperlinks, tables, lists, etc.
- The `<h1>` element defines a large heading
- The `<p>` element defines a paragraph

Note: Some HTML elements have no content (like the `<br>` element). These elements are called empty elements. Empty elements do not have an end tag!

***

**HTML attributes** provide additional information about HTML elements.

- E.g. The `<a>` tag defines a hyperlink. The (href) attribute in `<a href>` specifies the URL of the page the link goes to:

***

#### <u>HTML is Not Case Sensitive: </u>
HTML tags are not case sensitive: `<P>` means the same as `<p>`.

The HTML standard does not require lowercase tags, but W3C recommends lowercase in HTML, and demands lowercase for stricter document types like XHTML.

***

__<u>HTML Structure</u>__

![HTML  structure](/HTML/Screenshot%202024-10-22%20143648.png)

You can add comments to your HTML source by using the following syntax:

`<!-- Write your comments here -->`


# HTML Element Types <a id="1"></a>

## HTML Headings <a id="1a"></a> 
HTML headings are defined with the `<h1>` to `<h6>` tags.

- `<h1>` defines the most important heading. `<h6>` defines the least important heading.
  
Note: Browsers automatically add some white space (a margin) before and after a heading.


  
## HTML Paragraphs <a id="1b"></a>
  - HTML paragraphs are defined with the `<p>` tag:




## HTML Links <a id="1c"></a>
- HTML links are defined with the `<a>` tag:
- The link's destination is specified in the href attribute. Attributes are used to provide additional information about HTML elements.

By default, links will appear as follows in all browsers:

- An unvisited link is underlined and blue
- A visited link is underlined and purple
- An active link is underlined and red  

TIP: Links can be styles in CSS

### `<Target>` Arribute 

By default, the linked page will be displayed in the current browser window. To change this, you must specify another `<target>` for the link.

The `<target>` attribute specifies where to open the linked document.

The `<target>` attribute can have one of the following values:

- _self - Default. Opens the document in the same window/tab as it was clicked
- _blank - Opens the document in a new window or tab
- _parent - Opens the document in the parent frame
- _top - Opens the document in the full body of the window

### Email property
Use mailto: inside the href attribute to create a link that opens the user's email program (to let them send a new email):

`<a href="mailto:someone@example.com">Send email</a>`

NOTE:
- For `<a>` and `<area>` elements, the href attribute specifies the URL of the page the link goes to.

- For `<base>` elements, the href attribute specifies the base URL for all relative URLs on a page.

- For `<link>` elements, the href attribute specifies the location (URL) of the external resource (most often a style sheet file).

### `<id>` attribute
HTML links can be used to create bookmarks, so that readers can jump to specific parts of a web page.

- Use the id attribute (id="value") to define bookmarks in a page
- Use the href attribute (href="#value") to link to the bookmark

## HTML Images <a id="1d"></a>
- HTML images are defined with the `<img>` tag.
- The source file (`src`), alternative text (`alt`), `(width)`, and `(height)` are provided as attributes
- The `<img>` tag creates a placeholder space within the webpage that the browser displays once the page is rendered. The Image is not part of the HTML file, it only links to a URL of the actual image.

- Can use the `<img>` element inside `<a></a>` to link an image

There are two ways to specify the URL in the (`src`)attribute:
1. Absolute URL - Links to an external image that is hosted on another website


2. Relative URL - Links to an image that is hosted within the website. Here, the URL does not include the domain name. If the URL begins without a slash, it will be relative to the current page. Example: src="img_girl.jpg". If the URL begins with a slash, it will be relative to the domain. Example: src="/images/img_girl.jpg".

Tip: It is almost always best to use relative URLs. They will not break if you change domain.

- The required (`alt`) attribute for the `<img>` tag specifies an alternate text for an image:  
`<img src="img_girl.jpg" alt="Girl with a jacket">`

- The `<img>` tag should also contain the width and height attributes, which specify the width and height of the image (in pixels):  
`<img src="img_girl.jpg" width="500" height="600">`  

- But the width and height can be overriden by CSS style sheets. So its best to use the inline Style attribute and put the width and height indside that:  
`<img src="img_girl.jpg" style="width:500px;height:600px;">`  

HTML allows the following image formats:
- APNG
- GIF
- ICO
- JPEG
- PNG
- SVG

### <u>Image Maps</u>
The HTML `<map>` tag defines an image map. An image map is an image with clickable areas. The areas are defined with one or more `<area>` tags.

The idea behind an image map is that you should be able to perform different actions depending on where in the image you click.

- Use the `<usemap>` attribute: (usemap="#workmap")
- Create the Image Map `<map>` : (map name="workmap")
- Create clickable areas using the `<area>` tags. The shape must be defined
  - rect - defines a rectangular region
  - circle - defines a circular region
  - poly - defines a polygonal region
  - default - defines the entire region
- Lastly the coordinates must be defined

## HTML Picture <a id="1e"></a>

The `<picture>` element contains one or more `<source>` elements, each referring to different images through the srcset attribute. This way the browser can choose the image that best fits the current view and/or device.

Each `<source>` element has a media attribute that defines when the image is the most suitable

Purpose:
- Bandwidth - If you have a small screen or device, it is not necessary to load a large image file. The browser will use the first `<source>` element with matching attribute values, and ignore any of the following elements.

- Format support - Some browsers or devices may not support all image formats. By using the `<picture>` element, you can add images of all formats, and the browser will use the first format it recognizes, and ignore any of the following elements.

- The (srcset) in the `<source>` element works like the (src) in the `<img>` tag but is conditional on the (media) query.


## HTML Colors <a id="1f"></a>
HTML colors are specified with predefined color names, or with RGB, HEX, HSL, RGBA, or HSLA values.
HTML supports 140 standard color names.  
- Background Color
- Text Color
- Border Color  
`<p style="color:DodgerBlue;">Lorem ipsum...</p>`

## HTML Tables <a id="1g"></a>
- Each table cell is defined by a `<td>` and a `</td>` tag.
- Each table row starts with a `<tr>` and ends with a `</tr>` tag.
- You can have as many rows as you like in a table; just make sure that the number of cells are the same in each row.
- In those cases use the `<th>` tag instead of the `<td>` tag. By default, the text in `<th>` elements are bold and centered

### Borders
- To add a border, use the CSS border property on table, th, and td elements:
>```CSS
> table, th, td {
>  border: 1px solid black;
>}

- To avoid having double borders like in the example above, set the CSS border-collapse property to collapse: (  border-collapse: collapse;)

<u>Border Properties</u>
- border-color
- border-style
- ![Border Style](/HTML/border_style.png)
- border-radius
- background-color

### Table Sizes
- Use the style attribute with the width or height properties to specify the size of a table, row or column.
- style="width:100%" || style="height:200px;"
- Using a percentage as the size unit for a width means how wide will this element be compared to its parent element

### Table Headers
- You can add a `<caption>` that serves as a heading for the entire table.

### Padding and Spacing
-  HTML tables can adjust the padding inside the cells, and also the space between the cells.
-  Use CSS padding property on ceels and border-spacing property on table 

### Colspan & Rowspan
- To make a cell span over multiple columns, use the (colspan) attribute
- To make a cell span over multiple rows, use the (rowspan) attribute

### Styling
Use CSS styling to make tables look better
- To style every other table row element, use the :nth-child(even) selector.
- If you specify borders only at the bottom of each table row, you will have a table with horizontal dividers. Add the border-bottom property to all tr elements to get horizontal dividers. NOTE: it only works if the borders are collapsed.
- Use the :hover selector on tr to highlight table rows on mouse over.

```CSS
>tr:hover {background-color: #D6EEEE;}
```


### Colgroup
The `<colgroup>` element is used to style specific columns of a table.

- The `<colgroup>` element should be used as a container for the column specifications.
- Each group is specified with a `<col>` element.
- The span attribute specifies how many columns that get the style.
- The style attribute specifies the style to give the columns.

```CSS
<table>
  <colgroup>
    <col span="2" style="background-color:red">
  </colgroup>
  <tr>
    <th>MON</th>
    <th>TUE</th>
    <th>WED</th>
    <th>THU</th>
```

- The `<colgroup>` tag must be a child of a `<table>` element and should be placed before any other table elements, like `<thead>`, `<tr>`, `<td>` etc., but after the `<caption>` element, if present.
  

There is only a very limited selection of CSS properties that are allowed to be used in the colgroup:
- width property
- visibility property
- background properties
- border properties

If you want to style columns in the middle of a table, insert a "empty" `<col>` element (with no styles) for the columns before:

## HTML Lists <a id="1h"></a>

### Unordered Lists
- By default are black dots: Uses the `<ul>` tag  
  
Each list item starts with the `<li>` tag
### Order Lists
- By default are numbers: uses the `<ol>`
- Use start attribute to start the list from a number other than 1 (start="50")

### Description Lists
- A description list is a list of terms, with a description of each term.
- The `<dl>` tag defines the description list, the `<dt>` tag defines the term (name), and the `<dd>` tag describes each term

```HTML
<dl>
  <dt>Coffee</dt>
  <dd>- black hot drink</dd>
  <dt>Milk</dt>
  <dd>- white cold drink</dd>
</dl>
```

- Use the CSS style="List-Style-Type:" to choose the the style
- Lists can be nested
- Lists can be styles horizontally using the CSS propety float:left



## HTML Block and Inline Elements <a id="1i"></a>

### Block-Level Elements
- A block-level element always starts on a new line, and the browsers automatically add some space (a margin) before and after the element.
- A block-level element always takes up the full width available (stretches out to the left and right as far as it can).
- ![Blockl-level-Elements](/HTML/block-level-element.png)
- The `<div>` element is often used as a container for other HTML elements.


### Inline Elements
- An inline element does not start on a new line.
- An inline element only takes up as much width as necessary.
- ![Inline Elements](/HTML/inline-span-element.png)
- The `<span>` element is an inline container used to mark up a part of a text, or a part of a document.

## Div Element
- a block element by default and so it takes all available width and has line breaks before and after
- The `<div>` element is often used to group sections of a web page together: Used as a container
- To center a `<div>` element who width has been changed, use style="margin:auto;"

Usually `<div>` elements stack vertically if there are multiple. If you want to align them side by side there are a couple of methods using CSS properties:
- style="float:left;" : Although this wasn't originally meant to align `<div>` elements side by side.
- style="display:inline-block;" : Removes the line-breaks from the div blocks and displays them side by side
- Flexbox: To make the CSS flex method work, surround the `<div>` elements with another `<div>` element and give it the status as a flex container.
- CSS Grid: Can set up a class="gridcontainer" and style a column grid (specify the width of each column). Apply the class to a div container for the child div elements.

## iframe <a id="1j"></a>

- An HTML iframe is used to display a web page within a web page.
- The HTML `<iframe>` tag specifies an inline frame.

``` HTML 
<iframe src="url" title="description"></iframe>
```
Tip: It is a good practice to always include a title attribute for the `<iframe>`. This is used by screen readers to read out what the content of the iframe is.

- Use the height and width attributes to specify the size of the iframe.
- Or you can add the style attribute and use the CSS height and width properties
- To remove the border, add the style attribute and use the CSS border property:- style="border:none;"

### Iframe - Target for a Link
- The target attribute of the link must refer to the name attribute of the iframe:

```HTML
<iframe src="demo_iframe.htm" name="iframe_a" title="Iframe Example"></iframe>

<p><a href="https://www.w3schools.com" target="iframe_a">W3Schools.com</a></p>
```

## Head Element <a id="1k"></a>
- The HTML `<head>` element is a container for the following elements: `<title>`, `<style>`, `<meta>`, `<link>`, `<script>`, and `<base>`.
- The `<head>` element is a container for metadata (data about data). HTML metadata is data about the HTML document. Metadata is not displayed. Metadata typically define the document title, character set, styles, scripts, and other meta information

### `<Title>` Element
The `<title>` element:
- defines a title in the browser toolbar
- provides a title for the page when it is added to favorites
- displays a title for the page in search engine-results

### `<meta>` Element
The `<meta>` element is typically used to specify the 
- character set, page description (Browser)
- keywords (Search Engines)
- author of the document
- viewport settings (Browser)

```HTML
<meta charset="UTF-8">
<meta name="keywords" content="HTML, CSS, JavaScript">
<meta name="description" content="Free Web tutorials">
<meta name="author" content="John Doe">
<meta http-equiv="refresh" content="30">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
- The content attribute gives the value associated with the http-equiv or name attribute.
- You should include: `<meta name="viewport" content="width=device-width, initial-scale=1.0">` in all your web pages. This gives the browser instructions on how to control the page's dimensions and scaling. The width=device-width part sets the width of the page to follow the screen-width of the device. The initial-scale=1.0 part sets the initial zoom level when the page is first loaded by the browser.

- `<base>`  element specifies the base URL and/or target for all relative URLs in a page. The `<base>` tag must have either an href or a target attribute present, or both. There can only be one single `<base>` element in a document!


# HTML Layout ELements <a id="1k"></a>
- HTML has several semantic elements that define the different parts of a web page:
- ![HTML Semantics Layout](/HTML/HTML%20Semantics%20layout.png)

There are four different techniques to create multicolumn layouts. Each technique has its pros and cons:

- CSS framework
- CSS float property
- CSS flexbox
- CSS grid

### CSS framework
If you want to create your layout fast, you can use a CSS framework, like W3.CSS or Bootstrap.

### CSS Float property
It is common to do entire web layouts using the CSS float property. Float is easy to learn - you just need to remember how the float and clear properties work. 
Disadvantages: Floating elements are tied to the document flow, which may harm the flexibility.




# HTML Computer Code <a id="1l"></a>
- HTML contains several elements for defining user input and computer code.
- The HTML `<kbd>` element is used to define keyboard input. The content inside is displayed in the browser's default monospace font.
```HTML
<p>Save the document by pressing <kbd>Ctrl + S</kbd></p>
```
- The HTML `<samp>` element is used to define sample output from a computer program. The content inside is displayed in the browser's default monospace font.
```HTML
<p><samp>File not found.<br>Press F1 to continue</samp></p>
```
- The HTML `<code>` element  is used to define a piece of computer code. The content inside is displayed in the browser's default monospace font.
```HTML
<code>
x = 5;
y = 6;
z = x + y;
</code>
```
Notice that the `<code>` element does not preserve extra whitespace and line-breaks. To fix this, you can put the `<code>` element inside a `<pre>` element.

- The HTML `<var>` element  is used to define a variable in programming or in a mathematical expression. The content inside is typically displayed in italic.
```HTML
<p>The area of a triangle is: 1/2 x <var>b</var> x <var>h</var>, where <var>b</var> is the base, and <var>h</var> is the vertical height.</p>
```


# HTML Semantic Elements <a id="1m"></a>
- A semantic element clearly describes its meaning to both the browser and the developer.

### `<section>`
- The `<section>` element defines a section in a document.
- According to W3C's HTML documentation: "A section is a thematic grouping of content, typically with a heading."
- 
Examples of where a `<section>` element can be used:
- Chapters
- Introduction
- News items
- Contact information


### `<article>`
- The `<article>` element specifies independent, self-contained content.
- An article should make sense on its own, and it should be possible to distribute it independently from the rest of the web site.
  
Examples of where the <article> element can be used:
- Forum posts
- Blog posts
- User comments
- Product cards
- Newspaper articles

### `<header>`
- The `<header>` element represents a container for introductory content or a set of navigational links.
```HTML
<article>
  <header>
    <h1>What Does WWF Do?</h1>
    <p>WWF's mission:</p>
  </header>
  <p>WWF's mission is to stop the degradation of our planet's natural environment,
  and build a future in which humans live in harmony with nature.</p>
</article>
```

### `<footer>`
- The `<footer>` element defines a footer for a document or section.

A `<footer>` element typically contains:
- authorship information
- copyright information
- contact information
- sitemap
- back to top links
- related documents

### `<nav>`
- The `<nav>` element defines a set of navigation links.
- Notice that NOT all links of a document should be inside a `<nav>` element. The `<nav>` element is intended only for major blocks of navigation links.

### `<aside>`
- The `<aside>` element defines some content aside from the content it is placed in (like a sidebar).
- The `<aside>` content should be indirectly related to the surrounding content.

### `<figure>` & `<figcaption>`

- The `<figure>` tag specifies self-contained content, like illustrations, diagrams, photos, code listings, etc.
- he `<figcaption>` tag defines a caption for a `<figure>` element. The `<figcaption>` element can be placed as the first or as the last child of a `<figure>` element.


### List of Semantic Elements
![Semantic Elements](/HTML/SemanticElements.png)


# HTML Attribute <a id="2"></a>

Attributes usually come in name/value pairs like: name="value"

<u>Single or Double Quotes?</u>  
In some situations, when the attribute value itself contains double quotes, it is necessary to use single quotes:  

`<p title='John "ShotGun" Nelson'>`

## Style Attribute <a id="2a"></a>
The style attribute is used to add styles to an element, such as color, font, size, and more:  
`<p style="color:red;">This is a red paragraph.</p>`

The HTML style attribute has the following syntax:  
`<tagname style="property:value;">`  
The property is a CSS property. The value is a CSS value.

<u>CSS Properties for `<style="">` include</u>
- color
- font-family
- font-size
- text-align
- background-color
- border


### Background Image property
To add a background image on an HTML element, use the HTML style attribute and the CSS background-image property:  
`<p style="background-image: url('img_girl.jpg');">`


<u>Properties:  </u>

>```html
><style>  
>body {  
>  background-image: url('img_girl.jpg');  
>  background-repeat: no-repeat;  
>  background-attachment: fixed;  
>  background-size: cover;  
>}  
></style>

- background-repeat: no-repeat; ___stops the image from repeating if its smaller (it will only be displayed once in the top left corner of the element).
- background-attachment: fixed; ____This property keeps the background image fixed in place while scrolling. The image will not move with the content of the page, creating a parallax effect.
- background-size: cover;____The background image is resized to cover the entire element, while maintaining its aspect ratio. This means the image will fill the element entirely, but parts of the image may be cropped if the aspect ratios of the image and the element do not match. It will scale up to fit
- background-size: 100% 100%; ______ The background image is stretched to fit the entire element, both in width and height, regardless of its original aspect ratio. This means that the image will be resized to exactly match the width and height of the element, which can lead to distortion if the aspect ratios differ.






## lang Attribute <a id="2b"></a>
You should always include the lang attribute inside the `<html>` tag, to declare the language of the Web page. This is meant to assist search engines and browsers.

## Title Attribute <a id="2c"></a>
The title attribute defines some extra information about an element.

The value of the title attribute will be displayed as a tooltip when you mouse over the element:
`<p title="I'm a tooltip">This is a paragraph.</p>`

## dir Attribute <a id="2d"></a>
How the dir Attribute Works:
The dir attribute specifies the directionality of text. It can have the following values:

- ltr: Left-to-right (default for most languages like English).
- rtl: Right-to-left (used for languages like Arabic, Hebrew).
- auto: Automatically determines the text direction based on the first strong directional character (like a letter or number).


## Class Attribute <a id="2e"></a>

- The class attribute is often used to point to a class name in a style sheet. It can also be used by a JavaScript to access and manipulate elements with the specific class name.

Tip: The class attribute can be used on any HTML element.
Note: The class name is case sensitive!

- The Syntax For Class  
To create a class; write a period (.) character, followed by a class name. Then, define the CSS properties within curly braces {}:
- To define multiple classes, separate the class names with a space, e.g. <div class="city main">. The element will be styled according to all the classes specified.
- JavaScript can access elements with a specific class name with the getElementsByClassName() method:

```JavaScript
<script>
function myFunction() {
  var x = document.getElementsByClassName("city");
  for (var i = 0; i < x.length; i++) {
    x[i].style.display = "none";
  }
}
</script>
```

## id Attribute <a id="2f"></a>

- The id attribute specifies a unique id for an HTML element. The value of the id attribute must be unique within the HTML document.
- The syntax for id is: write a hash character (#), followed by an id name. Then, define the CSS properties within curly braces {}.
```CSS
<style>
#myHeader {
  background-color: lightblue;
  color: black;
  padding: 40px;
  text-align: center;
}
</style>
```

- A class name can be used by multiple HTML elements, while an id name must only be used by one HTML element within the page:

### Used as a bookmark
- First, create a bookmark with the id attribute
- Then, add a link to the bookmark ("Jump to Chapter 4"), from within the same page

```CSS
<h2 id="C4">Chapter 4</h2>

<a href="#C4">Jump to Chapter 4</a>
```

### Used in JavaScript
- JavaScript can access an element with a specific id with the getElementById() method:
```JavaScript
<script>
function displayResult() {
  document.getElementById("myHeader").innerHTML = "Have a nice day!";
}
</script>
```






# Empty Tags <a id="3"></a>

## HTML Horizontal Rules

The `<hr>` tag defines a thematic break in an HTML page, and is most often displayed as a horizontal rule.

## HTML Line Breaks
The HTML `<br>` element defines a line break.

Use `<br>` if you want a line break (a new line) without starting a new paragraph

## Other

- `<img>`
- `<link>`

# HTML Tags <a id="4"></a>

## `<pre>`

The HTML `<pre>` element defines preformatted text.

The text inside a `<pre>` element is displayed in a fixed-width font (usually Courier), and it preserves both spaces and line breaks

## HTML Formatting Elements
Formatting elements were designed to display special types of text:

>- `<b>` - Bold text: The HTML `<b>` element defines bold text, without any extra importance.

>- `<strong>` - Important text: The HTML `<strong>` element defines text with strong importance. The content inside is typically displayed in bold.

>- `<i>` - Italic text: The HTML `<i>` element defines a part of text in an alternate voice or mood. The content inside is typically displayed in italic.

>- `<em>` - Emphasized text - The HTML `<em>` element defines emphasized text. The content inside is typically displayed in italic.
>
>Tip: A screen reader will pronounce the words in `<em>` with an emphasis, using verbal stress.

>- `<mark>` - Marked text: The HTML `<mark>` element defines text that should be marked or highlighted:  

>- `<small>` - Smaller text: The HTML `<small>` element defines smaller text

>- `<del>` - Deleted text: The HTML `<del>` element defines text that has been deleted from a document. Browsers will usually strike a line through deleted text

>- `<ins>` - Inserted text: The HTML `<ins>` element defines a text that has been inserted into a document. Browsers will usually underline inserted text

>- `<sub>` - Subscript text: The HTML `<sub>` element defines subscript text. Subscript text appears half a character below the normal line, and is sometimes rendered in a smaller font. Subscript text can be used for chemical formulas, like H2O:

>- `<sup>` - Superscript text: The HTML `<sup>` element defines superscript text. Superscript text appears half a character above the normal line, and is sometimes rendered in a smaller font. Superscript text can be used for footnotes, like WWW<sup>`[1]`

>- `<blockquote>` for Quotations: The HTML `<blockquote>` element defines a section that is quoted from another source.
>
>Browsers usually indent `<blockquote>` elements.

>- `<q>` defines a short quotation. Browsers normally insert quotation marks around the quotation.

>- `<abbr>` defines an abbreviation or an acronym, like "HTML", "CSS". Use the global title attribute to show the description for the abbreviation/acronym when you mouse over the element. 

>- `<cite>` defines the title of a creative work (e.g. a book, a poem, a song, a movie, a painting, a sculpture, etc.). The text in the <cite> element usually renders in italic.

>- `<bdo>` BDO stands for Bi-Directional Override. The HTML `<bdo>` tag is used to override the current text direction:  
`<bdo dir="rtl">This text will be written from right to left </bdo>`

# CSS <a id="5"></a>
Cascading Style Sheets (CSS) is used to format the layout of a webpage.

With CSS, you can control the color, font, the size of text, the spacing between elements, how elements are positioned and laid out, what background images or background colors are to be used, different displays for different devices and screen sizes, and much more!

CSS can be added to HTML documents in 3 ways:

Inline - by using the style attribute inside HTML elements
Internal - by using a `<style>` element in the `<head>` section
External - by using a `<link>` element to link to an external CSS file

CSS properties:  
- Color, Font, Size
- Border, Padding, Margin

## INLINE CSS
An inline CSS is used to apply a unique style to a single HTML element.

An inline CSS uses the style attribute of an HTML element.


## INTERNAL CSS
An internal CSS is used to define a style for a single HTML page.

An internal CSS is defined in the `<head>` section of an HTML page, within a `<style>` element:

>```CSS
><style>  
>body {background-color: powderblue;}  
>h1   {color: blue;}  
>p    {color: red;}  
></style>

### CSS Links Styling

>```CSS
><style>
>a:link {  
>  color: green;  
>  background-color: transparent;  
>  text-decoration: none;  
>}  
>
>a:visited {  
>  color: pink;  
>  background-color: transparent;  
>  text-decoration: none;  
>}  
>
>a:hover {  
>  color: red;  
>  background-color: transparent;  
>  text-decoration: underline;  
>}  
>
>a:active {  
>  color: yellow;  
>  background-color: transparent;  
>  text-decoration: underline;  
>}  
></style>

# JavaScript <a id="6"></a>
JavaScript makes HTML pages more dynamic and interactive.

- The HTML `<script>` tag is used to define a client-side script (JavaScript).
- The `<script>` element either contains script statements, or it points to an external script file through the (src) attribute.
- Common uses for JavaScript are image manipulation, form validation, and dynamic changes of content.
- To select an HTML element, JavaScript most often uses the document.getElementById() method.
- The HTML `<noscript>` tag defines an alternate content to be displayed to users that have disabled scripts in their browser or have a browser that doesn't support scripts
```Javascript
<script>
document.getElementById("demo").innerHTML = "Hello JavaScript!";
</script>
<noscript>Sorry, your browser does not support JavaScript!</noscript>
```

# HTML ENTITES <a id="7"></a>

- Reserved characters in HTML must be replaced with entities:  
`<` (less than) = `&lt;`  
`>` (greather than) = `&gt;`
- Entities names are written as: &<em>entityname</em>
- Entities numbers are written as: &#<em>entitynumber</em>
- To display a less than sign (<) we must write: `&lt;` or `&#60;`
- `&nbsp;` is a non-breaking space which you can use to keep words together incase the page width chnages and those words end up getting cut with one at the end of one line and the other at the beginnng of the next line.(Eg.Mr.Smith, 10 kg)
- ![HTML Entities](/HTML/html_entities.png)

### Diacritical marks
- A diacritical mark is a "glyph" added to a letter.
- Some diacritical marks, like grave ( &#768; )  and acute ( &#769; ) are called accents.
- Diacritical marks can be used in combination with alphanumeric characters to produce a character that is not present in the character set (encoding) used in the page.
- ![diacritical marks](/HTML/diacritical_marks.png)

## HTML Symbol Entities

To add such symbols to an HTML page, you can use the entity name or the entity number (a decimal or a hexadecimal reference) for the symbol:
```HTML
<p>I will display &euro;</p>
<p>I will display &#8364;</p>
<p>I will display &#x20AC;</p>
```
Full list of UTF-8 Reference: https://www.w3schools.com/charsets/ref_html_utf8.asp


## Character Sets
### The ASCII Character Set
ASCII was the first character encoding standard for the web. It defined 128 different characters that could be used on the internet:

- English letters (A-Z)  
- Numbers (0-9)  
- Special characters like ! $ + - ( ) @ < >.  

### The ANSI Character Set
ANSI (Windows-1252) was the original Windows character set:

- Identical to ASCII for the first 127 characters
- Special characters from 128 to 159
- Identical to UTF-8 from 160 to 255


### The ISO-8859-1 Character Set
ISO-8859-1 was the default character set for HTML 4. This character set supported 256 different character codes. HTML 4 also supported UTF-8.

- Identical to ASCII for the first 127 characters
- Does not use the characters from 128 to 159
- Identical to ANSI and UTF-8 from 160 to 255

### The UTF-8 Character Set

- is identical to ASCII for the values from 0 to 127
- Does not use the characters from 128 to 159
- Identical to ANSI and 8859-1 from 160 to 255
- Continues from the value 256 to 10 000 characters

## URL

- A URL is another word for a web address.
- A URL can be composed of words (e.g. w3schools.com), or an Internet Protocol (IP) address (e.g. 192.68.20.50).

The syntax is: `scheme://prefix.domain:port/path/filename`
- scheme - defines the type of Internet service (most common is http or https)
- prefix - defines a domain prefix (default for http is www)
- domain - defines the Internet domain name (like w3schools.com)
- port - defines the port number at the host (default for http is 80)
- path - defines a path at the server (If omitted: the root directory of the site)
- filename - defines the name of a document or resource 

### Common url schemes

- http: HyperText Transfer Protocol
- https: Secure HyperText Transfer Protocol
- ftp: File Transfer protocol
- file

#### URL Encoding
- URLs can only be sent over the Internet using the ASCII character-set. 
- If a URL contains characters outside the ASCII set, the URL has to be converted: URL encoding replaces non-ASCII characters with a "%" followed by hexadecimal digits.
- URLs cannot contain spaces. URL encoding normally replaces a space with a plus (+) sign, or %20.

Url encoding reference: https://www.w3schools.com/tags/ref_urlencode.asp

# XHTML <a id="8"></a>
XHTML is a stricter, more XML-based version of HTML.
- XHTML stands for EXtensible HyperText Markup Language
- XHTML is a stricter, more XML-based version of HTML
- XHTML is HTML defined as an XML application
- XHTML is supported by all major browsers

Why
- XML is a markup language where all documents must be marked up correctly. In addition, browsers ignore errors in HTML pages, and try to display the website even if it has some errors in the markup. So XHTML comes with a much stricter error handling.
- XHTML was developed to make HTML more extensible and flexible to work with other data formats (such as XML).

The Most Important Differences from HTML
- <!DOCTYPE> is mandatory
- The xmlns attribute in `<html>` is mandatory
- `<html>`, `<head>`, `<title>`, and `<body>` are mandatory
- Elements must always be properly nested
- Elements must always be closed
- Elements must always be in lowercase
- Attribute names must always be in lowercase
- Attribute values must always be quoted
- Attribute minimization is forbidden

# HTML Forms <a id="9"></a>
An HTML form is used to collect user input. The user input is most often sent to a server for processing.

1. The HTML `<form>` element is used to create an HTML form for user input:
   - The `<form>` element is a container for different types of input elements, such as: text fields, checkboxes, radio buttons, submit buttons, etc.
2. The HTML `<input>` element is the most used form element. An `<input>` element can be displayed in many ways, depending on the type attribute.
![input_types](/HTML/input_types.png)
