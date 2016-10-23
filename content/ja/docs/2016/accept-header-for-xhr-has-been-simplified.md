---
title: "XHR 向け `Accept` ヘッダーが簡素化されました"
date: "2016-09-07T02:26:00-04:00"
categories: ["networking"]
tags: []
versions: ["51"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=918752"
      title: "Bug 918752 - [XHR2] Default Accept: header more complex than */*"
---
Firefox は従来、[`setRequestHeader`](https://developer.mozilla.org/ja/docs/Web/API/XMLHttpRequest/setRequestHeader) で開発者定義の値が与えられていない場合は、[`XMLHttpRequest.send`](https://developer.mozilla.org/ja/docs/Web/API/XMLHttpRequest/send) メソッド向け `Accept` HTTP ヘッダーの値として、`text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8` を送信していました。XMLHttpRequest Level 2 仕様に従い、Firefox 51 以降この既定値は `*/*` となります。
