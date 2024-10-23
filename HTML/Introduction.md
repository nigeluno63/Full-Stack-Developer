
# Table of Contents

1. [HTML Element Types](#1)
2. [HTML Attribute Types](#2)

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

# HTML Element Types <a id="1"></a>

## HTML Headings  
HTML headings are defined with the `<h1>` to `<h6>` tags.

- `<h1>` defines the most important heading. `<h6>` defines the least important heading.
  
## HTML Paragraphs
  - HTML paragraphs are defined with the `<p>` tag:




## HTML Links
- HTML links are defined with the `<a>` tag:
- The link's destination is specified in the href attribute. Attributes are used to provide additional information about HTML elements.

## HTML Images
- HTML images are defined with the `<img>` tag.
- The source file (`src`), alternative text (`alt`), `(width)`, and `(height)` are provided as attributes

>There are two ways to specify the URL in the (`src`)attribute:
>1. Absolute URL - Links to an external image that is hosted on another website
>
>
> 2. Relative URL - Links to an image that is hosted within the website. Here, the URL does not include the domain name. If the URL begins without a slash, it will be relative to the current page. Example: src="img_girl.jpg". If the URL begins with a slash, it will be relative to the domain. Example: src="/images/img_girl.jpg".
>
>Tip: It is almost always best to use relative URLs. They will not break if you change domain.

>The required (`alt`) attribute for the `<img>` tag specifies an alternate text for an image:  
`<img src="img_girl.jpg" alt="Girl with a jacket">`

>The `<img>` tag should also contain the width and height attributes, which specify the width and height of the image (in pixels):  
`<img src="img_girl.jpg" width="500" height="600">`

# HTML Attribute Types (for multiple tags) <a id="2"></a>

Attributes usually come in name/value pairs like: name="value"

## Style Attribute
The style attribute is used to add styles to an element, such as color, font, size, and more:  
`<p style="color:red;">This is a red paragraph.</p>`

## lang Attribute
You should always include the lang attribute inside the <html> tag, to declare the language of the Web page. This is meant to assist search engines and browsers.
