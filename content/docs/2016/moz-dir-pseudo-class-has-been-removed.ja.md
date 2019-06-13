---
title: "`:-moz-dir` 擬似クラスが廃止されました"
date: "2016-11-25T18:48:00-05:00"
categories: ["css"]
tags: []
versions: ["53"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1270406"
      title: "Bug 1270406 - remove pseudo class :-moz-dir after :dir is shipped"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/F0_UbXAfB_4/discussion"
      title: "Intent to ship: unprefix :dir pseudo-class"
---
[Firefox 49](https://www.fxsitecompat.dev/ja/docs/2016/dir-css-pseudo-class-has-been-unprefixed/) 以降廃止予定となっていた接頭辞付き `:-moz-dir` 擬似クラスが Firefox 53 で削除されました。標準の接頭辞なし [`:dir`](https://developer.mozilla.org/docs/Web/CSS/:dir) 擬似クラスに置き換えてください。
