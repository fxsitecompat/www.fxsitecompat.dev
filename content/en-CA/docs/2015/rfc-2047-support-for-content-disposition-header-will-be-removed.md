---
title: "RFC 2047 support for `Content-Disposition` header will be removed"
date: "2015-10-27T14:25:00-07:00"
categories: ["networking"]
tags: []
versions: ["future"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=601933"
      title: "Bug 601933 - remove RFC 2047 encoding support for HTTP header field parameters"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=875615"
      title: "Bug 875615 - Revert to decoding RFC 2047-encoding until we have telemetry on usage"
---
Firefox tries to decode the `filename` parameter in the HTTP `Content-Disposition` header using the RFC 2047 encoding. This is a bug according to the spec, and implemented only by Firefox and Google Chrome. Therefore, The support for RFC 2047 is considered to be removed. This change was [originally planned for Firefox 22](https://www.fxsitecompat.com/en-CA/docs/2013/rfc-2047-encoding-support-for-http-header-field-parameters-has-been-removed/), but has been postponed due to interoperability issues. The RFC 2231 and 5987 encodings should be used instead.
