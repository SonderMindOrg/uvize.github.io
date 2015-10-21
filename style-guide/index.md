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

Refer to the official Bootstrap documentation for details of the frameworks markup / styles design patterns:

<a class="btn btn-success btn-lg">Show Bootstrap Docs &rsaquo;</a>



### CSS Architecture

The less precompiler is used

documentation on less here

IE 9 hack.. split..

Color themeing, more detail here


### Modifications to Frameworks

The core code of frameworks should never be edited directly. This makes it to complete minor version updates (by simply replacing the entire folder for Bootstrap etc), and easier to track where customisations have been made.

If a file from the framework is edited, comment out the link to the previous file in the master `index-lib.less` or `index-uvize.less`, and import a modified version from a separate folder, i.e. `/hacks/` along with a brief comment explaining the changes.

eg

```
// Components
@import "twitter/bootstrap/component-animations";
//@import "icons/glyphicons"; // Using modified version above that uses asset-url 
@import "twitter/hacks/dropdowns"; // Tweaked version allows <span> as well as <a>
```

