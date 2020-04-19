---
title: "`let` statement no longer requires explicit JavaScript version"
date: "2015-10-28T02:02:00-07:00"
categories: ["javascript"]
tags: []
versions: ["44", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=855665"
      title: "Bug 855665 - Enable let without version=1.7+"
aliases:
    - "/en-CA/docs/2015/let-statement-no-longer-requires-explicit-javascript-version-in-non-strict-mode/"
---
Previously, the [`let`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/let) statement required an explicit JavaScript version, specifically [1.7](https://developer.mozilla.org/docs/Web/JavaScript/New_in_JavaScript/1.7) or later, on the [`<script>`](https://developer.mozilla.org/docs/Web/HTML/Element/script) element like this:

```html
<script type="application/javascript;version=1.7"></script>
```

The `let` statement has been standardized in ECMAScript 2015 (ES6) and therefore such a version is no longer required to use it. This change should be backward compatible, but [let us know](https://www.fxsitecompat.dev/en-CA/contribute/) if you find any issues (pun intended). The non-standard JavaScript versioning will be [completely retired](https://www.fxsitecompat.dev/en-CA/docs/2015/javascript-versions-will-be-retired/) in the near future.
