---
title: "JavaScript versions will be retired"
date: "2015-10-26T17:40:00-07:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=855665": "Bug 855665 - Enable let without version=1.7+"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=867609": "Bug 867609 - Retire JavaScript versions"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=867612": "Bug 867612 - Make sure JavaScript version is not used on the web"
---
Traditionally, Firefox has required an explicit version on the [`<script>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/script) element to use some advanced JavaScript features.

```html
<script type="application/javascript;version=1.7"></script>
```

The [`let`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let) statement, standardized in ECMAScript 2015 (ES6), will soon be working without `version=1.7` and later, and this Firefox-specific versioning will be retired.
