---
title: "Support for `Event.returnValue` has been added"
date: "2018-08-14T19:14:00-04:00"
categories: ["dom"]
tags: []
versions: ["63"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=218415"
      title: "Bug 218415 - Request for window.event object added to DOM to ease cross browser scripting"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1452569"
      title: "Bug 1452569 - Implement Event's returnValue"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1479964"
      title: "Bug 1479964 - Tracking event.keyCode issue due to the implementation of window.event"
aliases:
    - "/en-CA/docs/2018/window-event-has-been-added-for-compatibility-but-some-browser-detections-are-broken/"
    - "/en-CA/docs/2018/support-for-window-event-and-event-returnvalue-has-been-added"
---
Firefox 63 has implemented the [`window.event`](https://developer.mozilla.org/docs/Web/API/Window/event) property, which is derived from Internet Explorer but now standardized in the DOM spec along with `Event.prototype.srcElement` and `Event.prototype.returnValue`.

While this change aims at improving web compatibility, it's expected that certain browser detection code using the once-non-standard property will rather be broken. A typical case already reported involves `event.keyCode` returning `0` in Firefox, which is being solved by Mozilla engineers. There might be other issues, so please scan your code and, if `window.event` is found, make sure the functionality works with Firefox.

Note that the support for `srcElement` has already been [added with Firefox 62](https://www.fxsitecompat.com/en-CA/docs/2018/support-for-event-prototype-srcelement-has-been-added/), and it also causes at least one compatibility issue.

**Update**: The [`Event.prototype.returnValue`](https://developer.mozilla.org/docs/Web/API/Event/returnValue) property has also been added with Firefox 63. The title of this post has been updated accordingly.

**Update 2**: `window.event` is not going to ship with Firefox 63 due to several compatibility issues, mainly because Firefox doesn't support the `keyCode` property on it. Now `window.event` is [disabled](https://bugzilla.mozilla.org/show_bug.cgi?id=1493869) on non-Nightly channels. The title of this post has been updated again.

**Update 3**: The support for `Event.returnValue` has been [temporarily disabled](https://bugzilla.mozilla.org/show_bug.cgi?id=1510985) in Firefox 64 due to some broken web apps. It will be enabled again with Firefox 65 after the `keypress` event's compatibility issue is solved.
