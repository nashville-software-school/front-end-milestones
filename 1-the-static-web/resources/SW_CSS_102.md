# :pushpin: Exercises

1. [Relationship Selectors](../exercises/SW_CSS_RELATIONSHIP_SELECTORS.md)
1. [Pseudoclasses](../exercises/SW_CSS_PSEUDOCLASSES.md)
1. [Zen Garden](../exercises/SW_CSS_ZEN_GARDEN.md)
1. [Music History 1](../exercises/SW_MUSIC_HISTORY_01.md)
1. [Product Cards](../exercises/SW_CSS_PRODUCT_CARDS.md)

# CSS 102

You will learn more advanced CSS features

## The box model

<img src="https://css-tricks.com/wp-content/csstricks-uploads/firebox.png">

### Display properties

There are quite a few values for the display property, but the most common are `block`, `inline`, `inline-block`, and `none`.

#### block

A value of `block` will make an element behave like an block-level element.

```
display: block;
```

#### inline

A value of `inline` will make an element behave like an inline-level element.

```
display: inline;
```

#### inline-block

A value of `inline-block` will make an element behave like an inline-level element, but will allow you to style it with block level properties.

```
display: inline;
```

#### **Margin & Padding on Inline-Level Elements**

Inline-level elements are affected a bit differently than `block` and `inline-block` elements when it comes to margins and padding. Margins only work horizontally—left and right—on inline-level elements. Padding works on all four sides of inline-level elements; however, the vertical padding—the top and bottom—may bleed into the lines above and below an element.

Margins and padding work like normal for block and inline-block elements.

## Advanced layouts with Flexible Box Layout

A relatively new CSS feature is the [Flexible Box Layout module](http://css-tricks.com/snippets/css/a-guide-to-flexbox/). Explain how `display: flex`, `flex-flow`, and `flex-grow` works. Using this should help those who struggled with the first Music History layout.

```html
<div class="flex-container">
  <header class="flex-item">Header</header>
  <section class="flex-item sidebar__left">Sidebar</section>
  <section class="flex-item main">Main</section>
  <section class="flex-item sidebar__right">This is some longer sidebar content that shows how every cell in this row will grow to be the same size as this one.</section>
  <footer class="flex-item">Footer</footer>
</div>
```

```css
.flex-container {
  padding: 0;
  margin: 0;
  list-style: none;
  height: 200px;
  display: flex;
  flex-flow: row wrap;
}

.flex-container > header,
.flex-container > footer {
  flex: 1 100%;
}

.sidebar__left {
  flex-grow: 2;
}

.sidebar__right {
  flex-grow: 1;
}

.main {
  flex-grow: 6;
}

.flex-item {
  background: tomato;
  padding: 10px;
  width: 100px;
  border: 3px solid rgba(0,0,0,.2);
  color: white;
  font-weight: bold;
  font-size: 2em;
  text-align: center;
}
```

## Selecting specific elements in a list

### nth-child
Using the `nth-child` [pseudo class](https://developer.mozilla.org/en-US/docs/Web/CSS/:nth-child) in CSS is a newer addition that let's you select either a specific item in a list of child DOM elements, or a general class of child DOM elements.

Using the formula `an+b` where `a` and `b` are integer values.

1. `1n+0` to select all elements
1. `2n+0` to select even elements (2, 4, 6, ...)
1. `3n+0` to select every third element (3, 6, 9, ...)
1. `2n+1` to select odd elements (1, 3, 5, ...)

There are also shortcut selectors

1. `odd` is the same as `2n+1`
1. `even` is the same as `2n+0`

```html
<article>
  <section> A </section>
  <section> B </section>
  <section> C </section>
  <section> D </section>
</article>
```

The following selector will put a border around the even sections

```css
article section:nth-child(2n+0) {
  border: 1px solid black;
}
```

### nth-of-type

This pseudo selector will only count the specific element type that you specify, instead of against all children. This is useful when the children of an element aren't all the same type.

```html
<article>
  <section> A </section>
  <section> B </section>
  <aside> Aside </aside>
  <section> C </section>
  <section> D </section>
  <section> E </section>
</article>
```

The following code will put a border around sections 1 and 5 because 3 isn't a section.

```css
article section:nth-child(2n+1) {
  border: 1px solid black;
}
```

However, the following code will make sections 1, 3 and 5 because it's only counting the section elements and ignores the aside element.

```css
article section:nth-of-type(2n+1) {
  color: blue;
}
```

### first-of-type

When you only want to select the first child element that of a type.

```html
<article>
  <section> A </section>
  <section> B </section>
  <aside> Aside </aside>
  <section> C </section>
  <section> D </section>
  <section> E </section>
</article>
```

The following code will highlight the first section, and the aside.

```css
article :first-of-type {
  background-color: lime;
}
```

The following code will highlight the **only** first section because we made the selector more specific.

```css
article section:first-of-type {
  background-color: lime;
}
```

### first-child, last-child

This will only select the first sibling child of a shared parent

```html
<article>
  <section> A </section>
  <section> B </section>
  <aside> Aside </aside>
  <section> C </section>
  <section> D </section>
  <section> E </section>
</article>
```

The following code will highlight the first section, and the aside.

```css
section {
  background-color: orange;
}

article section:first-child {
  background-color: lime;
}
```

### not()

Show a standard `<ul>` as a comma separated list.

```
ul > li {
  list-style-type: none;
  display: inline;
}

ul > li:not(:last-child)::after {
  content: ",";
}
```


## Positioning (fixed, relative, absolute)

### Absolute

Absolute positioning is the easiest to understand. You start with the CSS position property:

```
position: absolute;
```

This tells the browser that whatever is going to be positioned should be removed from the normal flow of the document and will be placed in an exact location on the page. It is also taken out of the normal flow of the document - it won't affect how the elements before it or after it in the HTML are positioned on the Web page.

If you want to position an element 10ems from the top of the document window, you would use the "top" offset to position it there with absolute positioning:

```
position: absolute; top: 10em;
```

This element will then always display 10em from the top of the page - no matter what else displays there in normal flow.

Absolutely positioned boxes that have no width set on them behave a bit strangely. Their width is only as wide as it needs to be to hold the content. So if the box contains a single word, the box is only as wide as that word renders. If it grows to two words, it'll grow that wide.

### Relative (static)

These two values are basically the same. The difference is that you'll never explicitly state `static` as the value of the position because that is the default value.

Relative positioning uses the same four positioning properties as absolute positioning. But instead of basing the position of the element upon the browser view port, it starts from where the element would be if it were still in the normal flow.

For example, if you have three paragraphs on your Web page, and the third has a position: relative style placed on it, it's position will be offset based on it's current location - not from the original sides of the view port.

```html
<p>Paragraph 1.</p>
<p>Paragraph 2.</p>
<p style="position: relative;left: 2em;">Paragraph 3.</p>
```

In the above example, the third paragraph will be positioned 3em from the left side of the container element, but will still be below the first two paragraphs. It would remain in the normal flow of the document, and just be offset slightly.

### Fixed

Fixed positioning is a lot like absolute positioning. The position of the element is calculated in the same way as the absolute model - from the sides of the view port. But fixed elements are then fixed in that location, like a watermark. Everything else on the page will then scroll past that element.

```
position: fixed;
```



## Advanced pseudo-classes

`:checked` for selected any checkboxes in a form that have been checked by the user.

### HTML5 form type validation classes

```
<form>
  <div>
    <label>Enter a URL:</label>
    <input type="url" />
  </div>

  <div>
    <label>Enter an email address:</label>
    <input type="email" required/>
  </div>
</form>
```

```css
input:valid {
  background-color: #ddffdd;
}

input:invalid {
  background-color: #ffdddd;
}
```

# Resources

[CSS Pro Tips](https://github.com/AllThingsSmitty/css-protips)
[Flexbox Froggy](http://flexboxfroggy.com/)
[Learn How To Create Drop Cap Letters In CSS](https://paulund.co.uk/learn-how-to-create-drop-cap-letters-in-css)
[Amazing CSS examples on CodePen](http://codepen.io/search/pens?q=css&limit=all&type=type-pens)
