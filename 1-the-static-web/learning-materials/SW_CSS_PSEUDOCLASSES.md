# CSS pseudo-class exercise

## Setup

These commands are a helpful quick start. You may choose to ignore them completely and create your own directory structure. If you choose to use this recommendation, just copy the commands below. It doesn't matter what directory you are currently in.

```bash
mkdir -p ~/workspace/exercises/the-static-web/pseudo-classes && cd $_
touch index.html
touch pseudo-classes.css
```

## Requirements

Copy and paste the code below into the `index.html` file for this exercise.

> For this exercise you can't add any classes or ids

1. Currently, the `<li>` items are block level elements. Add correct styles to remove the bullets and display them as inline elements.
1. The three `<span>` elements should be displayed as block elements with a 1 pixel border and 25 pixel margin on **all** sides.
1. In the `article` element with the class `n-child`, add a 1 pixel border around every even numbered section element.

```html
<ul class="top">
  <li class="block">1</li>
  <li class="block">2</li>
  <li class="block">3</li>
</ul>

<span class="inline">X</span>
<span class="inline">Y</span>
<span class="inline">Z</span>

<article class="n-child">
  <section> A </section>
  <div> X </div>
  <section> B </section>
  <section> C </section>
  <section> D </section>
</article>

<article class="n-type">
  <section> A </section>
  <section> B </section>
  <aside> Aside </aside>
  <section> C </section>
  <section> D </section>
  <section> E </section>
</article>

<article class="first-of-type">
  <section> A </section>
  <section> B </section>
  <aside> Aside 1 </aside>
  <section> C </section>
  <section> D </section>
  <aside> Aside 2 </aside>
  <section> E </section>
  <footer>Footer</footer>
</article>

<article class="three">
  <section> A </section>
  <section> B </section>
  <aside> Aside </aside>
  <section> C </section>
  <section> D </section>
  <section> E </section>
</article>
```
