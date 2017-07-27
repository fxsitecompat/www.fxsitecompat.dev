---
title: "`UIEvent.isChar` has been removed"
date: "2017-03-18T21:48:00-04:00"
categories: ["dom"]
tags: []
versions: ["55"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1347073"
      title: "Bug 1347073 - Get rid of UIEvent.isChar because no other browsers support it"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/IVcGOOeOThw/discussion"
      title: "Intent to remove UIEvent.isChar"
---
The non-standard [`UIEvent.prototype.isChar`](https://developer.mozilla.org/en-US/docs/Web/API/UIEvent/isChar) property has been removed with Firefox 55. It was always returning `false` on platforms other than macOS, and is not supported by any other browsers.
