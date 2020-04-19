---
title: "Custom cursor larger than 32px will be ignored when intersecting UI"
date: "2019-05-13T14:47:00-04:00"
categories: ["css"]
tags: []
versions: ["67", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1445844"
      title: "Bug 1445844 - Custom cursor goes outside the bounds of the web content in \"malware\" website"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1534761"
      title: "Bug 1534761 - Change maximum cursor size when intersecting UI to 32 pixels."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/ke-KMmY1Mak/discussion"
      title: "Intent to Ship: Ignore custom cursors over 32 pixels intersecting UI"
---
The CSS `cursor` property allows websites to change the style of the mouse pointer to one of predefined types or custom image. While most use cases are legit, some malicious sites are known to be abusing this functionality to hijack the cursor, preventing users from closing the browser tab.

In an effort to prevent this kind of UX issues, on Firefox 67 and later, custom cursor images larger than 32 pixels will be ignored and failed back to the default cursor while intersecting with the browser UI. Web developers can still use a large custom cursor in the content area, particularly for games.

Google is making the same change to [Chrome 75](https://bugs.chromium.org/p/chromium/issues/detail?id=880863).
