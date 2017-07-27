---
title: "JavaScript versions will be retired"
date: "2015-10-26T17:40:00-07:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=867609"
      title: "Bug 867609 - Retire JavaScript versions"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=867612"
      title: "Bug 867612 - Make sure JavaScript version is not used on the web"
---
Traditionally, Firefox has required an explicit version on the [`<script>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/script) element to use some advanced JavaScript features.

```html
<script type="application/javascript;version=1.7"></script>
```

Starting with Firefox 44, the [`let`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let) statement [no longer requires an explicit JavaScript version](https://www.fxsitecompat.com/en-CA/docs/2015/let-statement-no-longer-requires-explicit-javascript-version/), and this Firefox-specific versioning will soon be retired.
