---
layout: style-guide
title: Welcome | Uvize Style Guide
---

#Getting Started

>Welcome! What follows is a guide for designers and front end developers who wish to work on the Uvize **web app** and **marketing site**.

Uvize is an [Angular JS](https://angularjs.org/) / [Rails app](http://rubyonrails.org/). The web app primarily uses Angular for templating, so content is not shown for users who have Javascript disabled (a warning is shown). Marketing site content and login pages however are built on static HTML / Rails and visible to users regardless of javascript settings / browser capabilities.

Javascript aside, modern markup and CSS properties degrade gracefully for older devices, and should be structurally and sematically correct for screen readers.

Uvize is designed primarily as a desktop web app, but utilizes responsive design to also present as a highly functional mobile web app.

This documentation uses a compiled version of the actual [uvize.com](http://uvize.com) css, so examples and content here should be consistent with uses on the site. In rare cases where a modification specific to the documentation site is present these classes will be prefixed `.docs-`.

### Targeted Browsers

Desktop: 

- Recent versions of Chrome, Firefox, Safari. 
- IE 9 and higher.

Mobile: 

- iOS 6.0 and higher. 
- Android 4.0 and higher.


### Frameworks

Uvize is built off Bootstrap 3.

Refer to the official Bootstrap documentation for details of markup / styles design patterns used in the framework:

<a href="http://getbootstrap.com/" target="blank" class="btn btn-success btn-lg">Show Bootstrap Docs &rsaquo;</a>
<br/><br/>

### CSS Architecture

CSS is written in Less, for more information visit [lesscss.org](http://lesscss.org/).

When the rails app is running the less will be compiled automatically so there is no need to run a seperate compiler.

Because of the [theming setup](theming.html) the less is compiled via `@import` through a string of files.

Here is a basic outline of css / less content located at `app/assets/stylesheets/`:


- `index-lib.less` (Compiles code from bootstrap)
- `index-uvize.less` (Compiles custom app css)
- `variables.less` (Customized version of bootstrap variables used by all code)
- `application-<org_canonical_name>-lib.less` (Compiles library code with custom org swatch)
- `application-<org_canonical_name>-lib.less` (Compiles Uvize code with custom org swatch)
- `/uvize/` (Aapp specific less files)
- `/swatches/` (Org swatch vars)
- `/twitter/bootstrap/` (Raw Bootstrap source files)
- `/twitter/hacks/` (Modified versions of bootstrap source files)
- `/icons/` (Less files for icon sets)
- `/other/` (CSS used by other third party libraries)



The css is split between code from bootstrap (`index-lib.less`)and custom uvize styles(`index-uvize.less`) - an unfortunate workaround to accomodate IE 9's [4095 rule limit](http://blogs.msdn.com/b/ieinternals/archive/2011/05/14/internet-explorer-stylesheet-rule-selector-import-sheet-limit-maximum.aspx). 

### Modifications to Frameworks

Where possible the core code of frameworks has not been edited directly. This makes it to complete minor version updates without overwriting changes (by simply replacing the entire folder for Bootstrap etc), and easier to track where customisations have been made.



