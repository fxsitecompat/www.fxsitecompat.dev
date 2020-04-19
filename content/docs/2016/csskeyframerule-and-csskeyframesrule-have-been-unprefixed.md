---
title: "`CSSKeyframeRule` and `CSSKeyframesRule` have been unprefixed"
date: "2016-03-16T05:34:00-04:00"
categories: ["css", "dom"]
tags: []
versions: ["48", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1256178"
      title: "Bug 1256178 - Drop the moz prefix from the MozCSSKeyframeRule and MozCSSKeyframesRule interfaces"
---
The prefixed `MozCSSKeyframeRule` and `MozCSSKeyframesRule` interfaces have been replaced with the standard [`CSSKeyframeRule`](https://developer.mozilla.org/docs/Web/API/CSSKeyframeRule) and [`CSSKeyframesRule`](https://developer.mozilla.org/docs/Web/API/CSSKeyframesRule) interfaces respectively. The prefixed ones are no longer available in Firefox 48 and later.
