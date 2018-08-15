---
title: "`image-orientation` プロパティが角度の値を受け付けなくなりました"
date: "2018-08-14T23:13:00-04:00"
categories: ["css"]
tags: []
versions: ["63"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1473450"
      title: "Bug 1473450 - remove <angle> values from image-orientation"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/A1aaENcsR6k/discussion"
      title: "Intent to unship: explicit <angle> values in image-orientation"
---
CSS [`image-orientation`](https://developer.mozilla.org/docs/Web/CSS/image-orientation) プロパティに指定できる明示的な角度の値と `flip` キーワードへの対応が、最新の CSS Images Module 仕様に従い Firefox 63 で廃止されました。初期値は `0deg` の代わりに `none` となり、`from-image` が使用可能な唯一のキーワードとなります。このプロパティは今のところ Firefox にしか実装されていないことから、互換性リスクは非常に低いはずです。
