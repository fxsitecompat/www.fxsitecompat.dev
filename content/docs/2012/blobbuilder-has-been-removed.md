---
title: "`BlobBuilder` has been removed"
date: "2012-12-03T03:53:26-05:00"
categories: ["dom"]
tags: []
versions: ["18", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=744907"
      title: "Bug 744907 – Remove BlobBuilder"
---
The deprecated [`BlobBuilder`](https://developer.mozilla.org/docs/Web/API/BlobBuilder) (`MozBlobBuilder`) interface has been removed. From now on, use the [`Blob`](https://developer.mozilla.org/docs/Web/API/Blob) constructor to create a `Blob` object.
