---
title: "`DOMQuad.bounds` has been dropped in favour of `getBounds()`"
date: "2019-06-29T22:49:00-04:00"
categories: ["dom"]
tags: []
releases: ["69"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1454622"
      title: "Bug 1454622 - Change DOMQuad bounds to getBounds() as per specification"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/q01sJZp3LH8/discussion"
      title: "Intent to unship: DOMQuad.prototype.bounds"
---
The `bounds` property on the [`DOMQuad`](https://developer.mozilla.org/docs/Web/API/DOMQuad) interface, deprecated since [Firefox 62](https://www.fxsitecompat.dev/en-CA/docs/2018/dompoint-constructor-no-longer-accepts-dompointinit-as-argument-domquad-bounds-has-been-deprecated/), has been removed with Firefox 69, as per the current Geometry Interfaces spec. Given that no other browsers support the property, the compatibility risk should be low. Use the standard `getBounds` method instead.
