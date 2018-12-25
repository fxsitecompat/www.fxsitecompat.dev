---
title: "`xml:base` attribute has been deprecated"
date: "2017-02-21T20:16:00-05:00"
categories: ["misc"]
tags: []
versions: ["53"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=903372"
      title: "Bug 903372 - Remove support for xml:base"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1340926"
      title: "Bug 1340926 - Add telemetry for xml:base attribute"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/1JDnJWefe1E/discussion"
      title: "Intent to unship: xml:base attribute"
---
The [`xml:base`](https://www.w3.org/TR/xmlbase/) attribute similar to the HTML [`<base>`](https://developer.mozilla.org/docs/Web/HTML/Element/base) element is now considered deprecated and will be removed in the near future. It was removed from the spec years ago and no other browsers support it at this time.

**Update**: The attribute support has been removed with [Firefox 66](https://www.fxsitecompat.com/en-CA/docs/2018/xml-base-attribute-is-no-longer-supported/).
