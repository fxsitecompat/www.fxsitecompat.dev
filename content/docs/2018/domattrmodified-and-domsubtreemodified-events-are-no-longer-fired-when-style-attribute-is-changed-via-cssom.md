---
title: "`DOMAttrModified` and `DOMSubtreeModified` events are no longer fired when `style` attribute is changed via CSSOM"
date: "2018-05-23T21:22:00-04:00"
categories: ["css", "dom"]
tags: []
versions: ["62"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1460295"
      title: "Bug 1460295 - unresponsive visiting login page on eqbank.ca"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/YD4jeL00HHU/discussion"
      title: "Intent to unship: DOMAttrModified and DOMSubtreeModified event for changes via CSSOM"
---
Firefox has stopped triggering the `DOMAttrModified` and `DOMSubtreeModified` [mutation events](https://developer.mozilla.org/docs/Web/Guide/Events/Mutation_events) for changes on the element's `style` attribute via CSSOM such as the [`style`](https://developer.mozilla.org/docs/Web/API/HTMLElement/style) property.

This change has been made to solve site performance issues where a nested `DOMSubtreeModified` event could go into an infinite loop in some cases. Such issues don't occur on Chrome and Safari because the `DOMAttrModified` event is not implemented in these browsers.

The alternative [mutation observers](https://developer.mozilla.org/docs/Web/API/MutationObserver) are not affected by this change.

Note that mutation events are marked as deprecated in the DOM3 UI Events spec, and therefore the support will be removed from the browsers in the future. Use mutation observers instead in any case.
