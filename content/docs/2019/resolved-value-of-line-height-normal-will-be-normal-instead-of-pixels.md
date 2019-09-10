---
title: "Resolved value of `line-height:normal` will be `normal` instead of pixels"
date: "2019-09-09T13:35:00-04:00"
categories: ["css", "dom"]
tags: []
versions: ["71"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1536871"
      title: "Bug 1536871 - Return the keyword value for line-height: normal in getComputedStyle."
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1579624"
      title: "Bug 1579624 - Turn the \"line-height computes as normal\" pref on for release users."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/8uvGB3BCpl8/discussion"
      title: "Intent to Ship: line-height returns normal as a resolved value."
---
Starting with Firefox 71, the [resolved value](https://developer.mozilla.org/docs/Web/CSS/resolved_value) of the `line-height` CSS property will be `normal` instead of an actual length if the specified value is `normal` or undefined.

```js
// This can now return `normal` instead of pixels
window.getComputedStyle(element).getPropertyValue('line-height');
```

This change has already been made on the Nightly and early Beta channels since Firefox 69 after a [discussion](https://github.com/w3c/csswg-drafts/issues/3749) in the CSS Working Group, and Mozilla developers haven't seen compatibility issue reports so far. The new behaviour matches Google Chrome. Safari will make the same change soon.
