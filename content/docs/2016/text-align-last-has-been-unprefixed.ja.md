---
title: "`text-align-last` の接頭辞が外れました"
date: "2016-05-30T09:38:00-04:00"
categories: ["css"]
tags: []
versions: ["49"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1039541"
      title: "Bug 1039541 - Unprefix -moz-text-align-last"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/jbMO8mkFZwE/discussion"
      title: "Intent to ship: Unprefixed text-align-last"
---
Firefox 49 で [`text-align-last`](https://developer.mozilla.org/ja/docs/Web/CSS/text-align-last) CSS プロパティの接頭辞が外れました。ベンダー接頭辞付きの `-moz-text-align-last` プロパティは近い将来削除されます。

**更新**: 接頭辞付きプロパティは [Firefox 53](https://www.fxsitecompat.com/ja/docs/2016/moz-text-align-last-property-has-been-removed/) で削除されました。
