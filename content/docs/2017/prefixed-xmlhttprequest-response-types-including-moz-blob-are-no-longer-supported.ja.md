---
title: "`moz-blob` などの接頭辞付き `XMLHttpRequest` レスポンスタイプへの対応が打ち切られました"
date: "2017-10-03T05:38:00-04:00"
categories: ["dom"]
tags: []
versions: ["58"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1120171"
      title: "Bug 1120171 - Remove support for moz-prefixed XHR responseTypes"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1397145"
      title: "Bug 1397145 - Remove moz-blob support from XHR"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1397151"
      title: "Bug 1397151 - Remove moz-chunked-text support from XHR"
aliases:
    - "/ja/docs/2015/prefixed-xmlhttprequest-response-types-will-be-removed/"
---
[`XMLHttpRequest.prototype.responseType`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest/responseType) プロパティによって返される、非標準で `moz` 接頭辞が付いている値、具体的には `moz-blob`、`moz-chunked-text` への対応が、[Telemetry](https://telemetry.mozilla.org/) でそれらの使用率が低いことが確認されたことから、Firefox 58 で削除されました。本稿執筆時点で `moz-chunked-arraybuffer` はまだ使用可能ですが、ウェブ開発者はこの非標準タイプの使用を避けるべきです。

**更新** `moz-chunked-arraybuffer` は [Firefox 68 で削除されました](https://www.fxsitecompat.com/ja/docs/2019/xhr-moz-chunked-arraybuffer-response-type-is-no-longer-supported/)。
