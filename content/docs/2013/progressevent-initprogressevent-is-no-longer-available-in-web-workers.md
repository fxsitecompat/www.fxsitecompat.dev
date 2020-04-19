---
title: "`ProgressEvent.initProgressEvent()` is no longer available in Web Workers"
date: "2013-05-19T07:35:00-04:00"
categories: ["dom"]
tags: []
releases: ["24", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=870466"
      title: "Bug 870466 – Remove initProgressEvent from workers too"
---
The obsolete `ProgressEvent.initProgressEvent` method is no longer available in [Web Workers](https://developer.mozilla.org/docs/Web/Guide/Performance/Using_web_workers). This method in general use has already been [removed from Firefox 22](https://www.fxsitecompat.dev/en-CA/docs/2013/progressevent-initprogressevent-has-been-removed/).
