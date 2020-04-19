---
title: "UA string no longer reveals 32-bit Firefox running on 64-bit OS"
date: "2019-07-07T01:03:00-04:00"
categories: ["networking"]
tags: []
releases: ["69"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1559747"
      title: "Bug 1559747 - User-Agent string needn't reveal a user is running 32-bit Firefox on a 64-bit OS"
---
Previously, the user agent (UA) string of Firefox was revealing the fact that the user was running the 32-bit version of Firefox on a 64-bit operating system by saying "WOW64" or "Linux i686 on x86_64". This was needed particularly to detect the browser compatibility with Adobe Flash Player, but the current plug-in installer comes with both the 32-bit and 64-bit versions, and [Flash Player has been deprecated](https://www.fxsitecompat.dev/en-CA/docs/2018/flash-plug-in-support-will-be-removed-in-2020/) anyway.

Firefox 69 has removed the extra information from the UA string, so it now simply says "Win64" or "Linux x86_64" in the `User-Agent` HTTP request header as well as the `navigator.userAgent`, `navigator.platform`, and `navigator.oscpu` DOM APIs.

This change is expected to reduce UA fingerprinting factors, and improves the UX on software download sites which should be serving a 64-bit application to a 64-bit OS even if the user is running the 32-bit version of Firefox.
