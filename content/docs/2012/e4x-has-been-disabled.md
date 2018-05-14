---
title: "E4X has been disabled"
date: "2012-12-03T03:50:54-05:00"
categories: ["javascript"]
tags: []
versions: ["17"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=778851"
      title: "Bug 778851 – Turn javascript.options.xml.content off by default"
---
[ECMAScript for XML (E4X)](https://developer.mozilla.org/docs/E4X) has been deprecated and disabled in Firefox 17. Though the feature can be enabled by changing the value of a hidden preference `javascript.options.xml.content` to `true`, the implementation will be [completely removed](https://bugzilla.mozilla.org/show_bug.cgi?id=788293) from <del>Firefox 18</del> <ins>a near-future version of Firefox (the original plan was Firefox 18 but currently TBD)</ins>.

**Update**: The E4X support has been [removed with Firefox 21](https://www.fxsitecompat.com/en-CA/docs/2013/e4x-support-has-been-completely-removed/).
