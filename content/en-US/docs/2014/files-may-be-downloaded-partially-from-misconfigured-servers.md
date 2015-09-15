---
title: "Files may be downloaded partially from misconfigured servers"
date: "2014-07-22T05:06:26-04:00"
categories: ["networking"]
tags: []
versions: "33"
statuses: "regressed"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1083090": "Bug 1083090 – Broken CSS and JavaScript errors with Firefox 33 (regression) [partial transfer]"
---
Due to the proper framing check for HTTP 1.1 and later, introduced with Firefox 33, JavaScript, CSS, CSV, PDF and other types of files are partially transferred from misconfigured Web servers. The first case is where the `Content-Encoding: gzip` header is set while the `Content-Length` header has a wrong file size. On Apache servers, disabling the `mod_deflate` module may quickly workaround the issue, though it's not a right solution. Another case is where the terminating zero chunk is missing in chunked transfer encoding responses. These interoperability problems will be fixed with Firefox 33.1 where the framing check is forced only to SPDY, HTTP/2 and later.
