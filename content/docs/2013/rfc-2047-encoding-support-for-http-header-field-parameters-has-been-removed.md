---
title: "RFC 2047 encoding support for HTTP header field parameters has been removed"
date: "2013-02-24T03:44:31-05:00"
categories: ["misc"]
tags: []
versions: ["22"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=601933"
      title: "Bug 601933 – remove RFC 2047 encoding support for HTTP header field parameters"
---
When decoding the `filename` parameter in `Content-Disposition` headers, Firefox had attempted to unescape using the RFC 2047 encoding. This was a bug according to the relevant specs, and implemented only on Firefox and Chrome. The RFC 2231 and RFC 5987 encodings can be used instead.

<ins>Update: [**This change has been postponed**](https://bugzilla.mozilla.org/show_bug.cgi?id=875615) to collect and analyze data on the usage of the RFC 2047 encoding.</ins>
