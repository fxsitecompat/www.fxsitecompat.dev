---
title: "Non-standard `type` argument for `document.open()` is no longer supported"
date: "2018-06-03T21:42:00-04:00"
categories: ["dom"]
tags: []
releases: ["61", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1444872"
      title: "Bug 1444872 - Remove processing for document.open()'s type parameter"
---
Firefox supports 2 non-standard optional arguments for the [`document.open`](https://developer.mozilla.org/docs/Web/API/Document/open) method: `type` and `replace`. Starting with Firefox 61, `type` will be ignored and `text/html` will always be used as the MIME type for a newly opened document. Since these arguments are not supported by any other browsers, the compatibility risk should be very low.
