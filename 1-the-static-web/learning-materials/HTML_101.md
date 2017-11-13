# HTML

**H**yper**t**ext **M**arkup **L**anguage: The Building Blocks of the Web

## HTML5 semantic structure
HTML5 introduces several new semantic elements representing logical sections or components of a web app or document: `<section>`, `<nav>`, `<article>`, `<aside>`, `<hgroup>`, `<header>`, and `<footer>`, along with new rules for using the old `<h1>–<h6>` and `<address>` elements. None of the new elements actually “do” anything by themselves, but they provide a much nicer way for web authors to define the various parts of a document, and open the door for user agents and assistive technologies to use this information to enable alternate ways of viewing and navigating a page.

  + __article__ - specifies independent, self-contained content.
  + __section__ - defines sections in a document, such as chapters, headers, footers, or any other sections of the document.
  + __nav__  - contains any navigation elements of the document (navigation bar, breadcrumbs, etc.)
  + __footer__ - usually information to be displayed at the bottom of the document
  + __header__ - element represents a container for introductory content and/or a set of navigational links.
  + __time__ - defines a human-readable date/time. 
    can also be used to encode dates and times in a machine-readable way allowing user agents more functionality (add to calendar) `<time datetime="2008-02-14 20:00">`
  + __mark__ - highlight parts of your text.
  + __aside__ - defines some content aside from the content it is placed in. This content should be related to the surrounding content.

### Text related tags
  + h1...h5
  + `p`
  + `strong`
  + `em`
  + `br`
  + +more

### Links
  + `a` anchor

### Media

Use, or fork, this [Codepen project](http://codepen.io/chortlehoort/pen/qdoKqr) to show examples of video and audio tags.

  + img
  + audio
  + video

### Lists
  + li
  + ul
  + ol

### Tables
  + table
  + td
  + tr
  + th

## Commenting your code

`<!-- This is how you comment HTML code -->`

### Element Attributes
> **MDN:** "Additional values that configure the elements or adjust their behavior"

+ `<a href="...">`
+ `<div id="...">`
+ `<span class="...">`
+ `<p style="...">`
+ `<img src="...">`
+ `<input name="...">`
+ `<input type="...">`
+ `<input required>`

They can, and usually are, combined.

`<div id="bio" class="student--biography" style="color: red">`

### Forms & element types

Use, or fork, an example [HTML form Codepen project](http://codepen.io/chortlehoort/pen/ogpVZq) to show all the major field types that can be used.

  + form
  + select
  + option
  + textarea
  + text
  + password
  + date
  + submit
  + radio
  + checkbox
  + button
  + range
  + number
  + tel
  + url
  + email

---

## Block elements vs inline elements

A [block element](https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements) is an element that has, but may not be limited to, the following characteristics:

+ If no width is set, will expand naturally to fill its parent container
+ Can have margins and/or padding
+ If no height is set, will expand naturally to fit its child elements (assuming they are not floated or positioned)
+ By default, will be placed below previous elements in the markup (assuming no floats or positioning on surrounding elements)
+ Ignores the vertical-align property

An [inline element](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elemente) has, but may not be limited to, the following characteristics:

+ Flows along with text content
+ Will not clear previous content to drop to the next line like block elements
+ Is subject to white-space settings in CSS
+ Will ignore top and bottom margin settings, but will apply left and right margins, and any padding
+ Will ignore the width and height properties
+ If floated left or right, will automatically become a block-level element, subject to all block characteristics
+ Is subject to the vertical-align property

The easiest way to picture an inline element is to think of it as a box that acts like text. What happens, for example, to text that’s not separated by other elements? It flows one letter after the other. If you put an inline element next to text, it will flow next to that text just like another piece of text.

<img src="http://www.w3.org/wiki/images/3/38/Fc-ss-01.png">

---

## The Document Object Model (DOM)

The Document Object Model is a platform- and language-neutral interface that will allow programs and scripts to dynamically access and update the content, structure and style of documents. The document can be further processed and the results of that processing can be incorporated back into the presented page.

The HTML you write is parsed by the browser and turned into the DOM. But your HTML is not the DOM. Mistakes/omissions can be 'fixed' by the browser, such as when you add a `<table>` element in your HTML and leave out the required `<tbody>` element. The browser will just insert that `<tbody>` for you. The Javscript you write can also really change what's rendered far beyond the original markup.

