---
layout: style-guide
title: Theming | Uvize Style Guide
---

# Custom Themes for Orgs

Uvize is developed so each instance can be skinnable with a custom color scheme and logo.

Each org has a `brand` color and a `highlight` color.

The `brand` color should contrast with white backgrounds, the `highlight` color should stand out on dark / black backgrounds.

The `highlight` color can match the `brand` color if it contrasts well on both white and black, it can be a lighter tint of the `brand` color, or a lighter complimentary color from the organization's marketing guidelines.

### Logos

Only one logo file is required for each org.

It should be the wide version of the logo, and simple enough to read well at small sizes.

Because the logo is potentially shown on different light color backgrounds it **must** be a transparent `.png` file with no background color.

The pixel dimensions for the file are as follows:

- **Width:** Maximum of 420px
- **Height:** Exactly 84px

Transparent padding above and below the logo to fill out the height is acceptable if neccesary, but no horizontal padding should ever be added.

The logo will display on screen at half this size (the extra resolution is to accomodate @2x retina screens)

Example logo file:

<span class="community-logo-full">
    <img class="logo-img" src="/gfx/style-guide/Staff-Edition.png" alt="Staff Edition">
</span>
<br /><br />


### CSS swatches for Orgs

Each org has its own swatch file. Both the `brand` and `highlight` color can be set here.

These colors are set as less variables and compiled into the master styles for the site.

For each org 3x less files need to be created in `app/assets/stylesheets/`:

1. `application-<org_canonical_name>-lib.less` 
2. `application-<org_canonical_name>-uvize.less` 
3. `swatches/<org_canonical_name>.less`

Sheets 1. and 2. are neccesary because the `canonical_name` for the org is not currently available in the CSS, hence its hard coding into the file name.

These sheets contain a minimum of code, they load the main less files along with the correct swatch, heres how they would look for an org with `wcu` as its `canonical_name`:

```
/* wcu (application-wcu-lib.less) */
@import "swatches/wcu.less";
@import "index-lib.less";
```
```
/* wcu (application-wcu-uvize.less) */
@import "swatches/wcu.less";
@import "index-uvize.less";
```


The swatch sheet itself also includes options to set the color of the dark sidebar, the tone of the default blue/green used on links/alerts, and branded color themed alerts that are derived from the `brand_color`. 

```
/* WCU SWATCH (swatches/wcu.less) */

// PRIMARY BRAND COLOR
@swatch-brand: #8CCF62; // Brand

// PRIMARY HIGHLIGHT COLOR
@swatch-highlight: #8CCF62; // Brand Color, lightened if needs be, or light alt color

// BOOK COLOR (deprecated)
@book-color: @swatch-brand;

// COMPLIMENTARY DARK COLOR (Sidebar BG and darkest text)
@swatch-dark: #3A454D; // Dark Blue

// BRAND INFO
@swatch-info: #478DC8;// The default blue used across the site

// BRAND SUCCESS
@swatch-success: #8ccf62;// A default green for success messages etc

// BRAND LIGHT BG
@swatch-brand-light-bg: lighten(@swatch-brand, 30%);

// BRAND DARK TEXT
@swatch-brand-dark-text:  darken(spin(@swatch-brand, -10), 20%);
```


### Setting Brand Color in the DB

When adding an org via the admin tools it is also neccesary to specify the main `brand` color.

Additional css rules are written into the `<head>` of the app for each org a user is a member of so that the `brand` color for multiple orgs can be used alongside the main precompiled theme.

Heres an example of the classes that can be used to apply those colors:

```
.wcu-content .highlight-color {color: #8CCF62!important;}
.wcu-content .highlight-bg {background-color: #8CCF62!important;}
.wcu-content .highlight-border {border-color: #8CCF62!important;}
.wcu-content .item-flag {background-color: #8CCF62!important;}
.wcu-content .item-flag:after {border-top-color: #8CCF62!important;}
```


### Process for Adding and Testing an Org Locally

Here are some simple steps you can follow to cover all the basics of adding an org and testing the colors appear correctly:

- Create the less files and set the correct color values in the swatch.
- Create a logo `.png` file, 
- Name it after the `name` of the org with `-` in the place of any spaces (i.e. `Western-Carolina-University.png` and save it to `db/img/orgs`
- Add basic org data to your local seed data in `db/data/orgs.csv`

  ```
name,activation_code,short_name,canonical_name,community_title,org_type,swatch_highlight
Western Carolina University,wcu,WCU,wcu,Veterans,school,#8CCF62
  ````

- Reseed your local data
```` 
$ bundle exec rake db:drop db:create db:migrate db:seed
````

- Start your local dev environment and visit the sign up page. Add the `canonical_name` as a URL param, i.e. `http://localhost:5000/users/sign_up?c=wcu`
- Check that the background color of the alert looks good, maybe you will need to adjust the lightness in the swatch file.
<br /><br />
<img class="img-responsive" src="/gfx/style-guide/wcu-join.jpg" alt="WCU Example" />
<br />
- Create a new user account and view the welcome page. Does the `highlight` color stand out well on the sidebar buttons? Does the `brand` color stand out well on the buttons on white? If not you may need to tweak the swatch file / try different values.
<br /><br />
<img class="img-responsive" src="/gfx/style-guide/wcu-login.jpg" alt="WCU Example" />
<br /><br />
**Troubleshooting**

* DB won't reseed?
 - Check that you have named the logo correctly.
 
* Correct CSS swatches not loading?
 - Check the `canonical_name` is correct through all less files and file names.
 - Make sure the `canonical_name` is set correctly in the sample data.


 
