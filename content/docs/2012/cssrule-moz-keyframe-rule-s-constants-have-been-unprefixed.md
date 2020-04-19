---
title: "`CSSRule.MOZ_KEYFRAME_RULE(S)` constants have been unprefixed"
date: "2012-12-29T08:29:30-05:00"
categories: ["css"]
tags: []
versions: ["20", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=816431"
      title: "Bug 816431 – unprefix CSSRule.MOZ_KEYFRAME{,S}_RULE constants"
---
The `MOZ_KEYFRAME_RULE` and `MOZ_KEYFRAMES_RULE` constants of [`CSSRule`](https://developer.mozilla.org/docs/Web/API/CSSRule) have been unprefixed. While those prefixed constants will remain for the meantime, use the unprefixed ones instead from now on.
