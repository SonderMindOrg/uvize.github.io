---
layout: style-guide
title: Cards & Bubbles | Uvize Style Guide
---

# Avatars

Custom classes to crop Avatars into a round shape and set sizes that respond to different screen sizes. If a user doesn't have an icon set the server will return a default icon.

Use classes `.avatar-xx-small`, `.avatar-x-small`, `.avatar-small`, `.avatar-med`, `.avatar-large`, `.avatar-x-large`, `.avatar-xx-large` for the full range of sizes:

<div class="docs-example">
  <img class="avatar-xx-small" src="/gfx/style-guide/davecass.jpg">&nbsp;
  <img class="avatar-x-small" src="/gfx/style-guide/davecass.jpg">&nbsp;
  <img class="avatar-small" src="/gfx/style-guide/davecass.jpg">&nbsp;
  <img class="avatar-med" src="/gfx/style-guide/davecass.jpg">&nbsp;
  <img class="avatar-large" src="/gfx/style-guide/davecass.jpg">&nbsp;
  <img class="avatar-x-large" src="/gfx/style-guide/davecass.jpg">&nbsp;
</div>

### Avatar Labels

Wrap avatars in the `.avatar-item` class if you want to include a `.user-label` label. Mentors use the `.label-info` modifier class, Staff `.label-success`, and there is a custom `.label-uvize` class

<div class="docs-example clearfix">
  <div class="avatar-med-left" style="float: left;">
    <a class="avatar-item">
      <img class="avatar-med" src="/gfx/style-guide/davecass.jpg">
      <div class="labels">
        <span class="label label-info user-label">mentor</span>
      </div>
    </a>
  </div>
  
  <div class="avatar-med-left" style="float: left;">
    <a class="avatar-item">
      <img class="avatar-med" src="/gfx/style-guide/davecass.jpg">
      <div class="labels">
        <span class="label label-success user-label">staff</span>
      </div>
    </a>
  </div>
  
  <div class="avatar-med-left" style="float: left;">
    <a class="avatar-item">
      <img class="avatar-med" src="/gfx/style-guide/davecass.jpg">
      <div class="labels">
        <span class="label label-uvize user-label">uvize</span>
      </div>
    </a>
  </div>
</div>
<br>

### Avatar Layout Patterns

If you are using the common pattern of having an avatar in the left margin of a responsive block of text use classes like `.avatar-xx-small-left`, `.avatar-x-small-left`, `.avatar-small-left`, `.avatar-med-left`, `.avatar-med-right`, `.avatar-large-left` to wrap the content.

<div class="docs-example">
  <div class="avatar-med-left">
   <a class="avatar-item">
     <img class="avatar-med" src="/gfx/style-guide/davecass.jpg">
     <div class="labels">
       <span class="label label-info user-label">mentor</span>
     </div>
   </a>
   <a class="username">Dave Cass</a>
   <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
  </div>
</div>




