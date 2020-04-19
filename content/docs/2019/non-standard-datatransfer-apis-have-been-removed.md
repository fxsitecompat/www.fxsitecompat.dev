---
title: "Non-standard `DataTransfer` APIs have been removed"
date: "2019-09-05T18:13:00-04:00"
categories: ["dom"]
tags: []
releases: ["71"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1345192"
      title: "Bug 1345192 - Consider removing gecko-only DataTransfer APIs"
---
The non-standard `mozGetDataAt`, `mozSetDataAt`, `mozClearDataAt` and `mozTypesAt` methods as well as the `mozItemCount` property on the [`DataTransfer`](https://developer.mozilla.org/docs/Web/API/DataTransfer) interface, deprecated since [Firefox 63](https://www.fxsitecompat.dev/en-CA/docs/2018/non-standard-datatransfer-apis-have-been-deprecated/), have been removed with Firefox 71. Use the standard `getData`, `setData` and `clearData` methods as well as the `items` property instead.
