---
title: "Part of Shadow DOM v0 API has been removed"
date: "2019-05-12T22:11:00-04:00"
categories: ["dom"]
tags: []
releases: ["67", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1535438"
      title: "Bug 1535438 - Remove Shadow DOM v0 APIs"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/zFwps4VTiXw/discussion"
      title: "Intent to unship: Some Shadow DOM v0 APIs"
---
Firefox 67 has removed the `getElementsByTagName`, `getElementsByTagNameNS` and `getElementsByClassName` methods from the `ShadowRoot` interface, which were part of the deprecated Shadow DOM v0 API accidentally exposed when Shadow DOM v1 was shipped with Firefox 63.

Since `ShadowRoot` inherits `DocumentFragment`, the `querySelector`, `querySelectorAll` and `getElementById` methods can be used instead.
