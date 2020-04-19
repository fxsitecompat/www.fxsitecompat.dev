---
title: "XHR でファイルをアップロードする際、`filename` の先頭にスラッシュが付いてしまいます"
date: "2016-11-30T23:34:00-05:00"
categories: ["dom"]
tags: []
releases: ["50"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1319088"
      title: "Bug 1319088 - Bad filename in an xhr request"
---
Firefox 50 で、`XMLHttpRequest` を通じて [ファイルを動的にアップロード](https://developer.mozilla.org/docs/Using_files_from_web_applications) すると、[`Content-Disposition`](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Disposition) HTTP リクエストヘッダーに含まれる `filename` パラメーターの先頭にスラッシュが付加されてしまいます。このリグレッションは、[`File.prototype.webkitRelativePath`](https://developer.mozilla.org/docs/Web/API/File/webkitRelativePath) プロパティの実装時に混入したもので、Firefox 50.1.0 で修正されました。
