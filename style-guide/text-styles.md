---
layout: style-guide
title: Brand Elements | Uvize Style Guide
---

# Text Styles

The web app primarily uses the **Helvetica Neue** typeface in regular, light, and bold variations.

Through the recent brand update the **Lato** Typeface has  been introduced in regular, bold, and black variations. Marketing sites and some web app content uses these styles which can be applied by nesting content in an element with the `.marketing-site-wrapper` class.

### Headings

Heading tags `<h1>` through `<h6>` are mapped to relevant styles from the design. As with [Bootstrap](http://getbootstrap.com/css/#type-headings), classes `.h1` through `.h6` can also be used to the same effect.

In some cases a color variation is included by default. Headings can be featured via the `.hero-title` class which sets the heading in the `brand` color. 

<div class="docs-example">
<h1>Page Heading - h1</h1>
<h1 class="hero-title">Hero Page Heading - h1.hero-title</h1>
<h2>Major Content Heading - h2</h2>
<h3>Content Heading - h3</h3>
<h4>Minor Content Heading - h4</h4>
<h5>Caps Label - h5</h5>
<h6>Small Heading - h6</h6>
</div>

The headings appear differently when nested in the `.marketing-site-wrapper`.
<div class="docs-example">
  <div class="marketing-site-wrapper">
    <h1>Page Heading - h1</h1>
    <h1 class="hero-title">Hero Page Heading - h1.hero-title</h1>
    <h2>Major Content Heading - h2</h2>
    <h3>Content Heading - h3</h3>
    <h4>Minor Content Heading - h4</h4>
    <h5>Caps Label - h5</h5>
    <h6>Small Heading - h6</h6>
  </div>
</div>

### Copy

Paragraphs inherit their style from the `body` - Helvetica Neue @ 14px with 20px linespacing. 

As with [Bootstrap](http://getbootstrap.com/css/#type-headings), modifiers like `<strong>` and `<span class="text-muted">` can be applied with pre-styled effects.
  
<div class="docs-example">
  <p>A standard paragraph from with <strong>strong</strong> and <span class="text-muted">muted</span> text.</p>
</div>
  
For help copy the first `<p>` nested inside an element with the `.helper-info` class will get an icon:

<div class="docs-example">
  <div class="helper-info">
    <p>First paragraph of help</p>
    <p>Second paragraph of help</p>
  </div>
</div>

Marketing site copy is larger and set in Lato Light @ 16px with 140% linespacing.

<div class="docs-example">
  <div class="marketing-site-wrapper">
  <p>A paragraph from the marketing site with <strong>strong</strong> and <span class="text-muted">muted</span> text.</p>
  </div>
</div>



### Alerts

