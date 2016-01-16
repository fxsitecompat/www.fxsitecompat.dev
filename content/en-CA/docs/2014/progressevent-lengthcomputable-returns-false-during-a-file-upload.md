---
title: "`ProgressEvent.lengthComputable` returns `false` during a file upload"
date: "2014-02-07T11:57:09-05:00"
categories: ["dom"]
tags: []
versions: ["29"]
statuses: "regressed"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1009640": "Bug 1009640 – \"Unable to compute\" error on Ebay photo uploader due to XMLHttpRequest lengthComputable == false"
---
The [`ProgressEvent.lengthComputable`](https://developer.mozilla.org/en-US/docs/Web/API/ProgressEvent.lengthComputable) property used to [monitor `XMLHttpRequest` `progress` events](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/Using_XMLHttpRequest#Monitoring_progress) returns `false` while uploading a local file on Firefox 29, even when it should return `true`. This regression, found on *eBay Picture Uploader*, has been fixed with Firefox 30.
