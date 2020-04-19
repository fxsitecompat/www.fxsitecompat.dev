---
title: "JavaScript エラーメッセージの改善により従来の形式に依存していたコードに不具合が生じています"
date: "2018-09-22T14:42:00-04:00"
categories: ["javascript"]
tags: []
releases: ["63"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1259822"
      title: "Bug 1259822 - Improve the error message produced when a user attempts to access a property of [something that evaluated to] undefined."
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1488417"
      title: "Bug 1488417 - Even better error message on property access on undefined/null variable"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1490772"
      title: "Bug 1490772 - pro.beefree.io - blank page after 1259822 landed"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1498257"
      title: "Bug 1498257 - Infinite loop loading Flipkart.com because the site's regex fails to match Firefox's JS error message"
---
コンソール出力をウェブ開発者にとって分かりやすくする取り組みの一環として、`undefined` のプロパティへアクセスしようとした際に生成される JavaScript エラーメッセージが Firefox 63 と 64 で改善されました。例えば、

```js
window.x.y
// Firefox 62:
//// TypeError: window.x is undefined
// Firefox 63:
//// TypeError: window.x is undefined, can't access property "y" of it
// Firefox 64:
//// TypeError: window.x is undefined; can't access its "y" property
```

この変更は一見したところ無害に見えますが、ページが完全に空白になってしまう問題のあるサイトが報告されました。原因は、独自のエラー処理用に正規表現で JavaScript エラーメッセージを解析しているサイトのコードであることが、Mozilla の開発者によって特定されました。連絡を受けたウェブマスターは Firefox 63 の最終リリース前に問題を修正しました。

エラーメッセージの形式は ECMAScript 仕様で標準化されていないことから、ウェブ開発者はそれらをプログラム上で動的に使用することは避けるべきです。

**更新**: *Flipkart* がこの変更の影響を受けることが判明しています。

**更新 2** この変更は Firefox 63 Release Candidate 2 からバックアウトされました。
