---
title: "Prefixed `XMLHttpRequest` response types including `moz-blob` are no longer supported"
date: "2017-10-03T05:38:00-04:00"
categories: ["dom"]
tags: []
versions: ["58", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1120171"
      title: "Bug 1120171 - Remove support for moz-prefixed XHR responseTypes"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1397145"
      title: "Bug 1397145 - Remove moz-blob support from XHR"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1397151"
      title: "Bug 1397151 - Remove moz-chunked-text support from XHR"
aliases:
    - "/en-CA/docs/2015/prefixed-xmlhttprequest-response-types-will-be-removed/"
---
The support for the non-standard, `moz`-prefixed values returned by the [`XMLHttpRequest.prototype.responseType`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest/responseType) property, notably `moz-blob` and `moz-chunked-text`, has been removed with Firefox 58 after [Telemetry](https://telemetry.mozilla.org/) proved the low usage rates. `moz-chunked-arraybuffer` is still available at the time of this writing, but web developers are discouraged from using the non-standard type.

**Update** `moz-chunked-arraybuffer` has been [removed with Firefox 68](https://www.fxsitecompat.dev/en-CA/docs/2019/xhr-moz-chunked-arraybuffer-response-type-is-no-longer-supported/).
