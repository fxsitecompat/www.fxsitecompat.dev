---
title: "`XMLHttpRequest` may return corrupt data for large blobs"
date: "2017-03-27T13:11:00-04:00"
categories: ["dom"]
tags: []
versions: ["52"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1349862"
      title: "Bug 1349862 - XMLHttpRequest returning corrupt data for large blobs"
---
Firefox 52 has introduced a regression where `XMLHttpRequest` retrieving large data with the `blob` [response type](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest/responseType) results in a corrupt file in certain cases. The issue would likely occur with files more than 10 MB due to a race condition, and can be avoided, according to the bug reporter, by setting the response type to `moz-blob`. Mozilla developers are working on the solution.

**Update**: This issue has been fixed with Firefox 53 and Firefox ESR 52.1.
