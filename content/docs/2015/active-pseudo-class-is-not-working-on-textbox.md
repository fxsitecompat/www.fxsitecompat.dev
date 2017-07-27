---
title: "`:active` pseudo-class is not working on textbox"
date: "2015-10-21T02:20:00-07:00"
categories: ["css"]
tags: []
versions: ["38"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1168055"
      title: "Bug 1168055 - Active Pseudo class not working for textbox in firefox 38"
---
Firefox 38 has a regression where the [`:active`](https://developer.mozilla.org/en-US/docs/Web/CSS/:active) CSS pseudo-class is not applied to the [`<input>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input) and [`<textarea>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/textarea) elements. This bug has been fixed with Firefox 39.
