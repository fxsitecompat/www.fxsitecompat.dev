---
title: "Type of `CSS` interface has been changed from `function` to `object`"
date: "2018-05-07T21:30:00-04:00"
categories: ["css", "dom"]
tags: []
versions: ["61"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1455805"
      title: "Bug 1455805 - Make \"CSS\" a namespace, not interface"
---
The [`CSS`](https://developer.mozilla.org/en-US/docs/Web/API/CSS) interface has internally become a namespace after a [discussion](https://github.com/w3c/csswg-drafts/pull/437) in the CSS Working Group. According to the change, `typeof CSS` now returns `"object"` instead of `"function"` so be careful when implementing feature detection with it.

```js
// This will no longer work
if (typeof CSS === 'function' && typeof CSS.supports === 'function') {
  // CSS.supports is available
}

// Do this
if (typeof CSS !== 'undefined' && typeof CSS.supports === 'function')

// or this
if ('CSS' in window && typeof CSS.supports === 'function')
```
