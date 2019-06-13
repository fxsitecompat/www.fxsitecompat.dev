---
title: "XHR `moz-chunked-arraybuffer` response type is no longer supported"
date: "2019-05-28T06:06:00-04:00"
categories: ["dom"]
tags: []
versions: ["68"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1120171"
      title: "Bug 1120171 - Remove support for moz-prefixed XHR responseTypes (moz-blob, moz-chunked-text, and moz-chunked-arraybuffer)"
---
The non-standard `moz-chunked-arraybuffer` response type for the [`XMLHttpRequest.responseType`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest/responseType) property, deprecated since [Firefox 58](https://www.fxsitecompat.dev/en-CA/docs/2017/prefixed-xmlhttprequest-response-types-including-moz-blob-are-no-longer-supported/), has been removed with Firefox 68. You can instead use `fetch()` in combination with the Streams API which is available since Firefox 65. See [Using readable streams](https://developer.mozilla.org/docs/Web/API/Streams_API/Using_readable_streams) on MDN for details.

**Update**: The initial version of this note was mentioning the `arraybuffer` type as an alternative but it was wrong. We have corrected note according to the feedback.
