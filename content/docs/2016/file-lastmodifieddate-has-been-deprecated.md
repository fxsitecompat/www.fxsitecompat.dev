---
title: "`File.lastModifiedDate` has been deprecated"
date: "2016-06-01T17:16:00-04:00"
categories: ["dom"]
tags: []
releases: ["49", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1048291"
      title: "Bug 1048291 - Remove/Deprecate File::lastModifiedDate"
---
The [`File.prototype.lastModifiedDate`](https://developer.mozilla.org/docs/Web/API/File/lastModifiedDate) property is now deprecated and will be removed in the future. Use the `lastModified` property instead.

**Update**: The property has been [removed with Firefox 61](https://www.fxsitecompat.dev/en-CA/docs/2018/file-lastmodifieddate-has-been-removed/).
