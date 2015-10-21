---
title: "`CSSRule.MOZ_KEYFRAME_RULE(S)` 定数の接頭辞が外れました"
date: "2012-12-29T08:29:30-05:00"
categories: ["css"]
tags: []
versions: ["20"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=816431": "Bug 816431 – unprefix CSSRule.MOZ_KEYFRAME{,S}_RULE constants"
---
[`CSSRule`](https://developer.mozilla.org/ja/docs/DOM/cssRule) の `MOZ_KEYFRAME_RULE`、`MOZ_KEYFRAMES_RULE` 定数から `MOZ_` 接頭辞が外れました。接頭辞付き定数も当面残されますが、今後は接頭辞なし定数を使用してください。
