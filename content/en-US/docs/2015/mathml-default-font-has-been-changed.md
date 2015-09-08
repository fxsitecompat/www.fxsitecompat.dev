---
title: "MathML default font has been changed"
date: "2015-06-13T15:20:46-04:00"
categories: ["mathml"]
tags: []
versions: "41"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=947654": "Bug 947654 - Default fonts for MathML"
---
[MathML](https://developer.mozilla.org/en-US/docs/Web/MathML) font family names are no longer hardcoded in the user-agent stylesheet, and Firefox users can now use [any fonts](https://developer.mozilla.org/en-US/docs/Mozilla/MathML_Project/Fonts) by setting the new `font.name.serif.x-math` preference. The old fonts including MathJax and STIX General are considered deprecated in favor of Latin Modern Math that will be used as the primary fallback font.
