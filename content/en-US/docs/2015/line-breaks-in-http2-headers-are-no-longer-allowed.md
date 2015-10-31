---
title: "Line breaks in HTTP/2 headers are no longer allowed"
date: "2015-10-30T17:06:00-07:00"
categories: ["networking"]
tags: []
versions: ["44"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1197847": "Bug 1197847 - dont allow line folding in h2 headers"
---
Unlike the traditional HTTP, line break characters (`\n`) are not allowed in HTTP/2 response headers. Firefox 44 has updated the implementation to enforce the constraint so that such headers are now considered invalid.
