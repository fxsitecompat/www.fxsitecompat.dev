---
title: "`Element.getElementsBy*()` が `HTMLCollection` を返すようになりました"
date: "2012-12-03T03:54:45-05:00"
categories: ["dom"]
tags: []
releases: ["19", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=799464"
      title: "Bug 799464 – Make Element.getElementsBy* return HTMLCollection"
---
[`getElementsByTagName`](https://developer.mozilla.org/docs/DOM/element.getElementsByTagName)、[`getElementsByTagNameNS`](https://developer.mozilla.org/docs/DOM/element.getElementsByTagNameNS)、[`getElementsByClassName`](https://developer.mozilla.org/docs/DOM/document.getElementsByClassName) の各メソッドで取得できる要素リストの種類が、DOM3 Core の仕様書で定義されている [`NodeList`](https://developer.mozilla.org/docs/DOM/NodeList) から DOM4 の仕様書ドラフトで定義されている [`HTMLCollection`](https://developer.mozilla.org/docs/DOM/HTMLCollection) に変わりました。
