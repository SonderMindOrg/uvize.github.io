---
layout: style-guide
title: Buttons | Uvize Style Guide
---

# Buttons

All the [Bootstrap button conventions](http://getbootstrap.com/css/#buttons) can be used to generate different sizes and colors of buttons. 

Buttons are styled to be flat and solid color, `.btn-primary` matches the `brand` color for the org. The default button is an exception in that it is gray with shading:

<div class="docs-example">
  <button type="button" class="btn btn-primary">Primary</button>
  <button type="button" class="btn btn-success">Success</button>
  <button type="button" class="btn btn-info">Info</button>
  <button type="button" class="btn btn-warning">Warning</button>
  <button type="button" class="btn btn-danger">Danger</button>
  <button type="button" class="btn btn-link">Link</button>
  <button type="button" class="btn btn-default">Default</button>
</div>

### Main Button Design Patterns

If a button will result in a 'final' action like creating a post, or saving changes as opposed to navigation step it should have the `.btn-action` class applied which pushes the text into caps:

<div class="docs-example">
  <button type="button" class="btn btn-primary btn-action">Action</button>
</div>

Cancel buttons will typically be shown as a link style button next to an action:

<div class="docs-example clearfix">
  <button type="button" class="btn btn-primary btn-action pull-right">Action</button>
  <button type="button" class="btn btn-link pull-right">Cancel</button>
</div>


### Light Text Buttons

Less consequential actions use link style buttons with the custom `.light-txt-btn` modifier to create bold gray text. These buttons will also typically include an icon, or be an icon with no text:

<div class="docs-example">
  <a class="btn btn-link light-txt-btn">
    Comment &nbsp;<span class="glyphicon glyphicon-comment"></span>
  </a>
</div>

To space a set of buttons for actions on a post wrap them in a `<ul>` with the class `.post-interactions-mini`:

<div class="docs-example">
  <ul class="post-interactions-mini">
    <li>
      <a class="btn btn-link light-txt-btn">
        <span class="glyphicon glyphicon-comment"></span>
      </a>
    </li>
    <li>
      <a class="btn btn-link light-txt-btn">
        <span class="glyphicon glyphicon-pencil"></span>
      </a>
    </li>
  
    <li>
      <a class="btn btn-link light-txt-btn">
        <span class="glyphicon glyphicon-trash"></span>
      </a>
    </li>
  </ul>
</div>

### Hover Reveal

For buttons you want to reveal only when an item is hovered you can use the `.hover-reveal` pattern. Add the class `.hover-parent` to choose a parent item that will trigger the reveal, and add `.hover-reveal` to any items you want to hide.

The buttons will only hide on desktop browsers not touch devices.

<div class="docs-example hover-parent">
  <ul class="post-interactions-mini">
    <li>
      <a class="btn btn-link light-txt-btn">
        <span class="glyphicon glyphicon-comment"></span> Always Show
      </a>
    </li>
    <li>
      <a class="btn btn-link light-txt-btn hover-reveal">
        <span class="glyphicon glyphicon-pencil"></span> Show On Hover
      </a>
    </li>
  </ul>
</div> 

### Action Links

Sometimes the class `.accent-link` is used to give emphasis to an inline link instead of using a button:

<div class="docs-example">
  <a class="accent-link">
    Accent Link
  </a>
</div>

To add a cheveron to the right of the link use `.add-arrow`:

<div class="docs-example">
  <a class="accent-link add-arrow">
    Accent Link with Arrow
  </a>
</div>


### Button Groups

[Bootstrap Button groups](http://getbootstrap.com/components/#btn-groups) can be used, although typically only with the `default` button style. 

If multiple elements are shown / hidden based on the angular templating be sure to use `ng-if` so that hidden buttons do not interfere with `:first-child` `:last-child` style rules:

<div class="docs-example">
  <div class="btn-group" role="group" aria-label="...">
    <button type="button" class="btn btn-default">Left</button>
    <button type="button" class="btn btn-default">Middle</button>
    <button type="button" class="btn btn-default">Right</button>
  </div>
</div>
