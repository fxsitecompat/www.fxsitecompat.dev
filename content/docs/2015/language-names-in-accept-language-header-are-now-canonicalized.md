---
title: "Language names in `Accept-Language` header are now always canonicalized"
date: "2015-10-27T00:50:00-07:00"
categories: ["networking", "privacy-security"]
tags: []
releases: ["36", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1054739"
      title: "Bug 1054739 - Reduce HTTP Accept-Language Entropy"
---
Previously, language names in the HTTP `Accept-Language` request header turned out to be lowercase, like `en-US` to `en-us`, when the user had changed their preferred language through the browser's Preferences page. This issue has been fixed with Firefox 36, not only because those names were not canonicalized, but because that behaviour increased the fingerprintability of the browser.
