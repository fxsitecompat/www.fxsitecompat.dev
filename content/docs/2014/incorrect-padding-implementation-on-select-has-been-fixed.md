---
title: "Incorrect `padding` implementation on `<select>` has been fixed"
date: "2014-03-21T04:50:04-04:00"
categories: ["css"]
tags: []
releases: ["30", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=963970"
      title: "Bug 963970 – Arrow of drop-down list should not be affected by padding"
---
Firefox's incorrect implementation of [`padding`](https://developer.mozilla.org/docs/Web/CSS/padding) on the [`<select>`](https://developer.mozilla.org/docs/Web/HTML/Element/select) element has been fixed. Now `padding` spaces are added inside the dropdown list, instead of outside, to match with the CSS spec and other browsers' behaviour. This issue was found while developers were working on the same issue on the [`<textarea>`](https://developer.mozilla.org/docs/Web/HTML/Element/textarea) element [fixed with Firefox 29](https://www.fxsitecompat.dev/en-CA/docs/2014/incorrect-padding-implementation-on-textarea-has-been-fixed/). `<select>` elements with the `multiple` attribute won't be affected by this change.

A hack using `-moz-appearance:none` to hide the drop-down arrow no longer works, though there are [requests to allow styling of the arrow](https://bugzilla.mozilla.org/show_bug.cgi?id=649849). Page authors should create a custom element instead if you'd like to totally control the design of dropdown lists on all browsers.
