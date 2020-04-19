---
title: "`HTMLCanvasElement.getContext()` がオブジェクトでないコンテキスト属性を受け付けなくなりました"
date: "2016-02-07T23:01:00-05:00"
categories: ["canvas-webgl"]
tags: []
releases: ["44"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=645792"
      title: "Bug 645792 - Implement correct behavior for getContext() failures"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1215072"
      title: "Bug 1215072 - Assertion failure: !JS_IsExceptionPending(cx), at ./HTMLCanvasElementBinding.cpp:231"
---
標準準拠の一環として、[`HTMLCanvasElement.getContext`](https://developer.mozilla.org/docs/Web/API/HTMLCanvasElement/getContext) の 2 番目の `contextAttributes` 引数が `Object`、`null`、`undefined` のいずれでもない場合、`TypeError` が投げられるようになりました。取り得る属性については MDN の記事を参照してください。

**更新**: *Livecode* の Emscripten コードが不正な `false` 引数により動作しなくなったことから、この変更は [Firefox 45 で取り消されました](https://bugzilla.mozilla.org/show_bug.cgi?id=1244480)。
