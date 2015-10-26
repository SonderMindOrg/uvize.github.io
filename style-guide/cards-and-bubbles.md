---
layout: style-guide
title: Cards & Bubbles | Uvize Style Guide
---

# Cards and Bubbles

A commonly used layout pattern is for content to be displayed on a `.card`.

The `.card` style (internal padding, a light border and a drop shadow) can be applied to any sort of content. 

If the card is a link (`<a href="..." class="card">...</a>`) the card will have `:hover` styles. You can fake these behaviours by applying the `.fake-hover` modifier (if the element is not an `<a>` or lacks a typical `href`).

Heres an example of cards used within a two column grid.

<div class="docs-example">
  <div class="row">
    <div class="col-sm-9">
      <a href="#" class="card">
        <h2>Title A</h2>
        <p>Card is Link</p>
      </a>
    </div>
  
    <div class="col-sm-9">
      <div href="#" class="card fake-hover">
        <h2>Title B</h2>
        <p>Fake Hover</p>
      </div>
    </div>
  </div>
</div>


### Chat Bubbles

When a `.card` is placed inside a `.chat-block` it can be extended to become a `.chat` and combined with other layout patterns.

Here is a common example where an avatar layout class (`.avatar-med-left`), an avatar (`.avatar-item > .avatar-med`), a chat card (`.card.chat`), a `.title-bar` and a `.bubble-inner` are combined to make a chat bubble that will respect OOCSS responsive rules applied to all of the above patterns:

<div class="docs-example">
  <div class="chat-block">
    <div class="avatar-med-left">
      <!-- Avatar -->
      <div class="avatar-item">
        <img class="avatar-med" src="/gfx/style-guide/davecass.jpg">
      </div>
      <!-- Chat Card -->
      <div class="chat card ">
        <div class="title-bar">
          <a class="username">Username</a> Some text
        </div>
        <div class="bubble-inner">
          <p>Content</p>
        </div>
      </div>      
    </div>
  </div>
</div>


### Action Cards

The `.action-card` design pattern combines the above layouts with `.alert` classes in order to present distinctive prompts to action.

Here is an example of the default `.action-card` modifier with a `.title-bar`, `.bubble-inner'` and `.btn-row`:

<div class="docs-example">
  <div class="chat-block">
    <div class="avatar-med-left">
      <!-- Avatar -->
      <div class="avatar-item">
        <img class="avatar-med" src="/gfx/style-guide/davecass.jpg">
      </div>
      <!-- Chat Card -->
      <div class="card action-card chat">
        <div class="title-bar">
          <h1 class="logo-left">
            <span class="pad-icon-right hide-collapsed hidden-smp-inline"><span class="glyphicon-full glyphicon-download-right"></span></span>Do Something</h1>
        </div>
        <div class="bubble-inner">
          <p>If you don't want to do the main thing, maybe <a class="accent-link add-arrow" href="#">Do this</a></p>
        </div>
        
        <!-- Btn Row Options -->
        <div class="btn-row x2 base-bar">
          <a class="icon-btn">
            <span class="glyphicon-full glyphicon-remove"></span>
            No
          </a>
          <a class="icon-btn highlight-btn">
            <span class="glyphicon-full glyphicon-ok"></span>
            Yes
          </a>
        </div>
        
      </div>      
    </div>
  </div>
</div>


Here is a simpler version with just a `.bubble-inner` and an `.alert` class of `.alert-info`:

<div class="docs-example">
  <div class="chat-block">
    <div class="avatar-med-left">
      <!-- Avatar -->
      <div class="avatar-item">
        <img class="avatar-med" src="/gfx/style-guide/davecass.jpg">
      </div>
      <!-- Chat Card -->
      <div class="card action-card chat alert alert-info">
        <div class="bubble-inner">
          <p>Here is an important prompt added into a feed. <a class="accent-link add-arrow" href="#">Do this</a></p>
        </div>
      </div>      
    </div>
  </div>
</div>

And the pattern can also be used outside of the `.chat-block` layout:

<div class="docs-example">

    <!-- Chat Card -->
    <div class="card action-card">
      <div class="title-bar">
        <h1 class="logo-left">
          <span class="pad-icon-right hide-collapsed hidden-smp-inline"><span class="glyphicon-full glyphicon-download-right"></span></span>Start Something</h1>
      </div>
      <div class="bubble-inner">
        <p>Heres a gentle hint. <a class="accent-link add-arrow" href="#">Do this</a></p>
      </div>
      
    </div>      

</div>





