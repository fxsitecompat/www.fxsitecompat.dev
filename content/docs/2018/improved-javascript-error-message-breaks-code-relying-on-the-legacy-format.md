---
title: "Improved JavaScript error message breaks code relying on the legacy format"
date: "2018-09-22T14:42:00-04:00"
categories: ["javascript"]
tags: []
releases: ["63"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1259822"
      title: "Bug 1259822 - Improve the error message produced when a user attempts to access a property of [something that evaluated to] undefined."
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1488417"
      title: "Bug 1488417 - Even better error message on property access on undefined/null variable"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1490772"
      title: "Bug 1490772 - pro.beefree.io - blank page after 1259822 landed"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1498257"
      title: "Bug 1498257 - Infinite loop loading Flipkart.com because the site's regex fails to match Firefox's JS error message"
---
In an effort to make console outputs easier to understand for web developers, Firefox 63 and 64 have improved a JavaScript error message that will be produced when attempting to access a property of `undefined`. For example,

```js
window.x.y
// Firefox 62:
//// TypeError: window.x is undefined
// Firefox 63:
//// TypeError: window.x is undefined, can't access property "y" of it
// Firefox 64:
//// TypeError: window.x is undefined; can't access its "y" property
```

While these changes look harmless, there's a report of a broken site where the page becomes completely blank. Mozilla developers have figured out the cause was the site's code parsing JavaScript error messages with a regular expression for their own error handling. The notified webmaster has fixed the issue before the final release of Firefox 63.

Given that the format of error messages is not standardized in the ECMAScript spec, web developers are discouraged to use them programmatically.

**Update**: *Flipkart* is known to be affected by this change.

**Updated 2** This change has been backed out from Firefox 63 Release Candidate 2.
