---
title: "Uploading file using XHR prepends slash to `filename`"
date: "2016-11-30T23:34:00-05:00"
categories: ["dom"]
tags: []
versions: ["50"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1319088"
      title: "Bug 1319088 - Bad filename in an xhr request"
---
On Firefox 50, [dynamically uploading a file](https://developer.mozilla.org/en-US/docs/Using_files_from_web_applications) through an `XMLHttpRequest` results in a leading slash added to the `filename` parameter in the [`Content-Disposition`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Disposition) HTTP request header. This regression, introduced when the [`File.prototype.webkitRelativePath`](https://developer.mozilla.org/en-US/docs/Web/API/File/webkitRelativePath) property was implemented, will be fixed with Firefox 50.1.0.
