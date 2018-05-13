---
title: "`atob` now ignores whitespaces"
date: "2013-10-08T20:15:35-04:00"
categories: ["dom"]
tags: []
versions: ["27"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=711180"
      title: "Bug 711180 – atob should ignore whitespace"
---
The [`window.atob`](https://developer.mozilla.org/docs/Web/API/window.atob) method, that decodes a Base64-encoded string, has been updated to ignore all space characters in the argument to comply with the latest HTML5 spec.
