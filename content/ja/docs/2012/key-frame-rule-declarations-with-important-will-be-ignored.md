---
title: "`!important` 付きのキーフレームルール宣言は無視されるようになりました"
date: "2012-12-03T03:54:45-05:00"
categories: ["css"]
tags: []
versions: ["19"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=784466": "Bug 784466 – [css3-animations] we should drop declarations in keyframe rules that have !important"
---
[CSS3 アニメーション](https://developer.mozilla.org/ja/docs/CSS/Using_CSS_animations) の最新仕様に合わせて、`!important` キーワードが付いたキーフレームルール宣言は無視され、パースエラーが返るようになりました。
