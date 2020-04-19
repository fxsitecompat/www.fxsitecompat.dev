---
title: "`File.lastModifiedDate` now returns the current date if the modified date is unknown"
date: "2012-12-03T03:54:45-05:00"
categories: ["dom"]
tags: []
versions: ["19", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=793459"
      title: "Bug 793459 – Update File.lastModifiedDate to latest spec"
---
Following the latest [File API](https://www.w3.org/TR/FileAPI/) spec, the `lastModifiedDate` property of a [`File`](https://developer.mozilla.org/docs/Web/API/File) object now returns the current date if the file's last modified date is unknown. Previously it returns `null` in such case.
