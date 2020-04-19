---
title: "`DataContainerEvent`, `BrowserFeedWriter`, `EventListenerInfo` and `XPathNamespace` have been removed"
date: "2014-04-03T19:31:02-04:00"
categories: ["dom"]
tags: []
releases: ["31", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=980134"
      title: "Bug 980134 – Hide DataContainerEvent from content"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=983845"
      title: "Bug 983845 – Stop exposing BrowserFeedWriter to the Web"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=991690"
      title: "Bug 991690 – Remove the classinfo from EventListenerInfo"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=998738"
      title: "Bug 998738 – Consider removing nsIDOMXPathNamespace (and window.XPathNamespace)"
---
As part of the ongoing effort to standardize global objects, some interfaces have been removed from [`window`](https://developer.mozilla.org/docs/Web/API/window). The standard [`CustomEvent`](https://developer.mozilla.org/docs/Web/API/CustomEvent) interface should be used instead the Firefox-specific `DataContainerEvent` interface. `BrowserFeedWriter` was a Firefox-specific interface which should not be exposed to Web content. `EventListenerInfo` was also a non-standard interface which was not intended to be a global object. The `XPathNamespace` interface was part of the DOM3 XPath spec but has not been implemented.
