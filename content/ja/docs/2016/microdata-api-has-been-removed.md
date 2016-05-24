---
title: "Microdata API が削除されました"
date: "2016-05-24T09:20:00-04:00"
categories: ["dom"]
tags: []
versions: ["49"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=909633"
      title: "Bug 909633 - Remove HTML Microdata API"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=802548"
      title: "Bug 802548 - HTML5 microdata gives special meaning to itemId breaking some web content"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/tgXlkRhF6wo/discussion"
      title: "Intent to unship: HTML microdata API"
aliases:
    - "/docs/2015/microdata-api-will-be-removed-by-the-end-of-2015/"
---
[Microdata DOM API](http://www.w3.org/TR/microdata/) は Firefox 16 で実装されましたが、後に HTML5 仕様から削除され、今のところ他のどのブラウザにも実装されていません。主にその `itemId` プロパティに起因したさらなる [サイト互換性問題](https://www.fxsitecompat.com/ja/docs/2012/microdata-api-has-added-new-properties-to-elements/) を防ぐため、この廃止された API への対応は Firefox 49 で削除されました。前方互換性のため、Web 開発者には今後も、任意のプロパティの代わりに [`dataset`](https://developer.mozilla.org/ja/docs/Web/API/HTMLElement/dataset) プロパティを使うよう推奨します。
