---
title: "`box-sizing:padding-box` が削除されます"
date: "2015-10-27T19:28:00-07:00"
categories: ["css"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1166728"
      title: "Bug 1166728 - remove box-sizing: padding-box"
---
[`box-sizing`](https://developer.mozilla.org/ja/docs/Web/CSS/box-sizing) CSS プロパティが `padding-box` を受け付けなくなります。この値が仕様から削除されたためです。代わりに `border-box` を使ってください。
