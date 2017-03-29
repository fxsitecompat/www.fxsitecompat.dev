---
title: "Some of browser default fonts have been changed"
date: "2017-03-29T15:34:00-04:00"
categories: ["misc"]
tags: []
versions: ["55"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=548311"
      title: "Bug 548311 - Default Japanese font should be Meiryo or Yu Gothic for modern Windows"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=713680"
      title: "Bug 713680 - Use Consolas as the default monospace font on Windows Vista & 7"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1342741"
      title: "Bug 1342741 - Use Menlo as the default monospace font on macOS"
---
Firefox 55 and later will use [Consolas](https://en.wikipedia.org/wiki/Consolas) on Windows and [Menlo](https://en.wikipedia.org/wiki/Menlo_(typeface)) on macOS as the browser's default monospace Latin fonts. Previously, [Courier New](https://en.wikipedia.org/wiki/Courier_New) had been used for a long time on both platforms.

The default Japanese fonts on Windows have also been changed. The sans-serif font will be [Meiryo](https://en.wikipedia.org/wiki/Meiryo) instead of MS PGothic, while the serif font will be Yu Mincho instead of MS PMincho. MS Gothic remains the monospace font.

This may lead to layout changes on some pages especially when it has a `<textarea>` which size is specified in the number of characters. You can specify the size in pixels with CSS to avoid such issues. You can also use [web fonts](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Web_fonts), via [Google Fonts](https://fonts.google.com/) for instance, to achieve cross-platform, cross-browser design.
