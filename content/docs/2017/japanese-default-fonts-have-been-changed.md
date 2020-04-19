---
title: "Japanese default fonts have been changed"
date: "2017-09-20T14:23:00-04:00"
categories: ["misc"]
tags: []
versions: ["57", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=548311"
      title: "Bug 548311 - Default Japanese font should be Meiryo or Yu Gothic for modern Windows"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1351332"
      title: "Bug 1351332 - Needs hack for Meiryo to render italic/oblique style"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1354004"
      title: "Bug 1354004 - Change Japanese default fonts on release build"
aliases:
    - "/en-CA/docs/2017/some-of-browser-default-fonts-have-been-changed/"
---
The browser's default Japanese fonts on Windows have been changed with Firefox 55 Nightly and Firefox 57 on all channels, giving webpages a modern impression. The sans-serif font will be [Meiryo](https://en.wikipedia.org/wiki/Meiryo) instead of MS PGothic, while the serif font will be Yu Mincho instead of MS PMincho. MS Gothic remains as the monospace font. Meiryo doesn't have the italic variant, but Firefox added a hack to make it italic when styled.
