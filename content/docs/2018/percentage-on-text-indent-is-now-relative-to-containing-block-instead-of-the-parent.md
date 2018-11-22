---
title: "Percentage on `text-indent` is now relative to containing block instead of the parent"
date: "2018-11-21T17:41:00-05:00"
categories: ["css"]
tags: []
versions: ["65"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1453298"
      title: "Bug 1453298 - percentage text-indent should be relative to the containing block of the text, not the containing block of the block"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1508509"
      title: "Bug 1508509 - text indent isn't hiding text when using %"
---
Previously, when a percentage value was used for the [`text-indent`](https://developer.mozilla.org/docs/Web/CSS/text-indent) CSS property, it was resolved against the content width of the containing block's parent element. It means the following `p` element would have `50px` of indent, not `20px`.

```html
<div style="width: 500px;">
  <p style="width: 200px; text-indent: 10%;">
    Hello World!
  </p>
</div>
```

This weird behaviour has been solved in the latest CSS spec. Firefox 65 has made the change along with Chrome 72, so the value will be resolved against the width of the containing block itself from now on. You may want to double check your stylesheets as indents could be shorter than before in some cases like the example above, which will be `20px` as expected. In fact, the *BBC* homepage is known to be affected.
