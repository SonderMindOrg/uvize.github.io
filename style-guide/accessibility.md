---
layout: style-guide
title: Accessibility | Uvize Style Guide
---

# Accessibility

Uvize follows accessibility practices in alignment with Federal procurement requirements according to [Section 508](http://webaim.org/standards/508/checklist).  

### Testing & Development

The [Wave Website Accessibility Evaluation Tool](http://wave.webaim.org/extension/) is a useful browser extension for checking a range of accessibility concerns.

[Chromevox](http://www.chromevox.com/) is a screenreader that is available for free to use with Chrome.


### Colors and Contrast

Because organizations can specify a custom `brand` and `highlight` color there is potential for these to not meet color contrast requirements.

The `brand` color should meet contrast requirements on a white background, whereas the `highlight` color should meet contrast requirements against a dark gray (`#3A454D`) background.

Check color contrast using the [Web Aim Color Contrast Checker](http://webaim.org/resources/contrastchecker/)


### Links and Buttons

Links and buttons that trigger script actions (as opposed to using an `href`) don't work correctly when navigated via the keyboard / a screenreader app.

In cases where it is semantically correct, use `<button>` as opposed to `<a>` to remedy this, and improve the quality of markup.
  
In cases where `<button>` is not appropriate, add the attribute `ariaButton` - a custom directive will apply extra attributes needed to give the element tab focus and clickability, i.e:
  
`<a ng-click="getMentor()" ariaButton>Show mentor</a>`

### Forms

In cases where a form element doesn't have an associated `<label>` be sure to add a description via `aria-label`.
  
i.e.:
`<input type="email" aria-label="Email Address:" placeholder="name@example.com"/>`


### Bootstrap

Uvize uses the Bootstrap framework which includes considerations for accesibility. When using elements from the framework such as dropdowns, modals, close buttons, etc, be sure to correctly maintain accessibility features from the specified examples.

