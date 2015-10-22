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

As with [Bootstrap](http://getbootstrap.com/css/#type-headings), modifiers like `<strong>` and `<span class="text-muted">` can be applied with pre-styled effects. By default Links are styled <a href="#">blue</a>, links to <a class="username">usernames</a> and other things such as groups are in bold in dark blue via the `.username` class.
  
<div class="docs-example">
  <p>A standard paragraph from with a <a href="#">link</a>, a <a class="username">username</a>, and <strong>strong</strong> and <span class="text-muted">muted</span> text.</p>
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
  <p>A standard paragraph from with a <a href="#">link</a>, a <a class="username">username</a>, and <strong>strong</strong> and <span class="text-muted">muted</span> text.</p>
  </div>
</div>



### Alerts

[Bootstrap style alerts](http://getbootstrap.com/components/#alerts) can be used by adding the class `.alert`.

<div class="docs-example">
  <div class="alert alert-success" role="alert"><strong>Success!</strong> Add the classes .alert and .alert-success</div>
  <div class="alert alert-info" role="alert"><strong>Info!</strong> Add the classes .alert and .alert-info</div>
  <div class="alert alert-warning" role="alert"><strong>Warning!</strong> Add the classes .alert and .alert-warning</div>
  <div class="alert alert-danger" role="alert"><strong>Danger!</strong> Add the classes .alert and .alert-danger</div>
</div>

The default alert has also been added back as a hack so that the gray alert theme could be used:

<div class="docs-example">
  <div class="alert alert-default" role="alert"><strong>Default!</strong> Add the classes .alert and .alert-default</div>
</div>

And there is also a custom alert that uses the `brand` color (note that the `brand` color for these docs is green!):

<div class="docs-example">
  <div class="alert alert-brand" role="alert"><strong>Branded!</strong> Add the classes .alert and .alert-brand</div>
</div>

