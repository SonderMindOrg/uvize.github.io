---
layout: style-guide
title: Forms | Uvize Style Guide
---

# Forms

The basics of [Bootstrap's Form Element Conventions](http://getbootstrap.com/css/#forms) are utilized.

Here are some custom design patterns used in the Uvize app.


### Hero Check Boxes

Create a custom checkbox via the `.hero-checkbox` modifier to Bootstraps `.checkbox` wrapper. Note that the order of the markup for hero checkboxes is relevant. The `<input>` element must come directly before the `<label>`.

<div class="docs-example">
  <div class="row">
    <div class="col-sm-9">
      <div class="checkbox hero-checkbox">
        <input id="user_mentor" type="checkbox">
        <label for="user_mentor">Default</label>
      </div>
    </div>
  </div>
</div>

### Hero Radios

The same pattern can be used for radio buttons via the `.hero-radio` class.

<div class="docs-example">
  <div class="row">
    <div class="col-sm-9">
      <div class="radio hero-radio">
        <input id="radio_one" name="radio_example" type="radio" checked>
        <label for="radio_one">Option One</label>
      </div>
      <div class="radio hero-radio">
        <input id="radio_two" name="radio_example" type="radio">
        <label for="radio_two">Option Two</label>
      </div>
    </div>
  </div>
</div>


### Caps Labels

Newer style forms in the settings modal have a custom style that will be applied to and `<label>` with the `.control-label` class:

<div class="docs-example ">
  <div class="sidebar-modal modal-main-content" style="position:static">
    <div class="modal-main-content" style="position: static; padding: 0;">
      <div class="row">
        <div class="col-smp-9">
          <div class="form-group">
            <label class="control-label" for="user_first_name">First Name:</label>
            <input id="user_first_name" name="first_name" type="text" class="form-control">
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

