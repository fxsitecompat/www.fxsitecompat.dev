---
title: "`DOMMatrix.scaleNonUniformSelf()` has been dropped in favour of `scaleSelf()`"
date: "2019-07-06T21:58:00-04:00"
categories: ["dom"]
tags: []
releases: ["69"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1560119"
      title: "Bug 1560119 - Remove DOMMatrix.prototype.scaleNonUniformSelf()"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/r4B80kbt3FA/discussion"
      title: "Intent to unship: DOMMatrix.prototoype.scaleNonUniformSelf()"
---
The `scaleNonUniformSelf` method has been removed from the `DOMMatrix` interface with Firefox 69, since the Geometry Interfaces spec renamed it to `scaleSelf` back in 2016. Use the newer method from now on.
