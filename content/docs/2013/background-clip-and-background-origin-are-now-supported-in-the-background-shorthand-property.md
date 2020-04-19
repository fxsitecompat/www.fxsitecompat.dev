---
title: "`background-clip` and `background-origin` are now supported in the `background` shorthand property"
date: "2013-02-24T03:44:31-05:00"
categories: ["css"]
tags: []
versions: ["22", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=570896"
      title: "Bug 570896 - Add support for different background-origin and background-clip in background shorthand"
---
A possible compatibility issue here is that, if [`background-origin`](https://developer.mozilla.org/docs/Web/CSS/background-origin) or [`background-clip`](https://developer.mozilla.org/docs/Web/CSS/background-clip) is not explicitly set in the [`background`](https://developer.mozilla.org/docs/Web/CSS/background) shorthand property, those will be reset to their [initial value](https://developer.mozilla.org/docs/Web/CSS/initial).
