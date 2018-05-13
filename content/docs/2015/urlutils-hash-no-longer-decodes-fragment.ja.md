---
title: "`URLUtils.hash` がフラグメントをデコードしなくなりました"
date: "2015-06-13T15:20:46-04:00"
categories: ["dom"]
tags: []
versions: ["41"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1093611"
      title: "Bug 1093611 – AnchorElement.hash should be the encoded version of the href attribute\'s fragment"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1184589"
      title: "Bug 1184589 - window.location.hash exposes spaces as %20"
---
`location.hash`、`HTMLAnchorElement.hash`、`URL.hash` などで使用できる [`URLUtils.hash`](https://developer.mozilla.org/docs/Web/API/URLUtils/hash) プロパティが、最新の仕様に従い、[`href`](https://developer.mozilla.org/docs/Web/API/URLUtils/href) プロパティで取得できる文字列と同様にパーセントエンコードされたフラグメントを返すようになりました。そのため、例えばスペースは `%20` となり、デコードされたフラグメントを得るには [`decodeURIComponent`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/decodeURIComponent) メソッドを使う必要があります ([例](https://github.com/mozilla/phonebook/commit/78619461421f1619d32d89b4eaca0c0fb49ef164))。この変更は元々 Firefox 38 で予定されていましたが、互換性問題のため延期されていました。この新しい挙動は Safari の現行版と同じになります。
