---
title: "`requestAnimationFrame` and `cancelAnimationFrame` have been unprefixed"
date: "2013-04-06T04:52:59-04:00"
categories: ["dom"]
tags: []
versions: ["23"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=704063"
      title: "Bug 704063 – Add unprefixed requestAnimationFrame"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=876282"
      title: "Bug 876282 – Add unprefixed cancelAnimationFrame"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=753453"
      title: "Bug 753453 – requestAnimationFrame callback should return DOMHighResTimeStamp"
---
[`requestAnimationFrame`](https://developer.mozilla.org/docs/Web/API/window.requestAnimationFrame), the unprefixed version of `mozRequestAnimationFrame`, has been added. This unprefixed method passes a [`DOMHighResTimeStamp`](https://developer.mozilla.org/docs/Web/API/DOMHighResTimeStamp) to callbacks. It has microsecond precision and can be compared to [`performance.now`](https://developer.mozilla.org/docs/Web/API/window.performance.now).

On the other hand, the prefixed method, which will be removed in the future, continues to pass an epoch-based [`DOMTimeStamp`](https://developer.mozilla.org/docs/Web/API/DOMTimeStamp) to callbacks. The passed-in value has millisecond precision and can be compared to [`mozAnimationStartTime`](https://developer.mozilla.org/docs/Web/API/window.mozAnimationStartTime).

The unprefixed [`cancelAnimationFrame`](https://developer.mozilla.org/docs/Web/API/window.cancelAnimationFrame) method has also been added. It has the same behaviour as the prefixed `mozCancelAnimationFrame` method. Those `moz`-prefixed methods will be removed in the future.

**Update**: Those prefixed methods have been [removed with Firefox 42](https://www.fxsitecompat.com/en-CA/docs/2015/mozrequestanimationframe-and-related-apis-have-been-removed/).
