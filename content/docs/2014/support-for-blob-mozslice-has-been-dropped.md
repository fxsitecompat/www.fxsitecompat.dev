---
title: "Support for `Blob.mozSlice` has been dropped"
date: "2014-03-21T04:50:04-04:00"
categories: ["dom"]
tags: []
versions: ["30"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=961804"
      title: "Bug 961804 – Drop support for Blob.mozSlice"
---
The support for the `mozSlice` method of the [`Blob`](https://developer.mozilla.org/docs/Web/API/Blob) object, has been deprecated since Firefox 15 and removed with Firefox 30. Use the unprefied `slice` method instead.
