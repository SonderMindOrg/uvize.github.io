---
layout: style-guide
title: Grid and Layout | Uvize Style Guide
---

# Grid & Layout

The site uses the [Bootstrap grid](http://getbootstrap.com/css/#grid) and is based off an 18 column layout. 

Each major column of the grid matches a `96px` wide `@square-grid` value. The side menu is also sized based on the `@square-grid` size. Most padding is based on a fraction / multiple of `@grid-gutter-width` (`24px`).

The only customization to the grid is the addition of an extra breakpoint to accomodate portrait tablets (`.col-smp-X`).

<div class="docs-example">
<p>This layout will have 3 columns on desktop, 2 columns on a portrait tablet, and collapse to 1 column on mobile:</p>
  <div class="row">
    <div class="col-sm-6 col-smp-9">
      <div class="well">1</div>
    </div>
    <div class="col-sm-6 col-smp-9">
      <div class="well">2</div>
    </div>
    <div class="col-sm-6 col-smp-9">
      <div class="well">3</div>
    </div>
  </div>
</div>

### Button Rows

A custom grid with no gutters is used for rows of large buttons in some places.

Using `.card` class as a base, with `.btn-row` and `.x3` `.icon-btn` buttons:

<div class="docs-example">
  <div class="card btn-row x3">
    <a ng-click="$root.Modal.createEvent($root.user.primary_org.default_group.id)" class="icon-btn">
      <span class="glyphicon-full glyphicon-calendar"></span>
        Standard
    </a>
    <a ng-click="$root.Modal.createEvent($root.user.primary_org.default_group.id)" class="icon-btn">
      <span class="glyphicon-full glyphicon-calendar"></span>
        Standard
    </a>
    <a ng-click="$root.Modal.createEvent($root.user.primary_org.default_group.id)" class="icon-btn highlight-btn">
      <span class="glyphicon-full glyphicon-calendar"></span>
        Highlight
    </a>
  </div>
</div>


### Page Blocks

If a page has multiple major sections they will usually be wrapped in the `.page-block` class to ensure consistent base margins:

<div class="docs-example">
  <div class="page-block">
    <div class="well">Section 1</div>
  </div>
  <div class="page-block">
    <div class="well">Section 2</div>
  </div>
</div>

### Generic Padding

Use the `.padded-section` class to add generic padding to an object. For more padding include the `.medium-padded` modifier, for lots of padding use the `.jumbo-padded` modifier.

The padding will adjust based on responsive breakpoints.

<div class="docs-example">
  <div class="padded-section" style="border: solid #ccc 1px">
    <div class="well" style="margin: 0">Item in Padded Section</div>
  </div>
  <br>
  <div class="padded-section medium-padded" style="border: solid #ccc 1px">
    <div class="well" style="margin: 0">Item in Medium Padded Section</div>
  </div>
  <br>
  <div class="padded-section jumbo-padded" style="border: solid #ccc 1px">
    <div class="well" style="margin: 0">Item in Jumbo Padded Section</div>
  </div>
</div>  