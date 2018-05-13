---
title: "`URLUtils.hash` no longer decodes fragment"
date: "2015-06-13T15:20:46-04:00"
categories: ["dom"]
tags: []
versions: ["41"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1093611"
      title: "Bug 1093611 – AnchorElement.hash should be the encoded version of the href attribute\'s fragment"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1184589"
      title: "Bug 1184589 - window.location.hash exposes spaces as %20"
---
The [`URLUtils.hash`](https://developer.mozilla.org/docs/Web/API/URLUtils/hash) property, which is available as `location.hash`, `HTMLAnchorElement.hash`, `URL.hash`, etc., now returns a percent-encoded fragment as we see in the [`href`](https://developer.mozilla.org/docs/Web/API/URLUtils/href) property, to follow the latest specification. So, for instance, a space will be `%20`, and you have to use the [`decodeURIComponent`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/decodeURIComponent) method to get the decoded fragment ([example](https://github.com/mozilla/phonebook/commit/78619461421f1619d32d89b4eaca0c0fb49ef164)). This change was originally planned for Firefox 38 but has been postponed due to compatibility issues. This new behaviour matches the current version of Safari.
