---
title: "`line-height` is now applied to `<input>`"
date: "2014-03-21T04:50:04-04:00"
categories: ["css"]
tags: []
versions: ["30"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=349259"
      title: "Bug 349259 – CSS Property \'line-height\' has no effects on input text fields"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=697451"
      title: "Bug 697451 – Allow use of line-height for <input type=\"reset|button|submit\">"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1007454"
      title: "Bug 1007454 – Regression: Text on buttons on Ikea website are cut off"
---
Until now, Firefox has ignored the [`line-height`](https://developer.mozilla.org/docs/Web/CSS/line-height) property specified on the [`<input>`](https://developer.mozilla.org/docs/Web/HTML/Element/input) element, and always applied [`normal`](https://developer.mozilla.org/docs/Web/CSS/normal), while Internet Explorer and WebKit-based browsers allow authors to increase (but not decrease) the value. To improve interoperability, this behaviour has been changed to accept author-defined values. For backward compatibility, single-line text `<input>` elements still cannot have a `line-height` smaller than `1`.

A regression from this change has been found on *IKEA.com* where the `line-height` is `1px`, though this is considered intentional.
