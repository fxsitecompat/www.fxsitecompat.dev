---
title: "Undefined pseudo-header fields are no longer accepted in HTTP/2"
date: "2015-09-23T05:27:00-04:00"
categories: ["networking"]
tags: []
versions: ["42"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1136727"
      title: "Bug 1136727 - Firefox accepts undefined or invalid pseudo-header fields in HTTP/2"
---
Firefox 41 and the earlier versions were incorrectly accepting undefined or invalid pseudo-header fields in HTTP/2 responses. The `:version` field was being used on *Twitter* but later removed. Firefox 42 no longer accepts pseudo-header fields except `:status`, which is required as per the [specification](https://http2.github.io/http2-spec/index.html#HttpResponse), and response headers with arbitrary fields are considered malformed.
