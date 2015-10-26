---
layout: style-guide
title: Email Templates | Uvize Style Guide
---

# Email Templates

Developing robust HTML email templates is challenging due to the limited capabilities of many email clients, and restrictions they place on the use of CSS.

Uvize uses the [Zurb Ink](http://zurb.com/ink/templates.php) framework as the basis for responsive HTML email template designs.

<a href="http://zurb.com/ink/templates.php" target="blank" class="btn btn-success btn-lg">Show Ink Docs &rsaquo;</a>
<br/><br/>

### Inlining

Often styles for a template need to be inlined (we don't have automatic inlining set up for all mail unfortunately).

To make this more workable there are static, non-inlined, versions of the templates in the at `/misc/email_templates/`.

Edit the static template to perfect your designs / layouts, then use the [Ink Inliner](http://zurb.com/ink/inliner.php) to generate an inlined version to be selectively pasted into the final templates such as `/app/views/layouts/basic_mailer.html.erb`).

<a href="http://zurb.com/ink/inliner.php" target="blank" class="btn btn-success btn-lg">Ink Inliner &rsaquo;</a>
<br/><br/>