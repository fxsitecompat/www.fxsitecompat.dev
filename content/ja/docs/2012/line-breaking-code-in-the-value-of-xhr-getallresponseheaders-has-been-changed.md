---
title: "`XHR.getAllResponseHeaders()` の値に含まれる改行コードが変わりました"
date: "2012-12-03T03:50:54-05:00"
categories: ["dom"]
tags: []
versions: ["17"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=730925"
      title: "Bug 730925 – XHR.getAllResponseHeaders should use CRLF, not LF per spec"
---
[`XMLHttpRequest`](https://developer.mozilla.org/ja/docs/DOM/XMLHttpRequest) の [`getAllResponseHeaders`](https://developer.mozilla.org/ja/docs/DOM/XMLHttpRequest#getAllResponseHeaders%28%29) 関数は、レスポンスヘッダを改行で分割した文字列として返します。Firefox の実装では改行コードが LF (`\n`) となっていましたが、仕様に合わせて CR+LF (`\r\n`) を使うよう修正されました。ヘッダ情報を読み取って何らかの処理をしている場合は注意が必要です。
