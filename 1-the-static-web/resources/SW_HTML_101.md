# HTML

**H**yper**t**ext **M**arkup **L**anguage: The Building Blocks of the Web

## Elements

### Structure
  + html
  + head
  + body
  + div
  + span

#### HTML5 semantic structure
  + article
  + section
  + nav
  + footer
  + header
  + time `<time datetime="">`
  + mark

### Meta
  + DOCTYPE
  + title
  + link
  + meta
  + style

### Text
  + h1...h5
  + p
  + strong
  + em
  + br

### Links
  + anchor

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

Just touch on this by showing how some elements fill the width of their parent and some don't. Planting the seed for later when we begin styling.

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


## The Document Object Model (DOM)

The Document Object Model is a platform- and language-neutral interface that will allow programs and scripts to dynamically access and update the content, structure and style of documents. The document can be further processed and the results of that processing can be incorporated back into the presented page. This is an overview of DOM-related materials here at W3C and around the web.

<img src="http://www.w3.org/TR/DOM-Level-2-Core/images/table.gif">

The HTML you write is parsed by the browser and turned into the DOM. But your HTML is not the DOM. Mistakes/omissions can be 'fixed' by the browser, such as when you add a `<table>` element in your HTML and leave out the required `<tbody>` element. The browser will just insert that `<tbody>` for you. The Javscript you write can also really change what's rendered far beyond the original markup.

## Dive Deeper into HTML

### Required Reading

[Writing Your Best Code](http://learn.shayhowe.com/html-css/writing-your-best-code/)

### Learn more 

#### Articles and Tutorials

##### Basics
[Mozilla Developer Network's Intro to HTML](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Introduction)

[HTML Web Foundations: Elements](http://www.sitepoint.com/web-foundations/elements/)

[How to Structure an HTML Form](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Forms/How_to_structure_an_HTML_form)

##### Advanced
[HTML Advanced Tutorial](http://htmldog.com/guides/html/advanced/)

[All You Need to Know About the HTML5 Data Attribute ](http://webdesign.tutsplus.com/tutorials/all-you-need-to-know-about-the-html5-data-attribute--webdesign-9642)

[Authoring conformance criteria for bidirectional-algorithm formatting characters](http://www.echoecho.com/htmlframes.htm)

[HTML5 input types](http://www.htmldog.com/guides/html/advanced/html5forms1/)

[More HTML5 tags](http://www.html-5.com/tutorials/new-html-tags.html)