---
title: "Documents in `<frame>` or `<object>` can no longer request fullscreen"
date: "2015-10-13T02:44:00-04:00"
categories: ["dom"]
tags: []
releases: ["44", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1212299"
      title: "Bug 1212299 - Forbid documents inside <frame> and <object> from requesting fullscreen"
---
Firefox was incorrectly allowing documents inside a `<frame>` or `<object>` to use the [Fullscreen API](https://developer.mozilla.org/docs/Web/API/Fullscreen_API). This behaviour has been fixed to comply with the spec, so only topmost documents and documents inside `<iframe>` can now request fullscreen.
