---
title: "A minimum width has been set for the browser window"
date: "2014-02-07T11:57:09-05:00"
categories: ["misc"]
tags: []
versions: ["29"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=897160"
      title: "Bug 897160 – Set a minimum width for the Firefox window"
---
To avoid a potential UI clipping issue with the new [Australis theme](https://blog.mozilla.org/ux/2014/04/the-new-face-of-firefox/) introduced with Firefox 29, a minimum width has been set for the Firefox desktop browser window. This size is `425px` on OS X and `390px` on other platforms. If you were resizing the window to test your mobile site, the convenient [Responsive Design View](https://developer.mozilla.org/docs/Tools/Responsive_Design_View) can be used instead. The minimum width is not applied to pop-up windows, so this shouldn't affect content display.
