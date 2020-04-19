---
title: "`typemustmatch` attribute has been dropped from `<object>`"
date: "2019-05-28T00:20:00-04:00"
categories: ["dom", "html"]
tags: []
versions: ["68", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1548773"
      title: "Bug 1548773 - Remove support for typemustmatch"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/6dOIeUcHY6g/discussion"
      title: "Intent to unship: typeMustMatch attribute on <object> elements"
---
The support for the `typemustmatch` attribute on the HTML `<object>` element and the corresponding [`typeMustMatch`](https://developer.mozilla.org/docs/Web/API/HTMLObjectElement/typeMustMatch) property on the `HTMLObjectElement` DOM interface has been removed from the latest HTML Living Standard and Firefox 68. No other browsers support the attribute, so the compatibility risk should be very low.
