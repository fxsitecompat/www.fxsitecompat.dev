---
title: "Elements with `dir` attribute will have `unicode-bidi:isolate`"
date: "2016-03-07T11:46:00-05:00"
categories: ["css", "html"]
tags: []
versions: ["47"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1218706"
      title: "Bug 1218706 - Make unicode-bidi: isolate the default for elements with a dir attribute"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1249497"
      title: "Bug 1249497 - Make bdo element use unicode-bidi: isolate-override"
---
The HTML5 spec has changed the semantics of the `dir` attribute to use [`unicode-bidi`](https://developer.mozilla.org/en-US/docs/Web/CSS/unicode-bidi)`:isolate-override` instead of `unicode-bidi:bidi-override` on the [`<bdo>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/bdo) element and `unicode-bidi:isolate` instead of `unicode-bidi:embed` on all other elements.

The user agent stylesheet of Firefox has been updated to follow the spec, but `unicode-bidi:bidi-override` is still used on `<bdo>`. This inconsistency will be solved soon. Other elements will have `unicode-bidi:-moz-isolate` on Firefox 47 and later.

**Update**: Firefox 50 and later will use `unicode-bidi:isolate-override` for the `<bdo>` element.
