---
title: "`:dir` CSS 擬似クラスの接頭辞が外れました"
date: "2016-05-10T13:02:00-04:00"
categories: ["css"]
tags: []
versions: ["49"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=859301"
      title: "Bug 859301 - Unprefix css4 :dir"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1270406"
      title: "Bug 1270406 - remove pseudo class :-moz-dir after :dir is shipped"
---
[`:dir`](https://developer.mozilla.org/en-US/docs/Web/CSS/:dir) CSS4 擬似クラスがベンダー接頭辞なしに Firefox で使用可能となりました。接頭辞付きの `:-moz-dir` 擬似クラスは近い将来削除されます。
