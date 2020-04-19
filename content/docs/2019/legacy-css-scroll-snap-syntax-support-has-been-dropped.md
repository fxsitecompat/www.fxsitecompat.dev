---
title: "Legacy CSS Scroll Snap syntax support has been dropped"
date: "2019-05-28T05:04:00-04:00"
categories: ["css"]
tags: []
versions: ["68", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1312163"
      title: "Bug 1312163 - Update 'scroll-snap-type' to the latest specification and drop support for 'scroll-snap-type-x' and 'scroll-snap-type-y'"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1544136"
      title: "Bug 1544136 - Ship the new scroll snap"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/s0rMvOBnO_4/discussion"
      title: "Intent to implement and ship the CSS Scroll Snap Module Level 1 and unship old scroll snap properties"
---
Firefox 68 has implemented the [latest CSS Scroll Snap spec](https://drafts.csswg.org/css-scroll-snap-1/) that has been revised significantly since the [initial implementation](https://hacks.mozilla.org/2015/09/scroll-snapping-explained/) was shipped with Firefox 39. While Chrome and Safari have already added the support for the new syntax, the changes in Firefox are not backward-compatible:

* The `scroll-snap-coordinate`, `scroll-snap-destination`, `scroll-snap-type-x` and `scroll-snap-type-y` properties have been dropped
* The `scroll-snap-type` property has become a longhand, so the old shorthand syntax like `scroll-snap-type:mandatory` will stop working

Be sure to update your stylesheets accordingly for the new syntax if you have already utilized Scroll Snap.
