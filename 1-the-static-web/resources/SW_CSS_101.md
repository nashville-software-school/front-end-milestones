# CSS 101

**C**ascading **S**tyle **S**heets

## What is CSS?

In the earliest days of the World Wide Web, there were just documents. The Web was intended to share research documents, and so things that we see now like dynamic applications, beautiful layouts and colors, and cool animations were not even thought of.

Then, companies started to see a glimmer of promise for making money on the Web, so they started sharing their documents. Plain, boring text didn't cut it, so the W3C (World Wide Web Consortium) released CSS1 in 1996 so that professional web page developers - there weren't that many yet - could create more stylized documents with complex layouts and color schemes.

## Selecting an element

1. Show how to select elements by class, and by id.
1. Show how to select child, descendant, and sibling elements.

## Adding colors

1. Show how to use the color and background-color properties.

## Changing fonts (face, weight, and size)

1. Change the default font of the body.
2. Make different elements have different font faces.

## Aligning text

1. Give examples of left, center, and right aligned text.

## Floating elements

1. Float left, and right. Show how it affect the layout.
1. Show usage of `clear: both` to ensure page flow reverts back to standard after a floating element.

## Adding borders

1. Thickness & color.
1. Type (solid, dotted, dashed).
1. Show how to do rounded corners with `border-radius`.

## Create navigation with lists and CSS

Show students how to convert a standard `<ul>` element into a usable navigation section at the top of the page.

```css
.nav {
    background-color: goldenrod;
    height: 30px;
}

.nav > li {
    float: left;
    list-style-type: none;
    margin: 5px 15px 0 15px;
    font-family: "Arial";
    cursor: pointer;
}

.nav > li:hover {
    color: white;
}
```

## Validation for HTML5 inputs

With some of the new HTML5 input types, specifically the `url` and `email` types, the specification required that browsers provide the ability to write CSS pseudo classes that allows developers to style the inputs based on  the default validation rules.

```html
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

---

# Want to learn more?

1. A cool [CSS game](https://flukeout.github.io/)
1. **Generate and use a cool tooltip**. Visit the [CSS Tooltip Generator](http://www.cssportal.com/css-tooltip-generator/) and create the CSS you need. Then, see if you can get a tooltip to display when you hover a link in your profile page.
1. **Create awesome buttons**. Visit the [CSS3 Button Generator](http://css3button.net/) and make buttons for your navigation instead of links.
1. **Try some layout challenges**. Visit the [Wikiversity CSS Challenges](https://en.wikiversity.org/wiki/Web_Design/CSS_challenges) page and try to complete as many as you can.