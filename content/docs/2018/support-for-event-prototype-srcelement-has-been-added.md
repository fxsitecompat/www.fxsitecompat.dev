---
title: "Support for `Event.prototype.srcElement` has been added"
date: "2018-05-08T16:17:00-04:00"
categories: ["dom"]
tags: []
versions: ["62"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=453968"
      title: "Bug 453968 - Support IE extension Event.srcElement"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1444004"
      title: "Bug 1444004 - Implement Event.srcElement on nightly only for now"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/y9KU21IBFvo/discussion"
      title: "Intent to ship: event.srcElement"
---
Firefox now supports the non-standard [`srcElement`](https://developer.mozilla.org/en-US/docs/Web/API/Event/srcElement) property on the `Event` interface for a better cross-browser compatibility. Firefox Nightly has already added the support since the version 60. It's the standard [`target`](https://developer.mozilla.org/en-US/docs/Web/API/Event/target) property's alias originated from Internet Explorer, which has been implemented in all other browsers by now.

Mozilla engineers are concerned about the possibility of broken sites if it's misused for browser detection targeting Firefox. Make sure your site is not the case.
