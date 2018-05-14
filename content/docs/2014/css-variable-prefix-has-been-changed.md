---
title: "CSS variable prefix has been changed"
date: "2014-04-03T19:31:02-04:00"
categories: ["css"]
tags: []
versions: ["31"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=985838"
      title: "Bug 985838 – change \"var-\" prefix of CSS Variables to \"--\""
---
Since [CSS Variables](https://developer.mozilla.org/docs/Web/CSS/Using_CSS_variables) was landed in [Firefox 29](https://developer.mozilla.org/docs/Mozilla/Firefox/Releases/29) (disabled in the Beta and Release channels), the spec has been revised to change the prefix of custom properties from `var-` to `--`. CSS Variables are enabled with Firefox 31 in the all channels and this version follows the updated spec.
