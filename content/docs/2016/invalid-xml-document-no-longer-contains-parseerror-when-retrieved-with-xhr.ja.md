---
title: "不正な XML 文書を XHR で取得した際に `<parseerror>` が含まれなくなりました"
date: "2016-08-30T04:24:00-04:00"
categories: ["dom"]
tags: []
versions: ["51"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=289714"
      title: "Bug 289714 - Loaded-as-data XML documents should not generate <parsererror>"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/T5XmMus-aM0/discussion"
      title: "Intent to ship: XMLHttpRequest parsing errors will yield a null document for web content, not one with a <parsererror> root."
---
不正な XML 文書を読み込んだ際、Firefox は `<parseerror>` ノード内に描画された XML 解析エラーメッセージを含んだ黄色いページを表示します。Firefox 51 以降、[`XMLHttpRequest.responseXML`](https://developer.mozilla.org/ja/docs/Web/API/XMLHttpRequest/responseXML) プロパティは、そうした独自のエラー文書の代わりに `null` を返します。

文書を検証するには、`responseXML` の内容をチェックする代わりに「XML Parsing Error: not well-formed」という例外を監視すべきです。このエラーメッセージは Firefox 50 以前は単に「not well-formed」となっていました。
