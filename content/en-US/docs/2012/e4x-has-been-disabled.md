---
title: "E4X has been disabled"
date: "2012-12-03T03:50:54-05:00"
categories: ["javascript"]
tags: []
versions: "17"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=778851": "Bug 778851 – Turn javascript.options.xml.content off by default"
---
[ECMAScript for XML (E4X)](https://developer.mozilla.org/en-US/docs/E4X) has been deprecated and disabled in Firefox 17. Though the feature can be enabled by changing the value of a hidden preference `javascript.options.xml.content` to `true`, the implementation will be [completely removed](https://bugzilla.mozilla.org/show_bug.cgi?id=788293) from <del>Firefox 18</del> <ins>a near-future version of Firefox (the original plan was Firefox 18 but currently TBD)</ins>.
