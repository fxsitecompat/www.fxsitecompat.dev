---
title: "Line breaking code in the value of `XHR.getAllResponseHeaders()` has been changed"
date: "2012-12-03T03:50:54-05:00"
categories: ["dom"]
tags: []
versions: ["17"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=730925"
      title: "Bug 730925 – XHR.getAllResponseHeaders should use CRLF, not LF per spec"
---
The [`XMLHttpRequest.getAllResponseHeaders`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest#getAllResponseHeaders) function returns response headers as strings divided by line breaks. The Firefox implementation has been fixed to use CR+LF (`\r\n`) instead of LF (`\n`) as the line breaking code to follow the spec. You should be careful if you're doing something by reading header information.
