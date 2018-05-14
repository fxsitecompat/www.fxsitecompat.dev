---
title: "`java` object has been removed"
date: "2012-10-09T06:00:00-04:00"
categories: ["dom"]
tags: []
versions: ["16"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=748343"
      title: "Bug 748343 – remove support for “java” DOM object"
---
The `window.java` and `window.packages` global DOM objects have been removed. Those objects were not well documented and the actual use cases might be rare. This change was originally planned for Firefox 15 but has been [postponed](https://bugzilla.mozilla.org/show_bug.cgi?id=778073) to maintain compatibility with existing Firefox extensions.
